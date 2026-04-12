# GET /vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**Get AutoScaleGroup**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-auto_scale_groups-:{asg-id}`

Returns detailed information regarding given autocale group id.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `asg-id` | path | string | Yes | AutoScaleGroup ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.AsgInfo](../schemas/pb-AsgInfo/pb-AsgInfo.md)

## Security

- **ApiKeyAuth**
