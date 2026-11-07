---
layout: default
title: "Horizon Summary: 2026-11-08 (EN)"
date: 2026-11-08
lang: en
---

> From 38 items, 21 important content pieces were selected

---

1. [GitHub's Rubicon architecture sustains 7,200 pushes per second](#item-1) ⭐️ 9.0/10
2. [John Langford exits as Microsoft Research's AI Frontiers group is shut down](#item-2) ⭐️ 8.0/10
3. [Need for Speed Underground 2 Runs in Browser With Multiplayer](#item-3) ⭐️ 8.0/10
4. [Every Mac ships undocumented Apple Intelligence daemons that map your relationships](#item-4) ⭐️ 8.0/10
5. [Libghostty 1.0 Ships Stable-ABI C Library for Terminal Emulation](#item-5) ⭐️ 8.0/10
6. [SemiAnalysis Tours China's 800MW Wind-Powered AI Campus in Inner Mongolia](#item-6) ⭐️ 8.0/10
7. [China Blocks SoftBank's $5.4 Billion Acquisition of ABB Robotics](#item-7) ⭐️ 8.0/10
8. [Apple Unveils HALO: A Three-Layer Humanoid Robot Control System Powered by Two Qwen Models](#item-8) ⭐️ 8.0/10
9. [$10 OpenStick Homelab: Self-Hosting on a USB-Dongle Linux Box](#item-9) ⭐️ 7.0/10
10. [Apple's iPhone keyboard "grey list" silently skips thousands of words and phrases](#item-10) ⭐️ 7.0/10
11. [A UK lawyer runs an entire law firm on free and open-source software](#item-11) ⭐️ 7.0/10
12. [Asahi Linux 7.3 Report Flags Licensing Fears as Apple Silicon Work Continues](#item-12) ⭐️ 7.0/10
13. [Retrospective on Borland Turbo Pascal 7 and Its Blazing-Fast IDE](#item-13) ⭐️ 7.0/10
14. [Oracle Reportedly Cancels $7B AI Chip Lease Deal With Tencent](#item-14) ⭐️ 7.0/10
15. [Apple Said to Train China-Only LLM With Alibaba, May Be First Foreign Firm Approved](#item-15) ⭐️ 7.0/10
16. [Claude Code reportedly leaked users' login emails via web search requests](#item-16) ⭐️ 7.0/10
17. [$8 Linux Computer: Hacking Ultra-Cheap Hardware](#item-17) ⭐️ 6.0/10
18. [Harsh peer review accuses ML paper of being AI-generated and jargon-filled](#item-18) ⭐️ 6.0/10
19. [Pointer Networks Solve TSP Instantly but Degrade at Scale, Benchmark vs OR-Tools Shows](#item-19) ⭐️ 6.0/10
20. [OnlyFake founder confesses to AI fake ID fraud, deported from US](#item-20) ⭐️ 6.0/10
21. [Consumer Files Class Action Against Anthropic Over Alleged Misleading Max Plan Usage Limits](#item-21) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [GitHub's Rubicon architecture sustains 7,200 pushes per second](https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/) ⭐️ 9.0/10

GitHub unveiled a new Git storage architecture, codenamed Rubicon, which stores Git objects in Azure Blob Storage and manages reference state through a system called Ref-CAS. In internal tests it handled 5,000 concurrent AI agents writing to a single repository at 7,200 pushes per second while keeping read latency low. Coding agents are changing the load profile of repositories — many writers hammering one repo instead of many humans pushing occasionally — and GitHub's existing storage was not designed for that. If this design generalizes, it removes a key scalability bottleneck for AI-agent-driven development workflows across the entire GitHub platform. The design separates storage from compute and narrows ordering requirements to reference updates only, so each component can scale independently; every Ref-CAS update is a compare-and-swap that locks only the references it touches and becomes visible once a quorum of the log's replicas records it, while virtual replicas handle reads and writes and background nodes compact objects into packfiles. Rubicon is currently in a limited private preview, with a broader rollout to follow.

telegram · zaihuapd · Nov 7, 14:12

**Background**: Git traditionally stores each object as a loose file and periodically packs them into compressed packfiles, which works well when a repository sees occasional pushes from humans. Object storage like Azure Blob Storage is cheap and effectively unbounded but has high per-request overhead, so putting Git on it requires matching Git's unit of storage to the object store's unit. Git also relies on references (branches and tags) being updated atomically and consistently, the part that becomes hard when thousands of writers target the same repository at once.

<details><summary>References</summary>
<ul>
<li><a href="https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/">Inside GitHub's new Git storage architecture - The GitHub Blog</a></li>
<li><a href="https://meteoraweb.com/en/news/github-rubicon-nouvelle-architecture-git-agents-depot">GitHub Rubicon, new Git storage architecture • Meteora Web</a></li>
<li><a href="https://lumienai.com/news/github-project-rubicon-new-git-storage-architecture">GitHub's "Project Rubicon": A New Git Storage Built for…</a></li>

</ul>
</details>

**Tags**: `#GitHub`, `#Git storage architecture`, `#AI agents`, `#distributed systems`, `#infrastructure`

---

<a id="item-2"></a>
## [John Langford exits as Microsoft Research's AI Frontiers group is shut down](https://hunch.net/?p=13764006) ⭐️ 8.0/10

John Langford, the researcher who led Microsoft Research's AI Frontiers group, has left Microsoft and publicly declared the group finished after it was moved out of Microsoft Research and folded into the larger Microsoft AI organization. According to Langford, the dissolution reflects a philosophical shift: the new Microsoft AI leadership, which came in via the Inflection acquisition, favors a scaling-centric approach over the group's brand of open-ended fundamental research. The closure is being read as a signal that large labs are narrowing their AI bets to transformer scaling and product iteration, leaving less room for exploratory work on alternative architectures and methods. If that pattern holds across the industry, it could reduce the diversity of research directions that historically produced breakthroughs, and it affects researchers who choose non-mainstream agendas inside big companies. The group's work centered on fundamental advances in AI rather than scaling existing models, and its own lab page describes a culture of publishing research and contributing to open source. The reported trigger is organizational rather than technical: AI Frontiers was reassigned from Microsoft Research into Microsoft AI, a structure Langford says left little room for the kind of innovation his team wanted to pursue.

hackernews · srean · Nov 7, 18:02 · [Discussion](https://news.ycombinator.com/item?id=50406563)

**Background**: Microsoft Research is the company's long-standing fundamental-research arm, while Microsoft AI is the product-focused organization formed around Mustafa Suleyman after Microsoft's 2024 licensing deal and hiring from AI startup Inflection. AI Frontiers was a relatively small lab inside Microsoft Research aimed at high-risk, high-reward questions about how AI systems learn and reason, rather than incremental gains on existing large language models. Most current LLMs are built on the transformer architecture, and progress in recent years has largely come from scaling up data, parameters and compute following neural scaling laws.

<details><summary>References</summary>
<ul>
<li><a href="https://grafy.ai/news/microsoft-research-s-ai-frontiers-group-disbanded-following-reorg">Microsoft Research's AI Frontiers group — Grafy News</a></li>
<li><a href="https://www.indiatoday.in/technology/news/story/microsoft-ai-research-clash-john-langford-quits-declares-ai-frontiers-over-3034334-2026-11-07">Microsoft AI research clash: John Langford quits, declares AI ...</a></li>
<li><a href="https://www.microsoft.com/en-us/research/lab/ai-frontiers/">Microsoft Research AI Frontiers - Microsoft Research</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed that this is an industry-wide pattern, with one arguing that every large company is racing down the transformer "highway" and discouraging exploratory research, citing Meta's treatment of its own research leadership. Others pushed back or reframed: one noted the headline overstates things since only a specific group is ending, another suggested that AI coding agents with basic research capabilities may now make single-researcher ideas more viable, and a third questioned why firms with billions would stop R&D on the technology most likely to reshape the race, betting instead that the next breakthroughs will come from radical efficiency optimizations.

**Tags**: `#Microsoft Research`, `#AI research`, `#industry trends`, `#transformer models`, `#Hacker News`

---

<a id="item-3"></a>
## [Need for Speed Underground 2 Runs in Browser With Multiplayer](https://nfsu2.xyz/) ⭐️ 8.0/10

Need for Speed Underground 2 has been reverse-engineered and brought online in the browser at nfsu2.xyz, with working multiplayer and reports that it runs on phones as well as desktops. This is a technically impressive revival of a 2004 racing game that is difficult to run on modern PCs, showing how WebGPU and reverse engineering can support game preservation and browser-based gaming. The site is not an officially licensed release, so takedown risk is significant; Linux Chromium users reportedly need to enable unsafe WebGPU features for it to work.

hackernews · fluxusars · Nov 7, 09:36 · [Discussion](https://news.ycombinator.com/item?id=50403052)

**Background**: WebGPU is a modern browser API that exposes GPU graphics and compute capabilities, making complex 3D games possible inside a web page. Reverse engineering in this context means recreating or adapting the original game's engine and networking so it can run on new platforms. Abandonware refers to old software that is no longer sold or supported by its rights holder, but copyright restrictions can still apply.

<details><summary>References</summary>
<ul>
<li><a href="https://itch.io/games/tag-webgpu">Top games tagged webgpu - itch.io</a></li>
<li><a href="https://hammadshakeelai.github.io/gta5-web/">PlayGTA5 · WebAssembly & WebGPU Edition</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters are enthusiastic and nostalgic, with many reporting that it works well on phones and sharing Linux Chromium WebGPU workarounds. Several users worry about the site's legality and a potential takedown, and one commenter criticizes soliciting donations for copyrighted content.

**Tags**: `#WebGPU`, `#game-preservation`, `#reverse-engineering`, `#browser-gaming`, `#abandonware`

---

<a id="item-4"></a>
## [Every Mac ships undocumented Apple Intelligence daemons that map your relationships](https://8rank.ai/game/apple-intelligence-personal-knowledge-graph) ⭐️ 8.0/10

A reverse-engineering investigation published on 8rank.ai reports that every Mac released since roughly 2022 ships a pair of undocumented Apple Intelligence daemons whose job is to build a personal knowledge graph of the user — who they are, who they know, how those people relate to each other, and how, where and when they communicate. The researcher notes that none of this is described in Apple's user-facing documentation or settings. The finding matters because it means relationship and family-member profiling happens silently on hardware users bought specifically for its privacy reputation, directly testing Apple's long-standing "privacy by default" marketing. If accurate, it affects essentially every recent Mac owner and sets a precedent for how much on-device inference can be inferred about a person without explicit consent. The claims come from hands-on reverse engineering of the binaries rather than from any Apple disclosure, and the author has published a follow-up piece continuing the analysis and answered questions directly in the Hacker News thread. The researcher also points out that closely related personal-context capabilities are already visible in consumer features such as Photos, which knows the names and faces of the people and even pets in a user's life.

hackernews · infwhispers · Nov 7, 09:46 · [Discussion](https://news.ycombinator.com/item?id=50403097)

**Background**: Apple Intelligence is Apple's umbrella name for its AI features, announced on June 10, 2024, which combine on-device processing with server-side models and are marketed around "personal context understanding" — knowing enough about your messages, photos and calendar to act on your behalf. A personal knowledge graph, in the software-engineering sense, is a structured graph about a person: nodes for people, places and events, and edges for the relationships between them. In macOS, a daemon is a background process that runs without a visible app window, which is why such components can operate without the user ever noticing them.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Personal_knowledge_graph">Personal knowledge graph</a></li>
<li><a href="https://en.wikipedia.org/wiki/Personal_knowledge_base">Personal knowledge base - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The discussion is skeptical rather than alarmist: one commenter says they would once have found such data fascinating but now find it exhausting, arguing that ordinary conversation relies on a shared expectation that not everything will be remembered, while another quotes Steve Jobs' 2010 remark that privacy means asking users every time and telling them precisely what will be done with their data. Others say the accumulating weight of such revelations makes Linux plus a dumb phone look like the obvious choice, and several note that Apple's existing face and pet recognition already shows how much the system knows.

**Tags**: `#privacy`, `#apple`, `#macos`, `#knowledge-graph`, `#reverse-engineering`

---

<a id="item-5"></a>
## [Libghostty 1.0 Ships Stable-ABI C Library for Terminal Emulation](https://mitchellh.com/writing/libghostty-1-0) ⭐️ 8.0/10

Mitchell Hashimoto announced the 1.0 release of libghostty-vt, a portable, high-performance C library for terminal emulation extracted directly from the core of Ghostty. The 1.0 milestone means both the library itself and its C ABI are now stable. A stable ABI lets any application embed correct, fast terminal emulation without writing yet another emulator, which is already spawning a wave of new terminals and "agentic" coding tools such as herdr and cmux built on top of it. Because the ABI is frozen, downstream projects can upgrade the library without recompiling their own binaries. Hashimoto says he designed the API by borrowing from C libraries he enjoyed using, exposing objects as opaque handles and relying on enum-keyed getters and setters so implementation details don't leak to callers. The project ships both C and Zig APIs, is MIT licensed, and includes ghostling, a minimum-viable terminal demonstrating how to embed libghostty.

hackernews · mfiguiere · Nov 6, 23:30 · [Discussion](https://news.ycombinator.com/item?id=50399933)

**Background**: Ghostty is a fast, feature-rich, cross-platform terminal emulator that uses platform-native UI and GPU acceleration. libghostty is the embeddable piece extracted from Ghostty's core: it handles terminal emulation semantics (the VT parsing and terminal state) rather than the window or rendering chrome, so other programs — editors, IDEs, agent runtimes — can reuse Ghostty's behavior. An ABI (application binary interface) is the machine-code-level contract between a compiled program and a library; keeping it stable means programs built against older versions keep working with newer ones.

<details><summary>References</summary>
<ul>
<li><a href="https://mitchellh.com/writing/libghostty-1-0">Libghostty 1.0 – Mitchell Hashimoto</a></li>
<li><a href="https://lib.ghostty.org/vt/">libghostty-vt: libghostty-vt</a></li>
<li><a href="https://github.com/ghostty-org/ghostling">GitHub - ghostty-org/ghostling: A minimum viable terminal ...</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (984 points, 173 comments) is broadly enthusiastic: commenters praised Hashimoto for not sneaking a plug for his own competing product Rex into the announcement, and one developer working on a Zig project said the API design discussion prompted them to rethink their own overly leaky C interface. Others shared practical experience, with some saying Ghostty excels at fancy TUI programs like the pi agent and inline images via the Kitty graphics protocol, while one user said they had switched to kitty for its smoother rendering and animations.

**Tags**: `#terminal emulator`, `#C library`, `#ABI stability`, `#Ghostty`, `#open source`

---

<a id="item-6"></a>
## [SemiAnalysis Tours China's 800MW Wind-Powered AI Campus in Inner Mongolia](https://newsletter.semianalysis.com/p/we-visited-chinas-stargate-in-inner) ⭐️ 8.0/10

SemiAnalysis published a first-hand teardown of a wind-powered AI data center campus in Inner Mongolia rated at 800MW, reporting that roughly 120MW of capacity was built in under a year. The report also details a 5MW pilot using solid-state transformers to deliver 800V DC natively, plus a cooling architecture that does away with central chillers entirely. The build velocity and power architecture offer a rare concrete benchmark for how fast Chinese AI infrastructure can scale, at a time when US data center growth is increasingly constrained by grid interconnection and transformer lead times. If the SST-native 800V DC design proves out, it could compress the AC-to-DC conversion chain that dominates modern facility power loss. The campus is powered by wind and reached about 120MW of live capacity within roughly twelve months, with the 800MW figure describing the eventual full build-out rather than current load. The 800V DC effort is only a 5MW pilot and solid-state transformers remain an immature technology with open questions about reliability and cost at scale.

rss · Semianalysis · Nov 7, 19:01

**Background**: Hyperscale AI data centers traditionally take medium-voltage AC from the grid and step it down through transformers, switchgear, and multiple AC/DC conversion stages before reaching chips, with each stage losing energy. A solid-state transformer replaces the conventional iron-and-copper transformer with power electronics, allowing medium-voltage AC to be converted directly into high-voltage DC such as 800V, which is the voltage NVIDIA has targeted for next-generation rack power distribution. Cooling is the other major constraint: most large facilities rely on central chiller plants to produce cold water, so a design that eliminates them changes both the water footprint and the mechanical footprint of the campus.

<details><summary>References</summary>
<ul>
<li><a href="https://www.microchip.com/en-us/solutions/data-centers-and-computing/data-center-solutions/sst">Solid-State Transformer (SST) | Microchip Technology</a></li>
<li><a href="https://eepower.com/industry-articles/rearchitecting-data-center-power-for-ai-with-solid-state-transformers/">Rearchitecting Data Center Power for AI with Solid-State ...</a></li>
<li><a href="https://www.datacenterknowledge.com/energy-power-supply/solid-state-transformers-power-next-gen-ai-data-centers">Solid-State Transformers Power Next-Gen AI Data Centers</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#data centers`, `#power delivery`, `#cooling systems`, `#China tech`

---

<a id="item-7"></a>
## [China Blocks SoftBank's $5.4 Billion Acquisition of ABB Robotics](https://t.me/zaihuapd/44988) ⭐️ 8.0/10

On November 5, ABB confirmed it had been notified by China's foreign investment security review authority that SoftBank Group's roughly $5.4 billion acquisition of its robotics business is prohibited from being implemented in China. The block directly obstructs SoftBank's plan to build out a position across AI and robotics using ABB's industrial robotics assets. China accounts for roughly 30% of ABB's robotics business and is its largest robotics market, so a Chinese prohibition effectively kills a global deal rather than merely delaying it. The decision signals that Chinese regulators are now willing to use security review to keep industrial data, supply chains and core robotics technology inside the country, raising the bar for foreign M&A in strategic AI and automation sectors. Chinese regulators reportedly worried that industrial data, supply chain information and core technology tied to ABB's robotics unit could be transferred overseas and used to train AI models. Roughly 90% of the robots ABB sells to Chinese customers are already manufactured locally in China, which makes the data and technology-transfer concerns, rather than simple market access, the crux of the case.

telegram · zaihuapd · Nov 7, 11:24

**Background**: China's foreign investment security review system dates back to 2011 and was formalized in the Foreign Investment Security Review Measures that took effect in January 2021, with a working mechanism office housed at the National Development and Reform Commission and jointly led by the NDRC and the Ministry of Commerce. The mechanism reviews foreign deals touching national security, covering areas such as critical technology, important industrial supply chains and sensitive data. ABB, a Swiss industrial conglomerate, is one of the world's largest industrial robotics makers, and SoftBank has been assembling a full-stack AI portfolio spanning chips (Arm) and major model developers such as OpenAI.

<details><summary>References</summary>
<ul>
<li><a href="https://cn.nytimes.com/business/20261106/softbank-robotics-china-block/">中国阻止软银以54亿美元收购 ABB 机 器 人 业 务 - 纽约时报中文网</a></li>
<li><a href="https://www.kingandwood.com/cn/zh/insights/latest-thinking/china-s-national-security-review-system-for-foreign-investment.html">统筹对外开放与国家安全：中国外商投资安全审查制度详解 - 金杜律师事...</a></li>
<li><a href="https://www.ndrc.gov.cn/xxgk/zcfb/fzggwl/202012/P020201219582032130362.pdf">外商投资安全审查办法</a></li>

</ul>
</details>

**Tags**: `#China regulation`, `#SoftBank`, `#ABB robotics`, `#M&A`, `#AI geopolitics`

---

<a id="item-8"></a>
## [Apple Unveils HALO: A Three-Layer Humanoid Robot Control System Powered by Two Qwen Models](https://weibo.com/1642634100/RqjjGllvw) ⭐️ 8.0/10

Apple's robotics research team submitted a paper to arXiv on November 4 titled "Perceptive Humanoid Motion from Simulation," disclosing HALO, an autonomous humanoid control system that was validated on a Unitree G1 robot carrying out motions learned in simulation inside unfamiliar real-world rooms. HALO is structured in three layers: a high-level Qwen3.6-35B-A3B model that orchestrates tasks, a mid-level Qwen3.5-2B model that generates whole-body motions, and a low-level reinforcement-learning-trained motion tracker, with data generation, training, and deployment code released publicly. The work is a notable demonstration that large language models can serve as the high-level brain of a humanoid robot while a small model handles motion generation, showing a practical hierarchical path from language instruction and egocentric vision to real-world whole-body control. By open-sourcing the full pipeline and validating on the widely used Unitree G1, Apple gives academic and hobbyist robotics researchers a reproducible baseline for sim-to-real humanoid manipulation and locomotion. HALO takes language instructions plus egocentric camera images as input and sequences tasks, generates whole-body motions, and controls execution on the physical robot; reports citing Apple's team mention a roughly 91% success rate in real-world trials. The split between a 35B-parameter MoE orchestrator and a 2B motion generator is itself a notable design choice, keeping the low-level loop lightweight while leaning on a large model only for high-level reasoning.

telegram · zaihuapd · Nov 7, 13:35

**Background**: Sim-to-real transfer refers to training a robot policy inside a physics simulator and then deploying it on hardware without further real-world training, which is hard because simulated physics, sensing, and contact never perfectly match reality. Hierarchical control splits a task into a high-level planner that decides what to do and a low-level controller that decides how to move each joint, and recent work increasingly plugs vision-language models into the high-level slot. Apple's HALO uses Qwen models — Alibaba's open-weight LLM family, where "A3B" denotes a mixture-of-experts architecture with about 3B active parameters — and the Unitree G1 is a compact 1.32 m humanoid with 23–43 degrees of freedom that has become a common research platform.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/apple-aiml-research/ml-halo">GitHub - apple-aiml-research/ml-halo: HALO: Perceptive ...</a></li>
<li><a href="https://ai.42how.com/en/article/ee6a8f15-db79-4091-9a86-3bc31de6c02f">Apple Integrates Humanoid Perception Into Simulation for Zero ...</a></li>
<li><a href="https://www.gate.com/news/detail/apple-discloses-halo-robot-control-system-with-91-success-rate-on-november-25471644">Apple Discloses HALO Robot Control System with 91% Success ...</a></li>

</ul>
</details>

**Tags**: `#robotics`, `#humanoid-robots`, `#Qwen`, `#reinforcement-learning`, `#sim-to-real`

---

<a id="item-9"></a>
## [$10 OpenStick Homelab: Self-Hosting on a USB-Dongle Linux Box](https://blog.bosscher.ch/posts/openstick/) ⭐️ 7.0/10

A self-hosting enthusiast published a detailed write-up showing how they run a working homelab on an OpenStick, a roughly $10 Linux device in a USB-dongle form factor, by deliberately picking very lightweight software that fits the constrained hardware. The author says the point was to show others how cheaply they can get started with self-hosting, and the post sparked a wide-ranging Hacker News thread on tiny clusters, automation, and container update tooling. It demonstrates that the entry cost for a personal server stack has dropped to about the price of a meal, which matters for people who want to learn self-hosting, Linux administration, or container operations without buying a mini-PC or renting cloud instances. The discussion also reflects a broader shift toward "small software" and low-power nodes as RAM and hardware prices stay high. Commenters note the OpenStick sits somewhere around the performance of a Raspberry Pi Zero 2, so the practical ceiling is set by RAM rather than CPU. The author explicitly frames the build as an exercise in choosing software that fits tight memory limits, and readers chimed in with operational tips such as Podman auto-update for unattended container upgrades and delegating routine sysadmin to an AI agent with sudo access.

hackernews · LaurensBER · Nov 7, 18:12 · [Discussion](https://news.ycombinator.com/item?id=50406670)

**Background**: A homelab is a personal setup — usually at home — where enthusiasts run servers for services like file sync, password managers, media streaming, or monitoring, primarily to learn skills that transfer to professional infrastructure work. Self-hosting means running those services on your own hardware instead of relying on SaaS providers. The OpenStick is part of a wave of ultra-cheap ARM boards and USB-stick computers that run mainline Linux, and because such devices have very little RAM and storage, the community increasingly relies on containers (Docker/Podman) to package services into small, restartable units.

<details><summary>References</summary>
<ul>
<li><a href="https://forums.servethehome.com/index.php?threads/tiny-homelab-cluster-as-homelab.39241/">Tiny homelab Cluster as homelab | ServeTheHome Forums</a></li>
<li><a href="https://computingforgeeks.com/build-kubernetes-home-cluster/">Build a 3- Node Kubernetes Home Cluster | ComputingForGeeks</a></li>

</ul>
</details>

**Discussion**: The reception was enthusiastic, with readers calling it a fun and encouraging example of how much you can host on cheap hardware if you choose the right software. Several commenters pushed the idea further: one wants a PoE-enabled stick with a male Ethernet connector so nodes could be built into a cluster simply by plugging them into a switch, another shared that they hand sysadmin tasks to an AI agent with sudo, and a third recommended Podman auto-update for keeping containers patched amid frequent CVEs. At least one reader simply asked where the hardware can be purchased.

**Tags**: `#homelab`, `#self-hosting`, `#OpenStick`, `#Linux`, `#containerization`

---

<a id="item-10"></a>
## [Apple's iPhone keyboard "grey list" silently skips thousands of words and phrases](https://www.theguardian.com/technology/2026/nov/06/struggling-to-spell-male-chauvinist-pig-apple-grey-list-means-your-iphone-wont-help-you) ⭐️ 7.0/10

The Guardian reported on November 6, 2026 that a researcher decoded blocklists buried inside iOS and found 4,513 English phrases — plus separate lists in 27 other languages — that Apple's predictive text and swipe typing will refuse to suggest or autocomplete. The lists include unsurprising entries about drugs and sexual acts, but also phrases such as "iMessage isn't working", which the Guardian frames as a corporate-protection instinct. The finding turns a routine input-method design decision into a debate about soft censorship, because a platform can shape what people write simply by declining to suggest it, without ever blocking a keystroke. It affects hundreds of millions of iPhone users who rely on autocomplete and swipe typing daily, and it lands amid broader complaints that Apple's keyboard lags behind rival keyboards. Nothing is actually blocked — users can still type every one of these words by hand, since the lists only remove them from the candidate suggestions. The researcher extracted the material from on-device files, counting 4,513 English phrases across 27 additional language lists, and the Guardian notes Apple does not publish these lists.

hackernews · user_7832 · Nov 7, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50406111)

**Background**: Modern smartphone keyboards do more than map taps to letters: they run autocorrect, show a row of predicted next words, and support swipe typing, where you drag a finger across the letters of a word and the system infers it from the shape of the path. That inference ranks candidates using a word database and a language model, so an entry missing from the database is simply never offered — which is what "grey list" (as opposed to a hard blocklist) means here. Such lists are normally invisible to users and undocumented by vendors, which is why the researcher's extraction was newsworthy.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/06/struggling-to-spell-male-chauvinist-pig-apple-grey-list-means-your-iphone-wont-help-you">Struggling to spell ‘male chauvinist pig’? Apple ’s grey list means your...</a></li>
<li><a href="https://www.martincid.com/technology-sv/iphone-keyboard-blocked-phrases-autocomplete-swipe-list/">Your iPhone keyboard hides a list of 4,500 phrases it will ...</a></li>
<li><a href="https://www.androidheadlines.com/2026/11/apples-predictive-text-quietly-restricts-sensitive-words-political-phrases.html">Apple’s Predictive Text Quietly Restricts Sensitive Words ...</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters split sharply: some argued that declining to suggest a phrase is not censorship and is a sensible design choice, since a wild swipe is only a best guess and shouldn't auto-complete into something that makes the user look bad or, in some countries, get them arrested. Others countered that "soft coercion is still coercion" even when the words remain typeable, and several noted the behaviour is probably not unique to Apple, with one commenter suspecting Gboard has done the same for years. A separate thread of criticism focused on the iOS keyboard's overall quality, with users calling swipe typing painful compared with Google's Pixel keyboard and describing the keyboard as one of the most-used touch surfaces on iOS yet oddly neglected.

**Tags**: `#apple`, `#privacy`, `#censorship`, `#ios-keyboard`, `#ux-design`

---

<a id="item-11"></a>
## [A UK lawyer runs an entire law firm on free and open-source software](https://decoded.legal/blog/2026/11/running-a-law-firm-on-free-software-2026-edition/) ⭐️ 7.0/10

The decoded.legal blog published a "2026 edition" post describing how a practicing lawyer runs a law firm almost entirely on free and open-source software rather than the Microsoft-centric stack that dominates legal practice. The write-up is a practical, hands-on account of the tools and workflows used in day-to-day legal work, and it quickly drew attention on Hacker News. Law firms are among the most conservative software consumers, so a working, self-hosted open-source practice is a meaningful existence proof that the Microsoft Office monoculture is a convention rather than a hard technical requirement. It matters to anyone thinking about vendor lock-in, data sovereignty, and how professional norms — not just features — keep incumbents entrenched. Running a firm this way shifts real operational burden onto the practitioner: someone must choose, host, maintain, back up, and secure every tool, and must handle document exchange with clients and counterparties who live in Word. The comments also note the continuity risk — if the sole technical person is unavailable, colleagues and successors must be able to pick up the practice.

hackernews · DeepLogin · Nov 7, 09:39 · [Discussion](https://news.ycombinator.com/item?id=50403066)

**Background**: Most law firms standardize on Microsoft Word, Outlook and a set of niche practice-management, billing and document-management products, in part because courts, clients and opposing counsel all exchange .docx files with tracked changes and comments. Free and open-source alternatives exist for each layer — Linux desktops, LibreOffice or other word processors, self-hosted email, wikis and accounting tools — but assembling them into a coherent, compliant practice is unusual. "Vendor lock-in" refers to the difficulty of switching away from such a stack once documents, workflows and staff habits are built around it, and "self-hosting" means running the software on infrastructure you control rather than a vendor's cloud.

**Discussion**: Commenters were largely admiring but split on practicality: one lawyer in a large firm envied the freedom while describing an overloaded Word and a stack of slow, buggy billing and document tools, and another warned that firms adopting AI legal tools like Harvey are handing a vendor the data and reach to integrate vertically and become "the Amazon for law." The strongest pushback was about risk and professional norms — one reader asked what happens to clients if the sole IT-savvy lawyer is unavailable, and another relayed a respected open-source lawyer's remark that not using Microsoft Word in a law firm amounts to malpractice.

**Tags**: `#open-source`, `#legal-tech`, `#self-hosting`, `#vendor-lock-in`, `#hacker-news`

---

<a id="item-12"></a>
## [Asahi Linux 7.3 Report Flags Licensing Fears as Apple Silicon Work Continues](https://asahilinux.org/2026/11/progress-report-7-3/) ⭐️ 7.0/10

Asahi Linux published its 7.3 progress report, covering continued enablement work for Apple Silicon Macs, and used the update to raise concerns that outside parties have made multiple attempts to exploit the project's permissive licensing in order to "hijack" its work and aggressively monetize Linux on Apple hardware. The post drew heavy community attention, including a rival project (Gravity Linux) publicly claiming Vulkan 1.4 support and working M4/M5 hardware in the same thread. Asahi Linux is the main reason a modern Apple Silicon Mac can be used as a daily-driver Linux machine, so its licensing stance directly shapes whether downstream distros, vendors and commercial spin-offs can build on years of reverse-engineering effort. The dispute highlights a recurring tension in open-source hardware enablement: permissive licensing maximizes adoption but makes it easy for others to fork, rebrand and monetize the original work. Asahi's code is deliberately dual-licensed under both the upstream license (typically GPL) and a permissive license such as MIT, and the report suggests that policy is now being reconsidered in light of the alleged hijacking attempts; the post itself is a status update rather than a feature-release announcement. Notably, the biggest user-facing gaps remain practical ones — one commenter says missing USB-C external display support is the single blocker keeping them off Asahi.

hackernews · ackyshake · Nov 7, 05:20 · [Discussion](https://news.ycombinator.com/item?id=50401867)

**Background**: Asahi Linux is a community project that ports the Linux kernel and related software to Apple Silicon Macs, the Arm-based systems-on-chip Apple has used since late 2020. Because Apple publishes no documentation for these chips, the team reverse-engineers the SoCs to write drivers for the GPU, display, audio and other blocks, and upstreams the results. Its flagship distribution is Fedora Asahi Remix, a collaboration with the Fedora Project, and Apple explicitly permits booting unsigned custom kernels on Macs, which makes the whole effort possible.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Asahi_Linux">Asahi Linux - Wikipedia</a></li>
<li><a href="https://asahilinux.org/about/">About - Asahi Linux What Is Asahi Linux? Asahi Linux - GeeksforGeeks Asahi Linux - GitHub Unveiling Asahi Linux: A Technical Deep-Dive - linuxvox.com</a></li>
<li><a href="https://support.apple.com/en-us/116943">Mac computers with Apple silicon - Apple Support</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly supportive but pushed on two fronts: several asked whether the licensing warning targets Omarchy and expressed surprise that the work was ever MIT-licensed rather than GPL-only, while others said the missing USB-C display support is the dealbreaker keeping them on macOS. A developer also promoted a competing effort, Gravity Linux, claiming Vulkan 1.4, M4 and most of M5 support, and full suspend-to-RAM — features no Asahi release offers yet — prompting readers to weigh Asahi against alternatives like the Framework laptop.

**Tags**: `#linux`, `#apple-silicon`, `#asahi-linux`, `#open-source-licensing`, `#hardware-support`

---

<a id="item-13"></a>
## [Retrospective on Borland Turbo Pascal 7 and Its Blazing-Fast IDE](https://kevinboone.me/tpwin.html) ⭐️ 7.0/10

Developer Kevin Boone published a technically grounded retrospective on Borland Turbo Pascal 7, examining why its fast, tightly integrated development environment still outperforms much of today's tooling in responsiveness. The piece sparked a large Hacker News discussion (162 points, roughly 90 comments) in which veteran programmers shared firsthand memories of the compiler and IDE. The article lands in an ongoing debate about how modern IDEs and build systems have grown heavy and slow, and it uses Turbo Pascal 7 as a concrete benchmark for what a sub-second edit-compile-run loop feels like. For developers and tool builders, it is a reminder that compilation speed and integration are design choices with real effects on how people learn and iterate. Turbo Pascal 7, released by Borland in 1992 and originally written by Anders Hejlsberg, was famous for compiling and linking programs almost instantly on contemporary MS-DOS hardware, all inside a single full-screen editor with an integrated debugger and inline assembly support. The article and commenters note the counterpoint that TP's speed came partly from the simplicity of the Pascal language and the era's small program sizes, so the comparison with modern toolchains is not entirely like-for-like.

hackernews · andsoitis · Nov 7, 16:06 · [Discussion](https://news.ycombinator.com/item?id=50405678)

**Background**: Turbo Pascal is a Pascal compiler and integrated development environment originally developed by Anders Hejlsberg at Borland, running on CP/M and MS-DOS and notable for its very fast compiling; Turbo Pascal and the later Turbo C made Borland a leader in PC-based development tools. Version 7.0, documented in a 1992 user's guide, added new capabilities while remaining compatible with code written for earlier versions. Its all-in-one design — editor, compiler, linker, and debugger in a single executable launched from the DOS prompt — became a template for later IDEs such as Delphi, which succeeded it.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Turbo_Pascal">Turbo Pascal - Wikipedia</a></li>
<li><a href="https://winworldpc.com/product/turbo-pascal/7x">Borland Turbo Pascal 7.x - WinWorld</a></li>
<li><a href="https://turbopascal.org/wp-content/uploads/Turbo_Pascal_Version_7.0_Users_Guide_1992.pdf">USER'S GUIDE - turbopascal.org</a></li>

</ul>
</details>

**Discussion**: Commenters were overwhelmingly nostalgic and grateful, describing Turbo Pascal as the tool that taught them to program as teenagers, with several noting its inline assembly support as their gateway into low-level programming. A recurring regret was that Delphi never achieved the mainstream success of Visual Basic despite being, in their view, a superior environment; others linked classic essays on compilation speed and echoed the article's worry that few developers today could build something like TP.

**Tags**: `#turbo-pascal`, `#compilers`, `#programming-history`, `#ide-tooling`, `#retrospective`

---

<a id="item-14"></a>
## [Oracle Reportedly Cancels $7B AI Chip Lease Deal With Tencent](https://t.me/zaihuapd/44975) ⭐️ 7.0/10

Oracle has reportedly cancelled a five-year agreement worth roughly $7 billion to lease about 100,000 advanced AI chips to Tencent, after US officials raised concerns about the deal and the company came under pressure from the Trump administration. The arrangement, signed by Tencent this year, would have let the Chinese firm access chips it cannot obtain inside China by renting capacity through Oracle data centers in Southeast Asia. The cancellation signals that US export-control enforcement is now extending beyond direct chip sales to third-party cloud and leasing arrangements, making it harder for Chinese AI firms to route around restrictions via overseas data centers. If such deals are consistently blocked, Chinese companies will face tighter AI compute supply and will be pushed further toward domestic accelerators, reshaping global AI infrastructure supply chains. The deal was reportedly structured with an upfront payment accounting for about 30% of the total value, and the compute was to be delivered through multiple Oracle data centers in Southeast Asia rather than on Chinese soil. The report originates from a short, unverified Telegram news blurb citing TradingView, with no confirmation from Oracle, Tencent, or US officials, and no public disclosure of which specific chip models were involved.

telegram · zaihuapd · Nov 7, 02:00

**Background**: US export controls restrict the sale of advanced AI accelerators such as Nvidia's top-end GPUs to China, which has driven Chinese technology companies to seek compute through overseas cloud providers and data centers instead. Oracle has been expanding its AI cloud infrastructure rapidly, including in Southeast Asia, making it a plausible partner for such leasing arrangements. This type of transregional lease sits in a grey zone of the rules, and Washington has increasingly signaled that it views rented compute abroad as a form of controlled technology transfer.

**Tags**: `#AI chips`, `#export controls`, `#geopolitics`, `#AI infrastructure`, `#Tencent`

---

<a id="item-15"></a>
## [Apple Said to Train China-Only LLM With Alibaba, May Be First Foreign Firm Approved](https://t.me/zaihuapd/44977) ⭐️ 7.0/10

People familiar with the matter told Reuters that Apple has trained a large language model specifically for the Chinese market with support from Alibaba, abandoning its earlier strategy of relying on third-party models. Apple Intelligence is expected to launch in China in the coming months via an iOS update, and the Cyberspace Administration of China reportedly filed/registered its generative AI service last month. If the approval goes through, Apple would become the first foreign company allowed to offer its own AI model in China, a notable shift in how Beijing regulates generative AI services. It would also give Apple direct control over the AI experience on iPhones in its second-largest market, where rivals such as Huawei and Xiaomi are shipping aggressively marketed on-device AI features. The report is based on unnamed sources and has not been confirmed by Apple, Alibaba or Chinese regulators, so the timing and scope remain uncertain. Regulatory clearance in China hinges on generative AI service filing with the Cyberspace Administration of China, a process that requires security assessments and content-safety compliance rather than a purely technical review.

telegram · zaihuapd · Nov 7, 03:06

**Background**: Apple Intelligence is Apple's suite of AI features announced at WWDC 2024, which runs a mix of on-device and server-side models across iOS 18, iPadOS 18 and macOS Sequoia, and integrates third-party chatbots such as ChatGPT. China requires any public-facing generative AI service to complete a filing with the Cyberspace Administration of China, the country's top internet regulator, before launch — which is why Apple could not simply ship its global AI stack there. Previously, reports suggested Apple was negotiating with Chinese AI providers to supply models for the China market.

<details><summary>References</summary>
<ul>
<li><a href="https://maccome.com/en/blog/2026-apple-intelligence-china-qwen-baidu.html">Apple Intelligence Finally Gets Approved in China ... | MACCOME</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cyberspace_Administration_of_China">Cyberspace Administration of China - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#AI/ML`, `#China tech policy`, `#LLM`, `#Alibaba`

---

<a id="item-16"></a>
## [Claude Code reportedly leaked users' login emails via web search requests](https://github.com/anthropics/claude-code/issues/107757) ⭐️ 7.0/10

Developers reported that Claude Code was silently inserting users' login email addresses into outbound web requests, so that sites such as Wikipedia and the U.S. SEC received the address, and at least one user reported receiving large volumes of spam as a result. An Anthropic engineer confirmed the email had been placed in the model context to stop Claude from inventing author names, said version 2.1.317 added a filter that can still be bypassed with a Python script, and stated that the login email will be removed from the context in an upcoming release. Claude Code is a widely used agentic coding tool that runs with broad local permissions, so a leak of personally identifiable information through its own network requests is a trust problem for every developer using it in a corporate or open-source setting. It also shows how a well-intentioned prompt-engineering workaround can turn into a privacy incident once the model is allowed to browse the web. The issue was first reported back in July, and the current mitigation in version 2.1.317 is a filter rather than a removal of the data, so it can be circumvented—for example by a Python script—until the email is actually taken out of the model context in the next release. Because the address is exposed to arbitrary third-party sites during web fetches, the practical risk is targeted spam, phishing, and correlation of a developer's identity with their browsing activity.

telegram · zaihuapd · Nov 7, 08:09

**Background**: Claude Code is Anthropic's agentic coding tool that runs in the terminal and IDE, letting the model read a codebase, edit files, run commands, and fetch web pages on the user's behalf. To do that, the tool assembles a "context"—the background information fed to the model alongside each prompt—which in this case included the account's login email. Sending any part of that context to external websites means third parties can log it, which is normally something developers assume won't happen when an assistant searches the web.

<details><summary>References</summary>
<ul>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI coding agent and assistant</a></li>
<li><a href="https://www.salesforce.com/artificial-intelligence/ai-context/">What is AI Context, and How Does it Work? | Salesforce</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#security`, `#claude-code`, `#ai-tooling`, `#anthropic`

---

<a id="item-17"></a>
## [$8 Linux Computer: Hacking Ultra-Cheap Hardware](http://thelittleengineerthatcould.blogspot.com/2022/12/the-8-linux-computer.html) ⭐️ 6.0/10

A 2022 blog post about getting Linux running on an $8 piece of hardware has resurfaced on Hacker News, where a 174-point thread gathered practical tips on cheap Linux-capable boards and repurposed devices. It shows how hobbyists can turn extremely cheap or discarded hardware into functional Linux systems, which matters for low-cost IoT, education, and embedded experimentation even if the niche remains far from mainstream. Commenters cite options such as the $15-20 LicheeRV Nano on SG2002 with USB OTG, GPIO and microSD boot but no CPU governor, a ~€10 UZ801 4G dongle running OpenWrt with only 384MB RAM and 2GB flash, and the once-$5 Pi Zero; others warn that boards like the Ox64 suffered from incomplete peripheral support and stale kernels.

hackernews · zenincognito · Nov 7, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50404599)

**Background**: Embedded Linux means running the Linux kernel and user-space software on resource-constrained devices, from routers to tiny computers. A single-board computer (SBC) puts the processor, memory, I/O and other core components on one circuit board, making it easy to boot a full OS. OpenWrt is a lightweight, open-source Linux distribution built for embedded devices such as routers, with a writable filesystem and package management.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenWrt">OpenWrt</a></li>
<li><a href="https://en.wikipedia.org/wiki/Single-board_computer">Single-board computer</a></li>
<li><a href="https://en.wikipedia.org/wiki/Embedded_Linux">Embedded Linux</a></li>

</ul>
</details>

**Discussion**: The discussion is nostalgic and enthusiastic: one commenter fondly recalls repurposing kid-oriented or router hardware to get a Linux shell, while others share concrete buys like the LicheeRV Nano and UZ801 dongle. Enthusiasm is tempered by caveats, including missing CPU governors and poor support on the Ox64, and by the observation that cheap MCUs have stolen some of the thunder from full embedded Linux.

**Tags**: `#embedded-linux`, `#hardware-hacking`, `#low-cost-computing`, `#single-board-computers`, `#openwrt`

---

<a id="item-18"></a>
## [Harsh peer review accuses ML paper of being AI-generated and jargon-filled](https://www.reddit.com/r/MachineLearning/comments/1xpu1eq/the_most_scathing_reviewer_2_review_i_have_ever/) ⭐️ 6.0/10

A Reddit post shares an official review of Submission21893 in which Reviewer Xz8e gives a rating of 1 (clear rejection) and alleges that the machine learning paper is highly likely to be fully AI-generated. The review criticizes the paper for technical inaccuracies, undefined jargon, vague methods, and experiments that lack basic reporting such as random seeds, task descriptions, and metric explanations. This matters because it highlights growing concerns about AI-generated submissions burdening peer review and undermining trust in academic publishing, especially in fast-moving fields such as machine learning. It also illustrates how reviewers are increasingly asked to detect not only weak science but also whether authors understand the technical language they use. The reviewer quotes numerous unexplained phrases such as “scalar uncertainty,” “sparse latent dynamics,” “nominal imagination,” and “within-time DAG,” arguing that they are stitched together without clear definitions or motivation. The review also notes conflated notation, an unmotivated training objective, no reported random seeds, and no clear explanation of tasks or metrics, while stating confidence 4 based on substantial direct research experience.

reddit · r/MachineLearning · /u/MOSFETBJT · Nov 7, 01:30

**Background**: A world model is an AI system that learns an internal representation of an environment and predicts how that environment changes in response to actions. Latent-state representation learning compresses observations into lower-dimensional states that can be used for planning or control. In reinforcement learning, pessimistic objectives deliberately penalize uncertainty so that policies avoid unreliable regions, which is the kind of setting the reviewed paper claims to address.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/World_model_(artificial_intelligence)">World model (artificial intelligence) - Wikipedia</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/world-models/">What Is a World Model? | NVIDIA Glossary</a></li>
<li><a href="https://arxiv.org/pdf/1905.12621.pdf">Learning latent state representation for speeding up exploration</a></li>

</ul>
</details>

**Tags**: `#peer review`, `#AI-generated content`, `#machine learning`, `#research integrity`, `#academic publishing`

---

<a id="item-19"></a>
## [Pointer Networks Solve TSP Instantly but Degrade at Scale, Benchmark vs OR-Tools Shows](https://www.reddit.com/r/MachineLearning/comments/1xqgg4v/combinatorial_optimization_with_pointer_networks/) ⭐️ 6.0/10

A first-time public technical write-up benchmarks Pointer Networks (trained end-to-end with the REINFORCE policy-gradient algorithm) on the 2D Euclidean Travelling Salesman Problem against Google OR-Tools' Guided Local Search with a 10-second timeout, sweeping problem sizes from N=20 up to N=200. The author reports that although the neural model constructs tours in fractions of a millisecond, solution quality decays markedly as instance size grows. The article gives a concrete, head-to-head comparison between learned constructive heuristics and a mature classical solver, which is exactly the kind of evidence practitioners need before adopting neural approaches in routing and scheduling pipelines. Its diagnosis of why performance falls off — an architectural mismatch rather than a training issue — points the field toward permutation-invariant encoders (such as attention-based ones) as the path forward. The author attributes the quality decay to the LSTM encoder, which imposes an artificial sequential order and recency bias on a set of coordinates, conflicting with the permutation-invariant nature of geometric graphs. The comparison is also asymmetric in a favourable way for the baseline: OR-Tools is allowed a fixed 10-second budget per instance while the network runs in sub-millisecond time.

reddit · r/MachineLearning · /u/an2ancan · Nov 7, 20:44

**Background**: Pointer Networks are a neural architecture that extends sequence-to-sequence attention by pointing directly at elements of the input sequence instead of generating tokens from a fixed output vocabulary, which makes them naturally suited to problems whose output is a permutation of the input — such as the Travelling Salesman Problem, where the goal is to find the shortest tour visiting a set of cities exactly once. The classical way to train such models is supervised imitation of optimal tours, but REINFORCE, a policy-gradient reinforcement learning algorithm introduced by Ronald J. Williams in 1992, instead learns directly from the tour-length reward, removing the need for labelled optimal solutions. Google OR-Tools is a free, open-source operations-research suite for constraint optimization, linear and mixed-integer programming, and vehicle routing, and its Guided Local Search metaheuristic is a strong classical baseline for the TSP.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/pubs/pointer-networks/">Pointer Networks</a></li>
<li><a href="https://en.wikipedia.org/wiki/REINFORCE_algorithm">REINFORCE algorithm</a></li>
<li><a href="https://en.wikipedia.org/wiki/OR-Tools">OR - Tools - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#pointer-networks`, `#combinatorial-optimization`, `#travelling-salesman-problem`, `#reinforcement-learning`, `#benchmarking`

---

<a id="item-20"></a>
## [OnlyFake founder confesses to AI fake ID fraud, deported from US](https://www.404media.co/an-ai-fraud-kingpins-confessions/) ⭐️ 6.0/10

Yurii Nazarenko, creator of the AI-powered fake ID site OnlyFake, pleaded guilty in US federal court to selling more than 10,000 counterfeit digital identity documents, was sentenced to roughly the year of jail time he had already served, and was then deported after months in ICE custody. He is now permanently barred from re-entering the United States. The case is an early, concrete example of a generative-AI service industrialized identity fraud, selling fake driver's licenses for all 50 US states and passports from roughly 56 countries at prices as low as $15. Its documents were reportedly used to slip past KYC checks and by North Korean fake IT workers, showing how cheap synthetic documents undermine remote identity verification across finance, hiring, and border control. OnlyFake operated from 2021 to 2024, accepted only cryptocurrency, and automatically populated customer-supplied data into template documents; Nazarenko had earlier spent about a week hand-forging each passport pixel by pixel in Photoshop before building the automated site. The charges he faced carried a maximum of 15 years, and UN experts reportedly wrote to raise alarm about the platform's use by North Korean IT workers.

telegram · zaihuapd · Nov 7, 10:54

**Background**: Identity documents such as driver's licenses and passports are the backbone of remote verification: banks, crypto exchanges, and employers use KYC (Know Your Customer) checks that rely on users uploading photos of an ID plus a selfie. Generative AI makes producing realistic document images fast and cheap, so fraudsters no longer need Photoshop skills — and detection increasingly depends on liveness checks, document forensics, and cross-checking against issuer databases.

<details><summary>References</summary>
<ul>
<li><a href="https://www.justice.gov/usao-sdny/pr/creator-onlyfake-charged-and-pleads-guilty-selling-more-10000-digital-fake">Southern District of New York | Creator Of “OnlyFake” Charged ...</a></li>
<li><a href="https://www.bitdefender.com/en-us/blog/hotforsecurity/onlyfake-fakeid-creator-guilty-charged">Creator of ‘OnlyFake’ Pleads Guilty - Bitdefender</a></li>
<li><a href="https://didit.me/blog/generative-ai-document-fraud/">Generative AI & Document Fraud: A Guide. - didit.me</a></li>

</ul>
</details>

**Tags**: `#AI misuse`, `#identity fraud`, `#cybersecurity`, `#generative AI`, `#law enforcement`

---

<a id="item-21"></a>
## [Consumer Files Class Action Against Anthropic Over Alleged Misleading Max Plan Usage Limits](https://t.me/zaihuapd/44989) ⭐️ 6.0/10

Washington D.C. consumer Karl Kahn filed a class action lawsuit against Anthropic, alleging that the $100/month Max 5x and $200/month Max 20x subscription plans deliver far lower usage limits than advertised, despite being marketed as offering 5x and 20x the usage of the base $20 Claude Pro plan. The suit reportedly seeks refunds for users who purchased these plans since April of last year. This is one of the earliest legal challenges to how AI companies price and describe premium subscription tiers, and it could push the entire industry toward clearer, more quantifiable disclosure of usage caps. If it gains traction, it may affect how Anthropic and competitors like OpenAI structure and market their high-end consumer plans. The core dispute centers on measurability: Anthropic does not publish concrete message or token counts for its plans, instead relying on dynamic limits that vary with conversation length, model choice, and feature usage such as Claude Code, so users argue the advertised "5x" and "20x" multipliers cannot be verified or relied upon. The complaint also raises transparency concerns about how usage is calculated and communicated to paying subscribers.

telegram · zaihuapd · Nov 7, 12:44

**Background**: Anthropic sells Claude through consumer subscriptions: a free tier, a Claude Pro plan at roughly $20 per month, and two premium Claude Max tiers launched in 2024 at $100 and $200 per month for heavy users. Unlike API billing, which charges per token, subscription plans use soft, dynamically adjusted usage limits that Anthropic intentionally leaves vague to prevent abuse and manage capacity. Because these percentages are relative and the baseline itself shifts, "5x" and "20x" are hard for customers to independently verify, which is the gap the lawsuit targets.

<details><summary>References</summary>
<ul>
<li><a href="https://support.claude.com/en/articles/8325606-what-is-the-pro-plan">What is the Pro plan? | Claude Help Center</a></li>
<li><a href="https://blog.laozhang.ai/en/posts/claude-usage-limits-by-plan">Claude Usage Limits by Plan: What 5x and... | LaoZhang AI Blog</a></li>
<li><a href="https://gravity.fast/blog/claude-pricing-explained/">Claude Pricing 2026: Free, Pro, Max , Team and API Costs</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI subscriptions`, `#class action lawsuit`, `#consumer protection`, `#AI industry`

---