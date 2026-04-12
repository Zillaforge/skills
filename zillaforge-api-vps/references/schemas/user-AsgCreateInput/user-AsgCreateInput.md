# user.AsgCreateInput

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `boot_script` | string | No |  |
| `description` | string | No |  |
| `flavor_id` | string | Yes |  |
| `image_id` | string | Yes |  |
| `keypair_id` | string | No |  |
| `max_size` | integer | Yes |  |
| `metric` | enum: cpu, memory | Yes |  |
| `min_size` | integer | No | default value is '1' |
| `name` | string | Yes |  |
| `network_id` | string | Yes |  |
| `password` | string | No |  |
| `sg_ids` | string[] | Yes |  |
| `system_volume_type` | string | No |  |
| `threshold_down` | integer | Yes |  |
| `threshold_up` | integer | Yes |  |

