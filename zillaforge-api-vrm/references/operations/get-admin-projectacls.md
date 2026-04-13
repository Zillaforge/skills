# GET /admin/projectacls

**Resource:** [Admin/ProjectAcl](../resources/Admin-ProjectAcl.md)
**取得所有 project-acl**
**Operation ID:** `get--admin-projectacls`

List project ACLs with pagination and filtering support

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `limit` | query | integer | No | Number of items to return (default: 100) |
| `offset` | query | integer | No | Number of items to skip (default: 0) |
| `where` | query | string[] | No | Filter conditions |
| `namespace` | query | string | No | Filter by namespace |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.ListProjectAclsOutput](../schemas/admin-ListProjectAclsOutput/admin-ListProjectAclsOutput.md)

