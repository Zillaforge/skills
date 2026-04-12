# PUT /vps/api/v1/project/:{project-id}/keypairs/:{keypair-id}

**Resource:** [keypair](../resources/keypair.md)
**Update Keypair**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-keypairs-:{keypair-id}`

Updates the description about an existing keypair.

Parameters in the request body:
- description: New value for the description field.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `keypair-id` | path | string | Yes | Keypair ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.KeypairUpdateInput](../schemas/user-KeypairUpdateInput/user-KeypairUpdateInput.md)

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
