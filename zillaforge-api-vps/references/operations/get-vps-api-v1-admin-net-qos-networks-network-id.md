# GET /vps/api/v1/admin/net_qos/networks/:{network-id}

**Resource:** [system_net_qos](../resources/system-net-qos.md)
**get networks's QoS Policy**
**Operation ID:** `get--vps-api-v1-admin-net_qos-networks-:{network-id}`

Return QoS Policy for specific network.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `network-id` | path | string | Yes | Network ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.NetQoSOutput](../schemas/admin-NetQoSOutput/admin-NetQoSOutput.md)

