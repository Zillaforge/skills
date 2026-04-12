# DELETE /vps/api/v1/project/:{project-id}/keypairs/:{keypair-id}

**Resource:** [keypair](../resources/keypair.md)
**Delete Keypair**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-keypairs-:{keypair-id}`

Deletes an existing keypair.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `keypair-id` | path | string | Yes | Keypair ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
