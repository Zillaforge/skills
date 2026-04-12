# GET /projects

**Resource:** [User/Projects](../resources/User-Projects.md)
**取得 project**
**Operation ID:** `get--projects`

取得 Current User 所擁有的 project 列表


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `offset` | query | integer | No | The number of items to skip before starting to collect the result set. |
| `limit` | query | integer | No | The number of items to return. |
| `order` | query | string | No | todo. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[GetUserProjectsResponse](../schemas/Get/GetUserProjectsResponse.md)

## Security

- **bearerAuth**
