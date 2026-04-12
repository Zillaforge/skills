# GET /vps/api/v1/project/:{project-id}/routers/:{router-id}/networks

**Resource:** [router](../resources/router.md)
**List Associated Networks**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-routers-:{router-id}-networks`

Lists associated networks from a router.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `router-id` | path | string | Yes | Router ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.NetworkListOutput](../schemas/pb-NetworkListOutput/pb-NetworkListOutput.md)

## Security

- **ApiKeyAuth**
