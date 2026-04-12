# GET /vps/api/v1/project/:{project-id}/floatingips/:{fip-id}

**Resource:** [floating_ip](../resources/floating-ip.md)
**Get floatingIP**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-floatingips-:{fip-id}`

Return detailed information of specified floating ip.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `fip-id` | path | string | Yes | FloatingIP ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FloatingIPInfo](../schemas/pb-FloatingIPInfo/pb-FloatingIPInfo.md)

## Security

- **ApiKeyAuth**
