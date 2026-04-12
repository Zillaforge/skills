# GET /vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**List servers created by AutoScaleGroup**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-auto_scale_groups-:{asg-id}-servers`

Return servers associated with given ASG Id.

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

[pb.AsgServerListOutput](../schemas/pb-AsgServerListOutput/pb-AsgServerListOutput.md)

## Security

- **ApiKeyAuth**
