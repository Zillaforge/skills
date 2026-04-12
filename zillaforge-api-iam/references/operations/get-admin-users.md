# GET /admin/users

**Resource:** [Admin/User](../resources/Admin-User.md)
**ListUser**
**Operation ID:** `get--admin-users`

ListUser


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `offset` | query | integer | No | The number of items to skip before starting to collect the result set.  
#Tip 1: 當在 where條件式下，此參數為無效。
 |
| `limit` | query | integer | No | The number of items to return. |
| `order` | query | string | No | todo. |
| `where` | query | object[] | No | 此功能可以只列出特定欄位的某個值。  
例如： 當要只列出Namespace=ci.asus.com且Frozen=True時，  
可以帶入query parameters => where=namespace%3Dci.asus.com&where=frozen%3Dtrue
 |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | BadRequest |
| 500 | Internal Server Error |

**Success Response Schema:**

[ListUserResponse](../schemas/List/ListUserResponse.md)

## Security

- **bearerAuth**
