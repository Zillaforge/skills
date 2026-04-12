# GET /admin/projects

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**列出所有 project**
**Operation ID:** `get--admin-projects`

列出所有 project


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
| 200 | OK 回傳 projects array 及 project 數量 |
| 400 | bad request project 不存在 沒有輸入project id |
| 500 | IAM server內部發生錯誤 |

**Success Response Schema:**

[GetAdminProjectsResponse](../schemas/Get/GetAdminProjectsResponse.md)

## Security

- **bearerAuth**
