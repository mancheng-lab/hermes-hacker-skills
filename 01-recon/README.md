# 侦察与攻击面（`01-recon`）

_资产测绘、端点发现、指纹识别、源码泄露_

## recon-and-methodology  `P0`

侦察与方法论。当需要测绘资产、发现端点、指纹识别技术栈、为新目标建立结构化测试计划时使用。

## attack-surface-mapping  `P0`

从单个授权目标 URL 或单个应用画出可测试的攻击面。当用户说攻击面、画攻击面、map the surface、application recon、JS inventory，或唯一可见页面只有登录框时使用。从应用已暴露的信息推导主机、API、密钥与对象图；不要一上来就目录爆破或 payload 喷洒。

## subdomain-takeover  `P1`

子域名接管检测与利用。当目标存在指向已下线云资源的悬空 CNAME/NS/MX 记录、过期的第三方服务、未认领的 SaaS 租户时使用。

## insecure-source-code-management  `P0`

源码管理与构建产物泄露（.git、.svn、.hg、备份文件、.env）。当侦察发现 VCS 路径、隐藏目录返回 403、或配置/备份泄露时使用。
