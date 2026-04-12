# GET /vps/api/v1/project/:{project-id}/servers/:{svr-id}/metric

**Resource:** [server](../resources/server.md)
**Get Server Metric**
**Operation ID:** `get--vps-api-v1-project-:{project-id}-servers-:{svr-id}-metric`

Get server metrics including CPU/Memory/DISK/NETWORK usage info over time period.

Request cpu metric example:
curl -X 'GET' \
'https://localhost:9999/api/v1/project/871a0333-ae33-43f2-81f9-2432fa15cde7/servers/c43bcdda-a2de-400e-a510-537ed89e088a/metric?granularity=300&start=1735868843&type=cpu' \
-H 'accept: application/json'

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `svr-id` | path | string | Yes | Server ID |
| `direction` | query | enum: incoming, outgoing | No | Required if type is net |
| `granularity` | query | integer | No |  |
| `rw` | query | enum: read, write | No | Required if type is disk |
| `start` | query | integer | Yes | UNIX timestamp in second |
| `type` | query | enum: cpu, memory, disk... | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

Array of [op.MetricInfo](../schemas/op-MetricInfo/op-MetricInfo.md)

## Security

- **ApiKeyAuth**
