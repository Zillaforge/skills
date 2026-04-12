# GET /project/{project-id}/repositories

**Resource:** [User/Repository](../resources/User-Repository.md)
**列出所有的 repositories**
**Operation ID:** `get--project-{project-id}-repositories`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `where` | query | string[] | No | 此功能可以帶入欄位及值作為查詢條件，來篩選出滿足條件的清單。支援的欄位：os, creator, project-id
 |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 403 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[listRepositoriesOutput](../schemas/listRepositoriesOutput/listRepositoriesOutput.md)

## Security

- **bearerAuth**
