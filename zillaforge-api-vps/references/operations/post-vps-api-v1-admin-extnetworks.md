# POST /vps/api/v1/admin/extnetworks

**Resource:** [system_extnet](../resources/system-extnet.md)
**Import external network**
**Operation ID:** `post--vps-api-v1-admin-extnetworks`

This API will import a given external network into VPS if it exists in OPSK.

Request body parameters:
- opsk_extnetwork_id : External Network ID in Openstack.(required)
- namespace : Namespace which owns the external network.(required)
- description: Description of this external network.(optional)
- is_default: Whether this external network should be set default.

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.ExtNetCreateInput](../schemas/admin-ExtNetCreateInput/admin-ExtNetCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ExtNetInfo](../schemas/pb-ExtNetInfo/pb-ExtNetInfo.md)

## Security

- **ApiKeyAuth**
