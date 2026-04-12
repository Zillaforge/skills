# POST /vps/api/v1/project/:{project-id}/auto_scale_groups/

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**Create AutoScaleGroup**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-auto_scale_groups-`

Create an autoscale group for the specified parameters and returns its details on success.

Request Body Parameters :
- name: Name of the autoscale group.(required)
- description: Description about the autoscale group.(optional)
- min_size: Minimum number of servers allowed in asg. Default is 1.(optional)
- max_size: Maximum number of servers allowed in asg.(required).
- metric: Metric used to trigger scaling action. Must be one of "cpu" or "memory".(required)
- threshold_up: Percentage above which server instances will scale up when triggered based on selected metrics. Value between 1~99.(required)
- threshold_down: Percentage below which server instances will scale down when triggered based on selected metrics. Value between 1~99.(required)
- flavor_id: Flavor UUID to launch upon creation of each member of the autoscaling group.(required)
- image_id: Image UUID associated with server created within autoscale Group.(required)
- network_id: Network UUID attached to members of the autoscaling group.(required)
- sg_ids: Security groups IDs assigned to every instance launched into autoscale group.(array)(required)
- keypair_id: Keypair ID will be used when launching servers. Requiered if no password provided.
- password: Password set at time of creating server instance from Autoscale Group. Must be Base64 encoded.(optional)
- boot_script: Configuration information or scripts to use upon server launch. Must be Base64 encoded.(optional)
- system_volume_type: name of volume type to use for system volume.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.AsgCreateInput](../schemas/user-AsgCreateInput/user-AsgCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.AsgInfo](../schemas/pb-AsgInfo/pb-AsgInfo.md)

## Security

- **ApiKeyAuth**
