# PUT /vps/api/v1/admin/net_qos/default

**Resource:** [system_net_qos](../resources/system-net-qos.md)
**set default network QoS Policy**
**Operation ID:** `put--vps-api-v1-admin-net_qos-default`

Sets the default network QoS Policy that are used as defaults when creating projects.

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.NetQoSInput](../schemas/admin-NetQoSInput/admin-NetQoSInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.NetQoSOutput](../schemas/admin-NetQoSOutput/admin-NetQoSOutput.md)

