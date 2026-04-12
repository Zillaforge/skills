# GET /vps/api/v1/admin/servers/:{svr-id}

**Resource:** [system_server](../resources/system-server.md)
**Get Server (Admin)**
**Operation ID:** `get--vps-api-v1-admin-servers-:{svr-id}`

Get detailed information about a specific server with admin privileges.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `svr-id` | path | string | Yes | Server ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ServerInfo](../schemas/pb-ServerInfo/pb-ServerInfo.md)

