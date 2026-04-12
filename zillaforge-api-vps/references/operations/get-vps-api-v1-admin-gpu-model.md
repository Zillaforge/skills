# GET /vps/api/v1/admin/gpu_model/

**Resource:** [system_gpu_model](../resources/system-gpu-model.md)
**List All GPU models**
**Operation ID:** `get--vps-api-v1-admin-gpu_model-`

Return all gpu models and their types of passthough or VGPUs available for use by users.

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[admin.GpuModelInfo](../schemas/admin-GpuModelInfo/admin-GpuModelInfo.md)

## Security

- **ApiKeyAuth**
