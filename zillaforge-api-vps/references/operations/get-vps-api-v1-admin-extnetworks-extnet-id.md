# GET /vps/api/v1/admin/extnetworks/:{extnet-id}

**Resource:** [system_extnet](../resources/system-extnet.md)
**Get external network**
**Operation ID:** `get--vps-api-v1-admin-extnetworks-:{extnet-id}`

Return information of specific external network.

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

[pb.ExtNetInfo](../schemas/pb-ExtNetInfo/pb-ExtNetInfo.md)

## Security

- **ApiKeyAuth**
