# DELETE /project/:{project-id}/repository/:{repository-id}

**Resource:** [User/Repository](../resources/User-Repository.md)
**棄用指定的 repository**
**Operation ID:** `delete--project-:{project-id}-repository-:{repository-id}`

Delete a repository by ID. Only repository creators, tenant owners, and tenant admins can delete repositories. Protected repositories cannot be deleted.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `repository-id` | path | string | Yes | Repository ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 403 | Forbidden |
| 404 | Repository not found |
| 500 | Internal server error |

