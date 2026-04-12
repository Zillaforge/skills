# GET /vps/api/v1/project/:{project-id}/quotas

**Resource:** [quota](../resources/quota.md)
**Get Project Quotas**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-quotas`

Return quotas information about current project and usage that have been allocated currently.

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
