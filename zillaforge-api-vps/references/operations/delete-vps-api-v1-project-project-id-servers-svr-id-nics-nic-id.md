# DELETE /vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics/:{nic-id}

**Resource:** [server](../resources/server.md)
**Remove a vNIC from Server**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-servers-:{svr-id}-nics-:{nic-id}`

Removes a specific virtual NIC from its associated server.

Request example:
curl -X 'DELETE' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a/nics/171a4af0-b904-4239-bdce-0a5e17cf1828' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `svr-id` | path | string | Yes | Server ID |
| `nic-id` | path | string | Yes | vNIC ID |

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
