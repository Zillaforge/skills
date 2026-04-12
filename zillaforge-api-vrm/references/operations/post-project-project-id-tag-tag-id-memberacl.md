# POST /project/{project-id}/tag/{tag-id}/memberacl

**Resource:** [User/MemberAcl](../resources/User-MemberAcl.md)
**在指定的 tag 創建 member-acl**
**Operation ID:** `post--project-{project-id}-tag-{tag-id}-memberacl`

## Request Body

**Content Types:** `application/json`

**Schema:** [createMemberAclInput](../schemas/createMemberAclInput/createMemberAclInput.md)

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
