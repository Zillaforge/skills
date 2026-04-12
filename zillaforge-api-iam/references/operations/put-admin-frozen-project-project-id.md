# PUT /admin/frozen/project/{project-id}

**Resource:** [Admin/Frozen](../resources/Admin-Frozen.md)
**設定專案的啟用/停用狀態**
**Operation ID:** `put--admin-frozen-project-{project-id}`

以 Project ID 指定專案的啟用/停用狀態

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

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
