# Tools — 2026-07-07

## OfficeCLI v1.0.129 <a id="officecli"></a>

**Source:** [GitHub](https://github.com/iOfficeAI/OfficeCLI) · [HN](https://news.ycombinator.com/item?id=48807225) · **Type:** release · **Time (UTC):** Jul 6 · **HN:** 173 pts

OfficeCLI is an open-source (Apache 2.0) CLI purpose-built for AI agents to read, edit, and automate Word (.docx), Excel (.xlsx), and PowerPoint (.pptx) files without requiring Office to be installed. The tool ships as a single self-contained binary across Windows, macOS, and Linux. Key agent-friendly design choices: every document element has a deterministic path (e.g., `/slide[1]/shape[1]`), every command returns structured JSON, and an embedded formula engine handles 350+ Excel functions. A built-in MCP server enables one-line registration with Claude Code, Cursor, and VS Code; once registered, agents gain direct JSON-RPC access to document manipulation tools. The latest release (v1.0.129, July 6) adds headless screenshot rendering for visual output verification in pipelines.

**Why it matters:** Office documents remain a dominant enterprise data format. OfficeCLI gives coding agents a reliable, offline-first, no-platform-dependency way to interact with them—filling a gap that previously required proprietary SDKs or cloud document APIs.

---

## Ternlight — 7 MB WASM embedding model for browsers <a id="ternlight"></a>

**Source:** [Demo](https://ternlight-demo.vercel.app/) · [HN](https://news.ycombinator.com/item?id=48811644) · **Type:** release · **Time (UTC):** Jul 6 · **HN:** 211 pts

Ternlight is a sentence-embedding model packaged as a 7 MB WebAssembly bundle that runs entirely on the client CPU—no server calls, no GPU, no installation. It outputs 384-dimensional vectors where cosine similarity indicates semantic relatedness; the demo demonstrates searching React documentation with zero backend infrastructure (e.g., "reset my password" vs "I forgot my password" scores 0.88 similarity). A lighter mini variant weighs 5 MB. The entire bundle—execution engine, model weights, tokenizer—fits within a single fetch.

**Why it matters:** At 7 MB loaded once, Ternlight makes client-side semantic search a practical option for latency-sensitive or privacy-preserving use cases (local note search, document retrieval in offline apps) without calling an embedding API endpoint. The WASM approach sidesteps WebGPU availability constraints, making it work across any modern browser.

---
