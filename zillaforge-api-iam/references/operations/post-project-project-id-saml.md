# POST /project/{project-id}/saml

**Resource:** [User/Projects](../resources/User-Projects.md)
**創建saml by project id**
**Operation ID:** `post--project-{project-id}-saml`

Create a saml by project id


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | admin project id |

## Request Body

**Required:** Yes

**Content Types:** `multipart/form-data`

**Schema:** [CreateUserProjectSAMLRequest](../schemas/Create/CreateUserProjectSAMLRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | OK |
| 400 | admin project 不存在 |
| 500 | IAM Server 發生內部錯誤 |

**Success Response Schema:**

[UserProjectSAMLResponse](../schemas/User/UserProjectSAMLResponse.md)

## Security

- **bearerAuth**
