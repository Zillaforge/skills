# POST /project/:{project-id}/tag/:{tag-id}/share

**Resource:** [User/ProjectAcl](../resources/User-ProjectAcl.md)
**在指定的 tag 創建 project-acl 分享給其他成員使用**
**Operation ID:** `post--project-:{project-id}-tag-:{tag-id}-share`

Create a new project ACL for the specified tag and project

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `tag-id` | path | string | Yes | Tag ID |

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal Server Error |

**Success Response Schema:**

[user.CreateProjectAclOutput](../schemas/user-CreateProjectAclOutput/user-CreateProjectAclOutput.md)

