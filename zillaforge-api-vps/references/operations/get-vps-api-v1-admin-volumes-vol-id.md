# GET /vps/api/v1/admin/volumes/:{vol-id}

**Resource:** [system_volume](../resources/system-volume.md)
**Get Volume (Admin)**
**Operation ID:** `get--vps-api-v1-admin-volumes-:{vol-id}`

Get detailed information about a specific volume with admin privileges.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `vol-id` | path | string | Yes | Volume ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[pegasus-cloud_com_aes_virtualplatformserviceclient_pb.VolumeInfo](../schemas/pegasus-cloud/pegasus-cloud-com-aes-virtualplatformserviceclient-pb-VolumeInfo.md)

