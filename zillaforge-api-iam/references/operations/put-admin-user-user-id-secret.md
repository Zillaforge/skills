# PUT /admin/user/{user-id}/secret

**Resource:** [Admin/CliSecret](../resources/Admin-CliSecret.md)
**UpdateCliSecret**
**Operation ID:** `put--admin-user-{user-id}-secret`

更新 Cli Secret，若該 user未建立則自動建立 Cli Secret


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
