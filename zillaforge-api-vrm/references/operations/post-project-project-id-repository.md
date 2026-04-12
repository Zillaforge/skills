# POST /project/{project-id}/repository

**Resource:** [User/Repository](../resources/User-Repository.md)
**創建 repository**
**Operation ID:** `post--project-{project-id}-repository`

## Request Body

**Content Types:** `application/json`

**Schema:** [createRepositoryInput](../schemas/createRepositoryInput/createRepositoryInput.md)

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
