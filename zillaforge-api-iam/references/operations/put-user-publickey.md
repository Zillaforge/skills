# PUT /user/publickey

**Resource:** [User/Users](../resources/User-Users.md)
**更換公開金鑰**
**Operation ID:** `put--user-publickey`

更換指定用戶的公開金鑰


## Request Body

輸入欲更新的公開金鑰

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateUserPublicKey](../schemas/Update/UpdateUserPublicKey.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
