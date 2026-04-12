# PUT /admin/membership/project/{project-id}/user/{user-id}/

**Resource:** [Admin/Membership](../resources/Admin-Membership.md)
**UpdateMembership**
**Operation ID:** `put--admin-membership-project-{project-id}-user-{user-id}-`

UpdateMembership


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | todo |
| `user-id` | path | string | Yes | todo |

## Request Body

UpdateMembership


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateMembershipRequest](../schemas/Update/UpdateMembershipRequest.md)

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
