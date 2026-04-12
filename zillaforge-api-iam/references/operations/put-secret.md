# PUT /secret

**Resource:** [User/CliSecret](../resources/User-CliSecret.md)
**UpdateCliSecret**
**Operation ID:** `put--secret`

更新 Cli Secret，若該 user未建立則自動建立 Cli Secret


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
