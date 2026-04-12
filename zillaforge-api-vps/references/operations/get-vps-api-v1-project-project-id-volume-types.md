# GET /vps/api/v1/project/:{project-id}/volume_types

**Resource:** [volume_types](../resources/volume-types.md)
**List Name of Volume Types**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-volume_types`

List name of all available volume types in the system.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[user.VoltypeNameListOut](../schemas/user-VoltypeNameListOut/user-VoltypeNameListOut.md)

## Security

- **ApiKeyAuth**
