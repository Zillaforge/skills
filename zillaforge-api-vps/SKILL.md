---
name: zillaforge-api-vps
description: Virtual Platform Service (VPS) RESTful API documentation. Use this skill when you need to interact with the VPS service or look up API endpoints, request/response schemas, and parameters related to servers (instances), volumes, networks, routers, floating IPs, loadbalancers, auto scale groups (ASG), security groups, keypairs, shares, snapshots, flavors, or quotas. Load this skill to check VPS API contracts for both Project and Admin operations. Responses are in JSON format, and each API requires account authentication using an ApiKeyAuth token.
metadata:
  api-version: "0.4.24"
  openapi-version: "3.0.1"
---

# Virtual Platform Service RESTful API

Virtual Platform Service (VPS) RESTful API documentation. Covers operations for managing cloud infrastructure including servers (instances), volumes, networks, routers, floating IPs, loadbalancers, auto scale groups (ASG), security groups, keypairs, shares, snapshots, flavors, and quotas. Responses are in JSON format, and each API requires account authentication using an ApiKeyAuth token.

## How to Use This Skill

This API documentation is split into multiple files for on-demand loading.

**Directory structure:**
```
references/
├── resources/      # 34 resource index files
├── operations/     # 182 operation detail files
└── schemas/        # 134 schema groups, 135 schema files
```

**Navigation flow:**
1. Find the resource you need in the list below
2. Read `references/resources/<resource>.md` to see available operations
3. Read `references/operations/<operation>.md` for full details
4. If an operation references a schema, read `references/schemas/<prefix>/<schema>.md`

## Base URL

- `http://<HOST_IP>:<HOST_PORT>`

**Important Rule for API Execution:**
- Before calling or executing any API, you **MUST** refer to the Host Resolution Rules in the `zillaforge-api-guide` skill to obtain the correct `HOST_IP` and `HOST_PORT` for the testing environment.
- If you are only looking up API endpoints, schemas, or reading documentation without actually executing an API call, you do not need to look up the IP and Port.

## Authentication

Supported methods: **ApiKeyAuth**. See `references/authentication.md` for details.

## Resources

- **loadbalancer** → `references/resources/loadbalancer.md` (19 ops)
- **server** → `references/resources/server.md` (16 ops)
- **system_extnet** → `references/resources/system-extnet.md` (13 ops)
- **auto_scale_group** → `references/resources/auto-scale-group.md` (12 ops)
- **system_net_qos** → `references/resources/system-net-qos.md` (9 ops)
- **system_provider_network** → `references/resources/system-provider-network.md` (9 ops)
- **router** → `references/resources/router.md` (9 ops)
- **floating_ip** → `references/resources/floating-ip.md` (8 ops)
- **share** → `references/resources/share.md` (8 ops)
- **security_group** → `references/resources/security-group.md` (7 ops)
- **system_voltype** → `references/resources/system-voltype.md` (6 ops)
- **network** → `references/resources/network.md` (6 ops)
- **volumes** → `references/resources/volumes.md` (6 ops)
- **system_flavor** → `references/resources/system-flavor.md` (5 ops)
- **system_quota** → `references/resources/system-quota.md` (5 ops)
- **keypair** → `references/resources/keypair.md` (5 ops)
- **snapshots** → `references/resources/snapshots.md` (5 ops)
- **snapshot-schedules** → `references/resources/snapshot-schedules.md` (5 ops)
- **system_fip** → `references/resources/system-fip.md` (3 ops)
- **system_network** → `references/resources/system-network.md` (3 ops)
- **volume_types** → `references/resources/volume-types.md` (3 ops)
- **system_asg** → `references/resources/system-asg.md` (2 ops)
- **system_loadbalancer** → `references/resources/system-loadbalancer.md` (2 ops)
- **system_server** → `references/resources/system-server.md` (2 ops)
- **system_share** → `references/resources/system-share.md` (2 ops)
- **system_action** → `references/resources/system-action.md` (2 ops)
- **system_volume** → `references/resources/system-volume.md` (2 ops)
- **flavor** → `references/resources/flavor.md` (2 ops)
- **system_az** → `references/resources/system-az.md` (1 ops)
- **system_gpu_model** → `references/resources/system-gpu-model.md` (1 ops)
- **system_opsk** → `references/resources/system-opsk.md` (1 ops)
- **root_features** → `references/resources/root-features.md` (1 ops)
- **quota** → `references/resources/quota.md` (1 ops)
- **root_version** → `references/resources/root-version.md` (1 ops)
