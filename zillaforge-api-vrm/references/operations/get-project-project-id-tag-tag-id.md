# GET /project/{project-id}/tag/{tag-id}

**Resource:** [User/Tag](../resources/User-Tag.md)
**取得指定的 tag**
**Operation ID:** `get--project-{project-id}-tag-{tag-id}`

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[getTagOutput](../schemas/getTagOutput/getTagOutput.md)

## Security

- **bearerAuth**
