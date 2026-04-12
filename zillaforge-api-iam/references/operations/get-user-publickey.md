# GET /user/publickey

**Resource:** [User/Users](../resources/User-Users.md)
**取得公開金鑰**
**Operation ID:** `get--user-publickey`

取得指定用戶的公開金鑰


## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[GetUserPublicKey](../schemas/Get/GetUserPublicKey.md)

## Security

- **bearerAuth**
