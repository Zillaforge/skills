# GET /project/:{project-id}/repository/:{repository-id}

**Resource:** [User/Repository](../resources/User-Repository.md)
**取得指定的 repository**
**Operation ID:** `get--project-:{project-id}-repository-:{repository-id}`

Get repository details by project ID and repository ID

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `repository-id` | path | string | Yes | Repository ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal server error |

**Success Response Schema:**

[user.GetRepositoryOutput](../schemas/user-GetRepositoryOutput/user-GetRepositoryOutput.md)

