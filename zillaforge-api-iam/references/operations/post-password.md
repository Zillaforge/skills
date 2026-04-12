# POST /password

**Resource:** [User/Login](../resources/User-Login.md)
**使用臨時 Token 更新使用者密碼**
**Operation ID:** `post--password`

啟用強制更新密碼時， 當系統檢查到必須更新密碼的情況會核發臨時權杖 changePasswordToken， 讓使用者呼叫此 API 更新密碼


## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [ForceChangePasswordRequest](../schemas/Force/ForceChangePasswordRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 204 | No content, password has been changed successfully. |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
