# PUT /token/refresh

**Resource:** [User/Login](../resources/User-Login.md)
**更新 IAM token**
**Operation ID:** `put--token-refresh`

更新 IAM token


## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

**Success Response Schema:**

[TokenResponse](../schemas/Token/TokenResponse.md)

## Security

- **bearerAuth**
