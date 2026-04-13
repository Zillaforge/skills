# POST /admin/repository

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**創建 repository**
**Operation ID:** `post--admin-repository`

Create a new repository with administrative privileges

## Request Body

Repository creation payload

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.CreateRepositoryInput](../schemas/admin-CreateRepositoryInput/admin-CreateRepositoryInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.CreateRepositoryOutput](../schemas/admin-CreateRepositoryOutput/admin-CreateRepositoryOutput.md)

