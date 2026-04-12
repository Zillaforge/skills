# PUT /vps/api/v1/admin/net_qos/networks/:{network-id}

**Resource:** [system_net_qos](../resources/system-net-qos.md)
**set network's QoS Policy**
**Operation ID:** `put--vps-api-v1-admin-net_qos-networks-:{network-id}`

Set QoS Policy for specified project.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `network-id` | path | string | Yes | Network ID |

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

