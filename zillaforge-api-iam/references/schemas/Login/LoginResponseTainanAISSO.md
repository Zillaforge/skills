# LoginResponseTainanAISSO

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

### `extra`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `XMLName` | object | No |  |
| `Xmlns` | string | No |  |
| `VerifiedToken` | string | No |  |
| `VerifiedAPCode` | string | No |  |
| `VerifiedAccount` | string | No |  |
| `VerifiedResult` | boolean | No |  |
| `VerifiedMessage` | string | No |  |
| `UserPid` | string | No |  |
| `UserName` | string | No |  |
| `UserOrganId` | string | No |  |
| `UserDirectorOrganId` | string | No |  |
| `UserOrganName` | string | No |  |
| `UserOrganShortName` | string | No |  |
| `UserJobTitle` | string | No |  |
| `UserPortraitUrl` | string | No |  |
| `UserTelOffice` | string | No |  |
| `UserTelPersonal` | string | No |  |
| `UserEmail` | string | No |  |

#### `extra.XMLName`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `Space` | string | No |  |
| `Local` | string | No |  |

