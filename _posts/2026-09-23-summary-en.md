---
layout: default
title: "Horizon Summary: 2026-09-23 (EN)"
date: 2026-09-23
lang: en
---

> From 39 items, 25 important content pieces were selected

---

1. [OpenAI launches GPT-6 Sol and Luna, halving API token prices](#item-1) ⭐️ 9.0/10
2. [Anthropic Launches Claude Opus 5.5 With Lower Token Pricing](#item-2) ⭐️ 9.0/10
3. [Pentagon: AI overreliance contributed to deadly missile strike on Iranian school](#item-3) ⭐️ 9.0/10
4. [vLLM v0.30.0 ships Fast Start IPC weight caching and many new model integrations](#item-4) ⭐️ 8.0/10
5. [Claude Opus 5.5 Benchmark Analysis: Cost Gains vs. Reliability Concerns](#item-5) ⭐️ 8.0/10
6. [25 Fields Medalists Warn AI May Misalign with Math Research Goals](#item-6) ⭐️ 8.0/10
7. [OpenAI Begins Limited Preview of GPT-5.6 Family: Sol, Terra, Luna](#item-7) ⭐️ 8.0/10
8. [Apple adds persistent ads to iOS, frustrating users](#item-8) ⭐️ 7.0/10
9. [TypeSafe AI's Jev outputs typed probabilistic decisions instead of text](#item-9) ⭐️ 7.0/10
10. [Cloudflare Python Workers reach general availability after two-year preview](#item-10) ⭐️ 7.0/10
11. [Xiaomi releases MiMo-V2.6 omni-modal model with $3.5M RL training cost](#item-11) ⭐️ 7.0/10
12. [Complex KDA: Extending Kimi Delta Attention's Expressivity](#item-12) ⭐️ 7.0/10
13. [Qonto releases QontoFAQ retrieval benchmark and relevance metric](#item-13) ⭐️ 7.0/10
14. [Douyin Launches Wealth Management Section With Funds and Brokerage Accounts](#item-14) ⭐️ 7.0/10
15. [Alibaba Unveils Zhenwu V900 AI Chip, Claiming 3x Compute Over M890](#item-15) ⭐️ 7.0/10
16. [DeepSeek Releases DSec Sandbox Platform Report: 3M Sandboxes Daily for Agent Training](#item-16) ⭐️ 7.0/10
17. [Mimo CLI alleged to collect repo metadata and package source code](#item-17) ⭐️ 7.0/10
18. [China Probes DeepSeek and Moonshot Over Data Leak Claims](#item-18) ⭐️ 7.0/10
19. [DeepSeek to Brief UN Security Council on AI Risks This Week](#item-19) ⭐️ 7.0/10
20. [Reported GPT-6 'Astra' breaks Enigma message unsolved since 2005, sparking debate](#item-20) ⭐️ 6.0/10
21. [GrapheneOS hints at preinstalled devices shipping as early as 2027](#item-21) ⭐️ 6.0/10
22. [LinearSolveBench: new benchmark for AI-written sparse linear solvers in C](#item-22) ⭐️ 6.0/10
23. [Templar simulates stage-skipping fault tolerance for pipeline-parallel pre-training](#item-23) ⭐️ 6.0/10
24. [US Proposes AI Incident Notification Channel With China](#item-24) ⭐️ 6.0/10
25. [iOS 27.2 Beta 2 Adds China-Only Motion Data Restriction](#item-25) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [OpenAI launches GPT-6 Sol and Luna, halving API token prices](https://openai.com/index/introducing-gpt-6-sol-and-luna/) ⭐️ 9.0/10

OpenAI announced the GPT-6 model family, GPT-6 Sol and GPT-6 Luna, available starting today in ChatGPT Work and Codex for all Plus, Pro, Business, Enterprise, and Edu users, with Free and Go users getting GPT-6 Luna in the desktop app (the models are not yet in Chat). They ship in the API as gpt-6-sol and gpt-6-luna, with Sol aimed at complex coding and agentic workflows and Luna positioned as the most efficient model for focused, high-volume tasks. OpenAI cut token prices by half or more versus the 5.6 generation, which directly changes the cost-per-task economics for developers running long agentic coding loops, and the company attributes the drop to improvements in caching and inference. With Sol priced at $2/$10 per million input/output tokens against Claude Opus 5.5's much higher rates, the release intensifies price competition among frontier model providers even as it slightly trails its own predecessor on top-end coding benchmarks. GPT-6 Sol costs $2/$10 per million input/output tokens versus $4/$20 for GPT-5.6 Sol, while GPT-6 Luna is 50% cheaper on input and 58.3% cheaper on output than GPT-5.6 Luna (which was $0.20/$1.20). The trade-off is real: Sol gives up roughly 4 points of top-end DeepSWE performance compared with GPT-5.6 Sol in exchange for a 58% lower cost per task, and on OpenAI's internal factuality evaluation it makes about half as many mistakes as its predecessor, reaching Astra-level reliability at much lower cost.

hackernews · OfficialTurkey · Sep 22, 18:00 · [Discussion](https://news.ycombinator.com/item?id=49805509)

**Background**: Large language model providers typically sell access per million tokens, split into input (what you send) and output (what the model generates), and output tokens are usually several times more expensive. "Sol" and "Luna" are the two tiers of OpenAI's 6-series family: a larger, more capable model for demanding coding and agent work, and a cheaper, faster one for high-volume tasks. Codex and ChatGPT Work are OpenAI's developer- and enterprise-oriented surfaces, where agentic coding — models autonomously editing files, running tests and iterating — has made inference cost a first-order concern. OpenAI also reported a prompt-injection safety result: on a simulated message board seeded with unauthorized instructions, Sol complied in 11.3% of runs where it found the board, down from 51.9% for the prior generation.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-sol-and-luna/">Introducing GPT-6 Sol and Luna | OpenAI</a></li>
<li><a href="https://techcrunch.com/2026/09/22/openai-launches-gpt-6-sol-and-luna/">OpenAI launches GPT-6 Sol and Luna, boasting lower cost and fewer mistakes | TechCrunch</a></li>
<li><a href="https://venturebeat.com/technology/openai-releases-gpt-6-sol-and-luna-models-slashing-api-costs-50-or-more">OpenAI releases GPT-6 Sol and Luna models, slashing API costs 50% or more | VentureBeat</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters focused heavily on pricing: simonw called GPT-6 Luna costing half as much as GPT-5.6 Luna "a really big deal" and posted side-by-side SVG pelican generations for Sol, Luna and Astra, while pookieinc argued Claude's Opus pricing now looks uncompetitive next to what OpenAI is shipping. jeffnash said the deciding factor between Claude Code 20x and Codex Pro 20x is usage limits and reset windows, with Codex winning by a mile, and m_fayer expressed a more sentimental concern — attachment to 5.6 Sol's communication style and engineering instincts, and worry that a technically better successor won't feel as natural to work with.

**Tags**: `#OpenAI`, `#GPT-6`, `#LLM`, `#AI models`, `#pricing`

---

<a id="item-2"></a>
## [Anthropic Launches Claude Opus 5.5 With Lower Token Pricing](https://www.anthropic.com/claude-opus-5-5) ⭐️ 9.0/10

Anthropic announced Claude Opus 5.5, a new frontier model that cuts API token prices across the board compared with Opus 5: cache reads drop from $0.50 to $0.20, input tokens from $5 to $4, output tokens from $25 to $20, and cache writes from $6.25 to $5 per 1M tokens. Anthropic also says Opus 5.5 communicates more naturally than prior models, putting the most important information up front for better long-session collaboration. The price cut lands on what may be the highest-spend model in the world on OpenRouter, so cheaper Opus tokens directly lower costs for heavy agentic and coding workloads and intensify price competition with cheap-but-capable rivals such as DeepSeek. It also matters symbolically: Anthropic frames the release as its first since publicly calling for the industry to "pace the frontier," a tension the community immediately pounced on. The release note's opening line is "Claude Opus 5.5 is our first release since we called for pacing the frontier," and Anthropic's stated communication improvements were validated by early testers who said "it writes the way I do." Commenters noted Opus 5 leads OpenRouter's task-spend rankings, suggesting real-world spending, not just benchmark scores, is the battleground here.

hackernews · km144 · Sep 22, 16:29 · [Discussion](https://news.ycombinator.com/item?id=49803892)

**Background**: A "frontier model" is one of the most advanced AI models available at a given moment, trained on massive datasets and enormous compute to deliver state-of-the-art results across many tasks. Because these models are billed per token — with separate rates for input, output, and cached context, and cache reads typically far cheaper than fresh input — even small per-token reductions translate into large savings at scale. "Pacing the frontier" refers to the argument, advanced by Anthropic CEO Dario Amodei in a September 2026 essay titled "We Must Pace the Frontier," that the industry should deliberately moderate how fast it develops the most capable systems.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>
<li><a href="https://www.pacingthefrontier.com/">Pacing the Frontier</a></li>

</ul>
</details>

**Discussion**: The 662-comment Hacker News thread was dominated by two themes: relief at the price drop, and skepticism toward Anthropic's framing. The top-style critique was that the release invokes "pacing the frontier" in its first line while the rest of the post demonstrates with very specific numbers that Anthropic is doing the opposite; other commenters said they were happily sticking with much cheaper alternatives like DeepSeek v4.1, and some joked about the obligatory pelican benchmark images.

**Tags**: `#AI`, `#LLM`, `#Anthropic`, `#Claude`, `#Pricing`

---

<a id="item-3"></a>
## [Pentagon: AI overreliance contributed to deadly missile strike on Iranian school](https://www.bloomberg.com/graphics/2026-iran-school-attack/) ⭐️ 9.0/10

A Pentagon report concludes that the U.S. "failed in its obligation to do everything feasible to verify" that a school in Minab, Iran was a military objective, and that the failure "went beyond mere negligence," attributing the deadly strike in part to overreliance on AI targeting tools such as Project Maven. According to the report, the Minab site was cataloged as an Islamic Revolutionary Guard Corps facility based on outdated data, fed into Maven alongside other candidates, and came out as a recommended day-one target. This is one of the first official findings to tie a lethal civilian-casualty incident directly to AI-assisted targeting, undercutting the assumption that keeping a human "in the loop" is sufficient to satisfy legal and ethical obligations in war. It is likely to intensify scrutiny of military AI vendors, the pace of AI-driven kill chains, and international efforts to regulate autonomous weapons. The report notes that target-list work which once took hours was condensed into minutes, and that some users expected Maven to flag stale records or contradictions in the assembled intelligence — though officials said it is unclear why they believed the system would do that. The Pentagon and Palantir appear to be trading blame, with one side pointing to the software and the other to bad input data, and the site's mislabeling stemmed from an outdated catalog entry.

hackernews · devonnull · Sep 22, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49806430)

**Background**: Project Maven (the Maven Smart System) is a U.S. Department of Defense AI decision-support program that ingests intelligence and helps analysts and operators assemble and rank potential targets; such tools are sometimes called AI decision-support systems (AI-DSS). In the standard "human-in-the-loop" model, a human must authorize any strike, which governments argue preserves legal accountability under international humanitarian law, whose rules require distinguishing civilian from military objects and taking feasible precautions. Critics counter that as AI accelerates the targeting cycle from days to minutes, humans may rubber-stamp machine recommendations rather than genuinely verify them, an issue also debated globally under the rubric of lethal autonomous weapons systems (LAWS).

<details><summary>References</summary>
<ul>
<li><a href="https://onthewire.ai/article/human-in-the-loop-or-loophole">Human in the loop , or loophole? The phrase holding up the AI -war...</a></li>
<li><a href="https://opiniojuris.org/2026/04/13/beyond-anthropics-red-line-human-in-the-loop-and-the-illusion-of-legitimacy-in-ai-decision-support-systems/">Beyond Anthropic’s Red Line: Human - in - the - Loop and... - Opinio Juris</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lethal_autonomous_weapon">Lethal autonomous weapon - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters largely resisted framing AI as the culprit, arguing that outdated data and human decisions to delegate authority are the real root causes — "AI can't be tried in a court," so a responsible human must be accountable for every action. Several criticized optimizing the wrong metric (speed of target-list generation) and the apparent blame-shifting between the Pentagon and Palantir, while others noted that users who don't understand AI's blind spots should never have embraced it wholeheartedly.

**Tags**: `#AI Ethics`, `#Military AI`, `#AI Accountability`, `#Autonomous Systems`, `#AI Limitations`

---

<a id="item-4"></a>
## [vLLM v0.30.0 ships Fast Start IPC weight caching and many new model integrations](https://github.com/vllm-project/vllm/releases/tag/v0.30.0) ⭐️ 8.0/10

vLLM released v0.30.0, a major release containing 762 commits from 315 contributors (104 of them new), which adds support for a long list of new models including DeepSeek-V4.1-Flash, DeepSeek-V4-Flash-Vision-Exp, GLM-5.3-Flash, K2-Horizon, Cohere Compass, Bailing V3 VL and Nanbeige4.2. The headline infrastructure change is "Fast Start," a persistent per-GPU weight-cache daemon that keeps post-quantized, tensor-parallel-sharded weights resident in GPU memory so engines restart by mapping them over CUDA IPC via `--load-format ipc_cache` instead of reloading from disk, now extended to FP4 checkpoints and multi-node TP. vLLM is one of the most widely deployed open-source LLM inference and serving engines, so its releases directly shape the cost and latency profile of self-hosted AI infrastructure. Fast Start targets a real pain point — long engine restart times that slow down reinforcement-learning rollouts, autoscaling and cluster reconfiguration — while the broad model coverage helps keep vLLM as the default serving layer for newly published open-weight models. Beyond the new models, the release adds Gumbel-max watermarking for generated text with per-request opt-out (dual-key so it also works with speculative decoding), "HiSparse" — a host-resident tier for sparse-MLA decoding that spills KV pages to pinned host memory under GPU pressure and serves top-k misses from a per-request GPU hot buffer via `HiSparseConnector` — and many Model Runner V2 gains, including freezing garbage collection during CUDA graph capture that cut capture time from 12s to 2s and engine init from 28.9s to 8.2s on an H200. Performance work on Qwen3.8-Flash-Next and Kimi K3 is also extensive, with reported gains such as a 4-6x kernel speedup from grouped FP8 MLA cache insertion and a 12-81% speedup for DSV3 low-latency GEMM on strided tensors.

github · khluu · Sep 22, 05:20

**Background**: vLLM is an open-source inference and serving engine for large language models, known for memory-efficient KV-cache management and high-throughput batching. Releases like this bundle contributions from the community with low-level GPU kernel work: MXFP8 is a microscaling block floating-point format that shares one exponent across a block of 8-bit values to save memory, FlashMLA is a Multi-Latent-Attention decoding kernel optimized for NVIDIA GPUs, and DeepGEMM is DeepSeek's high-performance FP8/FP4/BF16 GEMM kernel library used in large model training and inference. Weight loading and engine startup are often dominated by reading and re-quantizing multi-gigabyte checkpoints, which is exactly what the new IPC weight cache aims to avoid.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MXFP8">MXFP8</a></li>
<li><a href="https://github.com/deepseek-ai/DeepGEMM">GitHub - deepseek-ai/ DeepGEMM : DeepGEMM : clean and efficient...</a></li>
<li><a href="https://www.deepep.org/en/flashmla">FlashMLA</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#model serving`, `#AI infrastructure`, `#release`

---

<a id="item-5"></a>
## [Claude Opus 5.5 Benchmark Analysis: Cost Gains vs. Reliability Concerns](https://artificialanalysis.ai/models/claude-opus-5-5) ⭐️ 8.0/10

Artificial Analysis published a dedicated evaluation page for Anthropic's Claude Opus 5.5 at its "max" reasoning setting, benchmarking the model across intelligence, output speed/latency, and price. A companion page exists for the "xhigh" setting, while the "medium" setting is the model's default. These independent benchmarks are widely used by developers and teams choosing which model to route production workloads to, so the reported halving of cost per task versus Opus 5 could directly shift buying decisions toward Anthropic's newest flagship. The accompanying Hacker News thread also highlights a broader industry worry: that early benchmark results may not hold up weeks after launch. Commenters note the "max" setting is not the default, and at least one user reported that a simple prompt ("Generate an SVG of a pelican riding a bicycle") failed twice because the model exhausted its 128,000-token budget while still reasoning. On the cost side, one commenter cites roughly half the cost per task compared with Opus 5 when comparing high-effort to high-effort settings.

hackernews · theanonymousone · Sep 22, 16:51 · [Discussion](https://news.ycombinator.com/item?id=49804316)

**Background**: Artificial Analysis is an independent benchmarking site that aggregates evaluations across mathematics, science, coding, and reasoning to produce comparable intelligence, speed, latency, and price metrics for AI models and API providers. Modern reasoning models such as Claude Opus expose adjustable "reasoning effort" settings (for example medium, xhigh, and max) that trade more internal thinking tokens for higher accuracy. Because higher effort consumes more tokens, both the token budget and the per-task price become practical constraints developers must weigh.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models">Comparison of AI Models across Intelligence, Performance, and Price | Artificial Analysis</a></li>
<li><a href="https://artificialanalysis.ai/evaluations">AI Model Evaluations | Artificial Analysis</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion is largely practical rather than celebratory: simonw reported the max setting burning through 128,000 tokens without completing a simple SVG task, breckenedge questioned whether benchmarks are re-run weeks after launch and claimed an internal re-test showed a model regressing, and linuxrebe1 said they had reverted to Opus 4.8 because it followed instructions and stayed on task better than Opus 5. On the positive side, hglaser highlighted the roughly 50% lower cost per task versus Opus 5, though khalic noted the model still looks expensive relative to similarly priced alternatives.

**Tags**: `#Claude Opus`, `#AI model evaluation`, `#Anthropic`, `#LLM performance`, `#AI pricing`

---

<a id="item-6"></a>
## [25 Fields Medalists Warn AI May Misalign with Math Research Goals](https://t.me/zaihuapd/43973) ⭐️ 8.0/10

Twenty-five Fields Medalists, including Terence Tao and Yu Deng, signed a joint statement warning that the rapid use of AI to solve mathematical problems could lead to a "serious misalignment" between the goals of AI development and the goals of mathematical research. The statement argues that the growing ability of large language models to crack major mathematical problems makes it risky to treat math problem-solving as a benchmark for AI capability. The signatories are among the most authoritative figures in mathematics, so their collective warning is likely to shape how AI labs, journals, and funders evaluate machine mathematical ability and how credit is assigned. It pushes the AI community to rethink benchmarks that reward answer production over genuine conceptual understanding, with consequences for research evaluation, academic publishing, and the broader debate about AI alignment. The statement stresses that the core of mathematical research is forming conceptual understanding and new insights rather than merely obtaining answers, and warns that AI-generated output at scale could squeeze the time available for verification, communication, and citing prior work, while raising problems of authorship and plagiarism. It also acknowledges that AI may improve research efficiency, with the outcome depending on how people choose to use the technology.

telegram · zaihuapd · Sep 22, 03:00

**Background**: The Fields Medal is widely regarded as mathematics' highest honor, awarded every four years to at most four mathematicians, usually under the age of 40, which makes a joint statement by 25 laureates an unusually weighty collective signal. Large language models have recently made notable progress on competition-style and research-level mathematics, and AI labs frequently cite such results as evidence of general reasoning ability. AI alignment refers to the effort to ensure that AI systems behave in ways consistent with human values and intentions; this statement applies that concern to the specific case of mathematics. It is a position statement about norms and incentives rather than a new technical result.

<details><summary>References</summary>
<ul>
<li><a href="https://juejin.cn/post/7328766815101337619">第十六天： 对 齐 （Alignment）人工智能 对 齐 ： AI Alignment AI ...</a></li>
<li><a href="https://llmbook-zh.github.io/LLMBook.pdf">The chinese book</a></li>

</ul>
</details>

**Tags**: `#AI and Mathematics`, `#Research Ethics`, `#Large Language Models`, `#Academic Publishing`, `#AI Alignment`

---

<a id="item-7"></a>
## [OpenAI Begins Limited Preview of GPT-5.6 Family: Sol, Terra, Luna](https://t.me/zaihuapd/43990) ⭐️ 8.0/10

OpenAI has reportedly begun a limited preview of its GPT-5.6 model family — flagship Sol, balanced Terra, and low-cost Luna — offered through the API and Codex to a small group of trusted partners. Sol emphasizes stronger coding, biology, and cybersecurity capabilities with new max reasoning effort and ultra mode, Terra is said to match GPT-5.5 at roughly half the price, and Luna is positioned as the cheapest option. This signals OpenAI's tiered 2026 strategy: a top-end flagship with expensive heavy-compute modes alongside cheaper mid- and low-tier models aimed squarely at price competition with rival labs. Developers and enterprises planning API budgets may need to reconsider which model tier they standardize on, while the US-government-gated rollout raises broader questions about how frontier model access is being mediated by regulators. Per third-party breakdowns, ultra mode is not a larger model but quietly runs around four agents in parallel while billing for all of them, reportedly scoring 91.9% on Terminal-Bench 2.1 versus 88.8% for single-agent Sol; max reasoning effort instead allocates more inference-time compute on hard problems. A key caveat is that this news comes from a single Telegram post with no accompanying discussion or independent confirmation, so model names, pricing, and availability details should be treated as unverified.

telegram · zaihuapd · Sep 22, 18:04

**Background**: GPT-5.6 is presented as the next step in OpenAI's GPT-5.x line, using a three-tier naming scheme — Sol for the flagship, Terra for the balanced middle, and Luna for the cheap, low-latency tier — roughly analogous to picking between frontier quality, general-purpose price/performance, and bulk-budget usage. "Reasoning effort" settings such as max let a model spend more compute thinking before answering, which typically improves hard coding or research tasks at higher cost, and "ultra" mode chains several agents together to push benchmark scores further. OpenAI Codex, mentioned as one of the delivery channels, is OpenAI's suite of AI coding agents used by developers to delegate software engineering work, so an early Codex rollout means the models are being tested where coding quality matters most. The mention of a US-government-requested short-term restriction means the preview is limited to vetted partners first, rather than being generally available.

<details><summary>References</summary>
<ul>
<li><a href="https://emergent.sh/learn/gpt-5-6-sol-vs-terra-vs-luna">GPT - 5 . 6 Sol vs Terra vs Luna: Which Model Should You Use?</a></li>
<li><a href="https://tosea.ai/blog/gpt-5-6-sol-terra-luna-complete-guide">GPT - 5 . 6 Sol, Terra & Luna: Complete Guide to... | Tosea.ai</a></li>
<li><a href="https://www.eesel.ai/blog/gpt-5-6-sol">What is GPT - 5 . 6 Sol? OpenAI's flagship model explained | eesel AI</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-5.6`, `#LLM`, `#AI模型发布`, `#API`

---

<a id="item-8"></a>
## [Apple adds persistent ads to iOS, frustrating users](https://www.techradar.com/phones/iphone/i-wish-apple-would-just-stop-that-crap-apple-has-added-persistent-ads-to-ios-and-its-driving-users-crazy) ⭐️ 7.0/10

Apple has introduced persistent advertising into iOS interfaces, most visibly in the App Store, where the home page and search results are now filled with promoted placements rather than only the update page. The change has sparked a large Hacker News discussion (509 points, 391 comments) in which users describe ads, update nagging, and aggressive upsells as evidence of declining platform quality. Apple has long marketed itself as the premium, privacy-first alternative to ad-driven platforms like Android and Google, so embedding persistent ads into core system surfaces erodes that differentiator and the trust users place in first-party apps. Because iOS controls a huge share of high-spending mobile users, this shift affects developers, advertisers, and anyone who assumed paying for Apple hardware meant an ad-free experience. The complaints center on the App Store, where users note the home page and search become 'an ad filled disaster' while the app update page remains relatively clean, reachable only by long-pressing the App Store icon. Commenters also pair the ad issue with macOS/iOS update behavior, saying Apple shows a permanent red badge and repeated nag prompts that can override a user's refusal if not rejected quickly enough.

hackernews · MC995 · Sep 22, 14:30 · [Discussion](https://news.ycombinator.com/item?id=49801939)

**Background**: The App Store has carried search ads since 2016, but historically they were limited to search results and the 'Today' tab, leaving most first-party surfaces free of promotion. iOS updates are also delivered through system notifications and Settings badges, and Apple does not provide a permanent 'never update' switch, only options to defer or disable automatic installation. This news reflects a broader industry pattern in which hardware vendors pursue high-margin services and advertising revenue as device sales growth slows.

**Discussion**: Commenters broadly agree that Apple's ad saturation marks a departure from its earlier design taste, with one noting that any leadership change would look like reversing the ads added under Tim Cook. Others extend the criticism to forced update nagging, bloated native apps, and iCloud storage upsells, while at least one user describes switching to Fedora Asahi Remix on an old M1 MacBook Air as an escape route — showing frustration that goes beyond ads alone.

**Tags**: `#Apple`, `#iOS`, `#Advertising`, `#User Experience`, `#Platform Policy`

---

<a id="item-9"></a>
## [TypeSafe AI's Jev outputs typed probabilistic decisions instead of text](https://simonwillison.net/2026/Sep/21/jev/) ⭐️ 7.0/10

TypeSafe AI has unveiled Jev, the first example of what it calls a "System One model" — a model that accepts text or semi-structured input (a "state" object of strings, string arrays, or name-value pairs) but returns typed probabilistic decisions rather than generated text. It supports three question types: Yes/No ("Noul", i.e. Bernoulli) questions returning a 0-1 confidence value, choice questions returning a probability distribution over options, and score questions returning a float along a numeric scale. If decision models prove reliable, they point to a different deployment pattern for LLMs: instead of bolting a text generator onto classification, ranking, or prioritization tasks and parsing its prose, software gets a typed number back directly. The economics are striking — Jev charges only for input at $0.042 per million tokens with free output — which makes it cheaper than OpenAI's GPT-5 Nano and could make large-scale scoring and reranking of documents economically trivial. Jev evaluates all questions attached to a single state in parallel, so asking many questions costs roughly the same latency as asking one, and questions are charged by input tokens only. Per TypeSafe's own "jaggedness" documentation for Jev 1.13, the model is currently weak on numbers, dates, and adversarial content, which limits how much of a decision pipeline it can safely own.

rss · Simon Willison · Sep 21, 23:09

**Background**: "System One" borrows Daniel Kahneman's distinction between fast, automatic, intuitive thinking (System 1) and slow, deliberate reasoning (System 2); TypeSafe positions Jev as the fast, cheap, always-available half of that pair. Conventional LLMs are autoregressive token generators: they emit a stream of text and are billed separately for input and output tokens, which is why long answers get expensive. A decision model instead behaves like a classic probabilistic classifier — text goes in, a calibrated score or label distribution comes out — which is what makes it fast, cheap, and easy for ordinary software to consume directly.

<details><summary>References</summary>
<ul>
<li><a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">Introducing System One Models & Jev - TypeSafe AI Blog</a></li>
<li><a href="https://docs.typesafe.ai/concepts/system-one">System One - TypeSafe AI</a></li>
<li><a href="https://www.datacamp.com/blog/system-one-models-jev">Jev: TypeSafe's System One Model Explained | DataCamp</a></li>

</ul>
</details>

**Discussion**: Commentators broadly liked the concept but pushed on the naming: Maggie Appleton argued "decision models" is a clearer term than "System One models", a view Simon Willison endorsed. On Hacker News, TypeSafe's CEO confirmed that the term "Noul" for yes/no questions is short for Bernoulli, and the recurring concern raised was opacity — Jev returns only a floating point number, so there is no way to ask which parts of the input drove a spam or relevance judgement.

**Tags**: `#LLM`, `#AI models`, `#decision models`, `#probabilistic inference`, `#model architecture`

---

<a id="item-10"></a>
## [Cloudflare Python Workers reach general availability after two-year preview](https://simonwillison.net/2026/Sep/21/cloudflare-python-worker/) ⭐️ 7.0/10

On September 21, Cloudflare announced that Python Workers are generally available, making Python a first-class, fully supported language on the Cloudflare Developer Platform. The release adds native support for frameworks such as FastAPI, Django and Flask, and lets Python code connect directly to Workers AI, R2, D1 and other platform services. Python is one of the most widely used languages in the world, so first-class support removes a major barrier for the huge pool of Python developers who want to deploy to edge and serverless environments. It also signals Cloudflare's long-term investment in the Python ecosystem, since the announcement is credited to Pyodide core maintainers Gyeongjae Choi and Hood Chatham. Python code is compiled to WebAssembly via Pyodide and executed inside Cloudflare's V8-based workerd runtime, which means threading and multiprocessing are non-functional in the WebAssembly VM. Local development is handled by the pywrangler tool (published on PyPI as workers-py), which simulates the whole stack locally using a roughly 123MB workerd binary.

rss · Simon Willison · Sep 21, 22:25

**Background**: Pyodide is a port of CPython to WebAssembly/Emscripten that makes it possible to install and run Python packages in browser-like environments. workerd is Cloudflare's open-source, server-first JavaScript and WebAssembly runtime that powers Cloudflare Workers, the company's serverless edge platform, and is also used by Wrangler for local development. By combining the two, Cloudflare can run Python on its global edge network without maintaining a separate native Python interpreter.

<details><summary>References</summary>
<ul>
<li><a href="https://pyodide.com/">Home - Pyodide</a></li>
<li><a href="https://flaviocopes.com/workerd/">How workerd , the Cloudflare Workers runtime, is built</a></li>
<li><a href="https://blog.cloudflare.com/workerd-open-source-workers-runtime/?ref=console.dev/">Introducing workerd : the Open Source Workers runtime</a></li>

</ul>
</details>

**Tags**: `#cloudflare`, `#python`, `#webassembly`, `#serverless`, `#edge-computing`

---

<a id="item-11"></a>
## [Xiaomi releases MiMo-V2.6 omni-modal model with $3.5M RL training cost](https://www.reddit.com/r/MachineLearning/comments/1wn36d4/xiaomi_releases_mimov26_frontier_intelligence_all/) ⭐️ 7.0/10

Xiaomi announced MiMo-V2.6, a frontier omni-modal model trained with reinforcement learning at a reported total RL training cost of $3.5M, and published it alongside a live "benchmaxxing" dashboard that publicly tracks its benchmark performance. The MiMo-V2.6 series brings three new models to the Xiaomi MiMo Open Platform, with API pricing unchanged from V2.5. A consumer-hardware company disclosing such a low RL training cost for a frontier multimodal model challenges the assumption that only a handful of cash-rich labs can compete at the frontier, and it puts pricing pressure on both closed APIs and other open-weight releases. The live benchmaxxing dashboard is a genuinely novel transparency experiment, though it also invites skepticism about benchmark over-optimization rather than real-world capability. MiMo-V2.6 is described as a 1M-token omnimodal model with MIT-licensed open weights and documented deployment paths via Transformers, vLLM, SGLang and Docker, plus a Pro variant callable in "UltraSpeed" mode at up to 20x output speed. The headline $3.5M figure covers the RL stage specifically rather than total pre-training compute, so it should not be read as the full cost of building the model.

reddit · r/MachineLearning · /u/we_are_mammals · Sep 22, 07:56

**Background**: "Benchmaxxing" refers to the practice of optimizing a model specifically against public leaderboards and benchmarks, which makes scores look strong even when they may not reflect everyday usefulness — a growing concern as benchmark tables from OpenAI, Google, Anthropic and Meta proliferate. Reinforcement learning has become the dominant post-training paradigm for pushing foundation models toward self-improvement, and multimodal or "omni-modal" models are those that handle text, images, audio and other inputs in a single system. Xiaomi is best known as a smartphone and IoT hardware maker, so a frontier-scale AI release marks a significant expansion into the foundation-model business.

<details><summary>References</summary>
<ul>
<li><a href="https://mimo.xiaomi.com/mimo-v2-6">MiMo - V 2 . 6 | Xiaomi</a></li>
<li><a href="https://notesgallery.in/ai-benchmark-scores-agentic-benchmaxxing/">AI Benchmark Scores Are Getting Harder to Trust. Here's Why</a></li>
<li><a href="https://kie.ai/blog/what-is-xiaomi-mimo-v2-6">Meet Xiaomi MiMo V 2 . 6 , the 1M-Token Omnimodal Model</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#multimodal`, `#model-release`, `#reinforcement-learning`, `#benchmarks`

---

<a id="item-12"></a>
## [Complex KDA: Extending Kimi Delta Attention's Expressivity](https://www.reddit.com/r/MachineLearning/comments/1wn5uv9/understanding_and_enhancing_kimi_delta_attention_r/) ⭐️ 7.0/10

A Reddit post presents Complex KDA (CKDA), a modification of Kimi Delta Attention that widens the diagonal gate range to [-1,1] and the delta-rule learning rate to [0,2], letting the full diagonal gate act as a reflection so 2D rotations can be carried out in a single step. The authors prove this form can express any orthogonal diagonal-plus-rank-one matrix and track the S3, S4 and A5 groups (but not S5), and their experiments show CKDA learns S3/S4, is competitive with standard KDA on language modelling, and shows promising results on audio continuation. It clarifies exactly where the expressivity gap between Gated DeltaNet and Kimi Delta Attention comes from, and shows that a minimal change to gate and learning-rate ranges can unlock rotation-like transforms. That matters for researchers designing linear-attention architectures that must trade off efficiency against the ability to model state-tracking tasks. The theory only guarantees tracking of finite groups up to S4/A5 and fails for S5, and extending the ranges changes the gating semantics from a decay/forget gate toward a signed reflection operation. Empirical gains are described as "promising" rather than state-of-the-art, and the work currently circulates as a preprint/community post rather than a peer-reviewed paper.

reddit · r/MachineLearning · /u/Yossarian_1234 · Sep 22, 10:34

**Background**: Kimi Delta Attention (KDA), the core of the Kimi Linear architecture, is a linear attention module that extends Gated DeltaNet (GDN) by replacing its scalar forget gate with a finer-grained, vector-valued decay. Gated DeltaNet itself improves on Mamba2 by combining the delta rule — an error-correcting memory update — with input-dependent gating to improve memory retention and selectivity. Linear attention methods aim to reduce the quadratic cost of standard softmax attention over sequence length, but they typically have weaker expressive power, which is the gap this work probes.

<details><summary>References</summary>
<ul>
<li><a href="https://jianyuh.github.io/attention/2025/12/13/KDA.html">Linear Attention : Kimi Delta Attention | Jianyu Huang</a></li>
<li><a href="https://arxiv.org/pdf/2510.26692">Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://arxiv.org/abs/2412.06464">[2412.06464] Gated Delta Networks: Improving Mamba2 with Delta Rule</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#attention-mechanisms`, `#linear-attention`, `#expressivity`, `#group-theory`

---

<a id="item-13"></a>
## [Qonto releases QontoFAQ retrieval benchmark and relevance metric](https://www.reddit.com/r/MachineLearning/comments/1wn9xqk/qontofaq_a_better_information_retrieval_benchmark/) ⭐️ 7.0/10

Qonto published QontoFAQ, a new information retrieval benchmark together with a companion metric designed to be more proportional to document relevance, along with an open-source benchmark dataset and code on GitHub. The work is documented in a Medium article on Qonto's engineering blog and was announced on r/MachineLearning by user /u/espadrine. Embedding models are increasingly judged by retrieval leaderboards, and teams building search or RAG systems have grown skeptical of benchmarks that models appear to have been tuned against. A benchmark tied to a concrete, practical objective — surfacing the article that actually answers a product question — gives practitioners a more trustworthy signal for choosing and validating embedding models. The proposed metric is intended to scale proportionally with how relevant a retrieved document is, rather than reducing retrieval to a pass/fail hit at a given cutoff. The dataset is built around Qonto's own product FAQ corpus, so its transferability to other domains or languages is not established, and the release is a practical evaluation contribution rather than a research breakthrough.

reddit · r/MachineLearning · /u/espadrine · Sep 22, 13:45

**Background**: Embedding models convert text into dense vectors so that semantically similar passages end up close together in vector space, which is the mechanism behind semantic search and retrieval-augmented generation (RAG). Retrieval benchmarks typically measure whether the correct document appears among the top-k results returned for a set of queries. Because models can be optimized for benchmark-adjacent data — a practice often called "benchmaxxing" — leaderboard scores may not reflect real-world retrieval quality, which is the problem QontoFAQ aims to address.

<details><summary>References</summary>
<ul>
<li><a href="https://adipod.ai/glossary/benchmaxxed/">Benchmaxxed — ADI Pod</a></li>
<li><a href="https://medium.com/@Nexumo_/the-8-retrieval-benchmarks-lying-to-your-rag-5811ca3ee057">The 8 Retrieval Benchmarks Lying to Your RAG | by Nexumo | Medium</a></li>

</ul>
</details>

**Tags**: `#information-retrieval`, `#benchmark`, `#embeddings`, `#evaluation`, `#nlp`

---

<a id="item-14"></a>
## [Douyin Launches Wealth Management Section With Funds and Brokerage Accounts](https://finance.jrj.com.cn/2026/09/21194458502389.shtml) ⭐️ 7.0/10

Douyin has opened a fund-purchasing entry point inside its wallet: users tap "My Wallet" to reach a wealth management page, at the bottom of which a fund portal now appears, split into five sections — current-account wealth management, bank certificates of deposit, steady wealth management, dividend funds, and return-seeking products — corresponding respectively to money market funds, bond funds, fixed-income-plus ("gu shou+"), active equity funds, and QDII public funds. The launch also supports brokerage account opening, and comes shortly before the 《金融产品网络营销管理办法》 (Administrative Measures for Online Marketing of Financial Products), issued on April 21, 2026 by the People's Bank of China and seven other departments, takes effect on September 30, 2026. A platform with hundreds of millions of daily users entering fund distribution and brokerage account opening could significantly reshape how retail investors in China are reached, putting Douyin in direct competition with established players such as Ant Group's Alipay, Tencent's Licaitong, and traditional banks and brokerages. It also makes Douyin a test case for how the new online financial marketing rules will be enforced against large third-party platforms, which are only allowed to market financial products as entrusted agents of licensed institutions. The five product categories map onto distinct risk-return profiles, from near-cash money market funds and bank deposit certificates at the low-risk end to active equity funds and QDII funds, which carry overseas market exposure and foreign-exchange quota constraints, at the high-risk end. The key caveat is regulatory: the new measures bar organizations and individuals other than financial institutions and authorized third-party platforms — explicitly including internet influencers and finance bloggers — from conducting or disguisedly conducting online marketing of financial products, so promotion within Douyin's ecosystem is confined to licensed entities.

telegram · zaihuapd · Sep 22, 01:56

**Background**: Douyin is ByteDance's short-video app and one of China's largest consumer internet platforms; "My Wallet" is its built-in payment and financial services hub. The products listed are publicly offered securities investment funds (公募基金): money market funds hold short-term debt instruments, bond funds invest mainly in bonds, "fixed-income-plus" funds combine a bond core with a small equity or derivatives allocation to boost returns, active equity funds are stock-picked portfolios, and QDII funds let domestic investors gain exposure to overseas stocks and bonds through domestic fund companies under quotas granted by the State Administration of Foreign Exchange. The 《金融产品网络营销管理办法》 was jointly released on April 21, 2026 by the central bank and seven other departments and takes effect on September 30, 2026, tightening licensing and content requirements for online marketing of financial products.

<details><summary>References</summary>
<ul>
<li><a href="http://m.ce.cn/bwzg/202605/t20260506_2947459.shtml">严 管 金 融 产 品 网 络 营 销 守好百姓“钱袋子”_中国经济 网</a></li>
<li><a href="https://cj.sina.com.cn/articles/view/5044281310/12ca99fde02002i8r8">cj.sina.com.cn/articles/view/5044281310/12ca99fde02002i8r8</a></li>
<li><a href="https://k.sina.com.cn/article_7879922977_1d5ae152101901amwc.html">带你一文读懂 QDII 基 金 | 新浪网</a></li>
<li><a href="https://www.21jingji.com/article/20230630/herald/c3917e4a261b435cb3d60d640b3178b0.html">近八成年内 收 益为正！ 震荡市下这类 基 金 “大回血”，还能上车吗？ - 21...</a></li>

</ul>
</details>

**Tags**: `#fintech`, `#Douyin`, `#wealth management`, `#China tech`, `#financial regulation`

---

<a id="item-15"></a>
## [Alibaba Unveils Zhenwu V900 AI Chip, Claiming 3x Compute Over M890](https://finance.sina.com.cn/stock/bxjj/2026-09-22/doc-inissitf7048094.shtml) ⭐️ 7.0/10

At the 2026 Yunqi (Apsara) Conference, Alibaba's chip unit T-Head unveiled the Zhenwu V900, which it claims delivers three times the compute of the previous-generation Zhenwu M890 and can scale a single cluster to 500,000 cards. CEO Eddie Wu said the self-developed M890 supernode already supports inference for 2-trillion-parameter models and is being scaled onto Alibaba Cloud this quarter, while announcing plans to train 5-10T-parameter Qwen models and to exceed 20GW of global data center capacity by 2032. The announcement positions Alibaba as one of the few players building a fully vertically integrated stack of chips, cloud and frontier models, a direct challenge to Nvidia's dominance in AI accelerators. Given ongoing US export restrictions on advanced chips to China, a credible domestic accelerator roadmap matters not only for Alibaba's own Qwen training plans but for the wider Chinese AI industry's ability to scale compute without relying on foreign hardware. Reported specifications put memory at 216 GB per V900 card, and the 500,000-card cluster figure is a scalability target rather than a demonstrated deployment. All performance numbers so far come from Alibaba itself, with no independent benchmarks or power-efficiency figures disclosed, and the 5-10T-parameter Qwen models and 20GW data center capacity are multi-year targets set for 2032 rather than near-term deliverables.

telegram · zaihuapd · Sep 22, 03:30

**Background**: T-Head (平头哥) is Alibaba's in-house semiconductor design unit, and Zhenwu (真武) is its line of AI accelerators, with the M890 as the previous generation; a 'supernode' refers to a tightly coupled group of accelerators networked together to serve very large models. Parameter count is a rough measure of a model's size and capacity — a 2-trillion-parameter model requires enormous memory and interconnect bandwidth to run inference, which is why chip vendors highlight how many cards can be linked into one cluster. Alibaba's Qwen (通义千问) is its family of open-weight large language models, and data center capacity measured in gigawatts (GW) is a common industry proxy for how much power-hungry AI infrastructure an operator plans to build.

<details><summary>References</summary>
<ul>
<li><a href="https://easternherald.com/2026/09/22/alibaba-zhenwu-v900-china-ai-chip/">Alibaba Unveils Zhenwu V 900 : China's Most Powerful AI Chip</a></li>
<li><a href="https://cryptobriefing.com/alibaba-ai-model-zhenwu-v900-chip/">Alibaba plans AI model with 5-10 trillion parameters, unveils Zhenwu ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#Alibaba`, `#semiconductors`, `#LLM infrastructure`, `#data centers`

---

<a id="item-16"></a>
## [DeepSeek Releases DSec Sandbox Platform Report: 3M Sandboxes Daily for Agent Training](https://arxiv.org/abs/2609.22978) ⭐️ 7.0/10

DeepSeek-AI and Tsinghua University jointly released a technical report on DeepSeek Elastic Compute (DSec), a production sandbox platform that serves roughly 3 million sandbox instances per day to support large-scale agent training and evaluation. DSec offers a unified SDK across four backends — FnCall, containers, Firecracker microVMs, and full VMs — and decouples stateful rollout execution from preemptible GPU training. Agent training and reinforcement learning increasingly depend on safely executing untrusted, stateful code at massive scale, and DSec shows what a production-grade solution looks like in practice. The disclosed numbers — about 3 million sandboxes per day, over 380K peak concurrency, and more than 5,000 creations per second — give AI infrastructure and systems engineers a concrete reference point for building their own agent sandboxing layers. A single production unit of DSec spans about 160 nodes and can densely host 3,200 containers or 800 microVMs per node; on-demand EROFS image loading via the 3FS distributed file system cut task completion time by 1.7x and disk writes by 57% versus traditional full Docker pulls, while memory sharing and reclamation reduced peak memory usage by roughly 40%. The platform covers workloads including online-judge grading, software engineering, security penetration testing, and computer-use tasks.

telegram · zaihuapd · Sep 22, 04:45

**Background**: AI agents are typically trained and evaluated by letting them actually run code, browse, or operate a computer, which requires isolating each run so it cannot damage the host or other runs — a task called sandboxing. Firecracker is AWS's open-source virtualization technology that creates lightweight microVMs, combining hardware-level isolation with fast startup, while EROFS is a read-only Linux file system originally developed by Huawei that is optimized for compact, high-performance image delivery. Reinforcement learning pipelines for agents need enormous numbers of these isolated environments simultaneously, which is why infrastructure at this scale has become an area of active engineering competition.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/firecracker-microvm/firecracker">GitHub - firecracker - microvm / firecracker : Secure and fast microVMs...</a></li>
<li><a href="https://en.wikipedia.org/wiki/EROFS">EROFS - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI Infrastructure`, `#Agent Training`, `#Sandboxing/MicroVMs`, `#Reinforcement Learning`, `#Distributed Systems`

---

<a id="item-17"></a>
## [Mimo CLI alleged to collect repo metadata and package source code](https://linux.do/t/topic/2935748) ⭐️ 7.0/10

A reverse-engineering analysis posted on LINUX DO found that Mimo CLI may by default upload a project's Git repository URL, commit hash, and branch information, behavior that can be disabled by setting MIMOCODE_ENABLE_ANALYSIS=false. The same analysis found an unused collectCodebase() function in Mimo CLI's closed-source trajectory-bundle and codebase-bundle extensions that can enumerate Git repository files, read source code, and compress it into a package. For developers, AI coding CLIs often run inside private repositories, so default telemetry of repository metadata and a hidden code-packaging capability in closed-source extensions raise serious privacy and supply-chain trust concerns. If confirmed, the findings could deter teams from adopting Mimo Code and add pressure on vendors to disclose telemetry and ship auditable open-source components. The disclosure stresses that the findings are not officially confirmed and that no evidence yet shows collectCodebase() is actually invoked or that any packaged source code is uploaded externally. The relevant code is said to reside only in the closed-source trajectory-bundle and codebase-bundle extensions, not in Mimo CLI's official open-source repository, and the telemetry can be opted out via an environment variable.

telegram · zaihuapd · Sep 22, 08:18

**Background**: Mimo CLI, also referred to as MiMo Code, is Xiaomi's AI-powered coding assistant distributed as a terminal CLI tool, similar in category to Claude Code and Gemini CLI. AI coding agents commonly include telemetry to improve product quality, but repository URLs, commit hashes, branch names, and source code are far more sensitive than ordinary usage metrics. Because parts of Mimo CLI are closed-source extensions, independent reverse engineering by developers is often the only way to inspect what data the tool can access. The MIMOCODE_ENABLE_ANALYSIS environment variable indicates that an analysis or telemetry feature can be toggled by the user.

<details><summary>References</summary>
<ul>
<li><a href="https://mimo.xiaomi.com/mimocode/install">Install MiMo Code and launch it in your terminal.</a></li>
<li><a href="https://mimo.mi.com/docs/en-US/tokenplan/integration/mimo-code">Xiaomi MiMo Home</a></li>
<li><a href="https://mimocode.org/">Mimo Code Guide — Install, Compare, Configure & AI Coding Agent...</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#security`, `#reverse-engineering`, `#developer-tools`, `#data-collection`

---

<a id="item-18"></a>
## [China Probes DeepSeek and Moonshot Over Data Leak Claims](https://www.theinformation.com/articles/china-probes-deepseek-moonshot-potential-data-leaks-anthropic) ⭐️ 7.0/10

Chinese internet regulators are reportedly investigating DeepSeek and Moonshot AI after Anthropic published a 154-page report on September 10 accusing seven Chinese companies of improperly routing sensitive user data through its Claude models. The report specifically cites an example in which DeepSeek allegedly forwarded requests from an engineer working on police surveillance systems to Claude. The case sits at the intersection of AI governance, data privacy and US-China tech tensions, and it signals that Chinese regulators are willing to scrutinize their own flagship AI labs over cross-border data handling. It could push domestic labs to harden their data-routing and third-party model usage policies, and it adds a compliance dimension to the already intense competition between Chinese open-weight model makers and US frontier labs. The trigger is Anthropic's 154-page report, which claims seven Chinese firms made improper use of Claude, with the DeepSeek example involving requests tied to police surveillance development. The investigation is reported by The Information based on people familiar with the matter, and neither DeepSeek nor Moonshot has publicly confirmed the probe, so the scope and any potential penalties remain unclear.

telegram · zaihuapd · Sep 22, 14:37

**Background**: DeepSeek is a Hangzhou-based AI company, funded by the hedge fund High-Flyer, that publishes open-weight large language models; Moonshot AI (月之暗面), named after Pink Floyd's album, is the Chinese lab behind the Kimi model family. Claude is Anthropic's commercial large language model, typically accessed through an API whose terms restrict certain uses and data handling. In practice, developers sometimes route queries from one model to another, which is what the alleged leak-and-forward pattern involves.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_(Company)">DeepSeek (Company)</a></li>
<li><a href="https://www.moonshot.ai/">Welcome to Moonshot AI . Our mission is to seek the optimal...</a></li>

</ul>
</details>

**Tags**: `#AI Regulation`, `#Data Privacy`, `#DeepSeek`, `#Anthropic`, `#China Tech`

---

<a id="item-19"></a>
## [DeepSeek to Brief UN Security Council on AI Risks This Week](https://t.me/zaihuapd/43989) ⭐️ 7.0/10

Two people familiar with the matter said Chinese AI startup DeepSeek will brief the UN Security Council this week on the risks posed by artificial intelligence, with the 15-member council scheduled to meet Wednesday to discuss AI and international security. OpenAI CEO Sam Altman is expected to attend the briefing, an Anthropic senior representative is also expected, and Chinese AI firms including DeepSeek and Moonshot were invited to speak — though DeepSeek founder Liang Wenfeng does not plan to attend and the arrangements could still change. It marks a rare moment where leading US and Chinese frontier AI labs share the same stage in a formal multilateral security forum, signaling that frontier AI risk is being treated as a geopolitical and international-security issue rather than a purely technical one. The outcome could shape how governments approach AI governance, export controls, and future international rules that directly affect labs, developers and users worldwide. The briefing is tied to a Security Council session on AI and international security, and participation spans US labs (OpenAI, Anthropic) and Chinese labs (DeepSeek, Moonshot), which is unusual given ongoing US-China tech tensions. Notably, DeepSeek founder Liang Wenfeng is not expected to appear personally, and sources caution the schedule may shift at short notice.

telegram · zaihuapd · Sep 22, 17:39

**Background**: DeepSeek is a Hangzhou-based Chinese AI company, owned and funded by the hedge fund High-Flyer, that develops open-weights large language models and gained global attention for releasing competitive models at unusually low cost. Anthropic is a US AI safety-focused lab behind the Claude models, while OpenAI is the maker of ChatGPT and GPT-series models; both have publicly emphasized the dangers of advanced AI. The UN Security Council, with 15 members and five permanent veto-holding powers, has held earlier discussions on AI as a emerging threat to international peace and security, but briefings by frontier AI companies remain a new and largely symbolic form of engagement.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_(Company)">DeepSeek (Company)</a></li>
<li><a href="https://huggingface.co/Anthropic">Org profile for Anthropic on Hugging Face, the AI community building...</a></li>
<li><a href="https://tracxn.com/d/companies/moonshot-ai/__wZzU6o3CAntBLbB5MXh7XINvgyVvzhQb4DNTaMgBTp4">Moonshot AI - 2026 Company Profile, Team, Funding... - Tracxn</a></li>

</ul>
</details>

**Tags**: `#AI governance`, `#AI safety`, `#DeepSeek`, `#UN Security Council`, `#geopolitics`

---

<a id="item-20"></a>
## [Reported GPT-6 'Astra' breaks Enigma message unsolved since 2005, sparking debate](https://www.cryptocellar.org/bgac/the-mvueh-break.html) ⭐️ 6.0/10

A reported OpenAI model called "GPT-6 Astra" is said to have decrypted a German Army Enigma radiogram from 1941 that had sat unsolved in the CryptoCellar archive since 2005, apparently by writing its own Enigma simulator in Python and C++. The claim drew 486 points and 341 comments on Hacker News, where several commenters noted that other tools — including something described as "gemini 3.8 flash" — also decrypted the same message within tens of minutes. If validated, this would be a striking example of an LLM autonomously building domain-specific tooling and working through a historical cryptanalysis problem that human researchers had left open for roughly two decades, which feeds directly into the debate about AI as an independent research agent. At the same time, it highlights how hard credit attribution becomes when the breakthrough depends on self-generated simulators and on prior human cryptanalysis. The recovered plaintext reads "BTTE UM ANGABE DES MARSQWEGES X BEFINDE MIQ IN X ROSENOW ROSENOW X SOFORT FUNKANTWORT X WASCHBBSCH", which with its misspellings translates roughly to "Please specify the route of march. I am in Rosenow, Rosenow. Immediate reply by radio. Waschbusch." Important caveats: the model names "GPT-6 Astra" and "gemini 3.8 flash" look unusual, the reported break relied on comparing a neighboring radiogram (SIPVX No. 173) that a human researcher had already solved in 2017, and with Enigma a key shorter than the message can in principle yield a plausible-looking but incorrect plaintext.

hackernews · sohkamyung · Sep 22, 13:52 · [Discussion](https://news.ycombinator.com/item?id=49801324)

**Background**: The Enigma is the rotor cipher machine Germany used for military communications in World War II, and breaking it at Bletchley Park is a foundational episode in computing history. CryptoCellar is an online archive of intercepted Enigma messages, some of which have remained unsolved since they were published around 2005. Cracking such a message usually requires cribs (guessed plaintext), knowledge of daily key settings and operator habits, and a large amount of trial-and-error search, which is exactly the kind of repetitive work that a program — written by a human or by a model — can automate.

<details><summary>References</summary>
<ul>
<li><a href="https://forklog.com/news/ai/gpt-6-astra-rasshifrovala-radiogrammu-enigma-1941-goda">GPT-6 Astra расшифровала радиограмму Enigma 1941... - ForkLog</a></li>
<li><a href="https://habr.com/ru/news/1084042/">GPT-6 Astra помогла прочесть зашифрованную Enigma ... / Хабр</a></li>

</ul>
</details>

**Discussion**: Commenters were largely skeptical about attribution: tantalor argued that "did it entirely on its own" is incongruous with the model writing Python and C++ Enigma simulator software, and asked how much of that code was novel and how much of the breaking process was simply offloaded to it. podgorniy reported that "gemini 3.8 flash" one-shotted the decryption in about 45 minutes while Opus was still running, suggesting the feat is not unique to Astra. Others supplied the German plaintext, wondered whether a wrong key could still produce a valid-looking message, and hoped the same approach might finally crack the fourth section of Kryptos.

**Tags**: `#ai`, `#cryptography`, `#enigma`, `#llm`, `#hackernews`

---

<a id="item-21"></a>
## [GrapheneOS hints at preinstalled devices shipping as early as 2027](https://grapheneos.social/@GrapheneOS/117299954135808210) ⭐️ 6.0/10

The GrapheneOS project stated on its official social account that there is a high chance devices will be sold with GrapheneOS preinstalled in 2027, with community members speculating the hardware partner is likely Motorola. Commenters clarified that this concerns factory preinstallation on planned models, not a change to the existing self-install process available for Pixel devices. The preinstalled units would reportedly come from a third-party company given the devices directly by the manufacturer rather than from Motorola's own store. If it happens, this would be the first real path for a hardened, de-Googled Android distribution to reach mainstream buyers without requiring them to unlock bootloaders and flash firmware by hand. That shift could pressure other OEMs to offer more privacy-respecting variants and give corporate and everyday users a legitimate alternative to stock Android. The timeline is distant and still speculative, and GrapheneOS itself framed it as a likely rather than confirmed outcome. A major open question is app compatibility: many banking and enterprise BYOD apps rely on Google's Play Integrity API and Google-certified devices, so a non-certified OS can fail attestation checks even when the apps install fine. Community members also raised pricing, noting the Motorola Signature line runs roughly $1,230–$1,460 depending on region, close to Pixel pricing.

hackernews · Cider9986 · Sep 22, 17:12 · [Discussion](https://news.ycombinator.com/item?id=49804683)

**Background**: GrapheneOS is an open-source, security- and privacy-hardened fork of Android (AOSP) that is best known for running on Google Pixel phones, where users install it themselves via a web-based flashing tool. Rather than removing Android features, it hardens sandboxing, adds permission controls and reduces the data the OS exposes to apps and Google services. For a manufacturer to ship it preinstalled, the vendor must be willing to sell a device that lacks Google Mobile Services certification, which is exactly what triggers compatibility problems with attestation-dependent apps such as mobile banking.

<details><summary>References</summary>
<ul>
<li><a href="https://privsec.dev/posts/android/banking-applications-compatibility-with-grapheneos/">Banking Applications Compatibility with GrapheneOS</a></li>
<li><a href="https://sy.st/blog/my-1-year-experience-of-using-grapheneos/">My 1 year experience of using GrapheneOS - Syst(em)</a></li>
<li><a href="https://developer.android.com/google/play/integrity/setup">Setup | Play Integrity | Android Developers</a></li>

</ul>
</details>

**Discussion**: The 91-comment thread was largely clarifying rather than dismissive: users stressed that this is about preinstallation on specific upcoming models while self-installation on planned hardware should remain possible, and that the seller is likely a third party rather than Motorola's own store. The dominant concerns were practical — whether corporate BYOD and banking apps would pass integrity checks — along with price comparisons against Pixel and a lighthearted demand for a $100 GrapheneOS phone.

**Tags**: `#GrapheneOS`, `#Mobile Security`, `#Privacy`, `#Android`, `#Motorola`

---

<a id="item-22"></a>
## [LinearSolveBench: new benchmark for AI-written sparse linear solvers in C](https://www.reddit.com/r/MachineLearning/comments/1wnctam/linearsolvebench_new_benchmark_for_linear_solvers/) ⭐️ 6.0/10

A new benchmark called LinearSolveBench was announced on r/MachineLearning (submitted by /u/hgarud, code at github.com/hgarud/LinearSolveBench) that measures the ability of a model or harness to write fast, accurate, and general numerical solvers for large sparse linear systems in C. Its stated goal is to encourage algorithmic advances in numerical methods for solving systems of linear equations. Most coding benchmarks reward functionally correct code on everyday software tasks, whereas numerical solvers are judged on asymptotic performance, numerical stability and generality across problem classes — a much harder target for code-generating models. If it gains traction, LinearSolveBench could become a useful yardstick for AI for scientific computing and for agents that must produce high-performance numerical kernels rather than just compiling code. The task is deliberately scoped to C implementations of solvers for large sparse systems, and solutions are evaluated along three axes — speed, accuracy and generality — which together discourage hard-coding or tuning to a single matrix family. The public announcement is brief: the repository is new and the post provides no leaderboard, baseline results, matrix suite details or versioning information, so the exact scoring methodology and problem distribution remain to be verified by inspecting the repo.

reddit · r/MachineLearning · /u/hgarud · Sep 22, 15:34

**Background**: Solving a sparse linear system means finding the vector x that satisfies Ax = b when the matrix A is mostly zeros but very large, as happens in finite-element simulation, computational fluid dynamics, structural analysis and graph problems. Two broad families of methods exist: direct methods such as sparse LU or Cholesky factorization, and iterative methods such as conjugate gradient and GMRES, which are usually paired with a preconditioner to converge quickly; choosing and implementing the right combination is a core skill in numerical analysis. Because sparse solvers are memory-bound, need careful data structures (e.g. compressed sparse row) and are sensitive to numerical conditioning, writing one that is simultaneously fast, accurate and general is considerably harder than writing typical application code — which is precisely what this benchmark tries to measure.

<details><summary>References</summary>
<ul>
<li><a href="https://amcs.kaust.edu.sa/topics/sparse-linear-systems">sparse linear systems | Applied Mathematics and Computational...</a></li>
<li><a href="https://gitlab.mn.tu-dresden.de/teaching/sparse_linear_systems">sparse _ linear _ systems · GitLab</a></li>
<li><a href="https://link.springer.com/article/10.1007/s11075-026-02463-z">On the adaptive-momentum variant for maximal weighted residual...</a></li>

</ul>
</details>

**Tags**: `#benchmark`, `#linear solvers`, `#numerical methods`, `#scientific computing`, `#code generation`

---

<a id="item-23"></a>
## [Templar simulates stage-skipping fault tolerance for pipeline-parallel pre-training](https://www.reddit.com/r/MachineLearning/comments/1wnd5ys/simulating_fault_tolerance_with_stage_skipping_in/) ⭐️ 6.0/10

Templar published a simulation study showing that its Crucible distributed pre-training platform can keep healthy workers training when one pipeline stage goes offline, by simply having activations and gradients bypass the failed stage for several steps. Using a 178M-parameter model with eight data-parallel replicas and four stages per replica, and a 1% per-replica failure probability per global step, validation loss stayed close to each configuration's own no-failure baseline even though every simulated outage removed a stage for six global steps. If these learning-dynamics results hold in real deployments, large pre-training runs could tolerate unreliable hardware instead of stalling or restarting, opening the door to training on cheaper spot instances and a broader, more heterogeneous pool of compute. That would directly attack the cost and scheduling bottlenecks that dominate large-scale distributed training today. The study is explicitly a simulation of the learning effects of stage failures rather than a measurement of physical worker replacement, recovery time, or production cost savings, so the practical systems overhead remains unquantified. The authors also report that fixed projections shared across layers further improve robustness when pipeline compression is used, and speculate that shared projectors align representations across stage boundaries so bypasses are less disruptive — but they flag this alignment explanation as a hypothesis rather than a demonstrated mechanism.

reddit · r/MachineLearning · /u/covenant_ai · Sep 22, 15:47

**Background**: Pipeline parallelism splits a model into sequential stages placed on different workers, so each worker only holds and computes part of the network; data parallelism instead replicates the full model across independent copies (replicas). Because a stage can only proceed once the previous stage has produced its activations, losing a single worker can stall an entire pipeline, which is why large training runs traditionally rely on checkpoint-and-restart recovery that wastes substantial time. SparseLoCo reduces communication between replicas by exchanging heavily compressed pseudo-gradients (for example with top-k sparsification), while pipeline compression reduces traffic across stage boundaries inside each replica; stage skipping builds on this setup by letting the remaining stages continue computing tokens while a missing stage is bypassed.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/one-covenant/SparseLoCo">GitHub - one-covenant/ SparseLoCo : CCLoco: Scaling Up Top-K Error...</a></li>
<li><a href="https://deepwiki.com/one-covenant/SparseLoCo/4.2-distributed-training-setup">Distributed Training Setup | one-covenant/ SparseLoCo | DeepWiki</a></li>
<li><a href="https://arxiv.org/pdf/2110.02781">FTPipeHD: A Fault - Tolerant Pipeline - Parallel</a></li>

</ul>
</details>

**Tags**: `#distributed-training`, `#fault-tolerance`, `#pipeline-parallelism`, `#machine-learning-systems`, `#pre-training`

---

<a id="item-24"></a>
## [US Proposes AI Incident Notification Channel With China](https://x.com/rohanpaul_ai/status/2102254209597157548) ⭐️ 6.0/10

The United States proposed to China the creation of an AI incident reporting channel for notifying each other about AI-related events that cross a national security threshold, a proposal raised at a September 20 meeting in New York between Treasury Secretary Scott Bessent and Chinese Vice Premier He Lifeng. The two sides also plan to establish a regular US-China AI dialogue on shared risks, but China's official statement only confirmed that AI topics were discussed and did not explicitly accept the specific mechanism, and no bilateral agreement or treaty has been reached. If realized, this would be the first dedicated bilateral crisis-communication channel for AI between the world's two leading AI powers, potentially reducing the risk of miscalculation when advanced AI systems cause security-relevant incidents. It signals that AI safety and risk management are moving from purely domestic regulation into the domain of great-power diplomacy, which would affect AI labs, cloud providers, and policymakers in both countries. The proposal is limited to incidents meeting a defined national security threshold rather than all AI incidents, and it remains only a proposal with no formal mechanism, timeline, or enforcement structure agreed. The discussion occurred just ahead of a September 24 White House meeting between Donald Trump and Xi Jinping, suggesting the channel is being positioned as a confidence-building measure rather than a binding treaty.

telegram · zaihuapd · Sep 22, 06:48

**Background**: AI incident reporting frameworks are governance mechanisms designed to capture and manage cases where AI systems behave unexpectedly, cause harm, or violate policy, typically defining what must be reported, to whom, and within what timeframe. A bilateral version differs from domestic regimes because it requires two rival governments to agree on shared definitions, thresholds, and confidentiality rules. The US and China have previously set up military hotlines and dialogue channels to avoid escalation, and this proposal applies that same crisis-communication logic to AI risks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/09/20/business/us-china-ai-warning-system-national-security.html">U.S. and China Discuss System to Warn of A . I . National Security Issues</a></li>
<li><a href="https://nationalcioreview.com/articles-insights/extra-bytes/the-u-s-and-china-want-a-crisis-hotline-for-the-ai-race/">The U.S. and China Want a Crisis Hotline... - The National CIO Review</a></li>

</ul>
</details>

**Tags**: `#AI Governance`, `#AI Policy`, `#US-China Relations`, `#AI Safety`, `#Geopolitics`

---

<a id="item-25"></a>
## [iOS 27.2 Beta 2 Adds China-Only Motion Data Restriction](https://t.me/zaihuapd/43986) ⭐️ 6.0/10

iOS 27.2 beta 2 reportedly introduces a new China-mainland-specific permission called "Restrict Motion Data" (限制動作資料), located under Settings → Privacy & Security → Motion & Fitness, which when enabled blocks designated third-party apps from reading accelerometer and gyroscope data. Testers note the toggle only appears when the device is signed into a China mainland Apple ID, and it may expand to other regions later. If confirmed, this would be the first platform-level switch letting users cut off raw motion sensor access for third-party apps, a meaningful step beyond the existing Motion & Fitness permission. Because it appears tied to Apple ID region, it also hints at region-specific privacy or regulatory requirements shaping iOS features in China. The toggle is reportedly reachable via Settings → Privacy & Security → Motion & Fitness and shows as "Restrict Motion Data" under a Simplified Chinese system language and "限制動作資料" under Traditional Chinese. The claim is an unverified observation from a Telegram tipster with no official Apple documentation, developer notes, or API details explaining how the block is enforced or which sensors are affected beyond accelerometer and gyroscope.

telegram · zaihuapd · Sep 22, 12:37

**Background**: iOS apps normally access device movement through Apple's Core Motion framework, which surfaces data from the accelerometer (measuring linear acceleration) and the gyroscope (measuring rotation rate) — both MEMS sensors now standard in smartphones. Access has historically been governed by the Motion & Fitness permission, which developers rely on for step counting, fitness tracking, and validating GPS distance in workout apps such as MapMyFitness. A hardware-level or permission-level block on raw motion data would therefore affect far more than fitness features, potentially including gesture controls, gaming, and stabilization-related use cases.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gyroscopic_sensor">Gyroscopic sensor</a></li>
<li><a href="https://developer.apple.com/forums/thread/60341">Misleading info on Motion data per… | Apple Developer Forums</a></li>
<li><a href="https://support.mapmyfitness.com/hc/en-us/articles/1500009118022-iOS-Motion-Sensor">iOS Motion Sensor – MapMyFitness</a></li>

</ul>
</details>

**Tags**: `#iOS`, `#privacy`, `#sensors`, `#Apple`, `#China`

---