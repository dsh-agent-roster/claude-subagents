# VoltAgent subagents (migrated)

**English** | [简体中文](README.zh.md)

An [Agent Roster](https://github.com/dsh-agent-roster/dsh-agent-roster) archive: fifteen subagents from
[`VoltAgent/awesome-claude-code-subagents`](https://github.com/VoltAgent/awesome-claude-code-subagents),
grouped into three teams — engineering, platform, and data/AI.

## Upstream

- Repo: [`VoltAgent/awesome-claude-code-subagents`](https://github.com/VoltAgent/awesome-claude-code-subagents)
- License: MIT
- Stars: 26,584 (as of 2026-11-16)
- Scope: the frontmatter and body of the fifteen `.md` files listed below, taken from
  `categories/01-core-development`, `categories/03-infrastructure`,
  `categories/04-quality-security`, and `categories/05-data-ai`.
  The other ~90 subagents are not migrated.

Upstream text is kept in its original wording. Only two things changed: field names were moved to this
roster format, and the upstream tool list (`Read, Write, Edit, Bash, Glob, Grep`) is recorded as a note
instead of a toolPolicy — those Claude Code tool names do not map to a deployment toolPolicy id, so the
tool boundary is **declared, not enforced**.

Groups and members:

| Roster | Members |
|---|---|
| `engineering-squad` | api-designer (captain) · backend-developer · frontend-developer · code-reviewer · test-automator |
| `platform-squad` | cloud-architect (captain) · kubernetes-specialist · deployment-engineer · incident-responder · security-auditor |
| `data-ai-squad` | llm-architect (captain) · data-engineer · data-scientist · mlops-engineer · ai-engineer |

## Usage

```bash
npx --yes @stofone/dsh-agent-roster@latest validate --dir .
```

Or subscribe to it from the plugin panel's Library tab (`dsh-agent-roster/claude-subagents`).

## CI

`validate --dir .`, `registry validate`, and a compile-diff check that keeps `dist/` in sync with
`rosters/` and `shared-roles/`.
