# Tools — 2026-06-17

## Wolfram Language & Mathematica 15 <a id="wolfram-15"></a>

**Source:** [Stephen Wolfram Writings](https://writings.stephenwolfram.com/2026/06/launching-version-15-of-wolfram-language-mathematica-built-in-useful-ai-lots-of-new-core-functionality/) · **Type:** release · **Time (UTC):** Jun 16

Version 15, released June 16, ships three AI-facing layers. The **Wolfram Agent Tools framework** auto-detects Claude Code or Codex installed on the user's machine and configures them to evaluate Wolfram Language code, read/write notebooks, and analyze WL expressions — no manual setup required. A **built-in AI Assistant chatbar** appears at the bottom of notebooks in three tiers (Basic free, Pro, Research subscription); it generates executable WL code from natural language and can insert results directly into the notebook. Finally, wolfram.com now auto-serves Markdown content to AI agent user-agents and exposes a "For AIs" link with machine-readable configuration documentation.

**Why it matters:** Engineers using Claude Code or Codex can now invoke 40 years of Mathematica's symbolic computation, solvers, and curated knowledge base as first-class tools without manual MCP configuration — an instant capability expansion for any scientific or mathematical workflow running in an AI coding session.

---

## Claude Code v2.1.178–179 <a id="claude-code-2118x"></a>

**Source:** [Anthropic Releasebot](https://releasebot.io/updates/anthropic/claude-code) · **Type:** update · **Time (UTC):** Jun 16–17

The June 16–17 Claude Code releases add granular tool permission matching and tighten subagent security. The new `Tool(param:value)` permission syntax supports rules like `Agent(model:opus)` to block Opus-based subagents specifically, enabling per-model allowlists and blocklists in project or user settings. Skills placed in nested `.claude/` directories now load contextually — a skill in `apps/web/.claude/` only activates when the working directory is under `apps/web/`, avoiding namespace pollution. Subagent spawns in auto-mode now pass through a security classifier before launch. Version 2.1.179 also fixes mid-stream connection drops: partial responses are now preserved instead of surfacing raw errors.

**Why it matters:** The `Tool(param:value)` syntax gives platform operators and enterprise admins a practical mechanism to enforce model-tier cost policies (e.g., restrict background agents to Haiku, block Opus except for specific named flows) without custom middleware or proxy layers.

---

## Datasette 1.0a34: Row Write Operations in the UI <a id="datasette-10a34"></a>

**Source:** [Simon Willison's Weblog](https://simonwillison.net/) · **Type:** release · **Time (UTC):** Jun 16

Simon Willison released Datasette 1.0a34, the first alpha to surface row insertion, editing, and deletion directly in the Datasette web UI — completing the CRUD loop for the open-source SQLite explorer. The implementation was informed by patterns from the Datasette Agent work (covered June 16). A companion `click-to-play` Web Component released June 17 transforms a static image into an on-demand GIF, used to demo the new row-editing interface without auto-playing animations.

**Why it matters:** Row write access in the browser UI makes Datasette viable as a lightweight database admin tool rather than a read-only exploration layer — relevant for small teams running local AI pipelines who want a low-ceremony data interface alongside query tooling.

---

## Grok for PowerPoint <a id="grok-powerpoint"></a>

**Source:** [xAI Releasebot](https://releasebot.io/updates/xai) · **Type:** release · **Time (UTC):** Jun 16

xAI shipped a free Microsoft 365 add-in that generates full PowerPoint decks from outlines, adds individual slides, applies themes, and restructures sections. The add-in can pull from web search, X posts, email, SharePoint, and Google Drive via Grok connectors, embedding research from connected sources directly into slide content.

**Why it matters:** First-party Grok integration into M365 — which has the largest existing enterprise install base — gives xAI a distribution channel in corporate environments that doesn't require replacing Copilot or new procurement decisions.

---

## Grok Build: Agent Dashboard and Priority Processing API <a id="grok-build-dashboard"></a>

**Source:** [xAI Releasebot](https://releasebot.io/updates/xai) · **Type:** release · **Time (UTC):** Jun 15

Two developer-facing Grok Build releases shipped June 15. The **Agent Dashboard** (accessible via the `/dashboard` shortcut) allows simultaneous management of multiple active coding sessions; sessions sort by state with blocking tasks prioritized, and users can reply inline, dispatch new work, or switch between sessions from a single view. The **Priority Processing API** adds a `service_tier: "priority"` parameter to text, image, and video inference requests, enabling priority queue scheduling with usage-based billing applying only to prioritized calls.

**Why it matters:** Multi-session management and a priority inference tier are table-stakes for production agentic workloads; their arrival in Grok Build narrows the workflow gap with Claude Code's sub-agent orchestration and OpenAI's operator-tier tooling.

---
