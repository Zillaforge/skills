# POST /vps/api/v1/project/:{project-id}/volumes/:{vol-id}/snapshot-schedules

**Resource:** [snapshot-schedules](../resources/snapshot-schedules.md)
**Create Snapshot Schedule**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-volumes-:{vol-id}-snapshot-schedules`

Creates a snapshot schedule for the specified volume.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `vol-id` | path | string | Yes | Volume ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.SnapshotScheduleCreateInput](../schemas/user-SnapshotScheduleCreateInput/user-SnapshotScheduleCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 409 | Conflict |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.SnapshotScheduleInfo](../schemas/pb-SnapshotScheduleInfo/pb-SnapshotScheduleInfo.md)

## Security

- **ApiKeyAuth**
