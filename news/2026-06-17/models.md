# Models — 2026-06-17

## Qwen Robot Suite: Three Embodied AI Foundation Models <a id="qwen-robotsuite"></a>

**Source:** [TechNode](https://technode.com/2026/06/17/alibaba-unveils-qwen-robot-series-with-three-foundation-models-for-embodied-ai/) · **Type:** release · **Time (UTC):** Jun 16–17

Alibaba's Qwen team released three foundation models targeting physical-world AI on June 16–17. **Qwen-RobotManip** standardizes end-effector motion as incremental poses in camera coordinates; trained on 38,100 hours of fully open-source data across multiple robot platforms, it topped the RoboChallenge generalist track with a process score of 59.83 and 45% task success rate. **Qwen-RobotNav** unifies instruction following, goal-directed navigation, target tracking, and autonomous driving within a single vision-language framework. **Qwen-RobotWorld** is a video world model that predicts physically consistent future states across manipulation, navigation, and driving scenarios, enabling a robot to simulate how a scene will unfold before acting.

**Why it matters:** A three-model suite trained on a shared open-source corpus across robot types signals that embodied AI is consolidating toward generalist foundation models — following the same trajectory as NLP two years ago. Researchers and integrators can build on a unified data story rather than assembling per-task fine-tunes.

| Model | Primary Task | Benchmark |
|-------|-------------|-----------|
| Qwen-RobotManip | Manipulation | 59.83 process score, 45% task success (RoboChallenge generalist) |
| Qwen-RobotNav | Navigation | Unified VLA across instruction-following, goal-nav, tracking, autonomous driving |
| Qwen-RobotWorld | World modeling | Predicts future states across manipulation/navigation/driving |

---

## Grok Imagine Video 1.5 Goes Generally Available <a id="grok-imagine-video-15"></a>

**Source:** [xAI](https://x.ai/news/grok-imagine-1-5) · **Type:** release · **Time (UTC):** Jun 16

xAI's Grok Imagine Video 1.5, first previewed May 30 and opened to API customers June 9, reached general availability on June 16 across grok.com, the Imagine API, and iOS/Android apps. The model animates a still image or text prompt into 720p/24fps clips (6–15 seconds) with natively synchronized audio — music, sound effects, and lip-synced dialogue. Generation time for a 6-second 720p clip is approximately 25 seconds, down from 40+ seconds. The model holds the top position on the Image-to-Video Arena leaderboard by a 52 Elo margin over the next competitor.

**Why it matters:** GA availability on the free grok.com tier removes the API-key barrier for native-audio video generation. Combined with SpaceX's Cursor acquisition (see ecosystem.md), image-to-video is now part of the same corporate stack as the AI IDE used by 4 million developers.

---

## Grok V9-Medium: 1.5T Coding Model in Final Pre-Release Window <a id="grok-v9-medium"></a>

**Source:** [TechTimes](https://www.techtimes.com/articles/318495/20260616/grok-v9-medium-arrives-spacex-seals-cursor-developers-face-model-choice-risk.htm) · **Type:** update · **Time (UTC):** Jun 16

Post-training on Grok V9-Medium (1.5 trillion parameters, approximately 3× the current Grok production model) is complete; xAI has been signaling a mid-June public release window, which opened June 16. The model is explicitly trained on Cursor developer workflow data — real IDE sessions from Cursor users — and is optimized for NVIDIA Blackwell GPU architecture. No public API endpoint or benchmark comparison was disclosed as of June 16. Grok V9-Medium is separate from Grok 5, which is a 6T MoE model still in training on Colossus 2.

**Why it matters:** V9-Medium represents xAI's targeted answer to Claude's coding benchmark lead, using training data sourced from the IDE SpaceX is acquiring. Once that deal closes, xAI will control both the training data pipeline and the primary distribution channel for the model.

---
