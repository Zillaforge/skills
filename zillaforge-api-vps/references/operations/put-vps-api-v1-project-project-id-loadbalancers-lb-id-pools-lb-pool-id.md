# PUT /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/pools/:{lb-pool-id}

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Update Pool**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-pools-:{lb-pool-id}`

Updates attributes of an existing pool.

Parameters in the request body:
- name: The pool name(optional)
- member_port: The port on which the backend member listens for traffic.(optional)
- method: The load-balancer algorithm, such as ROUND_ROBIN, LEAST_CONNECTIONS and SOURCE_IP, that distributes traffic to the pool members.(optional)
- asg_id: The autoscaling group id. Using the servers in the autoscaling group as the backend member to receive traffic when creating the pool.(optional)

Request example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/pools/6892ea37-ff4b-4394-9310-91441dca3a03' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&emsp;"member_port": 88
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

**Schema:** [user.PoolUpdateInput](../schemas/user-PoolUpdateInput/user-PoolUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.PoolInfo](../schemas/pb-PoolInfo/pb-PoolInfo.md)

## Security

- **ApiKeyAuth**
