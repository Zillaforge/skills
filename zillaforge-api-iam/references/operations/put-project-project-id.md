# PUT /project/{project-id}/

**Resource:** [User/Projects](../resources/User-Projects.md)
**更新 project 資訊**
**Operation ID:** `put--project-{project-id}-`

UpdateProject (目前僅能更新ProjectExtra, 僅供 Tenant Owner/Admin 使用)


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

UpdateProject


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateUserProjectRequest](../schemas/Update/UpdateUserProjectRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

**Success Response Schema:**

[UpdateUserProjectResponse](../schemas/Update/UpdateUserProjectResponse.md)

## Security

- **bearerAuth**
