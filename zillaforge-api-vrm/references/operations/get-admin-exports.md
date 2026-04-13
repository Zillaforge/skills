# GET /admin/exports

**Resource:** [Admin/Export](../resources/Admin-Export.md)
**列出所有的匯出資訊**
**Operation ID:** `get--admin-exports`

Get a paginated list of exports with optional filtering

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `limit` | query | integer | No | Number of items to return |
| `offset` | query | integer | No | Number of items to skip |
| `where` | query | string[] | No | Filter conditions |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 500 | Internal server error |

**Success Response Schema:**

[admin.ListExportsOutput](../schemas/admin-ListExportsOutput/admin-ListExportsOutput.md)

