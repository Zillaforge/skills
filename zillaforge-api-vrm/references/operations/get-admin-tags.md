# GET /admin/tags

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**取得所有 tags**
**Operation ID:** `get--admin-tags`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `where` | query | string[] | No | 此功能可以帶入欄位及值作為查詢條件，來篩選出滿足條件的清單。支援的欄位：status, type, repository-id, project-id
 |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[listTagsOutput](../schemas/listTagsOutput/listTagsOutput.md)

## Security

- **bearerAuth**
