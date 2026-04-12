# user.ListenerCreateInput

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowed_cidrs` | string[] | No |  |
| `insert_headers` | object | No |  |
| `name` | string | No |  |
| `pool` | [user.PoolCreateInput](user-PoolCreateInput.md) | No |  |
| `pool_id` | string | No |  |
| `protocol` | string | Yes |  |
| `protocol_port` | integer | Yes |  |
| `secret` | [user.SecretCreateInput](user-SecretCreateInput.md) | No |  |
| `timeout_client_data` | integer | No |  |
| `timeout_member_connect` | integer | No |  |
| `timeout_member_data` | integer | No |  |
| `timeout_tcp_inspect` | integer | No |  |

