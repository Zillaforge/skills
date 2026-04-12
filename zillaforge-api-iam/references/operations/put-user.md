# PUT /user

**Resource:** [User/Users](../resources/User-Users.md)
**更新 user (自身)資訊**
**Operation ID:** `put--user`

UpdateUser (目前僅能更新UserExtra)


## Request Body

UpdateUser


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateUserRequest](../schemas/Update/UpdateUserRequest.md)

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
