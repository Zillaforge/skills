# DELETE /admin/repository/:{repository-id}/protect

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**解除保護指定的 repository**
**Operation ID:** `delete--admin-repository-:{repository-id}-protect`

Disable protection for a specific repository with administrative privileges

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `repository-id` | path | string | Yes | Repository ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[admin.UnsetRepositoryProtectOutput](../schemas/admin-UnsetRepositoryProtectOutput/admin-UnsetRepositoryProtectOutput.md)

