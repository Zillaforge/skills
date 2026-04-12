# POST /vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics/:{nic-id}/floatingip

**Resource:** [server](../resources/server.md)
**Associate FloatingIP to a vNIC**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-servers-:{svr-id}-nics-:{nic-id}-floatingip`

Associates a floating IP to a specific vNIC attached to a given server.
Set the parameter 'fip_id' in the body with the id of a existing floating ip.
If not set then it will create a newly floating ip. Tenant member needs the tenant admin to review this creation.

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a/nics/064432b6-f1bd-4e9b-b2d9-d93f3719dd0f/floatingip' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&ensp;&ensp;"fip_id": "9078e07a-239b-4efb-bbfa-0bf7460c4f79"
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `svr-id` | path | string | Yes | Server ID |
| `nic-id` | path | string | Yes | vNIC ID |

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
