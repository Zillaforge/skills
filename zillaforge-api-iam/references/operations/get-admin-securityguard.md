# GET /admin/securityguard

**Resource:** [Admin/SecurityGuard](../resources/Admin-SecurityGuard.md)
**ListJailers**
**Operation ID:** `get--admin-securityguard`

使用帳號密碼登入時, 如果密碼錯誤過多次, 就會被鎖定帳號, 這邊是列出所有被鎖定的帳號


## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 500 | Internal Server Error |
| 501 | Not Implemented | SecurityGuard功能未被啟用或定義Provider, 無法提供此服務 |

## Security

- **bearerAuth**
