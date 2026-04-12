# DELETE /admin/user/{user-id}/secret

**Resource:** [Admin/CliSecret](../resources/Admin-CliSecret.md)
**刪除 CliSecret**
**Operation ID:** `delete--admin-user-{user-id}-secret`
⚠️ **Deprecated**

刪除 Cli Secret，目前會由 namespace決定是否啟用 Cli Secret(由 yaml檔設定)，若要取消 Cli Secret需要修改 namespace或更改 yaml檔設定


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Responses

| Status | Description |
|--------|-------------|
| 204 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
