# DELETE /vps/api/v1/project/:{project-id}/shares/:{share-id}/rules/:{share-rule-id}

**Resource:** [share](../resources/share.md)
**Delete Rule in Share**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-shares-:{share-id}-rules-:{share-rule-id}`

Removes existing rule allowing access from specific IP address and/or CIDRs.
Preconditions: Share status must be "available".

Request example:
curl -X 'DELETE' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/shares/6ec7a6f9-2cb9-4f4a-8843-3300fb364432/rules/e1a872ea-6eec-4956-a523-01ba01442e88' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `share-id` | path | string | Yes | Share ID |
| `share-rule-id` | path | string | Yes | Share Rule ID |

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
