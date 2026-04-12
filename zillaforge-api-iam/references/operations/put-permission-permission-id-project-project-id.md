# PUT /permission/{permission-id}/project/{project-id}

**Resource:** [User/Permission](../resources/User-Permission.md)
**在指定project下更新指定的permission**
**Operation ID:** `put--permission-{permission-id}-project-{project-id}`

根據project id及permission id更新屬於該project的permission


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | 要查詢的project id當參數 |
| `permission-id` | path | string | Yes | 要更新的permission id當參數 |

## Request Body

UpdatePermissionByProject


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdatePermissionByProjectRequest](../schemas/Update/UpdatePermissionByProjectRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[UpdatePermissionByProjectResponse](../schemas/Update/UpdatePermissionByProjectResponse.md)

## Security

- **bearerAuth**
