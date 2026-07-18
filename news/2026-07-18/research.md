# Research — 2026-07-18

## WAICA 2026: World AI Conference Inaugurates First Peer-Reviewed Academic Track <a id="waica-2026"></a>

**Source:** [WAICA 2026](https://waica2026.worldaic.com.cn/) · [36kr English](https://eu.36kr.com/en/p/3897977781946249) · [CGTN](https://news.cgtn.com/news/2026-07-15/Graphics-A-guide-to-WAIC-Academic-and-Awards-1ONG4oNcb9S/p.html) · **Type:** conference · **Time (UTC):** Jul 18 01:00 (opening)

The World AI Conference Academic (WAICA) held its inaugural session July 18–20, 2026 in Shanghai as a standalone peer-reviewed track within WAIC 2026. WAICA accepted 57 papers from 282 valid submissions (≈ 20% acceptance rate), with contributions from Princeton, Cambridge, Imperial College London, Tsinghua, Peking University, Nanyang Technological University, and Shanghai Jiao Tong University across ten-plus countries. Proceedings will be published by Springer LNCS. The afternoon of July 18 featured the inaugural Best Paper Award and Best Student Paper Award session, with five to seven domain experts scoring live. Andrew Chi-Chih Yao (Turing Award, Tsinghua) chairs the conference; Richard Sutton (Turing Award, co-developer of TD-learning and policy gradient methods) serves as international co-chair.

**Why it matters:** WAIC has historically been a product showcase and policy summit; WAICA transforms it into a venue for peer-reviewed science, a deliberate move to establish Shanghai alongside NeurIPS, ICML, and ICLR as a destination for frontier AI research. With two Turing Award laureates chairing, the conference has immediate credibility signaling. The accepted-paper pool spanning ten countries also tests whether China's AI academic institutions can attract international submissions in a post-WAIC governance year.

---

## VideoChat3: Fully Open 4B Video MLLM for Streaming and Long-Form Video <a id="videochat3"></a>

**Source:** [arXiv 2607.14935](https://arxiv.org/abs/2607.14935) · [GitHub MCG-NJU/VideoChat3](https://github.com/MCG-NJU/VideoChat3) · **Type:** paper · **Time (UTC):** submitted Jul 16

VideoChat3, from Nanjing University's MCG lab, is a fully open 4-billion-parameter multimodal video LLM designed for both offline and streaming video understanding. Its two core architectural contributions are an Inflated 3D Vision Transformer (I3D-ViT) that extends a 2D ViT to temporal sequences without retraining from scratch, and Adaptive Frame Resolution for Streaming Video Perception, which dynamically reduces the number of visual tokens at high frame rates. Training used three newly released datasets: VideoChat3-Academic2M (2M clip-instruction pairs), VideoChat3-LV116K (long-form, 116K), and VideoChat3-OL617K (online/streaming, 617K). The paper reports that VideoChat3 surpasses open-source models with equal or larger parameter counts on standard video QA benchmarks, and was the #1 trending model on Hugging Face in the week of July 14–17. Code, model weights, and all three datasets are released.

**Why it matters:** The combination of efficient streaming inference and full open release (code + data + weights) makes VideoChat3 a practical baseline for teams building on real-time video understanding — CCTV analysis, sports analytics, live-coding agents that watch the screen. The 4B parameter size keeps it runnable on a single consumer GPU, and the three-dataset release should enable independent fine-tuning at a scale that previous video MLLM work rarely shared.

---
