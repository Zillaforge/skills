# GET /vps/api/v1/admin/loadbalancers/:{lb-id}

**Resource:** [system_loadbalancer](../resources/system-loadbalancer.md)
**Get Load Balancer (Admin)**
**Operation ID:** `get--vps-api-v1-admin-loadbalancers-:{lb-id}`

Get detailed information about a specific load balancer with admin privileges.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `lb-id` | path | string | Yes | Load Balancer ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.LbInfo](../schemas/pb-LbInfo/pb-LbInfo.md)

