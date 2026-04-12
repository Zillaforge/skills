# POST /vps/api/v1/project/:{project-id}/loadbalancers/:{lb-id}/floatingip

**Resource:** [loadbalancer](../resources/loadbalancer.md)
**Associate FloatingIP to load balancer**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-loadbalancers-:{lb-id}-floatingip`

Associates a floating IP to the private vip of a load balancer.
Set the parameter 'fip_id' in the body with the id of a existing floating ip.
If not set then it will create a newly floating ip. Tenant member needs the tenant admin to review this creation.

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/loadbalancers/0485cb89-d1a4-4ad3-b8a7-cf28481ce27c/floatingip' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&ensp;&ensp;"fip_id": "9078e07a-239b-4efb-bbfa-0bf7460c4f79"
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

**Schema:** [user.FIPAssoInput](../schemas/user-FIPAssoInput/user-FIPAssoInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FloatingIPInfo](../schemas/pb-FloatingIPInfo/pb-FloatingIPInfo.md)

## Security

- **ApiKeyAuth**
