# POST /admin/user/{user-id}/personal_access_api_token

**Resource:** [Admin/PersonalAccessAPIToken](../resources/Admin-PersonalAccessAPIToken.md)
**CreatePersonalAccessAPIToken**
**Operation ID:** `post--admin-user-{user-id}-personal_access_api_token`

Create Personal Access API Token


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | todo |

## Request Body

CreatePersonalAccessAPIToken


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [AdminCreatePersonalAccessAPITokenRequest](../schemas/Admin/AdminCreatePersonalAccessAPITokenRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |

**Success Response Schema:**

[CreatePersonalAccessAPITokenResponse](../schemas/Create/CreatePersonalAccessAPITokenResponse.md)

## Security

- **bearerAuth**
