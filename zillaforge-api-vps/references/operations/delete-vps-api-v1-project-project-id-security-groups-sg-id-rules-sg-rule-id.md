# DELETE /vps/api/v1/project/:{project-id}/security_groups/:{sg-id}/rules/:{sg-rule-id}

**Resource:** [security_group](../resources/security-group.md)
**Delete Rule in Security Group**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-security_groups-:{sg-id}-rules-:{sg-rule-id}`

Removes rule from an existing security group.

Request example:
curl -X 'DELETE' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/security_groups/e7fd1372-f487-484c-a5a1-ec48a4be7cd1/rules/9f370233-dff4-4e2a-abaa-bb5dc57d20ae' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `sg-id` | path | string | Yes | Security Group ID |
| `sg-rule-id` | path | string | Yes | Security Group Rule ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.SgInfo](../schemas/pb-SgInfo/pb-SgInfo.md)

## Security

- **ApiKeyAuth**
