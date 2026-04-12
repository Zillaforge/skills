# listProjectsOutput

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `projects` | object | No |  |
| `total` | integer | No |  |

## Nested Fields

### `projects`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string (uuid) | No |  |
| `usedSize` | integer | No |  |
| `usedCount` | integer | No |  |
| `softLimitSize` | integer | No | unlimit if equal to -1 |
| `softLimitCount` | integer | No | unlimit if equal to -1 |

