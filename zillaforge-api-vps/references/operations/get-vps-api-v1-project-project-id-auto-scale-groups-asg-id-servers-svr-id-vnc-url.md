# GET /vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers/:{svr-id}/vnc_url

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**Get VNC console URL (asg's owner only)**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-auto_scale_groups-:{asg-id}-servers-:{svr-id}-vnc_url`

Gets the URL used to connect to the VNC console for a server in asg.

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

[pb.ServerConsoleURLOutput](../schemas/pb-ServerConsoleURLOutput/pb-ServerConsoleURLOutput.md)

## Security

- **ApiKeyAuth**
