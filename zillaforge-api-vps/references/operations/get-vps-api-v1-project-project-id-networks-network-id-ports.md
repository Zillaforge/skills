# GET /vps/api/v1/project/:{project-id}/networks/:{network-id}/ports

**Resource:** [network](../resources/network.md)
**List Network Ports**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-networks-:{network-id}-ports`

Lists all ports belonging to the selected network.

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

Array of [user.NetPort](../schemas/user-NetPort/user-NetPort.md)

## Security

- **ApiKeyAuth**
