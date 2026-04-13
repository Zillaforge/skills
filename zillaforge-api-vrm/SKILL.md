---
name: zillaforge-api-vrm
description: Virtual Registry Management (VRM) RESTful API documentation. Use this skill when you need to interact with the VRM service or look up API endpoints, request/response schemas, and parameters related to repositories, tags, images, snapshots, project ACLs, member ACLs, or export/import/upload operations. Load this skill to check VRM API contracts for both Admin and User (Project) operations. Responses are in JSON format, and each API requires account authentication using a Bearer token.
metadata:
  api-version: "0.1.11"
  openapi-version: "3.0.0"
---

# Virtual Registry Management RESTful API

Virtual Registry Management (VRM) RESTful API documentation. Covers repositories, tags, images, snapshots, project ACLs, member ACLs, and export/import/upload operations. Responses are in JSON format, and each API requires account authentication using a Bearer token.

## How to Use This Skill

This API documentation is split into multiple files for on-demand loading.

**Directory structure:**
```
references/
├── resources/      # 16 resource index files
├── operations/     # 59 operation detail files
└── schemas/        # 88 schema groups, 88 schema files
```

**Navigation flow:**
1. Find the resource you need in the list below
2. Read `references/resources/<resource>.md` to see available operations
3. Read `references/operations/<operation>.md` for full details
4. If an operation references a schema, read `references/schemas/<prefix>/<schema>.md`

## Base URL

- `http://<HOST_IP>:<HOST_PORT>/vrm/api/v1`

**Important Rule for API Execution:**
- Before calling or executing any API, you **MUST** refer to the Host Resolution Rules in the `zillaforge-api-guide` skill to obtain the correct `HOST_IP` and `HOST_PORT` for the testing environment.
- If you are only looking up API endpoints, schemas, or reading documentation without actually executing an API call, you do not need to look up the IP and Port.

## Authentication

Supported methods: **bearerAuth**. See `references/authentication.md` for details.

## Resources

- **User/Tag** → `references/resources/User-Tag.md` (8 ops)
- **Admin/Repository** → `references/resources/Admin-Repository.md` (7 ops)
- **Admin/Tag** → `references/resources/Admin-Tag.md` (7 ops)
- **Admin/ProjectAcl** → `references/resources/Admin-ProjectAcl.md` (5 ops)
- **User/Repository** → `references/resources/User-Repository.md` (5 ops)
- **User/MemberAcl** → `references/resources/User-MemberAcl.md` (4 ops)
- **Admin/Export** → `references/resources/Admin-Export.md` (3 ops)
- **Admin/Image** → `references/resources/Admin-Image.md` (3 ops)
- **Admin/MemberAcl** → `references/resources/Admin-MemberAcl.md` (3 ops)
- **Admin/Project** → `references/resources/Admin-Project.md` (3 ops)
- **User/Exports** → `references/resources/User-Exports.md` (3 ops)
- **User/Snapshot** → `references/resources/User-Snapshot.md` (2 ops)
- **User/Image** → `references/resources/User-Image.md` (2 ops)
- **User/ProjectAcl** → `references/resources/User-ProjectAcl.md` (2 ops)
- **Admin/Snapshot** → `references/resources/Admin-Snapshot.md` (1 ops)
- **User/Project** → `references/resources/User-Project.md` (1 ops)
