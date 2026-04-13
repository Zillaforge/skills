# DELETE /project/:{project-id}/tag/:{tag-id}

**Resource:** [User/Tag](../resources/User-Tag.md)
**棄用指定的 tag**
**Operation ID:** `delete--project-:{project-id}-tag-:{tag-id}`

Delete a tag by ID. Only creator, tenant owner, or tenant admin can delete tags. Protected tags cannot be deleted.

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
| 500 | Internal server error |

