# DELETE /admin/memberacl/:{member-acl-id}

**Resource:** [Admin/MemberAcl](../resources/Admin-MemberAcl.md)
**刪除指定的 member-acl**
**Operation ID:** `delete--admin-memberacl-:{member-acl-id}`

Delete a specific member ACL by ID

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `member-acl-id` | path | string | Yes | Member ACL ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

