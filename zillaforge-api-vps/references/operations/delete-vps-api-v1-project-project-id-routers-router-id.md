# DELETE /vps/api/v1/project/:{project-id}/routers/:{router-id}

**Resource:** [router](../resources/router.md)
**Delete Router**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-routers-:{router-id}`

Deletes a router which is not in-use and not created with network.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `router-id` | path | string | Yes | Router ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
