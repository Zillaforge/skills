# POST /admin/upload

**Resource:** [Admin/Image](../resources/Admin-Image.md)
**上傳 Image**
**Operation ID:** `post--admin-upload`

Creates a repository/tag if they don't exist and uploads image data to the specified tag

## Request Body

Upload image request

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.UploadImageInput](../schemas/admin-UploadImageInput/admin-UploadImageInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.UploadImageOutput](../schemas/admin-UploadImageOutput/admin-UploadImageOutput.md)

