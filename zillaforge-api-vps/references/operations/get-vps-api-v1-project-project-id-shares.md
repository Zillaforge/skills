# GET /vps/api/v1/project/:{project-id}/shares

**Resource:** [share](../resources/share.md)
**List Shares**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-shares`

Lists all shares of a given project. Search parameter is optional.

Example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/shares' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id(adm only) |
| `detail` | query | boolean | No | if true, return with rules |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ShareListOutput](../schemas/pb-ShareListOutput/pb-ShareListOutput.md)

## Security

- **ApiKeyAuth**
