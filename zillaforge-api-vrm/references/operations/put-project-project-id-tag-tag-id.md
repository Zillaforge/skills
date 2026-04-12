# PUT /project/{project-id}/tag/{tag-id}

**Resource:** [User/Tag](../resources/User-Tag.md)
**更新指定的 tag**
**Operation ID:** `put--project-{project-id}-tag-{tag-id}`

## Request Body

**Content Types:** `application/json`

**Schema:** [updateTagInput](../schemas/updateTagInput/updateTagInput.md)

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

[updateTagOutput](../schemas/updateTagOutput/updateTagOutput.md)

## Security

- **bearerAuth**
