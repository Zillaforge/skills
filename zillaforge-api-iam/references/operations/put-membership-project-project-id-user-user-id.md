# PUT /membership/project/{project-id}/user/{user-id}

**Resource:** [User/Membership](../resources/User-Membership.md)
**更新 membership 資訊**
**Operation ID:** `put--membership-project-{project-id}-user-{user-id}`

UpdateMembership (目前僅能更新MembershipExtra, 僅供 user本人修改 或 Tenant Owner/Admin 使用)


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `user-id` | path | string | Yes | User ID |

## Request Body

UpdateMembership


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UserUpdateMembershipRequest](../schemas/User/UserUpdateMembershipRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 403 | Forbidden |
| 500 | Internal Server Error |

**Success Response Schema:**

[UserUpdateMembershipResponse](../schemas/User/UserUpdateMembershipResponse.md)

## Security

- **bearerAuth**
