# GET /credential/project/{project-id}/

**Resource:** [User/Credentials](../resources/User-Credentials.md)
**取得 access/secret key**
**Operation ID:** `get--credential-project-{project-id}-`

取得 aws signature v4 access/secret key


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | UUID of the project |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[CredentialResponse](../schemas/Credential/CredentialResponse.md)

## Security

- **bearerAuth**
