---
layout: default
title: "Horizon Summary: 2026-07-09 (ZH)"
date: 2026-07-09
lang: zh
---

> 从 40 条内容中筛选出 14 条重要资讯。

---

1. [TypeScript 7.0：用 Rust 重写，编译速度提升 8-12 倍](#item-1) ⭐️ 10.0/10
2. [用 AI 代理将 Bun 从 Zig 重写为 Rust](#item-2) ⭐️ 9.0/10
3. [安卓远程 Root 漏洞链曝光](#item-3) ⭐️ 9.0/10
4. [约翰迪尔必须允许用户自行维修](#item-4) ⭐️ 8.0/10
5. [Chatto 开源：基于 NATS 的自托管聊天应用](#item-5) ⭐️ 8.0/10
6. [微软发布 Flint，面向 AI 代理的可视化中间语言](#item-6) ⭐️ 8.0/10
7. [OpenAI 推出 GPT-Live 实时语音模式](#item-7) ⭐️ 8.0/10
8. [Cloudflare Meerkat：无领导者全球共识](#item-8) ⭐️ 8.0/10
9. [欧盟重启私密信息扫描规则，仅差一步](#item-9) ⭐️ 8.0/10
10. [LingBot-Video：开源稀疏 MoE 视频扩散 Transformer](#item-10) ⭐️ 8.0/10
11. [阿里巴巴禁止员工使用 Anthropic 的 Claude](#item-11) ⭐️ 8.0/10
12. [华为 5G 旗舰重返海外，峰值速率超 1100 Mbps](#item-12) ⭐️ 8.0/10
13. [Cloudflare 联手 OpenAI 试点网络数据优化 AI 搜索](#item-13) ⭐️ 8.0/10
14. [LineageOS 推出浏览器刷机工具](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [TypeScript 7.0：用 Rust 重写，编译速度提升 8-12 倍](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 10.0/10

微软发布了 TypeScript 7.0 重大版本，该版本用 Rust 重写了编译器，编译速度相比 TypeScript 6.0 提升了 8 到 12 倍。 这是最广泛使用的编程语言之一的一次突破性性能飞跃，大幅减少了构建时间，为数百万开发者带来了更快的开发周期。 新编译器代号 tsgo，并非自托管，而是用 Rust 从头重写，移植了现有 TypeScript 编译器的结构。基准测试显示，VS Code 的构建时间从 125.7 秒降至 10.6 秒。

hackernews · DanRosenwasser · 7月8日 16:06 · [社区讨论](https://news.ycombinator.com/item?id=48833715)

**背景**: TypeScript 是 JavaScript 的一个类型超集，可编译为普通 JavaScript。其原始编译器 tsc 本身是用 TypeScript 编写的，这导致在大型代码库上出现性能瓶颈。改用 Rust 重写后，利用原生代码性能显著加快了编译和编辑器启动速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://devblogs.microsoft.com/typescript/typescript-native-port/">A 10x Faster TypeScript - TypeScript</a></li>
<li><a href="https://www.techtimes.com/articles/318666/20260618/typescript-70-rc-ships-go-compiler-cuts-vs-code-build-time-77-seconds-seven.htm">TypeScript 7.0 RC Ships: Go Compiler Cuts VS Code Build Time From 77 Seconds to Seven</a></li>
<li><a href="https://www.totaltypescript.com/rewriting-typescript-in-rust">Rewriting TypeScript in Rust? You'd have to be... | Total TypeScript</a></li>

</ul>
</details>

**社区讨论**: 社区反响极其正面，许多人祝贺团队完成这项工程壮举。评论者分享了 7.7 倍到 11.9 倍的速度提升数据，并讨论了重写期间维护两个代码库的挑战。一些人提到 Go 与 Rust 的选择争议，但整体情绪是对性能提升感到兴奋。

**标签**: `#TypeScript`, `#performance`, `#compilers`, `#programming languages`, `#Microsoft`

---

<a id="item-2"></a>
## [用 AI 代理将 Bun 从 Zig 重写为 Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/#atom-everything) ⭐️ 9.0/10

Bun 的创建者 Jarred Sumner 使用先进的智能体工程（Agentic Engineering）技术，借助 Mythos/Fable 和 Claude Code 等编码代理，在 11 天内将整个 JavaScript 运行时从 Zig 重写为 Rust。 这表明 AI 编码代理如今能够实现过去被认为风险过高的大规模重写，可能彻底改变软件的维护和升级方式。此次重写还解决了 Bun 中重大的内存安全问题，提高了稳定性和性能。 重写消耗了约 16.5 万美元的 API 代币（59 亿输入、6.9 亿输出），二进制大小减少 20%，Linux 启动时间提升 10%，并修复了 Zig 版本中大量内存错误，包括释放后使用（use-after-free）和双重释放（double-free）等问题。

rss · Simon Willison · 7月8日 23:57

**背景**: Bun 是一个快速的 JavaScript 运行时和打包工具，最初用 Zig 编写。Zig 是一种低级系统语言，提供手动内存管理；而 Rust 是一种内存安全的系统语言，具有编译时保证。Bun 重写使用了一套由人类工程师编排的 AI 编码代理，利用现有的 TypeScript 测试套件作为一致性套件来验证正确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/agentic-engineering">What is Agentic Engineering? | IBM</a></li>
<li><a href="https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/">What is agentic engineering? - Agentic Engineering Patterns - Simon Willison's Weblog</a></li>

</ul>
</details>

**社区讨论**: 评论者反应不一：有人赞扬了这种有人类监督的严谨工程方法，也有人批评在未提供 Zig 版本的长期支持（LTS）的情况下放弃该版本以进行关键修复。还有人指出，16.5 万美元的成本远低于一个软件工程团队完成如此大规模重写一年的薪资。

**标签**: `#Bun`, `#Rust`, `#Zig`, `#runtime`, `#software engineering`

---

<a id="item-3"></a>
## [安卓远程 Root 漏洞链曝光](https://www.coolapk.com/feed/72700258?s=ZGQ2MTVlZjYxMDYyNTM3ZzZhNGUzOThjega1640) ⭐️ 9.0/10

2026 年 7 月 8 日，网络安全公司 Nebula 曝光了一个影响安卓 17 及以下所有版本的远程 Root 漏洞链，该漏洞链结合了 Firefox 浏览器漏洞（最高至 151.0.2 版本）和潜伏 15 年的 Linux 内核提权漏洞（CVE-2026-43499，代号 GhostLock）。 该漏洞链允许攻击者仅通过诱骗用户点击恶意链接即可获得对任何受影响安卓设备的持久 Root 权限，对全球数十亿安卓用户构成直接且严重的威胁。 概念验证代码已上传至 GitHub，完整漏洞细节暂未披露，但 Linux 内核已发布补丁。谷歌 Pixel 设备已被成功测试，该漏洞链可在一分钟内植入权限文件并获取 Root 权限。

telegram · zaihuapd · 7月8日 13:01

**背景**: 远程 Root 漏洞链利用多个漏洞，通过网络实现代码执行和提权，无需物理接触。此次披露的漏洞链首先利用 Firefox 浏览器漏洞逃逸浏览器沙箱，然后借助 GhostLock Linux 内核漏洞获得安卓设备的完全 Root 控制。此类攻击极其危险，因为用户只需点击链接即可中招，且由于内核漏洞存在长达 15 年，影响设备范围极广。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/15-year-old-ghostlock-linux-kernel-vulnerability/">15-year-old GhostLock Linux Kernel Vulnerability Enables Privilege Escalation Attacks</a></li>
<li><a href="https://thehackernews.com/2026/07/15-year-old-ghostlock-flaw-enables-root.html">15-Year-Old GhostLock Flaw Enables Root and Container Escape on Most Linux Distros</a></li>
<li><a href="https://cybersecuritynews.com/firefox-152-vulnerabilities/">Multiple Vulnerabilities in Firefox 152 Enables Remote Code Execution Attacks</a></li>

</ul>
</details>

**标签**: `#Android`, `#vulnerability`, `#security`, `#root`, `#exploit`

---

<a id="item-4"></a>
## [约翰迪尔必须允许用户自行维修](https://apnews.com/article/john-deere-right-to-repair-agriculture-equipment-cb7514ffedb95c130a976af661f2bc02) ⭐️ 8.0/10

美国联邦贸易委员会（FTC）与迪尔公司达成和解，要求这家农业设备制造商允许车主和独立维修店自行维修设备。迪尔必须提供诊断工具、维修手册和软件，并向五个州支付 100 万美元的反垄断执法费用。 这项和解是“维修权”运动的一次重大胜利，可能为汽车、电子等其他行业树立先例。它使农民能够自行修理设备，降低成本和停机时间，并挑战了限制消费者选择的维修垄断。 迪尔将接受为期 10 年的合规监督，而 100 万美元的罚款与其利润相比相对较小。该和解特别针对软件工具的访问权限，这曾是农民维修现代化、依赖软件的设备的主要障碍。

hackernews · djoldman · 7月8日 23:37 · [社区讨论](https://news.ycombinator.com/item?id=48838876)

**背景**: “维修权”运动倡导消费者和独立维修店有权维修自己拥有的产品，反对制造商限制零件、工具和软件访问的做法。在农业领域，现代拖拉机和联合收割机配备了复杂的软件，而像迪尔这样的制造商因使维修依赖于经销商技术人员而受到批评。FTC 的行动是多年倡导和州级立法努力的结果，旨在赋予维修权利。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Right_to_repair_movement">Right to repair movement</a></li>
<li><a href="https://en.wikipedia.org/wiki/Right_to_repair">Right to repair - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者赞扬了这一结果，但批评罚款金额过小，有人指出‘大概 100 亿美元的利润’只罚了 100 万。还有人强调了维修权倡导者 Louis Rossmann 的工作，并希望这一标准能扩展到汽车领域。也有评论讽刺本网站对监管俘获的双重标准。

**标签**: `#right-to-repair`, `#FTC`, `#John Deere`, `#consumer rights`, `#legal`

---

<a id="item-5"></a>
## [Chatto 开源：基于 NATS 的自托管聊天应用](https://www.hmans.dev/blog/chatto-is-open-source) ⭐️ 8.0/10

Chatto 是一个基于 NATS 构建的自托管聊天应用，现已开源发布，代码公开于 GitHub。 此次发布为 Discord 或 Slack 等专有聊天平台提供了一个现代、易于自托管的替代方案，NATS 提供轻量级消息传递和内置持久化，吸引注重隐私的用户和开发者。 Chatto 以紧凑的自包含二进制文件形式提供，使用 NATS 进行消息传递和流持久化，并支持 S3 兼容的对象存储来存储媒体文件。其设计使得在个人基础设施上部署非常简便。

hackernews · speckx · 7月8日 15:19 · [社区讨论](https://news.ycombinator.com/item?id=48833116)

**背景**: NATS 是一个高性能、开源的消息传递系统，属于云原生计算基金会，用 Go 编写，支持发布/订阅、流式传输和对象存储。Agentic coding（代理编码）是指使用 AI 代理以最少的人工干预自主规划、编写、测试和修改代码。该开发者利用代理编码独自构建了 Chatto。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NATS_Messaging">NATS Messaging - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agentic_coding">Agentic coding</a></li>
<li><a href="https://nats.io/">NATS.io - Cloud Native, Open Source, High-performance Messaging</a></li>

</ul>
</details>

**社区讨论**: 社区评论总体积极，赞扬了自托管的便捷性和 NATS 的使用。有人指出与 Discord 相比的功能不足，如多社区访问，并提出了企业关注点，如工作消息的软删除。一条幽默评论开玩笑说，开源允许用户验证 AI 是否在评判他们，这参考了聊天应用中集成 AI 的趋势。

**标签**: `#open source`, `#chat`, `#self-hosted`, `#NATS`, `#agentic coding`

---

<a id="item-6"></a>
## [微软发布 Flint，面向 AI 代理的可视化中间语言](https://microsoft.github.io/flint-chart/#/) ⭐️ 8.0/10

微软开源了 Flint，这是一种可视化中间语言，通过提供高级规范并由编译器优化为详细的图表布局，旨在提高 AI 代理生成图表的可靠性。 Flint 解决了 AI 驱动数据可视化的关键挑战：在简单性和质量之间取得平衡。通过将低层视觉决策交给编译器，它使 AI 代理能够更可靠地生成精美的图表，这可能加速 AI 在数据分析工作流程中的采用。 Flint 使用基于语义类型的规范，并包含一个布局优化引擎，可以从高级意图自动添加比例、轴和间距等细节。它还提供了一个 MCP 服务器，便于与现有代理应用集成。

hackernews · chenglong-hn · 7月8日 17:46 · [社区讨论](https://news.ycombinator.com/item?id=48834924)

**背景**: 数据可视化语言如 Vega 或 D3 表达力强但需要指定许多低层细节。大型语言模型（LLM）可以生成代码，但通常难以可靠地生成图表，因为它们必须显式管理视觉编码。Flint 充当一个中间层：AI 代理输出简洁的高级规范，由确定性编译器处理其余部分，从而提高一致性。

**社区讨论**: 社区评论反应不一。一些人称赞 Flint 是代理系统中出现的'确定性层'模式的实用例子。另一些人质疑它与 Vega 的比较，认为 Vega 已经是一个很好的中间表示。一些评论者表示他们没有遇到 Flint 旨在解决的可靠性问题，LLM 在使用 Python 和 R 进行可视化时表现良好。一位评论者认为微软混淆了低层冗长与 LLM 在空间组合方面的实际困难。

**标签**: `#visualization`, `#AI agents`, `#Microsoft`, `#LLM`, `#chart generation`

---

<a id="item-7"></a>
## [OpenAI 推出 GPT-Live 实时语音模式](https://openai.com/index/introducing-gpt-live/) ⭐️ 8.0/10

OpenAI 推出了 GPT-Live 实时语音模式，使用户能与 AI 进行自然对话，并可将复杂推理任务委派给 GPT-5.5。 这标志着向着更自然的人机交互迈出了重要一步，弥合了语音助手与前沿 AI 模型之间的差距，可能改变人们使用 AI 进行工作和陪伴的方式。 GPT-Live 是该语音模式的首个版本，它可以在后台将问题委派给 GPT-5.5，这意味着用户不再受限于能力较弱的专用语音模型。

hackernews · logickkk1 · 7月8日 17:03 · [社区讨论](https://news.ycombinator.com/item?id=48834405)

**背景**: GPT-Live 是 OpenAI 推出的新语音界面，支持实时语音对话。GPT-5.5 于 2026 年 4 月 23 日发布，代号 'Spud'，在推理任务上取得了高基准分数。这种结合使得交互更流畅，能够在不产生明显延迟的情况下利用高级推理能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT-5.5</a></li>

</ul>
</details>

**社区讨论**: 评论褒贬不一：simonw 称赞其长对话的有用性，而 jonstaab 和 overgard 等人则对 AI 取代人际关系表示担忧。artdigital 指出语音模式缺乏工具集成。OpenAI 的 Atty 确认这是首个版本。

**标签**: `#AI`, `#voice assistant`, `#OpenAI`, `#GPT-5.5`, `#real-time interaction`

---

<a id="item-8"></a>
## [Cloudflare Meerkat：无领导者全球共识](https://blog.cloudflare.com/meerkat-introduction/) ⭐️ 8.0/10

Cloudflare 宣布了 Meerkat，一种使用无领导者异步 QuePaxa 协议的全球分布式共识算法。这是 QuePaxa 的首次生产实现。 Meerkat 通过消除对领导者和超时的依赖，可能提升在不可预测网络条件下的性能。它为全球分布式系统提供了传统共识算法（如 Raft 和 Paxos）的替代方案。 Meerkat 尚未投入生产。它需要对每次读取操作进行全局共识，与支持本地读取的系统相比，可能增加读取延迟。

hackernews · bobnamob · 7月8日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=48831565)

**背景**: 共识算法确保多个节点对一个值达成一致。部分同步算法（如 Paxos、Raft）依赖超时并假设消息延迟有界。异步算法（如 QuePaxa）不依赖超时，即使在任意延迟波动下也能推进。Meerkat 在全球规模上实现了 QuePaxa。

**社区讨论**: 评论者讨论了 Meerkat 与现有无领导者协议相比的新颖性，有人质疑其与 Raft 的比较。其他人则指出生产级异步算法的重要性，并对实际性能（尤其是读取操作）表示谨慎。

**标签**: `#distributed systems`, `#consensus algorithms`, `#cloudflare`, `#meerkat`, `#quepaxa`

---

<a id="item-9"></a>
## [欧盟重启私密信息扫描规则，仅差一步](https://cyberinsider.com/eu-now-one-step-away-from-reviving-private-message-scanning-rules/) ⭐️ 8.0/10

欧盟推进了可能强制扫描私密信息、并可能破坏端到端加密的立法，距离生效仅差一步。 此举可能危及数百万欧盟公民的数字隐私和加密通信，为政府监控私人通信开创先例。 该提案包含两个版本：Chat Control 1.0 允许科技公司自愿扫描，而 Chat Control 2.0 则强制扫描并禁止端到端加密。

hackernews · ggirelli · 7月8日 16:53 · [社区讨论](https://news.ycombinator.com/item?id=48834296)

**背景**: 欧盟长期讨论打击儿童性虐待材料的措施，但之前的提案遭到隐私倡导者和科技公司的强烈反对。客户端扫描会在用户设备上对消息进行加密前分析，引发严重的隐私担忧。

**社区讨论**: 评论者对互联网观察基金会推动客户端扫描表示担忧，并指出自愿扫描（Chat Control 1.0）与强制扫描（Chat Control 2.0）之间的关键区别，认为后者更为危险。

**标签**: `#privacy`, `#encryption`, `#EU regulation`, `#surveillance`, `#technology policy`

---

<a id="item-10"></a>
## [LingBot-Video：开源稀疏 MoE 视频扩散 Transformer](https://www.reddit.com/r/MachineLearning/comments/1ur0bxq/lingbotvideo_sparsemoe_video_diffusion/) ⭐️ 8.0/10

LingBot-Video 是一个 13B 参数的视频扩散 Transformer，采用 DeepSeek-V3 风格的稀疏混合专家（MoE）架构，包含 128 个专家和 top-8 路由，因此仅激活 1.4B 参数。它经过包含物理合理性奖励的强化学习后训练，支持以动作为条件的机器人 rollout 世界建模，所有权重、代码和推理栈均以宽松许可证开源。 这一发布通过提供一个完全开源、高效激活的大模型，显著降低了视频世界模型的研究门槛。其基于强化学习的后训练结合新颖的物理合理性奖励，推动了视频生成与动作规划的结合，可能实现更稳健、物理上更真实的机器人模拟和规划。 该模型采用单流扩散 Transformer 架构，使用 DeepSeek-V3 风格的稀疏 MoE（128 个专家，top-8 路由），总参数 13B 但每次前向传播仅激活 1.4B。强化学习后训练包含六项奖励，包括由 VLM 从采样帧评分的物理合理性奖励，但作者添加了真实视频负样本以缓解奖励黑客（reward hacking）问题。

reddit · r/MachineLearning · /u/Savings-Display5123 · 7月8日 17:58

**背景**: 视频扩散模型通过逐步去噪随机噪声并依据文本或其他条件引导来生成视频。混合专家（MoE）架构每次输入仅激活部分参数，从而在较低计算成本下实现大模型容量。世界模型根据动作预测未来状态，对机器人领域的规划和强化学习非常有用；将视频生成与动作条件相结合旨在创建能够模拟机器人轨迹的模型。

**标签**: `#video diffusion`, `#mixture-of-experts`, `#world model`, `#reinforcement learning`, `#open source`

---

<a id="item-11"></a>
## [阿里巴巴禁止员工使用 Anthropic 的 Claude](https://t.me/zaihuapd/42424) ⭐️ 8.0/10

阿里巴巴内部下令全体卸载 Anthropic 的 Claude 及相关产品，包括 Sonnet、Opus、Fable 和 Claude Code，禁令将于 7 月 10 日生效。此前 Anthropic 指控阿里巴巴在 4 月 22 日至 6 月 5 日间使用约 2.5 万个虚假账号与 Claude 交互超 2800 万次。 这项禁令反映了主要 AI 公司在使用滥用和企业政策方面的紧张关系升级，可能引发行业对 AI 伦理和访问控制的更广泛讨论。 禁令前，阿里巴巴曾报销员工使用 Claude、GPT、Gemini 等外部模型的费用。此次禁令特别针对所有 Anthropic 产品，包括 Claude Code 等代理工具。

telegram · zaihuapd · 7月8日 06:09

**背景**: Anthropic 开发 Claude 系列大型语言模型，采用'宪法 AI'技术进行伦理合规训练。阿里巴巴是中国大型科技集团，拥有自有 AI 模型。虚假账号的指控凸显了防止 API 滥用的持续挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>

</ul>
</details>

**标签**: `#Alibaba`, `#Anthropic`, `#AI policy`, `#corporate ban`, `#AI ethics`

---

<a id="item-12"></a>
## [华为 5G 旗舰重返海外，峰值速率超 1100 Mbps](https://finance.sina.com.cn/tech/roll/2026-07-08/doc-inihapna8035781.shtml) ⭐️ 8.0/10

华为 Pura 90 Pro Max 国际版原生支持 5G 网络，实测峰值下载速率超过 1100 Mbps，标志着华为 5G 旗舰在美国制裁七年后正式重返海外市场。 这标志着华为的技术突破及其在全球智能手机市场的潜在复苏，将影响与其他主要厂商的竞争，并凸显国际贸易限制的动态变化。 该手机状态栏显示 5G 标识，并基于 2023 年 Mate 60 系列的技术突破，于 2026 年 1 月通过 HarmonyOS 6.0.0.125 进一步实装 5A 通信技术。

telegram · zaihuapd · 7月8日 12:17

**背景**: 自 2019 年以来，美国制裁阻止了华为在海外销售 5G 智能手机。2023 年的 Mate 60 系列展示了华为在受限条件下生产 5G 芯片的能力。Pura 90 Pro Max 国际版代表了华为恢复全球业务的下一步。

**标签**: `#Huawei`, `#5G`, `#smartphone`, `#international trade`, `#technology`

---

<a id="item-13"></a>
## [Cloudflare 联手 OpenAI 试点网络数据优化 AI 搜索](https://36kr.com/newsflashes/3886946347694593) ⭐️ 8.0/10

Cloudflare 与 OpenAI 宣布启动一项研究试点项目，利用 Cloudflare 全球网络的实时网站洞察数据，帮助 AI 搜索引擎更高效地发现和索引开放网络上的内容。 这一合作通过利用关于网页内容的新鲜、高质量信号，有望显著提升 AI 搜索结果的准确性和时效性，并展示了利用边缘网络基础设施解决 AI 数据挑战的新途径。 该项目将利用内容更新鲜度、流量质量及页面实际变动等实时网络信号，改进 AI 系统对网页的索引和抓取效率。

telegram · zaihuapd · 7月8日 15:27

**背景**: AI 搜索引擎依赖对海量网页内容进行索引以生成准确答案，但传统抓取方法可能速度慢且错过及时更新。Cloudflare 运营着一个处理全球相当一部分互联网流量的全球网络，能够独特地洞察网站变动和质量。该试点旨在利用这些实时数据来优先抓取和索引哪些页面，从而可能使 AI 搜索更加灵敏。

**标签**: `#AI搜索`, `#Cloudflare`, `#OpenAI`, `#网络数据`, `#索引优化`

---

<a id="item-14"></a>
## [LineageOS 推出浏览器刷机工具](https://www.androidauthority.com/lineageos-summertime-update-2026-3685112/) ⭐️ 8.0/10

LineageOS 在 2026 年夏季更新中推出了 Lineage Flash Tools，用户可直接在浏览器中刷入自定义 ROM，无需本地安装 adb 和 fastboot。此外，Updater 应用获得了 Material 3 Expressive 重新设计，基于 Android 17 的 LineageOS 24 的开发也已启动。 这降低了用户安装自定义 ROM 的门槛，使过程更加便捷和易用。同时体现了 LineageOS 在扩展设备支持的同时，致力于现代化用户体验的承诺。 该工具支持 Fastboot、ADB 和三星 Odin 协议，但需要使用 Chrome 或 Edge 等支持 WebUSB 的浏览器。它无法完全取代传统刷机方式，必须配合设备专属 Wiki 指南使用。

telegram · zaihuapd · 7月9日 01:46

**背景**: LineageOS 是一个流行的 Android 设备开源自定义 ROM，提供超越官方制造商支持的功能和更新。WebUSB 是一种网页 API，允许网页直接与 USB 设备通信。Odin 是三星用于刷入固件的协议。新工具利用这些技术简化了刷机流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Web_usability">Web usability</a></li>
<li><a href="https://en.wikipedia.org/wiki/OSI_protocols">OSI protocols</a></li>

</ul>
</details>

**标签**: `#LineageOS`, `#Android`, `#刷机工具`, `#定制ROM`, `#WebUSB`

---