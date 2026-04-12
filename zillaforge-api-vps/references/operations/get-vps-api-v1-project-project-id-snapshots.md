# GET /vps/api/v1/project/:{project-id}/snapshots

**Resource:** [snapshots](../resources/snapshots.md)
**List Snapshots**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-snapshots`

List all existing snapshots of this account or tenant.
You can filter results using various query string parameters such as name ,user_id, status and volume_id.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/snapshots?volume_id=ff430821-9498-47bf-b36f-c9e11dcf4d98' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id |
| `status` | query | string | No | search by status |
| `volume_id` | query | string | No | search by volume_id |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.SnapshotListOutput](../schemas/pb-SnapshotListOutput/pb-SnapshotListOutput.md)

## Security

- **ApiKeyAuth**
