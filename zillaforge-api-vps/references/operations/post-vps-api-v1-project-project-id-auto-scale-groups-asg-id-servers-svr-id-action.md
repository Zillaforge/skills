# POST /vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers/:{svr-id}/action

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**Do action to AutoScaleGroup's server**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-auto_scale_groups-:{asg-id}-servers-:{svr-id}-action`

Do actions against selected autoscalegroup's member(server), including stop/start/reboot/get_pwd.

Parameter in the request body:
- action : one of stop, start, reboot, get_pwd
- reboot_type : one of "hard" or "soft". Required if action is reboot.
- private_key : The private key of the server for getting password. Base-64 encoded PEM format. Required if action is get_pwd.

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

**Schema:** [user.SvrActionInput](../schemas/user-SvrActionInput/user-SvrActionInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
