# PUT /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/pools/:{lb-pool-id}/members

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Batch Update Members in Pool**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-pools-:{lb-pool-id}-members`

Updates multiple members at once using JSON array input

Parameters in the request body:
- members: A JSON array containing information about each desired member.

Member elements should have following fields:
- name: The name of member.(optional)
- address: The IPv4 address of the backend member.(required)

Request example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/pools/6892ea37-ff4b-4394-9310-91441dca3a03/members' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
"members": [
&emsp;{
&emsp;&emsp;  "address": "192.168.1.2"
&emsp;}
]
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `lb-id` | path | string | Yes | Load Balancer ID |
| `lb-pool-id` | path | string | Yes | Pool ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.MembersUpdateInput](../schemas/user-MembersUpdateInput/user-MembersUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
