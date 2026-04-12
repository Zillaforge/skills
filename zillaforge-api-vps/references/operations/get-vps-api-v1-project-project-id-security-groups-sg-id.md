# GET /vps/api/v1/project/:{project-id}/security_groups/:{sg-id}

**Resource:** [security_group](../resources/security-group.md)
**Get Security Group**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-security_groups-:{sg-id}`

Return detailed information about specific security group.

Request example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/security_groups/3e53eec2-50bf-41bb-9daa-88bcb525765f' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `sg-id` | path | string | Yes | Security Group ID |

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
