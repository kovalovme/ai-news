# Models — 2026-06-23

## GPT-5.5-Cyber (DayBreak update) <a id="gpt-55-cyber"></a>

**Source:** [OpenAI / Axios](https://www.axios.com/2026/06/22/openai-rolls-out-more-capable-version-of-cyber-model) · **Type:** update · **Time (UTC):** ~17:00

OpenAI released an improved version of GPT-5.5-Cyber on June 22 as part of the DayBreak initiative expansion. The updated model scores 85.6% on CyberGym (measuring autonomous reproduction of known vulnerabilities), up from 81.8% for standard GPT-5.5, and 39.5% on ExploitGym (up from 25.95%). On SEC-bench Pro the model reaches 69.8% versus 63.1% for the base model. During early access, it autonomously found a 23-year-old use-after-free bug in OpenBSD's kernel, five exploitable issues in Chrome's V8, and 10+ vulnerabilities in WebKit.

**Why it matters:** The gap between GPT-5.5-Cyber and the base GPT-5.5 on exploitation benchmarks is unusually large (+13.5 pp on ExploitGym), suggesting the specialized fine-tuning pipeline is doing real work rather than marginal tuning; security engineers using the DayBreak partner tools will get noticeably different results than using the standard API.

| Benchmark | GPT-5.5 | GPT-5.5-Cyber |
|-----------|--------:|---------------:|
| CyberGym | 81.8% | 85.6% |
| ExploitGym | 25.95% | 39.5% |
| SEC-bench Pro | 63.1% | 69.8% |

Access remains restricted to verified defenders through the Trusted Access for Cyber program; not available on the general API.

---
