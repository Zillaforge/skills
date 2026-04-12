# POST /vps/api/v1/project/:{project-id}/shares

**Resource:** [share](../resources/share.md)
**Create Share**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-shares`

Creates and returns information about newly created file share object.

Parameters in the request body:
- name : File share display name. (required)
- description : Optional text describing this resource.(optional)
- network_id : Network UUID that will host the share. (required)
- size : Size of the storage pool allocated for the share. Unit GB.(required)

Request example :
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/shares' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&ensp;&ensp;"name": "fs1736231338239",
&ensp;&ensp;"description": "",
&ensp;&ensp;"network_id": "bc10c427-a12e-4eee-a5fd-00319f5bbaf1",
&ensp;&ensp;"size": 1
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.ShareCreateInput](../schemas/user-ShareCreateInput/user-ShareCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ShareInfo](../schemas/pb-ShareInfo/pb-ShareInfo.md)

## Security

- **ApiKeyAuth**
