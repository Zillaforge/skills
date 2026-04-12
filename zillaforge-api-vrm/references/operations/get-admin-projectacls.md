# GET /admin/projectacls

**Resource:** [Admin/ProjectAcl](../resources/Admin-ProjectAcl.md)
**取得的所有 project-acl**
**Operation ID:** `get--admin-projectacls`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `where` | query | string[] | No | 此功能可以帶入欄位及值作為查詢條件，來篩選出滿足條件的清單。支援的欄位：tag-id, project-id
 |

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[listProjectAclsOutput](../schemas/listProjectAclsOutput/listProjectAclsOutput.md)

## Security

- **bearerAuth**
