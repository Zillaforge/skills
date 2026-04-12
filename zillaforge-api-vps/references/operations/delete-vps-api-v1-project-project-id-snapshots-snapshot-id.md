# DELETE /vps/api/v1/project/:{project-id}/snapshots/:{snapshot-id}

**Resource:** [snapshots](../resources/snapshots.md)
**Delete Snapshot**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-snapshots-:{snapshot-id}`

Deletes an existing snapshot resource.

Request example:
curl -X 'DELETE' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/snapshots/1fe99b3a-c1ad-41f7-9759-19bdbca0e096' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `snapshot-id` | path | string | Yes | Snapshot ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
