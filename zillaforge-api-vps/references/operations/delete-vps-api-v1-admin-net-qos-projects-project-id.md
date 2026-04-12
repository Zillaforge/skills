# DELETE /vps/api/v1/admin/net_qos/projects/:{project-id}

**Resource:** [system_net_qos](../resources/system-net-qos.md)
**reset project's network QoS Policy as default value**
**Operation ID:** `delete--vps-api-v1-admin-net_qos-projects-:{project-id}`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

