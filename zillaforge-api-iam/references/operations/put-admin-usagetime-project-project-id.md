# PUT /admin/usagetime/project/{project-id}

**Resource:** [Admin/UsageTime](../resources/Admin-UsageTime.md)
**create/update project usage time**
**Operation ID:** `put--admin-usagetime-project-{project-id}`

建立或更新專案的有效期限


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | project id |

## Request Body

UpdateProjectUsageTimeRequest:
1. if forzen is true, accept input activateTime and expiredTime or input activateTime
2. if frozen is false, only accept input expiredTime
3. activateTime need after currentTime.
4. expiredTime need after activateTime and currentTime.


**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateProjectUsageTimeRequest](../schemas/Update/UpdateProjectUsageTimeRequest.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | bad request |
| 500 | IAM server內部發生錯誤 |

## Security

- **bearerAuth**
