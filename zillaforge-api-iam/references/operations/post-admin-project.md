# POST /admin/project

**Resource:** [Admin/Project](../resources/Admin-Project.md)
**創建一個 project**
**Operation ID:** `post--admin-project`

Create a project without project id
1. if input usageTime not nil and forzen is true, accept input activateTime and expiredTime or input activateTime
2. if input usageTime not nil and frozen is false, only accept input expiredTime


## Request Body

body 請忽填 projectID , force 欄位


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateAdminProjectRequest](../schemas/Create/CreateAdminProjectRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | bad request |
| 500 | IAM server內部發生錯誤 |

**Success Response Schema:**

[CreateAdminProjectResponse](../schemas/Create/CreateAdminProjectResponse.md)

## Security

- **bearerAuth**
