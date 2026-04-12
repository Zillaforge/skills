# POST /vps/api/v1/admin/provider_networks/:{net-id}/ports

**Resource:** [system_provider_network](../resources/system-provider-network.md)
**Attach Provider Network to a Server**
**Operation ID:** `post--vps-api-v1-admin-provider_networks-:{net-id}-ports`

Creates a new port from the provider network and attaches it to a server.

Request Body Parameters:
- server_id: The UUID of the target server.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `net-id` | path | string | Yes | Provider Network ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [pb.ProviderNetPortAttachInput](../schemas/pb-ProviderNetPortAttachInput/pb-ProviderNetPortAttachInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
