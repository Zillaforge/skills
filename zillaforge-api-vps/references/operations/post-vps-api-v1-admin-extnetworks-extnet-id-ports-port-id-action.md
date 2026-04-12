# POST /vps/api/v1/admin/extnetworks/:{extnet-id}/ports/:{port-id}/action

**Resource:** [system_extnet](../resources/system-extnet.md)
**Do Action to Port**
**Operation ID:** `post--vps-api-v1-admin-extnetworks-:{extnet-id}-ports-:{port-id}-action`

Do an action on the specified port

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `extnet-id` | path | string | Yes | Ext-Network ID |
| `port-id` | path | string | Yes | Port ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.ExtnetPortActionInput](../schemas/admin-ExtnetPortActionInput/admin-ExtnetPortActionInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

