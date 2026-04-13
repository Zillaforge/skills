# GET /admin/projects

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**取得 project 資訊**
**Operation ID:** `get--admin-projects`

List all projects with their usage statistics and limits

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `limit` | query | integer | No | Number of items to return (default: 100) |
| `offset` | query | integer | No | Number of items to skip (default: 0) |
| `namespace` | query | string | No | Filter by namespace |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.ListProjectsOutput](../schemas/admin-ListProjectsOutput/admin-ListProjectsOutput.md)

