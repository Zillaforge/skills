# PUT /user/password

**Resource:** [User/Users](../resources/User-Users.md)
**更換密碼**
**Operation ID:** `put--user-password`

更換指定用戶的密碼


## Request Body

輸入欲更新的密碼，成功回 status 200

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateUserPassword](../schemas/Update/UpdateUserPassword.md)

## Responses

| Status | Description |
|--------|-------------|
| 204 | StatusNoContent |
| 400 | BadRequest |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
