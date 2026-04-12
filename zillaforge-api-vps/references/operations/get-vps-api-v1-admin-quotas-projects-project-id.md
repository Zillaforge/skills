# GET /vps/api/v1/admin/quotas/projects/:{project-id}

**Resource:** [system_quota](../resources/system-quota.md)
**get project's quotas**
**Operation ID:** `get--vps-api-v1-admin-quotas-projects-:{project-id}`

Return the current usage and quota limit about each resource type for specific project.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.QuotaInfo](../schemas/pb-QuotaInfo/pb-QuotaInfo.md)

## Security

- **ApiKeyAuth**
