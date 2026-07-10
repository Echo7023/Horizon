---
layout: default
title: "Horizon Summary: 2026-07-10 (EN)"
date: 2026-07-10
lang: en
---

> From 38 items, 10 important content pieces were selected

---

1. [OpenAI Releases GPT-5.6 with SOTA on ARC-AGI-3](#item-1) ⭐️ 9.0/10
2. [Postgres rewritten in Rust passes all regression tests](#item-2) ⭐️ 9.0/10
3. [TypeScript 7.0 Released: Go Rewrite Delivers Up to 12x Speed Boost](#item-3) ⭐️ 9.0/10
4. [EU Parliament Revives Mass Message Scanning via Procedural Trick](#item-4) ⭐️ 8.0/10
5. [Meta Releases Muse Spark 1.1 Agentic AI Model with API](#item-5) ⭐️ 8.0/10
6. [Meta's Superintelligence Progress: RL Startup and Compute Ramp](#item-6) ⭐️ 8.0/10
7. [IMGNet: Face Verification Using Sign Pattern Matching](#item-7) ⭐️ 8.0/10
8. [Ant Open-Sources World's First MoE Embodied Video Model](#item-8) ⭐️ 8.0/10
9. [DJI EV50 Drone Breaks Altitude Record over Everest](#item-9) ⭐️ 8.0/10
10. [China's Supercomputing Core Node Online with 100K+ AI Cards](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Releases GPT-5.6 with SOTA on ARC-AGI-3](https://openai.com/index/gpt-5-6/) ⭐️ 9.0/10

OpenAI has released GPT-5.6, its latest flagship model, which achieves a new state-of-the-art on the ARC-AGI-3 benchmark with a 7.8% score from the Sol variant. The model also features improved intent understanding and image handling capabilities. This release marks a significant step in frontier AI, as GPT-5.6 is the first verified model to beat an ARC-AGI-3 game, showcasing progress toward more general agentic intelligence. The improved intent understanding and image handling will enhance user experience in coding and multimedia tasks. GPT-5.6 comes in three sizes: Luna (smallest), Terra (medium), and Sol (largest). According to community testing, Terra's coding performance is similar to GPT-5.5 and slightly behind Sonnet 5, while Sol achieved the ARC-AGI-3 SOTA.

hackernews · logickkk1 · Jul 9, 17:04 · [Discussion](https://news.ycombinator.com/item?id=48849066)

**Background**: ARC-AGI-3 is an interactive reasoning benchmark designed to measure agentic intelligence through novel abstract environments. It requires AI agents to explore, infer goals, build internal models, and plan. The benchmark uses turn-based games to evaluate capabilities beyond static question-answering.

<details><summary>References</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arxiv.org/abs/2603.24621">[2603.24621] ARC-AGI-3: A New Challenge for Frontier Agentic Intelligence</a></li>

</ul>
</details>

**Discussion**: Comments highlight mixed reactions: some praise the ARC-AGI-3 SOTA as a first for a frontier model, while others note that GPT-5.6's coding performance (Terra) is comparable to previous versions and behind competitors like Sonnet 5. There is also critique about omitted benchmarks like Fable 5, and users debating whether to switch from Claude Code to Codex.

**Tags**: `#AI`, `#GPT`, `#OpenAI`, `#LLM`, `#Benchmark`

---

<a id="item-2"></a>
## [Postgres rewritten in Rust passes all regression tests](https://github.com/malisper/pgrust) ⭐️ 9.0/10

The pgrust project, a rewrite of PostgreSQL in Rust using large language models, has achieved 100% compatibility by passing all PostgreSQL regression tests. This demonstrates a potential paradigm shift in database engineering, showing that LLMs can assist in complex rewrites and that Rust may offer memory safety and performance benefits for critical infrastructure. The project has over 7,100 commits generated in less than a month by LLMs, and it uses the AGPL license instead of the original PostgreSQL license, raising compatibility concerns.

hackernews · SweetSoftPillow · Jul 9, 06:18 · [Discussion](https://news.ycombinator.com/item?id=48841676)

**Background**: PostgreSQL is a popular open-source relational database with decades of development. Rust is a systems programming language known for memory safety without garbage collection. Rewriting PostgreSQL in Rust could improve safety and performance, but the use of LLMs for code generation introduces new challenges in code review and licensing.

**Discussion**: Comments applaud the technical achievement but raise concerns about reviewing LLM-generated code, license compatibility (switching from PostgreSQL license to AGPL), and the purpose of such rewrites. Some suggest mirroring queries in production for testing, while others question the necessity and ethical implications.

**Tags**: `#PostgreSQL`, `#Rust`, `#LLM`, `#database`, `#rewrite`

---

<a id="item-3"></a>
## [TypeScript 7.0 Released: Go Rewrite Delivers Up to 12x Speed Boost](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 9.0/10

Microsoft has officially released TypeScript 7.0, a native version rewritten in Go that achieves 8-12x faster full builds compared to previous versions and introduces shared-memory multithreading. Users can install it via npm, and editors can support the new language server through LSP. This release marks a major performance milestone for TypeScript, significantly improving developer productivity by reducing build times. The multithreading support and Go-based architecture set a new standard for language tooling performance, impacting millions of developers in the JavaScript/TypeScript ecosystem. The new version introduces --checkers and --builders flags to customize parallelism and provides a compatibility package for coexistence with TypeScript 6. However, toolchains for embedded languages like Vue and Svelte still require the old version due to incomplete API migration.

telegram · zaihuapd · Jul 9, 04:01

**Background**: TypeScript is a typed superset of JavaScript that compiles to plain JavaScript, widely used for large-scale web applications. Previously, TypeScript's compiler was written in TypeScript itself, leading to performance bottlenecks. The Language Server Protocol (LSP) is a standard that enables editors to provide language features like auto-completion and diagnostics by communicating with a language server.

<details><summary>References</summary>
<ul>
<li><a href="https://www.totaltypescript.com/typescript-announces-go-rewrite">TypeScript Announces Go Rewrite, Achieves 10x Speedup | Total TypeScript</a></li>
<li><a href="https://en.wikipedia.org/wiki/Language_Server_Protocol">Language Server Protocol - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#TypeScript`, `#Go`, `#performance`, `#language-server`, `#release`

---

<a id="item-4"></a>
## [EU Parliament Revives Mass Message Scanning via Procedural Trick](https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/) ⭐️ 8.0/10

On July 9, 2026, the European Parliament allowed Chat Control 1.0 to pass, reauthorizing US tech companies to scan private messages without a warrant until 2028, despite a majority of MEPs voting against it. This decision undermines digital privacy and encryption for 450 million EU citizens, setting a precedent for mass surveillance by private companies and threatening fundamental rights. The motion to reject the measure failed because it required an absolute majority of all 720 MEPs (361 votes), but only 314 voted against, 276 in favor, and 17 abstained, with 113 absent. The scanning applies to direct messages on platforms like Instagram, Discord, Snapchat, Skype, Xbox, Gmail, and iCloud.

hackernews · rapnie · Jul 9, 11:03 · [Discussion](https://news.ycombinator.com/item?id=48843923)

**Background**: Chat Control 1.0 is a temporary EU regulation originally introduced in 2021 to combat child sexual abuse material (CSAM) by requiring platforms to scan private communications. It ended in March 2026 when a vote to extend it narrowly failed. Civil society organizations and privacy advocates have criticized the measure for mandating mass surveillance that breaks end-to-end encryption.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control_1.0">Chat Control 1.0</a></li>
<li><a href="https://www.theepochtimes.com/world/eu-lawmakers-advance-mass-private-message-scanning-measure-6059506">EU Lawmakers Advance Mass Private-Message Scanning Measure | The Epoch Times</a></li>
<li><a href="https://www.reddit.com/r/europe/comments/1urnadd/european_parliament_greenlights_chat_control_10/">r/europe on Reddit: European Parliament greenlights Chat Control 1.0, will now become law. 276 In Favour, 314 Against, 17 Abstentians.</a></li>

</ul>
</details>

**Discussion**: Commenters expressed outrage over the procedural maneuver, calling it a 'stupid parliamentary trick' and a threat to democracy. Many highlighted that the vote was held on the last day before summer break with many MEPs absent, and that the requirement for an absolute majority to reject allowed the measure to pass despite majority opposition. Some criticized European Parliament President Roberta Metsola for forcing the vote under urgency procedure.

**Tags**: `#privacy`, `#EU legislation`, `#surveillance`, `#chat control`, `#digital rights`

---

<a id="item-5"></a>
## [Meta Releases Muse Spark 1.1 Agentic AI Model with API](https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/) ⭐️ 8.0/10

Meta has released Muse Spark 1.1, its most capable agentic AI model for coding and autonomous task execution, now available via API with paid pricing starting at $1.25 per million input tokens. This release marks Meta's entry into the competitive AI coding assistant market, potentially challenging offerings from OpenAI and Anthropic while offering a more open model with detailed evaluation reports, sparking debate about evaluation standards and pricing. Muse Spark 1.1 shows substantial improvement on real-world coding tasks, including debugging and large code migrations, but community members noted that the evaluation used non-standard terminal bench settings with higher resource caps, potentially inflating results. The API pricing is $1.25/$4.5 per million tokens (input/output) with $0.15 for cached input.

hackernews · ot · Jul 9, 14:10 · [Discussion](https://news.ycombinator.com/item?id=48846184)

**Background**: Agentic AI models are designed to autonomously perform multi-step tasks, use external tools, and reason over complex workflows, going beyond simple text generation. Meta positions Muse Spark 1.1 as part of its vision for 'personal superintelligence,' competing in the rapidly growing AI coding assistant market alongside models like GPT-4 and Claude.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/">Introducing Muse Spark 1.1</a></li>
<li><a href="https://techcrunch.com/2026/07/09/meta-enters-the-crowded-ai-coding-battle-with-muse-spark-1-1/">Meta enters the crowded AI coding battle with Muse Spark 1.1 | TechCrunch</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The community discussion highlighted two main concerns: first, GodelNumbering argued that the evaluation used resource caps exceeding official limits for Terminal-Bench-2.1, making the benchmark results invalid. Second, simonw shared a practical plugin for using the model, while Tiberium and bradfa criticized the pricing and lack of clear data retention policy, respectively.

**Tags**: `#AI`, `#Meta`, `#Muse Spark`, `#LLM`, `#agentic model`

---

<a id="item-6"></a>
## [Meta's Superintelligence Progress: RL Startup and Compute Ramp](https://newsletter.semianalysis.com/p/the-future-of-meta-superintelligence) ⭐️ 8.0/10

Meta's superintelligence initiative has spawned a new top-tier reinforcement learning environment startup, and is pursuing an unprecedented compute ramp with over 2000km scale-across interconnects. This signals Meta's aggressive push toward superintelligence, potentially reshaping the AI landscape by enabling massive-scale RL training and challenging rivals like Google DeepMind. The compute ramp is described as the most aggressive ever seen, with a scale-across distance of over 2000 kilometers, suggesting a distributed cluster infrastructure. The RL environment startup emerged 'out of thin air,' indicating a significant new entity in the AI community.

rss · Semianalysis · Jul 9, 19:16

**Background**: Meta has been investing heavily in AI research and infrastructure, with a stated goal of achieving superintelligence. Reinforcement learning environments are critical for training AI agents in complex tasks, and large-scale compute is essential for modern AI breakthroughs.

**Tags**: `#Meta`, `#superintelligence`, `#AI infrastructure`, `#reinforcement learning`, `#compute`

---

<a id="item-7"></a>
## [IMGNet: Face Verification Using Sign Pattern Matching](https://www.reddit.com/r/MachineLearning/comments/1urxvxh/i_built_imgnet_a_face_verification_model_that/) ⭐️ 8.0/10

IMGNet replaces cosine similarity with sliding window sign pattern matching for face verification, achieving 96.27% on LFW with a 10.58 MB model trained on CASIA-WebFace. When applied to ArcFace embeddings without retraining, it achieves 99.58% on LFW. This work challenges the default use of cosine similarity in metric learning, showing that sign-based pattern matching can achieve competitive results with a compact model. It also suggests that sign pattern consistency is a fundamental property of well-trained face embeddings. IMGNet introduces several innovations: the SW Block that replaces standard convolution with multi-scale relational operations, the IMG Sign MSE Loss defined purely over sign pattern agreement, and a voting system with three metrics sharing one threshold. The model is only 10.58 MB in FP32 and was trained on 490k images from CASIA-WebFace.

reddit · r/MachineLearning · /u/img-_- · Jul 9, 18:00

**Background**: Face verification determines whether two face images belong to the same person. Traditional approaches use deep neural networks to extract embedding vectors and then compare them using cosine similarity or Euclidean distance. The Labeled Faces in the Wild (LFW) dataset is a standard benchmark for face verification, containing over 13,000 images of faces.

**Tags**: `#face verification`, `#deep learning`, `#metric learning`, `#sign pattern matching`, `#LFW`

---

<a id="item-8"></a>
## [Ant Open-Sources World's First MoE Embodied Video Model](https://www.qbitai.com/2026/07/446458.html) ⭐️ 8.0/10

Ant Group's LingBot-Video, the world's first embodied video generation model based on Mixture-of-Experts (MoE) architecture, has been open-sourced under the Apache 2.0 license. The model has 30B total parameters but activates only ~3B per inference, achieving 3x efficiency over dense models and scoring 0.620 on the RBench benchmark, surpassing Wan2.6, Seedance1.5 Pro, and Cosmos3 Super. This release marks a significant milestone in embodied AI by providing an efficient, open-source foundation model for generating robot-centric videos. It can accelerate robotics research in action prediction, simulation data generation, and world modeling, potentially lowering barriers for both academia and industry. LingBot-Video employs a DiT (Diffusion Transformer) backbone with MoE layers, and was trained on 70,000 hours of embodied data covering dexterous manipulation, robot locomotion, and first-person interactions. It also incorporates a multi-dimensional reinforcement learning reward system focusing on physics plausibility and task completion beyond aesthetics and motion consistency.

telegram · zaihuapd · Jul 9, 04:30

**Background**: Embodied AI refers to artificial intelligence systems that are embedded in a physical body, perceiving and acting within an environment, with cognition shaped by bodily interactions. Mixture-of-Experts (MoE) is a neural network architecture where only a subset of parameters (experts) are activated per input, enabling high capacity with lower computational cost. Video generation models for robotics, often termed 'world models,' aim to simulate future frames conditioned on actions, aiding planning and policy learning.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Embodied_artificial_intelligence">Embodied artificial intelligence</a></li>

</ul>
</details>

**Tags**: `#MoE`, `#embodied AI`, `#video generation`, `#open-source model`, `#robotics`

---

<a id="item-9"></a>
## [DJI EV50 Drone Breaks Altitude Record over Everest](https://www.163.com/dy/article/L1CUCV940514R9OJ.html) ⭐️ 8.0/10

DJI's unreleased EV50 VTOL cargo drone flew over Mount Everest at 8,861 meters, setting a world record for highest flight altitude among VTOL cargo drones and collecting atmospheric data above 8,000 meters. This achievement demonstrates the potential for high-altitude logistics and scientific research, showcasing DJI's advanced drone capabilities that could revolutionize cargo delivery in challenging terrains. The EV50 is a hybrid-wing drone that can vertically take off and land, then transition to fixed-wing cruise. During the 12-day mission, it completed 32 sorties, climbed 3,730 meters continuously, and still had 30% battery remaining on return.

telegram · zaihuapd · Jul 9, 06:00

**Background**: VTOL (Vertical Take-Off and Landing) drones combine the convenience of helicopter-like takeoff with the efficiency of fixed-wing flight. High-altitude operations like this one test drone performance in thin air and extreme cold, critical for future logistics in mountainous regions.

**Tags**: `#DJI`, `#Drone`, `#Everest`, `#UAV`, `#Logistics`

---

<a id="item-10"></a>
## [China's Supercomputing Core Node Online with 100K+ AI Cards](https://36kr.com/newsflashes/3887797387344387) ⭐️ 8.0/10

China's national supercomputing internet core node in Zhengzhou officially launched on July 9, 2026, providing over 100,000 domestic AI computing cards. This milestone significantly boosts China's AI computing capacity and demonstrates progress in reducing reliance on foreign GPUs. It enables efficient resource sharing and coordinated computing across the nation. The node acts as a central hub for operation management and resource scheduling, integrating services such as supply-demand matching and industry incubation.

telegram · zaihuapd · Jul 9, 07:00

**Background**: The National Supercomputing Internet is a project to link supercomputing centers across China, providing unified computing services. The use of domestic AI computing cards is part of China's push for self-sufficiency in semiconductors and AI hardware.

**Tags**: `#AI`, `#supercomputing`, `#domestic computing`, `#infrastructure`, `#China`

---