---
layout: default
title: "Horizon Summary: 2026-07-08 (ZH)"
date: 2026-07-08
lang: zh
---

> 从 42 条内容中筛选出 16 条重要资讯。

---

1. [欧盟议会首轮通过聊天控制法案](#item-1) ⭐️ 9.0/10
2. [MIRA：5B 参数的多玩家火箭联盟世界模型](#item-2) ⭐️ 9.0/10
3. [Anthropic 发布 Claude Sonnet 5，代理能力更强](#item-3) ⭐️ 9.0/10
4. [Januscape：潜伏 16 年的 KVM 虚拟机逃逸漏洞公开](#item-4) ⭐️ 9.0/10
5. [Kokoro：本地、CPU 友好的高质量 TTS 模型](#item-5) ⭐️ 8.0/10
6. [欧盟强制要求所有新车安装驾驶员监控摄像头](#item-6) ⭐️ 8.0/10
7. [高薪难留：德国技术工人为何离开](#item-7) ⭐️ 8.0/10
8. [微软裁掉 id Software 引擎团队](#item-8) ⭐️ 8.0/10
9. [sqlite-utils 4.0 引入数据库模式迁移](#item-9) ⭐️ 8.0/10
10. [可微光线追踪用于无线电传播建模的博士论文](#item-10) ⭐️ 8.0/10
11. [Mozilla CTO 就开源 AI 报告举行 AMA](#item-11) ⭐️ 8.0/10
12. [通过可信 LoRA 子空间防御微调投毒](#item-12) ⭐️ 8.0/10
13. [马斯克解散 xAI，更名为 SpaceXAI](#item-13) ⭐️ 8.0/10
14. [中国拟投 2 万亿元建设全国算力网络，优先采用国产 AI 芯片](#item-14) ⭐️ 8.0/10
15. [DeepSeek 自研 AI 推理芯片，减少对英伟达和华为依赖](#item-15) ⭐️ 8.0/10
16. [中国拟限制顶尖 AI 模型出口](#item-16) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [欧盟议会首轮通过聊天控制法案](https://www.heise.de/en/news/Showdown-in-Strasbourg-The-unexpected-return-of-Chat-Control-1-0-11356680.html) ⭐️ 9.0/10

欧盟议会通过程序性策略，在第一轮投票中通过了备受争议的聊天控制法案，最终投票定于周四进行，仅需出席议员的简单多数即可通过。 该立法将强制对私人通信进行大规模监控，可能破坏端到端加密，威胁欧盟及其他地区的数字隐私权，因为其他国家可能效仿此类法规。 这一程序性操作赋予了支持方战术优势：修正或否决需要绝对多数（361 票），而通过仅需出席议员的简单多数，而许多议员可能在暑假前已离席。

hackernews · miroljub · 7月7日 15:16 · [社区讨论](https://news.ycombinator.com/item?id=48819008)

**背景**: 聊天控制，正式名称为《防止和打击儿童性虐待条例》（CSAR），于 2022 年 5 月提出，旨在打击网络儿童性虐待。批评者认为它助长大规模监控并破坏加密。该立法此前曾被否决，现在正通过程序性渠道重新推进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>
<li><a href="https://reclaimthenet.org/eu-parliament-revives-chat-surveillance-for-thursday-vote">EU Parliament Revives Chat Surveillance for Thursday Vote</a></li>
<li><a href="https://www.heise.de/en/news/Partial-victory-with-a-catch-EU-Parliament-temporarily-defies-chat-control-11349760.html">Partial victory with a catch: EU Parliament temporarily defies chat control | heise online</a></li>

</ul>
</details>

**社区讨论**: 评论者对欧盟反复通过程序性策略推动不受欢迎的法律表示不满，有人引用让-克洛德·容克关于逐步侵蚀民主的言论。其他人指出，即使非欧盟国家也可能采取类似的监控措施。

**标签**: `#EU legislation`, `#surveillance`, `#privacy`, `#encryption`, `#digital rights`

---

<a id="item-2"></a>
## [MIRA：5B 参数的多玩家火箭联盟世界模型](https://www.reddit.com/r/MachineLearning/comments/1upofuw/mira_multiplayer_interactive_world_models_trained/) ⭐️ 9.0/10

General Intuition、Kyutai 和 Epic Games 发布了 MIRA，这是一个用于多人火箭联盟的 50 亿参数交互式世界模型，基于 10,000 小时的合成数据训练，能够在单个 B200 GPU 上以 20 FPS 运行完整的 2v2 比赛。 MIRA 是首个针对高度动态复杂物理环境的多玩家世界模型，无需真实数据收集即可实现实时交互模拟，可能加速强化学习和游戏 AI 研究。 该模型使用潜在扩散架构，根据所有四名玩家的动作生成视频帧，团队还发布了可玩演示、技术论文和 1000 小时的四人游戏数据集。

reddit · r/MachineLearning · /u/MasterScrat · 7月7日 07:59

**背景**: 世界模型是模拟环境动态的 AI 系统，使智能体无需真实交互即可进行规划和学习。以往的世界模型仅限于单玩家场景，将其他智能体视为环境的一部分。MIRA 通过条件化多个动作流将其扩展到多玩家设置，学习将变化归因于正确的玩家。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/mira-wm/mira">MIRA: Multiplayer Interactive World Models with ... - GitHub</a></li>
<li><a href="https://arxiv.org/abs/2607.05352">[2607.05352] Multiplayer Interactive World Models with ...</a></li>
<li><a href="https://www.linkedin.com/posts/generalintuition_introducing-mira-a-playable-multiplayer-activity-7479870314252922880-y9CV">Introducing MIRA. A playable, multiplayer world model. A ...</a></li>

</ul>
</details>

**标签**: `#world models`, `#reinforcement learning`, `#multiplayer`, `#Rocket League`, `#open source`

---

<a id="item-3"></a>
## [Anthropic 发布 Claude Sonnet 5，代理能力更强](https://t.me/zaihuapd/42404) ⭐️ 9.0/10

Anthropic 发布了 Claude Sonnet 5，称其是迄今代理能力最强的 Sonnet 模型，能够规划、使用浏览器和终端等工具并自主运行。该模型即日起面向所有套餐开放，包括 Free 和 Pro 计划，限时定价为每百万输入 token 2 美元、每百万输出 token 10 美元，截至 2026 年 8 月 31 日。 Claude Sonnet 5 带来了此前需要更大、更昂贵模型才能实现的代理能力，使高级 AI 代理更加易用且成本更低。其具有竞争力的定价以及在编码、工具使用和推理方面的强劲表现，可能加速 AI 代理在软件工程和其他专业工作流程中的采用。 Claude Sonnet 5 在推理、工具使用、编码和知识工作方面优于 Sonnet 4.6，性能接近 Opus 4.8 但价格更低。它成为 Claude.ai 上 Free 和 Pro 计划的默认模型，也可通过 Anthropic API 和 Amazon Bedrock 使用。

telegram · zaihuapd · 7月7日 09:02

**背景**: Anthropic 的 Claude 模型系列包括 Sonnet（中端，平衡速度和能力）和 Opus（高端，性能最强）。2026 年 5 月发布的 Opus 4.8 在代理任务上树立了高标准，而 Sonnet 5 现在以更低成本带来了类似能力。代理能力指的是模型自主规划、使用外部工具并执行多步骤任务而无需持续人工指导的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-sonnet-5">Introducing Claude Sonnet 5 \ Anthropic</a></li>
<li><a href="https://techcrunch.com/2026/06/30/anthropic-launches-claude-sonnet-5-as-a-cheaper-way-to-run-agents/">Anthropic launches Claude Sonnet 5 as a cheaper way to run ...</a></li>
<li><a href="https://www.anthropic.com/news/claude-opus-4-8">Introducing Claude Opus 4.8 \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI`, `#Anthropic`, `#Claude`, `#LLM`, `#agent`

---

<a id="item-4"></a>
## [Januscape：潜伏 16 年的 KVM 虚拟机逃逸漏洞公开](https://github.com/V4bel/Januscape) ⭐️ 9.0/10

安全研究人员公开了 Januscape（CVE-2026-53359），这是 KVM 影子 MMU 中的一个 use-after-free 漏洞，允许客户虚拟机在 Intel 和 AMD x86 平台上逃逸到宿主机。该漏洞在 Linux 内核中已存在约 16 年，并且概念验证代码已发布。 这是首个同时影响 Intel 和 AMD 平台的 KVM/x86 虚拟机逃逸漏洞，直接威胁公有云等多租户 KVM 宿主机的隔离边界。此外，在 RHEL 等发行版中，本地普通用户还可利用该缺陷提权至 root。 该漏洞是影子 MMU 代码中的 use-after-free 缺陷，该代码在 Intel 和 AMD 平台共享，仅通过客户机内部操作即可触发。它曾被用作 Google kvmCTF 的 0-day 攻击，影响 2010 年至 2026 年 6 月的 Linux 内核。

telegram · zaihuapd · 7月7日 10:14

**背景**: KVM（基于内核的虚拟机）是一个 Linux 内核模块，它将宿主机转变为虚拟机监控器，允许多个虚拟机（客户机）运行。影子 MMU 用于管理客户机内存映射；use-after-free 漏洞发生在已释放的内存区域仍被引用时，导致内存损坏。虚拟机逃逸漏洞打破了客户机与宿主机之间的隔离，可能允许攻击者控制宿主机系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/07/16-year-old-linux-kvm-flaw-lets-guest.html">16-Year-Old Linux KVM Flaw Lets Guest VMs Escape to Host on ...</a></li>
<li><a href="https://github.com/V4bel/Januscape">GitHub - V4bel/Januscape</a></li>
<li><a href="https://cybersecuritynews.com/16-year-old-linux-kvm-vulnerability/">16-Year-Old Linux KVM Vulnerability Allows Malicious Guest ...</a></li>

</ul>
</details>

**标签**: `#KVM`, `#VM escape`, `#security vulnerability`, `#CVE-2026-53359`, `#Linux kernel`

---

<a id="item-5"></a>
## [Kokoro：本地、CPU 友好的高质量 TTS 模型](https://ariya.io/2026/03/local-cpu-friendly-high-quality-tts-text-to-speech-with-kokoro/) ⭐️ 8.0/10

Kokoro，一个拥有 8200 万参数的开源权重 TTS 模型已发布，它能在 CPU 上高效运行，无需 GPU 即可实现高质量的语音合成。 这使得没有专用 GPU 的用户也能使用高质量 TTS，为更广泛的受众提供本地化、保护隐私的自动化和无障碍工具。 Kokoro 采用 Apache 许可证，可通过 Docker 容器部署，提供 Web 界面和兼容 OpenAI 的 API，便于集成。

hackernews · speckx · 7月7日 18:24 · [社区讨论](https://news.ycombinator.com/item?id=48821576)

**背景**: 传统的文本转语音（TTS）模型需要强大的 GPU 进行实时合成，限制了其使用范围，通常只能依赖云服务或高端硬件。Kokoro 的轻量级架构（8200 万参数）在 CPU 上实现了与更大模型相当的质量，同时速度更快、成本更低。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/hexgrad/Kokoro-82M">hexgrad/Kokoro-82M · Hugging Face</a></li>
<li><a href="https://github.com/hexgrad/kokoro">GitHub - hexgrad/kokoro: https://hf.co/hexgrad/Kokoro-82M</a></li>
<li><a href="https://ariya.io/2026/03/local-cpu-friendly-high-quality-tts-text-to-speech-with-kokoro/">Local, CPU-Friendly, High-Quality TTS (Text-to-Speech) with Kokoro · ariya.io</a></li>

</ul>
</details>

**社区讨论**: 社区成员称赞 Kokoro 易于使用且 CPU 效率高，有用户构建了将文章转换为播客的流水线，还有用户将其用于无障碍产品。一些人指出了在单词语音和同形异义词发音方面的局限性，但总体评价非常积极。

**标签**: `#TTS`, `#AI`, `#accessibility`, `#open-source`, `#local-models`

---

<a id="item-6"></a>
## [欧盟强制要求所有新车安装驾驶员监控摄像头](https://allaboutcookies.org/eu-mandatory-distracted-driver-system) ⭐️ 8.0/10

自 2024 年 7 月起，欧盟《通用安全法规》(EU) 2019/2144 要求所有在欧盟销售的新车必须配备驾驶员监控系统（DMS），通过摄像头检测驾驶员分心和疲劳状态。 该法规旨在减少因驾驶员注意力不集中导致的交通事故，每年可能挽救数千人的生命，但也引发了关于隐私、用户体验以及自动警报可靠性的担忧。 DMS 使用安装在转向柱上的红外摄像头，以每秒 60 帧的速度跟踪驾驶员的面部和眼睛，并与预碰撞辅助等其他安全系统协同工作。该法规适用于 2024 年 7 月起所有新认证的乘用车。

hackernews · nickslaughter02 · 7月7日 20:50 · [社区讨论](https://news.ycombinator.com/item?id=48823557)

**背景**: 驾驶员监控系统利用摄像头和传感器检测疲劳或分心迹象，例如点头或长时间视线偏离道路。欧盟于 2019 年推出的《通用安全法规》强制要求一系列先进安全功能，以减少死亡人数并为自动驾驶铺平道路。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Driver_monitoring_system">Driver monitoring system - Wikipedia</a></li>
<li><a href="https://autovista24.autovistagroup.com/news/what-is-the-general-safety-regulation/">What is the General Safety Regulation?</a></li>
<li><a href="https://grokipedia.com/page/2026_German_vehicle_regulations">2026 German vehicle regulations</a></li>

</ul>
</details>

**社区讨论**: 评论显示观点分歧：一些用户称赞系统在捕捉分心方面的准确性，而另一些用户则批评现代汽车的整体用户体验，抱怨恼人的警报和侵入性的车道辅助。此外还有隐私担忧，以及与波音警报疲劳的类比。

**标签**: `#regulation`, `#automotive`, `#privacy`, `#safety`, `#UX`

---

<a id="item-7"></a>
## [高薪难留：德国技术工人为何离开](https://www.dw.com/en/germany-migrants-skilled-workers-integration-labor-market-bureaucracy-language-housing/a-77853162) ⭐️ 8.0/10

德国之声的一篇文章及社区讨论指出，在德国的技术工人面临官僚主义、文化障碍和有限的晋升机会，导致许多人尽管薪资优厚仍选择离开。 这对德国的技术劳动力和移民政策至关重要，因为留住技术人才对经济竞争力至关重要。讨论揭示了可能阻碍未来移民的系统性问题。 社区评论提到官僚主义缓慢、基础设施恶化以及保守的文化限制了外来者的信任和领导机会。一位评论者指出，即使是高收入者（20 万欧元以上）也在考虑离开。

hackernews · theanonymousone · 7月7日 10:42 · [社区讨论](https://news.ycombinator.com/item?id=48815982)

**背景**: 德国长期以来凭借强劲的经济和高薪吸引技术工人，但融入挑战依然存在。该国面临住房危机、基础设施老化和官僚障碍，这些问题同时影响着本地人和移民。

**社区讨论**: 评论者分享了个人经历：一位入籍公民感到不受欢迎，另一位指出除非在国际公司工作否则晋升机会有限，还有长期居民感叹基础设施和官僚主义恶化。总体情绪对德国的融入和留人政策持批评态度。

**标签**: `#immigration`, `#talent retention`, `#Germany`, `#tech workforce`, `#cultural integration`

---

<a id="item-8"></a>
## [微软裁掉 id Software 引擎团队](https://gamefromscratch.com/microsoft-fire-idtech-team-at-id-software/) ⭐️ 8.0/10

微软裁掉了 id Software（idTech 引擎系列开发商）的引擎团队，这是该工作室更广泛裁员的一部分。 此举标志着微软旗下工作室可能放弃自研引擎开发，引发对行业同质化以及 id Software 独特技术专长流失的担忧。 裁员波及负责 idTech（驱动《毁灭战士》和《雷神之锤》等游戏的引擎）的团队。微软和 id Software 均未官方确认具体裁员人数。

hackernews · bauc · 7月7日 15:33 · [社区讨论](https://news.ycombinator.com/item?id=48819244)

**背景**: id Software 是传奇游戏开发商，以 idTech 等引擎开创了第一人称射击游戏。idTech 引擎是内部技术文化的基石，约翰·卡马克曾将早期版本开源。相比之下，Epic Games 的 Unreal Engine 是广泛采用的第三方引擎，许多工作室用它来降低开发成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Id_Tech">id Tech - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Unreal_Engine">Unreal Engine</a></li>
<li><a href="https://en.wikipedia.org/wiki/Id_Software">id Software - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者担心微软通过转向 Unreal Engine 使其工作室同质化，为节省成本牺牲独特的技术文化。有人认为像卡马克开源 Quake 3 引擎那样开源 idTech 引擎是更好的策略，而另一些人则指出缺乏具体证据表明引擎团队是裁员目标。

**标签**: `#gaming`, `#layoffs`, `#game engines`, `#Microsoft`, `#id Software`

---

<a id="item-9"></a>
## [sqlite-utils 4.0 引入数据库模式迁移](https://simonwillison.net/2026/Jul/7/sqlite-utils-4/#atom-everything) ⭐️ 8.0/10

sqlite-utils 4.0 已发布，新增了内置的数据库模式迁移、通过新的 db.atomic() 方法实现的嵌套事务，以及对复合外键的支持。 这是自 2020 年 3.0 版本以来的首次大版本更新，显著增强了 sqlite-utils 作为 SQLite 数据库管理工具的能力，使 Python 开发者和数据分析师的模式变更更安全、更可重复。 迁移通过使用 Migrations 类的 Python 函数定义，利用已有的 table.transform() 方法处理 SQLite 的 ALTER TABLE 无法完成的复杂模式变更。该版本还包含一些破坏性变更，详见升级指南。

rss · Simon Willison · 7月7日 19:32

**背景**: sqlite-utils 是一个用于操作 SQLite 数据库的 Python 库和命令行工具，常用于 Datasette 生态系统中。模式迁移允许开发者对数据库模式变更进行版本控制并逐步应用，此前这需要手动操作或依赖第三方工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jul/7/sqlite-utils-4/">sqlite-utils 4.0, now with database schema migrations</a></li>
<li><a href="https://sqlite-utils.datasette.io/en/latest/migrations.html">Database migrations - sqlite-utils</a></li>
<li><a href="https://github.com/simonw/sqlite-utils">GitHub - simonw/sqlite-utils: Python CLI utility and library ... Managing Database Versions and Migrations in SQLite sqlite-utils 4.0, now with database schema migrations #Shorts SQLite Schema Versioning: Track and Apply Migrations (2026) SQLite Versioning & Migration Strategies for Evolving Apps</a></li>

</ul>
</details>

**标签**: `#sqlite`, `#python`, `#database`, `#migrations`, `#open source`

---

<a id="item-10"></a>
## [可微光线追踪用于无线电传播建模的博士论文](https://www.reddit.com/r/MachineLearning/comments/1upvkp5/phd_thesis_on_differentiable_ray_tracing_for/) ⭐️ 8.0/10

一篇博士论文发表，提出了用于无线电传播建模的可微光线追踪，通过 JAX 集成自动微分，计算物理环境中的梯度以解决逆问题和机器学习训练。 这项工作弥合了可微仿真与无线通信之间的鸿沟，为信道建模、定位和材料校准提供了基于梯度的优化，这对下一代无线设计至关重要。 论文以易于理解的教科书形式组织，分为三部分：物理基础、算法核心（包括 GPU 加速路径追踪和不连续性平滑技术）以及实际应用。作者使用 JAX 包（jaxtyping、equinox、optimistix）开发了 DiffeRT 等开源库。

reddit · r/MachineLearning · /u/jeertmans · 7月7日 13:45

**背景**: 可微光线追踪通过支持渲染管道中的梯度计算扩展了传统光线追踪，适用于逆问题和机器学习。无线电传播建模预测无线电波在环境中的传播方式，对无线网络规划至关重要。JAX 是一个支持自动微分的高性能数值计算框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://people.csail.mit.edu/tzumao/diffrt/">Differentiable Monte Carlo Ray Tracing through Edge Sampling</a></li>
<li><a href="https://research.nvidia.com/publication/2024-10_learning-radio-environments-differentiable-ray-tracing">Learning Radio Environments by Differentiable Ray Tracing | Research</a></li>
<li><a href="https://docs.jax.dev/en/latest/automatic-differentiation.html">Automatic differentiation — JAX documentation</a></li>

</ul>
</details>

**社区讨论**: Reddit 社区对该论文反响积极，评论强调其教科书式资源的价值以及将 JAX 用于可微仿真的整合。作者积极参与，回答了关于可微光线追踪和基于 JAX 的光线追踪引擎的问题。

**标签**: `#differentiable ray tracing`, `#radio propagation`, `#automatic differentiation`, `#JAX`, `#wireless communications`

---

<a id="item-11"></a>
## [Mozilla CTO 就开源 AI 报告举行 AMA](https://www.reddit.com/r/MachineLearning/comments/1upxdvc/raffi_krikorian_cto_mozilla_ama_on_the_state_of/) ⭐️ 8.0/10

Mozilla 首席技术官 Raffi Krikorian 宣布将于 7 月 14 日举行 AMA，讨论首份《开源 AI 现状》报告，内容涵盖实际生产成本、企业采用、中国效应和开发者信任。 此次 AMA 为 AI/ML 社区提供了一个难得的机会，可以直接与行业领袖探讨开源 AI 的实际现状，这对于企业和开发者在成本、信任和地缘政治因素中做出决策至关重要。 报告聚焦于“免费”模型的隐性成本、营销与实际企业采用之间的差距、有能力的中国开源模型的影响，以及来自 950 多名开发者关于工具信任的见解。Krikorian 还计划讨论“代理框架”——模型之上的基础设施层，它正成为关键战场。

reddit · r/MachineLearning · /u/raffikrikorian · 7月7日 14:51

**背景**: 开源 AI 指以宽松许可证发布的 AI 模型和工具，允许自由使用、修改和分发。“代理框架”是围绕 LLM 或 AI 代理的软件基础设施，处理记忆、工具使用和沙箱等任务，实现自主行为。“中国效应”描述了中国 AI 实验室以低成本或免费发布有竞争力的开放权重模型，从而重塑全球 AI 开发中的杠杆关系。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.langchain.com/blog/the-anatomy-of-an-agent-harness">The Anatomy of an Agent Harness - langchain.com</a></li>
<li><a href="https://www.technologyreview.com/2026/04/21/1135658/china-open-source-models-ai-artificial-intelligence/">China’s open-source bet: 10 Things That Matter in AI Right ...</a></li>
<li><a href="https://www.mozilla.org/en-US/foundation/annualreport/2024/article/evolving-together-redefining-mozilla-in-the-ai-era/">Evolving Together: Redefining Mozilla in the AI Era</a></li>

</ul>
</details>

**标签**: `#open source AI`, `#Mozilla`, `#enterprise AI`, `#AI costs`, `#developer trust`

---

<a id="item-12"></a>
## [通过可信 LoRA 子空间防御微调投毒](https://www.reddit.com/r/MachineLearning/comments/1uq68li/what_if_a_model_could_only_learn_what_trusted/) ⭐️ 8.0/10

一篇新论文提出将微调限制在从可信 LoRA 适配器学习到的子空间中，使恶意更新在几何上不可达。该方法在 196 个公开 LoRA 适配器上进行了测试，对自适应攻击表现出强大的防御能力。 这为微调投毒攻击提供了一种新颖的防御方法，而投毒攻击是 AI 安全领域日益严重的问题。通过限制可学习更新的空间，它提供了一种主动防御替代基于检测的方法，有望提高生产环境中微调模型的安全性。 该防御将更新限制在由可信 LoRA 适配器张成的子空间中，确保只能学习池中已有的行为。论文报告称，攻击成功率大幅下降，而在适配器池覆盖的任务上，有用的适应能力基本得以保留。

reddit · r/MachineLearning · /u/Bright_Warning_8406 · 7月7日 20:00

**背景**: LoRA（低秩适应）是一种参数高效的微调方法，学习对预训练权重的低秩更新。微调投毒攻击通过注入恶意数据使模型学习隐藏后门。现有防御通常检测或过滤投毒数据，而这项工作通过几何约束更新空间采取了不同方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.01938">[2510.01938] StelLA: Subspace Learning in Low-rank Adaptation ... StelLA: Subspace Learning in Low-rank Adaptation using ... SuLoRA: Subspace Low-Rank Adaptation for Parameter-Efficient ... SuLoRA: Subspace Low-Rank Adaptation for Parameter-Efcient ... GitHub - SonyResearch/stella: StelLA: Subspace Learning in ... LaST-LoRA: Adaptive Knowledge Reuse and Latent Subspace ...</a></li>

</ul>
</details>

**社区讨论**: Reddit 评论讨论了该方法的可行性和局限性，一些人质疑子空间约束是否也会限制有益的适应。其他人表示有兴趣看到该方法被攻破，并提出了潜在的改进建议。

**标签**: `#AI Safety`, `#Fine-tuning`, `#LoRA`, `#Adversarial Robustness`, `#Machine Learning`

---

<a id="item-13"></a>
## [马斯克解散 xAI，更名为 SpaceXAI](https://x.com/i/status/2074214064746832060) ⭐️ 8.0/10

埃隆·马斯克宣布解散 xAI，将其更名为 SpaceXAI 并完全并入 SpaceX。该公司已在与 Anthropic 的计算合作公告中开始使用 SpaceXAI 这一名称。 此次重组将马斯克的 AI 工作整合到 SpaceX 旗下，可能加速 AI 在太空探索及其他领域的应用开发。这也标志着 xAI 作为独立实体的终结，重塑了 AI 初创公司的竞争格局。 收购于 2026 年 2 月 2 日完成，SpaceX 估值 1 万亿美元，xAI 估值 2500 亿美元。SpaceXAI 的核心产品仍是 Grok 聊天机器人，同时还运营 Colossus 超级计算机和数据中心业务。

telegram · zaihuapd · 7月7日 02:30

**背景**: xAI 由埃隆·马斯克于 2023 年创立，是一家独立的 AI 公司，旨在开发 Grok 聊天机器人。2026 年 2 月，SpaceX 以全股票交易方式收购了 xAI，使其成为全资子公司。更名为 SpaceXAI 反映了其与 SpaceX 运营的更深层次整合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/XAI_(company)">SpaceXAI - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/SpaceXAI">SpaceXAI</a></li>
<li><a href="https://www.businessinsider.com/xai-rebrand-spacexai-new-logo-x-handle-spacex-2026-7">XAI Rebrands to SpaceXAI With New Logo, X Handle, Under ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#Elon Musk`, `#xAI`, `#SpaceX`, `#corporate restructuring`

---

<a id="item-14"></a>
## [中国拟投 2 万亿元建设全国算力网络，优先采用国产 AI 芯片](https://t.me/zaihuapd/42399) ⭐️ 8.0/10

中国计划未来五年投入约 2 万亿元（2950 亿美元），建设全国互联数据中心网络，由国有电信企业运营主要设施。该计划优先采用华为等本土供应商的 AI 芯片，目标国产化率至少 80%，以减少对英伟达、AMD 等美国公司的依赖。 这一巨额投资标志着中国在 AI 基础设施上实现自给自足的战略推进，可能重塑全球技术供应链。将区域算力资源整合为统一网络，有望加速各行业 AI 应用，并减少对外国技术的依赖。 该计划是北京“六网”基础设施计划的关键一环，旨在整合分散的区域算力资源。中国电信、联通等运营商已推出 token 套餐，将算力像移动数据一样打包销售，为大规模 AI 应用铺路。

telegram · zaihuapd · 7月7日 04:45

**背景**: 中国的“东数西算”工程和全国一体化算力网旨在通过跨区域连接数据中心，解决供需错配和成本高昂的问题。“六网”计划包括水网、电网、通信网、地下管网、物流网和算力网，总投资超过 7 万亿元。基于 token 的算力定价是一种新模式，用户按 token 付费，类似移动数据套餐，使 AI 算力更易获取。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/2023358290831111769">国家数据局最新部署：全国一体化算力网8大枢纽+10大集群最全梳理</a></li>
<li><a href="https://www.gov.cn/zhengce/zhengceku/202401/content_6924596.htm">关于深入实施“东数西算”工程加快构建全国一体化算力网的实施意见_国务...</a></li>
<li><a href="https://news.qq.com/rain/a/20260518A05V3X00">Token套餐全面上线!三大运营商悉数入局，算力进入“按Token收费”时代_...</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#China tech policy`, `#semiconductors`, `#cloud computing`, `#national strategy`

---

<a id="item-15"></a>
## [DeepSeek 自研 AI 推理芯片，减少对英伟达和华为依赖](https://www.reuters.com/world/china/chinas-deepseek-developing-its-own-ai-chip-sources-say-2026-07-07/) ⭐️ 8.0/10

据三位知情人士透露，中国 AI 公司 DeepSeek 正在开发自己的 AI 芯片，专注于推理阶段，以减少对英伟达和华为的依赖。该项目始于约一年前，目前仍处于早期阶段，DeepSeek 已开始招募芯片设计工程师，并与代工厂和存储公司接洽。 这一战略举措可能重塑 AI 硬件格局，在美国出口管制下减少 DeepSeek 对受制裁芯片供应商的依赖。它也凸显了中国 AI 公司为应对地缘政治紧张局势并保障供应链安全而自主研发芯片的日益增长趋势。 该芯片专为推理设计，这是 AI 计算需求增长最快的领域，而非训练。DeepSeek 此前依赖英伟达 H800 和华为昇腾芯片，创始人梁文锋在 2024 年一次罕见采访中承认芯片管制是公司面临的挑战。

telegram · zaihuapd · 7月7日 11:08

**背景**: 美国出口管制限制向中国出口先进 GPU 和半导体制造设备，旨在限制中国的 AI 能力。以成本高效的 AI 模型闻名的 DeepSeek，如今正加入其他中国公司的行列，开发本土替代方案以应对这些限制并减少对外国供应商的依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/world/china/chinas-deepseek-developing-its-own-ai-chip-sources-say-2026-07-07/">EXCLUSIVE: China's DeepSeek developing its own AI chip ...</a></li>
<li><a href="https://www.cryptopolitan.com/deepseek-plans-its-own-inference-chip/">DeepSeek plans its own inference chip, a threat to Nvidia and ...</a></li>
<li><a href="https://tech-ish.com/2026/07/07/deepseek-own-ai-inference-chip-nvidia-huawei/">DeepSeek is building its own AI chip to cut reliance on ...</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#DeepSeek`, `#US-China tech`, `#semiconductors`, `#inference`

---

<a id="item-16"></a>
## [中国拟限制顶尖 AI 模型出口](https://www.reuters.com/world/beijing-is-looking-curbing-overseas-access-chinas-top-ai-models-sources-say-2026-07-07/) ⭐️ 8.0/10

中国商务部已召集阿里巴巴、字节跳动和智谱 AI 等企业开会，讨论限制海外用户访问国内最先进的 AI 模型，包括尚未发布的版本。 此举可能重塑全球 AI 格局，限制具有竞争力的中国 AI 模型的海外可用性，可能增加外国开发者的成本，并加速中美 AI 生态系统的脱钩。 限制可能同时适用于闭源和开源模型，包括可下载的权重文件，并可能限制境外资本投资国内 AI 初创企业。最终范围仍在商讨中。

telegram · zaihuapd · 7月7日 11:42

**背景**: 中国 AI 模型（如 DeepSeek 的 R1）因其低成本和高性能而获得全球关注。拟议的出口管制旨在防止核心 AI 技术泄露，这可能被视为对国家安全的威胁。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/2058096089899721357">中国也要限制AI模型出口了，中美AI正式脱钩 - 知乎</a></li>
<li><a href="https://www.yzaobao.com/news/china/202607/0775872.html">路透：北京研究限制海外获取中国最先进AI模型_联合早报网</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#China`, `#export control`, `#national security`, `#geopolitics`

---