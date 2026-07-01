# Tools — 2026-07-01

## Claude Code v2.1.197 <a id="claude-code-2197"></a>

**Source:** [Claude Code release notes](https://code.claude.com/docs/en/whats-new) · **Type:** update · **Time (UTC):** Jul 01

Claude Code v2.1.197 makes Claude Sonnet 5 the default model for all sessions, with its native 1-million-token context window active by default. The release also adds organizational controls: org admins can now set a default model for all members and apply model restrictions to prevent individual users from switching to higher-cost or unauthorized models. Additional changes include readable session names, clickable file attachments in the conversation pane, and a smoother agents view. On the security side, sandbox credential blocking prevents Claude Code from accessing credentials in the sandbox environment, and structured output reliability was improved.

MCP and plugin stability saw multiple fixes: remote MCP connection hangs, plugin startup failures, and background session recovery were all addressed. VS Code responsiveness was improved for large workspaces.

**Why it matters:** The combination of Sonnet 5 as the default and the 1M-token context window substantially extends the length of codebases and conversation histories Claude Code can reason about in a single session without truncation or context-window errors. Org model restrictions make Claude Code deployable in cost-controlled enterprise environments without per-user configuration.

---
