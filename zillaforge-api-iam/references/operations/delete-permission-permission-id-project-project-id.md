# DELETE /permission/{permission-id}/project/{project-id}

**Resource:** [User/Permission](../resources/User-Permission.md)
**在指定project下刪除指定的permission**
**Operation ID:** `delete--permission-{permission-id}-project-{project-id}`

根據project id及permission id刪除屬於該project的permission


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | 要查詢的project id當參數 |
| `permission-id` | path | string | Yes | 要刪除的permission id當參數 |

## Responses

| Status | Description |
|--------|-------------|
| 204 | NoContent |
| 403 | Forbidden |
| 500 | Internal Server Error |

## Security

- **bearerAuth**
