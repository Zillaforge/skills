# GET /project/:{project-id}/tag/:{tag-id}

**Resource:** [User/Tag](../resources/User-Tag.md)
**取得指定的 tag**
**Operation ID:** `get--project-:{project-id}-tag-:{tag-id}`

Retrieve tag information by tag ID

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `tag-id` | path | string | Yes | Tag ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[user.GetTagOutput](../schemas/user-GetTagOutput/user-GetTagOutput.md)

