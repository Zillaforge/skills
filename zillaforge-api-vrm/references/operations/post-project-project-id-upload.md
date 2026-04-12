# POST /project/{project-id}/upload

**Resource:** [User/Image](../resources/User-Image.md)
**上傳 Image**
**Operation ID:** `post--project-{project-id}-upload`

## Request Body

**Content Types:** `application/json`, `application/json/repositoryId`, `application/json/tagId`

**Schema:** [uploadImageInput](../schemas/uploadImageInput/uploadImageInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[uploadImageOutput](../schemas/uploadImageOutput/uploadImageOutput.md)

## Security

- **bearerAuth**
