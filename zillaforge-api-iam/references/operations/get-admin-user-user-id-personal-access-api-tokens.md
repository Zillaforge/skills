# GET /admin/user/{user-id}/personal_access_api_tokens

**Resource:** [Admin/PersonalAccessAPIToken](../resources/Admin-PersonalAccessAPIToken.md)
**ListPersonalAccessAPITokens**
**Operation ID:** `get--admin-user-{user-id}-personal_access_api_tokens`

List Personal Access API TokenResponse:


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |

**Success Response Schema:**

[ListPersonalAccessAPITokensResponse](../schemas/List/ListPersonalAccessAPITokensResponse.md)

## Security

- **bearerAuth**
