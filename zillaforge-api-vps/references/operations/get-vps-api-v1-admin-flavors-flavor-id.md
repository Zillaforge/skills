# GET /vps/api/v1/admin/flavors/:{flavor-id}

**Resource:** [system_flavor](../resources/system-flavor.md)
**Get Flavor**
**Operation ID:** `get--vps-api-v1-admin-flavors-:{flavor-id}`

Return information about an existing flavor identified by its unique identifier.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
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
