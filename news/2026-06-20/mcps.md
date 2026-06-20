# MCPs — 2026-06-20

## Simon Willison: MCP's idealized form is an auth gateway <a id="willison-mcp-auth-gateway"></a>

**Source:** [simonwillison.net](https://simonwillison.net) · **Type:** commentary · **Time (UTC):** Jun 19

Simon Willison surfaced a Hacker News comment arguing that the idealized form of MCP is simply "an auth gateway for the API and nothing else" — isolating authentication flows outside an agent's context window rather than encoding server logic inside the protocol. Willison's brief post framed this as a useful clarifying frame for MCP architecture debates.

**Why it matters:** The auth-gateway framing, if widely adopted, would push MCP servers toward thin authentication proxies rather than full application servers — a significant architectural choice that affects how teams build and secure MCP integrations.

---
