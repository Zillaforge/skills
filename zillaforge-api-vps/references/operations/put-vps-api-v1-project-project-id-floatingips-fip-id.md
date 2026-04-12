# PUT /vps/api/v1/project/:{project-id}/floatingips/:{fip-id}

**Resource:** [floating_ip](../resources/floating-ip.md)
**Update floatingIP**
**Operation ID:** `put--vps-api-v1-project-:{project-id}-floatingips-:{fip-id}`

Updates an existing floating ip.

Request body parameters:
- name: new name of the floating ip.(optional)
- description: new description for the floadting ip.(optional)
- reserved: true/false.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `fip-id` | path | string | Yes | FloatingIP ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.FIPUpdateInput](../schemas/user-FIPUpdateInput/user-FIPUpdateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FloatingIPInfo](../schemas/pb-FloatingIPInfo/pb-FloatingIPInfo.md)

## Security

- **ApiKeyAuth**
