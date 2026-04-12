# GET /vps/api/v1/admin/extnetworks/:{extnet-id}/ports

**Resource:** [system_extnet](../resources/system-extnet.md)
**List ports on external network**
**Operation ID:** `get--vps-api-v1-admin-extnetworks-:{extnet-id}-ports`

List all ports on the specific external network

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

[pb.ExtNetListPortOutput](../schemas/pb-ExtNetListPortOutput/pb-ExtNetListPortOutput.md)

