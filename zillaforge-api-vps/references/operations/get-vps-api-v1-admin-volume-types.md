# GET /vps/api/v1/admin/volume_types/

**Resource:** [system_voltype](../resources/system-voltype.md)
**List Volume Types**
**Operation ID:** `get--vps-api-v1-admin-volume_types-`

Return all volume types with optional filter.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | query | string | No | search by name |
| `project_id` | query | string | No | search by project_id |
| `public` | query | boolean | No | search by visibility |
| `protect` | query | boolean | No | search by is protected |
| `detail` | query | boolean | No | get detail informations |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

Array of [admin.VoltypeListOut](../schemas/admin-VoltypeListOut/admin-VoltypeListOut.md)

