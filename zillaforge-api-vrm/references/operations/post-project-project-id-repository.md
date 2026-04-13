# POST /project/:{project-id}/repository

**Resource:** [User/Repository](../resources/User-Repository.md)
**創建 repository**
**Operation ID:** `post--project-:{project-id}-repository`

Create a new repository within a specific project

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

Repository creation payload

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.CreateRepositoryInput](../schemas/user-CreateRepositoryInput/user-CreateRepositoryInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Repository created successfully |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal server error |

**Success Response Schema:**

[user.CreateRepositoryOutput](../schemas/user-CreateRepositoryOutput/user-CreateRepositoryOutput.md)

