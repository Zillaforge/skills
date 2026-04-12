# DELETE /admin/user/{user-id}/personal_access_api_token/{paat-id}

**Resource:** [Admin/PersonalAccessAPIToken](../resources/Admin-PersonalAccessAPIToken.md)
**DeletePersonalAccessAPIToken**
**Operation ID:** `delete--admin-user-{user-id}-personal_access_api_token-{paat-id}`

Delete Personal Access API TokenResponse:


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |
| `paat-id` | path | string | Yes | PAAT ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | NoContent |

## Security

- **bearerAuth**
