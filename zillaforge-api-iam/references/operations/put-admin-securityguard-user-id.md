# PUT /admin/securityguard/{user-id}/

**Resource:** [Admin/SecurityGuard](../resources/Admin-SecurityGuard.md)
**JailUser or ReleaseUser**
**Operation ID:** `put--admin-securityguard-{user-id}-`

變更使用者的鎖定狀態, 鎖定某帳號 或 解鎖某帳號


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | 要操作鎖定或解鎖帳號的userid
 |

## Request Body

欲鎖定請將jail帶true, 欲解除鎖定請將jail帶false; 解除鎖定一個非鎖定狀態的user會有error403; 鎖定已經是鎖定狀態的user會重新倒數鎖定時間


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateJailerRequest](../schemas/Update/UpdateJailerRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |
| 501 | Not Implemented | SecurityGuard功能未被啟用或定義Provider, 無法提供此服務 |

## Security

- **bearerAuth**
