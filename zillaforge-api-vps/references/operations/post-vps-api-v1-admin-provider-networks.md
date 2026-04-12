# POST /vps/api/v1/admin/provider_networks

**Resource:** [system_provider_network](../resources/system-provider-network.md)
**Import Provider Network from OPSK**
**Operation ID:** `post--vps-api-v1-admin-provider_networks`

Import an existing openstack network as a provider network into Virtual Platform Service.

Parameters in the request body:
- opsk_net_uuid: The UUID of the openstack network that you want to import.(required)
- name: The name of this provider network.(optional)
- description: The description for this provider network.(optional)
- sg_ids: The security group IDs associated with this network.(required)

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [pb.ProviderNetCreateInput](../schemas/pb-ProviderNetCreateInput/pb-ProviderNetCreateInput.md)

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
