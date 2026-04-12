# POST /admin/membership/batch

**Resource:** [Admin/Membership](../resources/Admin-Membership.md)
**CreateMembershipBatch**
**Operation ID:** `post--admin-membership-batch`

CreateMembershipBatch


## Request Body

CreateMembershipBatch


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateMembershipBatchRequest](../schemas/Create/CreateMembershipBatchRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[CreateMembershipBatchResponse](../schemas/Create/CreateMembershipBatchResponse.md)

## Security

- **bearerAuth**
