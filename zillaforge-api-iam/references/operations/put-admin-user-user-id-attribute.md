# PUT /admin/user/{user-id}/attribute

**Resource:** [Admin/User](../resources/Admin-User.md)
**更新指定使用者的 Attributes**
**Operation ID:** `put--admin-user-{user-id}-attribute`

更新指定使用者的 Attributes


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Request Body

輸入欲更新的使用者 Attributes

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [AdminUpdateUserAttributeRequest](../schemas/Admin/AdminUpdateUserAttributeRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
