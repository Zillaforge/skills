# GET /project/{project-id}/export/{export-id}

**Resource:** [User/Export](../resources/User-Export.md)
**取得指定匯出資訊**
**Operation ID:** `get--project-{project-id}-export-{export-id}`

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[getExportOutput](../schemas/getExportOutput/getExportOutput.md)

## Security

- **bearerAuth**
