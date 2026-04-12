# GET /vps/api/v1/project/:{project-id}/networks

**Resource:** [network](../resources/network.md)
**List Networks**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-networks`

List all networks that belong to current project.
You could search with different conditions including name,user_id,status,router_id.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id |
| `status` | query | string | No | search by status |
| `router_id` | query | string | No | search by router_id |
| `detail` | query | boolean | No | get detail infomations |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.NetworkListOutput](../schemas/pb-NetworkListOutput/pb-NetworkListOutput.md)

## Security

- **ApiKeyAuth**
