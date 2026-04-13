# GET /admin/repository/:{repository-id}

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**取得指定的 repository**
**Operation ID:** `get--admin-repository-:{repository-id}`

Get detailed information about a specific repository

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `repository-id` | path | string | Yes | Repository ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.GetRepositoryOutput](../schemas/admin-GetRepositoryOutput/admin-GetRepositoryOutput.md)

