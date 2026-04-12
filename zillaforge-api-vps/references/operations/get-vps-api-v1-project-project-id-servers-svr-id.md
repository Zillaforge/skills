# GET /vps/api/v1/project/:{project-id}/servers/:{svr-id}

**Resource:** [server](../resources/server.md)
**Get Server**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-servers-:{svr-id}`

Return server detailed information of the given server id
Example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `svr-id` | path | string | Yes | Server ID |

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
