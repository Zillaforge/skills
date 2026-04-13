# PUT /admin/repository/:{repository-id}

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**更新指定的 repository**
**Operation ID:** `put--admin-repository-:{repository-id}`

Update an existing repository with administrative privileges

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `repository-id` | path | string | Yes | Repository ID |

## Request Body

Repository update payload

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.UpdateRepositoryInput](../schemas/admin-UpdateRepositoryInput/admin-UpdateRepositoryInput.md)

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

[admin.UpdateRepositoryOutput](../schemas/admin-UpdateRepositoryOutput/admin-UpdateRepositoryOutput.md)

