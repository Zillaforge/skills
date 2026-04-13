# DELETE /project/:{project-id}/memberacl/:{member-acl-id}

**Resource:** [User/MemberAcl](../resources/User-MemberAcl.md)
**刪除指定的 member-acl**
**Operation ID:** `delete--project-:{project-id}-memberacl-:{member-acl-id}`

Delete a member ACL by ID. Only TENANT_OWNER, TENANT_ADMIN, or the creator can delete the ACL.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `member-acl-id` | path | string | Yes | Member ACL ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal Server Error |

