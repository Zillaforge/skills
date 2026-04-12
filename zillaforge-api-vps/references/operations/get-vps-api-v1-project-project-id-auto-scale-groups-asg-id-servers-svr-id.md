# GET /vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers/:{svr-id}

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**Get AutoScaleGroup's server info**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-auto_scale_groups-:{asg-id}-servers-:{svr-id}`

Return detailed information regarding one particular server being managed by ASG.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `asg-id` | path | string | Yes | AutoScaleGroup ID |
| `svr-id` | path | string | Yes | Server ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.AsgServerInfo](../schemas/pb-AsgServerInfo/pb-AsgServerInfo.md)

## Security

- **ApiKeyAuth**
