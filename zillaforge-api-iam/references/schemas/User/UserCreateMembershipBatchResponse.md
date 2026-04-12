# UserCreateMembershipBatchResponse

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `responses` | object[] | No |  |
| `errors` | object[] | No |  |

## Nested Fields

### `responses`

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

#### `responses.globalPermission`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | No |  |
| `label` | string | No |  |

#### `responses.userPermission`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | No |  |
| `label` | string | No |  |

### `errors`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `userId` | string | No |  |
| `account` | string | No |  |
| `errCode` | integer | No |  |
| `message` | string | No |  |

