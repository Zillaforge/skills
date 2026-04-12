# GetUserProjectsResponse

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `projects` | object[] | No |  |
| `total` | integer | No |  |

## Nested Fields

### `projects`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `project` | object[] | No |  |
| `globalPermissionId` | string | No |  |
| `userPermissionId` | string | No |  |
| `globalPermission` | object | No |  |
| `userPermission` | object | No |  |
| `frozen` | boolean | No |  |

#### `projects.project`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `projectId` | string | No |  |
| `displayName` | string | No |  |
| `description` | string | No |  |
| `extra` | object | No |  |
| `namespace` | string | No |  |
| `createdAt` | string | No |  |
| `updatedAt` | string | No |  |
| `force` | boolean | No |  |
| `usagetime` | object | No |  |

#### `projects.globalPermission`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | No |  |
| `label` | string | No |  |

#### `projects.userPermission`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | No |  |
| `label` | string | No |  |

