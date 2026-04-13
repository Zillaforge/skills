# POST /admin/tag/:{tag-id}/memberacl

**Resource:** [Admin/MemberAcl](../resources/Admin-MemberAcl.md)
**在 repository 創建 member-acl**
**Operation ID:** `post--admin-tag-:{tag-id}-memberacl`

Create multiple member ACLs in batch for specified tags and users

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `tag-id` | path | string | Yes | Tag ID |

## Request Body

Member ACL batch creation payload

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.CreateMemberAclBatchInput](../schemas/admin-CreateMemberAclBatchInput/admin-CreateMemberAclBatchInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad request |
| 403 | Forbidden - User not belong to project or tag not belong to repository |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.CreateMemberAclBatchOutput](../schemas/admin-CreateMemberAclBatchOutput/admin-CreateMemberAclBatchOutput.md)

