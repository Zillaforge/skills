# POST /vps/api/v1/project/:{project-id}/shares/:{share-id}/extend

**Resource:** [share](../resources/share.md)
**Extend Share**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-shares-:{share-id}-extend`

Increases the size of a share.

Parameter in the request body:
&ensp;&ensp;new_size : New size of the share, in GiBs. Must greater than original size.(required)

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/shares/6ec7a6f9-2cb9-4f4a-8843-3300fb364432/extend' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&ensp;&ensp;"new_size": 2
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

**Schema:** [user.ShareExtendInput](../schemas/user-ShareExtendInput/user-ShareExtendInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
