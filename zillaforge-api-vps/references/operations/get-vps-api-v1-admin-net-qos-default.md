# GET /vps/api/v1/admin/net_qos/default

**Resource:** [system_net_qos](../resources/system-net-qos.md)
**get default network QoS Policy**
**Operation ID:** `get--vps-api-v1-admin-net_qos-default`

Returns the network QoS Policy used as defaults when creating projects.

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.NetQoSOutput](../schemas/admin-NetQoSOutput/admin-NetQoSOutput.md)

