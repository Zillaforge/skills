---
name: zillaforge-api-iam
description: Pegasus IAM (Identity and Access Management) RESTful API documentation. Use this skill when you need to interact with the IAM service or look up API endpoints, request/response schemas, and parameters related to authentication (login/logout, MFA, SAML), authorization, users, projects (tenants), memberships (role assignments), permissions, CLI secrets, Personal Access API Tokens (PAAT), credentials, usage time, or account freezing. Load this skill to check IAM API contracts for both User and Admin operations. Responses are in JSON format, and each API requires account authentication using a Bearer Token.
metadata:
  api-version: "1.8.3"
  openapi-version: "3.0.0"
---

# Pegasus IAM RESTful API

Pegasus IAM (Identity and Access Management) RESTful API documentation. Covers authentication (login/logout, MFA, SAML), authorization, users, projects (tenants), memberships (roles), permissions, CLI secrets, Personal Access API Tokens (PAAT), credentials, usage time, and account freezing. Responses are in JSON format, and each API requires account authentication using a Bearer Token.

## How to Use This Skill

This API documentation is split into multiple files for on-demand loading.

**Directory structure:**
```
references/
├── resources/      # 25 resource index files
├── operations/     # 110 operation detail files
└── schemas/        # 20 schema groups, 93 schema files
```

**Navigation flow:**
1. Find the resource you need in the list below
2. Read `references/resources/<resource>.md` to see available operations
3. Read `references/operations/<operation>.md` for full details
4. If an operation references a schema, read `references/schemas/<prefix>/<schema>.md`

## Base URL

- `http://<HOST_IP>:<HOST_PORT>/iam/api/v1`

**Important Rule for API Execution:**
- Before calling or executing any API, you **MUST** refer to the Host Resolution Rules in the `zillaforge-api-guide` skill to obtain the correct `HOST_IP` and `HOST_PORT` for the testing environment.
- If you are only looking up API endpoints, schemas, or reading documentation without actually executing an API call, you do not need to look up the IP and Port.

## Authentication

Supported methods: **bearerAuth**. See `references/authentication.md` for details.

## Resources

- **Admin/Project** → `references/resources/Admin-Project.md` (10 ops) - Project API by Admin
- **Admin/User** → `references/resources/Admin-User.md` (9 ops) - User API by Admin
- **Admin/Membership** → `references/resources/Admin-Membership.md` (9 ops) - Membership API by Admin
- **User/Login** → `references/resources/User-Login.md` (8 ops) - Login API by User
- **User/Projects** → `references/resources/User-Projects.md` (8 ops) - Project API by User
- **User/Membership** → `references/resources/User-Membership.md` (8 ops) - Membership API by User
- **User/MFA** → `references/resources/User-MFA.md` (6 ops) - MFA API by User
- **User/Users** → `references/resources/User-Users.md` (5 ops) - User API by User
- **User/Permission** → `references/resources/User-Permission.md` (5 ops) - Permission API by TENANT_ADMIN
- **Admin/UsageTime** → `references/resources/Admin-UsageTime.md` (4 ops) - User and Project Usage Time API by Admin
- **Admin/CliSecret** → `references/resources/Admin-CliSecret.md` (4 ops) - CliSecret API by Admin
- **Admin/Permission** → `references/resources/Admin-Permission.md` (4 ops) - Permission API by Admin
- **User/PersonalAccessAPIToken** → `references/resources/User-PersonalAccessAPIToken.md` (3 ops) - Personal Access API Token
- **User/SAML** → `references/resources/User-SAML.md` (3 ops) - SAML API by User
- **Admin/Login** → `references/resources/Admin-Login.md` (3 ops) - Login API by Admin
- **Admin/PersonalAccessAPIToken** → `references/resources/Admin-PersonalAccessAPIToken.md` (3 ops) - Personal Access API Token
- **Admin/Frozen** → `references/resources/Admin-Frozen.md` (3 ops) - Frozen API by Admin
- **Admin/SAML** → `references/resources/Admin-SAML.md` (3 ops) - SAML API by Admin
- **User/Credentials** → `references/resources/User-Credentials.md` (2 ops) - Credential API by User
- **User/CliSecret** → `references/resources/User-CliSecret.md` (2 ops) - CliSecret API by User
- **Admin/Credential** → `references/resources/Admin-Credential.md` (2 ops) - Credential API by Admin
- **Admin/SecurityGuard** → `references/resources/Admin-SecurityGuard.md` (2 ops) - SecurityGuard API by Admin
- **Admin/System** → `references/resources/Admin-System.md` (2 ops) - Get system information
- **Admin/Action** → `references/resources/Admin-Action.md` (1 ops) - Action API by Admin
- **Admin/MFA** → `references/resources/Admin-MFA.md` (1 ops) - MFA API by Admin
