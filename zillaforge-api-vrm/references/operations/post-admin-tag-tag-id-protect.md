# POST /admin/tag/{tag-id}/protect

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**設定保護指定的 tag (避免被刪除)**
**Operation ID:** `post--admin-tag-{tag-id}-protect`

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | (reference) |
| 401 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[updateTagOutput](../schemas/updateTagOutput/updateTagOutput.md)

## Security

- **bearerAuth**
