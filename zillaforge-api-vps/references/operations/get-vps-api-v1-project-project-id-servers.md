# GET /vps/api/v1/project/:{project-id}/servers

**Resource:** [server](../resources/server.md)
**List Servers**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-servers`

List all servers of a given project. Search parameter is optional.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id |
| `status` | query | string | No | search by status |
| `image_id` | query | string | No | search by image_id |
| `flavor_id` | query | string | No | search by flavor_id |
| `detail` | query | boolean | No | get detail infomations |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ServerListOutput](../schemas/pb-ServerListOutput/pb-ServerListOutput.md)

## Security

- **ApiKeyAuth**
