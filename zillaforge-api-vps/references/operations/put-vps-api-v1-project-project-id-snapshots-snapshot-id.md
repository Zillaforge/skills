# PUT /vps/api/v1/project/:{project-id}/snapshots/:{snapshot-id}

**Resource:** [snapshots](../resources/snapshots.md)
**Update Snapshot**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-snapshots-:{snapshot-id}`

Updates the name or description of a snapshot using PUT method.

Body parameters :
- name : New name for snapshot.(Optional)
- descirption : New text descripton for snapshot.(Optional)

Request example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/:871a0333-ae33-43f2-81f9-2432fa15cde7/snapshots/:8a5fc96a-731a-448e-9660-3b1d3629e26d' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{"description": "new description", "name": "newName"}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `snapshot-id` | path | string | Yes | Snapshot ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.SnapshotUpdateInput](../schemas/user-SnapshotUpdateInput/user-SnapshotUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pegasus-cloud_com_aes_virtualplatformserviceclient_pb.SnapshotInfo](../schemas/pegasus-cloud/pegasus-cloud-com-aes-virtualplatformserviceclient-pb-SnapshotInfo.md)

## Security

- **ApiKeyAuth**
