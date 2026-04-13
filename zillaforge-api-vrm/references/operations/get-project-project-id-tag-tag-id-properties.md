# GET /project/:{project-id}/tag/:{tag-id}/properties

**Resource:** [User/Tag](../resources/User-Tag.md)
**取得指定 tag 的屬性**
**Operation ID:** `get--project-:{project-id}-tag-:{tag-id}-properties`

Get hardware properties (hw_machine_type, hw_firmware_type, hw_disk_bus) for a specific tag

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `tag-id` | path | string | Yes | Tag ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad request |
| 403 | Forbidden |
| 500 | Internal server error |

**Success Response Schema:**

[user.ListPropertiesOutput](../schemas/user-ListPropertiesOutput/user-ListPropertiesOutput.md)

