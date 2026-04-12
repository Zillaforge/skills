# GET /admin/project/{project-id}/

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**取得特定 project-id 的 project 資訊**
**Operation ID:** `get--admin-project-{project-id}-`

Get a user project by project id


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | user project id |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | user project 不存在 |
| 500 | IAM Server 發生內部錯誤 |

**Success Response Schema:**

[GetAdminProjectResponse](../schemas/Get/GetAdminProjectResponse.md)

## Security

- **bearerAuth**
