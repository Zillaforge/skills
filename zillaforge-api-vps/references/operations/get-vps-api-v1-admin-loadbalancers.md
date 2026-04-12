# GET /vps/api/v1/admin/loadbalancers

**Resource:** [system_loadbalancer](../resources/system-loadbalancer.md)
**List Load Balancers (Admin)**
**Operation ID:** `get--vps-api-v1-admin-loadbalancers`

List all load balancers across all projects with admin privileges. Supports filtering by various parameters.
Query parameters:
- project_id: Filter by project ID
- name: Filter by load balancer name
- status: Filter by load balancer status
- user_id: Filter by user ID
- namespace: Filter by namespace
- network_id: Filter by network ID
- detail: Set to true to get detailed information

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project_id` | query | string | No | Project ID |
| `name` | query | string | No | Load balancer name |
| `status` | query | string | No | Load balancer status |
| `user_id` | query | string | No | User ID |
| `namespace` | query | string | No | Namespace |
| `network_id` | query | string | No | Network ID |
| `detail` | query | boolean | No | Get detailed information |

## Responses

| Status | Description |
|--------|-------------|
| 400 | Bad Request |
| 500 | Internal Server Error |

