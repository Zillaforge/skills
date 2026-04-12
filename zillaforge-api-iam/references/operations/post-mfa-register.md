# POST /mfa/register

**Resource:** [User/MFA](../resources/User-MFA.md)
**註冊 MFA**
**Operation ID:** `post--mfa-register`

使用 mfaRegisterToken 註冊 MFA

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [RegisterMfaRequest](../schemas/Register/RegisterMfaRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 204 | No content, MFA was registered successfully. |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

