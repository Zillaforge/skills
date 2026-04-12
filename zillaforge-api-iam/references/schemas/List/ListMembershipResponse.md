# ListMembershipResponse

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `memberships` | object[] | No |  |
| `total` | integer | No |  |

## Nested Fields

### `memberships`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `membershipId` | string | No |  |
| `projectId` | string | No |  |
| `user` | object | No |  |
| `globalPermissionId` | string | No |  |
| `userPermissionId` | string | No |  |
| `frozen` | boolean | No |  |
| `tenantRole` | string | No |  |

#### `memberships.user`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `userId` | string | No |  |
| `account` | string | No |  |
| `displayName` | string | No |  |
| `description` | string | No |  |
| `extra` | object | No |  |
| `namespace` | string | No |  |
| `email` | string | No |  |
| `createdAt` | string | No |  |
| `updatedAt` | string | No |  |
| `lastLoginAt` | string | No |  |

