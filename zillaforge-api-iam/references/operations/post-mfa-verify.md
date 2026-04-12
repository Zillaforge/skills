# POST /mfa/verify

**Resource:** [User/MFA](../resources/User-MFA.md)
**驗證 MFA**
**Operation ID:** `post--mfa-verify`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [VerifyMfaRequest](../schemas/Verify/VerifyMfaRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 302 | 轉到至目標網頁並且攜帶IAM_TOKEN |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

