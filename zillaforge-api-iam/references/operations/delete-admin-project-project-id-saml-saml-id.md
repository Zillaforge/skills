# DELETE /admin/project/{project-id}/saml/{saml-id}

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**刪除 saml by project id and saml-id**
**Operation ID:** `delete--admin-project-{project-id}-saml-{saml-id}`

Delete a saml by project id and saml-id


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | admin project id |
| `saml-id` | path | string | Yes | saml id |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | admin project 不存在 |
| 500 | IAM Server 發生內部錯誤 |

## Security

- **bearerAuth**
