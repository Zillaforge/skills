# POST /vps/api/v1/project/:{project-id}/routers/:{router-id}/action

**Resource:** [router](../resources/router.md)
**Do Action to Router**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-routers-:{router-id}-action`

Do an action on the specified router.
The supported action is "set_state"

Parameter in the request body:
- action: Current support "set_state".(required)
- state : true for enable; false for disable.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `router-id` | path | string | Yes | Router ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.RouterActionInput](../schemas/user-RouterActionInput/user-RouterActionInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
