# DELETE /project/:{project-id}/export/:{export-id}

**Resource:** [User/Exports](../resources/User-Exports.md)
**刪除指定匯出紀錄**
**Operation ID:** `delete--project-:{project-id}-export-:{export-id}`

Delete an export by ID. Only the creator, tenant owner, or tenant admin can delete an export.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `export-id` | path | string | Yes | Export ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | Export deleted successfully |
| 403 | Forbidden - Only creator, tenant owner, or tenant admin can delete |
| 404 | Not found |
| 500 | Internal server error |

