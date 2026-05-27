# Models — 2026-05-27

## Xiaomi MiMo-V2.5 Global API Launch <a id="xiaomi-mimo-v25-global"></a>

**Source:** [GSMArena](https://www.gsmarena.com/xiaomi_releases_openweight_mimov25_ai_model_claims_frontierlevel_agentic_capability-news-72585.php) · [MiMo Platform](https://platform.xiaomimimo.com/docs/en-US/news/v2.5-open-sourced) · **Type:** release · **Time (UTC):** —

Released April 28 under an MIT license, MiMo-V2.5 opened its token-plan API globally on May 27 via platform.xiaomimimo.com and Xiaomi AI Studio, with a promotional 100-trillion-token giveaway running through May 28. The base model is a sparse MoE with 310 billion total parameters and 15 billion active, trained on 48 trillion tokens; a Pro tier scales to 1.02 trillion total (42B active). Both variants support a 1M-token context window with native text, image, and video inputs. Xiaomi claims MiMo-V2.5-Pro matches closed-source frontier models on image and video understanding tasks. API pricing is $1 per million input tokens — roughly one-seventh the cost of comparable Western offerings.

**Why it matters:** A production-ready, MIT-licensed multimodal MoE at sub-$2/M pricing adds a credible low-cost option for agent builders who need long context and vision. The open weights on Hugging Face make local deployment viable for teams with the hardware to run a 310B MoE.

| Variant | Total params | Active params | Context | Input price |
|---------|-------------|---------------|---------|-------------|
| MiMo-V2.5 | 310B | 15B | 1M | $1/M tokens |
| MiMo-V2.5-Pro | 1.02T | 42B | 1M | TBD |

---
