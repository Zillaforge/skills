# PUT /admin/permission/{permission-id}

**Resource:** [Admin/Permission](../resources/Admin-Permission.md)
**更新指定的 permission**
**Operation ID:** `put--admin-permission-{permission-id}`

根據permission id 更新permission


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `permission-id` | path | string | Yes | 要更新的permission id當參數 |

## Request Body

UpdatePermission


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdatePermissionRequest](../schemas/Update/UpdatePermissionRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[UpdatePermissionResponse](../schemas/Update/UpdatePermissionResponse.md)

## Security

- **bearerAuth**
