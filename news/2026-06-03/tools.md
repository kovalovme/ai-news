# Tools — 2026-06-03

## Claude Code v2.1.161 <a id="claude-code-2-1-161"></a>

**Source:** [GitHub releases](https://github.com/anthropics/claude-code/releases) · **Type:** release · **Time (UTC):** Jun 2, 21:58

Claude Code v2.1.161 focuses on observability improvements and correctness fixes. Notable changes:

- **OTEL labels:** `OTEL_RESOURCE_ATTRIBUTES` values now appear as labels on metric datapoints, enabling custom dimensions in existing telemetry stacks.
- **MCP UI cleanup:** `/mcp` panel collapses unused connectors behind a "Show unused connectors" disclosure row.
- **Parallel tool call fix:** Failed Bash commands in a parallel tool-call batch no longer cancel other calls in the same batch — a correctness regression from earlier versions.
- **Linux clipboard:** Full Wayland clipboard support added (wl-copy / xclip / xsel).
- Additional fixes: background subagent stdout corruption in `claude -p`, Windows bash hooks with explicit paths, OpenTelemetry log events dropped before telemetry initialization, `claude mcp` commands that were printing secrets to output.

**Why it matters:** The parallel-call cancellation bug was silently aborting unrelated shell commands in multi-step agent loops; the fix is critical for any workflow that fans out Bash work in parallel. The OTEL label support lets platform teams track Claude Code usage by workspace, project, or team without custom instrumentation.

---

## Workday Developer Agent and Agent Passport <a id="workday-developer-agent"></a>

**Source:** [Workday newsroom](https://newsroom.workday.com/2026-06-02-Workday-Launches-New-Tools-for-Developers-to-Build,-Connect,-and-Verify-AI-Agents-For-HR,-Finance,-and-IT) · **Type:** launch · **Time (UTC):** Jun 2, ~13:00

Workday DevCon 2026 unveiled two developer-facing tools. **Developer Agent** accepts plain-language instructions from within Claude Code, Cline, Cursor, or Google Antigravity and scaffolds or modifies Workday apps and agents directly using the open AgentSkills standard — going from a natural-language request to a working Workday extension without leaving the coding environment. **Agent Passport** is a runtime compliance layer: security vendors (Cisco, CrowdStrike, and others) can issue a digital credential certifying an agent is safe to deploy; Agent Passport then continuously monitors running agents and can block, reroute, or restrict them based on company policy. Both features are in early access via Workday Extend Professional; GA is projected for H2 2026.

**Why it matters:** Agent Passport directly addresses the enterprise blocker of "who is responsible if an AI agent takes a destructive action in a payroll system?" — it externalizes accountability to a verifiable credential issued by an audited third party and provides continuous runtime enforcement, not just pre-deployment review.

---
