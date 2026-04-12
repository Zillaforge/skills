# PUT /project/{project-id}/repository/{repository-id}

**Resource:** [User/Repository](../resources/User-Repository.md)
**更新指定的 repository**
**Operation ID:** `put--project-{project-id}-repository-{repository-id}`

## Request Body

**Content Types:** `application/json`

**Schema:** [updateRepositoryInput](../schemas/updateRepositoryInput/updateRepositoryInput.md)

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
