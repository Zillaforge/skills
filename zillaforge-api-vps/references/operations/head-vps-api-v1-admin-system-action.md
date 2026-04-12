# HEAD /vps/api/v1/admin/system/action

**Resource:** [system_action](../resources/system-action.md)
**Check system action existence**
**Operation ID:** `head--vps-api-v1-admin-system-action`

Verify if a specific system action exists

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `method` | query | string | Yes | HTTP method |
| `endpoint` | query | string | Yes | API endpoint |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

