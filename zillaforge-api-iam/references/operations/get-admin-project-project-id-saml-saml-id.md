# GET /admin/project/{project-id}/saml/{saml-id}

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**取得 saml by project id and saml-id**
**Operation ID:** `get--admin-project-{project-id}-saml-{saml-id}`

Get a saml by project id and saml-id


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | admin project id |
| `saml-id` | path | string | Yes | saml id |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | admin project 不存在 |
| 500 | IAM Server 發生內部錯誤 |

**Success Response Schema:**

[AdminProjectSAMLResponse](../schemas/Admin/AdminProjectSAMLResponse.md)

## Security

- **bearerAuth**
