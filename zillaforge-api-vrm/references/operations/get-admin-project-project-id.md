# GET /admin/project/:{project-id}

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**取得 project 資訊**
**Operation ID:** `get--admin-project-:{project-id}`

Get project usage statistics and limits information

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.GetProjectInfoOutput](../schemas/admin-GetProjectInfoOutput/admin-GetProjectInfoOutput.md)

