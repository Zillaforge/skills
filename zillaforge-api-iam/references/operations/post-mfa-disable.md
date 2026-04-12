# POST /mfa/disable

**Resource:** [User/MFA](../resources/User-MFA.md)
**取消 MFA 認證**
**Operation ID:** `post--mfa-disable`

## Responses

| Status | Description |
|--------|-------------|
| 204 | No content, MFA was disabled successfully. |
| 403 | Forbidden |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
