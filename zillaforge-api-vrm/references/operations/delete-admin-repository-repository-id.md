# DELETE /admin/repository/:{repository-id}

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**棄用指定的 repository**
**Operation ID:** `delete--admin-repository-:{repository-id}`

Delete a specific repository and all its associated tags (if not protected)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `repository-id` | path | string | Yes | Repository ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

