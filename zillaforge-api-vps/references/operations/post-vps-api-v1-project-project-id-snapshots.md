# POST /vps/api/v1/project/:{project-id}/snapshots

**Resource:** [snapshots](../resources/snapshots.md)
**Create Snapshot**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-snapshots`

Creates a snapshot from specified volume.

The request payload should contain following fields :
- name: the name for created snapshot.(required)
- description: the detailed description about it.(optional)
- volume_id: the source volume that will be snapshotted.(required)

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/snapshots' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{"name":"sn1736756502","volume_id":"ff430821-9498-47bf-b36f-c9e11dcf4d98"}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.SnapshotCreateInput](../schemas/user-SnapshotCreateInput/user-SnapshotCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pegasus-cloud_com_aes_virtualplatformserviceclient_pb.SnapshotInfo](../schemas/pegasus-cloud/pegasus-cloud-com-aes-virtualplatformserviceclient-pb-SnapshotInfo.md)

## Security

- **ApiKeyAuth**
