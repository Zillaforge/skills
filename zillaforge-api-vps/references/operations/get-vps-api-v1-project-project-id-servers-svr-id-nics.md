# GET /vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics

**Resource:** [server](../resources/server.md)
**List Server's vNICs**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-servers-:{svr-id}-nics`

List all vNICs associated with this server.
vNIC info includes MAC addr, IP addresses, security groups, etc.

Request Example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a/nics' \
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

[pb.ServerNICListOutput](../schemas/pb-ServerNICListOutput/pb-ServerNICListOutput.md)

## Security

- **ApiKeyAuth**
