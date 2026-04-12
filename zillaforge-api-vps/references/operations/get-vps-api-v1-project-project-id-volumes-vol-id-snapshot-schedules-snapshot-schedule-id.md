# GET /vps/api/v1/project/:{project-id}/volumes/:{vol-id}/snapshot-schedules/:{snapshot-schedule-id}

**Resource:** [snapshot-schedules](../resources/snapshot-schedules.md)
**Get Snapshot Schedule**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-volumes-:{vol-id}-snapshot-schedules-:{snapshot-schedule-id}`

Gets specific snapshot schedule by its unique identifier.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `vol-id` | path | string | Yes | Volume ID |
| `snapshot-schedule-id` | path | string | Yes | Snapshot Schedule ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.SnapshotScheduleInfo](../schemas/pb-SnapshotScheduleInfo/pb-SnapshotScheduleInfo.md)

## Security

- **ApiKeyAuth**
