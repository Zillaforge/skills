# PUT /vps/api/v1/admin/extnetworks/:{extnet-id}

**Resource:** [system_extnet](../resources/system-extnet.md)
**Update external network**
**Operation ID:** `put--vps-api-v1-admin-extnetworks-:{extnet-id}`

This method updates description of a particular external network.

Request body parameter:
- description: New description of this external network.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `extnet-id` | path | string | Yes | Ext-Network ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.ExtNetUpdateInput](../schemas/admin-ExtNetUpdateInput/admin-ExtNetUpdateInput.md)

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
