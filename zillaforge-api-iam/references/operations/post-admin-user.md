# POST /admin/user

**Resource:** [Admin/User](../resources/Admin-User.md)
**CreateUser**
**Operation ID:** `post--admin-user`

CreateUser:
1. if input usageTime not nil and forzen is true, accept input activateTime and expiredTime or input activateTime
2. if input usageTime not nil and frozen is false, only accept input expiredTime


## Request Body

CreateUser


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateUserRequest](../schemas/Create/CreateUserRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[CreateUserResponse](../schemas/Create/CreateUserResponse.md)

## Security

- **bearerAuth**
