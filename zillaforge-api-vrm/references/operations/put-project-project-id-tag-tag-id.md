# PUT /project/:{project-id}/tag/:{tag-id}

**Resource:** [User/Tag](../resources/User-Tag.md)
**更新指定的 tag**
**Operation ID:** `put--project-:{project-id}-tag-:{tag-id}`

Update an existing tag by ID. Only the tag creator, tenant owner, or tenant admin can perform this operation.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `tag-id` | path | string | Yes | Tag ID |

## Request Body

Tag update data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.UpdateTagInput](../schemas/user-UpdateTagInput/user-UpdateTagInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successfully updated tag |
| 400 | Bad request - malformed input |
| 401 | Unauthorized - insufficient permissions |
| 403 | Forbidden |
| 404 | Tag not found |
| 500 | Internal server error |

**Success Response Schema:**

[user.UpdateTagOutput](../schemas/user-UpdateTagOutput/user-UpdateTagOutput.md)

