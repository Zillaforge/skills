# POST /admin/projectacl

**Resource:** [Admin/ProjectAcl](../resources/Admin-ProjectAcl.md)
**在指定的 tag 創建 project-acl 分享給其他成員使用**
**Operation ID:** `post--admin-projectacl`

Create a new project access control list entry for tag sharing and project access management

## Request Body

Project ACL creation payload

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.CreateProjectAclInput](../schemas/admin-CreateProjectAclInput/admin-CreateProjectAclInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.CreateProjectAclOutput](../schemas/admin-CreateProjectAclOutput/admin-CreateProjectAclOutput.md)

