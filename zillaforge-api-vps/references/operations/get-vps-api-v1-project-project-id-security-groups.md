# GET /vps/api/v1/project/:{project-id}/security_groups

**Resource:** [security_group](../resources/security-group.md)
**List Security Groups**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-security_groups`

Return all security groups of a given project. Search parameter is optional.
If parameter 'detail=true', return details including rules.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/security_groups' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `name` | query | string | No | search by name |
| `user_id` | query | string | No | search by user_id(adm only) |
| `detail` | query | boolean | No | if true, retuen with rules |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.SgListOutput](../schemas/pb-SgListOutput/pb-SgListOutput.md)

## Security

- **ApiKeyAuth**
