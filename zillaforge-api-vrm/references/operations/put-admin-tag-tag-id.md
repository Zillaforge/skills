# PUT /admin/tag/:{tag-id}

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**更新指定的 tag**
**Operation ID:** `put--admin-tag-:{tag-id}`

Update an existing tag with administrative privileges

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `tag-id` | path | string | Yes | Tag ID |

## Request Body

Tag update payload

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.UpdateTagInput](../schemas/admin-UpdateTagInput/admin-UpdateTagInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.UpdateTagOutput](../schemas/admin-UpdateTagOutput/admin-UpdateTagOutput.md)

