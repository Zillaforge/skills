# GET /vps/api/v1/project/:{project-id}/shares/:{share-id}

**Resource:** [share](../resources/share.md)
**Get Share**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-shares-:{share-id}`

Shows details for a share.

Request example:
curl -X 'GET' \
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
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ShareInfo](../schemas/pb-ShareInfo/pb-ShareInfo.md)

## Security

- **ApiKeyAuth**
