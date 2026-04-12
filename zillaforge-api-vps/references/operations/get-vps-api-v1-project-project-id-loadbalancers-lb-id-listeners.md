# GET /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/listeners

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**List Listeners**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-listeners`

Lists listeners associated with this load balancer.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/listeners/' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `lb-id` | path | string | Yes | Load Balancer ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ListenerListOutput](../schemas/pb-ListenerListOutput/pb-ListenerListOutput.md)

## Security

- **ApiKeyAuth**
