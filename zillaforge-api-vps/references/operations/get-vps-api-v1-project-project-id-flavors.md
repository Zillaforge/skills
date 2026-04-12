# GET /vps/api/v1/project/:{project-id}/flavors/

**Resource:** [flavor](../resources/flavor.md)
**List Flavors**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-flavors-`

List all available flavors.
You may use some filters on your request like tags, names etc...

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `public` | query | boolean | No | search by visibility |
| `tag` | query | string | No | search by tag (multiple) |
| `global` | query | boolean | No | search by global flag |
| `resize_server_id` | query | string | No | 可供該server resize之flavor |

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
