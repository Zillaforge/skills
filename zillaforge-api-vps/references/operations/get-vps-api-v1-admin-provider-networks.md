# GET /vps/api/v1/admin/provider_networks

**Resource:** [system_provider_network](../resources/system-provider-network.md)
**List Provider Networks**
**Operation ID:** `get--vps-api-v1-admin-provider_networks`

Return a list of provider networks and their details.

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ProviderNetListOutput](../schemas/pb-ProviderNetListOutput/pb-ProviderNetListOutput.md)

## Security

- **ApiKeyAuth**
