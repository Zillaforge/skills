# PUT /vps/api/v1/project/:{project-id}/networks/:{network-id}

**Resource:** [network](../resources/network.md)
**Update Network**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-networks-:{network-id}`

Updates the name or description of a given network.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `network-id` | path | string | Yes | Network ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.NetUpdateInput](../schemas/user-NetUpdateInput/user-NetUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.NetworkInfo](../schemas/pb-NetworkInfo/pb-NetworkInfo.md)

## Security

- **ApiKeyAuth**
