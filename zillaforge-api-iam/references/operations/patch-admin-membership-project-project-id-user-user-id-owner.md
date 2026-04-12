# PATCH /admin/membership/project/{project-id}/user/{user-id}/owner

**Resource:** [Admin/Membership](../resources/Admin-Membership.md)
**設定專案Owner**
**Operation ID:** `patch--admin-membership-project-{project-id}-user-{user-id}-owner`

設定專案Owner，該專案的Tenant Admin才能被設為Owner


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
