# DELETE /admin/membership/project/{project-id}/user/{user-id}/

**Resource:** [Admin/Membership](../resources/Admin-Membership.md)
**DeleteMembership**
**Operation ID:** `delete--admin-membership-project-{project-id}-user-{user-id}-`

DeleteMembership


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | todo |
| `user-id` | path | string | Yes | todo |

## Responses

| Status | Description |
|--------|-------------|
| 204 | NoContent |
| 400 | BadRequest |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
