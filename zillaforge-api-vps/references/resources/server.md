# server

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/vps/api/v1/project/:{project-id}/servers` | List Servers | [View](../operations/get-vps-api-v1-project-project-id-servers.md) |
| POST | `/vps/api/v1/project/:{project-id}/servers` | Create Server | [View](../operations/post-vps-api-v1-project-project-id-servers.md) |
| GET | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}` | Get Server | [View](../operations/get-vps-api-v1-project-project-id-servers-svr-id.md) |
| PUT | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}` | Update Server | [View](../operations/put-vps-api-v1-project-project-id-servers-svr-id.md) |
| DELETE | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}` | Delete Server | [View](../operations/delete-vps-api-v1-project-project-id-servers-svr-id.md) |
| POST | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/action` | Do Action to server | [View](../operations/post-vps-api-v1-project-project-id-servers-svr-id-action.md) |
| GET | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/metric` | Get Server Metric | [View](../operations/get-vps-api-v1-project-project-id-servers-svr-id-metric.md) |
| GET | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics` | List Server's vNICs | [View](../operations/get-vps-api-v1-project-project-id-servers-svr-id-nics.md) |
| POST | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics` | Add a new vNIC to Server | [View](../operations/post-vps-api-v1-project-project-id-servers-svr-id-nics.md) |
| PUT | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics/:{nic-id}` | update server's vNIC | [View](../operations/put-vps-api-v1-project-project-id-servers-svr-id-nics-nic-id.md) |
| DELETE | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics/:{nic-id}` | Remove a vNIC from Server | [View](../operations/delete-vps-api-v1-project-project-id-servers-svr-id-nics-nic-id.md) |
| POST | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/nics/:{nic-id}/floatingip` | Associate FloatingIP to a vNIC | [View](../operations/post-vps-api-v1-project-project-id-servers-svr-id-nics-nic-id-floatingip.md) |
| GET | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/vnc_url` | Get VNC console URL (server's owner only) | [View](../operations/get-vps-api-v1-project-project-id-servers-svr-id-vnc-url.md) |
| GET | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/volumes` | List Server's volumes | [View](../operations/get-vps-api-v1-project-project-id-servers-svr-id-volumes.md) |
| POST | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/volumes/:{vol-id}` | Attach a Volume to Server | [View](../operations/post-vps-api-v1-project-project-id-servers-svr-id-volumes-vol-id.md) |
| DELETE | `/vps/api/v1/project/:{project-id}/servers/:{svr-id}/volumes/:{vol-id}` | Detach a volume from a server | [View](../operations/delete-vps-api-v1-project-project-id-servers-svr-id-volumes-vol-id.md) |
