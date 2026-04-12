# GET /vps/api/v1/admin/floatingips/:{fip-id}

**Resource:** [system_fip](../resources/system-fip.md)
**Get Floating IP (Admin)**
**Operation ID:** `get--vps-api-v1-admin-floatingips-:{fip-id}`

Get detailed information about a specific floating IP with admin privileges.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `fip-id` | path | string | Yes | Floating IP ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FloatingIPInfo](../schemas/pb-FloatingIPInfo/pb-FloatingIPInfo.md)

