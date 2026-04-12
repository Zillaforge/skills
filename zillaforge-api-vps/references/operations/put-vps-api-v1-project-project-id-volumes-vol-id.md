# PUT /vps/api/v1/project/:{project-id}/volumes/:{vol-id}

**Resource:** [volumes](../resources/volumes.md)
**Update Volume**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-volumes-:{vol-id}`

Updates the name or description of a specific volume.

Body parameters :
- name : New name for volume.(Optional)
- descirption : New text descripton for volume.(Optional)

Request example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/volumes/77e7fa89-c5a4-432f-8acb-361e6594d4b3' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{"description":"update description","name":"vol1736736428"}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `vol-id` | path | string | Yes | Volume ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.VolumeUpdateInput](../schemas/user-VolumeUpdateInput/user-VolumeUpdateInput.md)

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
