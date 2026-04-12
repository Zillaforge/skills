# PUT /vps/api/v1/admin/provider_networks/:{net-id}

**Resource:** [system_provider_network](../resources/system-provider-network.md)
**Update Provider Network**
**Operation ID:** `put--vps-api-v1-admin-provider_networks-:{net-id}`

This operation updates attributes of provider network such as name/description/security groups attached.

Parameter in the request body:
- name: New name for this provider network.(optional)
- description: Description for this provider network.(optional)
- sg_ids: The security group IDs associated with this network.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `net-id` | path | string | Yes | Provider Network ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [pb.ProviderNetUpdateInput](../schemas/pb-ProviderNetUpdateInput/pb-ProviderNetUpdateInput.md)

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
