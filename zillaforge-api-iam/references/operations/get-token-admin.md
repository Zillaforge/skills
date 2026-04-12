# GET /token/admin

**Resource:** [User/Login](../resources/User-Login.md)
**取得 IAM admin token**
**Operation ID:** `get--token-admin`

取得 IAM admin token


## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

**Success Response Schema:**

[GetAdminAPITokenResponse](../schemas/Get/GetAdminAPITokenResponse.md)

## Security

- **bearerAuth**
