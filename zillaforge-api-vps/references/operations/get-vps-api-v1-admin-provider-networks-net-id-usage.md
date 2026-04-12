# GET /vps/api/v1/admin/provider_networks/:{net-id}/usage

**Resource:** [system_provider_network](../resources/system-provider-network.md)
**get IP usage**
**Operation ID:** `get--vps-api-v1-admin-provider_networks-:{net-id}-usage`

Retrieves current ip address usgae statistics of the provided provider network.

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

[pb.NetIPUsage](../schemas/pb-NetIPUsage/pb-NetIPUsage.md)

## Security

- **ApiKeyAuth**
