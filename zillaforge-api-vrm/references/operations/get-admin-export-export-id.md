# GET /admin/export/:{export-id}

**Resource:** [Admin/Export](../resources/Admin-Export.md)
**取得指定的匯出資訊**
**Operation ID:** `get--admin-export-:{export-id}`

Retrieve export details by export ID

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `export-id` | path | string | Yes | Export ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.GetExportOutput](../schemas/admin-GetExportOutput/admin-GetExportOutput.md)

