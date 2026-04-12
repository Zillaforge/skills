# POST /vps/api/v1/project/:{project-id}/servers/:{svr-id}/volumes/:{vol-id}

**Resource:** [server](../resources/server.md)
**Attach a Volume to Server**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-servers-:{svr-id}-volumes-:{vol-id}`

Attaches a volume to a server.

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/:871a0333-ae33-43f2-81f9-2432fa15cde7/servers/:c43bcdda-a2de-400e-a510-537ed89e088a/volumes/:82931dcb-7676-40ae-807b-1d349bf84afb' \
-H 'accept: application/json' \
-d ”

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `svr-id` | path | string | Yes | Server ID |
| `vol-id` | path | string | Yes | Volume ID |

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
