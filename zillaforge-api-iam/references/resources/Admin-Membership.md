# Admin/Membership

Membership API by Admin

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/admin/membership` | List ALL Existing memberships | [View](../operations/get-admin-membership.md) |
| POST | `/admin/membership` | CreateMembership | [View](../operations/post-admin-membership.md) |
| POST | `/admin/membership/batch` | CreateMembershipBatch | [View](../operations/post-admin-membership-batch.md) |
| GET | `/admin/membership/user/{user-id}/` | ListMembershipsByUser | [View](../operations/get-admin-membership-user-user-id.md) |
| GET | `/admin/membership/project/{project-id}/` | ListMembershipsByProject | [View](../operations/get-admin-membership-project-project-id.md) |
| GET | `/admin/membership/project/{project-id}/user/{user-id}/` | GetMembershipAndPermission | [View](../operations/get-admin-membership-project-project-id-user-user-id.md) |
| PUT | `/admin/membership/project/{project-id}/user/{user-id}/` | UpdateMembership | [View](../operations/put-admin-membership-project-project-id-user-user-id.md) |
| DELETE | `/admin/membership/project/{project-id}/user/{user-id}/` | DeleteMembership | [View](../operations/delete-admin-membership-project-project-id-user-user-id.md) |
| PATCH | `/admin/membership/project/{project-id}/user/{user-id}/owner` | 設定專案Owner | [View](../operations/patch-admin-membership-project-project-id-user-user-id-owner.md) |
