# GET /vps/api/v1/admin/auto_scale_groups

**Resource:** [system_asg](../resources/system-asg.md)
**List Auto Scaling Groups (Admin)**
**Operation ID:** `get--vps-api-v1-admin-auto_scale_groups`

List all auto scaling groups across all projects with admin privileges. Supports filtering by various parameters.
Query parameters:
- project_id: Filter by project ID
- name: Filter by auto scaling group name
- status: Filter by auto scaling group status
- user_id: Filter by user ID
- namespace: Filter by namespace
- network_id: Filter by network ID
- flavor_id: Filter by flavor ID
- detail: Set to true to get detailed information

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project_id` | query | string | No | Project ID |
| `name` | query | string | No | Auto scaling group name |
| `status` | query | string | No | Auto scaling group status |
| `user_id` | query | string | No | User ID |
| `namespace` | query | string | No | Namespace |
| `network_id` | query | string | No | Network ID |
| `flavor_id` | query | string | No | Flavor ID |
| `detail` | query | boolean | No | Get detailed information |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.AsgListOutput](../schemas/pb-AsgListOutput/pb-AsgListOutput.md)

