# POST /admin/tag/:{tag-id}/protect

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**設定保護指定的 tag (避免被刪除)**
**Operation ID:** `post--admin-tag-:{tag-id}-protect`

Set a tag as protected to prevent deletion

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `tag-id` | path | string | Yes | Tag ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.SetTagProtectOutput](../schemas/admin-SetTagProtectOutput/admin-SetTagProtectOutput.md)

