# GET /admin/membership

**Resource:** [Admin/Membership](../resources/Admin-Membership.md)
**List ALL Existing memberships**
**Operation ID:** `get--admin-membership`

ListMembership
撈取目前所有Memberships (User與所在Projects之關係)


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `offset` | query | integer | No | The number of items to skip before starting to collect the result set. |
| `limit` | query | integer | No | The number of items to return. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 500 | Internal Server Error | IAM Server 發生內部錯誤 |

**Success Response Schema:**

[ListMembershipResponse](../schemas/List/ListMembershipResponse.md)

## Security

- **bearerAuth**
