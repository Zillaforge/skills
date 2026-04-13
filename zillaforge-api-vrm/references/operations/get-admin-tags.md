# GET /admin/tags

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**取得所有 tags**
**Operation ID:** `get--admin-tags`

Get a paginated list of tags with optional filtering by namespace and where conditions

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `limit` | query | integer | No | Number of items to return (default: 100) |
| `offset` | query | integer | No | Number of items to skip (default: 0) |
| `where` | query | string[] | No | Filter conditions |
| `namespace` | query | string | No | Filter by namespace |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.ListTagsOutput](../schemas/admin-ListTagsOutput/admin-ListTagsOutput.md)

