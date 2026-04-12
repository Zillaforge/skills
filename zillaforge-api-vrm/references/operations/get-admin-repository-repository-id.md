# GET /admin/repository/{repository-id}

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**取得指定的 repository**
**Operation ID:** `get--admin-repository-{repository-id}`

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[getRepositoryOutput](../schemas/getRepositoryOutput/getRepositoryOutput.md)

## Security

- **bearerAuth**
