# POST /vps/api/v1/admin/networks/:{network-id}/action

**Resource:** [system_network](../resources/system-network.md)
**Do Action to Network**
**Operation ID:** `post--vps-api-v1-admin-networks-:{network-id}-action`

Do an action on the specified network

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `network-id` | path | string | Yes | Network ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.AdmNetActionInput](../schemas/admin-AdmNetActionInput/admin-AdmNetActionInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.NetworkInfo](../schemas/pb-NetworkInfo/pb-NetworkInfo.md)

