# MCPs — 2026-06-25

## Salesforce Agentforce 3 Anchors Around MCP <a id="salesforce-agentforce-3-mcp"></a>

**Source:** [thenewstack.io — MCP's growing pains](https://thenewstack.io/model-context-protocol-roadmap-2026/) · [getknit.dev — Future of MCP](https://www.getknit.dev/blog/the-future-of-mcp-roadmap-enhancements-and-whats-next) · **Type:** adoption · **Time (UTC):** Jun 23

Salesforce anchored the latest version of its Agentforce agent platform (v3) around MCP, treating the protocol as the primary interoperability layer. The announcement included three immediately available servers: Salesforce DX (developer tooling), Heroku Platform, and MuleSoft — plus a Slack MCP server listed as in development. The MCP spec update from June 18 that preceded this announcement formalized OAuth Resource Server classification for MCP servers and added resource indicators to prevent access token reuse across servers, directly addressing the authentication attack surface that had been the main enterprise adoption blocker. Salesforce joining with named servers representing its entire cloud portfolio signals MCP has reached a tier where major PaaS vendors are building first-party integrations rather than relying on the community.

**Why it matters:** Four named Salesforce servers covering DX, Heroku, MuleSoft, and (soon) Slack give agents a standardized path into the Salesforce ecosystem without custom connectors. For engineers building cross-platform workflows that touch Salesforce CRM or Heroku deployments, MCP-native access removes the need for Apex REST wrappers or third-party middleware.

---
