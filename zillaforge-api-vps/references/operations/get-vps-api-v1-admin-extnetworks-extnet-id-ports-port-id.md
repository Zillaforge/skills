# GET /vps/api/v1/admin/extnetworks/:{extnet-id}/ports/:{port-id}

**Resource:** [system_extnet](../resources/system-extnet.md)
**Get port**
**Operation ID:** `get--vps-api-v1-admin-extnetworks-:{extnet-id}-ports-:{port-id}`

Gets detailed information about a single port.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `extnet-id` | path | string | Yes | Ext-Network ID |
| `port-id` | path | string | Yes | Port ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ExtNetPortInfo](../schemas/pb-ExtNetPortInfo/pb-ExtNetPortInfo.md)

