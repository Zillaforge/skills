# POST /admin/user/{user-id}/secret

**Resource:** [Admin/CliSecret](../resources/Admin-CliSecret.md)
**建立 CliSecret**
**Operation ID:** `post--admin-user-{user-id}-secret`
⚠️ **Deprecated**

建立 Cli Secret，目前會由 namespace決定是否啟用 Cli Secret(由 yaml檔設定)，並在 GetCliSecret時自動建立 CliSecret。


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[CreateCliSecretResponse](../schemas/Create/CreateCliSecretResponse.md)

## Security

- **bearerAuth**
