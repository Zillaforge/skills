# POST /admin/repository

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**創建 repository**
**Operation ID:** `post--admin-repository`

## Request Body

**Content Types:** `application/json`

**Schema:** [createRepositoryInput.admin](../schemas/createRepositoryInput-admin/createRepositoryInput-admin.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[createRepositoryOutput](../schemas/createRepositoryOutput/createRepositoryOutput.md)

## Security

- **bearerAuth**
