# PUT /admin/project/{project-id}

**Resource:** [Admin/Repository](../resources/Admin-Repository.md)
**更新指定的 project**
**Operation ID:** `put--admin-project-{project-id}`

## Request Body

**Content Types:** `application/json`

**Schema:** [updateProjectInput](../schemas/updateProjectInput/updateProjectInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | (reference) |
| 401 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[updateProjectOutput](../schemas/updateProjectOutput/updateProjectOutput.md)

## Security

- **bearerAuth**
