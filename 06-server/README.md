# 服务端漏洞（`06-server`）

_SSRF、请求走私、反序列化、竞态、未授权服务_

## ssrf-server-side-request-forgery  `P0`

服务端请求伪造 SSRF。当服务端会抓取 URL、解析主机名、导入远程内容，或可被驱动访问内网、云元数据与二级协议时使用。

## request-smuggling  `P0`

HTTP 请求走私与反序列化失步。当前置代理、CDN 或负载均衡与源站对消息分帧（Content-Length 与 Transfer-Encoding）判断不一致、存在 HTTP/2 到 HTTP/1 转换，或需要探索浏览器 fetch 流水线导致的客户端失步时使用。

## deserialization-insecure  `P0`

不安全反序列化。当 Java、PHP 或 Python 应用通过 ObjectInputStream、unserialize、pickle 或类似机制反序列化不可信数据，可能导致 RCE、文件访问或提权时使用。

## race-condition  `P0`

竞态条件与 TOCTOU。当需要测试一次性操作、并发 HTTP 滥用、速率限制绕过、Turbo Intruder 并发门、HTTP/2 单包攻击与 CWE-362 型同步缺口时使用。

## http-host-header-attacks  `P1`

HTTP Host 头注入与路由滥用。当应用信任 Host 头来生成 URL、路由请求或做访问控制时——可导致密码重置投毒、Web 缓存投毒、经路由的 SSRF 与虚拟主机绕过。

## unauthorized-access-common-services  `P0`

常见服务未授权访问。当 Redis、Rsync、PHP-FPM、AJP/Ghostcat、Hadoop YARN、H2 Console 等管理接口暴露且无认证时使用。
