# 认证与授权（`03-auth`）

_认证绕过、IDOR、JWT/OAuth、CSRF_

## authbypass-authentication-flaws  `P0`

认证绕过。当需要评估登录流程、密码重置逻辑、账户恢复、MFA 绕过、令牌可预测性、暴力破解防护与会话边界缺陷时使用。

## idor-broken-object-authorization  `P0`

IDOR 与对象级授权失效。当请求暴露对象标识符、租户边界、可写字段，或缺少对象级授权校验时使用。

## jwt-oauth-token-attacks  `P0`

JWT 与 OAuth 令牌攻击。当需要验证令牌信任、签名算法、密钥处理、声明滥用、bearer 流程与 OAuth 账户绑定缺陷时使用。

## oauth-oidc-misconfiguration  `P1`

OAuth 与 OIDC 配置错误。当需要审查重定向 URI 处理、state 与 nonce 校验、PKCE、令牌 audience、回调绑定与身份提供方信任缺陷时使用。

## csrf-cross-site-request-forgery  `P1`

CSRF 跨站请求伪造。当需要审查状态变更型 Web 流程、反 CSRF 防御、SameSite 行为、JSON CSRF、登录 CSRF 与 OAuth state 处理时使用。
