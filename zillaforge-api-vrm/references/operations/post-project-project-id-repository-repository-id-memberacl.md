# POST /project/{project-id}/repository/{repository-id}/memberacl

**Resource:** [User/MemberAcl](../resources/User-MemberAcl.md)
**在 repository 創建 member-acl**
**Operation ID:** `post--project-{project-id}-repository-{repository-id}-memberacl`

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
