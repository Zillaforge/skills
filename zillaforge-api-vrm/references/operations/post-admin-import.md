# POST /admin/import

**Resource:** [Admin/Image](../resources/Admin-Image.md)
**匯入 Image (已存在於openstack)**
**Operation ID:** `post--admin-import`

Creates a common tag from an existing OpenStack Glance image and sets it as public

## Request Body

Import image request

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.ImportImageInput](../schemas/admin-ImportImageInput/admin-ImportImageInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.ImportImageOutput](../schemas/admin-ImportImageOutput/admin-ImportImageOutput.md)

