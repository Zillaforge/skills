# POST /admin/upload

**Resource:** [Admin/Image](../resources/Admin-Image.md)
**上傳 Image**
**Operation ID:** `post--admin-upload`

## Request Body

**Content Types:** `application/json`, `application/json/repositoryId`, `application/json/tagId`

**Schema:** [uploadImageInput.admin](../schemas/uploadImageInput-admin/uploadImageInput-admin.md)

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
