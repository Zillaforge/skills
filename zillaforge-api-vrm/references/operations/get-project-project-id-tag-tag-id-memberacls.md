# GET /project/:{project-id}/tag/:{tag-id}/memberacls

**Resource:** [User/MemberAcl](../resources/User-MemberAcl.md)
**取得此 tag 的所有 member-acl**
**Operation ID:** `get--project-:{project-id}-tag-:{tag-id}-memberacls`

Get a paginated list of member ACLs with optional filtering

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `tag-id` | path | string | Yes | Tag ID |
| `limit` | query | integer | No | Number of items to return (default: 100) |
| `offset` | query | integer | No | Number of items to skip (default: 0) |
| `where` | query | string[] | No | Filter conditions, 支援的欄位：user-id |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal server error |

**Success Response Schema:**

[user.ListMemberAclsOutput](../schemas/user-ListMemberAclsOutput/user-ListMemberAclsOutput.md)

