# ListMembershipsByUserResponse

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
| `project` | object | No |  |
| `userId` | string | No |  |
| `globalPermissionId` | string | No |  |
| `userPermissionId` | string | No |  |
| `frozen` | boolean | No |  |
| `tenantRole` | string | No |  |

#### `memberships.project`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `projectId` | string | No |  |
| `displayName` | string | No |  |
| `description` | string | No |  |
| `extra` | object | No |  |
| `namespace` | string | No |  |
| `createdAt` | string | No |  |
| `updatedAt` | string | No |  |
| `lastLoginAt` | string | No |  |

