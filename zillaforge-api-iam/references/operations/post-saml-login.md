# POST /saml/login

**Resource:** [User/SAML](../resources/User-SAML.md)
**產生saml response info 傳送給 service provider**
**Operation ID:** `post--saml-login`

generate saml response send to service provider


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `entityID` | query | string | Yes | 用來查找是哪一筆entityID |
| `SAMLRequest` | query | string | Yes | saml request 是由 service provider 傳送給idp的 xml authn request info. |
| `RelayState` | query | string | Yes | service provider用來重新導向用戶到原始請求的Context, idp 收到值不做任何處理 |

## Request Body

需要登入資訊, 登入成功的資訊會把user info 打包在saml response


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [LoginRequestDefault](../schemas/Login/LoginRequestDefault.md)

## Responses

| Status | Description |
|--------|-------------|
| 302 | StatusFound |
| 400 | BadRequest |
| 404 | NotFound |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
