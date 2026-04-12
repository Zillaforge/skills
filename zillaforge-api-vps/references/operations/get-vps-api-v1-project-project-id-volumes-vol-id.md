# GET /vps/api/v1/project/:{project-id}/volumes/:{vol-id}

**Resource:** [volumes](../resources/volumes.md)
**Get Volume**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-volumes-:{vol-id}`

Returns detailed information about the requested volume resource.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/volumes/77e7fa89-c5a4-432f-8acb-361e6594d4b3' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `vol-id` | path | string | Yes | Volume ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pegasus-cloud_com_aes_virtualplatformserviceclient_pb.VolumeInfo](../schemas/pegasus-cloud/pegasus-cloud-com-aes-virtualplatformserviceclient-pb-VolumeInfo.md)

## Security

- **ApiKeyAuth**
