# GET /admin/user

**Resource:** [Admin/User](../resources/Admin-User.md)
**GetUser**
**Operation ID:** `get--admin-user`

取得用戶資訊 (myself)


## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[GetUserResponse](../schemas/Get/GetUserResponse.md)

## Security

- **bearerAuth**
