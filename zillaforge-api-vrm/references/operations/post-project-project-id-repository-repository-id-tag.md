# POST /project/:{project-id}/repository/:{repository-id}/tag

**Resource:** [User/Tag](../resources/User-Tag.md)
**在 repository 創建 tag**
**Operation ID:** `post--project-:{project-id}-repository-:{repository-id}-tag`

Create a new tag with the specified name, type, disk format, and container format

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `repository-id` | path | string | Yes | Repository ID |

## Request Body

Tag creation input

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.CreateTagInput](../schemas/user-CreateTagInput/user-CreateTagInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Successfully created tag |
| 400 | Bad request - invalid input |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[user.CreateTagOutput](../schemas/user-CreateTagOutput/user-CreateTagOutput.md)

