# DELETE /vps/api/v1/project/:{project-id}/volumes/:{vol-id}

**Resource:** [volumes](../resources/volumes.md)
**Delete Volume**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-volumes-:{vol-id}`

Deletes a specific volume.

Request Example:
curl -X 'DELETE' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/volumes/77e7fa89-c5a4-432f-8acb-361e6594d4b3' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `vol-id` | path | string | Yes | Volume ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
