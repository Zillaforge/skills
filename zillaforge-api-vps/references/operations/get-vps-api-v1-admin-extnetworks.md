# GET /vps/api/v1/admin/extnetworks

**Resource:** [system_extnet](../resources/system-extnet.md)
**List external networks**
**Operation ID:** `get--vps-api-v1-admin-extnetworks`

Return all available external networks.

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ExtNetListOutput](../schemas/pb-ExtNetListOutput/pb-ExtNetListOutput.md)

## Security

- **ApiKeyAuth**
