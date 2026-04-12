---
name: zillaforge-api-vrm
description: Virtual Registry Management (VRM) RESTful API documentation. Use this skill when you need to interact with the VRM service or look up API endpoints, request/response schemas, and parameters related to repositories, tags, images, snapshots, project ACLs, member ACLs, or export/import/upload operations. Load this skill to check VRM API contracts for both Admin and User (Project) operations. Responses are in JSON format, and each API requires account authentication using a Bearer token.
license: Apache 2.0 (http://www.apache.org/licenses/LICENSE-2.0.html)
metadata:
  api-version: "1.0.0"
  openapi-version: "3.0.0"
  contact: "osci_admin@asus.com"
---

# Virtual Registry Management RESTful API

Virtual Registry Management (VRM) RESTful API documentation. Covers repositories, tags, images, snapshots, project ACLs, member ACLs, and export/import/upload operations. Responses are in JSON format, and each API requires account authentication using a Bearer token.

## How to Use This Skill

This API documentation is split into multiple files for on-demand loading.

**Directory structure:**
```
references/
├── resources/      # 16 resource index files
├── operations/     # 56 operation detail files
└── schemas/        # 55 schema groups, 55 schema files
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

- **Admin/Repository** → `references/resources/Admin-Repository.md` (8 ops) - Repository RESTful APIs
- **Admin/Tag** → `references/resources/Admin-Tag.md` (7 ops) - Tag RESTful APIs
- **User/Tag** → `references/resources/User-Tag.md` (6 ops) - Tag RESTful APIs
- **User/Repository** → `references/resources/User-Repository.md` (5 ops) - Repository RESTful APIs
- **Admin/ProjectAcl** → `references/resources/Admin-ProjectAcl.md` (5 ops) - ProjectAcl RESTful APIs
- **User/MemberAcl** → `references/resources/User-MemberAcl.md` (4 ops) - MemberAcl RESTful APIs
- **User/Export** → `references/resources/User-Export.md` (3 ops) - Export RESTful APIs
- **Admin/Image** → `references/resources/Admin-Image.md` (3 ops) - Image RESTful APIs
- **Admin/Export** → `references/resources/Admin-Export.md` (3 ops) - Export RESTful APIs
- **Admin/MemberAcl** → `references/resources/Admin-MemberAcl.md` (3 ops) - MemberAcl RESTful APIs
- **User/Image** → `references/resources/User-Image.md` (2 ops) - Image RESTful APIs
- **User/ProjectAcl** → `references/resources/User-ProjectAcl.md` (2 ops) - ProjectAcl RESTful APIs
- **Admin/Project** → `references/resources/Admin-Project.md` (2 ops) - Project RESTful APIs
- **User/Project** → `references/resources/User-Project.md` (1 ops) - Project RESTful APIs
- **User/Snapshot** → `references/resources/User-Snapshot.md` (1 ops) - Snapshot RESTful APIs
- **Admin/Snapshot** → `references/resources/Admin-Snapshot.md` (1 ops) - Snapshot RESTful APIs
