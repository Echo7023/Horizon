---
layout: default
title: "Horizon Summary: 2026-07-09 (ZH)"
date: 2026-07-09
lang: zh
---

> 从 40 条内容中筛选出 14 条重要资讯。

---

1. [TypeScript 7.0 发布，用 Rust 重写，速度提升 8-12 倍](#item-1) ⭐️ 9.0/10
2. [Bun 从 Zig 重写为 Rust](#item-2) ⭐️ 9.0/10
3. [Mistral 发布 8B 参数机器人导航模型 Robostral Navigate](#item-3) ⭐️ 8.0/10
4. [Grok 4.5 发布，使用 Cursor 数据，引发信任争议](#item-4) ⭐️ 8.0/10
5. [OpenAI 推出 GPT-Live 语音模式，可委托 GPT-5.5 处理任务](#item-5) ⭐️ 8.0/10
6. [Cloudflare Meerkat：无领导者异步共识](#item-6) ⭐️ 8.0/10
7. [欧盟重启聊天控制 1.0，扫描非端到端加密消息](#item-7) ⭐️ 8.0/10
8. [LingBot-Video：开源稀疏 MoE 视频扩散 Transformer](#item-8) ⭐️ 8.0/10
9. [DeepSeek 自研 AI 芯片以减少对英伟达和华为的依赖](#item-9) ⭐️ 8.0/10
10. [阿里下令全员卸载 Claude，7 月 10 日生效](#item-10) ⭐️ 8.0/10
11. [华为 5G 旗舰重返海外，峰值速率突破 1100 Mbps](#item-11) ⭐️ 8.0/10
12. [安卓远程 Root 漏洞链曝光](#item-12) ⭐️ 8.0/10
13. [美团 OWL 测试模型泄露用户对话](#item-13) ⭐️ 8.0/10
14. [研究人员通过电磁信号识别手机应用，准确率达 99%](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [TypeScript 7.0 发布，用 Rust 重写，速度提升 8-12 倍](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 9.0/10

微软宣布了 TypeScript 7.0，其编译器完全用 Rust 重写，带来了 8-12 倍的性能提升（在 VS Code 代码库上最高达 11.9 倍）。该版本还引入了新的语法特性，如 `using` 声明和 `satisfies` 操作符。 这一重大版本飞跃大幅减少了大型 TypeScript 代码库的编译时间，显著加快了开发工作流程。用 Rust 重写也为 JavaScript 生态系统的编译器性能树立了新标准，可能影响未来的工具选择。 基准测试显示，TypeScript 7.0 编译 VS Code 代码库只需 10.6 秒，而 TypeScript 6.0 需要 125.7 秒，速度提升 11.9 倍。新的 `using` 声明提供了确定性资源管理，`satisfies` 操作符则允许在不改变推断类型的情况下进行更精确的类型检查。

hackernews · DanRosenwasser · 7月8日 16:06 · [社区讨论](https://news.ycombinator.com/item?id=48833715)

**背景**: TypeScript 是 JavaScript 的类型化超集，编译为普通 JavaScript，广泛用于大型应用程序。其原始编译器是用 TypeScript 自身编写的，这导致大型代码库出现性能瓶颈。Rust 是一种以高性能和内存安全著称的系统编程语言，因此成为重写编译器的理想选择。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dev.to/amarjit_yadav/typescript-7-whats-new-and-exciting-4d26">TypeScript 7: What's New and Exciting? - DEV Community</a></li>
<li><a href="https://www.blog.brightcoding.dev/2025/03/22/exploring-typescript-7-new-features-and-enhancements/">Exploring TypeScript 7: New Features and Enhancements - BrightCoding</a></li>

</ul>
</details>

**社区讨论**: 社区反响极为积极，用户们对巨大的速度提升和团队的工程壮举表示赞赏。一些用户对继续支持 JSDoc 和新语法特性表示赞赏，而另一些用户则反思了 TypeScript 在 JavaScript 中普及类型的作用。

**标签**: `#TypeScript`, `#programming languages`, `#performance`, `#compiler`, `#Rust`

---

<a id="item-2"></a>
## [Bun 从 Zig 重写为 Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/#atom-everything) ⭐️ 9.0/10

Jarred Sumner 宣布 JavaScript 运行时 Bun 已从 Zig 重写为 Rust，重写过程借助 AI 编程代理在 11 天内完成。基于 Rust 的新版 Bun 自 2026 年 6 月 17 日起已在 Claude Code 中投入使用。 此次重写通过消除 Zig 版本中常见的释放后使用和双重释放等内存错误，显著提升了 Bun 的稳定性。同时，它证明了借助 AI 进行大规模重写是可行的，挑战了长期以来“不应重写”的信念。 重写花费了约 16.5 万美元的 API token（59 亿输入 token、6.9 亿输出 token），但由于 Bun 属于 Anthropic 而免费。Rust 移植版将二进制体积缩小了 20%，并在 Linux 上将启动性能提升了 10%。

rss · Simon Willison · 7月8日 23:57

**背景**: Bun 是一个 JavaScript 运行时、包管理器和测试运行器，旨在作为 Node.js 的即插即用替代品。它最初用 Zig 编写，Zig 是一种需要手动管理内存的系统编程语言。将垃圾回收的 JavaScript 与手动管理的 Zig 代码混合导致了大量内存相关错误，而 Rust 的所有权模型和 RAII 可以在编译时防止这些问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bun_(software)">Bun (software) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论普遍赞赏了严谨的方法以及 AI 与人工监督的结合。一些人指出，重写的成功反映了 Zig 在内存安全方面的不足，而另一些人则质疑将 AI 辅助重写成本与人类团队进行比较的公平性，因为 16.5 万美元的 token 费用被免除了。

**标签**: `#Bun`, `#Rust`, `#Zig`, `#JavaScript runtime`, `#rewrite`

---

<a id="item-3"></a>
## [Mistral 发布 8B 参数机器人导航模型 Robostral Navigate](https://mistral.ai/news/robostral-navigate/) ⭐️ 8.0/10

Mistral AI 发布了 Robostral Navigate，这是一个 80 亿参数的机器人导航模型，仅使用单个 RGB 摄像头就在 R2R-CE 基准上达到了 76.6% 的准确率，无需深度传感器、激光雷达或多摄像头。 该模型证明了仅用极简硬件即可实现无地图导航，这有望大幅降低在家庭、仓库和工业环境中部署自主机器人的成本和复杂度。 该模型完全在模拟环境中训练，并使用自然语言指令引导机器人。这是 Mistral 的首个机器人模型，目前未公开开放，但公司可能通过合作或 API 提供访问。

hackernews · ottomengis · 7月8日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=48832212)

**背景**: 传统机器人导航通常依赖预建地图或激光雷达等昂贵传感器。无地图导航（也称视觉导航）利用摄像头输入和深度学习，无需地图即可导航，解决了“绑架机器人问题”——即机器人无法定位自身。R2R-CE 基准测试评估从视觉观察和语言指令进行导航的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/robostral-navigate/">Robostral Navigate: single-camera AI navigation | Mistral AI</a></li>
<li><a href="https://cryptobriefing.com/mistral-robostral-navigate-robotics-model/">Mistral AI unveils Robostral Navigate, an 8B robotics model that could reshape industrial automation investing</a></li>
<li><a href="https://alphasignal.ai/news/mistral-s-robostral-navigate-beats-sensor-heavy-robots-with-just-one-camera">Mistral's Robostral Navigate Beats Sensor-Heavy Robots With Just One Camera | AlphaSignal</a></li>

</ul>
</details>

**社区讨论**: 评论者对无地图导航能力感到兴奋，有人希望将其用于农场机器人等业余项目。另一些人指出，虽然户外无地图导航已存在，但室内无地图导航相对较新。还有人对将模型扩展到物体操作等高级任务感兴趣。

**标签**: `#robotics`, `#navigation`, `#AI`, `#Mistral`, `#deep learning`

---

<a id="item-4"></a>
## [Grok 4.5 发布，使用 Cursor 数据，引发信任争议](https://x.ai/news/grok-4-5) ⭐️ 8.0/10

xAI 发布了 Grok 4.5，该模型使用数万亿个 Cursor 用户交互数据 token 进行训练，声称在更低成本（每百万 token $2/$6）下推理效率比 Opus 提升 4 倍。 这标志着首个使用真实开发者-智能体交互数据训练的主流模型，可能为编程 AI 设立新标准，但也引发了关于数据隐私和政治偏见的伦理担忧。 Grok 4.5 基于 xAI 的 1.5T V9 基础模型，并补充了 Cursor 数据，目前在 SpaceX 和 Tesla 进行私人测试。定价为每百万输入 token $2，每百万输出 token $6。

hackernews · BoumTAC · 7月8日 18:00 · [社区讨论](https://news.ycombinator.com/item?id=48835111)

**背景**: Grok 是 xAI 的大型语言模型系列，以编程和推理能力著称。Cursor 是一款 AI 编程助手，在隐私模式关闭时会收集用户代码和交互数据。xAI 因涉嫌塑造 Grok 的回复以符合政治叙事而受到批评，最近的系统提示指示其假设媒体观点存在偏见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.ai/news/grok-4-5">Introducing Grok 4.5 | SpaceXAI</a></li>
<li><a href="https://cursor.com/data-use">Cursor · Data Use & Privacy Overview</a></li>
<li><a href="https://fortune.com/2025/07/08/elon-musk-grok-ai-conservative-bias-system-prompt/">Users accuse Elon Musk's Grok of a rightward tilt after xAI changes its internal instructions to assume viewpoints from the media are 'biased' | Fortune</a></li>

</ul>
</details>

**社区讨论**: 社区评论褒贬不一：一些人称赞该模型的成本效益和基准性能，而另一些人则因 xAI 的政治倾向和数据隐私问题表示不信任。有用户质疑花费数十亿美元打造第三好的模型的经济合理性。

**标签**: `#AI`, `#LLM`, `#Grok`, `#xAI`, `#benchmarks`

---

<a id="item-5"></a>
## [OpenAI 推出 GPT-Live 语音模式，可委托 GPT-5.5 处理任务](https://openai.com/index/introducing-gpt-live/) ⭐️ 8.0/10

OpenAI 推出了 GPT-Live，这是一种用于 ChatGPT 的全双工语音模式，可以在后台将复杂推理和网络搜索任务委托给 GPT-5.5，从而实现更长的、富有成效的对话。 该功能弥合了语音助手与前沿 AI 模型之间的差距，让用户既能进行自然的实时对话，又能访问最新的推理能力，这可能会显著提升头脑风暴、研究和编程等任务的生产力。 GPT-Live 是一种全双工模型，可以同时听和说，并将深度推理委托给 2026 年 4 月发布的 GPT-5.5。该系统包含安全集成，可实时检查输入和输出，并在检测到不安全内容时中断或结束对话。

hackernews · logickkk1 · 7月8日 17:03 · [社区讨论](https://news.ycombinator.com/item?id=48834405)

**背景**: 传统的语音助手（如 Siri 和 Google Assistant）通常仅限于简单命令，并且无法访问最先进的 AI 模型。GPT-Live 通过将轻量级语音模型与强大的后端模型（GPT-5.5）相结合来解决这一问题，从而在不牺牲对话流畅性的情况下处理复杂任务。GPT-5.5 本身是一个大型语言模型，擅长编程、研究和数据分析。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.marktechpost.com/2026/07/08/openai-releases-gpt-live-and-gpt-live-1-mini-full-duplex-voice-models-that-delegate-deeper-reasoning-to-gpt-5-5/">OpenAI Releases GPT-Live and GPT-Live-1 mini: Full-Duplex Voice Models That Delegate Deeper Reasoning to GPT-5.5 - MarkTechPost</a></li>
<li><a href="https://venturebeat.com/technology/openai-launches-gpt-live-a-full-duplex-voice-upgrade-that-lets-chatgpt-talk-more-like-a-person">OpenAI launches GPT-Live, a full-duplex voice upgrade that lets ChatGPT talk more like a person | VentureBeat</a></li>

</ul>
</details>

**社区讨论**: 社区评论褒贬不一：一些用户称赞该功能能够实现长时间、富有成效的对话（例如一小时的头脑风暴），而另一些人则担心 AI 会取代人际关系，以及语音模式缺乏工具/连接器支持。有用户报告了一个 bug，即模型会在不恰当的时候打断并大笑。

**标签**: `#AI`, `#OpenAI`, `#voice assistant`, `#GPT-5.5`, `#productivity`

---

<a id="item-6"></a>
## [Cloudflare Meerkat：无领导者异步共识](https://blog.cloudflare.com/meerkat-introduction/) ⭐️ 8.0/10

Cloudflare 宣布了 Meerkat，一种基于 QuePaxa 的全球分布式、无领导者共识算法，它异步运行，不依赖超时。 这是异步共识算法的首个生产级实现，可能提高在不可靠网络中的鲁棒性，而像 Raft 这样基于领导者的协议在这种网络中会面临困难。 Meerkat 使用随机化异步共识来保证在最坏情况下的活性，并依靠对冲（hedging）而非超时来提高效率。然而，它要求每次读取操作都进行全局共识，这可能会增加延迟。

hackernews · bobnamob · 7月8日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=48831565)

**背景**: 像 Paxos 和 Raft 这样的共识算法是分布式系统的基础，它们使多个服务器即使在某些故障情况下也能就一个值达成一致。传统协议是部分同步的，依赖超时来检测故障，这在高延迟或丢包的网络中可能引发问题。Meerkat 的基础 QuePaxa 是一种异步共识算法，不依赖超时，因此在恶劣条件下更加鲁棒。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bford.info/pub/os/quepaxa/">QuePaxa: Escaping the Tyranny of Timeouts in Consensus – Bryan Ford's Home Page</a></li>
<li><a href="https://bford.info/pub/os/quepaxa/quepaxa.pdf">QuePaxa: Escaping the Tyranny of Timeouts in Consensus Pasindu Tennage* EPFL</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，Meerkat 是异步共识算法的首个生产级实现，但一些人质疑其在读密集型工作负载下的性能，因为每次读取都需要全局共识。其他人则欣赏它在混乱网络中的潜力，因为基于领导者的协议会遭受领导者抖动和选举风暴。

**标签**: `#distributed systems`, `#consensus`, `#cloudflare`, `#asynchronous`, `#meerkat`

---

<a id="item-7"></a>
## [欧盟重启聊天控制 1.0，扫描非端到端加密消息](https://cyberinsider.com/eu-now-one-step-away-from-reviving-private-message-scanning-rules/) ⭐️ 8.0/10

欧盟距离重启“聊天控制 1.0”仅一步之遥，该法规允许服务提供商扫描非端到端加密消息以查找儿童性虐待材料（CSAM）。决定性投票预计在 2026 年 7 月 9 日进行，需要 361 名欧洲议会议员的绝对多数才能阻止该法规。 这一进展对欧盟公民的隐私具有重大影响，因为它允许大规模扫描私人通信，尽管仅限于非端到端加密的通信。同时，这也为更具争议性的“聊天控制 2.0”铺平了道路，后者将强制要求扫描并禁止端到端加密。 聊天控制 1.0 仅适用于非端到端加密服务，如 Facebook Messenger 或 Gmail，而不适用于 WhatsApp 或 Signal 等加密平台。该法规最初于 2026 年 3 月 26 日以一票之差被否决，但随后被重启并快速推进至 2026 年 7 月 9 日的决定性投票。

hackernews · ggirelli · 7月8日 16:53 · [社区讨论](https://news.ycombinator.com/item?id=48834296)

**背景**: 聊天控制是一项拟议中的欧盟法规，旨在通过要求数字平台检测和报告儿童性虐待材料来防止在线儿童性虐待。民间社会组织认为，该提案实际上将强制对私人通信进行大规模监控，破坏端到端加密并侵犯基本隐私权。第一版（1.0）侧重于非端到端加密消息，而第二版（2.0）将扩展到所有通信，包括加密通信。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control_1.0">Chat Control 1.0</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍区分了聊天控制 1.0 和 2.0，一些人指出 1.0 似乎可以接受，因为它只允许扫描非端到端加密消息，用户已经预期这些消息对服务提供商可见。然而，其他人担心这可能是迈向 2.0 的垫脚石，后者将强制扫描并禁止端到端加密。一些用户提供了可操作的链接，如 fightchatcontrol.eu，供欧盟公民联系其代表。

**标签**: `#privacy`, `#EU legislation`, `#encryption`, `#surveillance`, `#CSAM`

---

<a id="item-8"></a>
## [LingBot-Video：开源稀疏 MoE 视频扩散 Transformer](https://www.reddit.com/r/MachineLearning/comments/1ur0bxq/lingbotvideo_sparsemoe_video_diffusion/) ⭐️ 8.0/10

LingBot-Video 是一个 13B 参数的稀疏 MoE 视频扩散 Transformer，仅 1.4B 活跃参数，已开源并具备 RL 后训练和动作条件世界模型能力。 这项工作通过结合稀疏 MoE 效率和 RL 微调，推动了开源视频生成和世界建模的发展，但其依赖 VLM 的物理合理性奖励以及缺乏闭环机器人评估，引发了关于世界模型主张有效性的重要问题。 该模型采用 DeepSeek-V3 风格的稀疏 MoE，包含 128 个专家和 top-8 路由，总参数 13B 中活跃参数仅 1.4B。RL 后训练使用六种奖励信号，包括由 VLM 评分的物理合理性奖励，并支持动作到视频模式用于机器人 rollout。

reddit · r/MachineLearning · /u/Savings-Display5123 · 7月8日 17:58

**背景**: 视频扩散 Transformer 通过迭代去噪潜在表示来生成视频。稀疏混合专家（MoE）通过每个 token 仅激活部分参数来降低计算成本。世界模型旨在根据动作预测未来状态，从而支持机器人规划，但将其与视频生成器区分需要闭环评估。

**社区讨论**: Reddit 帖子作者邀请社区审视两个关键点：VLM 能否在没有奖励黑客的情况下合理判断物理合理性，以及该模型在没有闭环机器人结果的情况下是否真正符合世界模型的标准。鉴于该模型在 RBench 上平均分最高但在通用 T2V 上排名第二，社区预计将就这些问题展开辩论。

**标签**: `#video diffusion`, `#sparse MoE`, `#world model`, `#reinforcement learning`, `#open source`

---

<a id="item-9"></a>
## [DeepSeek 自研 AI 芯片以减少对英伟达和华为的依赖](https://t.me/zaihuapd/42423) ⭐️ 8.0/10

中国 AI 公司 DeepSeek 正在自研专注于推理的 AI 芯片，旨在减少对英伟达和华为芯片的依赖。该计划已进行约一年，目前仍处于早期阶段。 此举可能重塑中国的 AI 硬件格局，尤其是在美国出口管制限制先进英伟达芯片获取的背景下。这也标志着中国科技公司追求芯片自给自足的更广泛趋势。 该芯片专为推理而非训练设计，DeepSeek 已开始与芯片设计、代工和存储公司接洽，并大量招募芯片设计工程师。此前 DeepSeek 依赖英伟达 H800 和华为昇腾芯片。

telegram · zaihuapd · 7月8日 05:20

**背景**: DeepSeek 是一家以大型语言模型闻名的中国 AI 初创公司。英伟达 H800 是一款面向数据中心的 GPU，但美国出口管制限制了其对华销售。开发自研芯片有助于 DeepSeek 等公司绕过此类限制并减少对外国供应商的依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NVIDIA_H800_GPU">NVIDIA H800 GPU</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#DeepSeek`, `#hardware`, `#semiconductors`, `#China`

---

<a id="item-10"></a>
## [阿里下令全员卸载 Claude，7 月 10 日生效](https://t.me/zaihuapd/42424) ⭐️ 8.0/10

阿里巴巴内部下令要求所有员工卸载 Anthropic 产品，包括 Claude、Sonnet、Opus、Fable 和 Claude Code 等，禁令于 7 月 10 日生效。此前 Anthropic 指控阿里在 4 月 22 日至 6 月 5 日期间使用约 2.5 万个虚假账号与 Claude 交互超过 2800 万次。 这一事件标志着两家主要 AI 公司之间的直接对抗，凸显了围绕 API 滥用和使用政策的紧张局势升级。它可能为企业如何管理员工对外部 AI 工具的访问树立先例，并影响跨公司的 AI 合作。 禁令涵盖所有 Anthropic 产品，包括 Sonnet、Opus 和 Fable 等模型，以及 Claude Code 等 Agent 产品。阿里此前曾报销员工使用 Claude、GPT 和 Gemini 等外部模型的费用，但该政策现已逆转。

telegram · zaihuapd · 7月8日 06:09

**背景**: Anthropic 是一家 AI 安全公司，开发了 Claude 模型系列，与 OpenAI 的 GPT 和 Google 的 Gemini 竞争。API 滥用（例如使用虚假账户绕过速率限制或提取数据）是 AI 提供商普遍关注的问题。阿里巴巴是一家中国科技巨头，拥有自己的 AI 模型，包括通义千问系列。

**标签**: `#Alibaba`, `#Anthropic`, `#Claude`, `#AI policy`, `#enterprise security`

---

<a id="item-11"></a>
## [华为 5G 旗舰重返海外，峰值速率突破 1100 Mbps](https://finance.sina.com.cn/tech/roll/2026-07-08/doc-inihapna8035781.shtml) ⭐️ 8.0/10

华为 Pura 90 Pro Max 国际版原生支持 5G 网络，海外实测峰值下载速率突破 1100 Mbps，标志着华为 5G 旗舰在受美国制裁 7 年后正式重返海外市场。 这标志着重要的地缘政治和技术里程碑，华为重新获得全球智能手机市场竞争力，并展示了其用先进 5G 技术克服美国制裁的能力。 该设备状态栏显示 5G 图标，并搭载 HarmonyOS 6.0.0.125 及 5A 通信技术，为重返海外奠定了技术基础。

telegram · zaihuapd · 7月8日 12:17

**背景**: 自 2019 年以来，美国制裁阻止华为在海外销售 5G 手机。2023 年 Mate 60 系列突破技术封锁，如今 Pura 90 Pro Max 国际版将 5G 带回全球市场。

**标签**: `#Huawei`, `#5G`, `#smartphone`, `#sanctions`, `#technology`

---

<a id="item-12"></a>
## [安卓远程 Root 漏洞链曝光](https://www.coolapk.com/feed/72700258?s=ZGQ2MTVlZjYxMDYyNTM3ZzZhNGUzOThjega1640) ⭐️ 8.0/10

7 月 8 日，网络安全公司 Nebula 披露了一套影响安卓 17 及所有旧版本的远程 Root 漏洞链，该链结合了 Firefox 151.0.2 及更早版本的浏览器漏洞和一个潜伏 15 年的 Linux 内核漏洞。用户点击恶意链接后，攻击者可在 1 分钟内获得持久 Root 权限。 该漏洞链严重性极高，因为用户只需点击链接即可被远程完全控制设备，无需其他交互。它影响大量安卓设备，且概念验证代码已公开，可能很快被广泛利用。 攻击链首先利用 Firefox 漏洞获得初始代码执行权限，然后通过一个 Linux 内核漏洞（CVE 尚未公开）提升权限。谷歌 Pixel 设备已被证实可被攻破，Linux 内核修复补丁已发布。

telegram · zaihuapd · 7月8日 13:01

**背景**: 安卓安全依赖于沙箱和权限模型，但内核级漏洞可以绕过这些保护。远程 Root 漏洞很少见，因为它们需要串联多个漏洞。此次披露的链结合了浏览器漏洞用于初始访问和内核漏洞用于权限提升，使其尤其危险。

**标签**: `#android`, `#security`, `#vulnerability`, `#root`, `#exploit`

---

<a id="item-13"></a>
## [美团 OWL 测试模型泄露用户对话](https://github.com/gumusserv/ProducerBenchV2/blob/83cad6007ef3fe8df33386e8f43738fe62337e16/parsed_source_data/data/) ⭐️ 8.0/10

据报道，美团在 OpenRouter 上的 OWL（LongCat）免费测试模型泄露了用户对话数据，包含该数据的 GitHub 仓库已被下架。 此事件凸显了在 AI 模型交互中暴露敏感信息的安全风险，尤其对于使用公开测试模型的开发者和企业。 泄露数据至少早在 2026 年 7 月 7 日就出现在 GitHub 仓库中，随后被 Discord 机器人令牌扫描器发现，报告令牌已暴露并被重置。

telegram · zaihuapd · 7月8日 13:35

**背景**: 像美团 OWL 这样的 AI 模型通常在 OpenRouter 等平台上提供免费测试。Google、DeepSeek 等公司曾在隐私说明中表示，用户对话数据可能用于服务改进、分析或模型训练。此次事件强调了在 AI 模型中输入 API 密钥、私钥或企业源代码等敏感信息的风险。

**社区讨论**: Telegram 讨论中包括用户对泄露的警告，并提及类似过往事件，增加了问题的可信度和紧迫性。

**标签**: `#data leak`, `#AI security`, `#Meituan`, `#privacy`, `#LLM`

---

<a id="item-14"></a>
## [研究人员通过电磁信号识别手机应用，准确率达 99%](https://www.scmp.com/news/china/science/article/3359688/chinese-researchers-find-peephole-any-smartphone-its-leaked-radio-signal) ⭐️ 8.0/10

中国研究人员开发出一种非接触式技术，通过分析智能手机泄露的低频电磁信号来识别正在使用的应用，在 iPhone 15 Pro、小米 15 Pro 和 OPPO Reno 13 等设备上准确率高达 99.07%。 这种侧信道攻击构成了重大的隐私威胁，因为它即使在手机离线、飞行模式、加密或锁定状态下也能工作，且无需访问设备的系统或存储数据。 该技术针对智能手机 CPU 和 GPU 等组件发出的低频电磁辐射（低于 1 MHz），能够区分抖音、微信视频通话、百度地图、短信、浏览器、相机和云存储等应用。

telegram · zaihuapd · 7月8日 16:05

**背景**: 侧信道攻击利用系统无意中泄露的物理信息（如电磁辐射、功耗或时序）来提取敏感数据。与传统针对软件漏洞的网络攻击不同，侧信道攻击利用了系统的物理实现。这项研究表明，即使加密或离线的智能手机在应用使用过程中也会泄露可识别的电磁模式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Side-channel_attack">Side-channel attack</a></li>

</ul>
</details>

**标签**: `#side-channel attack`, `#smartphone security`, `#privacy`, `#electromagnetic signals`, `#forensics`

---