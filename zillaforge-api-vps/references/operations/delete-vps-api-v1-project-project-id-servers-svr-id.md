# DELETE /vps/api/v1/project/:{project-id}/servers/:{svr-id}

**Resource:** [server](../resources/server.md)
**Delete Server**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-servers-:{svr-id}`

Deletes a server.
The ports attached to the server are also deleted.
Example:
curl -X 'DELETE' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `svr-id` | path | string | Yes | Server ID |

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
