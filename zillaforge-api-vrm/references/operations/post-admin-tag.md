# POST /admin/tag

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**創建 tag**
**Operation ID:** `post--admin-tag`

Create a new tag with administrative privileges and simultaneously create an empty Glance image

## Request Body

Tag creation payload

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.CreateTagInput](../schemas/admin-CreateTagInput/admin-CreateTagInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.CreateTagOutput](../schemas/admin-CreateTagOutput/admin-CreateTagOutput.md)

