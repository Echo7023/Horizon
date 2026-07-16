---
layout: default
title: "Horizon Summary: 2026-07-17 (EN)"
date: 2026-07-17
lang: en
---

> From 40 items, 13 important content pieces were selected

---

1. [Kimi K3: Open-Weight LLM with 1M Context and Frontier Performance](#item-1) ⭐️ 9.0/10
2. [Rust-to-Zig Compiler Rewrite: Safety vs. Performance](#item-2) ⭐️ 8.0/10
3. [Sony Deletes Movies from 'Purchased' Libraries Again](#item-3) ⭐️ 8.0/10
4. [GPT-5.6 Codex Bug Can Delete $HOME Directory](#item-4) ⭐️ 8.0/10
5. [Thinking Machines Releases Inkling Open-Weights MoE Model](#item-5) ⭐️ 8.0/10
6. [Linus Torvalds Declares Linux Not Anti-AI](#item-6) ⭐️ 8.0/10
7. [xAI open-sources Grok Build after privacy backlash](#item-7) ⭐️ 8.0/10
8. [ExTernD: Expanded-Rank Ternary Decomposition for LLM Quantization](#item-8) ⭐️ 8.0/10
9. [PnP-CoSMo: Plug-and-Play Multi-Contrast MRI Reconstruction without Raw k-Space Data](#item-9) ⭐️ 8.0/10
10. [xAI Sues Grok User for Child Sexual Abuse Deepfakes](#item-10) ⭐️ 8.0/10
11. [CXMT to Match Micron's DRAM Capacity by 2026](#item-11) ⭐️ 8.0/10
12. [Japan buys 27,500 Nvidia Rubin chips for sovereign robot AI](#item-12) ⭐️ 8.0/10
13. [TSMC to invest additional $100B in Arizona, Q2 profit surges 77%](#item-13) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Kimi K3: Open-Weight LLM with 1M Context and Frontier Performance](https://www.kimi.com/en) ⭐️ 9.0/10

Moonshot AI has launched Kimi K3, a new open-weight large language model with a 1-million-token context window, competitive pricing at $3/$15 per million tokens (cached at $0.3), and claims of frontier-level performance second only to Claude Fable 5 and GPT-5.6 Sol. The full model weights will be released by July 27, 2026, along with a technical report. If verified, Kimi K3 represents a major milestone for open-weight LLMs, offering near-frontier performance at competitive pricing, which could democratize access to advanced AI capabilities. Its 1M context window and native vision support make it suitable for complex, long-context tasks, challenging proprietary models like Anthropic's Sonnet series. Kimi K3 is a 2.5-trillion-parameter mixture-of-experts (MoE) model, with pricing matching Anthropic's Sonnet series (1:1), though it is notably expensive for a Chinese open-weight model. The model launches with maximum thinking effort by default, with low/high effort modes planned for future updates; earlier Kimi K3 configurations show up to 1M context on higher-tier plans like Allegretto.

hackernews · vincent_s · Jul 16, 14:46 · [Discussion](https://news.ycombinator.com/item?id=48935342)

**Background**: An open-weight LLM makes its pre-trained parameters publicly available, allowing others to use, modify, or build upon the model. This contrasts with proprietary models like GPT-4, which are only accessible via API. The frontier of large language models has been dominated by closed-source models, but recent open-weight releases like Llama and Qwen have narrowed the gap; Kimi K3 aims to push this further.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/open-weights-llms-in-depth-analysis-adoption-usage-performance-jha-kymhc">Open - Weights LLMs: In-Depth Analysis of Adoption, Usage, and...</a></li>
<li><a href="https://kie.ai/blog/what-is-kimi-k3">What Is Kimi K3? Moonshot's 2.5T, 1M-Context Flagship</a></li>
<li><a href="https://kimi-k2.org/kimi-k3-status">Kimi K3 Status - Release Date, Official Updates and 2026 News</a></li>

</ul>
</details>

**Discussion**: Community comments show high engagement, with users noting the pricing is extremely high for a Chinese open-weight model but justified if performance truly rivals frontier models like Sonnet. Some users tested the model and reported high costs, while others highlighted the upcoming weight release and technical report, expressing cautious optimism.

**Tags**: `#AI`, `#large language models`, `#open-source`, `#context window`, `#benchmarks`

---

<a id="item-2"></a>
## [Rust-to-Zig Compiler Rewrite: Safety vs. Performance](https://rtfeldman.com/rust-to-zig) ⭐️ 8.0/10

Richard Feldman details the decision to rewrite the Roc compiler from Rust to Zig, citing better incremental builds and more control over memory, while acknowledging trade-offs in memory safety. This experiment highlights the practical tensions between safety (Rust) and low-level control (Zig) in systems programming, influencing future language adoption for performance-critical tools like compilers. The rewrite is for the Roc compiler; Zig offers faster incremental builds and precise memory control, but lacks Rust's compile-time safety guarantees, relying instead on runtime checks in ReleaseSafe mode.

hackernews · jorangreef · Jul 16, 11:39 · [Discussion](https://news.ycombinator.com/item?id=48933149)

**Background**: Rust is a systems language known for memory safety without garbage collection through its ownership model, but some tasks like binary patching require unsafe code. Zig is a newer language that prioritizes simplicity and manual memory management, offering runtime safety checks in debug modes but leaving safety to the programmer in release builds.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>
<li><a href="https://doc.rust-lang.org/nomicon/meet-safe-and-unsafe.html">Meet Safe and Unsafe - The Rustonomicon</a></li>
<li><a href="https://ziglang.org/">Home ⚡ Zig Programming Language</a></li>

</ul>
</details>

**Discussion**: The comments include steveklabnik questioning the claim that compilers often need unsafe code, landr0id expressing skepticism about Zig's use-after-free detection, and arthurbrown wondering why OCaml wasn't chosen, while onlyrealcuzzo praises Zig's incremental builds but hopes Rust will add similar features.

**Tags**: `#zig`, `#rust`, `#compilers`, `#systems-programming`, `#memory-safety`

---

<a id="item-3"></a>
## [Sony Deletes Movies from 'Purchased' Libraries Again](https://www.techdirt.com/2026/07/15/sony-deletes-a-bunch-more-movies-from-the-accounts-of-people-who-bought-them/) ⭐️ 8.0/10

Sony has deleted several movies from users' PlayStation Store libraries that customers had previously paid for, reigniting controversy over digital ownership. This marks another instance of the company revoking access to content after purchase. This ongoing practice undermines the concept of digital ownership and highlights the need for stronger consumer protection laws regarding digital purchases. It affects millions of PlayStation users and erodes trust in digital storefronts. The deletions are made possible through digital rights management (DRM) technology, which gives publishers ongoing control over content even after a sale. Users do not truly own digital media but instead hold a revocable license.

hackernews · nekusar · Jul 16, 12:13 · [Discussion](https://news.ycombinator.com/item?id=48933419)

**Background**: Digital rights management (DRM) combines encryption, licensing, and device authentication to control how content is accessed and shared. When users 'buy' digital movies, they are actually purchasing a limited license, not the content itself. This allows companies like Sony to revoke access if licensing agreements change or for other business reasons.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_rights_management">Digital rights management - Wikipedia</a></li>
<li><a href="https://www.fortinet.com/resources/cyberglossary/digital-rights-management-drm">What Is DRM? Digital Rights Management Explained | Fortinet</a></li>

</ul>
</details>

**Discussion**: Commenters expressed frustration, with some calling for legal action against the misleading 'Buy' button. Others noted that this is a recurring issue and advocated for offline physical media or piracy as alternatives. A few users speculated that the console era might be ending as gamers migrate to PC.

**Tags**: `#digital rights`, `#consumer protection`, `#Sony`, `#digital media`, `#ownership`

---

<a id="item-4"></a>
## [GPT-5.6 Codex Bug Can Delete $HOME Directory](https://simonwillison.net/2026/Jul/16/bad-codex-bug/#atom-everything) ⭐️ 8.0/10

A bug in GPT-5.6 Codex can accidentally delete the user's $HOME directory when full access mode is enabled without sandboxing protections or auto-review, as confirmed by Thibault Sottiaux on July 16, 2026. This bug highlights critical safety risks in AI coding agents, potentially causing irreversible data loss for developers who trust these tools with full system access. It underscores the need for robust sandboxing and review mechanisms in AI-assisted development. The bug occurs when full access mode is enabled and Codex runs without sandboxing or auto-review; the model attempts to override the $HOME environment variable to define a temporary directory, but mistakenly deletes $HOME instead.

rss · Simon Willison · Jul 16, 17:45

**Background**: AI coding agents like Codex often require filesystem access to write code and manage files. Sandboxing isolates the agent's environment to prevent harm to the host system, while full access mode grants unrestricted permissions. Without these protections, a model error can lead to destructive actions like deleting critical directories.

<details><summary>References</summary>
<ul>
<li><a href="https://www.explainx.ai/blog/openai-codex-gpt-5-6-home-deletion-full-access-july-2026">Codex GPT-5.6 $HOME Deletion — Full Access | explainx.ai Blog</a></li>
<li><a href="https://www.bunnyshell.com/guides/sandboxed-environments-ai-coding/">Sandboxed Environments for AI Coding: The Complete Guide | Bunnyshell</a></li>

</ul>
</details>

**Tags**: `#codex`, `#gpt-5`, `#ai-safety`, `#coding-agents`, `#generative-ai`

---

<a id="item-5"></a>
## [Thinking Machines Releases Inkling Open-Weights MoE Model](https://simonwillison.net/2026/Jul/16/inkling/#atom-everything) ⭐️ 8.0/10

Thinking Machines Lab, led by former OpenAI CTO Mira Murati, released Inkling, an open-weights Mixture-of-Experts multimodal model with 975B total parameters (41B active) under the Apache 2.0 license. This release adds a strong US-based contender to the open-weights ecosystem, offering a competitive alternative to Chinese open models and NVIDIA's Nemotron. Its Apache 2.0 license and focus on fine-tuning via Tinker platform make it suitable for customization. Inkling is not a frontier model but a strong base model for fine-tuning, trained on 45 trillion tokens of text, images, audio, and video. A smaller Inkling-Small (276B total, 12B active) is promised but not yet released.

rss · Simon Willison · Jul 16, 15:35

**Background**: Mixture-of-Experts (MoE) is an architecture that uses multiple specialized submodels ('experts') and a gating network to activate only relevant experts per input, improving efficiency. Open-weights models release the trained parameters publicly, allowing download, study, and modification, but do not include full training code or data.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**Tags**: `#open-weights`, `#multimodal`, `#Mixture-of-Experts`, `#AI model release`

---

<a id="item-6"></a>
## [Linus Torvalds Declares Linux Not Anti-AI](https://simonwillison.net/2026/Jul/16/linus-torvalds/#atom-everything) ⭐️ 8.0/10

Linus Torvalds, the creator and top maintainer of Linux, stated on the Linux Media mailing list that Linux is not an anti-AI project and that AI is a clearly useful tool, challenging any opposition within the community. This high-profile endorsement from Linux's leader signals official acceptance of AI in kernel development, potentially influencing industry practices and encouraging broader adoption of AI tools in open-source projects. Torvalds acknowledged that AI's usefulness was questionable a year ago but is no longer in doubt today, though he noted unresolved questions about its economic impact.

rss · Simon Willison · Jul 16, 13:26

**Background**: Linus Torvalds is the creator and lead maintainer of the Linux kernel, one of the world's largest open-source projects. His statements carry significant weight in the developer community. The debate over AI's role in software development has been growing, with some projects adopting strict anti-AI policies.

**Tags**: `#Linux`, `#AI`, `#Kernel Development`, `#Linus Torvalds`

---

<a id="item-7"></a>
## [xAI open-sources Grok Build after privacy backlash](https://simonwillison.net/2026/Jul/15/grok-build/#atom-everything) ⭐️ 8.0/10

Following a severe privacy incident where the grok CLI tool uploaded entire directories to xAI servers, xAI has open-sourced the entire Grok Build codebase under the Apache 2.0 license. The company also disabled default data retention and deleted all previously retained coding data. This move aims to restore user trust by providing complete transparency into how the tool operates, allowing users to audit or run it locally. It sets a precedent for AI coding tools to be more open about their data handling practices. The codebase contains 844,530 lines of Rust (only ~3% vendored) and was released in a single commit, providing no commit history. Notable components include a Mermaid diagram renderer in the terminal and tool implementations mimicking other coding agents like Codex and OpenCode.

rss · Simon Willison · Jul 15, 23:59

**Background**: The grok CLI is a terminal-based AI coding agent by xAI that can edit files, run commands, and manage tasks. Earlier, users discovered that running the CLI in a directory would upload the entire directory to xAI's Google Cloud buckets, leading to a privacy outcry. In response, xAI disabled the upload feature, deleted retained data, and released the code as open source.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/xai-org/grok-build">GitHub - xai-org/grok-build: SpaceXAI's coding agent harness ...</a></li>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://github.com/Norlem/grok-cli">GitHub - Norlem/ grok - cli : A terminal UI for xAI 's Grok models...</a></li>

</ul>
</details>

**Discussion**: Community sentiment was highly negative initially, with users reporting sensitive data like SSH keys and password managers being uploaded. After the open-source release, reactions were mixed — some appreciated the transparency, while others remained skeptical about past data handling.

**Tags**: `#open source`, `#security`, `#AI`, `#xAI`, `#privacy`

---

<a id="item-8"></a>
## [ExTernD: Expanded-Rank Ternary Decomposition for LLM Quantization](https://www.reddit.com/r/MachineLearning/comments/1uy2zb3/externd_expandedrank_ternary_decomposition/) ⭐️ 8.0/10

A new post-training quantization method called ExTernD decomposes LLM weight matrices into two ternary matrices and a diagonal scaling matrix, allowing arbitrary accuracy by expanding the inner rank. This technique bridges the accuracy gap between low-bit ternary quantization and higher-bit methods, enabling efficient LLM deployment with minimal loss in model quality and only slightly increased VRAM usage. ExTernD factorizes each weight matrix as A ≈ D1 * T1 * D2 * T2, where T1 and T2 are ternary matrices and D1, D2 are diagonal scaling matrices, providing continuous control over memory and compute trade-offs.

reddit · r/MachineLearning · /u/LMTLS5 · Jul 16, 13:31

**Background**: Large language models are often quantized to reduce memory and computational costs. Ternary quantization restricts weights to values in {-1, 0, +1}, which is extremely efficient but often suffers from significant accuracy loss. Post-training quantization (PTQ) applies quantization after training without retraining. Fixed-rank ternary decomposition has been a dead end because it cannot represent full-precision matrices accurately; ExTernD overcomes this by expanding the decomposition rank.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2607.13511v1">ExTernD: Expanded-Rank Ternary Decomposition Ternary LLM PTQ ...</a></li>
<li><a href="https://papers.cool/arxiv/2607.13511">ExTernD: Expanded-Rank Ternary Decomposition Ternary LLM PTQ ...</a></li>
<li><a href="https://aipapers.ai/paper/26889608">ExTernD: Expanded-Rank Ternary Decomposition Ternary LLM PTQ ...</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#quantization`, `#ternary decomposition`, `#post-training quantization`, `#model efficiency`

---

<a id="item-9"></a>
## [PnP-CoSMo: Plug-and-Play Multi-Contrast MRI Reconstruction without Raw k-Space Data](https://www.reddit.com/r/MachineLearning/comments/1uy2h66/pnpcosmo_a_multicontrast_mri_reconstruction/) ⭐️ 8.0/10

Researchers have proposed PnP-CoSMo, a plug-and-play framework for multi-contrast MRI reconstruction that learns a content/style model from purely image-domain data and applies it as a prior in iterative reconstruction, requiring no raw k-space training data. This framework addresses a major data bottleneck in machine learning-based MRI reconstruction by eliminating the need for raw k-space data, which is difficult to obtain. It also generalizes across different MR contrasts and forward operators, potentially enabling more flexible and accessible reconstruction in clinical settings. PnP-CoSMo consists of two stages: first, it learns a content/style model from image-domain data; second, it freezes the model and uses it as a plug-and-play prior within an iterative reconstruction algorithm. The method is validated on the public NYU fastMRI DICOM dataset and shows equivalent or superior quality compared to end-to-end methods.

reddit · r/MachineLearning · /u/void_gear · Jul 16, 13:10

**Background**: Multi-contrast MRI acquires images with different contrast mechanisms (e.g., T1-weighted, T2-weighted) to highlight various tissue properties. Machine learning methods for MRI reconstruction typically require raw k-space data, which is not always available. Plug-and-play priors combine denoisers with iterative reconstruction, but often need separate training for each contrast. Content/style modeling separates images into shared content (anatomical structure) and contrast-specific style, enabling cross-contrast learning.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sciencedirect.com/science/article/pii/S136184152600229X">A plug-and-play method for guided multi-contrast MRI ...</a></li>
<li><a href="https://arxiv.org/html/2409.13477v3">A Plug-and-Play Method for Guided Multi-contrast MRI ...</a></li>
<li><a href="https://github.com/cnmy-ro/pnp-cosmo">GitHub - cnmy-ro/pnp-cosmo: PnP-CoSMo algorithm for multi ...</a></li>

</ul>
</details>

**Tags**: `#MRI reconstruction`, `#machine learning`, `#medical imaging`, `#plug-and-play`, `#content/style model`

---

<a id="item-10"></a>
## [xAI Sues Grok User for Child Sexual Abuse Deepfakes](https://www.reuters.com/legal/litigation/musks-xai-sues-grok-user-over-sexualized-deepfakes-2026-07-15/) ⭐️ 8.0/10

Elon Musk's xAI has filed a lawsuit against South Carolina man Terry Harwood for using the Grok chatbot to generate child sexual abuse material and non-consensual adult deepfakes, violating the platform's terms of service. This is one of the first lawsuits by an AI company against a user for generating illegal deepfake content, setting a precedent for AI platform liability and highlighting critical ethical and legal issues in AI governance. xAI has requested a permanent injunction barring Harwood from using Grok, and seeks damages. The company reported that in 2026 it suspended 52,222 accounts, made 73,604 reports to the National Center for Missing & Exploited Children, and facilitated at least 244 arrests.

telegram · zaihuapd · Jul 16, 01:45

**Background**: Grok is a generative AI chatbot developed by xAI, launched in November 2023. Deepfakes are synthetic media created using AI, often used to depict real people in fake scenarios. This lawsuit addresses the misuse of AI tools to generate illegal content, a growing concern in the AI industry.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_(chatbot)">Grok ( chatbot ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Deepfake">Deepfake - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI ethics`, `#legal`, `#Grok`, `#deepfake`, `#child safety`

---

<a id="item-11"></a>
## [CXMT to Match Micron's DRAM Capacity by 2026](https://www.tomshardware.com/pc-components/dram/cxmt-close-to-matching-microns-memory-capacity-in-2026-research-claims-would-put-china-on-track-to-become-worlds-second-largest-dram-producer) ⭐️ 8.0/10

Chinese DRAM maker CXMT is projected to reach 350,000 wafers per month by the end of 2026, matching Micron's 375,000 wafers per month, according to Citrini Research. This expansion could make China the world's second-largest DRAM producer, challenging the dominance of Samsung and SK Hynix, and may reshape global memory supply chains amid geopolitical tensions. Chinese total DRAM capacity could exceed 600,000 wafers per month when including other firms like Nexchip and Jinhua, but the US MATCH Act may restrict exports of immersion DUV lithography equipment vital for scaling production.

telegram · zaihuapd · Jul 16, 02:30

**Background**: DRAM is a volatile memory widely used in computers and servers. Advanced immersion DUV lithography, which uses water between the lens and wafer to improve resolution, is critical for manufacturing high-density DRAM. The US MATCH Act of 2026 aims to restrict exports of such semiconductor manufacturing equipment to China to limit its technological progress.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography - Wikipedia</a></li>
<li><a href="https://informedclearly.com/en/trade-war/52262/match-act-chip-export-controls-us-china-2026">MATCH Act: 2026's Toughest Chip Export Controls Reshape US ...</a></li>
<li><a href="https://www.govtrack.us/congress/bills/119/hr8170">H.R. 8170: MATCH Act - GovTrack.us</a></li>

</ul>
</details>

**Tags**: `#DRAM`, `#semiconductor`, `#China`, `#memory`, `#supply chain`

---

<a id="item-12"></a>
## [Japan buys 27,500 Nvidia Rubin chips for sovereign robot AI](https://www.bloomberg.com/news/articles/2026-07-16/japan-to-buy-nvidia-rubin-chips-to-build-sovereign-ai-for-robots) ⭐️ 8.0/10

Japan plans to purchase 27,500 Nvidia Rubin chips led by new company Noetra to build a large data center and develop a domestic AI foundation model for robotics, with a government grant of 387.3 billion yen ($24 billion). This marks a major government-backed investment in sovereign AI infrastructure, aiming to reduce reliance on US and Chinese technology and capture over 30% of the global robotics market by 2040. It signals a strategic push for AI autonomy and competitiveness. The project involves SoftBank, Toyota-backed Preferred Networks, and NEC. Noetra president Hiroshi Tabata aims to release the first AI model by March 2027 and a robot-specific version within a few years.

telegram · zaihuapd · Jul 16, 10:59

**Background**: Sovereign AI refers to national efforts to independently develop, deploy, and govern AI using local infrastructure, data, and models, reducing dependence on foreign providers. Nvidia Rubin is the next-generation AI chip architecture after Blackwell, unveiled at CES 2026, offering significant improvements in computational power and efficiency. Japan's initiative reflects a global trend where countries seek to build their own AI capabilities, especially in critical sectors like robotics.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sovereign_AI">Sovereign AI</a></li>
<li><a href="https://www.mckinsey.com/featured-insights/mckinsey-explainers/what-is-sovereign-ai">What is sovereign AI? | McKinsey</a></li>
<li><a href="https://www.linkedin.com/posts/theodoreaggelopoulos_nvidia-launches-powerful-new-rubin-chip-architecture-activity-7414286177656119296-o6T0">Nvidia launches powerful new Rubin chip architecture | TechCrunch</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#Nvidia`, `#robotics`, `#sovereign AI`, `#Japan`

---

<a id="item-13"></a>
## [TSMC to invest additional $100B in Arizona, Q2 profit surges 77%](https://www.reuters.com/world/asia-pacific/tsmcs-second-quarter-profit-seen-hitting-record-ai-boom-2026-07-15/) ⭐️ 8.0/10

TSMC announced an additional $100 billion investment in Arizona factories and reported a record Q2 net profit of T$706.6 billion, up 77% year-over-year, far exceeding market expectations. This expansion solidifies TSMC's commitment to US chip manufacturing amid rising AI demand, potentially reshaping the global semiconductor supply chain and reducing reliance on Taiwan. The new $100 billion is on top of the previously announced $165 billion, bringing TSMC's total planned US investment to $265 billion, with eight factories already under construction or planned in Arizona.

telegram · zaihuapd · Jul 16, 12:29

**Background**: TSMC is the world's largest dedicated semiconductor foundry, producing chips for companies like Apple, NVIDIA, and AMD. The US government has been pushing to onshore advanced chip manufacturing through the CHIPS Act to secure supply chains.

**Tags**: `#semiconductors`, `#AI`, `#manufacturing`, `#TSMC`, `#business`

---