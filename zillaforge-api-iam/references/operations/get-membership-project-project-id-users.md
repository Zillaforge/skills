# GET /membership/project/{project-id}/users

**Resource:** [User/Membership](../resources/User-Membership.md)
**List all users**
**Operation ID:** `get--membership-project-{project-id}-users`

List All of users, only TENANT_ADMIN or TENANT_OWNER can request


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `offset` | query | integer | No | The number of items to skip before starting to collect the result set.
 |
| `limit` | query | integer | No | The number of items to return. |
| `project-id` | path | string | Yes | Project ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |

**Success Response Schema:**

[UserListUsersResponse](../schemas/User/UserListUsersResponse.md)

## Security

- **bearerAuth**
