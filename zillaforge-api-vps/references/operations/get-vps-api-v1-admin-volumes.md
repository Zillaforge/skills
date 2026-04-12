# GET /vps/api/v1/admin/volumes

**Resource:** [system_volume](../resources/system-volume.md)
**List Volumes (Admin)**
**Operation ID:** `get--vps-api-v1-admin-volumes`

List all volumes across all projects with admin privileges. Supports filtering by various parameters.
Query parameters:
- project_id: Filter by project ID
- name: Filter by volume name
- status: Filter by volume status
- user_id: Filter by user ID
- namespace: Filter by namespace
- type: Filter by volume type
- size: Filter by volume size
- detail: Set to true to get detailed information

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project_id` | query | string | No | Project ID |
| `name` | query | string | No | Volume name |
| `status` | query | string | No | Volume status |
| `user_id` | query | string | No | User ID |
| `namespace` | query | string | No | Namespace |
| `type` | query | string | No | Volume type |
| `size` | query | string | No | Volume size |
| `detail` | query | boolean | No | Get detailed information |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.VolumeListOutput](../schemas/pb-VolumeListOutput/pb-VolumeListOutput.md)

