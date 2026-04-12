# PUT /vps/api/v1/project/:{project-id}/routers/:{router-id}/networks/:{network-id}

**Resource:** [router](../resources/router.md)
**Associate Network to Router**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-routers-:{router-id}-networks-:{network-id}`

Associate a network to a router.

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
