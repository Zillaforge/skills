# GET /vps/api/v1/admin/quotas/default

**Resource:** [system_quota](../resources/system-quota.md)
**get default quotas**
**Operation ID:** `get--vps-api-v1-admin-quotas-default`

Returns the quota limits used as defaults when creating projects.

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
