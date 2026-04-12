# DELETE /vps/api/v1/admin/provider_networks/:{net-id}

**Resource:** [system_provider_network](../resources/system-provider-network.md)
**Delete Provider Network**
**Operation ID:** `delete--vps-api-v1-admin-provider_networks-:{net-id}`

This will remove the specified provider network from virtual platform service database.
It will fail if there are still some ports bound to it.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `net-id` | path | string | Yes | Provider Network ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
