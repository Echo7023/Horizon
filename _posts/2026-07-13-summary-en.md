---
layout: default
title: "Horizon Summary: 2026-07-13 (EN)"
date: 2026-07-13
lang: en
---

> From 29 items, 7 important content pieces were selected

---

1. [GPT-5.6 Sol Ultra Proves 50-Year-Old Graph Conjecture in Under Hour](#item-1) ⭐️ 10.0/10
2. [Grok Build CLI Uploads Entire Repo Including Git History, Analysis Finds](#item-2) ⭐️ 9.0/10
3. [World's First Invasive BCI Medical Device Approved by China's NMPA](#item-3) ⭐️ 9.0/10
4. [vLLM v0.25.0: MRv2 Default, PagedAttention Removed, Faster Backend](#item-4) ⭐️ 8.0/10
5. [Fields Medalist Terry Tao explores LLM coding agents for app building](#item-5) ⭐️ 8.0/10
6. [EU to Fine Big Tech for Consumer Protection Failures](#item-6) ⭐️ 8.0/10
7. [OpenAI releases GPT-5.6 series with Sol, Terra, Luna models](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GPT-5.6 Sol Ultra Proves 50-Year-Old Graph Conjecture in Under Hour](https://www.qbitai.com/2026/07/447873.html) ⭐️ 10.0/10

OpenAI's GPT-5.6 Sol Ultra model has produced a proof of the cycle double cover conjecture, a 50-year-old unsolved problem in graph theory, in less than one hour using 64 parallel sub-agents. This achievement demonstrates AI's capability to solve long-standing mathematical problems autonomously, potentially accelerating discovery in mathematics and other sciences. It also validates the effectiveness of parallel agent architectures and prompt engineering. The proof was generated in under an hour and resulted in a 3-page PDF. OpenAI released the full prompt (about 700 characters) which specifies acceptance criteria, definitions, and constraints rather than step-by-step instructions.

telegram · zaihuapd · Jul 12, 03:49

**Background**: The cycle double cover conjecture asks whether every bridgeless graph (a graph with no edge whose removal disconnects the graph) has a collection of cycles that together cover each edge exactly twice. It was independently posed by Szekeres (1973) and Seymour (1979) and remained unsolved for over 50 years. GPT-5.6 Sol is OpenAI's latest model, released in July 2026, with stronger reasoning and coding capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover_conjecture">Cycle double cover conjecture</a></li>
<li><a href="https://the-decoder.com/openais-gpt-5-6-sol-ultra-reportedly-solves-a-50-year-old-math-problem-in-under-an-hour/">OpenAI's GPT-5.6 Sol Ultra reportedly solves a 50-year-old ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#mathematics`, `#graph theory`, `#GPT-5.6`, `#breakthrough`

---

<a id="item-2"></a>
## [Grok Build CLI Uploads Entire Repo Including Git History, Analysis Finds](https://gist.github.com/cereblab/dc9a40bc26120f4540e4e09b75ffb547) ⭐️ 9.0/10

A wire-level analysis of xAI's Grok Build CLI (version 0.2.93) reveals that the tool uploads the entire repository content and git history to xAI servers with every request, regardless of what the agent actually reads. This raises severe privacy and data security concerns for developers, as sensitive code, secrets accidentally committed, and full project history are exposed to a third-party service, even when not needed. The analysis captured 82 /v1/storage calls, all returning 200 OK, indicating successful upload of every file. The upload includes not just the working directory but also .git history, far exceeding what the agent needs.

hackernews · jhoho · Jul 12, 01:09 · [Discussion](https://news.ycombinator.com/item?id=48877371)

**Background**: Wire-level analysis involves inspecting network traffic at the protocol level to understand exactly what data an application sends to its servers. Grok Build is a command-line coding agent from xAI (SpaceXAI) that integrates AI into development workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://gist.github.com/cereblab/dc9a40bc26120f4540e4e09b75ffb547">What xAI Grok Build CLI actually sends to xAI - a wire-level analysis (grok 0.2.93) · GitHub</a></li>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://docs.x.ai/build/overview">Grok Build | SpaceXAI Docs</a></li>

</ul>
</details>

**Discussion**: Commenters express shock and concern, with many noting they expected better privacy practices. Some suggest sandboxing tools like bubblewrap to restrict file access and network, while others argue developers should never store secrets in their repos.

**Tags**: `#privacy`, `#AI agents`, `#CLI`, `#data security`, `#wire-level analysis`

---

<a id="item-3"></a>
## [World's First Invasive BCI Medical Device Approved by China's NMPA](https://t.me/zaihuapd/42515) ⭐️ 9.0/10

China's National Medical Products Administration (NMPA) has approved the world's first invasive brain-computer interface (BCI) medical device, a hand function compensation system for quadriplegic patients, developed by Beijing NerAcure Technology Co., Ltd. This approval marks the clinical translation of invasive BCI technology, offering a new therapeutic option for quadriplegic patients and setting a regulatory precedent globally. It could significantly improve the quality of life for millions with spinal cord injuries. The device uses epidural minimally invasive implantation and wireless power and data communication, and is indicated for patients aged 18–60 with cervical spinal cord injury. Clinical trials showed improved hand grasp function and quality of life.

telegram · zaihuapd · Jul 12, 14:39

**Background**: Invasive brain-computer interfaces involve surgically implanting electrodes into the brain or epidural space to record neural signals and decode them into commands for external devices. Previously, such technology was primarily in research phases. This approval by the NMPA represents the first regulatory clearance for a clinical-grade invasive BCI medical device worldwide.

<details><summary>References</summary>
<ul>
<li><a href="https://flcube.com/?p=59388">China NMPA Approves World's First Invasive BCI Medical Device...</a></li>
<li><a href="https://www.tsinghua.edu.cn/en/info/1399/12721.htm">Minimally Invasive Brain Computer Interface helps tetraplegia restore...</a></li>

</ul>
</details>

**Tags**: `#brain-computer interface`, `#medical device`, `#regulatory approval`, `#neural prosthetics`, `#clinical translation`

---

<a id="item-4"></a>
## [vLLM v0.25.0: MRv2 Default, PagedAttention Removed, Faster Backend](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 8.0/10

vLLM v0.25.0 makes Model Runner V2 the default execution path for all dense models and removes the legacy PagedAttention implementation. It also achieves Transformers backend parity with native performance, introduces new models like LLaVA-OneVision-2, and adds a Streaming Parser Engine for tool-call/reasoning parsing. This release significantly improves LLM inference performance and maintainability by adopting a modular execution core and removing outdated attention mechanisms. Practitioners can expect faster model serving, easier integration of new architectures, and broader model support. The release includes 558 commits from 232 contributors, with Model Runner V2 now supporting EVS, realtime embeddings, Mamba hybrid prefix caching, and dynamic speculative decoding compatible with full CUDA graphs. The Transformers backend gained FP8 MoE support and migrated several model architectures.

github · khluu · Jul 11, 20:06

**Background**: PagedAttention is an attention algorithm that stores the key-value cache in fixed-size blocks mapped to non-contiguous physical memory, reducing fragmentation and enabling larger batch sizes. Model Runner V2 (MRv2) is a redesigned, modular execution core that simplifies adding new models and features, replacing the monolithic GPU model runner. The removal of PagedAttention indicates that vLLM's newer V1/MRv2 backends have fully superseded the original attention implementation.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PagedAttention">PagedAttention</a></li>
<li><a href="https://zenn.dev/tosshi/articles/f540eb0cad3901">vLLM Model Runner V 2 - モジュラーで高速な推論コアの再設計</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#LLM inference`, `#open source`, `#model serving`, `#AI infrastructure`

---

<a id="item-5"></a>
## [Fields Medalist Terry Tao explores LLM coding agents for app building](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 8.0/10

Terry Tao, a Fields Medalist, shared his experience using LLM-based coding agents to build applications, demonstrating how these tools can accelerate software development beyond traditional methods. This shows that even world-class mathematicians find value in AI-assisted coding, potentially expanding software creation to domain experts who are not professional programmers. It also highlights a 'latent demand' for software outside traditional tech spaces. Tao noted that while LLM-generated code can be complex and sometimes abandoned, it remains useful for non-mission-critical supplements like visualizations. The community discussion emphasizes balanced use and educational benefits.

hackernews · subset · Jul 12, 11:09 · [Discussion](https://news.ycombinator.com/item?id=48880170)

**Background**: LLM coding agents are AI tools that help write code based on natural language prompts. They have become popular for automating code generation, debugging, and refactoring. However, questions about code ownership and reliability persist.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI-assisted_software_development">AI-assisted software development - Wikipedia</a></li>
<li><a href="https://opencode.ai/">OpenCode | The open source AI coding agent</a></li>

</ul>
</details>

**Discussion**: Commenters noted diverse benefits: educators built long-desired visualizations, one joked about Tao facing Docker issues like everyone else, and others highlighted the latent demand for software outside traditional domains. Some urged caution, calling LLM coding a tool with acceptable risks for non-critical tasks.

**Tags**: `#AI-assisted coding`, `#large language models`, `#software development`, `#mathematical applications`

---

<a id="item-6"></a>
## [EU to Fine Big Tech for Consumer Protection Failures](https://www.ft.com/content/25640be5-a5bd-4548-81f9-bd0e16f87f35) ⭐️ 8.0/10

The EU plans to grant itself new enforcement powers to fine large tech companies for failing to protect consumers, especially children, from dark patterns and subscription traps, with proposals expected by the end of this year. This represents a major escalation in EU digital regulation, directly targeting manipulative design practices that have long drawn criticism. It could force major platforms to redesign user interfaces and adjust business models to comply. The new powers would enable cross-border enforcement against systemic violations, covering not only large tech firms but also smaller online merchants and game developers. Current member-state enforcement has never resulted in fines, which the EU commissioner says is insufficient to deter violations.

telegram · zaihuapd · Jul 12, 06:25

**Background**: Dark patterns are user interface designs crafted to trick users into taking actions they did not intend, such as signing up for recurring bills or buying overpriced insurance. The EU has previously enacted broad digital regulations like the Digital Services Act, but consumer protection enforcement has been fragmented and weak.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Dark_pattern">Dark pattern - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#EU regulation`, `#consumer protection`, `#big tech`, `#dark patterns`, `#child safety`

---

<a id="item-7"></a>
## [OpenAI releases GPT-5.6 series with Sol, Terra, Luna models](https://t.me/zaihuapd/42512) ⭐️ 8.0/10

OpenAI announced the GPT-5.6 series, featuring three models—Sol (flagship), Terra (balanced), and Luna (high-concurrency, low-cost)—with improvements in code, research, and cybersecurity, and introduces max/ultra reasoning, multi-agent collaboration, and programmatic tool calling. This release significantly improves performance-cost ratios and expands the range of tasks AI can handle efficiently, from complex reasoning to multi-step tool orchestration, potentially accelerating adoption in enterprise and research settings. The three models are optimized for different scenarios: Sol for maximum capability, Terra for balanced performance and cost, and Luna for high-concurrency low-cost tasks. GPT-5.6 also introduces max/ultra reasoning modes and programmatic tool calling, which reduces token usage and latency for multi-step tasks.

telegram · zaihuapd · Jul 12, 11:19

**Background**: GPT-5.6 is a language model family from OpenAI. The new 'max' and 'ultra' reasoning modes allow the model to allocate more computational resources to difficult problems, improving accuracy. Multi-agent collaboration enables multiple AI agents to work together on complex tasks, while programmatic tool calling lets the model write and execute code to orchestrate tool calls without repeated model round-trips.

<details><summary>References</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/agents-and-tools/tool-use/programmatic-tool-calling">Programmatic tool calling - Claude Platform Docs</a></li>
<li><a href="https://www.u7buy.com/blog/gpt-5-6-reasoning-modes-explained/">GPT-5.6 Reasoning Modes Explained - Medium vs High vs Max vs Ultra</a></li>
<li><a href="https://codersera.com/blog/gpt-5-6-sol-terra-luna/">GPT-5.6 Sol, Terra & Luna: Developer Preview Guide</a></li>

</ul>
</details>

**Tags**: `#GPT-5.6`, `#OpenAI`, `#LLM`, `#AI models`

---