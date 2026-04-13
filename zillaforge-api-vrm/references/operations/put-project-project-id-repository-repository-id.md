# PUT /project/:{project-id}/repository/:{repository-id}

**Resource:** [User/Repository](../resources/User-Repository.md)
**更新指定的 repository**
**Operation ID:** `put--project-:{project-id}-repository-:{repository-id}`

Update repository information including name and description

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `repository-id` | path | string | Yes | Repository ID |

## Request Body

Repository update data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.UpdateRepositoryInput](../schemas/user-UpdateRepositoryInput/user-UpdateRepositoryInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successfully updated repository |
| 400 | Bad request - malformed input |
| 401 | Unauthorized - insufficient permissions |
| 403 | Forbidden |
| 404 | Repository not found |
| 500 | Internal server error |

**Success Response Schema:**

[user.UpdateRepositoryOutput](../schemas/user-UpdateRepositoryOutput/user-UpdateRepositoryOutput.md)

