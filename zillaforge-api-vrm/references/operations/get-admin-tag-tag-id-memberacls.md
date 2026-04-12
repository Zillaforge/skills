# GET /admin/tag/{tag-id}/memberacls

**Resource:** [Admin/MemberAcl](../resources/Admin-MemberAcl.md)
**取得此 tag 的所有 member-acl**
**Operation ID:** `get--admin-tag-{tag-id}-memberacls`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `where` | query | string[] | No | 此功能可以帶入欄位及值作為查詢條件，來篩選出滿足條件的清單。支援的欄位：tag-id, user-id
 |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[listMemberAclsOutput](../schemas/listMemberAclsOutput/listMemberAclsOutput.md)

## Security

- **bearerAuth**
