# GET /vps/api/v1/project/:{project-id}/networks/:{network-id}

**Resource:** [network](../resources/network.md)
**Get Network**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-networks-:{network-id}`

Gets detailed information about a single network.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `network-id` | path | string | Yes | Network ID |

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
