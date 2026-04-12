# DELETE /vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**Delete AutoScaleGroup**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-auto_scale_groups-:{asg-id}`

Remove an autoscale group. This operation will terminate instances belonging to ASGs. This action cannot revert back once performed!

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
