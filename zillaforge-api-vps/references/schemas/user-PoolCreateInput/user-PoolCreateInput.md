# user.PoolCreateInput

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `asg_id` | string | No |  |
| `member_port` | integer | Yes |  |
| `members` | user.MemberCreateInput[] | No |  |
| `method` | enum: ROUND_ROBIN, LEAST_CONNECTIONS, SOURCE_IP | Yes |  |
| `name` | string | Yes |  |
| `protocol` | string | Yes |  |

