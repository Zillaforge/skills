# GET /vps/api/v1/project/:{project-id}/volume_types/:{voltype-id}

**Resource:** [volume_types](../resources/volume-types.md)
**Get Volume Type**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-volume_types-:{voltype-id}`

Get volume type details.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `voltype-id` | path | string | Yes | Volume Type ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.VoltypeInfo](../schemas/admin-VoltypeInfo/admin-VoltypeInfo.md)

