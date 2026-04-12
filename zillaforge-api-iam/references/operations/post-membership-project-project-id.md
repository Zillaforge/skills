# POST /membership/project/{project-id}

**Resource:** [User/Membership](../resources/User-Membership.md)
**Create Membership**
**Operation ID:** `post--membership-project-{project-id}`

Create membership by tenant admin/owner


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

CreateMembership


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UserCreateMembershipRequest](../schemas/User/UserCreateMembershipRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[UserCreateMembershipResponse](../schemas/User/UserCreateMembershipResponse.md)

## Security

- **bearerAuth**
