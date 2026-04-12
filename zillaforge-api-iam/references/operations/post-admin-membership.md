# POST /admin/membership

**Resource:** [Admin/Membership](../resources/Admin-Membership.md)
**CreateMembership**
**Operation ID:** `post--admin-membership`

CreateMembership


## Request Body

CreateMembership


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateMembershipRequest](../schemas/Create/CreateMembershipRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[CreateMembershipResponse](../schemas/Create/CreateMembershipResponse.md)

## Security

- **bearerAuth**
