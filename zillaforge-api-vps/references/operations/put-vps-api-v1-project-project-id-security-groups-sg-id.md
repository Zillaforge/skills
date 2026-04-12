# PUT /vps/api/v1/project/:{project-id}/security_groups/:{sg-id}

**Resource:** [security_group](../resources/security-group.md)
**Update Security Group**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-security_groups-:{sg-id}`

Updates the name or description of a specific security group.

Body parameters :
- name : New name for security group.(Optional)
- descirption : New text descripton for security group.(Optional)

Request example:
curl -X 'PUT' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/security_groups/3e53eec2-50bf-41bb-9daa-88bcb525765f' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&emsp;"description": "newDescript",
&emsp;"name": "newName"
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `sg-id` | path | string | Yes | Security Group ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.SgUpdateInput](../schemas/user-SgUpdateInput/user-SgUpdateInput.md)

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
