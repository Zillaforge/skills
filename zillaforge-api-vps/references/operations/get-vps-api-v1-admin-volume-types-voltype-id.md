# GET /vps/api/v1/admin/volume_types/:{voltype-id}

**Resource:** [system_voltype](../resources/system-voltype.md)
**Get Volume Type**
**Operation ID:** `get--vps-api-v1-admin-volume_types-:{voltype-id}`

Return information about an existing volume type identified by its unique identifier.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `voltype-id` | path | string | Yes | Volume Type ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.VoltypeInfo](../schemas/admin-VoltypeInfo/admin-VoltypeInfo.md)

