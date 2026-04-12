# PATCH /membership/project/{project-id}/user/{user-id}/owner

**Resource:** [User/Membership](../resources/User-Membership.md)
**設定專案Owner**
**Operation ID:** `patch--membership-project-{project-id}-user-{user-id}-owner`

設定專案Owner，只有該專案的Owner可以轉換其他人為Owner


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `user-id` | path | string | Yes | User ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 403 | Forbidden |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
