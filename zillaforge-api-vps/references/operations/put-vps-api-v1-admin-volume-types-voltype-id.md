# PUT /vps/api/v1/admin/volume_types/:{voltype-id}

**Resource:** [system_voltype](../resources/system-voltype.md)
**Update Volume Type**
**Operation ID:** `put--vps-api-v1-admin-volume_types-:{voltype-id}`

Modify attributes of an existing volume type identified by its unique identifier.

Request body parameters:
- description: New value for the description attribute.(optional)
- public: Whether the volume type is public (available to all projects) or scoped to a set of projects. Default is False.
- project_ids: The IDs of one or more projects who can use this volume type if this volume type is private.(optional)
- qos_specs: the QoS specs for this volume type.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `voltype-id` | path | string | Yes | Volume Type ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.VoltypeUpdateInput](../schemas/admin-VoltypeUpdateInput/admin-VoltypeUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.VoltypeInfo](../schemas/admin-VoltypeInfo/admin-VoltypeInfo.md)

