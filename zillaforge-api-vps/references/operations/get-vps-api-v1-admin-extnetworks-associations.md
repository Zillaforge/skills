# GET /vps/api/v1/admin/extnetworks/associations

**Resource:** [system_extnet](../resources/system-extnet.md)
**list all Associations**
**Operation ID:** `get--vps-api-v1-admin-extnetworks-associations`

This api lists all associations between projects and external networks.
It also provides information about which namespaces are associated with each other.

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.ExtnetAssoInfo](../schemas/admin-ExtnetAssoInfo/admin-ExtnetAssoInfo.md)

## Security

- **ApiKeyAuth**
