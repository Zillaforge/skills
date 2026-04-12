# POST /admin/permission

**Resource:** [Admin/Permission](../resources/Admin-Permission.md)
**創建一條 permission**
**Operation ID:** `post--admin-permission`

創建一條 permission來管理project或user權限，permission Type可為GLOBAL或USER

## Request Body

創建一條 permission

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreatePermissionRequest](../schemas/Create/CreatePermissionRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[CreatePermissionResponse](../schemas/Create/CreatePermissionResponse.md)

