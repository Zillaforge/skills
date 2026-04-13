# DELETE /admin/export/:{export-id}

**Resource:** [Admin/Export](../resources/Admin-Export.md)
**刪除指定的匯出紀錄**
**Operation ID:** `delete--admin-export-:{export-id}`

Delete an export record by its ID

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `export-id` | path | string | Yes | Export ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal server error |

