# GET /mfa/get

**Resource:** [User/MFA](../resources/User-MFA.md)
**產生 MFA secret, token, URL**
**Operation ID:** `get--mfa-get`

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 500 | Internal Server Error |

**Success Response Schema:**

[GetMfaResponse](../schemas/Get/GetMfaResponse.md)

## Security

- **bearerAuth**
