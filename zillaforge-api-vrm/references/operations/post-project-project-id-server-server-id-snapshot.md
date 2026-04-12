# POST /project/{project-id}/server/{server-id}/snapshot

**Resource:** [User/Snapshot](../resources/User-Snapshot.md)
**對 Server 建立 snapshot**
**Operation ID:** `post--project-{project-id}-server-{server-id}-snapshot`

## Request Body

**Content Types:** `application/json`, `application/json/repositoryId`

**Schema:** [createSnapshotInput](../schemas/createSnapshotInput/createSnapshotInput.md)

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
