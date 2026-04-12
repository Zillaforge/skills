# GET /vps/api/v1/project/:{project-id}/routers/:{router-id}

**Resource:** [router](../resources/router.md)
**Get Router**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-routers-:{router-id}`

Retrieve detailed information of a router.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `router-id` | path | string | Yes | Router ID |

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
