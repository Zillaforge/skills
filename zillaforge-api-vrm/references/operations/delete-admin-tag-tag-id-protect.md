# DELETE /admin/tag/:{tag-id}/protect

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**解除保護指定的 tag**
**Operation ID:** `delete--admin-tag-:{tag-id}-protect`

Unset a tag as protected to allow deletion

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `tag-id` | path | string | Yes | Tag ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.UnsetTagProtectOutput](../schemas/admin-UnsetTagProtectOutput/admin-UnsetTagProtectOutput.md)

