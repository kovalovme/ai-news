# Tools — 2026-07-06

## Claude Apps Gateway: SSO and Spend Controls for Claude Code on Bedrock and Google Cloud <a id="claude-apps-gateway"></a>

**Source:** [Anthropic Blog](https://claude.com/blog/introducing-the-claude-apps-gateway) · [DevOps.com](https://devops.com/anthropic-adds-enterprise-gateway-to-simplify-claude-code-access-on-aws-and-google-cloud/) · [Google Cloud Blog](https://cloud.google.com/blog/topics/developers-practitioners/announcing-claude-apps-gateway-for-google-cloud) · **Type:** release · **Time (UTC):** June 29, 2026

Anthropic published the **Claude Apps Gateway**, a self-hosted control plane that sits between an organization's identity provider and Claude Code running on Amazon Bedrock or Google Cloud. The gateway is a single stateless container backed by PostgreSQL and handles:

- **Identity**: Acts as an OIDC relying party against Google Workspace, Microsoft Entra ID, Okta, or any standards-compliant provider; issues short-lived sessions to replace per-developer credentials.
- **Policy**: Distributes managed settings (model defaults, tool permissions, context window limits) to all developers at sign-in time, enforced at the gateway rather than individually.
- **Routing**: Holds the upstream cloud credential and routes inference to Anthropic's API, Amazon Bedrock, or Google Cloud with optional provider failover.
- **Spend control**: Daily, weekly, and monthly spend limits configurable per organization, group, or individual user, with OTLP-based reporting to customer-operated collectors.

The gateway is available now; code and deployment docs are at [code.claude.com/docs/en/claude-apps-gateway](https://code.claude.com/docs/en/claude-apps-gateway).

**Why it matters:** The major blocker for enterprise Claude Code adoption has been credential management — each developer needing their own Bedrock or Vertex credentials created friction and made audit trails fragmented. The gateway collapses this to a single upstream credential with per-user attribution, which is what security and finance teams require before approving org-wide rollouts. The provider failover feature also addresses the reliability concerns that have made some enterprises reluctant to commit to a single cloud path.

---

## Claude Code Dynamic Workflows Reach General Availability for Pro Users <a id="claude-code-dynamic-workflows-ga"></a>

**Source:** [TechTimes](https://www.techtimes.com/articles/319532/20260702/claude-code-dynamic-workflows-go-ga-pro-users-can-now-spawn-1000-parallel-agents.htm) · [Augment Code](https://www.augmentcode.com/learn/claude-code-general-availability) · **Type:** release · **Time (UTC):** July 2, 2026

Claude Code's **Dynamic Workflows** feature graduated from research preview to general availability on July 2, extending access to all Pro plan subscribers for the first time. The feature enables Claude to write its own orchestration scripts (`.claude/workflows/*.ts`) and coordinate up to **1,000 parallel subagents** within a single run — each running in an isolated worktree. Previously, orchestrated multi-agent runs were available only to enterprise accounts and limited research partners.

Key operational details:
- Subagents can be spawned with `isolation: "worktree"` for parallel file mutation without conflicts; worktrees clean up automatically if unchanged.
- The concurrency cap is `min(16, cpu_cores - 2)` at any moment; excess agents queue.
- A token budget parameter (`budget.total`) lets workflows self-limit on cost.
- Scripts are persisted per-session for resume after interruption.

**Why it matters:** The 1,000-agent ceiling at the Pro tier makes large-scale autonomous coding tasks accessible outside enterprise contracts. Workflows that previously required a codebase migration service or custom orchestration can now be expressed as a single `claude /loop` invocation. This also directly addresses the use case behind the ZCode and similar multi-agent coding tools that gained traction last week (covered Jul 2 digest).

---
