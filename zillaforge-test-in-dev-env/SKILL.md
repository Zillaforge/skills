---
name: zillaforge-test-in-dev-env
description: Validate features in the docker-compose dev environment which includes ZillaForge micro services. Use when testing API functionality, verifying feature correctness, troubleshooting startup errors, or debugging integration issues between micro services and OpenStack in the local dev environment. Covers environment lifecycle, API testing with correct authorization, OpenStack configuration adjustments, and error resolution workflow.
argument-hint: Describe the feature or API flow you want to test
---

# ZillaForge Dev Environment Testing

## When to Use
- Verifying a new feature works end-to-end in the docker-compose environment
- Testing API flows using accounts
- Troubleshooting service startup errors or OpenStack integration issues
- Validating that code changes work correctly before committing
- Running through a multi-step API scenario (e.g., create project → add member → create resource)

## Environment Overview

- The project runs inside a **devcontainer**. The test environment is composed of multiple docker-compose stacks:

   | Stack | Start Command | Stop Command |
   |-------|--------------|--------------|
   | Persistent (container for setup volume or network) | `make start-dev-persistent` | `make clean-dev-persistent` |
   | System (DB, Redis, etc.) | `make start-dev-system` | `make stop-dev-system` |
   | Service (IAM、VPS、VRM, etc.) | `make start-dev-service` | `make stop-dev-service` |

- Not all test scenarios involve an external OpenStack. If an external OpenStack is present:
  - It is deployed via `kolla-ansible`. On the bastion node, there is a container where `kolla-ansible` commands are executed to deploy and manage OpenStack.
  - It can be accessed via the `openstack` CLI. Before executing any `openstack` commands, authentication is performed via environment variables (such as `OS_AUTH_URL`, `OS_USERNAME`, `OS_PASSWORD`, etc.). You must verify that these environment variables are already set in your terminal session.
  - Alternatively, you can connect to the OpenStack's bastion node via SSH using the `$CLOUD_USER` and `$BASTION_IP` environment variables and enter the `kolla-ansible` container to debug OpenStack.

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

> **Important**: Before executing a login or any API calls, always consult the `zillaforge-api-guide` skill for the correct endpoints, parameters, and expected responses.

1. Obtain an IAM token by calling the login endpoint with the appropriate account.
2. Use the token in the `Authorization` header for subsequent API calls.
3. Execute each step of the scenario in sequence, verifying the response at each step.
4. For scenarios involving OpenStack resources (security groups, volumes, snapshots), confirm the resource exists in OpenStack after creation via the zillaforge micro serive's API.

### Phase 3 — Troubleshoot Errors

When an API call or service startup fails, follow this resolution workflow:

#### 3a. Identify the Root Cause
- Check service logs for error messages and stack traces.
- Check if the error is a **configuration mismatch** (service configuration and OpenStack), a **code bug**.
- **Do NOT directly modify data in the docker-compose DB** to fix issues.

#### 3b. Configuration Issues
Configuration issues may stem from **service config** or **OpenStack config**.

- **Service Config**: Config files live in `docker-compose/etc/*.yaml`, where each service has its own configuration in YAML format. After adjusting service config, restart the service stack:
  ```bash
  make stop-dev-service; make start-dev-service
  ```
- **OpenStack Config**:
  - If adjusting OpenStack settings without modifying config files, use the `openstack` CLI directly.
  - If modifying OpenStack deployment config files, reconfigure it via the bastion's kolla-ansible container:
    ```bash
    ssh $CLOUD_USER@$BASTION_IP
    # Inside bastion, enter the kolla-ansible container to perform reconfiguration
    docker exec -it <kolla_container> bash
    ```

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


### Phase 4 — Verify OpenStack Side Effects

For resources that should be reflected in OpenStack (such as security groups, volumes, snapshots):


### Phase 5 — Document the Results

After a successful test run, produce a **Step-by-Step API guide** that includes:
- Prerequisites (environment up, accounts)
- Each API call: method, URL, headers, request body, expected response. **The documented API calls MUST be formatted as a `.rest` file, referring to `examples/example.rest` for the correct syntax (e.g., using variables like `@IAM_ENDPOINT`, delimiters `###`, and named requests `# @name`).**
- Verification steps for side effects (OpenStack resource existence)

## Key Constraints

- **Never modify the docker-compose DB directly** (no manual SQL inserts/updates to fix issues).
- Always fix problems through config changes or code fixes, then restart the environment.
- OpenStack adjustments go through the bastion kolla-ansible container.
- The bastion IP and openstack connection information vary per environment — confirm before use.

## Quick Reference

| Task | Command / Location |
|------|--------------------|
| Start full env | `make start-dev-persistent; make start-dev-system; make start-dev-service` |
| Stop full env | `make stop-dev-service; make stop-dev-system; make clean-dev-persistent` |
| service config | `docker-compose/etc/*.yaml` |
| Rebuild image | `make RELEASE_MODE=prod release-image` (check `Makefile` for exact target) |
| API document | refer `zillaforge-api-guide` skill |
