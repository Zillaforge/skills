# POST /admin/project/{project-id}/server/{server-id}/snapshot

**Resource:** [Admin/Snapshot](../resources/Admin-Snapshot.md)
**對 Server 建立 snapshot**
**Operation ID:** `post--admin-project-{project-id}-server-{server-id}-snapshot`

## Request Body

**Content Types:** `application/json`, `application/json/repositoryId`

**Schema:** [createSnapshotInput.admin](../schemas/createSnapshotInput-admin/createSnapshotInput-admin.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | (reference) |
| 403 | (reference) |
| 404 | (reference) |
| 500 | (reference) |

**Success Response Schema:**

[createSnapshotOutput](../schemas/createSnapshotOutput/createSnapshotOutput.md)

## Security

- **bearerAuth**
