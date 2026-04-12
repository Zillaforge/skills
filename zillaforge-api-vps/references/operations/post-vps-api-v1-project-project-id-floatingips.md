# POST /vps/api/v1/project/:{project-id}/floatingips/

**Resource:** [floating_ip](../resources/floating-ip.md)
**Create floatingIP**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-floatingips-`

Creates a new floating IP.

Request body parameters:
- name: Name of Floating Ip Address.(optional)
- description: Description of Floating Ip Address.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.FIPCreateInput](../schemas/user-FIPCreateInput/user-FIPCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FloatingIPInfo](../schemas/pb-FloatingIPInfo/pb-FloatingIPInfo.md)

## Security

- **ApiKeyAuth**
