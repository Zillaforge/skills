# GET /vps/api/v1/admin/auto_scale_groups/:{asg-id}

**Resource:** [system_asg](../resources/system-asg.md)
**Get Auto Scaling Group (Admin)**
**Operation ID:** `get--vps-api-v1-admin-auto_scale_groups-:{asg-id}`

Get detailed information about a specific auto scaling group with admin privileges.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `asg-id` | path | string | Yes | Auto Scaling Group ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.AsgInfo](../schemas/pb-AsgInfo/pb-AsgInfo.md)

