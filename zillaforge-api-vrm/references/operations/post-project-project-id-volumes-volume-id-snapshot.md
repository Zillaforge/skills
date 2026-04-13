# POST /project/:{project-id}/volumes/:{volume-id}/snapshot

**Resource:** [User/Snapshot](../resources/User-Snapshot.md)
**對 Volume 建立 snapshot**
**Operation ID:** `post--project-:{project-id}-volumes-:{volume-id}-snapshot`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `volume-id` | path | string | Yes | Volume ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.CreateSnapshotInput](../schemas/user-CreateSnapshotInput/user-CreateSnapshotInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[user.CreateSnapshotOutput](../schemas/user-CreateSnapshotOutput/user-CreateSnapshotOutput.md)

