# POST /admin/tag/:{tag-id}/download

**Resource:** [Admin/Image](../resources/Admin-Image.md)
**下載 Image**
**Operation ID:** `post--admin-tag-:{tag-id}-download`

Downloads a image based on the provided filepath and tag ID

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `tag-id` | path | string | Yes | Tag ID |

## Request Body

Download image request

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.DownloadImageInput](../schemas/admin-DownloadImageInput/admin-DownloadImageInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.DownloadImageOutput](../schemas/admin-DownloadImageOutput/admin-DownloadImageOutput.md)

