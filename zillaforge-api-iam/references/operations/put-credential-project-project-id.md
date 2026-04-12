# PUT /credential/project/{project-id}/

**Resource:** [User/Credentials](../resources/User-Credentials.md)
**更新 access/secret key**
**Operation ID:** `put--credential-project-{project-id}-`

更新 aws signature v4 access/secret key


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
