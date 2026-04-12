# DELETE /admin/usagetime/project/{project-id}

**Resource:** [Admin/UsageTime](../resources/Admin-UsageTime.md)
**delete project usage time**
**Operation ID:** `delete--admin-usagetime-project-{project-id}`

刪除專案的有效期限


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | project id |

## Responses

| Status | Description |
|--------|-------------|
| 200 | 刪除成功 |
| 500 | IAM server內部發生錯誤 |

## Security

- **bearerAuth**
