# GET /admin/membership/project/{project-id}/

**Resource:** [Admin/Membership](../resources/Admin-Membership.md)
**ListMembershipsByProject**
**Operation ID:** `get--admin-membership-project-{project-id}-`

ListMembershipsByProject


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | todo |
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

[ListMembershipsByProjectResponse](../schemas/List/ListMembershipsByProjectResponse.md)

## Security

- **bearerAuth**
