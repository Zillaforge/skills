# POST /project/:{project-id}/upload

**Resource:** [User/Image](../resources/User-Image.md)
**上傳 Image**
**Operation ID:** `post--project-:{project-id}-upload`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.UploadImageInput](../schemas/user-UploadImageInput/user-UploadImageInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[user.UploadImageOutput](../schemas/user-UploadImageOutput/user-UploadImageOutput.md)

