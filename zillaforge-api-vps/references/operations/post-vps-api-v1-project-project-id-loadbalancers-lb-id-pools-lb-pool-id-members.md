# POST /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/pools/:{lb-pool-id}/members

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Create Member in Pool**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-pools-:{lb-pool-id}-members`

This operation provisions a member and adds it to a pool.

Parameters in the request body:
- name: The name of member.(optional)
- address: The IPv4 address of the backend member.(required)

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/pools/6892ea37-ff4b-4394-9310-91441dca3a03/members' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&emsp;"address": "192.168.1.2"
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

**Schema:** [user.MemberCreateInput](../schemas/user-MemberCreateInput/user-MemberCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.PoolInfo](../schemas/pb-PoolInfo/pb-PoolInfo.md)

## Security

- **ApiKeyAuth**
