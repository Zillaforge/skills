# GET /vps/api/v1/project/:{project-id}/volumes/:{vol-id}/snapshot-schedules

**Resource:** [snapshot-schedules](../resources/snapshot-schedules.md)
**List Snapshot Schedules**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-volumes-:{vol-id}-snapshot-schedules`

List snapshot schedule for the specified volume.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `vol-id` | path | string | Yes | Volume ID |

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
