# POST /vps/api/v1/admin/floatingips

**Resource:** [system_fip](../resources/system-fip.md)
**Create Reserved Floating IP (Admin)**
**Operation ID:** `post--vps-api-v1-admin-floatingips`

Create a reserved floating IP for a specific project/user/namespace with admin privileges.
This API allows administrators to pre-allocate floating IPs to specific projects and users.
Optional parameters:
- address: Specify a specific IP address (must be within the external network's CIDR)
- extnet_id: Specify which external network to use (defaults to project's default external network)
The created floating IP will be marked as reserved=true and can be associated with devices later.

## Request Body

Floating IP creation parameters

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.FIPCreateInput](../schemas/admin-FIPCreateInput/admin-FIPCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Invalid input or validation failed |
| 404 | Project, user, or external network not found |
| 409 | Address already in use or conflicts with device's network |
| 500 | Internal server error |

**Success Response Schema:**

[pb.FloatingIPInfo](../schemas/pb-FloatingIPInfo/pb-FloatingIPInfo.md)

