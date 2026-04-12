# GET /admin/membership/project/{project-id}/user/{user-id}/

**Resource:** [Admin/Membership](../resources/Admin-Membership.md)
**GetMembershipAndPermission**
**Operation ID:** `get--admin-membership-project-{project-id}-user-{user-id}-`

GetMembershipAndPermission


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | todo |
| `user-id` | path | string | Yes | todo |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[CreateMembershipResponse](../schemas/Create/CreateMembershipResponse.md)

## Security

- **bearerAuth**
