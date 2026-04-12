# DELETE /vps/api/v1/admin/provider_networks/:{net-id}/ports/:{port-id}

**Resource:** [system_provider_network](../resources/system-provider-network.md)
**Delete port on Provider Network**
**Operation ID:** `delete--vps-api-v1-admin-provider_networks-:{net-id}-ports-:{port-id}`

This deletes the specified port from the provider network.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `net-id` | path | string | Yes | Provider Network ID |
| `port-id` | path | string | Yes | Port ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
