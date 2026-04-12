# POST /vps/api/v1/project/:{project-id}/volumes/:{vol-id}/action

**Resource:** [volumes](../resources/volumes.md)
**Do action to Volume**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-volumes-:{vol-id}-action`

Perform some operation against this volume object such as attaching it to VM etc...

Parameter in the request body:
- action: The type of action you want to perform on the volume. Valid values include attach/detach/extend/revert.(required)
- server_id: The uuid of the target server.(Required when performing attachment operations.)
- new_size: The desired extension size value in GB.(Only applicable for extend action.)

Request Example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/volumes/ff430821-9498-47bf-b36f-c9e11dcf4d98/action' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{"action":"extend","new_size":2}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `vol-id` | path | string | Yes | Volume ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.VolActionInput](../schemas/user-VolActionInput/user-VolActionInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
