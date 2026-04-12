# POST /vps/api/v1/project/:{project-id}/servers/:{svr-id}/action

**Resource:** [server](../resources/server.md)
**Do Action to server**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-servers-:{svr-id}-action`

Do an action on the specified server instance.
The supported actions are: stop/start/reboot/resize/approve/reject/extend_root/get_pwd
The 'approve'/'reject' action can only be used by tenant admin.

Parameter in the request body:
- action : one of stop, start, reboot, resize, approve, reject, extend_root, get_pwd, shelve, shelve_offload, unshelve
- reboot_type : Hard or soft. Required if action is reboot.
- flavor_id : The new flavor id for resize vm. Required if action is resize.
- root_size : The new size for extending the vm's root disk. Required if action is extend_root.
- private_key : The private key of the server for getting password. Base-64 encoded PEM format. Required if action is get_pwd.

Request Example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a/action' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
"action": "reboot",
"reboot_type": "soft"
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `svr-id` | path | string | Yes | Server ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.SvrActionInput](../schemas/user-SvrActionInput/user-SvrActionInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 202 | Accepted |
| 400 | Bad Request |
| 500 | Internal Server Error |

## Security

- **ApiKeyAuth**
