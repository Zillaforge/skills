# POST /vps/api/v1/project/:{project-id}/security_groups

**Resource:** [security_group](../resources/security-group.md)
**Create Security Group**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-security_groups`

Creates a security group under current project.

Body parameters :
- name : The name of security group.(required)
- description: Text describing this resource.(optional)
- rules: The initial set of ingress/outgoing traffic policy rule sets.

Each rule contains following fields:
- direction: One of ingress/egress, which is the direction in which the security group rule is applied.(required)
- protocol: The IP protocol can be represented by a string or an integer. \
Valid string or integer values are any or 0, ah or 51, dccp or 33, egp or 8, esp or 50, gre or 47, icmp or 1, icmpv6 or 58, igmp or 2, ipip or 4, ipv6-encap or 41, ipv6-frag or 44, ipv6-icmp or 58, ipv6-nonxt or 59, ipv6-opts or 60, ipv6-route or 43, ospf or 89, pgm or 113, rsvp or 46, sctp or 132, tcp or 6, udp or 17, udplite or 136, vrrp or 112. \
The string any (or integer 0) means all IP protocols.(required)
- remote_cidr: CIDRs allowed access from/to VM instances within same subnet. Only IPv4 cidrs currently support.(required)
- port_min: The minimum port number in the range that is matched by the security group rule. \
If the protocol is TCP, UDP, DCCP, SCTP or UDP-Lite this value must be less than or equal to the port_max attribute value. \
If the protocol is ICMP, this value must be an ICMP type.(optional)
- port_max: The maximum port number in the range that is matched by the security group rule. \
If the protocol is TCP, UDP, DCCP, SCTP or UDP-Lite this value must be greater than or equal to the port_min attribute value. \
If the protocol is ICMP, this value must be an ICMP code.

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/security_groups' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
"name": "sg1736415348416",
"rules": [
&emsp;  {
&emsp;&emsp;"direction": "egress",
&emsp;&emsp;"port_max": 0,
&emsp;&emsp;"port_min": 0,
&emsp;&emsp;"protocol": "any",
&emsp;&emsp;"remote_cidr": "0.0.0.0/0"
&emsp;  }
]
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.SgCreateInput](../schemas/user-SgCreateInput/user-SgCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.SgInfo](../schemas/pb-SgInfo/pb-SgInfo.md)

## Security

- **ApiKeyAuth**
