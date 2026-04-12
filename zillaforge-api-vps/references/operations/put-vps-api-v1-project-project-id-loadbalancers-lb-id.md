# PUT /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Update Load Balancer**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}`

Updates name or description of a load balancer.

Parameters in the request body:
- name : New value for the name field(optional)
- descirption : New value for the description field(optional)

Request example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&ensp;&ensp;"description": "newDescription",
&ensp;&ensp;"name": "newName"
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `lb-id` | path | string | Yes | Load Balancer ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.LbUpdateInput](../schemas/user-LbUpdateInput/user-LbUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.LbInfo](../schemas/pb-LbInfo/pb-LbInfo.md)

## Security

- **ApiKeyAuth**
