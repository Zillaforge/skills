# GET /vps/api/v1/admin/extnetworks/:{extnet-id}/usage

**Resource:** [system_extnet](../resources/system-extnet.md)
**get IP usage**
**Operation ID:** `get--vps-api-v1-admin-extnetworks-:{extnet-id}-usage`

This API returns the number of IPs used and total on given external network.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `extnet-id` | path | string | Yes | Ext-Network ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.NetIPUsage](../schemas/pb-NetIPUsage/pb-NetIPUsage.md)

## Security

- **ApiKeyAuth**
