# GET /user

**Resource:** [User/Users](../resources/User-Users.md)
**取得 user 資訊**
**Operation ID:** `get--user`

取得指定用戶資訊


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
