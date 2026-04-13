# GET /project/:{project-id}/exports

**Resource:** [User/Exports](../resources/User-Exports.md)
**列出所有的匯出資訊**
**Operation ID:** `get--project-:{project-id}-exports`

Get a list of exports with pagination and filtering

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `limit` | query | integer | No | Limit number of results, -1表示全部顯示 |
| `offset` | query | integer | No | Offset for pagination, 從第幾筆開始取得 |
| `where` | query | string[] | No | Filter conditions, 此功能可以帶入欄位及值作為查詢條件，來篩選出滿足條件的清單 |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successfully retrieved exports list |
| 403 | Forbidden |
| 500 | Internal server error |

**Success Response Schema:**

[user.ListExportsOutput](../schemas/user-ListExportsOutput/user-ListExportsOutput.md)

