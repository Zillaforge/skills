# DELETE /vps/api/v1/admin/volume_types/:{voltype-id}

**Resource:** [system_voltype](../resources/system-voltype.md)
**Delete Volume Type**
**Operation ID:** `delete--vps-api-v1-admin-volume_types-:{voltype-id}`

This operation deletes an existing volume type by its unique identifier.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `voltype-id` | path | string | Yes | Volume Type ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

