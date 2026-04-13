# GET /admin/tag/:{tag-id}/memberacls

**Resource:** [Admin/MemberAcl](../resources/Admin-MemberAcl.md)
**取得此 tag 的所有 member-acl**
**Operation ID:** `get--admin-tag-:{tag-id}-memberacls`

List member ACLs with pagination and filtering support

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `tag-id` | path | string | Yes | Tag ID |
| `limit` | query | integer | No | Number of items to return (default: 100) |
| `offset` | query | integer | No | Number of items to skip (default: 0) |
| `where` | query | string[] | No | Filter conditions |
| `namespace` | query | string | No | Filter by namespace |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.ListMemberAclsOutput](../schemas/admin-ListMemberAclsOutput/admin-ListMemberAclsOutput.md)

