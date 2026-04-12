# POST /admin/tag/{tag-id}/memberacl

**Resource:** [Admin/MemberAcl](../resources/Admin-MemberAcl.md)
**在 repository 創建 member-acl**
**Operation ID:** `post--admin-tag-{tag-id}-memberacl`

## Request Body

**Content Types:** `application/json`

**Schema:** [createMemberAclInput.batch](../schemas/createMemberAclInput-batch/createMemberAclInput-batch.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[createMemberAclOutput](../schemas/createMemberAclOutput/createMemberAclOutput.md)

## Security

- **bearerAuth**
