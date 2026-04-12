# GET /project/{project-id}/tags

**Resource:** [User/Tag](../resources/User-Tag.md)
**取得可使用的所有 tags**
**Operation ID:** `get--project-{project-id}-tags`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `where` | query | string[] | No | 此功能可以帶入欄位及值作為查詢條件，來篩選出滿足條件的清單。支援的欄位：project-id
 |
| `adminRole` | query | string | No | set false to disable admin ability if admin called and wanted |
| `creator` | query | string | No | belong to the current user, default is true |
| `projectLimit` | query | string | No | share to current User, default is true |
| `projectPublic` | query | string | No | public in project, default is true |
| `globalLimit` | query | string | No | share to current project, default is true |
| `globalPublic` | query | string | No | public in namespace, default is true |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[listTagsOutput](../schemas/listTagsOutput/listTagsOutput.md)

## Security

- **bearerAuth**
