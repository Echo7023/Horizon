---
layout: default
title: "Horizon Summary: 2026-08-05 (ZH)"
date: 2026-08-05
lang: zh
---

> 从 38 条内容中筛选出 10 条重要资讯。

---

1. [生成多样化肤色的简单色彩空间](#item-1) ⭐️ 8.0/10
2. [DeepSeek V4 Flash 单卡 AMD MI300X 跑出 150+ tok/s](#item-2) ⭐️ 8.0/10
3. [Keyv 及相关 npm 包在活跃的 Shai-Hulud 供应链攻击中遭入侵](#item-3) ⭐️ 8.0/10
4. [Xbox 宕机致光盘游戏不可玩，DRM 争议再起](#item-4) ⭐️ 8.0/10
5. [AI 智能体 harness 工程：通往自我改进之路](#item-5) ⭐️ 8.0/10
6. [MiniMax-H3 全模态模型通过 MLX 移植可在苹果芯片上运行](#item-6) ⭐️ 8.0/10
7. [Kimi K3 发布新架构：压缩记忆与潜路由](#item-7) ⭐️ 8.0/10
8. [俄罗斯 9 月起强制苹果设备支持 RuStore 第三方商店](#item-8) ⭐️ 8.0/10
9. [华为提出“韬定律”：以时间缩微替代几何缩微](#item-9) ⭐️ 8.0/10
10. [谷歌为 Anthropic 搭建 2000 亿美元华尔街融资机器](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [生成多样化肤色的简单色彩空间](https://toneyalexander.github.io/inclusive-color-space/) ⭐️ 8.0/10

一位开发者发布了一种新的色彩空间和算法，用于生成多样化且可信的肤色。该项目包含交互式 JavaScript 演示、详细说明以及用 Python 实现的程序化生成代码。 这为数字艺术家和游戏开发者提供了一种快速、易用的方法来生成任意角色的真实肤色，减轻了创作流程中常见的痛点。它也顺应了行业向包容性色彩工具（如 Google 的 Monk Skin Tone 量表）迈进的更广泛趋势。 该色彩空间基于真实肤色数据构建，使用的是手工拟合的数学函数，而非 PCA 之类的数据驱动方法。作者公开讨论了方法论上的局限性和“未来工作”部分，并提供了该空间所用的公式。

hackernews · automatoney · 8月4日 15:16 · [社区讨论](https://news.ycombinator.com/item?id=49170165)

**背景**: 肤色是物理因素与感知因素（如光照）共同作用的复杂结果，因此无法用简单的 RGB 坐标准确表示。诸如 Oklab 这类感知均匀的色彩空间以匹配人类感知的方式排列颜色，常用于分析肤色数据。Google 的 Monk Skin Tone 量表等现有倡议聚焦 AI 公平性，而这个工具则面向数字艺术和游戏开发等创意工作流。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://toneyalexander.github.io/inclusive-color-space/">What Colors Are We? Constructing A Color Space For Skin Tones</a></li>
<li><a href="https://skintone.google/">Skin Tone Research @ Google</a></li>
<li><a href="https://buzzverified.com/diverse-skin-tones-algorithm/">Diverse Skin Tones Algorithm - buzzverified.com</a></li>

</ul>
</details>

**社区讨论**: 评论者大多持正面态度，称赞呈现方式以及『巧妙』的手工拟合函数方法。有人指出肤色在很大程度上取决于光照条件，因此蓝肤色在月光下也可能成立，并建议参考 Pantone 肤色等现有标准。另一位评论者发现真实的粉底色号在 Oklab 中形成月牙形状，与文章中的形状一致。

**标签**: `#color space`, `#skin tones`, `#procedural generation`, `#digital art`, `#color science`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 单卡 AMD MI300X 跑出 150+ tok/s](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

GitHub 上的一个项目展示了在单个 AMD MI300X GPU 上以完整权重运行 DeepSeek V4 Flash，速度超过每秒 150 tokens，但上下文窗口从原来的 1M 缩减至 256K。 这表明一个 284B 参数的 MoE 大模型可以在单块常见加速器上以高吞吐量运行，从而降低运行前沿大模型的硬件门槛。同时它也凸显了实际部署中上下文长度、量化与推理速度之间的取舍。 DeepSeek V4 Flash 是一个专家混合（MoE）模型，总参数 284B，激活参数 13B，原生支持 1M token 的上下文窗口。单卡 MI300X 方案保留完整权重，未做激进量化，但为了装进 GPU 的 192GB HBM，牺牲了 75% 的上下文窗口，降至 256K。

hackernews · zhoutong · 8月4日 10:00 · [社区讨论](https://news.ycombinator.com/item?id=49166386)

**背景**: DeepSeek V4 Flash 是 DeepSeek 推出的面向效率优化的专家混合（MoE）模型，总参数 284B，每个 token 激活 13B 参数，支持 1M token 上下文。AMD Instinct MI300X 是数据中心 GPU，拥有 192GB HBM3 显存，高于 NVIDIA H100 的 80GB，因此很适合在无需多卡分片的情况下运行大型语言模型。MoE 模型每个 token 只激活一部分参数，从而在保持高容量的同时降低算力成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash">DeepSeek V 4 Flash - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://moreh.io/technical-report/moreh-vllm-performance-evaluation-deepseek-v3-r1-671b-on-amd-instinct-mi300x-gpus-250829/">Moreh vLLM Performance Evaluation: DeepSeek V3/R1 671B on AMD ...</a></li>

</ul>
</details>

**社区讨论**: 有评论者指出 MI300X 不是单卡零售，而是以 8 卡整机形式销售，价格约 25 万欧元，并建议改用即将推出的 MI350P（144GB 显存的 PCIe 卡）来降低门槛。也有人将这项工作与此前的 DwarfStar 方案比较，讨论 MXFP4 量化版本是否能装进更小显存；还有用户认为 256K 上下文是实用的取舍，认为其与 Codex 使用的范围相当。

**标签**: `#deepseek`, `#AMD MI300X`, `#inference optimization`, `#MoE`, `#LLM deployment`

---

<a id="item-3"></a>
## [Keyv 及相关 npm 包在活跃的 Shai-Hulud 供应链攻击中遭入侵](https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack) ⭐️ 8.0/10

npm 包 Keyv 及相关“friends”包在活跃的 Shai-Hulud 供应链攻击中遭到入侵。这种自我复制型蠕虫正在通过 npm 生态和 GitHub 仓库传播，使下游用户面临风险。 Keyv 是一个广泛使用的键值存储库，因此它的失陷可能影响大量依赖它的 JavaScript 项目。该事件暴露了 npm 依赖生态中的系统性风险，也凸显了加强供应链防御的必要性。 Shai-Hulud 蠕虫目前仍在活跃，并通过被入侵的 npm 包和 GitHub 仓库传播，据称 Shai-Hulud 2.0 已在超过 25,000 个仓库中暴露了密钥。建议开发者禁用安装脚本、对新增预安装钩子的包保持警惕，并采取隔离开发环境的做法。

hackernews · cimi_ · 8月4日 11:01 · [社区讨论](https://news.ycombinator.com/item?id=49166874)

**背景**: Keyv 是一个简单的键值存储 npm 包，支持多种存储后端，常用于 Node.js 项目。Shai-Hulud 攻击是一种供应链攻击，通过安装钩子等方式向广泛使用的包中注入恶意代码，导致任何执行 npm install 的人都可能被入侵。由于 npm 生态高度依赖传递依赖，单个流行包被攻破就可能对大量下游应用造成连锁影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/security/blog/2025/12/09/shai-hulud-2-0-guidance-for-detecting-investigating-and-defending-against-the-supply-chain-attack/">Shai-Hulud 2.0: Guidance for detecting, investigating, and ...</a></li>
<li><a href="https://unit42.paloaltonetworks.com/npm-supply-chain-attack/">" Shai-Hulud " Worm Compromises npm Ecosystem in Supply Chain ...</a></li>
<li><a href="https://www.wiz.io/blog/shai-hulud-2-0-ongoing-supply-chain-attack">Shai-Hulud 2.0 Supply Chain Attack : 25K+ Repos Exposing Secrets</a></li>

</ul>
</details>

**社区讨论**: 社区评论者对脆弱的 npm 依赖系统表示不满，称这类供应链攻击很难清理，且往往带来连锁性入侵。有人呼吁取消或限制 pre-install / post-install 钩子，也有人提出实际缓解措施，比如设置包的最低发布年龄，以及使用隔离的开发环境。

**标签**: `#security`, `#supply-chain`, `#npm`, `#open-source`, `#malware`

---

<a id="item-4"></a>
## [Xbox 宕机致光盘游戏不可玩，DRM 争议再起](https://birchtree.me/blog/xbox-goes-down-you-cant-play-games-you-own-on-disc/) ⭐️ 8.0/10

最近一次 Xbox 服务中断导致即使实体光盘游戏也无法启动，因为主机在启动游戏时需要进行服务器验证。这一事件暴露出看似物理副本的游戏实际上仍然依赖在线服务器。 这一事件意义重大，因为它动摇了“拥有实体光盘就能确保玩到游戏”的普遍认知。它进一步引发了关于数字所有权、DRM 以及消费者是否真正拥有所购游戏的讨论。 几乎所有现代 Xbox 主机即使是使用光盘的实体游戏，也需要联网并通过服务器验证才能运行，这实际上使每款游戏都变成了强制在线产品。这导致了一个单点故障：当服务器中断时，即使是原本可玩的光盘游戏也变得无法访问。

hackernews · surprisetalk · 8月4日 12:01 · [社区讨论](https://news.ycombinator.com/item?id=49167448)

**背景**: 强制在线 DRM 是一种数字版权管理方式，要求用户持续联网并通过服务器验证才能使用产品。该技术旨在防止盗版，但因服务器故障时会给正版用户带来不便而备受批评，同时它也削弱了所有权的概念——消费者购买的往往只是许可证，而非游戏本身。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Always-online_DRM">Always-online DRM</a></li>
<li><a href="https://www.pcgamingwiki.com/wiki/List_of_games_using_Always_Online_DRM">List of games using Always Online DRM - PCGamingWiki</a></li>

</ul>
</details>

**社区讨论**: HN 评论者普遍对游戏行业向依赖服务器的所有权模式转变持批评态度。有用户指出 PS3 等旧主机仍由玩家主机托管多人游戏，而另一用户则强调真正的问题在于所有权，而非实体版与数字版之分：买家应当能够保留、转售和归档自己所购买的内容。

**标签**: `#digital ownership`, `#DRM`, `#gaming`, `#Xbox`, `#cloud services`

---

<a id="item-5"></a>
## [AI 智能体 harness 工程：通往自我改进之路](https://lilianweng.github.io/posts/2026-07-04-harness/) ⭐️ 8.0/10

Lilian Weng 发表了一篇技术深度文章，提出围绕 AI 智能体的“harness”（提示词、工具、上下文与评估等外部层）是提升性能、质量和成本效率的关键杠杆。文章认为，除了升级模型权重，工程化这一外圈层是智能体自我改进的新前沿。 在模型训练改进放缓的背景下，工程化 harness 为现有 LLM 智能体挖掘更多能力提供了切实可行的路径。对于构建智能体系统的开发者和团队而言，这点很重要，因为对 harness 的微小调整可能带来可靠性和成本上的显著收益。 讨论中提到了优化 AGENTS.md、技能和工具等具体实践，以及为代码库建立通用、可靠、精确的适应度函数（fitness function）的需求。一些评论者已经在生产系统中应用爬山式（hillclimbing）实验来改进自己的 harness。

hackernews · tosh · 8月4日 06:17 · [社区讨论](https://news.ycombinator.com/item?id=49164896)

**背景**: LLM 智能体通常将语言模型与外部脚手架相结合，包括系统提示词、工具定义、上下文管理和反馈循环。这层脚手架常被称为“harness”，它决定了模型如何理解任务以及可以采取哪些行动。自我改进型智能体旨在通过“规划—执行—评估”的循环随时间变得更好。Harness 工程把这一外部层视作可供优化的设计面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.andela.com/publication/inside-the-architecture-of-self-improving-llm-agents">Inside the architecture of self - improving LLM agents</a></li>
<li><a href="https://www.linkedin.com/pulse/what-happens-when-llm-agents-evolve-themselves-andela-ysehe">How to Build Self - Improving AI Agents That Think in Loops</a></li>
<li><a href="https://github.com/wronai/ellma">GitHub - wronai/ellma: Evolutionary Local LLM Agent - Self - improving ...</a></li>

</ul>
</details>

**社区讨论**: 评论者总体持积极务实态度，分享的是实际实验和工具而非空谈理论。有一位用户强调，定义“质量”并构建通用的适应度函数是第一步；另一位则认为，下一个大范式是训练提示词和代码，而不是继续训练模型权重。还有人分享了自己构建 harness 的项目，并称这篇博客帮助改进了他们的 harness 工程技能。

**标签**: `#AI`, `#LLM agents`, `#harness engineering`, `#software engineering`, `#self-improvement`

---

<a id="item-6"></a>
## [MiniMax-H3 全模态模型通过 MLX 移植可在苹果芯片上运行](https://simonwillison.net/2026/Aug/4/minimax-h3-mlx/#atom-everything) ⭐️ 8.0/10

MiniMax 发布了 MiniMax-H3，这是一个通用全模态生成系统；社区移植项目 PipeNetwork/minimax-h3-mlx 使其可以在 Apple Silicon 上运行。Simon Willison 在 M5 Max MacBook Pro 上使用该移植成功生成了带音频的 15 秒视频片段。 这使 Apple 用户无需依赖云端即可使用最先进的全模态模型，降低了本地 AI 视频生成的门槛。同时也展示了 MLX 生态系统的成长，它正成为在消费级硬件上运行大型生成模型的实用框架。 该模型需要下载约 115 GB 的模型文件，生成视频耗时不到 45 分钟。示例输出中的音频是“类似语音的奇怪噪音”，因为未对音轨提供提示词指导；官方提示词指南解释了如何改进结果。

rss · Simon Willison · 8月4日 19:10

**背景**: MiniMax-H3 是一种全模态生成模型，可接受文本、图像、音频和视频作为输入，并能生成最长 15 秒、带音频的视频片段。MLX 是 Apple 为 Apple Silicon 上的机器学习开发的开源数组框架，提供类似 NumPy 的 API。该移植将 MiniMax-H3 适配到 MLX，使其可以在搭载 Apple Silicon 的 Mac 上本地运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/MiniMaxAI/MiniMax-H3">MiniMaxAI/MiniMax-H3 · Hugging Face</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks and Modalities - MiniMax Research | MiniMax</a></li>
<li><a href="https://opensource.apple.com/projects/mlx/">MLX</a></li>

</ul>
</details>

**标签**: `#omni-modal`, `#MLX`, `#video generation`, `#MiniMax-H3`, `#Apple Silicon`

---

<a id="item-7"></a>
## [Kimi K3 发布新架构：压缩记忆与潜路由](https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the) ⭐️ 8.0/10

SemiAnalysis 发表了对 Kimi K3 的技术深度分析，介绍了一种结合压缩记忆、深度方向注意力、潜在专家路由以及推理性能优化的 LLM 架构。该文将 K3 描述为前沿大模型领域中的一个独特设计。 Kimi K3 的架构创新有望提升推理效率和长上下文处理能力，这是大模型部署的关键瓶颈。如果该设计被证明有效，可能会影响其他研究机构在下一代 LLM 中优化记忆、路由和注意力机制的方式。 该架构据称使用压缩记忆来降低 KV 缓存开销，通过深度方向注意力增强层间信息流动，并利用潜在专家路由动态选择计算路径。SemiAnalysis 重点关注推理性能的影响，而非基准分数。

rss · Semianalysis · 8月3日 19:42

**背景**: 压缩记忆技术通过缩小 KV 缓存或模型权重的内存占用，降低推理成本。深度方向注意力将标准 Transformer 的注意力机制扩展到层与层之间，而潜在专家路由则利用学到的潜在表示将输入路由到专门的专家模块。这些概念建立在已有的 Transformer 和混合专家（MoE）研究之上，但以新颖的方式组合应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2502.15443">[2502.15443] When Compression Meets Model Compression: Memory-Efficient Double Compression for Large Language Models</a></li>
<li><a href="https://d2l.ai/chapter_attention-mechanisms-and-transformers/transformer.html">11.7. The Transformer Architecture — Dive into Deep Learning 1.0.3 documentation</a></li>
<li><a href="https://github.com/MilkThink-Lab/Awesome-Routing-LLMs">GitHub - MilkThink-Lab/Awesome-Routing-LLMs: A curated list of awesome works in Routing LLMs paradigm (👉 Welcome to submit your contributions to this code repository)</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#architecture`, `#inference`, `#memory`

---

<a id="item-8"></a>
## [俄罗斯 9 月起强制苹果设备支持 RuStore 第三方商店](https://t.me/zaihuapd/42963) ⭐️ 8.0/10

俄罗斯国家杜马于 2025 年 6 月 26 日通过三读法案，要求苹果公司自 2025 年 9 月 1 日起允许用户在其 iPhone 和 iPad 上安装俄罗斯第三方应用商店 RuStore。该法律禁止苹果和谷歌设置安装限制、封锁替代功能、强制开发者定价或限制支付方式。 此举打破了苹果 App Store 在俄罗斯的垄断地位，迫使苹果向一个国家支持的第三方应用市场开放 iOS 生态系统。这也可能为其他国家监管应用商店的主导地位树立先例。 该法案适用于在俄罗斯销售或使用的苹果设备，涵盖第三方软件的安装与更新，并明确禁止厂商限制替代支付方式或强迫开发商定价。RuStore 此前主要面向 Android 和鸿蒙设备；新法案将把这一要求扩展到苹果的 iOS 生态系统。

telegram · zaihuapd · 8月4日 05:25

**背景**: RuStore 是由 VK 公司于 2022 年 5 月推出、并得到俄罗斯数字发展部支持的政府背景应用商店。它是在西方制裁导致许多外国平台限制对俄服务后诞生的，俄罗斯当局也日益要求在俄销售的设备上预装本地应用。新法律将这些要求从 Android 扩展到苹果 iOS，直接挑战了 App Store 对应用分发的独家控制权。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://meduza.io/en/feature/2025/06/27/an-app-store-ultimatum">An App Store ultimatum New legislation will require Apple to open iPhones and iPads to Russia’s state-backed marketplace — Meduza</a></li>
<li><a href="https://iphonewired.com/news/984725/">Effective in September: New Russian regulations require iPhone/iPad and other Apple devices to support the installation of third-party app stores RuStore - iPhone Wired</a></li>
<li><a href="https://asoworld.com/en/aso-glossary/rustore/">RuStore -ASOWorld UK</a></li>

</ul>
</details>

**标签**: `#Regulation`, `#App Store`, `#Apple`, `#Russia`, `#RuStore`

---

<a id="item-9"></a>
## [华为提出“韬定律”：以时间缩微替代几何缩微](https://t.me/zaihuapd/42966) ⭐️ 8.0/10

在上海举行的 2026 年 IEEE 国际电路与系统研讨会上，华为发布了“韬定律”，这是一项以“时间缩微”替代“几何缩微”的新半导体演进原则。华为声称过去六年已据此设计并量产 381 款芯片，今年秋季将推出采用“逻辑折叠”技术的新麒麟手机芯片。 “韬定律”挑战了长期主导的摩尔定律范式，在几何缩微逼近物理极限之际提供了一条潜在的前进路径。如果得到验证，它可能重塑全球半导体竞争格局，为华为和中国提供一条绕开西方主导工艺技术的替代路线。 “韬定律”的核心是系统地降低电子系统每个层次的特征时间常数，从晶体管开关到系统级响应均涵盖在内。华为预计，到 2031 年基于该定律开发的高端芯片晶体管密度可达到 1.4 纳米制程同等水平，但华为尚未公布“逻辑折叠”的完整技术细节。

telegram · zaihuapd · 8月4日 08:04

**背景**: 摩尔定律传统上预测芯片上的晶体管数量大约每两年翻一番，其驱动力是缩小特征尺寸的几何缩微。然而，随着晶体管逼近原子尺度极限，这种缩微速度已经放缓，由互连电阻和电容引起的 RC 延迟成为主要瓶颈。“韬定律”提出了不同的优化目标：不是缩小物理尺寸，而是压缩信号传输的时间常数，通过在器件、电路、芯片和系统等多个层级进行时间维度的协同优化来获得性能提升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://xtechpioneer.com/huawei-proposes-new-semiconductor-law-tao-scaling-replaces-geometry-to-fold-time/">Huawei Proposes New Semiconductor Law : ‘ Tao Scaling ’ Replaces...</a></li>
<li><a href="https://chinarxiv.org/items/chinaxiv-202605.00224">A Time Scaling Theory for Multi-Layer Electronic Systems</a></li>
<li><a href="https://en.wikipedia.org/wiki/RC_time_constant">RC time constant - Wikipedia</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#Huawei`, `#Moore's law`, `#chip design`, `#technology`

---

<a id="item-10"></a>
## [谷歌为 Anthropic 搭建 2000 亿美元华尔街融资机器](https://www.ft.com/content/549f2e23-5aa2-49c7-9ea6-a9784ab7087c) ⭐️ 8.0/10

《金融时报》8 月 4 日发布的调查发现，谷歌已悄然搭建了史上规模最大的基础设施融资架构之一，总额约 2000 亿美元，用于向 Anthropic 交付 AI 芯片。今年 6 月，名为 Compute SPV 的特殊目的载体完成首批交易，购入约 350 亿美元硬件。 这是 AI 基础设施融资领域的里程碑：它让没有信用评级的 Anthropic 能够获得大规模算力，同时让 2000 亿美元的硬件不进入相关公司的资产负债表。这可能成为 AI 公司为算力融资的模板，并影响整个行业的厂商融资实践。 由于 Anthropic 没有信用评级，风险由多方分担：谷歌为数据中心背书，博通购买并协助融资芯片，阿波罗和黑石则购买硬件并回租给 Anthropic。Compute SPV 今年 6 月的首批交易涵盖约 1 吉瓦算力和 100 万颗 TPU。

telegram · zaihuapd · 8月4日 10:52

**背景**: 特殊目的载体（SPV）是为持有资产、管理风险或为特定项目融资而设立的独立法律实体，可将财务风险与母公司隔离。这笔交易类似于厂商融资模式，该模式由波音、通用电气等制造商推广，用于帮助客户购买飞机、发动机等昂贵设备。在该案例中，谷歌、博通和投资者利用 SPV 为大规模 AI 硬件采购提供资金，而无需任何一方将全部负担记入自己的资产负债表。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Special-purpose_entity">Special-purpose entity - Wikipedia</a></li>
<li><a href="https://www.investopedia.com/terms/s/spv.asp">Special Purpose Vehicle (SPV): Definition and Reasons Companies Use Them</a></li>
<li><a href="https://www.cscglobal.com/service/entity-solutions/spv-management/guide-to-special-purpose-vehicles-spvs/">Special Purpose Vehicles (SPVs) Guide | CSC</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google`, `#Anthropic`, `#Finance`, `#Infrastructure`

---