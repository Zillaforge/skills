# DELETE /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/pools/:{lb-pool-id}/members/:{lb-member-id}

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Delete Member in Pool**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-pools-:{lb-pool-id}-members-:{lb-member-id}`

Removes a specific member from a pool.

Request example:
curl -X 'DELETE' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/pools/6892ea37-ff4b-4394-9310-91441dca3a03/members/ef835a66-a6cb-48af-ab75-a26930125ac3' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `lb-id` | path | string | Yes | Load Balancer ID |
| `lb-pool-id` | path | string | Yes | Pool ID |
| `lb-member-id` | path | string | Yes | Member ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
