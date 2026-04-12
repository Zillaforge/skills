# HEAD /saml/auth_request/validate

**Resource:** [User/SAML](../resources/User-SAML.md)
**驗證 saml request 是否合法**
**Operation ID:** `head--saml-auth_request-validate`

驗證 saml request 是否合法


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `entityID` | query | string | Yes | 用來查找是哪一筆entityID |
| `SAMLRequest` | query | string | Yes | saml request 是由 service provider 傳送給idp的 xml authn request info. |
| `RelayState` | query | string | Yes | service provider用來重新導向用戶到原始請求的Context, idp 收到值不做任何處理 |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 404 | NotFound |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
