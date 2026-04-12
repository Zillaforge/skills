# PUT /admin/user/{user-id}/password

**Resource:** [Admin/User](../resources/Admin-User.md)
**UpdatePassword**
**Operation ID:** `put--admin-user-{user-id}-password`

UpdatePassword


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Request Body

UpdatePassword


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateUserPassword](../schemas/Update/UpdateUserPassword.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
