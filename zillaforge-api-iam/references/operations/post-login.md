# POST /login

**Resource:** [User/Login](../resources/User-Login.md)
**登入 IAM**
**Operation ID:** `post--login`

## Request Body

登入頁面需輸入登入資訊，成功後會取得 JWT Token 、 user 資訊 與 extra 資訊


**Required:** Yes

**Content Types:** `application/json`

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 205 | 驗證成功，回應轉址的網址並挾帶Token，
強制MFA模式且未設定MFA時Token為mfaRegisterToken，
啟用MFA之後Token為mfaToken，
啟用強制更新密碼時Token為changePasswordToken，
Token則會以Query Parameter方式帶入
 |
| 302 | 驗證成功，進行轉址並挾帶Token，
強制MFA模式且未設定MFA時Token為mfaRegisterToken，
啟用MFA之後Token為mfaToken，
啟用強制更新密碼時Token為changePasswordToken，
Token則會以Query Parameter方式帶入
 |
| 403 | Forbidden |
| 500 | Internal Server Error |

