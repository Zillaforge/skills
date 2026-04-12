# PUT /vps/api/v1/project/:{project-id}/shares/:{share-id}

**Resource:** [share](../resources/share.md)
**Update Share**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-shares-:{share-id}`

Updates name or description of a share.

Parameters in the request body:
- name : New value for the name field(optional)
- descirption : New value for the description field(optional)

Request example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/:871a0333-ae33-43f2-81f9-2432fa15cde7/shares/:6ec7a6f9-2cb9-4f4a-8843-3300fb364432' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&ensp;&ensp;"description": "newDescription",
&ensp;&ensp;"name": "newName"
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `share-id` | path | string | Yes | Share ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.ShareUpdateInput](../schemas/user-ShareUpdateInput/user-ShareUpdateInput.md)

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
