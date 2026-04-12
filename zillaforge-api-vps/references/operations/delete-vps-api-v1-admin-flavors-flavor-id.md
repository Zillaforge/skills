# DELETE /vps/api/v1/admin/flavors/:{flavor-id}

**Resource:** [system_flavor](../resources/system-flavor.md)
**Delete Flavor**
**Operation ID:** `delete--vps-api-v1-admin-flavors-:{flavor-id}`

This operation deletes an existing flavor by its unique identifier.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `flavor-id` | path | string | Yes | Flavor ID |

## Responses

| Status | Description |
|--------|-------------|
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
