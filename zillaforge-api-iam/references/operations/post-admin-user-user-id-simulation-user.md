# POST /admin/user/{user-id}/simulation_user

**Resource:** [Admin/User](../resources/Admin-User.md)
**模擬分身功能, 產生SAAT**
**Operation ID:** `post--admin-user-{user-id}-simulation_user`

CreateSimulationAccessAPIToken (for SystemAdmin). 此 Token 為 User 權限, 且無法 "更新 IAM token"


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `user-id` | path | string | Yes | simulated user's ID |

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |

**Success Response Schema:**

[CreateSimulationAccessAPITokenResponse](../schemas/Create/CreateSimulationAccessAPITokenResponse.md)

## Security

- **bearerAuth**
