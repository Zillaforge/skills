# PUT /project/{project-id}/saml/{saml-id}

**Resource:** [User/Projects](../resources/User-Projects.md)
**更新 saml by project id and saml-id**
**Operation ID:** `put--project-{project-id}-saml-{saml-id}`

Update a saml by project id and saml-id


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

[UserProjectSAMLResponse](../schemas/User/UserProjectSAMLResponse.md)

## Security

- **bearerAuth**
