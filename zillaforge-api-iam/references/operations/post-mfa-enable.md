# POST /mfa/enable

**Resource:** [User/MFA](../resources/User-MFA.md)
**啟用 MFA 認證**
**Operation ID:** `post--mfa-enable`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [EnableMfaRequest](../schemas/Enable/EnableMfaRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 204 | No content, MFA was enabled successfully. |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
