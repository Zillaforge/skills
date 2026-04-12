# GET /project/{project-id}/samls

**Resource:** [User/Projects](../resources/User-Projects.md)
**取得所有的saml by project id**
**Operation ID:** `get--project-{project-id}-samls`

List samls by project id


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | admin project id |
| `offset` | query | integer | No | The number of items to skip before starting to collect the result set. |
| `limit` | query | integer | No | The number of items to return. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | admin project 不存在 |
| 500 | IAM Server 發生內部錯誤 |

**Success Response Schema:**

[ListUserProjectSAMLResponse](../schemas/List/ListUserProjectSAMLResponse.md)

## Security

- **bearerAuth**
