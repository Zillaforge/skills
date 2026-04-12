# Admin/Project

Project API by Admin

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/admin/projects` | 列出所有 project | [View](../operations/get-admin-projects.md) |
| POST | `/admin/project` | 創建一個 project | [View](../operations/post-admin-project.md) |
| GET | `/admin/project/{project-id}/` | 取得特定 project-id 的 project 資訊 | [View](../operations/get-admin-project-project-id.md) |
| PUT | `/admin/project/{project-id}/` | 更新一個project | [View](../operations/put-admin-project-project-id.md) |
| DELETE | `/admin/project/{project-id}/` | 刪除一個管理群組透過 ID | [View](../operations/delete-admin-project-project-id.md) |
| POST | `/admin/project/{project-id}/saml` | 創建saml by project id | [View](../operations/post-admin-project-project-id-saml.md) |
| GET | `/admin/project/{project-id}/saml/{saml-id}` | 取得 saml by project id and saml-id | [View](../operations/get-admin-project-project-id-saml-saml-id.md) |
| PUT | `/admin/project/{project-id}/saml/{saml-id}` | 更新 saml by project id and saml-id | [View](../operations/put-admin-project-project-id-saml-saml-id.md) |
| DELETE | `/admin/project/{project-id}/saml/{saml-id}` | 刪除 saml by project id and saml-id | [View](../operations/delete-admin-project-project-id-saml-saml-id.md) |
| GET | `/admin/project/{project-id}/samls` | 取得所有的saml by project id | [View](../operations/get-admin-project-project-id-samls.md) |
