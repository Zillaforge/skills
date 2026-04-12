# GET /permissions/project/{project-id}

**Resource:** [User/Permission](../resources/User-Permission.md)
**列出project下的所有permission**
**Operation ID:** `get--permissions-project-{project-id}`

根據project id列出該project下的所有permission


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | 要查詢的project id當參數 |
| `offset` | query | integer | No | The number of items to skip before starting to collect the result set. |
| `limit` | query | integer | No | The number of items to return. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error | IAM Server 發生內部錯誤 |

**Success Response Schema:**

[ListPermissionsByProjectResponse](../schemas/List/ListPermissionsByProjectResponse.md)

## Security

- **bearerAuth**
