# POST /project/{project-id}/repository/{repository-id}/tag

**Resource:** [User/Tag](../resources/User-Tag.md)
**在 repository 創建 tag**
**Operation ID:** `post--project-{project-id}-repository-{repository-id}-tag`

## Request Body

**Content Types:** `application/json`

**Schema:** [createTagInput](../schemas/createTagInput/createTagInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[createTagOutput](../schemas/createTagOutput/createTagOutput.md)

## Security

- **bearerAuth**
