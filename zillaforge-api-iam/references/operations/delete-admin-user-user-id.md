# DELETE /admin/user/{user-id}/

**Resource:** [Admin/User](../resources/Admin-User.md)
**DeleteUser**
**Operation ID:** `delete--admin-user-{user-id}-`

DeleteUser


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Responses

| Status | Description |
|--------|-------------|
| 204 | NoContent |
| 400 | BadRequest |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
