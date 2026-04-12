# PUT /admin/project/{project-id}/

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**更新一個project**
**Operation ID:** `put--admin-project-{project-id}-`

Update user Project, you can update project name.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | user project id |

## Request Body

UpdateProject


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateAdminProjectRequest](../schemas/Update/UpdateAdminProjectRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | bad request |
| 500 | IAM server內部發生錯誤 |

**Success Response Schema:**

[UpdateAdminProjectResponse](../schemas/Update/UpdateAdminProjectResponse.md)

## Security

- **bearerAuth**
