# GET /admin/tag/:{tag-id}

**Resource:** [Admin/Tag](../resources/Admin-Tag.md)
**取得指定的 tag**
**Operation ID:** `get--admin-tag-:{tag-id}`

Get detailed information about a specific tag

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `tag-id` | path | string | Yes | Tag ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.GetTagOutput](../schemas/admin-GetTagOutput/admin-GetTagOutput.md)

