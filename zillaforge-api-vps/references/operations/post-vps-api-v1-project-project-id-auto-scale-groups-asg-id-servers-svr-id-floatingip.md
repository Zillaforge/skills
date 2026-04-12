# POST /vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers/:{svr-id}/floatingip

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**Associate FloatingIP to ASG's server**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-auto_scale_groups-:{asg-id}-servers-:{svr-id}-floatingip`

Associates a floating IP to the target server within an Autoscale Group.
Set the parameter 'fip_id' in the request body with the id of a existing floating ip.
If not set then it will create a newly floating ip. Tenant member needs the tenant admin to approve this creation.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `asg-id` | path | string | Yes | AutoScaleGroup ID |
| `svr-id` | path | string | Yes | Server ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.FIPAssoInput](../schemas/user-FIPAssoInput/user-FIPAssoInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FloatingIPInfo](../schemas/pb-FloatingIPInfo/pb-FloatingIPInfo.md)

## Security

- **ApiKeyAuth**
