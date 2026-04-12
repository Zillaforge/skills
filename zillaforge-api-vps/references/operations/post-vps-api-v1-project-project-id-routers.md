# POST /vps/api/v1/project/:{project-id}/routers

**Resource:** [router](../resources/router.md)
**Create Router (tenant_admin only)**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-routers`

Create new router under current project.

Request Body Parameters:
- name: name of the router.(required)
- description: description about it.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.RouterCreateInput](../schemas/user-RouterCreateInput/user-RouterCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.RouterInfo](../schemas/pb-RouterInfo/pb-RouterInfo.md)

## Security

- **ApiKeyAuth**
