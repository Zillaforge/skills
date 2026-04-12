# GET /vps/api/v1/admin/volume_backends/

**Resource:** [system_voltype](../resources/system-voltype.md)
**List Volume Backends**
**Operation ID:** `get--vps-api-v1-admin-volume_backends-`

Return list of volume backend form IaaS.

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

Array of [admin.VoltypeBackendListOut](../schemas/admin-VoltypeBackendListOut/admin-VoltypeBackendListOut.md)

