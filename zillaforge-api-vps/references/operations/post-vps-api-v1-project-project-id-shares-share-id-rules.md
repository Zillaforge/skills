# POST /vps/api/v1/project/:{project-id}/shares/:{share-id}/rules

**Resource:** [share](../resources/share.md)
**Create Rule in Share**
**Operation ID:** `post--vps-api-v1-project-:{project-id}-shares-:{share-id}-rules`

Creates rule that allows access from specific IP address and/or CIDRs.
All shares begin with no access. Clients must be provided with explicit access via this API.
Preconditions: Share status must be "available".

Parameters in the request body:
- level : Access levels. One of "rw" or "ro". "rw"means read and write (RW) access. "ro" means read-only (RO) access.
- cidr : Authenticates a client through its IP address. You may specify a single client IP address or a range of IP addresses in a valid IPv4 CIDR notation. For example 0.0.0.0/0.

Request example:
curl -X 'POST' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/shares/6ec7a6f9-2cb9-4f4a-8843-3300fb364432/rules' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
&ensp;&ensp;"cidr": "10.50.0.0/24",
&ensp;&ensp;"level": "rw"
}'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `share-id` | path | string | Yes | Share ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.ShareRuleCreateInput](../schemas/user-ShareRuleCreateInput/user-ShareRuleCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.ShareInfo](../schemas/pb-ShareInfo/pb-ShareInfo.md)

## Security

- **ApiKeyAuth**
