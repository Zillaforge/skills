# AdminCreatePersonalAccessAPITokenRequest

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `description` | string | No |  |
| `expiredAt` | string | No | 當unlimited是false這個項目才有效, format is RFC3339 |
| `unlimited` | boolean | No | 啟用無期限的 expiration |
| `type` | string | No | PAAT 類型，當前僅允許 ADMIN 與 USER |

