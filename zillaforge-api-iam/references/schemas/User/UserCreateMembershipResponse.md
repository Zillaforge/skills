# UserCreateMembershipResponse

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `membershipId` | string | No |  |
| `projectId` | string | No |  |
| `userId` | string | No |  |
| `globalPermission` | object | No |  |
| `userPermission` | object | No |  |
| `frozen` | boolean | No |  |
| `quota` | string | No |  |
| `tenantRole` | string | No |  |
| `extra` | object | No |  |

## Nested Fields

### `globalPermission`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | No |  |
| `label` | string | No |  |

### `userPermission`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | No |  |
| `label` | string | No |  |

