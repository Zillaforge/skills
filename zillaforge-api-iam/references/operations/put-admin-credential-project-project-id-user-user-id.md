# PUT /admin/credential/project/{project-id}/user/{user-id}/

**Resource:** [Admin/Credential](../resources/Admin-Credential.md)
**UpdateCredential**
**Operation ID:** `put--admin-credential-project-{project-id}-user-{user-id}-`

UpdateCredential


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | todo |
| `user-id` | path | string | Yes | todo |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[UpdateCredentialResponse](../schemas/Update/UpdateCredentialResponse.md)

## Security

- **bearerAuth**
