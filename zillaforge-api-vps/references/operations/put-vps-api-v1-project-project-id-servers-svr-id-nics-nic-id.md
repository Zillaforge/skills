# PUT /vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics/:{nic-id}

**Resource:** [server](../resources/server.md)
**update server's vNIC**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-servers-:{svr-id}-nics-:{nic-id}`

Updates ids of security groups assigned to the server’s existing vNICs.

Request example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a/nics/064432b6-f1bd-4e9b-b2d9-d93f3719dd0f' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&ensp;&ensp;"sg_ids": [
&ensp;&ensp;&ensp;&ensp;  "396616bc-6e1a-4e47-ac11-8b3a2e39d2a3",
&ensp;&ensp;&ensp;&ensp;  "71225d34-57fa-45fe-91aa-7e95f15bd881"
&ensp;&ensp;]
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `svr-id` | path | string | Yes | Server ID |
| `nic-id` | path | string | Yes | vNIC ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.NicUpdateInput](../schemas/user-NicUpdateInput/user-NicUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
