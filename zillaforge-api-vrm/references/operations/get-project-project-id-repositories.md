# GET /project/:{project-id}/repositories

**Resource:** [User/Repository](../resources/User-Repository.md)
**列出所有的 repositories**
**Operation ID:** `get--project-:{project-id}-repositories`

Get a list of repositories with pagination and filtering

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `limit` | query | integer | No | Number of items to return, -1表示全部顯示 (default: 100) |
| `offset` | query | integer | No | Number of items to skip (default: 0) |
| `where` | query | string[] | No | Filter conditions, 此功能可以帶入欄位及值作為查詢條件，來篩選出滿足條件的清單 |

## Responses

| Status | Description |
|--------|-------------|
| 200 | List of repositories |
| 403 | Forbidden |
| 500 | Internal server error |

**Success Response Schema:**

[user.ListRepositoriesOutput](../schemas/user-ListRepositoriesOutput/user-ListRepositoriesOutput.md)

