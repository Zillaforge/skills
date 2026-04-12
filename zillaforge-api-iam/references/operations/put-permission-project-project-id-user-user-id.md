# PUT /permission/project/{project-id}/user/{user-id}

**Resource:** [User/Permission](../resources/User-Permission.md)
**在指定project下更新指定的user permission**
**Operation ID:** `put--permission-project-{project-id}-user-{user-id}`

根據project user id更新該project下的user permission


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | 要查詢的project id當參數 |
| `user-id` | path | string | Yes | 要更新的user id當參數 |

## Request Body

UpdateUserPermissionByProject


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateUserPermissionByProjectRequest](../schemas/Update/UpdateUserPermissionByProjectRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[UpdateUserPermissionByProjectResponse](../schemas/Update/UpdateUserPermissionByProjectResponse.md)

## Security

- **bearerAuth**
