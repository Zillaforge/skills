# PUT /vps/api/v1/admin/quotas/projects/:{project-id}

**Resource:** [system_quota](../resources/system-quota.md)
**set project's quotas**
**Operation ID:** `put--vps-api-v1-admin-quotas-projects-:{project-id}`

Set quota limits of each resource type for specified project.

Request body parameters:
- vm: The maximum number of VM instances allowed per project.(optional)
- vcpu: The total amount of virtual CPU cores allowed per project.(optional)
- ram: The total RAM size allowed per project in MB.(optional)
- gpu: The count of GPUs allowed per project.(optional)
- block_size: The disk space limit on all volumes created within the project in GB.(optional)
- network: The total number of network allowed per project.(optional)
- router: The total number of routers allowed per project.(optional)
- floating_ip: The total number of Floating IP addresses allowed per project.(optional)
- loadbalancer: The total number of Load Balancers allowed per project.(optional)
- share: The total number of shares allowed per project.(optional)
- share_size: The max size of all shares per project in GB.(optional)

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [pb.QuotaUpdateInfo](../schemas/pb-QuotaUpdateInfo/pb-QuotaUpdateInfo.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.QuotaInfo](../schemas/pb-QuotaInfo/pb-QuotaInfo.md)

## Security

- **ApiKeyAuth**
