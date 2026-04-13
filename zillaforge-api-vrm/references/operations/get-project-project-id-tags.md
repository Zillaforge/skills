# GET /project/:{project-id}/tags

**Resource:** [User/Tag](../resources/User-Tag.md)
**取得可使用的所有 tags**
**Operation ID:** `get--project-:{project-id}-tags`

Get a list of tags that the user has access to, with optional filtering

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `limit` | query | integer | No | Limit number of results |
| `offset` | query | integer | No | Offset for pagination |
| `where` | query | string[] | No | Filter conditions |
| `adminRole` | query | boolean | No | set false to disable admin ability if admin called and wanted |
| `creator` | query | boolean | No | belong to the current user, default is true |
| `projectLimit` | query | boolean | No | share to current User, default is true |
| `projectPublic` | query | boolean | No | public in project, default is true |
| `globalLimit` | query | boolean | No | share to current project, default is true |
| `globalPublic` | query | boolean | No | public in namespace, default is true |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal server error |

**Success Response Schema:**

[user.ListTagsOutput](../schemas/user-ListTagsOutput/user-ListTagsOutput.md)

