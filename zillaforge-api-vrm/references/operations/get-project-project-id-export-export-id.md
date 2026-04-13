# GET /project/:{project-id}/export/:{export-id}

**Resource:** [User/Exports](../resources/User-Exports.md)
**取得指定匯出資訊**
**Operation ID:** `get--project-:{project-id}-export-:{export-id}`

Retrieve export information by export ID

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `export-id` | path | string | Yes | Export ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal server error |

**Success Response Schema:**

[user.GetExportOutput](../schemas/user-GetExportOutput/user-GetExportOutput.md)

