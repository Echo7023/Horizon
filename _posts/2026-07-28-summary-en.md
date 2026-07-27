---
layout: default
title: "Horizon Summary: 2026-07-28 (EN)"
date: 2026-07-28
lang: en
---

> From 29 items, 7 important content pieces were selected

---

1. [Moonshot AI Releases Open-Weight 3T Model Kimi-K3](#item-1) ⭐️ 9.0/10
2. [Critical RCE Vulnerability in Fastjson 1.x Without Gadgets](#item-2) ⭐️ 9.0/10
3. [vLLM v0.26.0 Released with New Model Family and DeepSeek-V4 Boost](#item-3) ⭐️ 8.0/10
4. [Bun's Rust Rewrite Progresses, Release Delayed](#item-4) ⭐️ 8.0/10
5. [Chinese DRAM Maker CXMT Soars 471% on STAR Market Debut](#item-5) ⭐️ 8.0/10
6. [Google Teases Gemini 4, Its Most Ambitious Pretraining Yet](#item-6) ⭐️ 8.0/10
7. [SMIC Tests China's First Domestic DUV Lithography Machine](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Moonshot AI Releases Open-Weight 3T Model Kimi-K3](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 9.0/10

Moonshot AI has released Kimi-K3, a 3 trillion parameter mixture-of-experts (MoE) model, on HuggingFace under an open-weight license, accompanied by a detailed technical report. This release provides a rare opportunity for the community to study and fine-tune a model of this scale, with discussions centering on the cost of serving a 3T model, customization potential, and licensing terms that require a separate agreement for large commercial users. The model uses mxfp4 precision natively, requiring approximately 1.5 TB of VRAM for inference, which is at the limit of an 8×B200 setup and likely needs 16×B200 for practical throughput. Initial API pricing shows $3.00/M tokens uncached input, $0.30/M cached input, and $15.00/M output.

hackernews · nateb2022 · Jul 27, 06:18 · [Discussion](https://news.ycombinator.com/item?id=49065752)

**Background**: Kimi-K3 is a mixture-of-experts (MoE) large language model developed by Moonshot AI, a Beijing-based AI company. The model's open-weight release allows developers to download, customize, and fine-tune the model for specific use cases, but the license includes a clause requiring companies with over $20 million annual revenue in aggregate to enter a separate commercial agreement with Moonshot AI.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://kimi-ai.chat/models/kimi-k3/">Kimi K 3 : 1M Context, API Pricing & Limits</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The community is highly engaged, with key discussions focusing on the high cost of serving a 3T model (requiring ~1.5TB VRAM), the customization and IP sovereignty advantages of open weights, and the licensing restrictions that target large commercial entities. A commenter also lamented the lack of prosumer GPUs with sufficient VRAM for such models.

**Tags**: `#AI`, `#Open Weights`, `#Large Language Model`, `#Kimi-K3`, `#HuggingFace`

---

<a id="item-2"></a>
## [Critical RCE Vulnerability in Fastjson 1.x Without Gadgets](https://t.me/zaihuapd/42797) ⭐️ 9.0/10

Security researcher Kirill Firsov disclosed a critical remote code execution vulnerability in Fastjson versions 1.2.68 to 1.2.83 that requires no gadget chain or autoTypeSupport, affecting JDK 8, 17, and 21. This vulnerability is especially dangerous because it bypasses common mitigations and affects multiple JDK versions, with no official patch due to Fastjson 1.x being end-of-life. Users must urgently upgrade to Fastjson 2 or apply workarounds. The vulnerability can be exploited without needing any classpath gadgets or enabling autoType, making it easier to weaponize. Fastjson 1.x has been end-of-life since October 2024, so the only mitigation is upgrading to Fastjson 2 or applying configuration workarounds as suggested by the researcher.

telegram · zaihuapd · Jul 27, 10:31

**Background**: Fastjson is a popular JSON parsing library for Java maintained by Alibaba, widely used in enterprise applications. A 'gadget chain' in Java deserialization refers to a series of classes available on the classpath that can be chained to achieve arbitrary code execution. 'autoTypeSupport' is a feature in Fastjson that allows deserialization of arbitrary classes and is often disabled in secure configurations. This vulnerability is notable because it does not require either, making it more severe and easier to exploit.

<details><summary>References</summary>
<ul>
<li><a href="https://threatbook.io/blog/fastjson-rce-1.2.83-active-exploitation-detected-detection-mitigation">Fastjson RCE ( 1.2.83): Active Exploitation Detected — Detection...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#fastjson`, `#java`, `#rce`

---

<a id="item-3"></a>
## [vLLM v0.26.0 Released with New Model Family and DeepSeek-V4 Boost](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 introduces the Inkling model family with full support including piecewise CUDA graphs and NVFP4 quantization, and delivers significant performance optimizations for DeepSeek-V4 such as a specialized routing kernel and fused_topk_bias. The release also adds fp32 lm_head support, flexible attention backends, and matured KV offloading, with 411 commits from 212 contributors. This release enhances vLLM's support for cutting-edge models like DeepSeek-V4 and the new Inkling family, improving inference efficiency and accuracy for the LLM community. The high contributor engagement reflects the growing importance of optimized inference frameworks in production AI deployments. Inkling model family includes piecewise CUDA graph support, Hopper FA4 relative attention, MTP=1 speculative decoding, LoRA, and standard ModelOpt NVFP4 quantization. DeepSeek-V4 optimizations yield a 2.94% end-to-end TPOT improvement via a specialized routing kernel, plus 1.5–2x kernel speedup from fused_topk_bias. fp32 lm_head with head_dtype improves generation head accuracy, extended to LoRA and ROCm paths.

github · khluu · Jul 27, 01:06

**Background**: vLLM is a high-throughput and memory-efficient inference engine for large language models, widely used in production. DeepSeek-V4 is a Mixture-of-Experts model with 1M context support, and the Inkling family leverages advanced features like Hopper FA4 and NVFP4 quantization to push inference performance. This release builds on vLLM's ongoing efforts to support diverse model architectures and hardware backends.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2603.05451v1">FlashAttention-4: Algorithm and Kernel Pipelining Co-Design for Asymmetric Hardware Scaling</a></li>
<li><a href="https://docs.vllm.ai/projects/vllm-omni/en/latest/user_guide/quantization/modelopt/">ModelOpt - vLLM-Omni</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#model optimization`, `#release`, `#deep learning`

---

<a id="item-4"></a>
## [Bun's Rust Rewrite Progresses, Release Delayed](https://lockwood.dev/ai/2026/07/27/how-is-the-bun-rewrite-in-rust-going.html) ⭐️ 8.0/10

Bun's rewrite from Zig to Rust has shipped in Claude Code, but the next version (1.4) is delayed until a target number of newly passing Node.js compatibility tests is met. This rewrite is significant for Bun's performance and maintainability, and its integration into Claude Code demonstrates real-world deployment. The delay shows a commitment to compatibility over speed. The Rust version was shipped in Claude Code over a month ago. Bun v1.4 release is delayed until a specific number of newly passing Node.js tests is true, with PRs up but not yet merged, likely releasing next Tuesday.

hackernews · tomlockwood · Jul 27, 11:12 · [Discussion](https://news.ycombinator.com/item?id=49067854)

**Background**: Bun is a fast all-in-one JavaScript runtime that bundles, installs, and runs JavaScript & TypeScript. It was originally written in Zig, but a rewrite in Rust was announced to leverage Rust's ecosystem and safety. Claude Code is an AI-powered coding tool by Anthropic that lives in the terminal.

<details><summary>References</summary>
<ul>
<li><a href="https://bun.sh/">Bun — A fast all-in-one JavaScript runtime</a></li>
<li><a href="https://github.com/oven-sh/bun">GitHub - oven-sh/ bun : Incredibly fast JavaScript runtime , bundler...</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**Discussion**: Jarred confirmed progress and delay, emphasizing compatibility. Some commenters noted post-refactor slowdown is expected, while others questioned using an LLM to translate the codebase, suggesting the original Zig issues were fixable.

**Tags**: `#Bun`, `#Rust`, `#rewrite`, `#JavaScript runtime`, `#software engineering`

---

<a id="item-5"></a>
## [Chinese DRAM Maker CXMT Soars 471% on STAR Market Debut](https://www.stcn.com/article/detail/4042119.html) ⭐️ 8.0/10

ChangXin Memory Technologies (CXMT) opened at 49.5 yuan per share on its STAR Market debut on July 27, surging 471.59% from its IPO price of 8.66 yuan. The company raised approximately 57.9 billion yuan, making it the largest IPO on the STAR Market to date. As China's leading DRAM manufacturer, CXMT's successful listing and massive fundraising underscore strong capital market support for domestic semiconductor self-sufficiency. This IPO surpasses SMIC's previous record, signaling the growing importance of memory chips in China's tech ecosystem. If the over-allotment option is fully exercised, total proceeds could reach approximately 66.6 billion yuan. The company expects net profit attributable to parent of 50 to 57 billion yuan for the first half of 2026, reversing a significant loss.

telegram · zaihuapd · Jul 27, 01:29

**Background**: ChangXin Memory Technologies (CXMT) is a major Chinese DRAM producer, focusing on dynamic random-access memory chips used in computers, smartphones, and servers. The STAR Market is China's Nasdaq-style board for tech companies, and CXMT's IPO is a milestone for the domestic memory industry amid US-China tech tensions.

**Tags**: `#半导体`, `#国产替代`, `#IPO`, `#存储芯片`, `#科创板`

---

<a id="item-6"></a>
## [Google Teases Gemini 4, Its Most Ambitious Pretraining Yet](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

Google CEO Sundar Pichai announced during Alphabet’s Q2 2026 earnings call that Gemini 4, its next-generation large model, is currently in training as the company’s most ambitious pretraining project, with a target release in late 2026. This signals Google’s commitment to maintaining frontier AI leadership, as larger pretraining runs are critical for advancing capabilities. The release could significantly impact the AI landscape, potentially setting new benchmarks across reasoning, coding, and multimodal tasks. Pichai emphasized that Google will prioritize compute allocation for frontier AGI research to ensure Gemini 4 remains state-of-the-art upon release. Additionally, the Gemini 3.x Flash series will continue with near-monthly updates, focusing on improvements like intelligent coding.

telegram · zaihuapd · Jul 27, 04:06

**Background**: Pretraining is the initial phase where a large language model is trained on a massive corpus of text (and often multimodal data) to predict the next token, forming the foundation of its knowledge and capabilities. According to recent trends, frontier models are now routinely pretrained on tens of trillions of tokens with multimodal extensions, making each new pretraining run a massive engineering and research undertaking. Google's Gemini 4 pretraining follows this trend, aiming to push the boundaries of scale and performance.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3 .6 Flash — Google DeepMind</a></li>
<li><a href="https://medium.com/@nursena_kok/pre-training-phase-of-large-language-models-the-foundation-of-modern-ai-111b377f0a33">Pre-training Phase of Large Language Models: The Foundation of Modern AI | by Nursena Kok | Medium</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Google`, `#Gemini`, `#large language models`, `#pre-training`

---

<a id="item-7"></a>
## [SMIC Tests China's First Domestic DUV Lithography Machine](https://t.me/zaihuapd/42800) ⭐️ 8.0/10

SMIC is testing China's first domestically developed DUV lithography machine, created by Shanghai startup Yuliangsheng, with an aim to produce 28nm chips and potentially 7nm using multi-patterning, targeting mass production by 2027. This development marks a critical step toward China's semiconductor self-sufficiency, potentially reducing reliance on Dutch company ASML and reshaping global chip supply chains. The machine uses mostly domestic components but still relies on some imported parts. SMIC is also exploring multi-patterning to reach 7nm and even 5nm, though yields may be lower.

telegram · zaihuapd · Jul 27, 14:10

**Background**: DUV lithography uses deep ultraviolet light (193nm or 248nm) to print circuit patterns on silicon wafers. Multiple patterning is a technique that improves resolution beyond the single-exposure limit, commonly used for 10nm and 7nm nodes. Currently, China's most advanced chips rely on ASML's DUV tools, while EUV machines are banned for export to China due to US restrictions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multiple_patterning">Multiple patterning - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Extreme_ultraviolet_lithography">EUV lithography - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#lithography`, `#China`, `#SMIC`, `#DUV`

---