---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 31 条内容中筛选出 17 条重要资讯。

---

1. [Claude 破解 NIST ECDSA 曲线种子来源之谜](#item-1) ⭐️ 8.0/10
2. [Mercor 研究：美国 90%的工作时间缺乏 AI 基准测试覆盖](#item-2) ⭐️ 8.0/10
3. [苹果 MLX 新增分布式推理，四台 Mac Studio 跑通近万亿参数模型](#item-3) ⭐️ 8.0/10
4. [Anthropic IPO 估值预期下调至 1.5 万亿美元](#item-4) ⭐️ 8.0/10
5. [Waymo 宣布进军多伦多，引发自动驾驶出租车热议](#item-5) ⭐️ 7.0/10
6. [StarSkirmish Bench v0.2：让大模型在一小时内编写《星际争霸》机器人](#item-6) ⭐️ 7.0/10
7. [Rust 框架 DenseCore 在 CPU 上逐位复现 PyTorch 的 nanoGPT 训练](#item-7) ⭐️ 7.0/10
8. [阶跃星辰发布 Step 5 Preview 智能体旗舰模型](#item-8) ⭐️ 7.0/10
9. [商务部拟对 40 项 AI、生物医药、光伏技术实施出口管制并公开征求意见](#item-9) ⭐️ 7.0/10
10. [特斯拉发布搭载 SpaceX 冷气推进器的新款 Roadster](#item-10) ⭐️ 6.0/10
11. [博文《我爱软件渲染》引发 Hacker News 激辩](#item-11) ⭐️ 6.0/10
12. [快手可灵 Kling 4.0 全量上线，接入 MCP/CLI 并将开放 API](#item-12) ⭐️ 6.0/10
13. [未经证实的消息称 OpenAI 将 GPT-Live-1 全双工语音模型上线 API](#item-13) ⭐️ 6.0/10
14. [市场回调与利率上升冲击 AI 数据中心交易热潮](#item-14) ⭐️ 6.0/10
15. [长宁 4.7 级地震首报 7.7 级，为 15 年来最大偏差](#item-15) ⭐️ 6.0/10
16. [传闻苹果折叠屏 iPhone Duo 一分钟售罄，盘前股价涨超 2%](#item-16) ⭐️ 6.0/10
17. [法院文件曝光：Telegram 向美国执法部门移交用户数据](#item-17) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Claude 破解 NIST ECDSA 曲线种子来源之谜](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 8.0/10

Anthropic 前沿红队（Frontier Red Team）称，Claude 在不到半小时内就找出了 NIST P-192、P-224、P-256、P-384 和 P-521 五条椭圆曲线种子值的来源：它们并非长期假设的哈希算法产物，而是 C 标准库中 lrand48 伪随机数生成器以 Unix 时间戳作为种子生成的输出。Anthropic 以「ECDSA 曲线种子的起源」为题发布了这项研究，密码学工程师 Filippo Valsorda 也撰文披露了细节。 这些种子值是证明 NIST 广泛部署的曲线是「袖中无物」（nothing up my sleeve）式公正生成、而非有意嵌入后门的主要公开证据，因此这一发现部分终结了密码学界争论数十年、并在 Dual_EC_DRBG 事件后进一步升温的争议。同时，它也生动展示了 AI 辅助研究在破解长期悬而未决的密码学问题上的能力。 lrand48 是 System V Unix 中一个 48 位线性同余伪随机数生成器，其输出完全由单个种子值决定；该发现表明这些种子不过是被送入 srand48 的时间戳，本身几乎不含熵，无法提供任何密码学保证。关键在于，这一结果只解释了种子「如何生成」，却没有解释曲线「如何被挑选」——用其他时间戳生成后被丢弃的候选曲线无从查看，因此在理论上仍可能通过遍历时间戳来刻意筛选出特定性质；此外第五条二进制曲线种子 B-163 至今与 Claude 尝试的任何方法都不吻合，最可能的解释是公布过程中出现了一个数字笔误。

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**背景**: ECDSA（椭圆曲线数字签名算法）是 TLS/HTTPS、加密货币以及无数安全系统使用的签名方案，其安全性依赖于 NIST 标准化的命名曲线的具体参数。为了证明这些常量不是为隐藏弱点而人为挑选的，标准机构通常会公布一个「种子」（seed）——即通过哈希该值来派生曲线参数——以便任何人都能重现派生过程，检验设计者没有随意挑选恶意曲线的自由。由于现代基于哈希的种子看起来随机却可验证，密码学家长期假定 NIST 的种子是对某个短语做哈希得到的；当这一假定无法重现种子时，怀疑便挥之不去，Koblitz 与 Menezes 的论文《谜中之谜》（A Riddle Wrapped in an Enigma）便是代表。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/ecdsa-curve-origins">Claude reveals ECDSA curve origins \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm">Elliptic Curve Digital Signature Algorithm - Wikipedia</a></li>
<li><a href="https://www.ibm.com/docs/en/zos/3.1.0?topic=functions-lrand48-pseudo-random-number-generator">lrand 48 () — Pseudo- random number generator</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍觉得这一结果十分精彩，但对其证明力提出保留：有人指出，确认生成方法并不能说明曲线是如何被挑选的，因为在使用时间戳的几个月里生成后又丢弃的候选值无从查看，仍然存在遍历时间戳进行筛选的可能。另一个反复出现的担忧是模型提供方（及其政府合作方）与公众之间日益扩大的能力鸿沟，有人认为开源模型是弥合这一鸿沟的唯一途径；也有人打趣说这终于「终结了 13 年的阴谋论」，并猜测 B-163 的种子只是被打错了一个数字。

**标签**: `#cryptography`, `#ECDSA`, `#AI-assisted-research`, `#NIST-standards`, `#security`

---

<a id="item-2"></a>
## [Mercor 研究：美国 90%的工作时间缺乏 AI 基准测试覆盖](https://www.mercor.com/research/labor-index/benchmark-map/) ⭐️ 8.0/10

Mercor 发布了一份名为“Benchmark Map”的劳动指数研究，发现美国约 90%的工作时间花在现有 AI 基准测试覆盖不佳、甚至完全没有覆盖的任务上，因此很难判断模型在美国人实际从事的工作上表现如何。该分析将基准测试的提示词与 O*NET 职业任务数据进行映射，并将其定位为构建“持续更新的全经济 AI 能力资源”的第一步。 这一发现表明，热门的基准测试分数可能无法反映真实的经济能力，从而可能误导研究人员、政策制定者和企业对 AI 究竟能自动化或增强哪些工作的判断。它还引发了人们对评测优先级的担忧：数据显示，即便在控制了 AI 暴露度之后，高薪职业的任务在基准提示词中仍被过度代表。 覆盖度是在任务层面上依据 O*NET 职业定义来判定的，甚至像“社工就育儿问题为家长提供咨询”这样的类别，仅凭 13 条提示词就被算作“覆盖良好”，评论者认为这一门槛过于宽松，远不足以代表这类工作。该指数被明确描述为第一步，因此其方法论预计会随时间不断完善和扩展。

hackernews · speckx · 10月16日 17:08 · [社区讨论](https://news.ycombinator.com/item?id=50121179)

**背景**: AI 基准测试是由提示词和任务组成的标准化测试集，用于给模型能力打分，但它们由研究者和实验室编写，而非从真实经济活动中采样。O*NET（职业信息网络）由美国劳工部维护，是一个免费数据库，收录了约一千种职业定义及其所需的任务、技能和能力。Mercor 的 Benchmark Map 把两者结合起来，考察美国经济中的工作究竟有多少真正被基准提示词所代表。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mercor.com/research/labor-index/benchmark-map/">A benchmark map of the US economy | Mercor</a></li>
<li><a href="https://en.wikipedia.org/wiki/Occupational_Information_Network">Occupational Information Network - Wikipedia</a></li>
<li><a href="https://www.onetcenter.org/database.html">O*NET Database at O*NET Resource Center</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认可这一差距，但在方法论和影响上存在分歧：有人 argued 数据表明基准制定者希望 AI 取代“好”工作；有人指出，对于仅由 13 条提示词支撑的类别，“覆盖良好”实际上等于“根本没有覆盖”；还有人以“门卫谬误”为例，指出自动化某个显性任务往往会摧毁那些未被衡量的价值。也有人持更悲观的看法，调侃软件工程师约 80%的工作是在处理利益相关者之间的分歧，或声称大多数人本来就没有产生可自动化的产出。

**标签**: `#AI benchmarks`, `#labor market`, `#AI evaluation`, `#future of work`, `#O*NET`

---

<a id="item-3"></a>
## [苹果 MLX 新增分布式推理，四台 Mac Studio 跑通近万亿参数模型](https://machinelearning.apple.com/research/mlx-distributed-inference) ⭐️ 8.0/10

苹果机器学习研究团队发布了 MLX 的分布式推理能力，并同步推出了新版本的 MLX，使 Meta 的近万亿参数开放权重模型 Muse Spark Open 能够在由四台 Mac Studio 组成的集群上以每秒超过 36 个 token 的速度运行。单台配备最高 512GB 统一内存的 Mac Studio 即可先行承载该模型，随后再横向扩展至多台机器。 这表明前沿级、接近万亿参数的模型不再严格依赖数据中心 GPU，对注重隐私的本地与端侧大模型工作流意义重大，也强化了苹果芯片作为 Mac 端推理平台的地位。同时它还加深了苹果 MLX 生态与 Meta 开放权重模型之间的绑定，为开发者提供了 H100 级硬件之外的一个实用替代方案。 这些数字是在以 4-bit 量化后的 Muse Spark Open 上测得的，而苹果在单台 Mac Studio 上的对比则把 Qwen 3.8 27B、Mistral Medium 3.5 128B 等模型跑在原生精度下，因此不同模型家族之间的吞吐量数据并非完全对等。分布式推理依赖 Mac 之间基于 Thunderbolt 5 的 RDMA 连接，其扩展瓶颈更多是每个节点的统一内存上限（最高 512GB），而非单纯算力。

hackernews · antipaul · 10月16日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=50118320)

**背景**: MLX 是苹果专为 Apple 芯片打造的开源数组与机器学习框架，它利用统一内存架构，使 CPU 与 GPU 可以直接操作同一份数据，无需在各自独立的内存池之间拷贝。Muse Spark Open 来自 Meta 的 Meta Superintelligence Labs，是一款面向长周期智能体编程任务的稀疏混合专家（MoE）开放权重模型；所谓 MoE，是指每个 token 只激活部分参数，因此其推理成本远低于总参数量所暗示的水平。分布式推理则是把单个模型的权重与计算分散到多台机器上，苹果的实现采用张量并行，并通过 Thunderbolt 5 上的 RDMA 把多台 Mac 连接成一个小型集群。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://machinelearning.apple.com/research/mlx-distributed-inference">Local and Distributed Large LLM Inference with MLX and RDMA ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/MLX_(Apple_ML_framework)">MLX (Apple ML framework)</a></li>
<li><a href="https://research.meta.ai/blog/muse-spark-open">Introducing Muse Spark Open, The Most Capable US Open‑Weight ...</a></li>

</ul>
</details>

**社区讨论**: 评论区整体持怀疑态度，认为苹果实际上是在为 Meta 的模型做营销，并且该基准测试并不公平——Muse Spark Open 是按 4-bit 量化测量的，而 Qwen 只以原生 BF16 精度作对比。也有人指出这篇新闻稿几乎没有点名 Meta；还有开发者分享了自己的独立测试数据：单台 256GB 内存的 M5 Ultra 运行 DeepSeek 4.1 Flash 时，prefill 约为 3200 tok/s、解码约 45 tok/s，暗示单机方案可能已经具备竞争力。

**标签**: `#MLX`, `#Apple`, `#distributed-inference`, `#LLM`, `#local-inference`

---

<a id="item-4"></a>
## [Anthropic IPO 估值预期下调至 1.5 万亿美元](https://www.reuters.com/business/finance/investors-temper-anthropic-ipo-valuation-expectations-over-revenue-growth-2026-10-15/) ⭐️ 8.0/10

部分投资者将 Anthropic 的 IPO 估值预期从此前的 2 万亿美元下调至约 1.5 万亿美元，尽管该公司第三季度营收达 168 亿美元、环比增长 45%，并实现经调整后盈利和季度现金流转正。路透社将此次下调归因于增速放缓、前沿模型之间的价格竞争加剧以及算力投入带来的资金压力。 作为最受关注、最接近上市的头部 AI 公司之一，Anthropic 的估值回调可能成为整个行业的压力测试，并对智谱 AI、MiniMax、Kimi（月之暗面）和 DeepSeek 等公司的估值形成压制。这表明投资者的关注点正从单纯的收入增速转向收入可持续性、毛利率和资本效率。 此次下调源于投资者提到的三重压力：增速放缓、模型价格战，以及算力成本。值得注意的是，这反映的是投资者愿意支付的估值倍数发生变化，而非 Anthropic 自身经营出现恶化——该公司营收仍环比增长 45%，并已实现现金流转正。

telegram · zaihuapd · 10月16日 15:46

**背景**: Anthropic 是一家美国 AI 实验室，开发 Claude 系列大语言模型，被普遍视为 OpenAI 最主要的挑战者之一，其在编程智能体等方向上的商业化成功也被认为带动了更广泛的 AI 产业链。IPO 估值预期由潜在机构投资者而非公司本身决定，因此会随市场对增长与盈利能力的情绪而波动。智谱 AI、MiniMax、Kimi（月之暗面）和 DeepSeek 等中国 AI 公司常被拿来与 Anthropic 对标——例如智谱就曾以“中国版 Anthropic”作为资本叙事——因此 Anthropic 预期定价的下调往往会直接传导到这些公司的估值逻辑上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cj.sina.com.cn/articles/view/1863057363/6f0bffd301901rk0u">对标Anthropic？ 5个月暴涨13倍的 智 谱 AI 凭 什 么 __财经头条__新浪财经</a></li>
<li><a href="https://zh.wikipedia.org/wiki/稀宇科技">MiniMax - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.minimax.cn/about">MiniMax - 关于我们 | MiniMax</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#IPO`, `#AI industry`, `#venture capital`, `#market valuation`

---

<a id="item-5"></a>
## [Waymo 宣布进军多伦多，引发自动驾驶出租车热议](https://waymo.com/blog/2026/10/waymo-in-toronto/) ⭐️ 7.0/10

Waymo 在其官方博客发布公告，宣布将自动驾驶网约车服务引入加拿大多伦多，把公司的 robotaxi 业务版图从目前运营的美国城市进一步向外扩展。该公告发布于 2026 年 10 月，随即在 Hacker News 上引发 277 条评论的热烈讨论，话题集中在乘车体验、定价与可靠性上。 对 Waymo 而言，多伦多意味着一个全新的国家和监管环境，而此前它的商业 robotaxi 服务一直集中在美国各大都市区。如果跨境扩张成功，将进一步证明自动驾驶网约车具备国际化落地的能力，而不只是美国本土的实验；同时也将迫使加拿大各城市面对目前几乎空白的无人驾驶车辆法规问题。 截至 2026 年年中，Waymo 的规模约为 3,871 辆 robotaxi，每周约 50 万次付费行程，在 10 个美国都市区累计完成 2 亿英里全自动驾驶里程，因此多伦多是为这项仍在全行业亏损的服务新增的重要据点。与此同时，Waymo 在 2026 年初也处于监管审视之下：NTSB 与 NHTSA 于 2026 年 1 月就其 robotaxi 多次违规超越停靠的校车，以及一起在学区撞到突然从停放 SUV 后方跑出的儿童的事故展开调查。

hackernews · ChrisArchitect · 10月16日 14:44 · [社区讨论](https://news.ycombinator.com/item?id=50118981)

**背景**: Waymo 是 Alphabet 旗下的自动驾驶子公司，其源头可追溯到 2009 年启动的谷歌自动驾驶汽车项目以及斯坦福大学的 DARPA 无人车挑战赛团队；该项目于 2016 年 12 月独立并更名为 Waymo，并在 2020 年 10 月成为首家向公众提供无安全员载客服务的公司。Robotaxi 指用于网约车服务的 SAE 四级或五级自动驾驶汽车，即在特定服务区域内无需人类驾驶员即可行驶。Robotaxi 的商业逻辑在于取消司机成本以降低车费，但整个行业目前仍在亏损，公众信任度也偏低——2025 年 AAA 的一项调查显示，仅有 13% 的受访者表示愿意信任自动驾驶汽车。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Waymo">Waymo</a></li>
<li><a href="https://en.wikipedia.org/wiki/Robotaxi">Robotaxi</a></li>
<li><a href="https://waymo.com/">Waymo - Self-Driving Cars - Autonomous Vehicles - Ride - Hail</a></li>

</ul>
</details>

**社区讨论**: 社区情绪褒贬不一：有用户称赞乘车体验，说旧金山的 Waymo“一直很棒”，还有人兴奋地在东京街头看到 Waymo；但也有用户反映洛杉矶的定价大幅上涨，一段短途行程报价超过每英里 10 美元。一位评论者讲述在奥斯汀的糟糕经历：原本 9 分钟的车程被临时延长到 45 分钟，最后客服把他们丢在一家餐厅；另一位则提出安全与法律层面的担忧，称丹佛有一辆 Waymo 开进了农贸市场，而当地警察表示现行法律无法对无人驾驶汽车提起指控。

**标签**: `#Waymo`, `#autonomous-vehicles`, `#robotaxi`, `#Toronto`, `#HN-discussion`

---

<a id="item-6"></a>
## [StarSkirmish Bench v0.2：让大模型在一小时内编写《星际争霸》机器人](https://starskirmish.com/bench/v0-2/) ⭐️ 7.0/10

StarSkirmish Bench v0.2 发布，评测 OpenAI、Anthropic、Google 和 Meta 的旗舰模型能否在一小时挂钟时间内用 C++ 写出尽可能强的《星际争霸：母巢之战》机器人，Gemini 4 Argon 也在参评之列。GPT-6 Astra 以约 57% 的得分（对阵人类编写机器人基线）领先，其后依次是 GPT-6.1 Sol、Gemini 4 Argon、Claude Opus 5.5、Claude Fable 5.1 和 Claude Sonnet 5.5。 这是一个长时程的智能体编程基准，而非聊天式评测，因此其结果直接反映前沿模型在严格时限下处理一个需求模糊、反馈稀缺的编程任务的能力。Hacker News 上的讨论指出，该榜单与一个独立的 9x9 围棋基准排名一致，如果这一相关性成立，则说明这类基准衡量的可能是相当通用的智能体能力，而非特定游戏的知识。 每个模型都在各自实验室的第一方 CLI 工具链中以可用的最高推理档位运行——Anthropic 用 Claude Code、OpenAI 用 Codex、Google 用 Antigravity CLI、Meta 用 Muse Code——并关闭联网搜索与网页抓取，模型没有其他互联网访问；Gemini 4 Argon 以对其可用的最高档位 "high" 运行。所有机器人都基于 BWAPI 4.4.0 并通过 OpenBW 运行，目前计分对局仅限神族对神族，即便是排名最高的模型也仍然不敌顶尖人类编写的机器人。

hackernews · __cayenne__ · 10月16日 14:18 · [社区讨论](https://news.ycombinator.com/item?id=50118688)

**背景**: 《星际争霸：母巢之战》是一款数十年来被当作 AI 挑战目标的即时战略游戏，因为它要求在不完全信息下进行资源管理、侦察、开局建造顺序规划以及单位微操。BWAPI 是一个历史悠久的接口，允许程序通过代码控制游戏客户端；OpenBW 则是该引擎的开源重实现，常用于无界面高速运行机器人。StarSkirmish 把通常的做法反过来：不让模型直接玩游戏，而是给它一小时去编写机器人代码，因此考察的是智能体式的软件工程能力，而不是实时反应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://starskirmish.com/bench/">StarSkirmish Bench</a></li>
<li><a href="https://www.youtube.com/watch?v=0BRyMXNgl4A">AI News: StarSkirmish Bench v0.2 — Explained in 60s - YouTube StarSkirmish Bench v0.2 - LLMs write · Hacker News | Zeli I'm launching StarSkirmish, an arena for LLMs to create ... StarSkirmish Bench v0.2: LLMs Write StarCraft Bots in One ...</a></li>
<li><a href="https://grokipedia.com/page/Gemini_4_Argon">Gemini 4 Argon</a></li>

</ul>
</details>

**社区讨论**: 这条约 73 条评论的讨论整体参与度高，也带有怀疑色彩。有评论者（GodelNumbering）指出，StarSkirmish 的排名顺序与一个以 KataGo 为对手锚点的独立 9x9 围棋基准完全一致，从而引出大模型智能体能力是否具有跨领域通用性的问题；另一位评论者（cgearhart）则质疑，智能体编写的机器人除了是人类机器人的劣化复制品之外还能带来什么洞见，以及它们是否只是照搬了从人类编写的机器人代码中学到的技巧。还有人提到 broodbench.com——一个让模型直接玩《星际争霸》的基准，并建议让这些机器人去对阵实力强劲的神经网络机器人 Pluto。

**标签**: `#LLM benchmarks`, `#AI agents`, `#code generation`, `#StarCraft`, `#model evaluation`

---

<a id="item-7"></a>
## [Rust 框架 DenseCore 在 CPU 上逐位复现 PyTorch 的 nanoGPT 训练](https://www.reddit.com/r/MachineLearning/comments/1x7ojxo/p_my_rust_framework_trains_nanogpt_with_the_exact/) ⭐️ 7.0/10

一名计算机科学专业的学生发布了 DenseCore，这是一个用 Rust 编写、带类 PyTorch Python API 的小型深度学习框架。他声称把 `import torch` 指向它并在 CPU 上原样运行 Andrej Karpathy 的 nanoGPT，可以得到与 PyTorch 逐位完全相同的结果——从 `manual_seed` 得到的初始权重、损失、梯度、权重在他测试的全部 50 个训练步骤中都一致，即便开启 dropout 也是如此。该项目体积约 2 MB，而 PyTorch 约 580 MB，作者目前公开征询是否值得继续做下去。 两个独立实现之间做到逐位一致是极难达成的目标，而作者逆向出的 PyTorch 内部细节（flash attention 路径、Adam 在尾部循环上的舍入方式、`clip_grad_norm_` 用 `reciprocal() * max_norm` 而非除法）对任何追求深度学习可复现性的人都很有参考价值。它还凸显了一个常被忽视的事实：PyTorch 自身在不同机器之间都无法复现，这对 CI 流水线、无服务器推理以及排查不稳定的训练过程都意义重大。 作者发现 PyTorch 的 CPU attention 并非教科书公式，而是一个 flash attention 内核，并在开启 dropout 时切换到另一条路径；Adam 由于编译器对尾部循环的融合，在每个线程分块的最后几个元素上舍入方式不同；`clip_grad_norm_` 实际计算的是 `reciprocal() * max_norm` 而非除法。一个关键限制是：PyTorch 在不同机器之间自身都不一致——在他测试的 26 个算子中，只有 1 个在 macOS 与 Linux x86 之间产生完全相同的比特——因此 DenseCore 只在 Apple Silicon Mac 上与 PyTorch 保持一致。

reddit · r/MachineLearning · /u/Mental-Feature-2377 · 10月16日 18:49

**背景**: nanoGPT 是 Andrej Karpathy 编写的极简、易读的 GPT Transformer 架构实现，常被用作训练代码的小规模试验平台。PyTorch 是主流深度学习框架，而 FlashAttention 是一种 IO 感知的精确注意力算法，通过对计算分块来减少显存读写，这正是它的数值序列与朴素注意力实现不同的原因。`clip_grad_norm_` 是 PyTorch 的梯度裁剪工具，会按比例缩放梯度使其全局范数不超过阈值。由于浮点加法不满足结合律，运算顺序或融合方式的任何改变都会影响结果，因此要与另一个框架做到逐位一致，就必须精确复刻其内核行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/nanoGPT">nanoGPT</a></li>
<li><a href="https://en.wikipedia.org/wiki/FlashAttention">FlashAttention</a></li>
<li><a href="https://docs.pytorch.org/docs/stable/search.html?q=clip_grad_norm&check_keywords=yes&area=default">Search - PyTorch 2.10 documentation</a></li>

</ul>
</details>

**标签**: `#Rust`, `#PyTorch`, `#Deep Learning Framework`, `#Reproducibility`, `#Numerical Computing`

---

<a id="item-8"></a>
## [阶跃星辰发布 Step 5 Preview 智能体旗舰模型](https://huggingface.co/stepfun-ai/Step-5-Preview) ⭐️ 7.0/10

阶跃星辰在 Hugging Face 上发布了旗舰模型 Step 5 Preview，采用稀疏 MoE 架构，总参数 6000 亿、每次激活 270 亿参数，支持最高 100 万 token 的上下文窗口，并可接收文本、图像和视频输入。该模型主打智能体工作流，官方称其在软件工程、长周期智能体执行以及专业知识任务上表现领先，尤其在金融场景中表现突出。 此次发布使阶跃星辰与其他推出开放权重智能体模型的中国大厂正面竞争，而 6000 亿总参数仅激活 2700 亿的组合，使推理成本远低于同等规模的稠密模型。由于该模型可通过 OpenAI 兼容 API 在 vLLM 或 SGLang 上部署，企业和开发者可以自托管一个具备智能体能力的前沿模型，而不必完全依赖闭源 API 供应商。 该模型采用 StepFun Model License 1.0 许可，这是一份自定义许可而非标准的完全宽松开源协议，因此商业使用条款需要仔细审阅。同时它被明确标注为“Preview”（预览）版本，意味着其基准测试成绩和长上下文表现尚未经过社区的独立验证。

telegram · zaihuapd · 10月16日 06:36

**背景**: 混合专家（MoE）是一种模型架构，其中包含许多独立的“专家”子网络，但每个 token 只被路由到其中少数几个；因此像这样的稀疏 MoE 拥有巨大的总参数量，却每次只激活一小部分，用内存换取计算效率。100 万 token 的上下文窗口让模型可以一次性处理超长输入，例如整个代码库或长篇文档，这对需要多步执行的智能体任务尤为重要。vLLM 和 SGLang 是开源的高吞吐推理引擎，均实现 OpenAI 兼容 API，因此在它们之上部署的模型可以直接替代闭源 API 使用。所谓“智能体”模型，是指经过专门调优、能够规划、调用工具并执行多步任务，而不仅仅是回答单个问题的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/VLLM">VLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/SGLang">SGLang</a></li>
<li><a href="https://www.emergentmind.com/topics/extreme-sparsity-mixture-of-experts-moe-architecture">Extreme- Sparsity MoE Architecture</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Mixture-of-Experts`, `#AI Agents`, `#Multimodal`, `#Model Release`

---

<a id="item-9"></a>
## [商务部拟对 40 项 AI、生物医药、光伏技术实施出口管制并公开征求意见](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 7.0/10

2026 年 10 月 16 日，商务部、科技部发布 2026 年第 48 号公告，就修订《中国禁止出口限制出口技术目录》公开征求意见，并对相关技术实施出口前登记的临时管理措施。此次拟新增 40 项技术，涉及人工智能领域 23 项（大模型、智能体、算力集群、信息处理）、生物医药领域 5 项（细胞和基因治疗、小核酸药、病原微生物）以及光伏领域 12 项（多晶硅制造、硅片制造、电池制造，并涵盖承载相关技术的关键和核心设备）。 如果最终落地，这些管制将使北京在人工智能前沿、先进生物疗法以及中国占据全球主导地位的光伏供应链上获得监管抓手。与中国伙伴开展技术许可、转让或联合开发的跨国企业将面临登记与许可要求，从而给跨境交易、研发合作和产能扩张带来合规风险与潜在延误。 草案设有两项缓冲安排：已通过开源或发表学术论文等方式进入公共领域的技术不纳入管理范围；在生物医药领域，不涉及所有权转让的对外授权模式可适用自动许可等便利措施。临时登记管理自公告发布之日起、至《目录》正式修订公告实施之日止，且该文本仍属公开征求意见的草案，并非已定稿的正式规则。

telegram · zaihuapd · 10月16日 09:12

**背景**: 《中国禁止出口限制出口技术目录》是中国的技术出口管制清单，依据《中华人民共和国对外贸易法》第十八条、第二十条和《中华人民共和国技术进出口管理条例》制定，列入其中的技术或被禁止出口，或需取得出口许可。该目录会定期修订以反映技术发展变化，本轮修订针对的是中国已形成竞争优势的领域。所谓“临时登记”是一种较为轻量的过渡性措施：出口方须在出口前就相关技术进行登记备案，使监管部门在正式修订仍处征求意见阶段时即可掌握技术出口需求情况。公告中列入的生物医药类别之一“小核酸药”，是指 siRNA、反义寡核苷酸等靶向 RNA 的疗法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mofcom.gov.cn:8443/xwfb/xwfyrth/art/2026/art_d7661dbf62794345a221404f82a25959.html">商务部新闻发言人就修订《中国禁止出口限制出口技术目录》答记者问</a></li>
<li><a href="https://www.news.cn/fortune/20261016/a36da321bae240ce896803485f9a52cb/c.html">两部门就修订中国禁止出口限制出口技术目录公开征求意见-新华网</a></li>
<li><a href="https://news.cctv.com/2026/10/16/ARTIvDJFbJhCwbMmCTdWztKG261016.shtml">商务部新闻发言人就修订《中国禁止出口限制出口技术目录》答记者问_新...</a></li>

</ul>
</details>

**标签**: `#export-controls`, `#ai-policy`, `#china-regulation`, `#biotech`, `#solar-technology`

---

<a id="item-10"></a>
## [特斯拉发布搭载 SpaceX 冷气推进器的新款 Roadster](https://www.tesla.com/roadster) ⭐️ 6.0/10

特斯拉在得克萨斯州韦科附近发布了重新设计的量产版 Roadster，并演示了包括让车辆倒挂行驶、以及用源自 SpaceX 的冷气推进器将另一辆车弹射升空等一系列特技。据称最高配的“Thrust”版本需要 25 万美元定金（基础版定金从 5 万美元起），宣称 0-60 英里加速时间低于 0.8 秒，并计划于 2028 年投产。 这场演示把汽车硬件的指标推进到了通常只属于航天器的领域，模糊了消费级电动车与航空航天工程之间的界限。同时它也再次点燃了业界长期存在的争论：戏剧化的概念演示究竟能否转化为可交付的产品，尤其是在特斯拉一贯延迟交付记录的背景下。 该推进系统使用 10000 psi 的复合材料缠绕压力容器（COPV），这与火箭上使用的高压储罐属于同一类别，为不进行燃烧的冷气推进器供气以产生推力。批评者指出，冷气系统本身推力和效率都很低，而且据称重新充装压缩气体需要数小时，充一次可能只够使用一次。

hackernews · shekhar101 · 10月16日 01:32 · [社区讨论](https://news.ycombinator.com/item?id=50112657)

**背景**: 冷气推进器是一种火箭发动机，它通过让加压的（通常为惰性）气体经喷嘴膨胀来产生推力，全程不涉及燃烧；它被称为最简单、最可靠的火箭推进形式，常用于小型卫星和 CubeSat 的姿态控制。特斯拉早在 2017 年 11 月就开始接受 Roadster 预订，因此这次提出的 2028 年投产目标，是在该车型多年未能交付之后给出的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.engadget.com/2288437/teslas-redesigned-roadster-cold-gas-thruster-option-reservation/">Tesla's redesigned Roadster has a cold-gas thruster option ...</a></li>
<li><a href="https://www.motortrend.com/news/tesla-roadster-thrust-system-spacex-technology-explained">How Did the Tesla Roadster Fly? Here's How It Works - MotorTrend Tesla's Flying Roadster: What Was Shown, How Cold-Gas ... Tesla Roadster Gets Redesigned With Cold-Gas Thrusters and a ... Tesla Reveals How New Roadster Can Fly Using SpaceX Rocket ... Tesla Roadster Flies With Cold-Gas Thrusters, Targets 2028 ... Tesla Unveils Production Roadster With SpaceX Cold-Gas Thrusters</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cold_gas_thruster">Cold gas thruster</a></li>

</ul>
</details>

**社区讨论**: 评论区观点严重分化：一些评论者称这是他们见过最酷的演示之一，并盛赞其背后的工程能力；另一些人则斥之为“画大饼”，指这款车自 2017 年起就开始接受预订却始终没有交付。质疑者集中在冷气推进器的实用性上（充电需数小时、充一次大约只能用一次），并怀疑让一辆 1000 多公斤的汽车悬停、乃至整个方案是否有可能合法上路。

**标签**: `#tesla`, `#electric-vehicles`, `#hardware-engineering`, `#product-demo`, `#hacker-news-discussion`

---

<a id="item-11"></a>
## [博文《我爱软件渲染》引发 Hacker News 激辩](https://www.jamesfmackenzie.com/2026/10/13/i-love-software-rendering/) ⭐️ 6.0/10

jamesfmackenzie.com 上的一篇题为《我爱软件渲染》的博文主张 CPU 渲染具有独特美感，并在 Hacker News 上引发了 179 条评论的讨论。有评论者反驳称，作者所推崇的那种观感——像素化纹理与锐利边缘——其实只是关闭了空间抗锯齿和双线性过滤的结果，并不能证明是真正的软件渲染。 这场讨论提醒人们，玩家与软件渲染联系在一起的“复古观感”很大程度上只是特定的过滤与抗锯齿选择所带来的副产品，而现代 GPU 可以轻松复现——这一区分对模拟器、复古风格游戏开发以及游戏保存工作都具有意义。它也说明，一篇小众的图形美学随笔可以引出通用 CPU 与专用 GPU 着色器硬件之间更广泛的工程权衡。 评论者指出，软件渲染器所用的阴影与纹理查找表（LUT）完全可以作为常量传入 GPU 着色器，从而削弱了“此类效果必须依赖 CPU 渲染”的说法；而作者描述的观感只要在现代游戏中关闭抗锯齿即可获得。还有评论提到，可编程着色器管线直到 2001 年 NVIDIA GeForce 3 才出现，因此在早期，软件渲染器有时能实现当时固定功能 GPU 管线做不到的特效。

hackernews · speckx · 10月16日 12:52 · [社区讨论](https://news.ycombinator.com/item?id=50117746)

**背景**: 软件渲染指完全依靠 CPU 用通用代码生成最终图像，不依赖显卡的专用硬件；在 3D 加速卡普及之前它是主流做法，但由于 CPU 并非专为图形工作设计，速度较慢。相对地，抗锯齿是一种减少高分辨率场景降采样时出现锯齿伪影的技术，而双线性过滤则通过混合相邻纹素来平滑纹理。DOOM 是软件渲染游戏的经典代表：id Software 于 1997 年公开了引擎源码，此后数百个粉丝制作的“源码移植版”（source port）如 Woof 和 Crispy Doom 在扩展功能的同时，仍由 CPU 完成核心渲染运算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Software_rendering">Software rendering</a></li>
<li><a href="https://en.wikipedia.org/wiki/Spatial_anti-aliasing">Spatial anti-aliasing</a></li>
<li><a href="https://en.wikipedia.org/wiki/Doom_source_ports">Doom source ports</a></li>

</ul>
</details>

**社区讨论**: 整体情绪偏向温和的纠正：多位评论者认为这篇文章讲的其实是像素化纹理和关闭抗锯齿，而非软件渲染，有人甚至建议把标题改成《我爱像素化纹理》。也有人保持怀旧基调，回忆起当年的性能趣事（“加一块声卡让我涨了 10 帧”），并称赞 Woof 是一个优秀的、基于 SDL3 的软件渲染 DOOM 源码移植版。

**标签**: `#graphics`, `#software-rendering`, `#retro-computing`, `#game-development`, `#doom`

---

<a id="item-12"></a>
## [快手可灵 Kling 4.0 全量上线，接入 MCP/CLI 并将开放 API](https://mp.weixin.qq.com/s/Dn2jAxV0m6kpt7y4edRvdg) ⭐️ 6.0/10

10 月 15 日，快手旗下的可灵 Kling 4.0 正式在 klingai.com 全量上线，创作页面同步全面升级，提供更灵活、自由的创作体验。官方表示后续还将推出 4K、1080p 的 10-bit HDR 格式输出，Kling 4.0 能力已接入 MCP/CLI，面向企业与开发者的 API 服务也将于近期开放。 可灵是当前领先的 AI 视频生成平台之一，此次 4.0 全量上线并接入 MCP/CLI，意味着 AI 视频生成正从面向消费者的网页工具，演进为可被智能体、IDE 和开发者流水线直接调用的可编程基础设施。即将开放的企业级 API 之所以重要，是因为它为商业化与自动化视频生产打开了通道，也将进一步加剧其与 OpenAI Sora、Runway 及其他国产视频模型之间的竞争。 该公告篇幅简短且偏宣传性质，并未披露任何基准测试成绩、模型架构细节或定价信息。4K 与 1080p 的 10-bit HDR 输出被描述为“后续推出”而非上线即具备，面向企业与开发者的 API 同样标注为“近期开放”，因此具体的商业条款与调用限制仍不得而知。

telegram · zaihuapd · 10月16日 04:30

**背景**: 可灵是快手推出的生成式 AI 视频模型，可根据文本或图片提示生成短视频片段，与 OpenAI 的 Sora、Runway 等工具同台竞争。MCP（Model Context Protocol，模型上下文协议）是 Anthropic 提出的开放标准，用于将 AI 应用与外部数据源和工具连接起来；因此接入 MCP/CLI 意味着 AI 智能体或命令行脚本可以直接调用可灵生成视频，而无需手动操作网页界面。10-bit HDR 格式指每个色彩通道携带 10 位数据（而非常见的 8 位），可在支持 HDR 的屏幕上呈现更平滑的渐变、更丰富的色彩和更明亮的高光。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://modelcontextprotocol.io/">What is the Model Context Protocol ( MCP )? - Model Context Protocol</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>
<li><a href="https://blinqdroid.com/guides/flat-hdr-video-android/">Flat, Log & HLG Video on Android: Shoot for Grading</a></li>

</ul>
</details>

**标签**: `#ai-video-generation`, `#kling`, `#generative-ai`, `#product-launch`, `#developer-tools`

---

<a id="item-13"></a>
## [未经证实的消息称 OpenAI 将 GPT-Live-1 全双工语音模型上线 API](https://t.me/zaihuapd/44453) ⭐️ 6.0/10

一个 Telegram 聚合频道发帖称，OpenAI 已于 2026 年 9 月 10 日在其 API 上线名为 GPT-Live-1 的语音模型，并将其描述为可同时听与说的全双工模型，支持自然打断、背景噪声处理、长对话以及电话语音代理场景。该帖还声称 GPT-Live-1 在 Full Duplex Bench 上比 GPT-Realtime-2.1 提升 30 个百分点，API 语音前端价格为每分钟 0.05 美元。 如果消息得到证实，一款在全双工能力上大幅领先、且每分钟仅 0.05 美元的语音模型将显著推动语音代理的发展，让可自由打断的电话式自然对话在客服、呼叫中心和实时助手中变得更便宜、更可行。但该说法目前仅来自一个未经核实的 Telegram 频道，没有官方公告、评测或其他来源佐证，因此应当视为传闻而非已确认的发布。 该帖称该模型将复杂推理与工具调用交给后端模型处理，而语音前端只负责实时音频，这种前后端分离的架构与近期关于全双工语音系统工具调用的研究方向一致。但仍有两点存疑：所给日期（2026 年 9 月 10 日）令人怀疑或至少无法核实；声称在 Full Duplex Bench 上比 GPT-Realtime-2.1 高出 30 个百分点也异常之大，需要官方基准测试结果来确认。

telegram · zaihuapd · 10月16日 04:50

**背景**: 全双工语音模型的设计目标是同时听与说，不同于传统轮次式语音管线必须等待用户说完才能回应，因此能够实现自然打断、附和应答（如“嗯嗯”）以及更顺畅的轮流发言。Full-Duplex-Bench 是一个公开基准，用于评估这些交互行为，包括停顿处理、附和、轮流发言，以及较新的多步工具调用能力。GPT-Realtime-2.1 是 OpenAI 现有的语音到语音 API 模型，相较前代在字母数字识别、静音与噪声处理以及打断行为上有所改进。这类模型的一个常见难题是：若在音频回路内处理工具调用或重型推理，会削弱对话连贯性，因此业界常提出前后端分离的架构方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.openai.com/api/docs/models/gpt-realtime-2.1">GPT - Realtime - 2 . 1 Model | OpenAI API</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Voice AI`, `#Full-Duplex Speech`, `#API Release`, `#Rumor/Unverified`

---

<a id="item-14"></a>
## [市场回调与利率上升冲击 AI 数据中心交易热潮](https://www.kitco.com/news/off-the-wire/2026-10-15/market-selloff-rising-rates-test-ai-data-centre-deal-boom) ⭐️ 6.0/10

过去一周内，AirTrunk 的 REIT 上市计划、英伟达支持的 Firmus 的 IPO，以及软银支持的 SB Energy 的上市安排均被撤回或暂停，投资者要求企业证明其能够消化更高的利率与算力成本。与此同时，Dealogic 数据显示，亚洲数据中心并购交易在 2026 年已达 213 亿美元，约为 2025 年全年 100 亿美元的两倍，而股权融资同比下降 4.6%。 这一回撤标志着 AI 基础设施投资正从“不惜代价追求增长”转向“看重质量”，可能在 AI 算力需求持续攀升之际拖慢新增产能的建设节奏。它也说明 AI 数据中心这一交易主题如今对利率等宏观环境同样敏感，而不再只取决于 GPU 供应和模型需求。 Firmus 建设液冷数据中心，自称“AI 工厂”，客户包括 OpenAI 和 Meta，并原计划与总部位于新加坡的 DayOne 在印尼巴淡岛建设一个 360MW、17 万块 GPU 的园区；其投资方包括英伟达和黑石。SB Energy 由软银集团和 OpenAI 支持，而 AirTrunk 是亚太地区最大的数据中心平台，已被黑石以 240 亿澳元（约 160 亿美元）收购。

telegram · zaihuapd · 10月16日 05:10

**背景**: AI 数据中心属于极度资本密集型的资产，开发商通常通过股权、债务以及日益常见的公开上市（如 IPO 或 REIT）来融资；REIT 即房地产投资信托，允许公众投资者持有可产生收益的物业。当利率上升时，借贷成本变高、未来现金流折现更重，这类上市也就更难定价和完成。AirTrunk 是成立于 2015 年的澳大利亚超大规模数据中心平台，而 Firmus Technologies、SB Energy 和 DayOne 都处于 AI 算力与实体基础设施的交汇点。Dealogic 是追踪并购与融资规模的投行及交易数据提供商，被媒体广泛引用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/ck9dzpw4ll8po">Firmus : Nvidia -backed data centre firm scraps IPO as AI valuation...</a></li>
<li><a href="https://techwireasia.com/2026/06/nvidia-firmus-batam-ai-data-centre/">Nvidia -backed Firmus plans 170,000-GPU Batam AI data centre</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#data centers`, `#venture financing`, `#interest rates`, `#market trends`

---

<a id="item-15"></a>
## [长宁 4.7 级地震首报 7.7 级，为 15 年来最大偏差](https://t.me/zaihuapd/44455) ⭐️ 6.0/10

8 月 24 日 8 时 26 分，四川宜宾长宁发生 4.7 级地震。成都高新减灾研究所预警网在震后第 5 秒首报震级为 7.7 级，随后依次修正为 6.4 级、3.7 级、4.1 级，并在震后第 17 秒收敛到 3.9 级。 这是该所预警网自 2011 年 9 月服务社会 15 年来偏差最大的一次，研究所已致歉并承诺尽快查明原因、改进技术。这说明面向公众的安全攸关类预警系统一旦首报严重失准，可能放大恐慌，同时也与国内“谁有权发布地震预警”的争议交织在一起。 地震预警震级是预警台网在震时自动选取少量台站、量取纵波（P 波）前几秒记录并凭经验快速估算的，因此预警时效性优先于准确性，必然不如正式速报震级精确——本次预警最终收敛到 3.9 级，而中国地震台网正式测定为 4.7 级。此次地震震源深度约 5 公里，震中位于北纬 28.33 度附近，这也影响了能多快触发足够多的台站来约束估算结果。

telegram · zaihuapd · 10月16日 05:23

**背景**: 地震预警并不是预测地震，而是利用破坏性较弱的纵波（P 波）先于破坏性强的横波（S 波）到达、以及电磁波远快于地震波传播的原理，在强震动到达前几秒向可能受影响的区域发出警报。由于系统必须在几秒内出报，它只能用少量近场台站和很短的 P 波记录窗口去估算震级，再随着数据增多不断修正，因此预警震级与最终正式震级出现偏差是常见的。成都高新减灾研究所运营着国内规模最大的此类预警网之一；此次事件后，四川省地震局还指其冒用“中国地震预警网”名义发布预警信息，该所曾发文否认后又删除相关声明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260824A0CFJJ00">震级预警误差大怎么回事？地震专家紧急提醒：收到预警后必须“闻警即动...</a></li>
<li><a href="https://m.163.com/dy/article/L3OFJREV0545FPOU.html">读懂地震预警：为何震级有偏差？|中国地震台网|纵波|震中|震感|震源|...</a></li>
<li><a href="https://m.ithome.com/html/993792.htm">IT早报 0825：2026...</a></li>

</ul>
</details>

**标签**: `#earthquake-early-warning`, `#system-reliability`, `#public-safety`, `#seismology`, `#failure-analysis`

---

<a id="item-16"></a>
## [传闻苹果折叠屏 iPhone Duo 一分钟售罄，盘前股价涨超 2%](https://api3.cls.cn/share/article/2507193?os=android&amp;sv=8.8.4&amp;app=cailianpress) ⭐️ 6.0/10

据财联社一则简短的市场快讯，苹果首款折叠屏手机（传闻命名为 iPhone Duo）正式开售后仅一分钟，全型号库存即告售罄，带动苹果美股盘前一度上涨超过 2%，开盘有望创下历史新高。该消息未提供售价、配置、正式发布日期确认或分区域销售数据。 若消息属实，这将是苹果首次进入长期被三星及多家中国安卓厂商主导的折叠屏手机市场，并可能为 iPhone 产品线开启新一轮换机周期。股价的即时反应也说明市场对苹果新硬件的预期已相当充分，因此这条尚未经证实的消息对据此交易的人而言本身即是风险。 该消息未披露任何技术细节，如屏幕尺寸、铰链设计、面板供应商、售价或产量，也未引用苹果官方新闻稿或零售页面来证实售罄。此外，盘前交易通过电子通信网络（ECN）撮合，成交量和流动性都较稀薄，因此盘前 2% 的涨幅可能夸大了正式交易时段的真实表现。

telegram · zaihuapd · 10月16日 12:45

**背景**: 折叠屏手机依靠柔性 OLED 面板与精密铰链，让单台设备展开后获得接近平板大小的屏幕；三星自 2019 年 Galaxy Z Fold 起带火了这一品类，而苹果多年来一直被传在研发自家折叠机型却始终未正式发售。美国盘前交易时段为东部时间凌晨 4:00 至上午 9:30，早于 9:30 开始的正式交易时段，且通过电子通信网络（ECN）而非主板交易所撮合，因此盘前价格波动往往剧烈且成交清淡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pre-market_trading">Pre-market trading</a></li>
<li><a href="https://www.cnn.com/markets/premarkets">Pre-market Stock Trading | CNN</a></li>

</ul>
</details>

**标签**: `#Apple`, `#iPhone Duo`, `#foldable smartphone`, `#market news`, `#consumer tech`

---

<a id="item-17"></a>
## [法院文件曝光：Telegram 向美国执法部门移交用户数据](https://www.404media.co/heres-what-telegram-giving-data-to-the-u-s-government-looks-like/) ⭐️ 6.0/10

新公开的法院文件显示，Telegram 在回应美国法院命令时，主动向美国执法部门提供了一名用户的手机号、用户 ID 和 IP 地址，同时在信函中声明不承认受美国司法管辖。截至今年 1 月，Telegram 已累计向美方提供了 2253 名用户的数据。 这一披露直接冲击了 Telegram 长期塑造的「隐私优先、抗拒政府」的公众形象，对关注隐私、加密与科技政策的群体意义重大，因为它表明企业可以一边在口头上否认司法管辖，一边在实务中配合数据调取请求。这也为其他平台树立了先例：所谓「不受管辖」的抗辩可能同样站不住脚。 该案涉及被控参与 2023 年 10 月 7 日袭击以色列事件的 Mahmoud Al-Muhtadi，Telegram 将其披露行为定性为「自愿」而非被迫。文中的 2253 名用户是截至 1 月的累计数字，意味着实际数据共享规模如今可能已经更大。

telegram · zaihuapd · 10月16日 14:57

**背景**: Telegram 是一款流行的跨平台即时通讯应用，其默认的云端聊天并非端到端加密（只有可选的「秘密聊天」才是），因此平台自身能够获取手机号、用户 ID、IP 地址等账户元数据。由于这些数据存储在服务器端，即便消息内容受保护，也可在法院命令下被交出。Telegram 创始人 Pavel Durov 于 2024 年 8 月在法国被捕，此后公司更新了隐私政策，表示可能应有效法律请求，向有关部门披露违规用户的 IP 地址和手机号。

**标签**: `#privacy`, `#telegram`, `#surveillance`, `#tech-policy`, `#encryption`

---