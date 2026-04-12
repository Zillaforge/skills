# PUT /admin/usagetime/user/{user-id}

**Resource:** [Admin/UsageTime](../resources/Admin-UsageTime.md)
**create/update user usage time**
**Operation ID:** `put--admin-usagetime-user-{user-id}`

建立或更新使用者帳號的有效期限


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | user id |

## Request Body

UpdateUserUsageTimeRequest: 
1. if forzen is true, accept input activateTime and expiredTime or input activateTime
2. if frozen is false, only accept input expiredTime
3. activateTime need after currentTime.
4. expiredTime need after activateTime and currentTime.


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateUserUsageTimeRequest](../schemas/Update/UpdateUserUsageTimeRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | bad request |
| 500 | IAM server內部發生錯誤 |

## Security

- **bearerAuth**
