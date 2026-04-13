# DELETE /admin/projectacl/:{project-acl-id}

**Resource:** [Admin/ProjectAcl](../resources/Admin-ProjectAcl.md)
**指定的 tag 停止分享給其他成員使用**
**Operation ID:** `delete--admin-projectacl-:{project-acl-id}`

Delete a specific project ACL by ID or remove project ACL from a tag

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-acl-id` | path | string | Yes | Project ACL ID (when deleting specific ACL) |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

