# POST /admin/repository/:{repository-id}/protect

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**設定保護指定的 repository (避免被刪除)**
**Operation ID:** `post--admin-repository-:{repository-id}-protect`

Enable protection for a specific repository with administrative privileges

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `repository-id` | path | string | Yes | Repository ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.SetRepositoryProtectOutput](../schemas/admin-SetRepositoryProtectOutput/admin-SetRepositoryProtectOutput.md)

