# HEAD /verify

**Resource:** [User/Login](../resources/User-Login.md)
**驗證 JWT Token 是否合法**
**Operation ID:** `head--verify`

驗證 JWT Token 是否合法


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `X-Verify-Authorization` | header | string | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
