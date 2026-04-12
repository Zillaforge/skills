# POST /vps/api/v1/project/:{project-id}/servers

**Resource:** [server](../resources/server.md)
**Create Server**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-servers`

Create new server with specified parameters.

Parameter in request body:
- name : The server name (required)
- description : Description for the server (optional)
- flavor_id : The id of the flavor for your server instance (required)
- image_id : The id of the image to use for your server instance (required)
- nics : The network information array which contains following fields: network_id and sg_ids,(required)
&ensp;&ensp;- network_id : The id of the network to provision the server instance with a NIC on it.(required)
&ensp;&ensp;- sg_ids : The id of the security group. One or more security groups.(required)
- volume_ids (Deprecated):The id of existed volumes attached to this server(optional).
- volumes :The volume array attached to the server which contains following fields:
&ensp;&ensp;- volume_id : The id of an existing volume that you want to attach to the server instance.(optional)
&ensp;&ensp;- name : The name of the newly-created volume. Required for creating a new volume.
&ensp;&ensp;- type : The volume type of the newly-created volume. Required for creating a new volume.
&ensp;&ensp;- size : The size of the newly created volume. Required for creating a new volume.
- keypair_id : The id of keypair used when launching instances. Requiered if no password provided.
- password : The administrative password of the server. Must be Base64 encoded.(optional)
- boot_script : Configuration information or scripts to use upon launch. Must be Base64 encoded.(optional)

Request Example :
curl -X 'POST' \
'https://localhost:9999/api/v1/project/2F871a0333-ae33-43f2-81f9-2432fa15cde7/servers/' \
-d '{
&ensp;&ensp;"name": "server1",
&ensp;&ensp;"description": "",
&ensp;&ensp;"image_id": "aac1e6b5-2d20-4292-9ce1-7e01bf49c88f",
&ensp;&ensp;"flavor_id": "3fe78aca-3ac7-4051-a1f0-5baf3d20443f",
&ensp;&ensp;"nics": [
&ensp;&ensp;&ensp;&ensp;{
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;"network_id": "bc10c427-a12e-4eee-a5fd-00319f5bbaf1",
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;"sg_ids": [
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;"396616bc-6e1a-4e47-ac11-8b3a2e39d2a3"
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;]
&ensp;&ensp;&ensp;&ensp;}
&ensp;&ensp;],
&ensp;&ensp;"volumes": [
&ensp;&ensp;&ensp;&ensp;{
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;"volume_id":null,
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;"name":"vol1735806385",
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;"size":10,
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;"type":"SSD"
&ensp;&ensp;&ensp;&ensp;}
&ensp;&ensp;],
&ensp;&ensp;"password": "OGJzdFEha1guUmJGVk5u",
&ensp;&ensp;"keypair_id": "0f026b25-b720-4329-96b9-c4229f6d3e50",
&ensp;&ensp;"boot_script": "I2Nsb3VkLWNvbmZpZwpib290Y21kOgotIHNlZCAtaSAiMXMvJC8gJChob3N0bmFtZSB8IHRyICdcbicgJyAnKS8iIC9ldGMvaG9zdHM="
&ensp;&ensp;"system_volume_type": name or volume type to use for system volume.(optional)
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.SvrCreateInput](../schemas/user-SvrCreateInput/user-SvrCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ServerInfo](../schemas/pb-ServerInfo/pb-ServerInfo.md)

## Security

- **ApiKeyAuth**
