# GET /vps/api/v1/project/:{project-id}/loadbalancers

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**List Load Balancers**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-loadbalancers`

Lists all load balancers for the project. Search parameter is optional.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/?detail=true' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id(adm only) |
| `detail` | query | boolean | No | if true, return loadbalancer with listeners and pools |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.LbListOutput](../schemas/pb-LbListOutput/pb-LbListOutput.md)

## Security

- **ApiKeyAuth**
