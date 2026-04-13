# PUT /admin/project/:{project-id}

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**更新指定的 project**
**Operation ID:** `put--admin-project-:{project-id}`

Update the soft limit count and size for a project

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

Update project request

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.UpdateProjectInput](../schemas/admin-UpdateProjectInput/admin-UpdateProjectInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.UpdateProjectOutput](../schemas/admin-UpdateProjectOutput/admin-UpdateProjectOutput.md)

