# POST /admin/mfa/user/{user-id}/disable

**Resource:** [Admin/MFA](../resources/Admin-MFA.md)
**取消指定 User 的 MFA 認證**
**Operation ID:** `post--admin-mfa-user-{user-id}-disable`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No content, MFA was disabled successfully. |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
