# POST /personal_access_api_token

**Resource:** [User/PersonalAccessAPIToken](../resources/User-PersonalAccessAPIToken.md)
**CreatePersonalAccessAPIToken**
**Operation ID:** `post--personal_access_api_token`

Create Personal Access API Token


## Request Body

CreatePersonalAccessAPIToken


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UserCreatePersonalAccessAPITokenRequest](../schemas/User/UserCreatePersonalAccessAPITokenRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |

**Success Response Schema:**

[CreatePersonalAccessAPITokenResponse](../schemas/Create/CreatePersonalAccessAPITokenResponse.md)

## Security

- **bearerAuth**
