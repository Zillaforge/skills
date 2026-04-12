# DELETE /membership/project/{project-id}/user/{user-id}

**Resource:** [User/Membership](../resources/User-Membership.md)
**Delete Membership**
**Operation ID:** `delete--membership-project-{project-id}-user-{user-id}`

Delete membership by tenant admin/owner


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `user-id` | path | string | Yes | User ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
