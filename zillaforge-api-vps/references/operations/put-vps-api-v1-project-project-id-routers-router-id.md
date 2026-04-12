# PUT /vps/api/v1/project/:{project-id}/routers/:{router-id}

**Resource:** [router](../resources/router.md)
**Update Router**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-routers-:{router-id}`

Updates the name or description of a router.

Request Body Parameters:
- Name: New name of the router.(Optional)
- Description: New description of the router.(Optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `router-id` | path | string | Yes | Router ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.RouterUpdateInput](../schemas/user-RouterUpdateInput/user-RouterUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.RouterInfo](../schemas/pb-RouterInfo/pb-RouterInfo.md)

## Security

- **ApiKeyAuth**
