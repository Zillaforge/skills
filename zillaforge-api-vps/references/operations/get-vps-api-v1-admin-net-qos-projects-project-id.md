# GET /vps/api/v1/admin/net_qos/projects/:{project-id}

**Resource:** [system_net_qos](../resources/system-net-qos.md)
**get project's network QoS Policy**
**Operation ID:** `get--vps-api-v1-admin-net_qos-projects-:{project-id}`

Return network QoS Policy for specific project.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.NetQoSOutput](../schemas/admin-NetQoSOutput/admin-NetQoSOutput.md)

