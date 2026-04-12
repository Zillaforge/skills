# DELETE /vps/api/v1/admin/net_qos/networks/:{network-id}

**Resource:** [system_net_qos](../resources/system-net-qos.md)
**reset network's QoS Policy as project default value**
**Operation ID:** `delete--vps-api-v1-admin-net_qos-networks-:{network-id}`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `network-id` | path | string | Yes | Network ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

