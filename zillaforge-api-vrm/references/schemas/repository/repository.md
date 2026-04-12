# repository

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string (uuid) | No |  |
| `name` | string | No |  |
| `namespace` | string | No |  |
| `operatingSystem` | string | No |  |
| `description` | string | No |  |
| `tags` | tag.info[] | No |  |
| `count` | integer | No |  |
| `creator` | [user.info](user-info.md) | No |  |
| `project` | [project.info](project-info.md) | No |  |
| `createdAt` | string (date-time) | No | UTC Time (RFC3339) |
| `updatedAt` | string (date-time) | No | UTC Time (RFC3339) |

