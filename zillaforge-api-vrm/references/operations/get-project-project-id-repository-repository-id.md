# GET /project/{project-id}/repository/{repository-id}

**Resource:** [User/Repository](../resources/User-Repository.md)
**取得指定的 repository**
**Operation ID:** `get--project-{project-id}-repository-{repository-id}`

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
