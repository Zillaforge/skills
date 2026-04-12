# GET /vps/api/v1/project/:{project-id}/keypairs

**Resource:** [keypair](../resources/keypair.md)
**List Keypairs**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-keypairs`

List all keypairs for a specific project id.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/keypairs' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.KeypairListOutput](../schemas/pb-KeypairListOutput/pb-KeypairListOutput.md)

## Security

- **ApiKeyAuth**
