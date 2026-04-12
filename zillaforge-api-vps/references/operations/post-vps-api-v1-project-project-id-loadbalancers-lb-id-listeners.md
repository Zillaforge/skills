# POST /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/listeners

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Create Listener in Load Balaner**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-listeners`

Creates listener under the specific load balancer.

Parameters in the request body:
- protocol: The protocol for the listener. One of HTTP, HTTPS, TERMINATED_HTTPS, TCP or UDP.(required)
- protocol_port: Port number associated with the listener.(required)
- name: The name of listener.(optional)
- timeout_client_data: Frontend client inactivity timeout in milliseconds. Default: 50000.(optional)
- timeout_member_connect: Backend member connection timeout in milliseconds. Default: 5000.(optional)
- timeout_member_data: Backend member inactivity timeout in milliseconds. Default: 50000.(optional)
- timeout_tcp_inspect: Time, in milliseconds, to wait for additional TCP packets for content inspection. Default: 0.(optional)
- allowed_cidrs: A list of IPv4 CIDRs from which connections may come into your load balancer. The default is all allowed. When a list of CIDRs is provided, the default switches to deny all.(optional)
- insert_headers: A dictionary of optional headers to insert into the request before it is sent to the backend member. (optional)
&ensp;&ensp;- X-Forwarded-For: When “true” a X-Forwarded-For header is inserted into the request to the backend member that specifies the client IP address.
&ensp;&ensp;- X-Forwarded-Port: When “true” a X-Forwarded-Port header is inserted into the request to the backend member that specifies the listener port.
&ensp;&ensp;- X-Forwarded-Proto: When “true” a X-Forwarded-Proto header is inserted into the request to the backend member. HTTP for the HTTP listener protocol type, HTTPS for the TERMINATED_HTTPS listener protocol type.
- secret: Containing the PKCS12 format certificate and key for TERMINATED_HTTPS listeners. Must be Base64 encoded.(optional)
- pool_id: The ID of the pool used by the listener. (optional)

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/listeners/' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
"allowed_cidrs": [
&emsp;  "1.1.1.0/24"
],
"insert_headers": {
&emsp;  "X-Forwarded-For": "true",
&emsp;  "X-Forwarded-Proto": "false",
&emsp;  "X-Forwarded-Port": "false"
},
"name": "listener1736319245251",
"protocol": "HTTP",
"protocol_port": 80,
"timeout_client_data": 50000,
"timeout_member_connect": 5000,
"timeout_member_data": 50000,
"timeout_tcp_inspect": 0
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

**Schema:** [user.ListenerCreateInput](../schemas/user-ListenerCreateInput/user-ListenerCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ListenerInfo](../schemas/pb-ListenerInfo/pb-ListenerInfo.md)

## Security

- **ApiKeyAuth**
