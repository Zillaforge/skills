# DELETE /vps/api/v1/project/:{project-id}/volumes/:{vol-id}/snapshot-schedules/:{snapshot-schedule-id}

**Resource:** [snapshot-schedules](../resources/snapshot-schedules.md)
**Delete Snapshot Schedule**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-volumes-:{vol-id}-snapshot-schedules-:{snapshot-schedule-id}`

Deletes an existing snapshot schedule.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `vol-id` | path | string | Yes | Volume ID |
| `snapshot-schedule-id` | path | string | Yes | Snapshot Schedule ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
