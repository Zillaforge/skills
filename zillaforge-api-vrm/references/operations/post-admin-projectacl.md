# POST /admin/projectacl

**Resource:** [Admin/ProjectAcl](../resources/Admin-ProjectAcl.md)
**在指定的 tag 創建 project-acl 分享給所有人**
**Operation ID:** `post--admin-projectacl`

## Request Body

**Content Types:** `application/json`

**Schema:** [createProjectAclInput](../schemas/createProjectAclInput/createProjectAclInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[createProjectAclOutput](../schemas/createProjectAclOutput/createProjectAclOutput.md)

## Security

- **bearerAuth**
