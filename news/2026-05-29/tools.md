# Tools — 2026-05-29

## Claude Code v2.1.154 + v2.1.156 <a id="claude-code-2-1-154"></a>

**Source:** [Claude Code Changelog](https://code.claude.com/docs/en/changelog) · **Type:** release · **Time (UTC):** May 28–29

v2.1.154 (May 28) is the largest Claude Code release in weeks, anchored by Opus 4.8 integration and the new Dynamic Workflows feature. `/workflows` opens a runs panel for monitoring background multi-agent jobs; `! <command>` in the agents view spawns a shell command as a detachable background session. Additional highlights: `/simplify` now runs cleanup-only (reuse, simplification, efficiency) instead of a full `--fix` review; Chrome browser selection via `/chrome`; `defaultEnabled: false` in plugin manifests; Lean System Prompt default for all post-4.7 models; Claude avoids multiple-choice questions when it already has enough context to decide. Thirty-five bug fixes include a critical `rm -rf $HOME` sandbox bypass when `HOME` has a trailing slash, orphaned `--bg-pty-host` processes spinning at 100% CPU on macOS, Windows update rollback failures, and numerous background-session edge cases.

v2.1.156 (May 29) is a single-fix hotfix: thinking blocks sent to Opus 4.8 were being silently modified in transit, causing API 400 errors on extended-thinking tasks.

v2.1.153 (also May 28, released earlier the same day): `skipLfs` option for git/github plugin sources, status line commands now receive `COLUMNS`/`LINES` environment variables, `claude doctor` shows last update result.

**Why it matters:** Dynamic Workflows is the Claude Code interface to Opus 4.8's multi-agent orchestration — complex agent pipelines are now a `/workflows` command away, without additional infrastructure. The `rm -rf $HOME` bypass fix is a security-critical patch that should prompt immediate updates.

```mermaid
flowchart LR
    CC[Claude Code\nv2.1.154] --> DW[Dynamic Workflows\n/workflows panel]
    CC --> FM[Fast Mode\n2.5x Opus speed]
    CC --> LSP[Lean System Prompt\nnew default]
    CC --> CP[Chrome Picker\n/chrome]
    CC --> SF[/simplify\ncleanup-only]
```

---

## QwenPaw v1.1.9 <a id="qwenpaw-v1-1-9"></a>

**Source:** [GitHub releases — agentscope-ai/QwenPaw](https://github.com/agentscope-ai/QwenPaw/releases/tag/v1.1.9) · **Type:** release · **Time (UTC):** May 27

QwenPaw v1.1.9 ships a full Coding Mode: a three-panel Web IDE layout with a file tree, tabbed code editor with inline diff review, and a Git panel, all served from the local QwenPaw process. A Skill Market tab consolidates plugins across Aliyun, ClawHub, and ModelScope into a single install flow. Background tasks now accept explicit timeout parameters. A new tool guard system returns explicit denial feedback to prevent agents from silently retrying blocked operations. Per-channel access controls (whitelist/blacklist) and QQ interactive approval cards also land in this release.

**Why it matters:** QwenPaw now competes directly with Claude Code and OpenClaw for developers who want a self-hosted, open-source coding agent with an IDE-grade interface — particularly relevant for teams outside Anthropic's geographic footprint or on restrictive network environments.

---
