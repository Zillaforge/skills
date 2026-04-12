# DELETE /vps/api/v1/admin/extnetworks/:{extnet-id}

**Resource:** [system_extnet](../resources/system-extnet.md)
**Delete external network**
**Operation ID:** `delete--vps-api-v1-admin-extnetworks-:{extnet-id}`

This operation deletes an external network from VPS.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `extnet-id` | path | string | Yes | Ext-Network ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
