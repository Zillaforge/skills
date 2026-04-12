# GET /vps/api/v1/admin/provider_networks/:{net-id}/ports

**Resource:** [system_provider_network](../resources/system-provider-network.md)
**List ports on Provider Network**
**Operation ID:** `get--vps-api-v1-admin-provider_networks-:{net-id}-ports`

Returns ports which belong to given provider network.
The result includes port details like IP addresses, server etc...

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `net-id` | path | string | Yes | Provider Network ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ProviderNetPortListOutput](../schemas/pb-ProviderNetPortListOutput/pb-ProviderNetPortListOutput.md)

## Security

- **ApiKeyAuth**
