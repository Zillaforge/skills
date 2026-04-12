# POST /vps/api/v1/admin/volume_types/

**Resource:** [system_voltype](../resources/system-voltype.md)
**Create Volume Type**
**Operation ID:** `post--vps-api-v1-admin-volume_types-`

Create a new volume type with specified parameters.

Request body parameters:
- name: Name for this volume type.(required)
- description: Description of this volume type(optional).
- public: Whether the volume type is public (available to all projects) or scoped to a set of projects. Default is False.
- project_ids: The IDs of one or more projects who can use this volume type if this volume type is private.(optional)
- qos_specs: the QoS specs for this volume type.(optional)

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.VoltypeCreateInput](../schemas/admin-VoltypeCreateInput/admin-VoltypeCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.VoltypeInfo](../schemas/admin-VoltypeInfo/admin-VoltypeInfo.md)

