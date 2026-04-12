# GET /project/{project-id}/repository/{repository-id}/tags

**Resource:** [User/Tag](../resources/User-Tag.md)
**取得此 repository 的所有 tags**
**Operation ID:** `get--project-{project-id}-repository-{repository-id}-tags`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `where` | query | string[] | No | 此功能可以帶入欄位及值作為查詢條件，來篩選出滿足條件的清單。支援的欄位：status, type
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
