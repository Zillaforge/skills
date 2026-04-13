# POST /project/:{project-id}/repository/:{repository-id}/memberacl

**Resource:** [User/MemberAcl](../resources/User-MemberAcl.md)
**Create member ACL batch**
**Operation ID:** `post--project-:{project-id}-repository-:{repository-id}-memberacl`

Create multiple member ACLs in batch for repository or tag context

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `repository-id` | path | string | Yes | Repository ID (for repository context) |

## Request Body

Create member ACL batch request

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.CreateMemberAclBatchInput](../schemas/user-CreateMemberAclBatchInput/user-CreateMemberAclBatchInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal Server Error |

**Success Response Schema:**

[user.CreateMemberAclBatchOutput](../schemas/user-CreateMemberAclBatchOutput/user-CreateMemberAclBatchOutput.md)

