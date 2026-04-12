# LoginResponseTwccAuth

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `token` | string | No |  |
| `userInfo` | object | No |  |
| `extra` | object | No |  |

## Nested Fields

### `userInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `account` | string | No |  |
| `userId` | string | No |  |
| `displayName` | string | No |  |
| `description` | string | No |  |
| `extra` | object | No |  |
| `namespace` | string | No |  |
| `frozen` | boolean | No |  |
| `createdAt` | string | No |  |
| `updatedAt` | string | No |  |
| `lastLoginAt` | string | No |  |

#### `userInfo.extra`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `twcc` | object | No |  |

### `extra`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `apiKey` | object | No |  |
| `userId` | string | No |  |
| `userInfo` | object | No |  |
| `hostInfo` | object | No |  |
| `s3` | object | No |  |
| `walletInfo` | object | No |  |
| `permission` | object | No |  |
| `projectId` | object | No |  |

#### `extra.hostInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `MACHINE_ACCOUNT_GID` | string | No |  |
| `MACHINE_ACCOUNT_UID` | string | No |  |
| `MACHINE_ACCOUNT_ID` | string | No |  |

