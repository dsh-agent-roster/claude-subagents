# VoltAgent 子代理（迁移）

[English](README.md) | **简体中文**

一份 [Agent Roster](https://github.com/dsh-agent-roster/dsh-agent-roster) 档案：把
[`VoltAgent/awesome-claude-code-subagents`](https://github.com/VoltAgent/awesome-claude-code-subagents)
里的十五个子代理按用途分成三套团队——工程、平台、数据与 AI。

## 上游

- 仓库：[`VoltAgent/awesome-claude-code-subagents`](https://github.com/VoltAgent/awesome-claude-code-subagents)
- 许可证：MIT
- 星数：26,584（截至 2026-11-16）
- 范围：下面列出的十五个 `.md` 的 frontmatter 与正文，分别来自
  `categories/01-core-development`、`categories/03-infrastructure`、
  `categories/04-quality-security`、`categories/05-data-ai`。
  其余约九十个子代理没有迁移。

上游正文保持原文。只改了两处：字段名换成本档案格式；上游的工具列表
（`Read, Write, Edit, Bash, Glob, Grep`）只写进备注，**没有**映射成 toolPolicy——这些 Claude Code
工具名在部署里没有对应的策略 id，所以工具边界是「声明」而不是「强制」。

三套档案与成员：

| 档案 | 成员 |
|---|---|
| `engineering-squad` | 接口设计（队长） · 后端 · 前端 · 代码审查 · 测试自动化 |
| `platform-squad` | 云架构（队长） · Kubernetes · 发布 · 事故响应 · 安全审计 |
| `data-ai-squad` | LLM 架构（队长） · 数据工程 · 数据科学 · MLOps · AI 工程 |

## 用法

```bash
npx --yes @stofone/dsh-agent-roster@latest validate --dir .
```

或者在插件面板的「档案库」页签里订阅 `dsh-agent-roster/claude-subagents`。

## CI

`validate --dir .`、`registry validate`，以及一个 compile-diff 检查，保证 `dist/` 与
`rosters/`、`shared-roles/` 同步。
