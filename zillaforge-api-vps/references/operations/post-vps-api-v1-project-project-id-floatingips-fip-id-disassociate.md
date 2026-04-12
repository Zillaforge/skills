# POST /vps/api/v1/project/:{project-id}/floatingips/:{fip-id}/disassociate

**Resource:** [floating_ip](../resources/floating-ip.md)
**Disassociate floatingIP from device**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-floatingips-:{fip-id}-disassociate`

Disassociates the specified floating ip from its attached resource.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `fip-id` | path | string | Yes | FloatingIP ID |

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
