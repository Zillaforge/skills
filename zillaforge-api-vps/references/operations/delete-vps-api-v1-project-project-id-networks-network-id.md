# DELETE /vps/api/v1/project/:{project-id}/networks/:{network-id}

**Resource:** [network](../resources/network.md)
**Delete Network**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-networks-:{network-id}`

Deletes the requested network from system. Deletion will be blocked if there were active ports.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `network-id` | path | string | Yes | Network ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
