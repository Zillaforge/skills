# GET /vps/api/v1/project/:{project-id}/routers

**Resource:** [router](../resources/router.md)
**List Routers**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-routers`

List routers that belong to current project with optional filtering options.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id |
| `status` | query | string | No | search by status |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.RouterListOutput](../schemas/pb-RouterListOutput/pb-RouterListOutput.md)

## Security

- **ApiKeyAuth**
