---
name: zillaforge-test-in-dev-env
description: 'Validate features in the docker-compose dev environment for ZillaForge service project. Use when testing API functionality, verifying feature correctness, troubleshooting startup errors, or debugging integration issues between VPS and OpenStack in the local dev environment. Covers environment lifecycle, API testing via IAM credentials, OpenStack configuration adjustments, and error resolution workflow.'
argument-hint: 'Describe the feature or API flow you want to test'
---

# ZillaForge Dev Environment Testing

## When to Use
- Verifying a new feature works end-to-end in the docker-compose environment
- Testing API flows using IAM accounts
- Troubleshooting VPS startup errors or OpenStack integration issues
- Validating that code changes work correctly before committing
- Running through a multi-step API scenario (e.g., create project → add member → create resource)

## Environment Overview

The project runs inside a **devcontainer**. The test environment is composed of multiple docker-compose stacks:

| Stack | Start Command | Stop Command |
|-------|--------------|--------------|
| Persistent (DB, Redis) | `make start-dev-persistent` | `make clean-dev-persistent` |
| System (IAM, etc.) | `make start-dev-system` | `make stop-dev-system` |
| Service (VPS) | `make start-dev-service` | `make stop-dev-service` |

External OpenStack is accessed via `clouds.yaml` in the workspace root, or via bastion SSH.

## Default IAM Accounts

| Account | Password | Role |
|---------|----------|------|
| `admin@ci.asus.com` | `admin` | Admin |
| `system@ci.asus.com` | `system` | System |

## Procedure

### Phase 1 — Start the Environment

```bash
make start-dev-persistent; make start-dev-system; make start-dev-service
```

Wait for all services to be healthy before proceeding. Check logs if any container fails to start:

```bash
docker-compose -f docker-compose/<stack>/docker-compose.yml logs --tail=50 <service>
```

### Phase 2 — Run the API Test Scenario

1. Obtain an IAM token by calling the login endpoint with the appropriate account.
2. Use the token in the `Authorization` header for subsequent VPS API calls.
3. Execute each step of the scenario in sequence, verifying the response at each step.
4. For scenarios involving OpenStack resources (security groups, volumes, snapshots), confirm the resource exists in OpenStack after creation via the VPS API.

### Phase 3 — Troubleshoot Errors

When an API call or service startup fails, follow this resolution workflow:

#### 3a. Identify the Root Cause
- Check VPS service logs for error messages and stack traces.
- Check if the error is a **configuration mismatch** (VPS config vs OpenStack), a **code bug**, or a **DB schema issue**.
- **Do NOT directly modify data in the docker-compose DB** to fix issues.

#### 3b. Configuration Issues
- config files live in `docker-compose/etc/*.yaml`, each service has is's own configuration in yaml format.
- OpenStack config is adjusted via the bastion kolla-ansible container:
  ```bash
  ssh cloud-user@<BASTION_IP>
  # Inside bastion, enter the kolla-ansible container
  docker exec -it <kolla_container> bash
  ```
- After adjusting config, restart only the affected service stack (no need to restart persistent stack).

#### 3c. Code Bugs
1. Identify the relevant source file from the error trace.
2. Fix the code.
3. Rebuild the image:
   ```bash
   make RELEASE_MODE=prod release-image
   ```
4. Restart the full environment:
   ```bash
   make stop-dev-service; make stop-dev-system; make clean-dev-persistent
   make start-dev-persistent; make start-dev-system; make start-dev-service
   ```
5. Re-run the test scenario from Phase 2.

#### 3d. DB Schema Issues (e.g., foreign key errors on startup)
- Investigate the migration files under `storages/versions/` or `storages/mariadb/`.
- Fix the migration/schema definition in code, then rebuild and restart (see 3c).
- Never patch the live DB directly.

### Phase 4 — Verify OpenStack Side Effects

For resources that should be reflected in OpenStack (security groups, volumes, snapshots):

```bash
# From devcontainer, using clouds.yaml
openstack --os-cloud <cloud_name> security group list --project <project_id>
openstack --os-cloud <cloud_name> volume list --project <project_id>
```

Or SSH to bastion and run equivalent commands inside the kolla-ansible container.

### Phase 5 — Document the Results

After a successful test run, produce a **Step-by-Step API guide** that includes:
- Prerequisites (environment up, accounts)
- Each API call: method, URL, headers, request body, expected response
- Verification steps for side effects (OpenStack resource existence)

## Key Constraints

- **Never modify the docker-compose DB directly** (no manual SQL inserts/updates to fix issues).
- Always fix problems through config changes or code fixes, then restart the environment.
- OpenStack adjustments go through the bastion kolla-ansible container.
- The bastion IP and `clouds.yaml` cloud name vary per environment — confirm before use.

## Quick Reference

| Task | Command / Location |
|------|--------------------|
| Start full env | `make start-dev-persistent; make start-dev-system; make start-dev-service` |
| Stop full env | `make stop-dev-service; make stop-dev-system; make clean-dev-persistent` |
| VPS config | `docker-compose/etc/*.yaml` |
| DB migrations | `storages/versions/`, `storages/mariadb/` |
| OpenStack access | `clouds.yaml` or `ssh cloud-user@<BASTION_IP>` |
| Rebuild image | `make RELEASE_MODE=prod release-image` (check `Makefile` for exact target) |
| API document | refer `zillaforge-api-doc` skill |
