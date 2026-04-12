# PUT /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/listeners/:{lb-listener-id}

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Update Listener**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-listeners-:{lb-listener-id}`

Updates attributes of existing listener identified by its UUID.

Parameters in the request body:
- name: The name of listener.(optional)
- insert_headers: A dictionary of optional headers to insert into the request before it is sent to the backend member. (optional)
&ensp;&ensp;- X-Forwarded-For: When “true” a X-Forwarded-For header is inserted into the request to the backend member that specifies the client IP address.
&ensp;&ensp;- X-Forwarded-Port: When “true” a X-Forwarded-Port header is inserted into the request to the backend member that specifies the listener port.
&ensp;&ensp;- X-Forwarded-Proto: When “true” a X-Forwarded-Proto header is inserted into the request to the backend member. HTTP for the HTTP listener protocol type, HTTPS for the TERMINATED_HTTPS listener protocol type.
- timeout_client_data: Frontend client inactivity timeout in milliseconds. Default: 50000.(optional)
- timeout_member_connect: Backend member connection timeout in milliseconds. Default: 5000.(optional)
- timeout_member_data: Backend member inactivity timeout in milliseconds. Default: 50000.(optional)
- timeout_tcp_inspect: Time, in milliseconds, to wait for additional TCP packets for content inspection. Default: 0.(optional)
- allowed_cidrs: A list of IPv4 CIDRs from which connections may come into your load balancer. The default is all allowed. When a list of CIDRs is provided, the default switches to deny all.(optional)
- pool_id: The ID of the pool associated to the listener. (optional)
- secret: Containing the PKCS12 format certificate and key for TERMINATED_HTTPS listeners. Must be Base64 encoded.(optional)

Request example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/listeners/6c5071b2-57d7-48cb-830d-2d48d981cab1' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
"allowed_cidrs": [
&emsp;"1.1.0.1/32"
]
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `lb-id` | path | string | Yes | Load Balancer ID |
| `lb-listener-id` | path | string | Yes | Listener ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.ListenerUpdateInput](../schemas/user-ListenerUpdateInput/user-ListenerUpdateInput.md)

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
