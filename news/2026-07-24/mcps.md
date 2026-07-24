# MCPs — 2026-07-24

## MCP 2026-07-28 Release Candidate: Breaking Changes Documented <a id="mcp-rc-2026-07-28"></a>

**Source:** [MCP blog](https://blog.modelcontextprotocol.io/posts/2026-07-28-release-candidate/) · **Type:** update · **Time (UTC):** —

The official release candidate post for the 2026-07-28 MCP specification is now published, with a migration-focused breakdown of breaking changes. The most disruptive change is removal of the `initialize`/`initialized` handshake and `Mcp-Session-Id` header — every request is now self-contained, enabling plain round-robin load balancing without sticky sessions or shared session stores. Error code `-32002` for missing resources is replaced by JSON-RPC standard `-32602`. The RC also formalizes MCP Apps (server-rendered UI via sandboxed iframe with prefetch declarations) and a formal Extensions framework with reverse-DNS identifiers and independent versioning. Authorization aligns to OAuth 2.0 / OIDC with mandatory `iss` parameter validation per RFC 9207.

**Why it matters:** Any MCP server currently using sticky sessions, SSE streams for server-to-client requests, or the old `-32002` error code will break on July 28. Hosts and gateways need to add `Mcp-Method` and `Mcp-Name` headers for proper routing; clients must thread explicit handles through tool calls instead of relying on session state. SDK betas (Python, TypeScript, Go, C#) covering these changes were released July 22.

| Change | Action required |
|---|---|
| No `initialize` handshake | Remove session init; each request is self-contained |
| `Mcp-Session-Id` removed | Drop session header from all clients |
| Error code `-32002` → `-32602` | Update error-matching logic |
| `InputRequiredResult` replaces SSE streams | Rewrite server-to-client request handling |
| `iss` validation mandatory | Validate issuer claim on all OAuth tokens |

---
