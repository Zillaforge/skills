# POST /admin/tag

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**創建 tag**
**Operation ID:** `post--admin-tag`

## Request Body

**Content Types:** `application/json`

**Schema:** [createTagInput.admin](../schemas/createTagInput-admin/createTagInput-admin.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[createTagOutput](../schemas/createTagOutput/createTagOutput.md)

## Security

- **bearerAuth**
