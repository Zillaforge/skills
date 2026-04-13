# POST /project/:{project-id}/tag/:{tag-id}/download

**Resource:** [User/Image](../resources/User-Image.md)
**下載 Image**
**Operation ID:** `post--project-:{project-id}-tag-:{tag-id}-download`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `tag-id` | path | string | Yes | Tag ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.DownloadImageInput](../schemas/user-DownloadImageInput/user-DownloadImageInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

