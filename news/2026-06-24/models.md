# Models — 2026-06-24

## Mistral OCR 4 <a id="mistral-ocr-4"></a>

**Source:** [mistral.ai/news/ocr-4](https://mistral.ai/news/ocr-4/) · **Type:** release · **Time (UTC):** Jun 23

Mistral released OCR 4, a structured document-understanding model supporting 170 languages across 10 language groups and file formats including PDF, DOC, PPT, and OpenDocument. It tops OlmOCRBench at 85.20 and OmniDocBench at 93.07; human annotators preferred it over competing systems in 72% of evaluations across 600+ multilingual documents. Beyond raw text, the model outputs bounding boxes, block classification labels (titles, tables, equations, signatures), and per-page and per-word confidence scores. Pricing is $4/1,000 pages standard, $2/1,000 pages batch, and $5/1,000 pages via Document AI. Available immediately on Mistral Studio, Amazon SageMaker, Microsoft Azure AI Foundry, and as a self-hosted enterprise deployment.

**Why it matters:** Structured spatial metadata (bounding boxes + confidence scores) makes OCR 4 a drop-in improvement for RAG pipelines and agentic document workflows without requiring post-processing to locate content on a page. Batch pricing at $2/1,000 pages undercuts most competing cloud OCR APIs.

| Benchmark | Mistral OCR 4 | Prior SOTA |
|-----------|:-------------:|:----------:|
| OlmOCRBench | **85.20** | ~82 |
| OmniDocBench | **93.07** | — |
| Annotator preference | **72%** win rate | — |

---

## Baidu Unlimited-OCR (3B) <a id="baidu-unlimited-ocr"></a>

**Source:** [github.com/baidu/Unlimited-OCR](https://github.com/baidu/Unlimited-OCR) · **Type:** release · **Time (UTC):** Jun 22

Baidu open-sourced Unlimited-OCR, a 3-billion-parameter document parsing model under MIT license, on June 22; the accompanying arXiv paper landed June 23. The model is designed for single-pass long-horizon parsing with a 32,768-token context window, processing multi-page PDFs and image stacks in one inference call rather than page-by-page. It integrates with vLLM, SGLang, Ollama, llama.cpp, and Hugging Face Transformers. No benchmark comparisons were disclosed at launch, and training data composition is not documented.

**Why it matters:** MIT license plus compatibility with popular inference runtimes makes this a self-hostable alternative to cloud OCR APIs for teams processing large document volumes. The absence of published benchmarks is a gap that community evaluations will likely fill quickly given the model's HN traction (468 points).

---

## Qwen-AgentWorld (35B-A3B / 397B-A17B) <a id="qwen-agentworld-models"></a>

**Source:** [arxiv.org/abs/2606.24597](https://arxiv.org/abs/2606.24597) · [github.com/QwenLM/Qwen-AgentWorld](https://github.com/QwenLM/Qwen-AgentWorld) · **Type:** release · **Time (UTC):** Jun 23–24

The Qwen team released two open-source world-model variants—Qwen-AgentWorld-35B-A3B (35B total, 3B active) and -397B-A17B (397B total, 17B active)—alongside the paper described in [Research](research.md#qwen-agentworld). Both models are trained to simulate environment dynamics across 7 agentic domains using a 3-stage pipeline (continued pretraining → SFT → RL with hybrid rewards) on 10M+ real-world interaction trajectories. They achieve higher scores than existing frontier models on the released AgentWorldBench across all 7 domains.

**Why it matters:** Open world models that predict next environment states allow training RL agents without live environment access, cutting iteration cycles and compute costs in simulation-heavy agentic pipelines. Having two scale points (efficient vs. capable) gives practitioners a direct trade-off lever.

---
