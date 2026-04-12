# POST /vps/api/v1/project/:{project-id}/loadbalancers

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Create Load Balancer**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-loadbalancers`

Creates a load balancer.
The network must belong to this project namespace.
You can create a fully populated load balancer by specifying the additional attributes of listener(s) and pool(s) in the request.

Request body parameters :
- name: The load balancer name (required)
- description : Description for the load balancer (optional)
- network_id: The network UUID that will host the load balancer VIP address (required)
- listeners: A JSON array containing information about each desired listener (optional)

Each listener element should contain these fields:
- protocol: The protocol for the listener. One of HTTP, HTTPS, TERMINATED_HTTPS, TCP or UDP.(required)
- protocol_port: Port number associated with the listener(required)
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
- pool: Create a pool object used by the listener. The pool defines how requests should be balanced across the backend member servers.

Pool element should contain these fields:
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
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&emsp;"name": "lb1736319244887",
&emsp;"description": "",
&emsp;"network_id": "bc10c427-a12e-4eee-a5fd-00319f5bbaf1",
&emsp;"listeners": [
&emsp;&emsp;{
&emsp;&emsp;&emsp;"name": "listener1736319245251",
&emsp;&emsp;&emsp;"protocol": "HTTP",
&emsp;&emsp;&emsp;"protocol_port": 80,
&emsp;&emsp;&emsp;"timeout_client_data": 50000,
&emsp;&emsp;&emsp;"timeout_member_connect": 5000,
&emsp;&emsp;&emsp;"timeout_member_data": 50000,
&emsp;&emsp;&emsp;"timeout_tcp_inspect": 0,
&emsp;&emsp;&emsp;"insert_headers": {
&emsp;&emsp;&emsp;&emsp;"X-Forwarded-For": "true",
&emsp;&emsp;&emsp;&emsp;"X-Forwarded-Proto": "false",
&emsp;&emsp;&emsp;&emsp;"X-Forwarded-Port": "false"
&emsp;&emsp;&emsp;},
&emsp;&emsp;&emsp;"allowed_cidrs": [
&emsp;&emsp;&emsp;&emsp;"1.1.1.0/24"
&emsp;&emsp;&emsp;],
&emsp;&emsp;&emsp;"pool": {
&emsp;&emsp;&emsp;&emsp;"name": "pool1736319245251",
&emsp;&emsp;&emsp;&emsp;"protocol": "HTTP",
&emsp;&emsp;&emsp;&emsp;"member_port": 80,
&emsp;&emsp;&emsp;&emsp;"members": [
&emsp;&emsp;&emsp;&emsp;&emsp;{
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;"name": "vm1735552353",
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;"address": "192.168.155.54"
&emsp;&emsp;&emsp;&emsp;&emsp;}
&emsp;&emsp;&emsp;&emsp;],
&emsp;&emsp;&emsp;&emsp;"method": "LEAST_CONNECTIONS"
&emsp;&emsp;&emsp;}
&emsp;&emsp;}
&emsp;]
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.LbCreateInput](../schemas/user-LbCreateInput/user-LbCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.LbInfo](../schemas/pb-LbInfo/pb-LbInfo.md)

## Security

- **ApiKeyAuth**
