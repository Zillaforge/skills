# POST /vps/api/v1/project/:{project-id}/keypairs

**Resource:** [keypair](../resources/keypair.md)
**Create Keypair**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-keypairs`

Creates a keypair. A keypair is a ssh key that can be injected into a server on launch.

Parameters in the request body:
- name: Name of this keypair.(required)
- description: Description about this keypair.(optional)
- public_key: The public ssh key to import.(optional)


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.KeypairCreateInput](../schemas/user-KeypairCreateInput/user-KeypairCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.KeypairInfo](../schemas/pb-KeypairInfo/pb-KeypairInfo.md)

## Security

- **ApiKeyAuth**
