# DELETE /admin/project/{project-id}/

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**刪除一個管理群組透過 ID**
**Operation ID:** `delete--admin-project-{project-id}-`

根據project id 刪除project


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | 要刪除的project id 當參數 |

## Responses

| Status | Description |
|--------|-------------|
| 200 | 刪除成功 |
| 500 | IAM server內部發生錯誤 |

## Security

- **bearerAuth**
