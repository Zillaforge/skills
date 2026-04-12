# GET /vps/api/v1/admin/networks/

**Resource:** [system_network](../resources/system-network.md)
**List Networks**
**Operation ID:** `get--vps-api-v1-admin-networks-`

List all networks
List all networks

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project_id` | query | string | No | Project ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.NetworkListOutput](../schemas/pb-NetworkListOutput/pb-NetworkListOutput.md)

