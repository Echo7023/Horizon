---
layout: default
title: "Horizon Summary: 2026-07-09 (EN)"
date: 2026-07-09
lang: en
---

> From 40 items, 14 important content pieces were selected

---

1. [TypeScript 7.0 Announced with Rust Rewrite, 8-12x Speedup](#item-1) ⭐️ 9.0/10
2. [Bun Rewritten from Zig to Rust](#item-2) ⭐️ 9.0/10
3. [Mistral Releases Robostral Navigate, an 8B Robotics Model](#item-3) ⭐️ 8.0/10
4. [Grok 4.5 Launches with Cursor Data, Sparks Trust Debate](#item-4) ⭐️ 8.0/10
5. [OpenAI Launches GPT-Live Voice Mode with GPT-5.5 Delegation](#item-5) ⭐️ 8.0/10
6. [Cloudflare Meerkat: Leaderless Async Consensus](#item-6) ⭐️ 8.0/10
7. [EU Revives Chat Control 1.0, Scanning Non-E2EE Messages](#item-7) ⭐️ 8.0/10
8. [LingBot-Video: Open-Source Sparse-MoE Video Diffusion Transformer](#item-8) ⭐️ 8.0/10
9. [DeepSeek Develops Own AI Chip to Cut Nvidia, Huawei Dependence](#item-9) ⭐️ 8.0/10
10. [Alibaba Orders Employees to Uninstall Claude by July 10](#item-10) ⭐️ 8.0/10
11. [Huawei 5G Flagship Returns Overseas, Peak Speed Exceeds 1100 Mbps](#item-11) ⭐️ 8.0/10
12. [Critical Android Remote Root Exploit Chain Disclosed](#item-12) ⭐️ 8.0/10
13. [Meituan OWL Test Model Leaks User Conversations](#item-13) ⭐️ 8.0/10
14. [Researchers ID smartphone apps via EM signals with 99% accuracy](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [TypeScript 7.0 Announced with Rust Rewrite, 8-12x Speedup](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 9.0/10

Microsoft announced TypeScript 7.0, featuring a complete rewrite of the compiler in Rust, resulting in dramatic performance improvements of 8-12x (up to 11.9x on the VS Code codebase). The release also introduces new syntax features such as the `using` declaration and the `satisfies` operator. This major version leap dramatically reduces compilation times for large TypeScript codebases, making developer workflows significantly faster. The Rust rewrite also sets a new standard for compiler performance in the JavaScript ecosystem, potentially influencing future tooling decisions. Benchmarks show TypeScript 7.0 compiles the VS Code codebase in 10.6 seconds versus 125.7 seconds in TypeScript 6.0, an 11.9x speedup. The new `using` declaration provides deterministic resource management, and the `satisfies` operator enables more precise type checking without changing the inferred type.

hackernews · DanRosenwasser · Jul 8, 16:06 · [Discussion](https://news.ycombinator.com/item?id=48833715)

**Background**: TypeScript is a typed superset of JavaScript that compiles to plain JavaScript, widely used for large-scale applications. Its original compiler was written in TypeScript itself, which led to performance bottlenecks on large codebases. Rust is a systems programming language known for its performance and memory safety, making it an ideal choice for a compiler rewrite.

<details><summary>References</summary>
<ul>
<li><a href="https://dev.to/amarjit_yadav/typescript-7-whats-new-and-exciting-4d26">TypeScript 7: What's New and Exciting? - DEV Community</a></li>
<li><a href="https://www.blog.brightcoding.dev/2025/03/22/exploring-typescript-7-new-features-and-enhancements/">Exploring TypeScript 7: New Features and Enhancements - BrightCoding</a></li>

</ul>
</details>

**Discussion**: The community response is overwhelmingly positive, with users celebrating the massive speed improvements and the team's engineering feat. Some users expressed appreciation for continued JSDoc support and new syntax features, while others reflected on TypeScript's role in popularizing types in JavaScript.

**Tags**: `#TypeScript`, `#programming languages`, `#performance`, `#compiler`, `#Rust`

---

<a id="item-2"></a>
## [Bun Rewritten from Zig to Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/#atom-everything) ⭐️ 9.0/10

Jarred Sumner announced that Bun, the JavaScript runtime, has been rewritten from Zig to Rust, with the rewrite completed in 11 days using AI coding agents. The new Rust-based Bun is now live in Claude Code since June 17, 2026. This rewrite significantly improves Bun's stability by eliminating memory bugs like use-after-free and double-free, which were common in the Zig version. It also demonstrates that large-scale rewrites are now feasible with AI assistance, challenging the long-held belief that rewrites should never be attempted. The rewrite cost approximately $165,000 in API tokens (5.9 billion input, 690 million output) but was free for Bun due to its Anthropic affiliation. The Rust port reduced binary size by 20% and improved startup performance by 10% on Linux.

rss · Simon Willison · Jul 8, 23:57

**Background**: Bun is a JavaScript runtime, package manager, and test runner designed as a drop-in replacement for Node.js. It was originally written in Zig, a systems programming language that requires manual memory management. Mixing garbage-collected JavaScript with manually-managed Zig code led to many memory-related bugs, which Rust's ownership model and RAII can prevent at compile time.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bun_(software)">Bun (software) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>

</ul>
</details>

**Discussion**: Comments on Hacker News generally praised the disciplined approach and the use of AI with human oversight. Some noted that the rewrite's success reflects poorly on Zig's memory safety, while others questioned the fairness of comparing AI-assisted rewrite costs to a human team, given the $165k token cost was waived.

**Tags**: `#Bun`, `#Rust`, `#Zig`, `#JavaScript runtime`, `#rewrite`

---

<a id="item-3"></a>
## [Mistral Releases Robostral Navigate, an 8B Robotics Model](https://mistral.ai/news/robostral-navigate/) ⭐️ 8.0/10

Mistral AI has released Robostral Navigate, an 8-billion-parameter robotics navigation model that achieves 76.6% on the R2R-CE benchmark using only a single RGB camera, without depth sensors, LiDAR, or multiple cameras. This model demonstrates that map-less navigation is possible with minimal hardware, which could significantly reduce the cost and complexity of deploying autonomous robots in homes, warehouses, and industrial settings. The model was trained entirely in simulation and uses natural language instructions to guide the robot. It is Mistral's first robotics model and is not openly available, but the company may offer access through partnerships or APIs.

hackernews · ottomengis · Jul 8, 14:09 · [Discussion](https://news.ycombinator.com/item?id=48832212)

**Background**: Traditional robot navigation often relies on pre-built maps or expensive sensors like LiDAR. Map-less navigation, also known as visual navigation, uses camera input and deep learning to navigate without a map, solving the 'kidnapped robot problem' where a robot cannot localize itself. The R2R-CE benchmark evaluates navigation from visual observations and language instructions.

<details><summary>References</summary>
<ul>
<li><a href="https://mistral.ai/news/robostral-navigate/">Robostral Navigate: single-camera AI navigation | Mistral AI</a></li>
<li><a href="https://cryptobriefing.com/mistral-robostral-navigate-robotics-model/">Mistral AI unveils Robostral Navigate, an 8B robotics model that could reshape industrial automation investing</a></li>
<li><a href="https://alphasignal.ai/news/mistral-s-robostral-navigate-beats-sensor-heavy-robots-with-just-one-camera">Mistral's Robostral Navigate Beats Sensor-Heavy Robots With Just One Camera | AlphaSignal</a></li>

</ul>
</details>

**Discussion**: Commenters are excited about the map-less navigation capability, with some hoping to use it in hobbyist projects like farm robots. Others note that while outdoor map-less navigation exists, indoor map-less navigation is relatively new. There is also interest in extending the model to higher-level tasks like object manipulation.

**Tags**: `#robotics`, `#navigation`, `#AI`, `#Mistral`, `#deep learning`

---

<a id="item-4"></a>
## [Grok 4.5 Launches with Cursor Data, Sparks Trust Debate](https://x.ai/news/grok-4-5) ⭐️ 8.0/10

xAI released Grok 4.5, a model trained on trillions of tokens of Cursor user interaction data, claiming 4x better reasoning efficiency than Opus at lower cost ($2/$6 per million tokens). This marks the first major model trained on real-world developer-agent interaction data, potentially setting a new standard for coding AI, but raises ethical concerns about data privacy and political bias. Grok 4.5 is based on xAI's 1.5T V9 foundation model with supplemental Cursor data, and is currently in private beta at SpaceX and Tesla. Pricing is $2 per million input tokens and $6 per million output tokens.

hackernews · BoumTAC · Jul 8, 18:00 · [Discussion](https://news.ycombinator.com/item?id=48835111)

**Background**: Grok is xAI's family of large language models, known for their coding and reasoning capabilities. Cursor is an AI coding assistant that collects user code and interaction data when privacy mode is off. xAI has faced criticism for allegedly shaping Grok's responses to fit a political narrative, with recent system prompts instructing it to assume media viewpoints are biased.

<details><summary>References</summary>
<ul>
<li><a href="https://x.ai/news/grok-4-5">Introducing Grok 4.5 | SpaceXAI</a></li>
<li><a href="https://cursor.com/data-use">Cursor · Data Use & Privacy Overview</a></li>
<li><a href="https://fortune.com/2025/07/08/elon-musk-grok-ai-conservative-bias-system-prompt/">Users accuse Elon Musk's Grok of a rightward tilt after xAI changes its internal instructions to assume viewpoints from the media are 'biased' | Fortune</a></li>

</ul>
</details>

**Discussion**: Community comments are mixed: some praise the model's cost-efficiency and benchmark performance, while others express distrust due to xAI's political alignment and data privacy concerns. A user questioned the economic sense of spending billions for a third-best model.

**Tags**: `#AI`, `#LLM`, `#Grok`, `#xAI`, `#benchmarks`

---

<a id="item-5"></a>
## [OpenAI Launches GPT-Live Voice Mode with GPT-5.5 Delegation](https://openai.com/index/introducing-gpt-live/) ⭐️ 8.0/10

OpenAI has introduced GPT-Live, a full-duplex voice mode for ChatGPT that can delegate complex reasoning and web search tasks to GPT-5.5 in the background, enabling extended, productive conversations. This feature bridges the gap between voice assistants and frontier AI models, allowing users to have natural, real-time conversations while still accessing the latest reasoning capabilities, which could significantly boost productivity for tasks like brainstorming, research, and coding. GPT-Live is a full-duplex model that can listen and speak simultaneously, and it delegates deeper reasoning to GPT-5.5, which was released in April 2026. The system includes safety integrations that check inputs and outputs in real time and can interrupt or end conversations if unsafe content is detected.

hackernews · logickkk1 · Jul 8, 17:03 · [Discussion](https://news.ycombinator.com/item?id=48834405)

**Background**: Voice assistants like Siri and Google Assistant have traditionally been limited to simple commands and lacked access to the most advanced AI models. GPT-Live addresses this by combining a lightweight voice model with a powerful backend model (GPT-5.5), allowing for complex tasks without sacrificing conversational flow. GPT-5.5 itself is a large language model that excels at coding, research, and data analysis.

<details><summary>References</summary>
<ul>
<li><a href="https://www.marktechpost.com/2026/07/08/openai-releases-gpt-live-and-gpt-live-1-mini-full-duplex-voice-models-that-delegate-deeper-reasoning-to-gpt-5-5/">OpenAI Releases GPT-Live and GPT-Live-1 mini: Full-Duplex Voice Models That Delegate Deeper Reasoning to GPT-5.5 - MarkTechPost</a></li>
<li><a href="https://venturebeat.com/technology/openai-launches-gpt-live-a-full-duplex-voice-upgrade-that-lets-chatgpt-talk-more-like-a-person">OpenAI launches GPT-Live, a full-duplex voice upgrade that lets ChatGPT talk more like a person | VentureBeat</a></li>

</ul>
</details>

**Discussion**: Community comments are mixed: some users praise the feature for enabling long, productive conversations (e.g., a one-hour brainstorming session), while others express concerns about AI replacing human relationships and the lack of tool/connector support in voice mode. A bug was reported where the model would interrupt and laugh at unintended moments.

**Tags**: `#AI`, `#OpenAI`, `#voice assistant`, `#GPT-5.5`, `#productivity`

---

<a id="item-6"></a>
## [Cloudflare Meerkat: Leaderless Async Consensus](https://blog.cloudflare.com/meerkat-introduction/) ⭐️ 8.0/10

Cloudflare announced Meerkat, a globally distributed, leaderless consensus algorithm based on QuePaxa that operates asynchronously without relying on timeouts. This is the first production implementation of an asynchronous consensus algorithm, potentially improving robustness in unreliable networks where leader-based protocols like Raft struggle. Meerkat uses randomized asynchronous consensus to guarantee liveness under worst-case conditions and relies on hedging instead of timeouts for efficiency. However, it requires global consensus for every read operation, which may increase latency.

hackernews · bobnamob · Jul 8, 13:18 · [Discussion](https://news.ycombinator.com/item?id=48831565)

**Background**: Consensus algorithms like Paxos and Raft are fundamental to distributed systems, enabling multiple servers to agree on a value even if some fail. Traditional protocols are partially synchronous, relying on timeouts to detect failures, which can cause issues in networks with high latency or packet loss. QuePaxa, the basis for Meerkat, is an asynchronous consensus algorithm that does not depend on timeouts, making it more robust under adverse conditions.

<details><summary>References</summary>
<ul>
<li><a href="https://bford.info/pub/os/quepaxa/">QuePaxa: Escaping the Tyranny of Timeouts in Consensus – Bryan Ford's Home Page</a></li>
<li><a href="https://bford.info/pub/os/quepaxa/quepaxa.pdf">QuePaxa: Escaping the Tyranny of Timeouts in Consensus Pasindu Tennage* EPFL</a></li>

</ul>
</details>

**Discussion**: Commenters noted that Meerkat is the first production implementation of an asynchronous consensus algorithm, but some questioned its performance for read-heavy workloads since every read requires global consensus. Others appreciated its potential for messy networks where leader-based protocols suffer from flapping and election storms.

**Tags**: `#distributed systems`, `#consensus`, `#cloudflare`, `#asynchronous`, `#meerkat`

---

<a id="item-7"></a>
## [EU Revives Chat Control 1.0, Scanning Non-E2EE Messages](https://cyberinsider.com/eu-now-one-step-away-from-reviving-private-message-scanning-rules/) ⭐️ 8.0/10

The EU is one step away from reviving Chat Control 1.0, a regulation that allows providers to scan non-end-to-end encrypted messages for child sexual abuse material (CSAM). A decisive vote is expected on July 9, 2026, where an absolute majority of 361 MEPs is needed to stop it. This development has significant privacy implications for EU citizens, as it permits mass scanning of private communications, albeit only those without end-to-end encryption. It also sets a precedent that could pave the way for the more controversial Chat Control 2.0, which would mandate scanning and ban end-to-end encryption. Chat Control 1.0 only applies to non-E2EE services like Facebook Messenger or Gmail, not to encrypted platforms like WhatsApp or Signal. The regulation was initially rejected on March 26, 2026, by a single vote, but was revived and fast-tracked for a decisive vote on July 9, 2026.

hackernews · ggirelli · Jul 8, 16:53 · [Discussion](https://news.ycombinator.com/item?id=48834296)

**Background**: Chat Control is a proposed EU regulation aimed at preventing child sexual abuse online by requiring digital platforms to detect and report CSAM. Civil society organizations argue that the proposal would effectively mandate mass surveillance of private communications, undermining end-to-end encryption and violating fundamental privacy rights. The first iteration (1.0) focuses on non-E2EE messages, while the second (2.0) would extend to all communications, including encrypted ones.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control_1.0">Chat Control 1.0</a></li>

</ul>
</details>

**Discussion**: Commenters generally distinguish Chat Control 1.0 from 2.0, with some noting that 1.0 seems acceptable as it only allows scanning of non-E2EE messages, which users already expect to be visible to providers. However, others express concern that this could be a stepping stone to 2.0, which would mandate scanning and ban E2EE. Several users provide actionable links, such as fightchatcontrol.eu, for EU citizens to contact their representatives.

**Tags**: `#privacy`, `#EU legislation`, `#encryption`, `#surveillance`, `#CSAM`

---

<a id="item-8"></a>
## [LingBot-Video: Open-Source Sparse-MoE Video Diffusion Transformer](https://www.reddit.com/r/MachineLearning/comments/1ur0bxq/lingbotvideo_sparsemoe_video_diffusion/) ⭐️ 8.0/10

LingBot-Video, a 13B-parameter sparse-MoE video diffusion transformer with only 1.4B active parameters, has been open-sourced with RL post-training and action-conditioned world model capabilities. This work pushes forward open-source video generation and world modeling by combining sparse MoE efficiency with RL fine-tuning, but its reliance on VLM-based physical plausibility rewards and lack of closed-loop robot evaluation raise important questions about the validity of world model claims. The model uses a DeepSeek-V3-style sparse MoE with 128 experts and top-8 routing, achieving 1.4B active parameters out of 13B total. It incorporates six reward signals in RL post-training, including a physical-plausibility reward graded by a VLM, and supports action-to-video mode for robot rollouts.

reddit · r/MachineLearning · /u/Savings-Display5123 · Jul 8, 17:58

**Background**: Video diffusion transformers generate videos by iteratively denoising latent representations. Sparse mixture-of-experts (MoE) reduces computational cost by activating only a subset of parameters per token. World models aim to predict future states given actions, enabling planning in robotics, but distinguishing them from video generators requires closed-loop evaluation.

**Discussion**: The Reddit post author invites scrutiny on two key points: whether a VLM can defensibly judge physical plausibility without reward hacking, and whether the model truly qualifies as a world model without closed-loop robot results. The community is expected to debate these issues, given the model's top average on RBench but second place on general T2V.

**Tags**: `#video diffusion`, `#sparse MoE`, `#world model`, `#reinforcement learning`, `#open source`

---

<a id="item-9"></a>
## [DeepSeek Develops Own AI Chip to Cut Nvidia, Huawei Dependence](https://t.me/zaihuapd/42423) ⭐️ 8.0/10

DeepSeek, a Chinese AI company, is developing its own AI chip focused on inference, aiming to reduce reliance on Nvidia and Huawei chips. The effort has been underway for about a year and is still in early stages. This move could reshape the AI hardware landscape in China, especially amid US export controls that restrict access to advanced Nvidia chips. It also signals a broader trend of Chinese tech firms pursuing chip self-sufficiency. The chip is designed specifically for inference, not training, and DeepSeek has begun contacting chip design, foundry, and memory companies while aggressively recruiting chip design engineers. Previously, DeepSeek relied on Nvidia H800 and Huawei Ascend chips.

telegram · zaihuapd · Jul 8, 05:20

**Background**: DeepSeek is a Chinese AI startup known for its large language models. The Nvidia H800 is a GPU designed for datacenters, but US export controls have restricted its sale to China. Developing proprietary chips helps companies like DeepSeek bypass such restrictions and reduce dependency on foreign suppliers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NVIDIA_H800_GPU">NVIDIA H800 GPU</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#DeepSeek`, `#hardware`, `#semiconductors`, `#China`

---

<a id="item-10"></a>
## [Alibaba Orders Employees to Uninstall Claude by July 10](https://t.me/zaihuapd/42424) ⭐️ 8.0/10

Alibaba has internally ordered all employees to uninstall Anthropic products, including Claude, Sonnet, Opus, Fable, and Claude Code, effective July 10, following Anthropic's accusation that Alibaba used about 25,000 fake accounts to interact with Claude over 28 million times between April 22 and June 5. This incident marks a direct confrontation between two major AI companies, highlighting escalating tensions over API abuse and usage policies. It could set a precedent for how enterprises manage employee access to external AI tools and may impact cross-company AI collaboration. The ban covers all Anthropic products, including models like Sonnet, Opus, and Fable, as well as agent products like Claude Code. Alibaba previously reimbursed employees for using external models such as Claude, GPT, and Gemini, but this policy has now been reversed.

telegram · zaihuapd · Jul 8, 06:09

**Background**: Anthropic is an AI safety company that developed the Claude model family, competing with OpenAI's GPT and Google's Gemini. API abuse, such as using fake accounts to bypass rate limits or extract data, is a common concern for AI providers. Alibaba is a Chinese tech giant with its own AI models, including the Tongyi Qianwen series.

**Tags**: `#Alibaba`, `#Anthropic`, `#Claude`, `#AI policy`, `#enterprise security`

---

<a id="item-11"></a>
## [Huawei 5G Flagship Returns Overseas, Peak Speed Exceeds 1100 Mbps](https://finance.sina.com.cn/tech/roll/2026-07-08/doc-inihapna8035781.shtml) ⭐️ 8.0/10

Huawei's Pura 90 Pro Max international version natively supports 5G, achieving peak download speeds over 1100 Mbps in overseas tests, marking the official return of Huawei's 5G flagship to overseas markets after 7 years of US sanctions. This signifies a major geopolitical and technological milestone, as Huawei regains competitiveness in the global smartphone market and demonstrates its ability to overcome US sanctions with advanced 5G technology. The device shows a 5G icon in the status bar and uses HarmonyOS 6.0.0.125 with 5A communication technology, which laid the technical foundation for the overseas return.

telegram · zaihuapd · Jul 8, 12:17

**Background**: Since 2019, US sanctions prevented Huawei from selling 5G phones overseas. In 2023, the Mate 60 series broke through the technology blockade, and now the Pura 90 Pro Max international version brings 5G back to global markets.

**Tags**: `#Huawei`, `#5G`, `#smartphone`, `#sanctions`, `#technology`

---

<a id="item-12"></a>
## [Critical Android Remote Root Exploit Chain Disclosed](https://www.coolapk.com/feed/72700258?s=ZGQ2MTVlZjYxMDYyNTM3ZzZhNGUzOThjega1640) ⭐️ 8.0/10

On July 8, cybersecurity firm Nebula disclosed a remote root exploit chain affecting all Android versions up to Android 17, combining a Firefox browser vulnerability (version 151.0.2 and earlier) and a 15-year-old Linux kernel bug. Clicking a malicious link can grant attackers persistent root access within a minute. This exploit chain is severe because it requires no user interaction beyond clicking a link, enabling full device compromise remotely. It affects a vast number of Android devices, and with proof-of-concept code already public, widespread exploitation is likely. The attack chain uses a Firefox exploit to gain initial code execution, then escalates privileges via a Linux kernel vulnerability (CVE not yet disclosed). Google Pixel devices have been confirmed vulnerable, and the Linux kernel fix is already available.

telegram · zaihuapd · Jul 8, 13:01

**Background**: Android security relies on sandboxing and permission models, but kernel-level bugs can bypass these protections. Remote root exploits are rare because they require chaining multiple vulnerabilities. The disclosed chain combines a browser bug for initial access and a kernel bug for privilege escalation, making it particularly dangerous.

**Tags**: `#android`, `#security`, `#vulnerability`, `#root`, `#exploit`

---

<a id="item-13"></a>
## [Meituan OWL Test Model Leaks User Conversations](https://github.com/gumusserv/ProducerBenchV2/blob/83cad6007ef3fe8df33386e8f43738fe62337e16/parsed_source_data/data/) ⭐️ 8.0/10

Meituan's OWL (LongCat) free test model on OpenRouter reportedly leaked user conversation data, with a GitHub repository containing the data now taken down. This incident highlights the security risks of exposing sensitive information in AI model interactions, especially for developers and enterprises using public test models. The leaked data appeared in a GitHub repository at least as early as July 7, 2026, and was later discovered by a Discord bot token scanner, which reported the token as exposed and reset.

telegram · zaihuapd · Jul 8, 13:35

**Background**: AI models like Meituan's OWL are often offered for free testing on platforms like OpenRouter. Companies such as Google and DeepSeek have stated in privacy notices that user conversation data may be used for service improvement, analysis, or model training. This incident underscores the risk of inputting sensitive information like API keys, private keys, or enterprise source code into AI models.

**Discussion**: The Telegram discussion includes warnings from users about the leak and references to similar past incidents, adding credibility and urgency to the issue.

**Tags**: `#data leak`, `#AI security`, `#Meituan`, `#privacy`, `#LLM`

---

<a id="item-14"></a>
## [Researchers ID smartphone apps via EM signals with 99% accuracy](https://www.scmp.com/news/china/science/article/3359688/chinese-researchers-find-peephole-any-smartphone-its-leaked-radio-signal) ⭐️ 8.0/10

Chinese researchers have developed a non-contact technique that analyzes leaked low-frequency electromagnetic signals from smartphones to identify which app is being used, achieving up to 99.07% accuracy on devices like iPhone 15 Pro, Xiaomi 15 Pro, and OPPO Reno 13. This side-channel attack poses a significant privacy threat because it works even when the phone is offline, in airplane mode, encrypted, or locked, without requiring any access to the device's system or stored data. The technique targets low-frequency electromagnetic emissions (below 1 MHz) from smartphone components like the CPU and GPU, and can distinguish between apps such as Douyin, WeChat video calls, Baidu Maps, SMS, browser, camera, and cloud storage.

telegram · zaihuapd · Jul 8, 16:05

**Background**: A side-channel attack exploits unintended physical emissions—such as electromagnetic radiation, power consumption, or timing—to extract sensitive information. Unlike traditional cyberattacks that target software vulnerabilities, side-channel attacks leverage the physical implementation of a system. This research demonstrates that even encrypted or offline smartphones leak identifiable electromagnetic patterns during app usage.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Side-channel_attack">Side-channel attack</a></li>

</ul>
</details>

**Tags**: `#side-channel attack`, `#smartphone security`, `#privacy`, `#electromagnetic signals`, `#forensics`

---