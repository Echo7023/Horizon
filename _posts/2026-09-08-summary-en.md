---
layout: default
title: "Horizon Summary: 2026-09-08 (EN)"
date: 2026-09-08
lang: en
---

> From 30 items, 18 important content pieces were selected

---

1. [LLM-guided program evolution breaks 10 Packomania circle-packing records](#item-1) ⭐️ 9.0/10
2. [Huawei's Kirin 9050 Pro debuts logic-folding in Mate XT 2](#item-2) ⭐️ 9.0/10
3. [LG Smart TVs Caught Logging Audio and Scanning Local Networks](#item-3) ⭐️ 8.0/10
4. [OpenAI reveals how coding agents and RSI accelerate research toward AGI](#item-4) ⭐️ 8.0/10
5. [KV Cache as an Agent Runtime: A New Path to Interactive LLMs](#item-5) ⭐️ 8.0/10
6. [Study of 31,352 LLM Benchmark Runs Finds Significant Daily Performance Drift](#item-6) ⭐️ 8.0/10
7. [China's Top Court Sets AI Liability Rules for Deepfakes and Algorithmic Pricing](#item-7) ⭐️ 8.0/10
8. [Caltech Mathathon: First Research-Level Math Hackathon Focused on Responsible AI](#item-8) ⭐️ 7.0/10
9. [TPU Inference Externalization Accelerates, Eroding Nvidia's CUDA Moat](#item-9) ⭐️ 7.0/10
10. [China's MIIT Plan Calls for Timely 6G Commercial Rollout](#item-10) ⭐️ 7.0/10
11. [bzip3 Compressor Sparks Debate Over Benchmark Methodology](#item-11) ⭐️ 6.0/10
12. [Internet Archive Urges Recurring Donations with 3x September Match](#item-12) ⭐️ 6.0/10
13. [Leaked 2003 Emails Show Bill Gates Struggling to Install Movie Maker](#item-13) ⭐️ 6.0/10
14. [Rustuna: High-Performance Rust Implementation of Optuna Released](#item-14) ⭐️ 6.0/10
15. [PINNStudio: Free Open-Source No-Code GUI for Physics-Informed Neural Networks](#item-15) ⭐️ 6.0/10
16. [Apple Overhauls EU App Store Fees with 5% Core Technology Commission](#item-16) ⭐️ 6.0/10
17. [First China Office-Agent Report: Top 20% of Users Consume 87.4% of Compute](#item-17) ⭐️ 6.0/10
18. [ChatGPT's rise devastates Nairobi's essay ghostwriting industry, up to 40,000 workers affected](#item-18) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [LLM-guided program evolution breaks 10 Packomania circle-packing records](https://www.reddit.com/r/MachineLearning/comments/1w9xlyi/llmguided_program_evolution_improves_10_bestknown/) ⭐️ 9.0/10

Researchers used an LLM to iteratively evolve an optimization program rather than directly solve circle-packing instances. On the Packomania csqv benchmark, their Discovery Loop system improved the best-known sum-of-radii for 10 values of N between 101 and 114, by 2.4–5.4%, in 15 iterations at a total LLM cost of $27.72; Packomania independently accepted the results. This result shows that LLM-driven program evolution can meaningfully advance a recognized mathematical optimization benchmark for under $30. It points toward a broader shift in which foundation models help discover novel algorithms, not just optimize prompts or code snippets. The system starts from a simple seed solver; the LLM proposes algorithm changes guided by a scoreboard of results and prior attempt history, and each candidate is scored by an independent verifier so only improvements are kept. The paper (arXiv:2609.05093) also invites scrutiny of its plateau-detection stopping rule, which the author identifies as the most fragile component.

reddit · r/MachineLearning · /u/SIGH_I_CALL · Sep 7, 16:54

**Background**: Circle packing in a square asks how to place circles without overlaps to maximize some objective; the csqv variant on Packomania seeks the maximum sum of radii for N variable-sized circles in the unit square. This is a notoriously difficult non-convex optimization problem with many local optima. Packomania maintains a list of best-known packings, and algorithms have traditionally relied on hand-designed heuristics or numerical optimization. LLM-guided evolutionary search instead repeatedly asks a language model to mutate solver code, evaluates variants, and keeps successful ones, an approach inspired by systems such as AlphaEvolve.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.05093">[2609.05093] LLM-Guided Program Evolution for Circle Packing: Breaking 10 Packomania Records for $28</a></li>
<li><a href="https://arxiv.org/html/2609.05093">LLM-Guided Program Evolution for Circle Packing:Breaking 10 Packomania Records for $28</a></li>
<li><a href="https://packomania.com/csqv/csqv.html">The best known packings of unequal circles in a square</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#program evolution`, `#optimization`, `#circle packing`, `#AI research`

---

<a id="item-2"></a>
## [Huawei's Kirin 9050 Pro debuts logic-folding in Mate XT 2](https://www.news.cn/20260907/adf46c5c003240d28cc3cf6de54f9b5f/c.html) ⭐️ 9.0/10

Huawei unveiled the Mate XT 2 triple-folding phone in Guangzhou, powered by the new Kirin 9050 Pro. This is Huawei's first flagship-grade Kirin chip since the Mate 40 era, and the first high-performance chip to feature logic-folding. Logic folding stacks transistors vertically, so Huawei may be able to keep improving performance and density without access to the most advanced lithography tools. If the chip performs as claimed, it could reshape the high-end smartphone market and accelerate alternatives to Moore's Law. The Kirin 9050 Pro's logic-folding design stacks logic units in vertical layers inside a single die and adds vertical interconnect channels—compared by Huawei to an elevator in a multi-story building—to shorten signal paths and lower latency. Huawei calls it a multi-level co-optimization of systems, chips, devices, and circuits; independent reports claim a 53% transistor-density gain for AI workloads, but official specifications and independent verification remain limited.

telegram · zaihuapd · Sep 7, 08:20

**Background**: Conventional chip scaling follows Moore's Law, squeezing more transistors onto flat silicon wafers, a process that increasingly relies on advanced lithography and faces physical limits. Logic folding instead builds circuits in the vertical dimension, with vertical interconnect channels that shorten wiring distances and reduce resistance-capacitance delay. This approach aims to boost density and performance without shrinking transistors further, effectively bypassing Moore's Law.

<details><summary>References</summary>
<ul>
<li><a href="https://www.geeky-gadgets.com/huawei-logic-folding-moores-law/">Huawei Logic Folding: A New Approach to Moore's Law - Geeky ...</a></li>
<li><a href="https://www.huaweicentral.com/huawei-logicfolding-architecture-everything-you-need-to-know/">Huawei LogicFolding Architecture: Everything you need to know</a></li>
<li><a href="https://skynexttech.com/huawei-logic-folding-chip-breakthrough/">Huawei Logic Folding Breakthrough Could Rewrite the Future of ...</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#semiconductor`, `#chip-design`, `#Kirin`, `#technology`

---

<a id="item-3"></a>
## [LG Smart TVs Caught Logging Audio and Scanning Local Networks](https://www.youtube.com/watch?v=6IFVTcM28KA) ⭐️ 8.0/10

An investigation by Gamers Nexus, Level1Techs, and independent researchers found that LG smart TVs running webOS log voice prompts and other audio in plain text even when the screen is off, and actively scan local networks to map nearby devices such as phones and smartwatches. The behavior affects millions of LG TVs, including the G5 OLED. With over 216 million LG smart TVs in use, this effectively turns living rooms into potential surveillance environments and deeply undermines user trust in connected appliances. It also highlights the broader industry problem of consumers having little control over data-hungry features embedded in smart devices. The TV logs captured audio in plain text and uploads data when network conditions allow, and it performs network scanning even in standby mode. LG's terms reportedly require owners to notify household members and guests that their voices may be captured and processed, exposing users to contractual surveillance obligations.

hackernews · treve · Sep 7, 00:22 · [Discussion](https://news.ycombinator.com/item?id=49592375)

**Background**: Modern smart TVs run full operating systems such as LG's webOS, enabling streaming apps, voice assistants, and automatic content recognition. Unlike phones or computers, a TV is a shared living-room device that is often always on and equipped with always-listening microphones, so tracking behavior can expose the private activities of everyone in the home. Prior research by RTINGS and others showed smart TVs collect viewing data, but the new findings reveal more invasive actions: capturing audio in standby and mapping the entire local network. This type of network scanning lets the TV build a profile of connected devices, effectively turning the home network into a surveillance target.

<details><summary>References</summary>
<ul>
<li><a href="https://www.notebookcheck.net/LG-smart-TVs-caught-logging-audio-with-screen-off-and-snooping-on-local-devices.1391214.0.html">LG smart TVs caught logging audio with screen off and snooping on...</a></li>
<li><a href="https://news.ycombinator.com/item?id=49594878">LG smart TVs caught logging audio with screen off ... | Hacker News</a></li>
<li><a href="https://cyberinsider.com/lg-smart-tvs-found-scanning-home-networks-for-nearby-devices/">LG Smart TVs found scanning home networks for nearby devices</a></li>

</ul>
</details>

**Discussion**: Commenters expressed outrage and a sense of vindication, with several noting they were ridiculed for disabling smart-TV networking features and now feel justified. Others highlighted LG's restrictive contract terms that require users to inform everyone near the TV of possible eavesdropping, while some lamented the scarcity of 'dumb' TVs and privacy-focused streaming boxes. Overall sentiment is highly critical of LG and of the broader industry trend toward surveillance-driven business models.

**Tags**: `#privacy`, `#smart-tv`, `#surveillance`, `#security`, `#lg`

---

<a id="item-4"></a>
## [OpenAI reveals how coding agents and RSI accelerate research toward AGI](https://simonwillison.net/2026/Sep/6/research-acceleration-the-view-inside-openai/) ⭐️ 8.0/10

Simon Willison reports on OpenAI's new 'Research acceleration: The view inside OpenAI' post, which reveals how coding agents are reshaping OpenAI researchers' daily work. Median daily AI spend per researcher went from near zero in February 2026 to roughly $600 by late August 2026. It is significant because it gives an unusually candid look at OpenAI's internal agentic engineering practices and ties them to Recursive Self-Improvement as part of the company's path toward AGI. As 2026 becomes the year agentic engineering took off, this suggests AI research itself is being accelerated by the same tools researchers help create. Willison notes that the acronym 'RSI' is used without being expanded, and he guesses the steep climb in per-researcher spend starting in late July corresponds to internal access to the model later released as GPT-6 Astra. The report accompanies a separate essay by Chief Scientist Jakub Pachocki titled 'An Alien Mind.'

rss · Simon Willison · Sep 6, 23:57

**Background**: Coding agents are AI tools that can independently write, debug, and refactor code; in 2026, agentic engineering — developing software by directing these agents — became a mainstream practice across the industry. Recursive Self-Improvement refers to AI systems helping to improve themselves, a concept closely tied to faster progress on OpenAI's AGI roadmap.

<details><summary>References</summary>
<ul>
<li><a href="https://datasciencedojo.com/blog/recursive-self-improvement-agentic-ai/">Recursive Self - Improvement in Agentic AI (2026 Guide)</a></li>
<li><a href="https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/">What is agentic engineering? - Agentic Engineering Patterns - Simon Willison's Weblog</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-engineering">What is Agentic Engineering? | IBM</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#coding agents`, `#AI research`, `#agentic engineering`, `#RSI`

---

<a id="item-5"></a>
## [KV Cache as an Agent Runtime: A New Path to Interactive LLMs](https://www.reddit.com/r/MachineLearning/comments/1w9myqc/kv_cache_as_an_agent_runtime_r/) ⭐️ 8.0/10

Researchers at Yandex propose treating the KV cache as an agent runtime, modifying the model's inference state to create more interactive LLMs. The idea builds on their earlier Hogwild! Inference and AsyncReasoning work and previews a Qwen3.8-27B agent playing DOOM interactively. This reframes inference and runtime design as an under-explored axis of agent capability, distinct from both the model weights and the outer harness. If successful, it could enable agents that respond and adapt in real time without costly retraining, benefiting interactive systems such as voice assistants and embodied agents. Hogwild! Inference runs multiple LLM instances in parallel on the same attention cache using Rotary Position Embeddings (RoPE), while AsyncReasoning processes multiple token streams concurrently without additional training. The blog post previews future work, not a fully released demo, where a Qwen3.8-27B model controls an agent playing DOOM.

reddit · r/MachineLearning · /u/_puhsu · Sep 7, 09:03

**Background**: A KV cache stores the key and value tensors computed for previous tokens, letting an LLM generate each new token without recomputing the whole conversation. Standard inference is sequential: a model must finish its current response before handling new input, which limits interactivity. This line of research modifies that inference state so reasoning, output, and new inputs can overlap, suggesting the runtime itself can serve as a substrate for LLM agents.

<details><summary>References</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms">Understanding and Coding the KV Cache in LLMs from Scratch</a></li>
<li><a href="https://arxiv.org/html/2504.06261v1">Hogwild! Inference: Parallel LLM Generation via Concurrent ...</a></li>
<li><a href="https://arxiv.org/abs/2512.10931">[2512.10931] Asynchronous Reasoning: Training-Free ... GitHub - yandex-research/AsyncReasoning Asynchronous Reasoning in LLMs | PDF | Thought | Computing (PDF) Asynchronous Reasoning: Training-Free Interactive ... Architecting Asynchronous Inference Engines for Real‑Time ... Async LLM Inference Patterns That Scale - Medium</a></li>

</ul>
</details>

**Tags**: `#KV cache`, `#LLM agents`, `#interactive inference`, `#systems for ML`, `#agent runtime`

---

<a id="item-6"></a>
## [Study of 31,352 LLM Benchmark Runs Finds Significant Daily Performance Drift](https://www.reddit.com/r/MachineLearning/comments/1w9llr4/measuring_llm_performance_drift_observations_and/) ⭐️ 8.0/10

A large-scale study analyzed 31,352 repeated benchmark measurements across 49 models and found that between-day median scores vary about three times as much as within-day variability (standard deviations 8.43 vs. 2.80 points). The authors propose a longitudinal benchmarking methodology that tracks model behavior over time rather than relying on snapshot leaderboard scores. Because API-served models can change behavior without version releases, static benchmark scores can mislead model selection and monitoring. This work underscores the need for continuous drift detection as LLM evaluation becomes a production reliability concern. Within-day score standard deviation was 2.80 points, while the standard deviation of between-day daily medians was 8.43 points, a roughly 3:1 ratio. The authors use versioned benchmark configurations, repeated execution-based evaluation, separate availability failure tracking, and deliberately withhold the full live task bank to reduce contamination.

reddit · r/MachineLearning · /u/ionutvi · Sep 7, 07:44

**Background**: LLM benchmark scores are commonly treated as stable properties of model names, but commercial models are often accessed via APIs whose underlying weights, infrastructure, and provider configurations can change over time. This can cause genuine performance drift that looks like ordinary noise. Related work, such as longitudinal datasets like HAPI and studies like ReasonBENCH, has shown that LLM behavior can vary considerably across repeated runs and over time.

<details><summary>References</summary>
<ul>
<li><a href="https://www.logicmonitor.com/blog/llms-dont-stand-still-how-to-monitor-and-trust-the-models-powering-your-ai">How to Monitor and Trust the LLMs Powering Your AI | LogicMonitor</a></li>
<li><a href="https://people.eecs.berkeley.edu/~matei/papers/2022/neurips_hapi.pdf">HAPI: A Large-scale Longitudinal Dataset of Commercial ML API Predictions</a></li>
<li><a href="https://arxiv.org/html/2512.07795v1">ReasonBENCH: Benchmarking the (In)Stability of LLM Reasoning</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#benchmarking`, `#performance drift`, `#evaluation methodology`, `#API models`

---

<a id="item-7"></a>
## [China's Top Court Sets AI Liability Rules for Deepfakes and Algorithmic Pricing](https://www.cnr.cn/news/20260907/t20260907_527806795.shtml) ⭐️ 8.0/10

On September 7, the Supreme People's Court issued a 24-article judicial interpretation clarifying legal liability for AI-related disputes. It states that using AI to create recognizable faces or voices without consent may constitute personality rights infringement, and algorithmic price discrimination can trigger legal responsibility. This interpretation gives Chinese courts concrete legal grounds to rule on AI-driven harms, directly affecting AI developers, platform operators, and consumers. It marks an important step in AI regulation by setting clearer compliance expectations for the industry. The interpretation consists of five parts and 24 articles, covering AI deepfakes, algorithmic price discrimination, AI impersonation in endorsements, autonomous driving, and intellectual property. It also regulates AI-assisted 'network open box' (doxxing) and privacy violations, and supports punitive damages where AI impersonation induces consumer spending.

telegram · zaihuapd · Sep 7, 09:32

**Background**: Algorithmic price discrimination, commonly called 'big data killing familiarity,' refers to platforms using personal data to charge different prices to different users, a practice China's laws prohibit as unreasonable differential treatment. 'Network open box' (kai he) is a type of doxxing where offenders illegally obtain and publicly expose private information such as names, addresses, and phone numbers. This judicial interpretation builds on existing laws like the Personal Information Protection Law, helping translate them into enforceable rules for AI cases.

<details><summary>References</summary>
<ul>
<li><a href="https://baike.baidu.com/item/网络开盒/67437911">网络开盒 - 百度百科</a></li>
<li><a href="https://m.thepaper.cn/newsDetail_forward_29760319">鲍翔 文学国｜大数据杀熟的法律性质与责任分析</a></li>
<li><a href="http://www.shfzb.com.cn/shfzb/html/2024-12/18/content_150505_1652847.htm">上海法治报数字报-禁止“利用算法杀熟”，监管如何破局</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#deepfakes`, `#algorithmic pricing`, `#law`, `#China`

---

<a id="item-8"></a>
## [Caltech Mathathon: First Research-Level Math Hackathon Focused on Responsible AI](https://mathathonchallenge.com/index.html) ⭐️ 7.0/10

Caltech undergraduates are organizing the Caltech Mathathon, described as the first hackathon ever devoted to research-level mathematics. The event emphasizes responsible AI use and is open to teams applying for participation. It combines two emerging trends — AI-assisted discovery and research-level math — in a novel competition format. The outcome could offer insight into whether LLMs can make meaningful progress on open mathematical questions in a short, intense setting. The organizers are Caltech undergrads acting independently, not representing Caltech or sponsors, and receive no monetary compensation; raised funds go to judges and participants. The FAQ page outlines their responsible-AI commitments.

hackernews · astroanax · Sep 7, 09:26 · [Discussion](https://news.ycombinator.com/item?id=49596055)

**Background**: Hackathons are typically fast-paced events where teams build software prototypes in a few days. This hackathon instead asks participants to use AI tools to tackle research-level mathematical problems, reflecting growing interest in using large language models for mathematical reasoning.

**Discussion**: Commenters were generally intrigued but skeptical: one asked whether waiting 40 hours on an LLM matches the classic hackathon appeal, while an organizer emphasized that the goal is to promote responsible AI use and help students gain ML recognition outside Caltech's weak CS program. One applicant said they hope the event serves as a test bed for building reasoning-maximizing harnesses for LLMs.

**Tags**: `#AI`, `#mathematics`, `#hackathon`, `#Caltech`, `#research`

---

<a id="item-9"></a>
## [TPU Inference Externalization Accelerates, Eroding Nvidia's CUDA Moat](https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam) ⭐️ 7.0/10

A new SemiAnalysis report says Google's TPU inference externalization is moving full steam ahead, with InferenceX benchmarks showing up to 50% better performance per dollar. The report also highlights a growing customer base and the upcoming Ironwood TPU (referred to as TPUv8i) as forces that will push this trend further. Nvidia's CUDA software ecosystem has long acted as a lock-in, so a credible non-Nvidia inference path with better price/performance threatens that advantage. If Google's TPU stack keeps expanding outside internal use, Google Cloud could capture more AI inference workloads and intensify competition in AI infrastructure. InferenceX is SemiAnalysis's open benchmark for AI inference across chips and serving stacks, including fixed-sequence and agentic long-context coding scenarios. The report emphasizes both a rapidly externalized TPU software stack and growing customer adoption, with Ironwood built specifically for the age of inference as the next catalyst.

rss · Semianalysis · Sep 7, 20:00

**Background**: TPUs are Google's custom tensor processing chips for AI workloads; for years they mainly powered Google's internal services before being offered more broadly on Google Cloud. SemiAnalysis's InferenceX measures both conventional and agentic inference, making TPU versus GPU comparisons more visible. The CUDA moat refers to Nvidia's extensive, mature software ecosystem that keeps developers tied to its GPUs. Ironwood is Google's newest TPU generation, designed specifically for AI inference.

<details><summary>References</summary>
<ul>
<li><a href="https://inferencex.semianalysis.com/about">About | InferenceX by SemiAnalysis</a></li>
<li><a href="https://blog.google/innovation-and-ai/infrastructure-and-cloud/google-cloud/ironwood-tpu-age-of-inference/">Ironwood : The first Google TPU for the age of inference</a></li>
<li><a href="https://multigrid.ai/learn/cuda-moat">CUDA and the Software Moat : What It Is Actually Made Of · Multigrid</a></li>

</ul>
</details>

**Tags**: `#AI hardware`, `#TPU`, `#Google Cloud`, `#Inference`, `#CUDA`

---

<a id="item-10"></a>
## [China's MIIT Plan Calls for Timely 6G Commercial Rollout](https://36kr.com/newsflashes/3973030022541575) ⭐️ 7.0/10

China's Ministry of Industry and Information Technology (MIIT) issued the '15th Five-Year Plan for the Information and Communication Industry', which calls for the timely launch of 6G commercialization, orderly deployment of eSIM and network-free communication technologies, and expansion of 5G-Advanced (5G-A) coverage. This high-level policy roadmap sets the direction for China's telecom industry over the next five years, influencing equipment makers, operators, and device vendors. Timely 6G commercialization and new technology adoption will shape global competition in next-generation communications. The plan calls for 'dual 10G' evolution in urban and hotspot areas, 5G-A continuous coverage in county-level urban areas and extension to key towns, with 10G downlink and 1G uplink peak rates in hotspot areas. It also requires establishing domestic rules for satellite internet equipment networking and organizing field trials of next-generation mobile smart terminals.

telegram · zaihuapd · Sep 7, 07:58

**Background**: 5G-A (5G-Advanced) is an enhanced evolution of 5G that works alongside 5G to support higher-rate, lower-latency applications such as 3D, cloud, IoT, and sensing-communication integration. 'Network-free communication' (无网通信) refers to direct device-to-device (D2D) communication that works without cellular base stations, a capability recently showcased in devices like the Huawei Mate 80's 700MHz emergency network-free feature. 'Dual 10G' refers to both 5G-A wireless and F5G-A wired optical network capabilities approaching 10 Gbps.

<details><summary>References</summary>
<ul>
<li><a href="https://www.iot101.com/mobile/news/10119.html">被华为Mate 80带火的“ 无 网 通 信 ” 是 什 么</a></li>
<li><a href="https://baike.baidu.com/item/5G-A/63815414">5G-A_百度百科</a></li>
<li><a href="https://www.cww.net.cn/article?id=140048A6C42D41319C6FB0EF88F673ED">北京移动启动“ 双 万 兆 ”计划 将建设1000个 万 兆 社区_ 通 信 世界网</a></li>

</ul>
</details>

**Tags**: `#6G`, `#telecom policy`, `#eSIM`, `#5G-A`, `#China`

---

<a id="item-11"></a>
## [bzip3 Compressor Sparks Debate Over Benchmark Methodology](https://github.com/iczelia/bzip3) ⭐️ 6.0/10

bzip3, an open-source compressor designed as a spiritual successor to bzip2, is drawing attention for claiming higher compression ratios and faster decompression via a modernized Burrows-Wheeler transform. Community reviewers have begun challenging the official benchmark charts, noting that bzip3 is tested with a 512 MiB block size while zstd's window size is left at its default of roughly 8 MiB. Compression tool choices directly affect storage costs, archival workloads, and software interoperability, so credible benchmarks matter to users. The debate also illustrates how BWT-based compressors can exploit long-range redundancy in source-code corpora, and how zstd with a sufficiently large window may close that perceived gap. bzip3 is not backward compatible with bzip2; it combines a suffix-array-based fast BWT, an LZP (Lempel-Ziv + Prediction) pass, and an order-0 context-mixing entropy coder. Its speed depends heavily on the compiler and platform, with Windows and 32-bit builds often being considerably slower than optimized x64 Linux clang builds.

hackernews · tosh · Sep 7, 13:35 · [Discussion](https://news.ycombinator.com/item?id=49598291)

**Background**: bzip2, first released in 1996, compresses data by applying the Burrows-Wheeler transform (BWT), move-to-front transform, and Huffman coding to 100-900 kB blocks; it is especially effective on text and source code but slower than gzip and modern codecs. bzip3 modernizes that concept by using suffix arrays to calculate the BWT, adding an LZP pre-pass, and employing context mixing for entropy coding, aiming for better ratios and faster decompression. General-purpose compressors such as zstd rely on LZ77-style matching and entropy coding, exposing a window-size parameter that controls how far back the compressor can search for repeated data.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bzip2">Bzip2</a></li>
<li><a href="https://github.com/ShawSumma/bzip-three-for-you-and-me">ShawSumma/bzip-three-for-you-and-me - GitHub BZip3: Compresses More, Decompresses Faster Than BZip2 bzip3 man - Linux Command Library Software:Bzip3 - HandWiki bzip3 - an efficient statistical file compressor and ...</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters generally welcome bzip3, with some linking to the author's detailed explanation of the Burrows-Wheeler transform and noting the tool's inclusion in the Large Text Compression Benchmark. The main criticism is that the benchmarks look disingenuous because bzip3 uses a 512 MiB block size while zstd's window is left at the default, and the corpus of concatenated Perl source versions is a best-case scenario for BWT compressors. Several users call for retesting zstd with larger windows and long-range mode, while others discuss practical archival trade-offs such as LZMA compressing JSONL better than gzip but lacking transparent support in common tools.

**Tags**: `#compression`, `#bzip3`, `#zstd`, `#benchmarks`, `#open-source`

---

<a id="item-12"></a>
## [Internet Archive Urges Recurring Donations with 3x September Match](https://blog.archive.org/2026/09/01/keep-our-servers-running-your-recurring-donation-goes-3x-this-september/) ⭐️ 6.0/10

In September 2026, the Internet Archive launched a fundraising appeal titled 'Keep Our Servers Running,' promising that recurring donations made during the month will be tripled (3x match). The campaign urges supporters to set up ongoing monthly contributions to help pay for the nonprofit's servers and digital preservation work. The Internet Archive is essential infrastructure for digital preservation, hosting billions of web pages, books, and media, and it relies on public support to stay operational. A 3x match, especially for recurring donations, can significantly boost the organization's predictable long-term funding, ultimately benefiting users of archive.org and Open Library. Commenters noted that the matching-gift scheme can be tied to 501(c)(3) public-support requirements: small donor contributions allow the charity to accept corresponding large matching gifts, with one commenter describing a 1:2 match ratio. They also raised practical concerns, such as difficulty canceling recurring donations without manual email requests, a lack of EU-based donation receipt options, and persistent technical problems like an email-address leak in the collection upload system and Solr performance issues on Open Library.

hackernews · sonicrocketman · Sep 7, 03:29 · [Discussion](https://news.ycombinator.com/item?id=49593563)

**Background**: The Internet Archive is a nonprofit digital library that provides free access to archived websites, books, audio, and software, including the well-known Wayback Machine. Open Library, a project of the Internet Archive, is an editable online catalog aiming to create a web page for every book ever published and currently offers more than 3 million books to read, borrow, and discover. As a nonprofit, the Internet Archive depends on public donations and grants; this September campaign leverages a matching pledge to multiply recurring donations.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open_Library">Open Library</a></li>
<li><a href="https://openlibrary.org/">Welcome to Open Library | Open Library</a></li>

</ul>
</details>

**Discussion**: Commenters overall expressed support for the Internet Archive and many donate regularly, but they also voiced concerns about cancellation difficulties, a lack of EU donation receipt options, and ongoing technical problems that undermine trust. One long-time Open Library volunteer encouraged experienced professionals to volunteer, noting that help is needed with Solr performance and other projects. Another commenter clarified that the matching scheme is tied to 501(c)(3) 'public support' rules, making the matching real even though the mechanics are indirect.

**Tags**: `#Internet Archive`, `#digital preservation`, `#fundraising`, `#open library`, `#non-profit`

---

<a id="item-13"></a>
## [Leaked 2003 Emails Show Bill Gates Struggling to Install Movie Maker](https://www.techemails.com/p/bill-gates-tries-to-install-movie-maker) ⭐️ 6.0/10

A leaked 2003 email chain published by TechEmails shows Bill Gates repeatedly failing to install Windows Movie Maker, sparking an internal discussion that exposed deep usability problems and blame-shifting among Microsoft executives. This anecdote matters because even Microsoft's top executive could not successfully use his own company's product, illustrating systemic design and organizational failures. It reinforces long-standing external criticism of Microsoft's usability issues and internal silos, and it remains relevant to discussions about accountability in tech companies. In the email chain, executives deflect blame and propose forming committees instead of directly fixing the underlying problem. Community commenters read this as a sign of zero ownership, zero accountability, and zero consequences, which they argue is how great products die.

hackernews · highfrequency · Sep 7, 15:27 · [Discussion](https://news.ycombinator.com/item?id=49599481)

**Background**: Windows Movie Maker was Microsoft's consumer video-editing application for Windows desktop PCs. It was widely appreciated for its simplicity and accessibility, but it is now outdated, unsupported, and no longer safe to download. Microsoft officially discontinued Movie Maker in 2017 and replaced it with the Video Editor formerly known as Microsoft Story Remix.

<details><summary>References</summary>
<ul>
<li><a href="https://www.movavi.com/windows-movie-maker-review.html">Windows Movie Maker Review 2026 – Pros and Cons, Pricing</a></li>
<li><a href="https://www.anymp4.com/video-editing/windows-movie-maker-review.html">A Comprehensive Windows Movie Maker Review in 2026</a></li>
<li><a href="https://www.wikihow.com/Use-Windows-Movie-Maker">How to Download & Use Windows Movie Maker on any PC</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters largely view the email chain as evidence of zero accountability, with executives passing the buck and creating committees instead of owning problems. Some extend the critique to today's Microsoft, citing frustrating Azure experiences, while others argue Gates himself bore ultimate responsibility and note the irony that one executive in the thread later became a TikTok lobbyist.

**Tags**: `#Microsoft`, `#design`, `#usability`, `#tech-culture`, `#email-history`

---

<a id="item-14"></a>
## [Rustuna: High-Performance Rust Implementation of Optuna Released](https://www.reddit.com/r/MachineLearning/comments/1w9nyhz/rustuna_a_highperformance_rust_implementation_of/) ⭐️ 6.0/10

The Optuna team released Rustuna, a high-speed, memory-efficient implementation of Optuna built natively in Rust. It keeps the familiar Optuna API and concept while eliminating Python dependencies to reduce supply chain risks. This release brings Rust's performance and security advantages to the hyperparameter optimization ecosystem, potentially enabling more efficient and safer ML infrastructure. It is especially relevant for users who want to embed optimization in Rust-based systems or who are concerned about Python supply chain vulnerabilities. Rustuna is hosted on GitHub (github.com/optuna/rustuna) and was announced via a Medium blog post. It is designed as an Optuna-compatible reimplementation with optimized memory management in Rust, though the announcement does not include specific benchmark numbers or a detailed feature parity list.

reddit · r/MachineLearning · /u/c-bata · Sep 7, 10:01

**Background**: Optuna is an automatic hyperparameter optimization framework for machine learning, known for its define-by-run API that allows dynamic construction of search spaces. Hyperparameter optimization is the process of tuning model settings that are not learned from data. Rustuna is a reimplementation that keeps Optuna's interface and concept but is written in Rust to improve speed, memory efficiency, and supply chain security by avoiding Python dependencies.

<details><summary>References</summary>
<ul>
<li><a href="https://optuna.org/">Optuna - A hyperparameter optimization framework</a></li>
<li><a href="https://github.com/optuna/optuna">Optuna: A hyperparameter optimization framework - GitHub Optuna: A hyperparameter optimization framework — Optuna 4.9. ... Optuna: A hyperparameter optimization framework — Optuna 3.6. ... Optuna: A hyperparameter optimization framework - GitHub [1907.10902] Optuna: A Next-generation Hyperparameter ... Optuna | Proceedings of the 25th ACM SIGKDD International ...</a></li>

</ul>
</details>

**Tags**: `#Rust`, `#Hyperparameter Optimization`, `#Optuna`, `#Machine Learning Infrastructure`, `#Performance`

---

<a id="item-15"></a>
## [PINNStudio: Free Open-Source No-Code GUI for Physics-Informed Neural Networks](https://www.reddit.com/r/MachineLearning/comments/1w9a2i7/pinnstudio_a_free_opensource_nocode_gui_for/) ⭐️ 6.0/10

A developer has released PINNStudio, a free and open-source no-code GUI that lets users define, train, and visualize physics-informed neural networks without writing boilerplate code. The tool automatically generates DeepXDE-based code, runs the model, and displays live loss curves and solution plots inside the app. This matters because it lowers the coding barrier for students and researchers in scientific machine learning, allowing them to focus on physics rather than implementation details. It could speed up experimentation with PINNs and help broaden their adoption beyond experienced programmers. Key features include PDE definitions and coupled multi-output PDE systems in 1D or 2D domains, boundary and initial conditions, custom network architectures and training schedules, as well as support for both forward and inverse problems. Built-in templates cover classic equations such as Heat, Allen-Cahn, and Cahn-Hilliard, and the package can be installed with pip install pinnstudio.

reddit · r/MachineLearning · /u/Impossible-Jello2749 · Sep 6, 22:19

**Background**: Physics-informed neural networks (PINNs) are neural networks trained to solve supervised learning tasks while respecting any given physical laws described by partial differential equations. By embedding physics knowledge as a regularizer, PINNs can generalize well even with low amounts of training data, which is valuable for engineering and biological problems where data is scarce. Scientific machine learning (SciML) combines domain science with machine learning, but traditionally setting up a new PINN problem requires writing code for PDEs, boundary conditions, architectures, and training schedules.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Physics-informed_neural_networks">Physics-informed neural networks</a></li>
<li><a href="https://www.sciencedirect.com/science/article/pii/S0021999118307125">Physics-informed neural networks: A deep learning framework ...</a></li>

</ul>
</details>

**Tags**: `#PINNs`, `#open-source`, `#scientific machine learning`, `#GUI`, `#deep learning`

---

<a id="item-16"></a>
## [Apple Overhauls EU App Store Fees with 5% Core Technology Commission](https://t.me/zaihuapd/43648) ⭐️ 6.0/10

Apple announced revised EU developer terms effective October 1, replacing the per-install Core Technology Fee with a 5% core technology commission on digital transactions in apps distributed outside the App Store. Apps using alternative payment links inside the App Store will pay a 20% commission, reduced to 10% for small business developers, and the initial acquisition fee and store services fee are removed. The change is part of Apple's effort to comply with the EU Digital Markets Act and follows European Commission scrutiny of its previous fee structure. It could materially lower costs for large developers distributing outside the App Store while preserving a commission on alternative payments. The 5% core technology commission applies specifically to digital transactions in apps distributed via alternative app marketplaces or the web, replacing the old per-install Core Technology Fee for developers that achieve extraordinary scale. The new terms eliminate the initial acquisition fee and store services fee, effective October 1.

telegram · zaihuapd · Sep 7, 02:24

**Background**: The EU Digital Markets Act (DMA) designates Apple and other large platforms as "gatekeepers" and requires them to allow alternative app stores and payment systems on iOS. Under Apple's previous EU terms, the Core Technology Fee was a per-install charge for developers reaching a very large scale, a structure that drew criticism. Apple says the new, simpler 5% commission reflects the value of its tools and services while better addressing DMA requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://www.apple.com/newsroom/2026/08/apple-announces-changes-for-apps-in-the-european-union/">Apple announces changes for apps in the European Union</a></li>
<li><a href="https://applemagazine.com/core-technology-fee-ends-five-percent-eu-commission/">Apple Ends Core Technology Fee With New 5% EU Commission ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/EU_Digital_Markets_Act">EU Digital Markets Act</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#EU`, `#App Store`, `#Developer Fees`, `#Digital Markets Act`

---

<a id="item-17"></a>
## [First China Office-Agent Report: Top 20% of Users Consume 87.4% of Compute](https://36kr.com/newsflashes/3972905839227142) ⭐️ 6.0/10

China's first informal report on office Agent user behavior, released today, reveals a pronounced 'head effect': the top 20% of users consume 87.4% of compute, and the top 5% alone account for 53.5% of token consumption. The data comes from real users of NetEase LobsterAI. This is one of the first data-driven portraits of how office AI agents are actually used, pointing to a power-law concentration where a small group of heavy users drives most compute and paid conversion. The findings give enterprise AI vendors practical signals for pricing, capacity planning, and feature design in the fast-growing agent market. Paying users show high stickiness: their token consumption, task volume, and monthly active days are 6.2x, 5.2x, and 3.0x those of free users, respectively, indicating heavy usage as the main driver for paid adoption. Additionally, the scale of a single task grew 3.1x over five months, with a 53% month-on-month increase in August.

telegram · zaihuapd · Sep 7, 06:18

**Background**: Office Agent products such as NetEase Youdao's LobsterAI are desktop-grade AI assistants built on the OpenClaw ecosystem; they can run tools on a real desktop and take remote commands from mobile devices via WeChat, Feishu, DingTalk, and Telegram, handling tasks like data analysis, slides, documents, video, and web research. Token consumption is the fundamental billing and usage unit for large language models, so the concentration of token usage indicates that a small group of heavy users generates most of the compute load. This 'incomplete report' is one of the first public data-driven snapshots of office Agent adoption in China, based on real user behavior rather than survey responses.

<details><summary>References</summary>
<ul>
<li><a href="https://lobsterai.youdao.com/">LobsterAI（有道龙虾）- 网易有道全场景办公助手 Agent</a></li>
<li><a href="https://github.com/netease-youdao/LobsterAI">GitHub - netease-youdao/LobsterAI: Open-source, desktop-grade ...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#user behavior`, `#enterprise AI`, `#compute usage`, `#China tech`

---

<a id="item-18"></a>
## [ChatGPT's rise devastates Nairobi's essay ghostwriting industry, up to 40,000 workers affected](https://the-decoder.com/how-ai-wiped-out-an-entire-industry-in-nairobi/) ⭐️ 6.0/10

A report from The Decoder reveals that ChatGPT has severely disrupted Nairobi's essay ghostwriting industry, which once employed at least 40,000 people writing papers mainly for overseas students at US and UK universities. Since ChatGPT's launch in 2022, order volumes and prices have plunged, and some workers have pivoted to making AI text evade detection. This shows concrete socio-economic disruption caused by generative AI in a global gig-economy niche, affecting tens of thousands of workers who depended on academic ghostwriting. It also highlights the emerging cat-and-mouse battle between AI text generation and AI detection, with implications for academic integrity and digital labor markets. The report says the ghostwriting work covered fields including medicine, computer science, and engineering. Some former ghostwriters now focus on 'humanizing' AI text or bypassing AI detectors, while other online gigs in Nairobi, such as transcription, data annotation, and content moderation, are also decreasing.

telegram · zaihuapd · Sep 7, 14:24

**Background**: ChatGPT, a generative AI chatbot that produces human-like text on demand, quickly became a cheap substitute for custom-written academic essays after its 2022 release. AI detection tools scan writing for signals such as low perplexity and burstiness, stylistic predictability, and word-probability patterns to identify machine-generated content. In response, AI humanizer tools rewrite AI text to make it appear more natural, which is why some ex-ghostwriters now offer to 'humanize' AI essays and beat anti-cheating software.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gptinf.com/blog/how-do-ai-detectors-work-understanding-the-methods-and-accuracy">How Do AI Detectors Work ? Understanding the Methods and Accuracy</a></li>
<li><a href="https://quillbot.com/ai-humanizer">Humanize AI Text: Free AI Humanizer by Quillbot</a></li>

</ul>
</details>

**Tags**: `#ChatGPT`, `#AI Impact`, `#Employment`, `#Kenya`, `#Academic Integrity`

---