# GET /vps/api/v1/admin/provider_networks/:{net-id}

**Resource:** [system_provider_network](../resources/system-provider-network.md)
**Get Provider Network**
**Operation ID:** `get--vps-api-v1-admin-provider_networks-:{net-id}`

Return information about one specific provider network.

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

[pb.ProviderNetInfo](../schemas/pb-ProviderNetInfo/pb-ProviderNetInfo.md)

## Security

- **ApiKeyAuth**
