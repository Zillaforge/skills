# DELETE /admin/usagetime/user/{user-id}

**Resource:** [Admin/UsageTime](../resources/Admin-UsageTime.md)
**delete user usage time**
**Operation ID:** `delete--admin-usagetime-user-{user-id}`

刪除使用者帳號的有效期限


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | user id |

## Responses

| Status | Description |
|--------|-------------|
| 200 | 刪除成功 |
| 500 | IAM server內部發生錯誤 |

## Security

- **bearerAuth**
