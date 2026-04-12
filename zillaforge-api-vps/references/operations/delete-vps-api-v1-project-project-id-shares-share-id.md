# DELETE /vps/api/v1/project/:{project-id}/shares/:{share-id}

**Resource:** [share](../resources/share.md)
**Delete Share**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-shares-:{share-id}`

Deletes a share.
Preconditions: Share status must be "available", "error" or "inactive".

Request example:
curl -X 'DELETE' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/shares/6ec7a6f9-2cb9-4f4a-8843-3300fb364432' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `share-id` | path | string | Yes | Share ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
