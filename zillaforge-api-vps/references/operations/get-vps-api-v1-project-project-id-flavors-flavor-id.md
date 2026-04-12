# GET /vps/api/v1/project/:{project-id}/flavors/:{flavor-id}

**Resource:** [flavor](../resources/flavor.md)
**Get Flavor**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-flavors-:{flavor-id}`

Shows details for a flavor.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `flavor-id` | path | string | Yes | Flavor ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FlavorInfo](../schemas/pb-FlavorInfo/pb-FlavorInfo.md)

## Security

- **ApiKeyAuth**
