# DELETE /admin/tag/:{tag-id}

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**棄用指定的 tag**
**Operation ID:** `delete--admin-tag-:{tag-id}`

Delete a specific tag (if not protected)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `tag-id` | path | string | Yes | Tag ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

