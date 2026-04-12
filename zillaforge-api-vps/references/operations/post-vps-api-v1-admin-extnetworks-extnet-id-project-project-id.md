# POST /vps/api/v1/admin/extnetworks/:{extnet-id}/project/:{project-id}

**Resource:** [system_extnet](../resources/system-extnet.md)
**Associate project with extnetworks**
**Operation ID:** `post--vps-api-v1-admin-extnetworks-:{extnet-id}-project-:{project-id}`

Associates given project with provided external network.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `extnet-id` | path | string | Yes | Ext-Network ID |
| `project-id` | path | string | Yes | Project ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
