# GET /vps/api/v1/admin/system/actions

**Resource:** [system_action](../resources/system-action.md)
**List system actions**
**Operation ID:** `get--vps-api-v1-admin-system-actions`

Get list of all available system actions with their details

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.ListSysActionsOutput](../schemas/admin-ListSysActionsOutput/admin-ListSysActionsOutput.md)

