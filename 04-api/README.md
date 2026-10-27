# API 安全（`04-api`）

_API 侦察、BOLA、令牌滥用、GraphQL_

## api-recon-and-docs  `P0`

API 侦察与文档审查。当需要发现端点、schema、版本、OpenAPI 规范、隐藏文档与 API 测试面时使用。

## api-authorization-and-bola  `P0`

API 授权与 BOLA 测试。当 API 暴露对象标识符、嵌套资源、隐藏可写字段或函数级授权薄弱时使用。

## api-auth-and-jwt-abuse  `P0`

API 认证与 JWT 滥用。当需要测试 bearer token、API key、声明信任、请求头伪造、速率限制与 API 认证边界弱点时使用。

## graphql-and-hidden-parameters  `P1`

GraphQL 与隐藏参数测试。当需要探测内省、批处理、未公开字段、隐藏参数、schema 滥用与 GraphQL 授权缺口时使用。
