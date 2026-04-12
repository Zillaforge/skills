# GET /admin/projects

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**取得 project 資訊**
**Operation ID:** `get--admin-projects`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `X-Namespace` | header | string | No | Namespace for filtering projects |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[listProjectsOutput](../schemas/listProjectsOutput/listProjectsOutput.md)

## Security

- **bearerAuth**
