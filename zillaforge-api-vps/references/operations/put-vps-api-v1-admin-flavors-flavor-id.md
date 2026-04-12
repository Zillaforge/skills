# PUT /vps/api/v1/admin/flavors/:{flavor-id}

**Resource:** [system_flavor](../resources/system-flavor.md)
**Update Flavor**
**Operation ID:** `put--vps-api-v1-admin-flavors-:{flavor-id}`

Modify attributes of an existing flavor identified by its unique identifier.

Request body parameters:
- description: New value for the description attribute.(optional)
- public: Whether the flavor is public (available to all projects) or scoped to a set of projects.(optional)
- project_ids: The IDs of one or more projects who can use this flavor if this flavor is private.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `flavor-id` | path | string | Yes | Flavor ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.FlvUpdateInput](../schemas/admin-FlvUpdateInput/admin-FlvUpdateInput.md)

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
