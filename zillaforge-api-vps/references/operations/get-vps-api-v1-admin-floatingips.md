# GET /vps/api/v1/admin/floatingips

**Resource:** [system_fip](../resources/system-fip.md)
**List Floating IPs (Admin)**
**Operation ID:** `get--vps-api-v1-admin-floatingips`

List all floating IPs across all projects with admin privileges. Supports filtering by various parameters.
Query parameters:
- id: Filter by floating IP ID
- project_id: Filter by project ID
- name: Filter by floating IP name
- status: Filter by floating IP status
- user_id: Filter by user ID
- namespace: Filter by namespace
- address: Filter by IP address
- reserved: Filter by reserved status
- device_id: Filter by device ID
- extnet_id: Filter by external network ID
- state: Filter by state
- detail: Set to true to get detailed information

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | query | string | No | Floating IP ID |
| `project_id` | query | string | No | Project ID |
| `name` | query | string | No | Floating IP name |
| `status` | query | string | No | Floating IP status |
| `user_id` | query | string | No | User ID |
| `namespace` | query | string | No | Namespace |
| `address` | query | string | No | IP address |
| `reserved` | query | boolean | No | Reserved status |
| `device_id` | query | string | No | Device ID |
| `extnet_id` | query | string | No | External network ID |
| `state` | query | string | No | State |
| `detail` | query | boolean | No | Get detailed information |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FIPListOutput](../schemas/pb-FIPListOutput/pb-FIPListOutput.md)

