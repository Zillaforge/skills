# PUT /vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**Update AutoScaleGroup**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-auto_scale_groups-:{asg-id}`

Updates attributes of the autocale group.

Request Body Parameters :
- name: New name of the asg.(optional)
- description: New description for the asg.(optional)
- min_size: New minimum size of servers allowed in asg.(optional)
- max_size: New maximum size of servers allowed in asg.(optional)
- threshold_up: New percentage value above which server instances should scale up when triggering based on selected metrics. Value between 1~99.(optional)
- threshold_down: New percentage value below which server instances should scale down when triggering based on selected metrics. Value between 1~99.(optional)
- sg_ids: New ids of security groups assigned to every instance launched into autoscale group. (optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `asg-id` | path | string | Yes | AutoScaleGroup ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.AsgUpdateInput](../schemas/user-AsgUpdateInput/user-AsgUpdateInput.md)

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
