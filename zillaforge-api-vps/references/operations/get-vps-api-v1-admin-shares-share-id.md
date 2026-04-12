# GET /vps/api/v1/admin/shares/:{share-id}

**Resource:** [system_share](../resources/system-share.md)
**Get Share (Admin)**
**Operation ID:** `get--vps-api-v1-admin-shares-:{share-id}`

Get detailed information about a specific share with admin privileges.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `share-id` | path | string | Yes | Share ID |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ShareInfo](../schemas/pb-ShareInfo/pb-ShareInfo.md)

