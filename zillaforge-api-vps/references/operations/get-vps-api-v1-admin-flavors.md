# GET /vps/api/v1/admin/flavors/

**Resource:** [system_flavor](../resources/system-flavor.md)
**List Flavors**
**Operation ID:** `get--vps-api-v1-admin-flavors-`

Return all flavors with optional filter.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | query | string | No | search by name |
| `project_id` | query | string | No | search by project_id |
| `public` | query | boolean | No | search by visibility |
| `global` | query | boolean | No | search by global flag |
| `tag` | query | string | No | search by tag (multiple) |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FlavorListOutput](../schemas/pb-FlavorListOutput/pb-FlavorListOutput.md)

## Security

- **ApiKeyAuth**
