# GET /vps/api/v1/admin/networks/:{network-id}

**Resource:** [system_network](../resources/system-network.md)
**Get Network**
**Operation ID:** `get--vps-api-v1-admin-networks-:{network-id}`

Gets detailed information about a single network.

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

[pb.NetworkInfo](../schemas/pb-NetworkInfo/pb-NetworkInfo.md)

