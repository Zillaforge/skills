# GET /vps/api/v1/project/:{project-id}/keypairs/:{keypair-id}

**Resource:** [keypair](../resources/keypair.md)
**Get Keypair**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-keypairs-:{keypair-id}`

Shows details for a keypair.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `keypair-id` | path | string | Yes | Keypair ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.KeypairInfo](../schemas/pb-KeypairInfo/pb-KeypairInfo.md)

## Security

- **ApiKeyAuth**
