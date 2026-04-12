# GET /membership/project/{project-id}

**Resource:** [User/Membership](../resources/User-Membership.md)
**List Memberships**
**Operation ID:** `get--membership-project-{project-id}`

List memberships


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `offset` | query | integer | No | The number of items to skip before starting to collect the result set. |
| `limit` | query | integer | No | The number of items to return. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[ListMembershipsByProjectResponse](../schemas/List/ListMembershipsByProjectResponse.md)

## Security

- **bearerAuth**
