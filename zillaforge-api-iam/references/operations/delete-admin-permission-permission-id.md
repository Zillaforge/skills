# DELETE /admin/permission/{permission-id}

**Resource:** [Admin/Permission](../resources/Admin-Permission.md)
**刪除指定的 permission**
**Operation ID:** `delete--admin-permission-{permission-id}`

根據permission id 刪除permission


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `permission-id` | path | string | Yes | 要刪除的permission id當參數 |

## Responses

| Status | Description |
|--------|-------------|
| 204 | 刪除成功 |
| 403 | permission正在被使用中 |
| 500 | IAM server內部發生錯誤 |

## Security

- **bearerAuth**
