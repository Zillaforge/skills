# GET /admin/user/{user-id}/

**Resource:** [Admin/User](../resources/Admin-User.md)
**GetUser**
**Operation ID:** `get--admin-user-{user-id}-`

GetUser


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[GetUserResponse](../schemas/Get/GetUserResponse.md)

## Security

- **bearerAuth**
