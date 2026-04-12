# DELETE /vps/api/v1/project/:{project-id}/floatingips/:{fip-id}

**Resource:** [floating_ip](../resources/floating-ip.md)
**Delete floatingIP**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-floatingips-:{fip-id}`

Deletes the specified floating ip address if exists.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `fip-id` | path | string | Yes | FloatingIP ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
