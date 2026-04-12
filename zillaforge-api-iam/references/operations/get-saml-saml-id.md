# GET /saml/{saml-id}

**Resource:** [User/SAML](../resources/User-SAML.md)
**取得 SAML metadata**
**Operation ID:** `get--saml-{saml-id}`

get saml metadata


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `saml-id` | path | string | Yes | saml id |

## Responses

| Status | Description |
|--------|-------------|
| 200 | OK |
| 400 | admin project 不存在 |
| 500 | IAM Server 發生內部錯誤 |

## Security

- **bearerAuth**
