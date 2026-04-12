# POST /vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/approve

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**Approve AutoScaleGroup Request**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-auto_scale_groups-:{asg-id}-approve`

This API allows tenant admins to accept requests from other tenant members who are trying to create their own Autoscaling Groups.
Only Tenant Admin has permission to do so!

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `asg-id` | path | string | Yes | AutoScaleGroup ID |

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
