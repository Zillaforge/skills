# UserScopes

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `userMFARequired` | boolean | No | 系統使用者登入時，是否強制驗證MFA |
| `adminMFARequired` | boolean | No | 系統管理員登入時，是否強制驗證MFA |
| `enableStandardRedirectCode` | boolean | No | 啟用時以302進行轉址，否則回傳205 |
| `enableNamespaced` | boolean | No | 是否啟用多重命名域 |
| `enablePasswordExpired` | boolean | No | 是否啟用使用者密碼到期檢查 |
| `enableSecurityGuard` | boolean | No | 是否啟用登入密碼重試檢查 |
| `permissionValidateMode` | string | No | 驗證模式是白名單或黑名單 |
| `enablePasswordHistory` | boolean | No | 是否啟用密碼與過去設定相同的檢查 |
| `enableUserChangeInitialPassword` | boolean | No | 是否強制使用者更新初始密碼 |
| `enableAdminChangeInitialPassword` | boolean | No | 是否強制管理員更新初始密碼 |

