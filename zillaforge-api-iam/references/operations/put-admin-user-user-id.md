# PUT /admin/user/{user-id}/

**Resource:** [Admin/User](../resources/Admin-User.md)
**UpdateUser**
**Operation ID:** `put--admin-user-{user-id}-`

UpdateUser


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Request Body

UpdateUser


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateUserRequest](../schemas/Update/UpdateUserRequest.md)

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
