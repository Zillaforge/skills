# DELETE /admin/repository/{repository-id}/protect

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**解除保護指定的 repository**
**Operation ID:** `delete--admin-repository-{repository-id}-protect`

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[updateRepositoryOutput](../schemas/updateRepositoryOutput/updateRepositoryOutput.md)

## Security

- **bearerAuth**
