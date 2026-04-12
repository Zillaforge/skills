# POST /vps/api/v1/admin/extnetworks/:{extnet-id}/default

**Resource:** [system_extnet](../resources/system-extnet.md)
**Set external network as default**
**Operation ID:** `post--vps-api-v1-admin-extnetworks-:{extnet-id}-default`

This API sets specified external network as default one for its namespace.

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
