# POST /vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics

**Resource:** [server](../resources/server.md)
**Add a new vNIC to Server**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-servers-:{svr-id}-nics`

Adds a new virtual NIC to the given server.

The following parameters must be provided in the POST payload:

- network_id -- UUID representing which private network should serve as parent interface.
- sg_ids -- Array containing ids of security group(s), that need to apply to newly added nics.
- fixed_ip(optional) -- An ip from subnet defined under selected network; If no fixed Ip was supplied then it'll try to allocate next free ip based upon availability range configured at neutron level.

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a/nics' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&ensp;&ensp;"network_id": "5a66fd8d-f405-4ae6-9835-b6ba1220cdc7",
&ensp;&ensp;"sg_ids": [
&ensp;&ensp;&ensp;&ensp;"396616bc-6e1a-4e47-ac11-8b3a2e39d2a3"
&ensp;&ensp;]
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `svr-id` | path | string | Yes | Server ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.NicCreateInput](../schemas/user-NicCreateInput/user-NicCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
