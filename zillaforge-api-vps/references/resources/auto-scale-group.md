# auto_scale_group

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/vps/api/v1/project/:{project-id}/auto_scale_groups/` | List AutoScaleGroup | [View](../operations/get-vps-api-v1-project-project-id-auto-scale-groups.md) |
| POST | `/vps/api/v1/project/:{project-id}/auto_scale_groups/` | Create AutoScaleGroup | [View](../operations/post-vps-api-v1-project-project-id-auto-scale-groups.md) |
| GET | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}` | Get AutoScaleGroup | [View](../operations/get-vps-api-v1-project-project-id-auto-scale-groups-asg-id.md) |
| PUT | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}` | Update AutoScaleGroup | [View](../operations/put-vps-api-v1-project-project-id-auto-scale-groups-asg-id.md) |
| DELETE | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}` | Delete AutoScaleGroup | [View](../operations/delete-vps-api-v1-project-project-id-auto-scale-groups-asg-id.md) |
| POST | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/approve` | Approve AutoScaleGroup Request | [View](../operations/post-vps-api-v1-project-project-id-auto-scale-groups-asg-id-approve.md) |
| POST | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/reject` | Reject AutoScaleGroup Request | [View](../operations/post-vps-api-v1-project-project-id-auto-scale-groups-asg-id-reject.md) |
| GET | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers` | List servers created by AutoScaleGroup | [View](../operations/get-vps-api-v1-project-project-id-auto-scale-groups-asg-id-servers.md) |
| GET | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers/:{svr-id}` | Get AutoScaleGroup's server info | [View](../operations/get-vps-api-v1-project-project-id-auto-scale-groups-asg-id-servers-svr-id.md) |
| POST | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers/:{svr-id}/action` | Do action to AutoScaleGroup's server | [View](../operations/post-vps-api-v1-project-project-id-auto-scale-groups-asg-id-servers-svr-id-action.md) |
| POST | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers/:{svr-id}/floatingip` | Associate FloatingIP to ASG's server | [View](../operations/post-vps-api-v1-project-project-id-auto-scale-groups-asg-id-servers-svr-id-floatingip.md) |
| GET | `/vps/api/v1/project/:{project-id}/auto_scale_groups/:{asg-id}/servers/:{svr-id}/vnc_url` | Get VNC console URL (asg's owner only) | [View](../operations/get-vps-api-v1-project-project-id-auto-scale-groups-asg-id-servers-svr-id-vnc-url.md) |
