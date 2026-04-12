# POST /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/pools

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Create Pool in Load Balaner**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-pools`

Creates a pool under a specific load balancer.

Parameters in the request body:
- name: The pool name(required)
- protocol: The protocol for which this pool and its members listen. A valid value is HTTP, HTTPS, TCP, or UDP.(required)
- member_port: The port on which the backend member listens for traffic.(required)
- method: The load-balancer algorithm, such as ROUND_ROBIN, LEAST_CONNECTIONS and SOURCE_IP, that distributes traffic to the pool members.(required)
- asg_id: The autoscaling group id. Using the servers in the autoscaling group as the backend member to receive traffic when creating the pool.(optional)
- members: A JSON array containing information about each desired member(server).(optional)

Member elements should have following fields:
- name: The name of member.(optional)
- address: The IPv4 address of the backend member.(required)

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/pools/' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&emsp;"member_port": 80,
&emsp;"members": [
&emsp;&emsp;  {
&emsp;&emsp;&emsp;    "address": "192.168.155.54",
&emsp;&emsp;&emsp;    "name": "vm1735552353"
&emsp;&emsp;  }
&emsp;],
&emsp;"method": "ROUND_ROBIN",
&emsp;"name": "target1736390395",
&emsp;"protocol": "HTTP"
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

**Schema:** [user.PoolCreateInput](../schemas/user-PoolCreateInput/user-PoolCreateInput.md)

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
