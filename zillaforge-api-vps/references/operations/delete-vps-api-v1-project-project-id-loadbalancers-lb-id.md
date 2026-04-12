# DELETE /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Delete Load Balancer**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}`

Deletes the specified load balancer.
This API will delete all child objects of the load balancer.
curl -X 'DELETE' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `lb-id` | path | string | Yes | Load Balancer ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
