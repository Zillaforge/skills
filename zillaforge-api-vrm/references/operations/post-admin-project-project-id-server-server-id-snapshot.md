# POST /admin/project/:{project-id}/server/:{server-id}/snapshot

**Resource:** [Admin/Snapshot](../resources/Admin-Snapshot.md)
**對 Server 建立 snapshot**
**Operation ID:** `post--admin-project-:{project-id}-server-:{server-id}-snapshot`

Create a snapshot of a VPS server, either by creating a new repository or using an existing one

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `server-id` | path | string | Yes | Server ID |

## Request Body

Snapshot creation parameters

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.CreateSnapshotInput](../schemas/admin-CreateSnapshotInput/admin-CreateSnapshotInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.CreateSnapshotOutput](../schemas/admin-CreateSnapshotOutput/admin-CreateSnapshotOutput.md)

