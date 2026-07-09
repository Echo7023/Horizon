---
layout: default
title: "Horizon Summary: 2026-07-09 (EN)"
date: 2026-07-09
lang: en
---

> From 40 items, 14 important content pieces were selected

---

1. [TypeScript 7.0: Rust Rewrite Boosts Compilation 8-12x](#item-1) ⭐️ 10.0/10
2. [Rewriting Bun from Zig to Rust Using AI Agents](#item-2) ⭐️ 9.0/10
3. [Critical Android Remote Root Exploit Chain Disclosed](#item-3) ⭐️ 9.0/10
4. [Deere Must Allow Repairs Under FTC Settlement](#item-4) ⭐️ 8.0/10
5. [Chatto open-sourced: self-hosted chat using NATS](#item-5) ⭐️ 8.0/10
6. [Microsoft releases Flint, a visualization language for AI agents](#item-6) ⭐️ 8.0/10
7. [OpenAI Launches GPT-Live Real-Time Voice Mode](#item-7) ⭐️ 8.0/10
8. [Cloudflare Meerkat: Leaderless Global Consensus](#item-8) ⭐️ 8.0/10
9. [EU revives private message scanning rules, one step away](#item-9) ⭐️ 8.0/10
10. [LingBot-Video: Open-Source Sparse-MoE Video Diffusion Transformer](#item-10) ⭐️ 8.0/10
11. [Alibaba Bans Employees from Using Anthropic's Claude](#item-11) ⭐️ 8.0/10
12. [Huawei 5G flagship returns overseas, peak speed over 1100 Mbps](#item-12) ⭐️ 8.0/10
13. [Cloudflare and OpenAI Pilot to Optimize AI Search with Network Data](#item-13) ⭐️ 8.0/10
14. [LineageOS Launches Browser-Based Flashing Tool](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [TypeScript 7.0: Rust Rewrite Boosts Compilation 8-12x](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 10.0/10

Microsoft has announced TypeScript 7.0, a major version that rewrites the compiler in Rust, achieving 8-12x faster compilation times compared to TypeScript 6.0. This is a groundbreaking performance leap for one of the most widely used programming languages, dramatically reducing build times and enabling faster development cycles for millions of developers. The new compiler, codenamed tsgo, is not self-hosted; it is a ground-up rewrite in Rust that ports the existing TypeScript compiler structure. Benchmarks show build time for VS Code dropped from 125.7 seconds to 10.6 seconds.

hackernews · DanRosenwasser · Jul 8, 16:06 · [Discussion](https://news.ycombinator.com/item?id=48833715)

**Background**: TypeScript is a typed superset of JavaScript that compiles to plain JavaScript. Its original compiler (tsc) was written in TypeScript itself, which led to performance bottlenecks on large codebases. The Rust rewrite leverages native code performance to drastically speed up compilation and editor startup.

<details><summary>References</summary>
<ul>
<li><a href="https://devblogs.microsoft.com/typescript/typescript-native-port/">A 10x Faster TypeScript - TypeScript</a></li>
<li><a href="https://www.techtimes.com/articles/318666/20260618/typescript-70-rc-ships-go-compiler-cuts-vs-code-build-time-77-seconds-seven.htm">TypeScript 7.0 RC Ships: Go Compiler Cuts VS Code Build Time From 77 Seconds to Seven</a></li>
<li><a href="https://www.totaltypescript.com/rewriting-typescript-in-rust">Rewriting TypeScript in Rust? You'd have to be... | Total TypeScript</a></li>

</ul>
</details>

**Discussion**: The community response is overwhelmingly positive, with many congratulating the team on the engineering feat. Commenters shared benchmarks showing 7.7x to 11.9x speedups, and discussed the challenge of maintaining two codebases during the rewrite. Some noted the tension between using Go vs Rust, but overall the sentiment is excitement about the performance gains.

**Tags**: `#TypeScript`, `#performance`, `#compilers`, `#programming languages`, `#Microsoft`

---

<a id="item-2"></a>
## [Rewriting Bun from Zig to Rust Using AI Agents](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/#atom-everything) ⭐️ 9.0/10

Jarred Sumner, creator of Bun, rewrote the entire JavaScript runtime from Zig to Rust using advanced agentic engineering techniques, completing the rewrite in 11 days with the help of coding agents like Mythos/Fable and Claude Code. This demonstrates that AI coding agents can now enable large-scale rewrites that were previously considered too risky, potentially transforming how software is maintained and upgraded. The rewrite also addresses major memory safety issues in Bun, improving stability and performance. The rewrite cost approximately $165,000 in API tokens (5.9B input, 690M output), reduced binary size by 20%, improved startup time by 10% on Linux, and fixed numerous memory bugs including use-after-free and double-free errors that plagued the Zig version.

rss · Simon Willison · Jul 8, 23:57

**Background**: Bun is a fast JavaScript runtime and bundler originally written in Zig. Zig is a low-level systems language that offers manual memory management, while Rust is a memory-safe systems language with compile-time guarantees. The Bun rewrite used a suite of AI coding agents orchestrated by a human engineer, leveraging the existing TypeScript test suite as a conformance suite to validate correctness.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/agentic-engineering">What is Agentic Engineering? | IBM</a></li>
<li><a href="https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/">What is agentic engineering? - Agentic Engineering Patterns - Simon Willison's Weblog</a></li>

</ul>
</details>

**Discussion**: Commenters expressed mixed reactions: some praised the disciplined engineering approach with human oversight, while others criticized the abandonment of the Zig version without LTS support for critical fixes. Some noted the cost of $165k is far cheaper than a year of a software engineering team's salary for such a massive rewrite.

**Tags**: `#Bun`, `#Rust`, `#Zig`, `#runtime`, `#software engineering`

---

<a id="item-3"></a>
## [Critical Android Remote Root Exploit Chain Disclosed](https://www.coolapk.com/feed/72700258?s=ZGQ2MTVlZjYxMDYyNTM3ZzZhNGUzOThjega1640) ⭐️ 9.0/10

On July 8, 2026, cybersecurity firm Nebula disclosed a remote root exploit chain affecting all Android versions up to Android 17, combining a Firefox browser vulnerability (up to version 151.0.2) and a 15-year-old Linux kernel privilege escalation flaw (CVE-2026-43499, dubbed GhostLock). This exploit chain allows attackers to gain persistent root access to any vulnerable Android device simply by tricking a user into clicking a malicious link, posing an immediate and severe threat to billions of Android users worldwide. The proof-of-concept code has been uploaded to GitHub, and while full exploit details are withheld, the Linux kernel patch has been released. Google Pixel devices have been successfully tested, and the exploit chain can implant privilege files and gain root access within one minute.

telegram · zaihuapd · Jul 8, 13:01

**Background**: A remote root exploit chain uses multiple vulnerabilities to achieve code execution and privilege escalation over the network without physical access. The disclosed chain exploits a Firefox browser vulnerability to escape the browser sandbox and then leverages the GhostLock Linux kernel flaw to gain full root control of the Android device. This type of attack is critical because it requires no user action beyond clicking a link and can affect a wide range of devices due to the kernel vulnerability's long-standing presence.

<details><summary>References</summary>
<ul>
<li><a href="https://cybersecuritynews.com/15-year-old-ghostlock-linux-kernel-vulnerability/">15-year-old GhostLock Linux Kernel Vulnerability Enables Privilege Escalation Attacks</a></li>
<li><a href="https://thehackernews.com/2026/07/15-year-old-ghostlock-flaw-enables-root.html">15-Year-Old GhostLock Flaw Enables Root and Container Escape on Most Linux Distros</a></li>
<li><a href="https://cybersecuritynews.com/firefox-152-vulnerabilities/">Multiple Vulnerabilities in Firefox 152 Enables Remote Code Execution Attacks</a></li>

</ul>
</details>

**Tags**: `#Android`, `#vulnerability`, `#security`, `#root`, `#exploit`

---

<a id="item-4"></a>
## [Deere Must Allow Repairs Under FTC Settlement](https://apnews.com/article/john-deere-right-to-repair-agriculture-equipment-cb7514ffedb95c130a976af661f2bc02) ⭐️ 8.0/10

The Federal Trade Commission (FTC) reached a settlement with Deere & Company, requiring the farm equipment manufacturer to allow owners and independent repair shops to repair their equipment. Deere must provide access to diagnostic tools, manuals, and software, and pay $1 million to five states for antitrust enforcement costs. This settlement is a significant victory for the right-to-repair movement, potentially setting a precedent for other industries like automotive and electronics. It empowers farmers to fix their own equipment, reducing costs and downtime, and challenges repair monopolies that have restricted consumer choice. Deere will be subject to 10 years of compliance oversight, and the $1 million fine is relatively small compared to its profits. The settlement specifically addresses access to software tools that have been a major barrier for farmers seeking to repair modern, software-dependent equipment.

hackernews · djoldman · Jul 8, 23:37 · [Discussion](https://news.ycombinator.com/item?id=48838876)

**Background**: The right-to-repair movement advocates for consumers' and independent repair shops' ability to repair products they own, opposing manufacturer practices that restrict access to parts, tools, and software. In agriculture, modern tractors and combines are equipped with sophisticated software, and manufacturers like Deere have been criticized for making repairs dependent on dealer technicians. The FTC's action follows years of advocacy and state-level legislative efforts to grant repair rights.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Right_to_repair_movement">Right to repair movement</a></li>
<li><a href="https://en.wikipedia.org/wiki/Right_to_repair">Right to repair - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters praised the outcome but criticized the small fine, with one noting it 'probably $10 billion in profit' versus $1 million. Others highlighted the work of right-to-repair advocate Louis Rossmann and hoped the standard would extend to cars. There was also a cynical remark about the site's hypocrisy regarding regulatory capture.

**Tags**: `#right-to-repair`, `#FTC`, `#John Deere`, `#consumer rights`, `#legal`

---

<a id="item-5"></a>
## [Chatto open-sourced: self-hosted chat using NATS](https://www.hmans.dev/blog/chatto-is-open-source) ⭐️ 8.0/10

Chatto, a self-hosted chat application built on NATS, has been released as open source under an unspecified license, making its codebase publicly available on GitHub. This release offers a modern, easy-to-self-host alternative to proprietary chat platforms like Discord or Slack, with NATS providing lightweight messaging and built-in persistence, appealing to privacy-conscious users and developers. Chatto ships as a compact self-contained binary, uses NATS for messaging and stream persistence, and supports S3-compatible object storage for media files. It is designed for easy deployment on personal infrastructure.

hackernews · speckx · Jul 8, 15:19 · [Discussion](https://news.ycombinator.com/item?id=48833116)

**Background**: NATS is a high-performance, open-source messaging system under the Cloud Native Computing Foundation, written in Go, supporting pub/sub, streaming, and object storage. Agentic coding refers to using AI agents to autonomously plan, write, test, and modify code with minimal human input. The developer used agentic coding to build Chatto single-handedly.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NATS_Messaging">NATS Messaging - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agentic_coding">Agentic coding</a></li>
<li><a href="https://nats.io/">NATS.io - Cloud Native, Open Source, High-performance Messaging</a></li>

</ul>
</details>

**Discussion**: Community comments were generally positive, praising the ease of self-hosting and the use of NATS. Some noted feature gaps compared to Discord, such as multi-community access, and raised enterprise concerns like soft delete for work messages. One humorous comment joked that open-sourcing allows users to verify if an AI is judging them, referencing the trend of AI integration in chat apps.

**Tags**: `#open source`, `#chat`, `#self-hosted`, `#NATS`, `#agentic coding`

---

<a id="item-6"></a>
## [Microsoft releases Flint, a visualization language for AI agents](https://microsoft.github.io/flint-chart/#/) ⭐️ 8.0/10

Microsoft has open-sourced Flint, a visualization intermediate language designed to improve the reliability of AI agents in generating charts by providing a high-level specification that a compiler optimizes into detailed chart layouts. Flint addresses a key challenge in AI-driven data visualization: balancing simplicity and quality. By offloading low-level visual decisions to a compiler, it enables AI agents to produce polished charts more reliably, which could accelerate the adoption of AI in data analytics workflows. Flint uses a 'semantic-type based specification' and includes a layout optimization engine that automatically adds details like scales, axes, and spacing from high-level intent. It also provides a MCP server for easy integration with existing agent applications.

hackernews · chenglong-hn · Jul 8, 17:46 · [Discussion](https://news.ycombinator.com/item?id=48834924)

**Background**: Data visualization languages like Vega or D3 are expressive but require specifying many low-level details. Large language models (LLMs) can generate code but often struggle with reliable chart generation because they must explicitly manage visual encodings. Flint acts as an intermediate layer: AI agents output a concise high-level specification, and a deterministic compiler handles the rest, improving consistency.

**Discussion**: The community comments show mixed reactions. Some praise Flint as a practical example of a 'deterministic layer' pattern emerging in agent systems. Others question how it compares to Vega, suggesting that Vega already serves as a good intermediate representation. Some commenters report that they have not encountered the reliability issues Flint aims to solve, with LLMs performing well using Python and R for visualization. One commenter argues that Microsoft conflates low-level verbosity with LLMs' actual difficulty in spatial composition.

**Tags**: `#visualization`, `#AI agents`, `#Microsoft`, `#LLM`, `#chart generation`

---

<a id="item-7"></a>
## [OpenAI Launches GPT-Live Real-Time Voice Mode](https://openai.com/index/introducing-gpt-live/) ⭐️ 8.0/10

OpenAI introduced GPT-Live, a real-time voice mode that allows users to have natural conversations with AI, and can delegate complex reasoning tasks to GPT-5.5. This marks a significant step toward more natural human-AI interaction, bridging the gap between voice assistants and frontier AI models, potentially changing how people use AI for productivity and companionship. GPT-Live is the first version of this voice mode, and it can delegate questions to GPT-5.5 in the background, meaning users are not limited to a less capable voice-specific model.

hackernews · logickkk1 · Jul 8, 17:03 · [Discussion](https://news.ycombinator.com/item?id=48834405)

**Background**: GPT-Live is a new voice interface from OpenAI that enables real-time spoken conversations. GPT-5.5, released on April 23, 2026, is a large language model codenamed 'Spud' that achieves high benchmarks in reasoning tasks. The combination allows for more fluid interactions that can leverage advanced reasoning without noticeable delays.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT-5.5</a></li>

</ul>
</details>

**Discussion**: Comments were mixed: simonw praised its usefulness for long conversations, while others like jonstaab and overgard expressed concerns about AI replacing human relationships. artdigital noted the lack of tool integration in voice mode. Atty from OpenAI confirmed it is the first version.

**Tags**: `#AI`, `#voice assistant`, `#OpenAI`, `#GPT-5.5`, `#real-time interaction`

---

<a id="item-8"></a>
## [Cloudflare Meerkat: Leaderless Global Consensus](https://blog.cloudflare.com/meerkat-introduction/) ⭐️ 8.0/10

Cloudflare announced Meerkat, a globally distributed consensus algorithm using the leaderless, asynchronous QuePaxa protocol. This is the first production implementation of QuePaxa. Meerkat could improve performance under unpredictable network conditions by eliminating leader dependencies and timeouts. It offers an alternative to traditional consensus algorithms like Raft and Paxos for globally distributed systems. Meerkat is not yet in production. It requires global consensus for every read operation, potentially increasing read latency compared to systems with local reads.

hackernews · bobnamob · Jul 8, 13:18 · [Discussion](https://news.ycombinator.com/item?id=48831565)

**Background**: Consensus algorithms ensure multiple nodes agree on a value. Partially synchronous algorithms (e.g., Paxos, Raft) rely on timeouts and assume bounded message delays. Asynchronous algorithms like QuePaxa do not rely on timeouts, making progress even under arbitrary delay fluctuations. Meerkat implements QuePaxa in a global scale.

**Discussion**: Commenters debated the novelty of Meerkat compared to existing leaderless protocols, with some questioning the comparison to Raft. Others noted the significance of a production asynchronous algorithm and expressed caution about real-world performance, especially for read operations.

**Tags**: `#distributed systems`, `#consensus algorithms`, `#cloudflare`, `#meerkat`, `#quepaxa`

---

<a id="item-9"></a>
## [EU revives private message scanning rules, one step away](https://cyberinsider.com/eu-now-one-step-away-from-reviving-private-message-scanning-rules/) ⭐️ 8.0/10

The European Union has advanced legislation that could mandate scanning of private messages, potentially breaking end-to-end encryption, bringing it one step closer to enactment. This move threatens to undermine digital privacy and encryption for millions of EU citizens, setting a precedent for government surveillance of private communications. The proposal includes two versions: Chat Control 1.0 allows voluntary scanning by tech companies, while Chat Control 2.0 mandates scanning and bans end-to-end encryption.

hackernews · ggirelli · Jul 8, 16:53 · [Discussion](https://news.ycombinator.com/item?id=48834296)

**Background**: The EU has long debated measures to combat child sexual abuse material, but previous proposals faced strong opposition from privacy advocates and tech companies. Client-side scanning would analyze messages on users' devices before encryption, raising significant privacy concerns.

**Discussion**: Commenters expressed concern over the Internet Watch Foundation pushing for client-side scanning, and noted a key distinction between voluntary (Chat Control 1.0) and mandatory (Chat Control 2.0) scanning, with the latter seen as far more dangerous.

**Tags**: `#privacy`, `#encryption`, `#EU regulation`, `#surveillance`, `#technology policy`

---

<a id="item-10"></a>
## [LingBot-Video: Open-Source Sparse-MoE Video Diffusion Transformer](https://www.reddit.com/r/MachineLearning/comments/1ur0bxq/lingbotvideo_sparsemoe_video_diffusion/) ⭐️ 8.0/10

LingBot-Video is a 13B-parameter video diffusion transformer using a DeepSeek-V3-style sparse mixture-of-experts (MoE) architecture with 128 experts and top-8 routing, resulting in only 1.4B active parameters. It is post-trained with reinforcement learning including a physical-plausibility reward, and supports action-conditioned world modeling for robot rollouts, with all weights, code, and inference stack open-sourced under a permissive license. This release significantly lowers the barrier for research into video-based world models by providing a large, efficiently activated model that is fully open-source. Its RL-based post-training with a novel physical-plausibility reward pushes the boundary of combining video generation with action planning, potentially enabling more robust and physically grounded robot simulation and planning. The model uses a single-stream diffusion transformer with DeepSeek-V3-style sparse MoE (128 experts, top-8 routing), achieving 13B total parameters but only 1.4B active per forward pass. The RL post-training incorporates six rewards, including a physical-plausibility reward graded by a VLM from sampled frames, though the authors add real-video negatives to mitigate reward hacking.

reddit · r/MachineLearning · /u/Savings-Display5123 · Jul 8, 17:58

**Background**: Video diffusion models generate videos by gradually denoising random noise, guided by text or other conditions. Mixture-of-experts (MoE) architectures activate only a subset of parameters per input, enabling large model capacity with lower computational cost. A world model predicts future states given actions, which is useful for planning and reinforcement learning in robotics; combining video generation with action conditioning aims to create a model that can simulate robot trajectories.

**Tags**: `#video diffusion`, `#mixture-of-experts`, `#world model`, `#reinforcement learning`, `#open source`

---

<a id="item-11"></a>
## [Alibaba Bans Employees from Using Anthropic's Claude](https://t.me/zaihuapd/42424) ⭐️ 8.0/10

Alibaba has internally ordered all employees to uninstall Anthropic's Claude and related products, including Sonnet, Opus, Fable, and Claude Code, effective July 10, following accusations that Alibaba used approximately 25,000 fake accounts to make over 28 million interactions with Claude between April 22 and June 5. This ban reflects escalating tensions between major AI companies over usage abuse and corporate policy, potentially sparking broader industry discussions on AI ethics and access control. Prior to the ban, Alibaba had reimbursed employees for using external models like Claude, GPT, and Gemini. The ban specifically targets all Anthropic products, including agent tools like Claude Code.

telegram · zaihuapd · Jul 8, 06:09

**Background**: Anthropic develops the Claude series of large language models, trained using 'constitutional AI' for ethical compliance. Alibaba is a major Chinese tech conglomerate with its own AI models. The accusation of fake account usage highlights ongoing challenges in preventing API abuse.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>

</ul>
</details>

**Tags**: `#Alibaba`, `#Anthropic`, `#AI policy`, `#corporate ban`, `#AI ethics`

---

<a id="item-12"></a>
## [Huawei 5G flagship returns overseas, peak speed over 1100 Mbps](https://finance.sina.com.cn/tech/roll/2026-07-08/doc-inihapna8035781.shtml) ⭐️ 8.0/10

Huawei's Pura 90 Pro Max international version natively supports 5G, with measured peak download speeds exceeding 1100 Mbps, marking the return of Huawei's 5G flagship to overseas markets after seven years of US sanctions. This signals Huawei's technological breakthrough and potential recovery in the global smartphone market, impacting competition with other major manufacturers and highlighting the evolving dynamics of international trade restrictions. The phone displays a 5G icon in the status bar, and builds on the Mate 60 series' earlier breakthrough in 2023, followed by the implementation of 5A communication technology via HarmonyOS 6.0.0.125 in January 2026.

telegram · zaihuapd · Jul 8, 12:17

**Background**: Since 2019, US sanctions prevented Huawei from selling 5G smartphones abroad. The Mate 60 series in 2023 demonstrated Huawei's ability to produce 5G-capable chips despite restrictions. The Pura 90 Pro Max international version represents the next step in restoring Huawei's global presence.

**Tags**: `#Huawei`, `#5G`, `#smartphone`, `#international trade`, `#technology`

---

<a id="item-13"></a>
## [Cloudflare and OpenAI Pilot to Optimize AI Search with Network Data](https://36kr.com/newsflashes/3886946347694593) ⭐️ 8.0/10

Cloudflare and OpenAI have launched a research pilot project to use real-time website insights from Cloudflare's global network to improve how AI search engines index and crawl web content. This collaboration could significantly enhance the accuracy and timeliness of AI search results by leveraging fresh, high-quality signals about web content, and it demonstrates a novel use of edge network infrastructure to address AI data challenges. The project will use real-time network signals such as content freshness, traffic quality, and actual page changes to improve indexing and crawling efficiency for AI systems.

telegram · zaihuapd · Jul 8, 15:27

**Background**: AI search engines rely on indexing vast amounts of web content to generate accurate answers, but traditional crawling methods can be slow and miss timely updates. Cloudflare operates a global network that handles a significant portion of internet traffic, giving it unique visibility into website changes and quality. This pilot aims to use that real-time data to prioritize which pages to crawl and index, potentially making AI search more responsive.

**Tags**: `#AI搜索`, `#Cloudflare`, `#OpenAI`, `#网络数据`, `#索引优化`

---

<a id="item-14"></a>
## [LineageOS Launches Browser-Based Flashing Tool](https://www.androidauthority.com/lineageos-summertime-update-2026-3685112/) ⭐️ 8.0/10

LineageOS introduced Lineage Flash Tools in its summer 2026 update, allowing users to flash custom ROMs directly from a web browser without installing adb and fastboot locally. Additionally, the Updater app received a Material 3 Expressive redesign, and development of LineageOS 24 based on Android 17 has begun. This lowers the barrier for users to install custom ROMs, making the process more accessible and convenient. It also demonstrates LineageOS's commitment to modernizing the user experience while expanding device support. The tool supports Fastboot, ADB, and Samsung Odin protocols, but requires a browser with WebUSB support like Chrome or Edge. It cannot fully replace traditional flashing methods and must be used alongside device-specific Wiki guides.

telegram · zaihuapd · Jul 9, 01:46

**Background**: LineageOS is a popular open-source custom ROM for Android devices, offering features and updates beyond official manufacturer support. WebUSB is a web API that enables web pages to communicate with USB devices directly. Odin is a protocol used by Samsung for flashing firmware. The new tool leverages these technologies to simplify the flashing process.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Web_usability">Web usability</a></li>
<li><a href="https://en.wikipedia.org/wiki/OSI_protocols">OSI protocols</a></li>

</ul>
</details>

**Tags**: `#LineageOS`, `#Android`, `#刷机工具`, `#定制ROM`, `#WebUSB`

---