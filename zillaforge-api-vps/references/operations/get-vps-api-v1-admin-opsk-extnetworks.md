# GET /vps/api/v1/admin/opsk_extnetworks

**Resource:** [system_extnet](../resources/system-extnet.md)
**List unused external networks from OPSK**
**Operation ID:** `get--vps-api-v1-admin-opsk_extnetworks`

Return a list of the unassociated external networks on OpenStack.

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.OpskExtNetListOutput](../schemas/pb-OpskExtNetListOutput/pb-OpskExtNetListOutput.md)

## Security

- **ApiKeyAuth**
