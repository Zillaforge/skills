# PUT /vps/api/v1/project/:{project-id}/servers/:{svr-id}

**Resource:** [server](../resources/server.md)
**Update Server**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-servers-:{svr-id}`

Updates the name or description of an existing server.
Request Body Format:
{"Name":"test-server","Description":""}
Example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a' \
-d '{
&ensp;&ensp;"name": "edit name"
&ensp;&ensp;"description": "edit description",
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

**Schema:** [user.SvrUpdateInput](../schemas/user-SvrUpdateInput/user-SvrUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ServerInfo](../schemas/pb-ServerInfo/pb-ServerInfo.md)

## Security

- **ApiKeyAuth**
