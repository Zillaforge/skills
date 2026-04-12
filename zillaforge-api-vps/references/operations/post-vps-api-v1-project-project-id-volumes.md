# POST /vps/api/v1/project/:{project-id}/volumes

**Resource:** [volumes](../resources/volumes.md)
**Create Volume**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-volumes`

Creates a new volume within your account.

Parameters in the request body:
- name: Name of this volume.(required)
- description: An arbitrary description you want associated with it.(optional)
- type: One of the available types from API call GET /volume_types/.(required)
- size: In GB; must not exceed quota limits.(required)
- snapshot_id: Snapshot Id when creating volume from a snapshot.(optional)

Request Sample:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/volumes' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{"name":"vol1736736428","size":1,"type":"SSD"}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.VolumeCreateInput](../schemas/user-VolumeCreateInput/user-VolumeCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pegasus-cloud_com_aes_virtualplatformserviceclient_pb.VolumeInfo](../schemas/pegasus-cloud/pegasus-cloud-com-aes-virtualplatformserviceclient-pb-VolumeInfo.md)

## Security

- **ApiKeyAuth**
