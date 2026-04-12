# GET /admin/membership/user/{user-id}/

**Resource:** [Admin/Membership](../resources/Admin-Membership.md)
**ListMembershipsByUser**
**Operation ID:** `get--admin-membership-user-{user-id}-`

ListMembershipsByUser


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |
| `offset` | query | integer | No | The number of items to skip before starting to collect the result set. |
| `limit` | query | integer | No | The number of items to return. |
| `order` | query | string | No | todo. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[ListMembershipsByUserResponse](../schemas/List/ListMembershipsByUserResponse.md)

## Security

- **bearerAuth**
