# GET /admin/permissions

**Resource:** [Admin/Permission](../resources/Admin-Permission.md)
**列出所有 permission**
**Operation ID:** `get--admin-permissions`

列出系統中所有被創建的 permission

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `offset` | query | integer | No | The number of items to skip before starting to collect the result set. |
| `limit` | query | integer | No | The number of items to return. |
| `order` | query | string | No | todo. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[ListPermissionsResponse](../schemas/List/ListPermissionsResponse.md)

## Security

- **bearerAuth**
