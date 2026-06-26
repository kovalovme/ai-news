# MCPs — 2026-06-26

## MCP Rust SDK rmcp-v1.8.0 <a id="rmcp-v180"></a>

**Source:** [modelcontextprotocol/rust-sdk](https://github.com/modelcontextprotocol/rust-sdk/releases) · **Type:** release · **Time (UTC):** 12:29 Jun 23

The official Rust SDK for MCP released rmcp-v1.8.0 and rmcp-macros-v1.8.0 simultaneously. Key changes:

- Resource-not-found error codes are now standardized across the codebase
- OAuth authorization response issuer is validated before acceptance, blocking authorization-server substitution attacks
- OIDC `application_type` is set to `native` during dynamic client registration, reducing misconfigured redirect-URI acceptance by downstream identity providers
- **Source-breaking change:** `Peer::peer_info()` now returns `PeerInfo` by value rather than by reference — callers must update
- `rmcp-macros`: deprecation warnings added for roots, sampling, and logging features; tool schema validation bug fixed

**Why it matters:** The OAuth hardening closes two attack surfaces that have been flagged in production MCP deployments. Any team running authenticated MCP servers with the Rust SDK should audit their `Peer::peer_info()` callers before upgrading — the return-type change is silent at runtime but breaks compilation.

---
