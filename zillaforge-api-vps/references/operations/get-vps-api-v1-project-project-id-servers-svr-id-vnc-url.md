# GET /vps/api/v1/project/:{project-id}/servers/:{svr-id}/vnc_url

**Resource:** [server](../resources/server.md)
**Get VNC console URL (server's owner only)**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-servers-:{svr-id}-vnc_url`

Gets the URL used to connect to the VNC console for a server.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a/vnc_url' \
-H 'accept: application/json'

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

[pb.ServerConsoleURLOutput](../schemas/pb-ServerConsoleURLOutput/pb-ServerConsoleURLOutput.md)

## Security

- **ApiKeyAuth**
