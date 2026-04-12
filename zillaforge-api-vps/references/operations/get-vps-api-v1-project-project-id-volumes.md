# GET /vps/api/v1/project/:{project-id}/volumes

**Resource:** [volumes](../resources/volumes.md)
**List Volumes**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-volumes`

List all volumes in the current project. Search parameter is optional.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/volumes?detail=true' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id |
| `status` | query | string | No | search by status |
| `type` | query | string | No | search by volume type |
| `detail` | query | boolean | No | if true, retuen with attachment info |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.VolumeListOutput](../schemas/pb-VolumeListOutput/pb-VolumeListOutput.md)

## Security

- **ApiKeyAuth**
