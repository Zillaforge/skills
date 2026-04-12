# GET /vps/api/v1/admin/az/compute

**Resource:** [system_az](../resources/system-az.md)
**List Nova AZ**
**Operation ID:** `get--vps-api-v1-admin-az-compute`

Return nova availability zone info.

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.NovaAZList](../schemas/pb-NovaAZList/pb-NovaAZList.md)

## Security

- **ApiKeyAuth**
