# POST /project/{project-id}/tag/{tag-id}/share

**Resource:** [User/ProjectAcl](../resources/User-ProjectAcl.md)
**在指定的 tag 創建 project-acl 分享給其他成員使用**
**Operation ID:** `post--project-{project-id}-tag-{tag-id}-share`

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
