# Hermes Hacker Skills

面向 [Hermes Agent](https://github.com/NousResearch/hermes-agent) 的渗透测试技能包，
按攻击阶段归类、去重、中文化，可直接放入 `\~/.hermes/skills/hacker/` 使用。

从 3 个上游仓库的 **105 个源技能**中整理出 **56 个高频技能**，归入 15 个子类。
全部 `SKILL.md` 统一为 Hermes 可直接加载的格式：front matter 仅含 `name` 与 `description`，
description 为中文并写明触发场景，正文保留原始可执行的命令、payload 与绕过手法（未删减技术细节）。

完整清单见 [技能清单.md](技能清单.md)。

\---

## 快速开始

```bash
git clone https://github.com/mancheng-lab/hermes-hacker-skills.git
mkdir -p \~/.hermes/skills/hacker
cp -r hermes-hacker-skills/\* \~/.hermes/skills/hacker/
```

启动 Hermes 确认加载：

```bash
hermes skills list | grep -c hacker
```

建议只装 P0 核心（约 30 个）以节省上下文，具体见 [技能清单.md](技能清单.md) 中的优先级标注。

## 子类总览

|子类|名称|数量|
|-|-|-|
|`00-router`|入口路由|1|
|`01-recon`|侦察与攻击面|4|
|`02-injection`|注入类|10|
|`03-auth`|认证与授权|5|
|`04-api`|API 安全|4|
|`05-file`|文件与上传|2|
|`06-server`|服务端漏洞|6|
|`07-bypass`|绕过与协议|7|
|`08-logic`|业务逻辑|1|
|`09-post-exploit`|后渗透与提权|7|
|`10-ad`|域渗透|3|
|`11-cloud`|云与容器|2|
|`12-ai-security`|AI 安全|2|
|`13-code-audit`|代码审计|1|
|`14-knowledge`|安全知识库|1|

## 来源与许可

本仓库是基于以下三个 MIT 许可项目的整理与二次分发：

|上游|地址|许可|
|-|-|-|
|hack-skills|https://github.com/yaklang/hack-skills|MIT（含 LICENSE 文件）|
|secknowledge-skill|https://github.com/Pa55w0rd/secknowledge-skill|MIT（README 声明）|
|code-audit|https://github.com/3stoneBrother/code-audit|MIT（README 声明）|

### 本仓库所做的改动

* 从 105 个源技能中筛选 56 个高频技能，按 15 个子类重新归档
* 合并 `prototype-pollution` 与 `prototype-pollution-advanced`（基础篇在前，进阶篇分节在后）
* 合并 `business-logic-vuln` 路由文件至 `business-logic-vulnerabilities` 主体
* 统一 front matter 为 `name` + `description`，description 译为中文
* 剔除 `site/`、`assets/`、`image/`、`.github/` 等静态资源与构建脚本
* **正文技术内容（命令、payload、绕过手法）未做删改**

未选入的 49 个源技能（CTF/二进制/密码学专项、低频专项）可回溯上游仓库获取。

## 安全与合规

> \*\*本仓库内容仅供授权安全测试、教学研究与 CTF 演练使用。\*\*
> 使用者须确保其行为符合所在地法律法规，并获得目标系统的明确书面授权。
> 作者不对任何未授权使用或滥用行为负责。

使用这些技能时，建议关闭 Hermes 的辅助客户端标题生成，
避免会话中抓到的凭据、令牌在上下文压缩时外发至模型服务端：

```yaml
# \~/.hermes/config.yaml
auxiliary:
  title\_generation:
    enabled: false
```

## 许可

[MIT](LICENSE) — 保留上游版权声明，修改部分另行署名。

