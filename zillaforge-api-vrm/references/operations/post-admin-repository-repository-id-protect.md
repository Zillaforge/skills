# POST /admin/repository/{repository-id}/protect

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**設定保護指定的 repository (避免被刪除)**
**Operation ID:** `post--admin-repository-{repository-id}-protect`

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | (reference) |
| 401 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[updateRepositoryOutput](../schemas/updateRepositoryOutput/updateRepositoryOutput.md)

## Security

- **bearerAuth**
