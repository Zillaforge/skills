# GET /project/{project-id}/exports

**Resource:** [User/Export](../resources/User-Export.md)
**列出所有的匯出資訊**
**Operation ID:** `get--project-{project-id}-exports`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `where` | query | string[] | No | 此功能可以帶入欄位及值作為查詢條件，來篩選出滿足條件的清單。支援的欄位：repository-id, tag-id, status
 |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[listExportsOutput](../schemas/listExportsOutput/listExportsOutput.md)

## Security

- **bearerAuth**
