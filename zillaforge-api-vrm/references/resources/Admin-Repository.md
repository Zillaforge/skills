# Admin/Repository

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/admin/repositories` | 列出所有的 repositories | [View](../operations/get-admin-repositories.md) |
| POST | `/admin/repository` | 創建 repository | [View](../operations/post-admin-repository.md) |
| GET | `/admin/repository/:{repository-id}` | 取得指定的 repository | [View](../operations/get-admin-repository-repository-id.md) |
| PUT | `/admin/repository/:{repository-id}` | 更新指定的 repository | [View](../operations/put-admin-repository-repository-id.md) |
| DELETE | `/admin/repository/:{repository-id}` | 棄用指定的 repository | [View](../operations/delete-admin-repository-repository-id.md) |
| POST | `/admin/repository/:{repository-id}/protect` | 設定保護指定的 repository (避免被刪除) | [View](../operations/post-admin-repository-repository-id-protect.md) |
| DELETE | `/admin/repository/:{repository-id}/protect` | 解除保護指定的 repository | [View](../operations/delete-admin-repository-repository-id-protect.md) |
