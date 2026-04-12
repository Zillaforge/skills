# GET /vps/api/v1/admin/servers

**Resource:** [system_server](../resources/system-server.md)
**List Servers (Admin)**
**Operation ID:** `get--vps-api-v1-admin-servers`

List all servers across all projects with admin privileges. Supports filtering by various parameters.
Query parameters:
- project_id: Filter by project ID
- name: Filter by server name
- user_id: Filter by user ID
- status: Filter by server status
- image_id: Filter by image ID
- flavor_id: Filter by flavor ID
- az: Filter by availability zone
- namespace: Filter by namespace
- detail: Set to true to get detailed server information

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project_id` | query | string | No | Project ID |
| `name` | query | string | No | Server name |
| `user_id` | query | string | No | User ID |
| `status` | query | string | No | Server status |
| `image_id` | query | string | No | Image ID |
| `flavor_id` | query | string | No | Flavor ID |
| `az` | query | string | No | Availability zone |
| `namespace` | query | string | No | Namespace |
| `detail` | query | boolean | No | Get detailed information |

## Responses

| Status | Description |
|--------|-------------|
| 400 | Bad Request |
| 500 | Internal Server Error |

