# PUT /membership/project/{project-id}/user/{user-id}/role

**Resource:** [User/Membership](../resources/User-Membership.md)
**Update Membership Role**
**Operation ID:** `put--membership-project-{project-id}-user-{user-id}-role`

Update membership role by tenant admin/owner


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `user-id` | path | string | Yes | User ID |

## Request Body

UpdateMembershipRole


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateMembershipRoleRequest](../schemas/Update/UpdateMembershipRoleRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[UserCreateMembershipResponse](../schemas/User/UserCreateMembershipResponse.md)

## Security

- **bearerAuth**
