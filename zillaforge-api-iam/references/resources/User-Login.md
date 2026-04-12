# User/Login

Login API by User

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/version` | PegasusIAM版本 | [View](../operations/get-version.md) |
| GET | `/scopes` | 取得系統的規模 | [View](../operations/get-scopes.md) |
| POST | `/login` | 登入 IAM | [View](../operations/post-login.md) |
| POST | `/logout` | 登出 IAM | [View](../operations/post-logout.md) |
| HEAD | `/verify` | 驗證 JWT Token 是否合法 | [View](../operations/head-verify.md) |
| PUT | `/token/refresh` | 更新 IAM token | [View](../operations/put-token-refresh.md) |
| GET | `/token/admin` | 取得 IAM admin token | [View](../operations/get-token-admin.md) |
| POST | `/password` | 使用臨時 Token 更新使用者密碼 | [View](../operations/post-password.md) |
