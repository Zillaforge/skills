# pb.AsgInfo

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `approvedAt` | string | No |  |
| `boot_script` | string | No |  |
| `createdAt` | string | No |  |
| `description` | string | No |  |
| `flavor` | [pb.IDName](pb-IDName.md) | No |  |
| `flavor_detail` | [pb.FlavorInfo](pb-FlavorInfo.md) | No |  |
| `flavor_id` | string | No |  |
| `id` | string | No |  |
| `image` | [pb.VRMImgInfo](pb-VRMImgInfo.md) | No |  |
| `image_id` | string | No |  |
| `keypair` | [pb.IDName](pb-IDName.md) | No |  |
| `keypair_id` | string | No |  |
| `lb_pool` | [pb.IDName](pb-IDName.md) | No |  |
| `lb_pool_id` | string | No |  |
| `max_size` | integer | No |  |
| `metadatas` | object | No |  |
| `metric` | string | No |  |
| `min_size` | integer | No |  |
| `name` | string | No |  |
| `namespace` | string | No |  |
| `network` | [pb.IDName](pb-IDName.md) | No |  |
| `network_id` | string | No |  |
| `project` | [pb.IDName](pb-IDName.md) | No |  |
| `project_id` | string | No |  |
| `security_groups` | pb.IDName[] | No |  |
| `servers` | pb.AsgServerInfo[] | No |  |
| `sg_ids` | string[] | No |  |
| `status` | string | No |  |
| `status_reason` | string | No |  |
| `system_volume_type` | string | No |  |
| `threshold_down` | integer | No |  |
| `threshold_up` | integer | No |  |
| `updatedAt` | string | No |  |
| `user` | [pb.IDName](pb-IDName.md) | No |  |
| `user_id` | string | No |  |
| `uuid` | string | No |  |

