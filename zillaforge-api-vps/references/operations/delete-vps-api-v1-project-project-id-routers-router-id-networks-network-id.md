# DELETE /vps/api/v1/project/:{project-id}/routers/:{router-id}/networks/:{network-id}

**Resource:** [router](../resources/router.md)
**Disassociate Network from Router**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-routers-:{router-id}-networks-:{network-id}`

Disassociates a network from a router.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `router-id` | path | string | Yes | Router ID |
| `network-id` | path | string | Yes | Network ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
