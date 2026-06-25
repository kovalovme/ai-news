# Tools — 2026-06-25

## RubyLLM — Unified Ruby Interface for 14+ AI Providers <a id="rubyllm"></a>

**Source:** [rubyllm.com](https://rubyllm.com/) · [github.com/crmne/ruby_llm](https://github.com/crmne/ruby_llm) · **Type:** release · **Time (UTC):** Jun 24 (HN: 383 pts)

RubyLLM is a Ruby gem (current version 1.3.0) that provides a single API surface covering OpenAI, Anthropic, Gemini, VertexAI, xAI, Bedrock, DeepSeek, Mistral, Ollama, OpenRouter, Perplexity, GPUStack, and any OpenAI-compatible endpoint — 1,166 models across 11 hosted providers as of June 8 update. The library has three runtime dependencies (Faraday, Zeitwerk, Marcel) and supports chat, image generation, embeddings, tool/function calling, and multimodal workflows with a unified interface. Version 1.3.0 additions include native AWS Bedrock credential chain resolution (no manual credential setup for IAM roles) and text-to-speech output handling. The model registry was refreshed in June with aliases for Claude Opus 4.7, DeepSeek V4 Flash/Pro, Gemini Embedding 2, Gemma 4, and GPT-5.5. It reached 383 Hacker News points upon surfacing June 24.

**Why it matters:** Ruby on Rails applications that need to switch between AI providers or run evaluations across multiple backends previously required per-provider SDK integrations with incompatible streaming and tool-call conventions. RubyLLM normalizes those differences behind one interface, which lowers the maintenance cost for Rails shops exploring model routing or fallback strategies.

---
