# user.SvrCreateInput

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `boot_script` | string | No |  |
| `description` | string | No |  |
| `flavor_id` | string | Yes |  |
| `image_id` | string | Yes |  |
| `keypair_id` | string | No |  |
| `name` | string | Yes |  |
| `nics` | user.NicCreateInput[] | Yes |  |
| `password` | string | No |  |
| `system_volume_type` | string | No |  |
| `volumes` | user.ServerDiskInput[] | Yes |  |

