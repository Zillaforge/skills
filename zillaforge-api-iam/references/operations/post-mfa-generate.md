# POST /mfa/generate

**Resource:** [User/MFA](../resources/User-MFA.md)
**產生 MFA 資訊**
**Operation ID:** `post--mfa-generate`

使用 mfaRegisterToken 產生 MFA secret, token, URL

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [GenerateMfaRequest](../schemas/Generate/GenerateMfaRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

**Success Response Schema:**

[GenerateMfaResponse](../schemas/Generate/GenerateMfaResponse.md)

