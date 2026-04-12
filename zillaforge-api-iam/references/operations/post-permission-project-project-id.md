# POST /permission/project/{project-id}

**Resource:** [User/Permission](../resources/User-Permission.md)
**在指定project下建立permission**
**Operation ID:** `post--permission-project-{project-id}`

根據project id建立屬於該project的permission


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | 要建立的project id當參數 |

## Request Body

CreatePermissionByProject


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreatePermissionByProjectRequest](../schemas/Create/CreatePermissionByProjectRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[CreatePermissionByProjectResponse](../schemas/Create/CreatePermissionByProjectResponse.md)

## Security

- **bearerAuth**
