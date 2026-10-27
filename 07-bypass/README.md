# 绕过与协议（`07-bypass`）

_WAF / 403 绕过、CSP、CORS、弱类型、HPP、开放重定向_

## waf-bypass-techniques  `P0`

WAF 绕过方法论与通用规避技术。当 Web 应用防火墙拦截注入 payload（SQLi、XSS、RCE），需要用编码、协议层技巧或 WAF 特有问题构造绕过时使用。

## 401-403-bypass-techniques  `P0`

401/403 绕过。当遇到管理后台、API 端点或受限路径返回拒绝访问时——覆盖路径操控、HTTP 方法篡改、请求头注入、协议降级与自动化绕过工具。

## csp-bypass-advanced  `P1`

高级 CSP 绕过。当 XSS 或数据外带被 CSP 拦截，需要寻找策略弱点、可信端点滥用、nonce 泄露或 CSP 拦不住的外带通道时使用。

## cors-cross-origin-misconfiguration  `P0`

CORS 跨域配置错误。当需要分析跨源信任、带凭据的浏览器读取、Origin 反射、预检策略缺陷与浏览器端对已认证 API 的访问时使用。

## type-juggling  `P1`

PHP 弱类型比较（==）绕过。当认证、HMAC/签名校验或令牌验证使用松散相等、数字强制转换或非严格类型的哈希比较时使用——常见于老旧 PHP 与 CTF 风格代码路径。

## http-parameter-pollution  `P1`

HTTP 参数污染 HPP。当重复的 query/body 键被服务器、代理、WAF 与应用框架以不同方式解析，导致过滤器与应用层取值不一致，可用于绕过、SSRF 第二 URL、逻辑滥用或 CSRF token 混淆时。

## open-redirect  `P1`

开放重定向。当 URL 参数、表单 action 或 JavaScript 汇聚点控制跳转目标，可能把用户重定向到攻击者可控地址时使用。
