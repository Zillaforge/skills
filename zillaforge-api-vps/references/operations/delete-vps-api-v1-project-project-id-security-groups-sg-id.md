# DELETE /vps/api/v1/project/:{project-id}/security_groups/:{sg-id}

**Resource:** [security_group](../resources/security-group.md)
**Delete Security Group**
**Operation ID:** `delete--vps-api-v1-project-:{project-id}-security_groups-:{sg-id}`

Deletes a specific security group identified by sg-id.

Request example:
curl -X 'DELETE' \
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
| 204 | No Content |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
