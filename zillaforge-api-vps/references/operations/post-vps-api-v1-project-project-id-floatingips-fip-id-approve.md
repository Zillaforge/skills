# POST /vps/api/v1/project/:{project-id}/floatingips/:{fip-id}/approve

**Resource:** [floating_ip](../resources/floating-ip.md)
**Approve floatingIP request**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-floatingips-:{fip-id}-approve`

Approves pending request made through API call to create a floating IP.
Only tenanet admin users are allowed to call this api.

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
