# DELETE /project/:{project-id}/tag/:{tag-id}/share

**Resource:** [User/ProjectAcl](../resources/User-ProjectAcl.md)
**指定的 tag 停止分享給其他成員使用**
**Operation ID:** `delete--project-:{project-id}-tag-:{tag-id}-share`

Delete project access control list entry for a specific tag and project

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `tag-id` | path | string | Yes | Tag ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal Server Error |

