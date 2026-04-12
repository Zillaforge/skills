# POST /admin/import

**Resource:** [Admin/Image](../resources/Admin-Image.md)
**匯入 Image (已存在於openstack)**
**Operation ID:** `post--admin-import`

## Request Body

**Content Types:** `application/json`, `application/json/repositoryId`

**Schema:** [importImageInput](../schemas/importImageInput/importImageInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[importImageOutput](../schemas/importImageOutput/importImageOutput.md)

## Security

- **bearerAuth**
