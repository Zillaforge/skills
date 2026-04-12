# POST /membership/project/{project-id}/batch

**Resource:** [User/Membership](../resources/User-Membership.md)
**Batch Create Memberships**
**Operation ID:** `post--membership-project-{project-id}-batch`

Batch create memberships by tenant admin/owner


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

CreateMembershipBatch


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UserCreateMembershipBatchRequest](../schemas/User/UserCreateMembershipBatchRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |

**Success Response Schema:**

[UserCreateMembershipBatchResponse](../schemas/User/UserCreateMembershipBatchResponse.md)

## Security

- **bearerAuth**
