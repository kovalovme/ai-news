# Products — 2026-07-04

## Claude Enterprise Gets Admin Analytics Dashboard and Spend Controls <a id="claude-enterprise-analytics"></a>

**Source:** [claude.com/blog](https://claude.com/blog/giving-admins-more-visibility-and-control-over-claude-usage-and-spend) · **Type:** update · **Time (UTC):** Jul 02

Anthropic shipped a significant update to the Claude Enterprise admin console on July 2, adding granular cost visibility and model access controls designed for the economics of agentic workloads. Admins can now view usage and cost breakdowns by SCIM group and by individual user, with Claude Code-specific metrics (active developers, session counts, artifacts created, files edited) displayed alongside their cost contribution. An "Analytics Chat" interface allows natural-language queries over usage data. New control mechanisms include model-level entitlements (restricting which Claude models a group can default to), spend-threshold alerts at 75% and 90% of organizational limits, and an Analytics API that integrates with external tooling such as Datadog and CloudZero. An admin API enables programmatic cost-control workflow automation at scale.

**Why it matters:** The previous admin tooling was designed for SaaS chat economics; this release reflects the shift to agentic workloads where a single long-running session can consume 10×–100× the tokens of a chat exchange. The threshold alerts and per-group caps give finance and IT teams practical levers to prevent the kind of budget exhaustion that made headlines at Uber (burned its 2026 token budget by April) without requiring manual monthly reporting cycles.

---

## California + Anthropic: Largest US State Government AI Deployment <a id="california-anthropic-deal"></a>

**Source:** [Governor of California](https://www.gov.ca.gov/2026/06/29/governor-newsom-announces-a-first-of-its-kind-partnership-providing-anthropic-tools-to-state-agencies-and-improving-services-for-californians/) · **Type:** launch · **Time (UTC):** Jun 29

Governor Gavin Newsom announced a first-of-its-kind partnership with Anthropic on June 29, providing Claude access to California's approximately 500,000 state employees at a 50% discount, with the same terms extended to all California cities and counties. The agreement includes free workforce training and developer technical assistance from Anthropic. Early pilot deployments include the California DMV (customer service automation, reducing wait times) and the Department of Healthcare Services — the largest Medicaid agency in the US — using Claude for internal Medicaid workflow assistance. The deal is described as the largest government AI deployment agreement in US history by contract size.

**Why it matters:** This is the first major example of a US state government procuring frontier AI at scale through a direct discount agreement rather than through federal GSA schedules or commercial cloud marketplaces. The structure — discounted access plus embedded training — positions Claude as the de facto AI default across 58 counties and hundreds of city governments, creating a significant distribution channel and a template that other states are likely to follow.

---
