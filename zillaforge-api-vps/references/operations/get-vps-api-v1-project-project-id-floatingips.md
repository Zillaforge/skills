# GET /vps/api/v1/project/:{project-id}/floatingips/

**Resource:** [floating_ip](../resources/floating-ip.md)
**List floatingIPs**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-floatingips-`

List all floating ips that belong to current project and namespace.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id |
| `status` | query | string | No | search by status |
| `reserved` | query | string | No | search by isReserved |
| `device_type` | query | string | No | search by device's type |
| `device_id` | query | string | No | search by device's id |
| `extnet_id` | query | string | No | search by external network |
| `address` | query | string | No | search by address |
| `detail` | query | boolean | No | get detail informations |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FIPListOutput](../schemas/pb-FIPListOutput/pb-FIPListOutput.md)

## Security

- **ApiKeyAuth**
