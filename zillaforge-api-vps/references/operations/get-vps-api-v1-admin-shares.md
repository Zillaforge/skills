# GET /vps/api/v1/admin/shares

**Resource:** [system_share](../resources/system-share.md)
**List Shares (Admin)**
**Operation ID:** `get--vps-api-v1-admin-shares`

List all shares across all projects with admin privileges. Supports filtering by various parameters.
Query parameters:
- project_id: Filter by project ID
- name: Filter by share name
- status: Filter by share status
- user_id: Filter by user ID
- namespace: Filter by namespace
- network_id: Filter by network ID
- type: Filter by share type
- protocol: Filter by share protocol
- size: Filter by share size
- detail: Set to true to get detailed information

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project_id` | query | string | No | Project ID |
| `name` | query | string | No | Share name |
| `status` | query | string | No | Share status |
| `user_id` | query | string | No | User ID |
| `namespace` | query | string | No | Namespace |
| `network_id` | query | string | No | Network ID |
| `type` | query | string | No | Share type |
| `protocol` | query | string | No | Share protocol |
| `size` | query | string | No | Share size |
| `detail` | query | boolean | No | Get detailed information |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ShareListOutput](../schemas/pb-ShareListOutput/pb-ShareListOutput.md)

