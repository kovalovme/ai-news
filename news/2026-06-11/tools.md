# Tools — 2026-06-11

## Claude Code v2.1.172 <a id="claude-code-2-1-172"></a>

**Source:** [Anthropic changelog](https://code.claude.com/docs/en/changelog) · **Type:** update · **Time (UTC):** 2026-06-10

Claude Code v2.1.172 ships four developer-facing changes. The headline addition is **nested sub-agents up to five levels deep**: a top-level session can now spawn an agent, which can spawn its own agents, and so on, enabling hierarchical multi-agent decomposition entirely within a single Claude Code invocation. A **plugin marketplace search** is now available from within the CLI, letting teams discover and install community-built tools without leaving the terminal. **Context optimization for 1M-context sessions** resolves a regression where sessions using the full one-million-token window would stall when usage credits ran out instead of gracefully truncating. AWS Bedrock **region handling** also receives fixes that surface the correct endpoint by default rather than requiring manual configuration.

**Why it matters:** Five-level sub-agent nesting removes the primary depth constraint that previously forced large agentic workflows to flatten their hierarchy or manage inter-process communication externally. The plugin marketplace integrates discovery into the existing session UX rather than requiring out-of-band package searches.

---
