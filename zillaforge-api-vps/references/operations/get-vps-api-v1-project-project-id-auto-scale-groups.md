# GET /vps/api/v1/project/:{project-id}/auto_scale_groups/

**Resource:** [auto_scale_group](../resources/auto-scale-group.md)
**List AutoScaleGroup**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-auto_scale_groups-`

List all autoscale groups of a given Project.
Filter parameter : name, user_id, status , image, flavor, network.
Parameter 'detail' equals to "True", return more information.

Request example:
curl -X 'GET' 'https://localhost:9999/api/v1/project/87659158-4d37-4742-9f83-3e0cd6494b80/auto_scale_groups/?status=ACTIVE&detail=true'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id |
| `status` | query | string | No | search by status |
| `image_id` | query | string | No | search by image |
| `flavor_id` | query | string | No | search by flavor |
| `network_id` | query | string | No | search by network |
| `detail` | query | boolean | No | get detail infomations |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.AsgListOutput](../schemas/pb-AsgListOutput/pb-AsgListOutput.md)

## Security

- **ApiKeyAuth**
