# GET /admin/repositories

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**列出所有的 repositories**
**Operation ID:** `get--admin-repositories`

Get a paginated list of repositories with optional filtering

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `limit` | query | integer | No | Limit number of results |
| `offset` | query | integer | No | Offset for pagination |
| `where` | query | string[] | No | Filter conditions |
| `namespace` | query | string | No | Filter by namespace |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 500 | Internal server error |

**Success Response Schema:**

[admin.ListRepositoriesOutput](../schemas/admin-ListRepositoriesOutput/admin-ListRepositoriesOutput.md)

