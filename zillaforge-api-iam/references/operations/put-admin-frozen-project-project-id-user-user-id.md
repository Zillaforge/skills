# PUT /admin/frozen/project/{project-id}/user/{user-id}/

**Resource:** [Admin/Frozen](../resources/Admin-Frozen.md)
**設定使用者在特定專案的啟用/停用狀態**
**Operation ID:** `put--admin-frozen-project-{project-id}-user-{user-id}-`

以 User ID 及 Project ID 指定使用者在特定專案的啟用/停用狀態

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `user-id` | path | string | Yes | User ID |

## Request Body

當 frozen 為 true 是停用，否則啟用

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [SetAdminFrozenRequest](../schemas/Set/SetAdminFrozenRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 403 | Forbidden |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
