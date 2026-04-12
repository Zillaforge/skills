# GET /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/listeners/:{lb-listener-id}

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Get Listener**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-listeners-:{lb-listener-id}`

Returns details about the listener with the given id.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/listeners/6c5071b2-57d7-48cb-830d-2d48d981cab1' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `lb-id` | path | string | Yes | Load Balancer ID |
| `lb-listener-id` | path | string | Yes | Listener ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ListenerInfo](../schemas/pb-ListenerInfo/pb-ListenerInfo.md)

## Security

- **ApiKeyAuth**
