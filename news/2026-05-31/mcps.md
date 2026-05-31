# MCPs — 2026-05-31

## Anthropic Claude Platform: mid-conversation system messages, refusal categories, sandboxes on AWS <a id="anthropic-api-may29"></a>

**Source:** [Anthropic Release Notes](https://platform.claude.com/docs/en/release-notes/overview) · **Type:** update · **Time (UTC):** ~14:00

Three distinct Anthropic API updates landed May 29, all scoped to Claude Opus 4.8.

**Mid-conversation system messages.** The Messages API now accepts `role: "system"` entries at non-first positions in the messages array. Prior to this, any system-prompt change mid-session invalidated the prompt cache and forced a full re-encode. With Opus 4.8, cache hits are preserved even when the instruction context changes — useful for long-running agent loops that need to inject scoped directives without paying re-tokenization costs.

**Refusal categories in stop_details.** When Opus 4.8 declines a request, the response now includes a structured refusal category in `stop_details`, replacing the previous need to parse free-text refusal strings. Applications can branch on category type (policy, capability, safety, etc.) programmatically.

**Self-hosted sandboxes and Managed Agents on AWS.** Claude Platform on AWS now supports self-hosted sandboxes and Managed Agents multiagent orchestration — capabilities that were previously restricted to the direct Claude Platform (Cloudflare, Daytona, Modal, Vercel providers). Managed Agents webhooks (session and vault lifecycle events, announced May 7) are also now available on AWS.

**Why it matters:** Mid-conversation system messages let long-horizon agent sessions inject scoped context changes without cache invalidation — a meaningful latency and cost reduction for multi-step pipelines. Structured refusal categories eliminate fragile string-matching from safety-aware applications.

---
