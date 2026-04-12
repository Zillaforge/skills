# POST /vps/api/v1/project/:{project-id}/networks

**Resource:** [network](../resources/network.md)
**Create Network (tenant_admin only)**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-networks`

Creates a network for specified project.

Request Body Parameters:
- name: The network's display name.(required)
- description: Description of the network.(optional)
- cidr: CIDR block used for subnet allocation within the network.(required)
- gateway: Gateway ip address inside CIDR Block.(optional)
- router_id: The router UUID which will connect the created network to it.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.NetCreateInput](../schemas/user-NetCreateInput/user-NetCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.NetworkInfo](../schemas/pb-NetworkInfo/pb-NetworkInfo.md)

## Security

- **ApiKeyAuth**
