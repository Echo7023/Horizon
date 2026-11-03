---
layout: default
title: "Horizon Summary: 2026-11-04 (ZH)"
date: 2026-11-04
lang: zh
---

> 从 36 条内容中筛选出 17 条重要资讯。

---

1. [Qwen 3.8 27B 在笔记本上复现权重空间编程](#item-1) ⭐️ 8.0/10
2. [Postman 被指静默自动安装 AI 插件并上传 API 请求数据](#item-2) ⭐️ 8.0/10
3. [「Mac at Any Scale」：把 Mac 机群当作数据中心基础设施来运营](#item-3) ⭐️ 8.0/10
4. [谷歌将校园搜索访问权与强制采用 AI 绑定](#item-4) ⭐️ 8.0/10
5. [利用飞机多普勒音频可精确定位视频拍摄地点](#item-5) ⭐️ 8.0/10
6. [DeepSeek 开源内部大规模推理框架 DeepInfer](#item-6) ⭐️ 8.0/10
7. [Stringman：售价 800 美元的开源房间级缆索驱动机器人](#item-7) ⭐️ 7.0/10
8. [批评者称“Astra 读写权重提升 Qwen”的说法具有误导性](#item-8) ⭐️ 7.0/10
9. [现代国际象棋引擎跑在 1996 年的奔腾上，能击败卡斯帕罗夫吗？](#item-9) ⭐️ 7.0/10
10. [犹他州对 Kalshi 及其联合创始人提起赌博重罪指控](#item-10) ⭐️ 7.0/10
11. [SemiAnalysis：SpaceX 或成全球最大 AI 云](#item-11) ⭐️ 7.0/10
12. [Protegrity 发布 278M 开放权重 RoBERTa 个人信息检测模型及 PII-SCOPE 基准](#item-12) ⭐️ 7.0/10
13. [OpenAI 指控《纽约时报》索要 2000 万条 ChatGPT 对话侵犯用户隐私](#item-13) ⭐️ 7.0/10
14. [字节跳动火山引擎发布 Seedance 2.5 4K 视频模型，主打大荧幕质感](#item-14) ⭐️ 7.0/10
15. [普京要求俄私营数据中心预留 10%算力供政府征用](#item-15) ⭐️ 7.0/10
16. [传英伟达要求全球数据中心将中国企业业务占比限制在 49%以内](#item-16) ⭐️ 7.0/10
17. [Atlas 将 10.9 万篇机器学习会议论文整理成 1260 个主题页面](#item-17) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Qwen 3.8 27B 在笔记本上复现权重空间编程](https://simonwillison.net/2026/Nov/3/qwen-can-interpret-model-weights/) ⭐️ 8.0/10

Simon Willison 报告称，在他笔记本上本地运行的 Qwen 3.8 27B 能够解读原始神经网络权重，并复现了 Rikiya Takehi 等人《Sparks of Weight-Space Programming》中的一个示例。该论文声称，GPT-6 Astra 等前沿模型仅凭浮点权重、无需工具或代码执行，就能判断一个网络被训练来做什么。 如果一款可在本地运行的开源权重 27B 模型就能读取模型权重，那么权重空间可解释性与编辑就不再是前沿实验室的专属能力，个人研究者和开发者也能参与。这可能催生新的调试、模型手术和教学流程，同时也让严格的正确性验证变得更加重要。 这项研究自称为博客文章而非经过同行评审的论文，批评者 Matthew Honnibal 和 Sean Goedecke 认为它把无工具读取权重与借助代码的优化混为一谈。Willison 则聚焦更困难的无工具“识别游戏”任务：仅凭权重判断小型策略网络是在 10x10 版本的 Breakout、Pong、Pac-Man 还是 Freeway 上训练的。

rss · Simon Willison · 11月3日 16:29 · [社区讨论](https://news.ycombinator.com/item?id=50355251)

**背景**: 神经网络权重是训练过程中学到的浮点参数；对大模型而言，这些参数多达数十亿，通常被视为不透明的二进制产物，而不是模型可以直接推理的文本。权重空间编程指的是让大语言模型直接检查和编辑这些原始参数的能力，与探针、引导向量或 LoRA 适配器等既有技术形成对比。Qwen 3.8 27B 是阿里巴巴 Qwen 团队发布的开源权重、可在本地运行的多模态模型，而 GPT-6 Astra 是 OpenAI 于 2026 年 9 月发布的前沿模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Nov/3/qwen-can-interpret-model-weights/">Qwen 3.8 27B on my laptop can interpret model weights , too</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen/Qwen3.8-27B · Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra</a></li>

</ul>
</details>

**社区讨论**: 评论者既感兴趣又持怀疑态度：有人引用 Glendower/Hotspur 的台词追问模型对权重的解读是否真的正确，另有人问 Qwen 3.8 能否编辑自己这一代模型的权重，以及这与引导向量、LoRA 和已知的神经元级干预有何关系。也有人称赞 Qwen 3.8 27B 是强大的本地模型，调侃可以设立“自行车上的鹈鹕”权重编辑基准，并对现有模型已能在一定程度上把权重操纵当作编程任务感到惊讶。

**标签**: `#LLMs`, `#interpretability`, `#model-weights`, `#local-models`, `#research`

---

<a id="item-2"></a>
## [Postman 被指静默自动安装 AI 插件并上传 API 请求数据](https://github.com/postmanlabs/postman-app-support/issues/14370) ⭐️ 8.0/10

一份 GitHub issue（postman-app-support #14370）指控 Postman 桌面客户端在未明确征得用户同意的情况下静默自动安装 AI 智能体插件，包括 Codex/Claude 集成和 Postman MCP 技能；同时有评论者指出，Postman 会记录每一次 API 请求的详细信息，包括 {{some_secret}} 这类模板变量展开后的真实值。 Postman 是使用最广泛的 API 开发工具之一，把展开后的密钥发送到厂商服务器、并且在屏蔽该端点时让应用无法正常工作，会给处理医疗、金融等受监管数据的团队带来严重的合规与安全风险。 根据该 issue 和评论者的说法，屏蔽发往日志端点的出站流量会导致整个应用无法正常工作，而不只是遥测功能降级；一位调查 HIPAA 合规性的评论者据此认为 Postman 不合规。上述内容均为社区陈述，在所提供的材料中尚未看到 Postman 的确认回应。

hackernews · sidgarimella · 11月3日 17:22 · [社区讨论](https://news.ycombinator.com/item?id=50354960)

**背景**: Postman 是一款历史悠久的图形化工具，用于构建、发送和测试 HTTP API 请求，团队通常会在其中保存环境变量以及 API key、token 等模板化取值。近年来 Postman 陆续加入了云端同步、账号体系、AI 功能以及面向编码智能体的插件生态，这意味着请求数据可能离开本地机器。其官方文档也介绍了 Postman Vault 和 Secret Scanner 等功能，初衷正是避免凭据以明文形式存储或被共享到集合中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/postmanlabs/postman-app-support/issues/14370">[SEVERE] Desktop auto - installs Codex/Claude plugins ; installer...</a></li>
<li><a href="https://learning.postman.com/docs/getting-started/basics/about-ai">About Postman AI features | Postman Docs</a></li>
<li><a href="https://learning.postman.com/v11/docs/reports/secret-scanner-reports">View reports about detected, unresolved, and resolved secrets</a></li>

</ul>
</details>

**社区讨论**: 这场约 297 条评论的讨论整体偏负面：开发者称 Postman 变得又慢又臃肿，提到某医疗行业雇主的安全团队已将其取消认证，并称一夜之间迁移到了可将请求定义存入 git 的 Bruno；也有人感叹这款曾经小巧的开发者工具融资超过 4 亿美元后，如今靠强制登录、订阅和 AI 功能来支撑其估值。

**标签**: `#privacy`, `#security`, `#postman`, `#developer-tools`, `#api-testing`

---

<a id="item-3"></a>
## [「Mac at Any Scale」：把 Mac 机群当作数据中心基础设施来运营](https://namespace.so/blog/mac-at-any-scale) ⭐️ 8.0/10

Namespace 发布了一篇题为《Mac at Any Scale》的工程实录，详细记录了把成批 Mac mini 与 Virtualization.Framework 虚拟机当作数据中心基础设施来运营究竟需要付出什么代价，并逐一列出了为绕开 Apple 平台与工具链限制而不得不采用的各种变通做法。该文在 Hacker News 上获得 285 分和 166 条评论，来自 CI 厂商和家庭实验室的实践者补充了大量一线经验。 任何需要发布 iOS 或 macOS 软件的团队最终都得用真正的 Apple 硬件，因此文中描述的运维痛点实际上是整个 Apple 开发者生态——从小型 CI 服务商到大型应用工作室——共同承担的一笔隐性成本。文章的观点是：如果 Apple 推出一款真正面向服务器的 Mac（类似当年 Xserve 的思路），即便溢价明显也一定有人买单，因为自己重建一整套数据中心运维能力的成本远高于硬件本身。 文章点出了若干具体障碍：代码签名与描述文件的复杂度、FileVault 在开机时弹出的密码输入成为阻止无人值守重启的硬性关卡、笔记本或 iOS 设备长期上架充电导致的电池鼓包风险，以及 Virtualization.Framework 作为 Apple Silicon 上运行 macOS 或 Linux 客户机唯一受支持途径所固有的限制。这些并非边角案例，而是每一台 Mac 上架前都必须逐一工程化绕开的常规阻塞点，否则整机柜的 Mac 无法像普通服务器那样运作。

hackernews · anner_ · 11月3日 14:53 · [社区讨论](https://news.ycombinator.com/item?id=50352758)

**背景**: Apple 的 macOS 授权条款要求为 iPhone、iPad、Mac 等 Apple 平台构建软件必须在真正的 Apple 硬件上运行，这正是 MacStadium 这类公司在数据中心机柜里塞进数万台 Mac、AWS 也推出 EC2 Mac 实例的原因。由于 macOS 本质上是按桌面操作系统设计的，它缺少 Linux 和 Windows 服务器习以为常的远程管理、无头启动和生命周期管理工具。Virtualization.Framework 是 Apple 随 Apple Silicon 一同推出的原生 API，利用宿主 CPU 的虚拟化扩展来运行 Linux 或 macOS 客户机，如今多数 CI 机群都用它而非 QEMU 来做虚拟化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://summithq.com/mac-mini-as-a-server/">Mac Mini as a Server: The Definitive Guide | Summit</a></li>
<li><a href="https://www.veloworkspaces.com/blog/virtualization-framework-vs-qemu/">Virtualization . framework vs. QEMU on Apple ... — Velo Workspaces</a></li>
<li><a href="https://aws.amazon.com/ec2/instance-types/mac/">Amazon EC2 Mac Instances - Amazon Web Services</a></li>

</ul>
</details>

**社区讨论**: 评论者大多用亲身经历印证了文章的说法：TestingBot 的一位工程师介绍了用 Virtualization.Framework 部署 Mac mini M6 实例做 macOS 自动化测试的经历，并提醒上架使用的 iOS 设备用几个月后电池会鼓包把屏幕顶起来；一位家庭服务器的运维者则直言 FileVault 的开机密码关卡对服务器来说简直是灾难。也有人对 Apple 的开发者工具更为不满，称 Xcode Cloud 和 Apple 的自动化能力「就是个笑话」，并把 Apple 自家研发进度受拖累归咎于同样晦涩的签名、plist、证书体系以及遗留的 Objective-C/C++ 代码；还有评论者畅想把 Mac mini 主板重新封装、配上液冷散热器，做成高密度刀片服务器。

**标签**: `#macOS`, `#infrastructure`, `#data-center`, `#Apple`, `#CI/CD`, `#virtualization`

---

<a id="item-4"></a>
## [谷歌将校园搜索访问权与强制采用 AI 绑定](https://www.nytimes.com/2026/11/03/us/google-search-schools-restrict-ai.html) ⭐️ 8.0/10

谷歌宣布推出新的管理员控制选项，允许使用 Google Workspace for Education 的学校限制或关闭其 AI 工具，但如果学校完全拒绝 AI，其域名下的谷歌搜索访问权限也会一并被取消。该政策详述于 2026 年 11 月 3 日发布的谷歌教育博客文章中，并由《纽约时报》、CNN 和 Ars Technica 报道，实际上让学校在 AI 功能与基础搜索之间做全有或全无的选择。 搜索是教学、研究和学校管理的核心基础设施，将其与接受生成式 AI 捆绑，使谷歌对可能出于教学、隐私或法律原因而希望退出 AI 的教育机构拥有了不寻常的支配力。此举很可能加剧监管机构和反垄断观察者对谷歌捆绑行为的审视，并为 AI 如何被推向全球课堂树立先例。 这些控制选项被描述为让教育者对课堂中的 AI 拥有细致的选择权，但 AI 设置与搜索本身相互纠缠——搜索如今默认展示 AI Overviews——使得彻底退出在技术上变得困难。这一结构与批评者此前在 Gmail 中指出的模式类似：关闭生成式 AI 功能可能会同时关闭诸如智能收件箱排序等更早的机器学习功能。

hackernews · ceejayoz · 11月3日 15:25 · [社区讨论](https://news.ycombinator.com/item?id=50353192)

**背景**: Google Workspace for Education 是大量中小学和高校使用的云端套件（包括 Classroom、Docs、Gmail、Drive 以及搜索访问权限），谷歌一直在其上不断叠加 Gemini for Education 等生成式 AI 功能。与此同时，谷歌搜索已围绕 AI Overviews 和 AI Mode 重建，即在传统链接上方放置 AI 生成的答案。用反垄断术语来说，要求客户为了保留一个产品（搜索）而必须接受另一个产品（AI），属于典型的搭售或捆绑安排；当占据支配地位的卖方以强制而非分售的方式迫使买方接受时，这种安排可能具有反竞争性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnn.com/2026/11/03/tech/google-ai-search-policy">Google will let schools turn off AI, but they may also lose ...</a></li>
<li><a href="https://arstechnica.com/ai/2026/11/google-will-let-schools-skip-ai-tools-but-they-have-to-give-up-search-too/">Google will let schools skip AI tools, but they have to give ...</a></li>
<li><a href="https://www.justice.gov/sites/default/files/atr/legacy/2007/04/18/chapter_5.pdf">Chapter 5 : Antitrust Issues in the Tying and Bundling of Intellectual...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（515 分、374 条评论）几乎一边倒地持批评态度，评论者将该政策称为胁迫性捆绑，并列举了相关不满：Gmail 的生成式 AI 无法在不关闭原有机器学习功能的情况下被禁用，Family Link 据称也不允许家长为年幼子女屏蔽谷歌应用。反复出现的疑问是谷歌究竟为何要力推 AI 摘要，不过也有评论者认为，相比充斥垃圾博客的前十条链接，AI Overviews 如今可能更可靠。

**标签**: `#google`, `#ai-in-education`, `#search`, `#policy`, `#big-tech-power`

---

<a id="item-5"></a>
## [利用飞机多普勒音频可精确定位视频拍摄地点](https://simonwillison.net/2026/Nov/3/a-sound-that-leaks-your-exact-location/) ⭐️ 8.0/10

一位名为 Colsto 的研究者演示了如何从视频音轨中提取几乎听不见的飞机背景噪音，分析其多普勒曲线，并与公开的 ADS-B 航班数据交叉比对，从而精确定位视频拍摄地点，据报道仅凭 60 秒音频即可将位置缩小到约 100 米范围内。 这把一种常被忽视的环境声音变成了视频创作者可能并未意识到的定位信号，对 YouTube 博主、记者以及任何在敏感地点发布音视频的人构成显著隐私风险。它还表明，公开的航班追踪数据可以与普通消费级媒体结合，从而对录音录像进行去匿名化定位。 该技术依赖于飞机飞越头顶时产生的可听或几乎不可听的多普勒频移、准确的录音时间，以及包含飞机位置、高度、速度和身份信息的公开 ADS-B 数据。其精度受航班轨迹质量、捕捉到的飞机数量以及航班间隔影响，在航空交通频繁且音频未经滤波的地区最为有效。

rss · Simon Willison · 11月3日 05:32

**背景**: ADS-B 是一种航空监视技术，飞机通过它定期广播自身位置、高度、速度和身份信息，这些数据由相关网络和航班追踪应用公开收集。多普勒效应是指声源靠近或远离听者时音调发生变化的现象；飞机飞越头顶时会在音频中留下独特的多普勒曲线。传统 OSINT 地理定位依赖地标、标牌和阴影等视觉线索，而这项技术表明背景声音也可以作为辅助性的位置指纹。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_Dependent_Surveillance–Broadcast">Automatic Dependent Surveillance–Broadcast - Wikipedia</a></li>
<li><a href="https://www.techradar.com/computing/cyber-security/youtuber-discovers-aircraft-noise-trick-that-can-geolocate-your-videos-to-within-100m-doppler-effect-pinpoints-locations-from-just-60-seconds-of-audio">YouTuber discovers aircraft noise trick that can geolocate ...</a></li>
<li><a href="https://maxintel.org/aircraft-doppler-audio-geolocation-2026.html">Planes Leak Your Location: Doppler Audio Geolocation Explained</a></li>

</ul>
</details>

**标签**: `#privacy`, `#OSINT`, `#geolocation`, `#audio-analysis`, `#ADS-B`

---

<a id="item-6"></a>
## [DeepSeek 开源内部大规模推理框架 DeepInfer](https://t.me/zaihuapd/44874) ⭐️ 8.0/10

10 月 20 日，DeepSeek 将其内部生产环境使用的大规模推理框架 DeepInfer 开源，并同步开源配套的 Token 编解码组件 deepseek-recipe。DeepSeek 表示，基于该框架，V4.1 Flash 在单一集群上的吞吐量可达每天 155 万亿 Tokens。 生产级的服务框架很少对外公开，因此这次开源为外部团队提供了构建高吞吐 LLM 服务的具体参考，而不必再从论文里逆向摸索性能优化技巧。框架同时支持英伟达与华为昇腾也值得关注，因为硬件多元化正是大规模推理中成本与供应链讨论的核心议题。 该框架支持分布式推理、推测解码与结构化输出，可运行在英伟达 GPU 和华为昇腾 NPU 上，并且 KVCache 可保留 72 小时以上。如此长的缓存保留时间说明它针对的是多轮对话、重复前缀等需要大量复用缓存的工作负载，而非一次性请求。

telegram · zaihuapd · 11月3日 06:20

**背景**: 大模型推理是自回归的：模型每次只生成一个 token，而每个新 token 都依赖此前所有 token，因此 KV Cache 会缓存中间注意力状态以避免重复计算。推测解码则通过让一个小的草稿模型先提出若干 token、再由更大的目标模型并行验证，在不影响输出质量的前提下降低延迟。华为昇腾是华为自研的 AI 加速器产品线，被广泛视为大规模训练与推理中英伟达 GPU 的替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency ...</a></li>
<li><a href="https://www.baseten.co/inference-engineering/book/05-techniques/caching/">Caching | Inference Engineering</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/huawei-ascend-npu-roadmap-examined-company-targets-4-zettaflops-fp4-performance-by-2028-amid-manufacturing-constraints">Huawei Ascend NPU roadmap examined — company targets 4 ...</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#open source`, `#DeepSeek`, `#distributed systems`, `#Huawei Ascend`

---

<a id="item-7"></a>
## [Stringman：售价 800 美元的开源房间级缆索驱动机器人](https://neufangled.com/) ⭐️ 7.0/10

独立开发者 Nathaniel（Neufangled Robotics）发布了 Stringman，这是一台售价约 800 美元的开源房间级机器人：它通过四个安装在天花板上的电动绞盘收放绷紧的绳索来悬吊一个夹爪，从而在约 7×7×3 米的空间内任意移动。该项目已获得 OSHWA 开源硬件认证，机械 CAD 图纸、PCB 设计和控制软件全部公开。 与受限于固定半径的桌面机械臂不同，缆索驱动架构只需四个执行器就能覆盖整个房间的空间，单位成本可获得的工作空间远超同类方案，让爱好者以远低于移动操作机器人的价格进入家用机器人领域。此外，其开源、本地运行、可断网（air-gapped）的设计也使其成为相较云端联网家用机器人更注重隐私的替代方案。 Stringman 在 7×7×3 米的工作空间内平均可承载约 1.9 公斤，并设有张力上限机制：当有人用力拉扯时绳索会自动放出，因此基本不会造成人身伤害。创作者表示，只要把工作区域的上界设定在吊扇下方，在有吊扇的房间里通常也能正常使用；目前最主要的易用性短板在于停机时绳索和夹爪仍悬在原处、无法收纳。

hackernews · nharada · 11月3日 16:47 · [社区讨论](https://news.ycombinator.com/item?id=50354358)

**背景**: Stringman 属于缆索驱动并联机器人（CDPR），这类并联机构用绞盘收放的柔性绳索代替刚性连杆来定位末端执行器。CDPR 以结构轻巧、工作空间大、响应速度快和成本低著称，已被用于运动模拟器、大型 3D 打印和工业搬运，但很少以消费级价格出现。Stringman 把这一架构用于家庭场景中的操作任务，例如拾取玩具、衣物和各种杂物。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://neufangled.com/">Stringman from Neufangled Robotics</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cable_robots">Cable robots - Wikipedia</a></li>
<li><a href="https://neufangled.com/stringman">Stringman | Neufangled Robotics</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论整体非常热情，最受支持的诉求是希望机器人闲置时能把斜拉绳索收回并收纳起来，有评论者称这样会让它更容易成为冲动购买的选择。其他人则提出了新的应用场景，例如装上旋转刀片用于自动除草（但也担心会误伤较高的植物以及切割反作用力），创作者本人也现身直接回答了安全性、吊扇和育儿方面的提问；还有几条纯属玩梗，其中一条拿“Tension is all you need”开玩笑。

**标签**: `#robotics`, `#open-source-hardware`, `#cable-driven-robots`, `#DIY`, `#hacker-news`

---

<a id="item-8"></a>
## [批评者称“Astra 读写权重提升 Qwen”的说法具有误导性](https://honnibal.dev/blog/astra-read-write-misleading) ⭐️ 7.0/10

Matthew Honnibal 发表博客文章指出，近期被广泛传播的说法——GPT-6 Astra 能原生读取并改写 Qwen3.5-0.8B 的部分权重，在无需梯度的情况下将其 MATH-500 成绩从 7.9% 提升到 48.1%——具有误导性。他认为这次干预并没有让模型“更擅长数学”，而只是消除了 Qwen 自己模型卡中就已提示的推理循环失效模式。 这一事件是机械可解释性领域研究炒作的典型案例：一个针对退化解码循环的局部修复，被包装成前沿模型直接重编程另一个模型的知识。社区如何定性此事，将影响从业者把“权重空间编程”视为微调的真实替代方案，还是视为被夸大包装的引导技巧。 被修改的权重仅约 0.016%，而根本问题在于模型生成用于结束推理段的 </think> 词元概率过低，而这一问题是简单的激活引导同样可以修复的。因此那个惊人的基准分数跃升，实际上是把“跳出重复推理循环”与“获得数学能力”混为一谈。

hackernews · syllogism · 11月3日 12:21 · [社区讨论](https://news.ycombinator.com/item?id=50351111)

**背景**: 机械可解释性是 AI 研究的一个子领域，目标是逆向分析神经网络内部到底在计算什么，而不只是测量其输出。激活引导（activation steering）则是一种相关的推理期技术，通过向模型的内部状态叠加向量来改变其行为，而无需重新训练。原始说法来自 MIT CSAIL 研究人员 2026 年 11 月 2 日的一篇文章，其中提出“权重空间编程”：前沿模型可 supposedly 直接编辑小模型的参数，不使用梯度下降，也没有训练循环；MATH-500 则是用来评估此类主张的标准竞赛数学基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://honnibal.dev/blog/astra-read-write-misleading">The 'Astra can read and write weights to improve Qwen' post ...</a></li>
<li><a href="https://explainx.ai/blog/weight-space-programming-gpt-6-astra-edits-qwen3-5-0-8b-weights-math-7-9-to-48-1-mit-csail-2026">GPT-6 Astra Edits Qwen Weights: MATH-500 7.9% to 48.1% ...</a></li>
<li><a href="https://dev.to/iamfaham/llm-steering-from-prompting-tricks-to-activation-control-33d0">LLM Steering : From Prompting Tricks to Activation... - DEV Community</a></li>

</ul>
</details>

**社区讨论**: 评论者大多支持这一批评：一位自称从事机械可解释性研究的网友称原文“确实具有误导性”，并解释说该结果只是通过简单引导即可实现的循环减少；另一位读者则认为该技术看起来只是已有权重编辑与引导论文的重新包装。也有人持不同意见，指出原文其实明确解释过推理循环问题，并且即便示例被夸大，仍有读者认为“权重空间编程”这一概念确实令人印象深刻。

**标签**: `#mechanistic-interpretability`, `#AI-research-critique`, `#LLM-steering`, `#Qwen`, `#research-hype`

---

<a id="item-9"></a>
## [现代国际象棋引擎跑在 1996 年的奔腾上，能击败卡斯帕罗夫吗？](https://nicholas.carlini.com/writing/2026/algorithmic-improvements-chess.html) ⭐️ 7.0/10

Nicholas Carlini 发表了一篇分析文章，认为现代国际象棋引擎远强于上世纪 90 年代的引擎，主要原因在于评估函数与搜索算法上的算法改进，而非单纯的硬件性能提升；他并以此为前提提出一个问题：如果把现代引擎跑在 90 年代的奔腾硬件上，它能否在 1996 年击败加里·卡斯帕罗夫。该文在 Hacker News 上获得 421 分和 194 条评论。 这篇文章重新审视了一个关于人工智能进步的常见问题：棋类系统实力的提升究竟有多少来自更聪明的算法、多少来自更强的算力。这个问题的答案意义远不止于国际象棋，因为当下围绕机器学习的讨论同样存在这种归因之争，同时也呼应了人们长久以来对“深蓝”与卡斯帕罗夫的历史性假设推演。 评论者反驳了“击败卡斯帕罗夫”这一字面设想，指出现代引擎是针对庞大算力预算调优的，在评估与搜索深度之间做出的权衡与旧引擎大不相同；一旦算力被严重限制，其激进的剪枝策略会暴露出明显弱点，足以被世界冠军的团队针对利用。也有人对文章的旁枝观点提出挑刺，指出 Pentium Pro 是首个采用 P6 乱序微架构的处理器（Pentium II 的前身），并非简单地不如 Pentium MMX。

hackernews · markusw · 11月3日 07:56 · [社区讨论](https://news.ycombinator.com/item?id=50349276)

**背景**: 上世纪 90 年代的棋类引擎（包括 IBM 的“深蓝”）将 alpha-beta 剪枝与人工编写的评估函数结合使用：前者是一种极小化极大搜索优化，会丢弃不可能影响最终决策的分支；后者则对子力、王的安全和兵形结构打分。而 Stockfish 等现代引擎改用 NNUE（高效可更新神经网络）——一种源自计算机将棋、2020 年被 Stockfish 采纳的小型神经网络评估函数，使引擎实力一夜之间大幅提升。深蓝在 1996 年的比赛中以 2 比 4 负于卡斯帕罗夫，又在 1997 年的复赛中获胜，因此“某种算法需要多强的硬件”这一问题才让这个反事实假设如此有趣。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Alpha-beta_pruning">Alpha-beta pruning</a></li>
<li><a href="https://en.wikipedia.org/wiki/Efficiently_updatable_neural_network">Efficiently updatable neural network - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Stockfish_chess_engine">Stockfish chess engine</a></li>

</ul>
</details>

**社区讨论**: 总体情绪是：文章的核心论点——实力提升主要来自算法而非硬件——是正确的，但涉及卡斯帕罗夫的具体推断站不住脚；一位评论者认为，一名水平接近专家的棋手就能轻易利用算力受限的现代引擎在搜索深度上的权衡弱点。也有人质疑文中“特级大师与业余爱好者分析的变化数量大致相同”的说法，并举出特级大师直播对局时明显探索更多分支、算得更深的例子。还有评论者发散地类比道，像 AV1、HEVC 这样的现代视频编码或许能让 90 年代的 ISDN 连接也实现可接受的流媒体播放。

**标签**: `#chess engines`, `#algorithms`, `#performance`, `#hardware`, `#AI history`

---

<a id="item-10"></a>
## [犹他州对 Kalshi 及其联合创始人提起赌博重罪指控](https://arstechnica.com/tech-policy/2026/10/trump-admin-sues-utah-to-save-kalshi-from-the-states-total-ban-on-gambling/) ⭐️ 7.0/10

犹他州于周三对预测市场运营商 Kalshi 及其两位联合创始人提起刑事指控，公司及每位个人均面临 13 项重罪指控和一项轻罪指控，罪名是违反该州赌博法。这些指控提出于一名联邦法官驳回 Kalshi 阻止犹他州执行其严格反赌博法规的请求数月之后，同时特朗普政府正起诉犹他州，试图让 Kalshi 免于该州的全面禁令。 这是围绕“谁有权监管预测市场”之争的急剧升级：州政府不再依赖罚款或民事禁令，而是动用刑法直接针对一家受联邦监管的交易所及其高管个人。该案的结果可能确立判例，决定受 CFTC 监管的事件合约是否仍须服从各州赌博禁令，从而影响 Kalshi、Polymarket 等竞争对手，以及 Robinhood 等分销此类产品的合作方。 每位被告面临 13 项重罪和一项轻罪指控，这种异常强硬的做法被法律观察人士视为州与联邦监管冲突中的新战术。Kalshi 的核心抗辩建立在联邦优先权之上——它是经 CFTC 指定设立的合约市场，而一家联邦上诉法院最近裁定新泽西州不能像监管赌博那样监管其预测市场。

hackernews · rbanffy · 11月3日 15:29 · [社区讨论](https://news.ycombinator.com/item?id=50353229)

**背景**: 预测市场允许用户买卖“事件合约”，其收益取决于现实世界某件事是否发生，例如选举结果或经济指标。在联邦层面，这类合约被视为由美国商品期货交易委员会（CFTC）监管的金融衍生品，Kalshi 是首个被指定为 CFTC 受监管合约市场的平台。相比之下，犹他州拥有美国最严格的反赌博制度之一，实际上禁止一切形式的博彩，并认为预测市场不过是换了名字的赌博。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/tech-policy/2026/10/trump-admin-sues-utah-to-save-kalshi-from-the-states-total-ban-on-gambling/">Kalshi and its co-founders face felony charges for violating Utah ...</a></li>
<li><a href="https://www.theguardian.com/us-news/2026/oct/28/utah-criminal-charges-kalshi">Utah files criminal charges against prediction market... | The Guardian</a></li>
<li><a href="https://pmwisdom.com/learn/are-prediction-markets-legal">Are Prediction Markets Legal? US State-by-State Guide... | PM Wisdom</a></li>

</ul>
</details>

**社区讨论**: 评论者意见分歧，但总体上同情犹他州主张州主权，其中一人称赞该州“认真对待自身主权”，并敢于同时对抗 Kalshi 和联邦政府。其他人则提出了执法层面的现实担忧，例如 VPN 和代理服务器与犹他州“网站担责”思路如何相互作用；还有人以 Kalshi 此前挑衅性的深伪运动员营销视频为例，认为这显示该公司乐于“试探体面底线”。

**标签**: `#Kalshi`, `#prediction markets`, `#gambling regulation`, `#state vs federal law`, `#fintech`

---

<a id="item-11"></a>
## [SemiAnalysis：SpaceX 或成全球最大 AI 云](https://newsletter.semianalysis.com/p/elon-is-doing-it-again-spacex-will) ⭐️ 7.0/10

SemiAnalysis 发布分析称，SpaceX 有望通过在约一年半内建设 13GW 数据中心容量并改造火箭飞船园区，成为全球最大的 AI 云服务商。文章还探讨了在 TeraFab 部署数据中心的设想。 如果这一设想落地，13GW 的新增容量将极大改变 AI 算力供给格局，并加剧超大规模云厂商、芯片厂商和能源供应商在电力与数据中心选址上的竞争。这也可能推动发射基础设施、芯片生产与 AI 云服务之间更深度的垂直整合。 在约 18 个月内实现 13GW 的目标远快于典型数据中心建设周期，电力采购、冷却、审批和网络连接将是关键瓶颈；文章还提出在 TeraFab 这一马斯克推动的垂直整合芯片设施部署数据中心的设想。这些说法属于分析性推演，而非 SpaceX 已确认的承诺。

rss · Semianalysis · 11月3日 20:44

**背景**: 吉瓦是持续功率单位，13GW 数据中心容量意味着相当于多座大型发电厂的电力足迹，而不仅是装满服务器的厂房。TeraFab 是马斯克在奥斯汀推动的半导体综合体，计划把芯片设计、制造、内存生产、先进封装和测试集中在一个园区内，并与 Gigafactory Texas 相邻。SemiAnalysis 的论述把 SpaceX 的大型发射与制造园区同 AI 数据中心对电力和空间的需求联系起来，其数据中心行业模型也按站点追踪容量与电力预测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Terafab">Terafab - Wikipedia</a></li>
<li><a href="https://www.basenor.com/blogs/news/terafab-construction-underway-first-look-at-tesla-spacex-xai-chip-facility">Terafab Construction Underway: First Look at Tesla-SpaceX-xAI ...</a></li>
<li><a href="https://semianalysis.com/datacenter-industry-model/">Datacenter Industry Model: AI Datacenter Capacity & Power ...</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#datacenters`, `#SpaceX`, `#AI cloud`, `#energy`

---

<a id="item-12"></a>
## [Protegrity 发布 278M 开放权重 RoBERTa 个人信息检测模型及 PII-SCOPE 基准](https://www.reddit.com/r/MachineLearning/comments/1xn2lro/a_new_openweights_278m_pii_detection_model_and/) ⭐️ 7.0/10

Protegrity 发布了一个 278M 参数的开放权重个人信息（PII）检测模型，它是在 RoBERTa 基础上微调而来，训练数据约为 12 亿条包含各类个人信息的合成样本。除已在 Hugging Face 上架的模型外，团队还同步发布了 PII-SCOPE 基准（Synthetic Context and Ontology for PII Extraction，即用于 PII 抽取的合成上下文与本体）以及一份 arXiv 技术报告（2610.30518v2）。 目前生产环境中的 PII 清洗大多仍依赖正则表达式和词典规则，这类方法在遇到非常规格式时容易失效，也难以识别依赖上下文才能判断的标识符；一个可免费下载的上下文感知模型，为那些无法将数据发送给第三方 API 的受监管团队降低了门槛。同时，开放基准让隐私工程社区有了统一的模型对比方式，而此前这类对比基本只存在于厂商的宣传材料中。 该模型是一个编码器架构，依据上下文标注 PII 片段，可直接返回每个检测实例的位置索引与类型，也可返回已将全部 PII 脱敏的输入文本；而 PII-SCOPE 的构建初衷正是为了解决公开的 LLM 生成数据集存在的已知问题。由于 12 亿条训练样本全部为合成数据，模型在真实场景中的表现将取决于该合成分布与实际部署领域及语言的匹配程度。

reddit · r/MachineLearning · /u/shanekj · 11月3日 19:29

**背景**: PII（个人可识别信息）涵盖姓名、邮箱、电话号码、身份证号、账户信息等数据，GDPR、CCPA 等法规要求企业识别并保护这些信息。RoBERTa 是 2019 年提出的 BERT 风格 Transformer 编码器，它保持 BERT 架构不变，但通过动态掩码、更大批量和更多数据改进了预训练过程，因而成为 token 分类任务中常用且廉价的骨干模型。“开放权重”指训练好的参数可以下载，机构能在自有基础设施上运行推理，而不必调用托管 API——这正是隐私敏感场景最关键的特性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1907.11692">[1907.11692] RoBERTa: A Robustly Optimized BERT Pretraining ... RoBERTa - PyTorch Large Language Models: RoBERTa - A Robustly Optimized BERT ... RoBERTa - Hugging Face RoBERTa: A Robustly Optimized BERT Pretraining Approach</a></li>
<li><a href="https://huggingface.co/docs/transformers/model_doc/roberta">RoBERTa · Hugging Face</a></li>
<li><a href="https://www.ai21.com/glossary/foundational-llm/open-weights-model/">What is an Open - Weights Model ? | AI 21</a></li>

</ul>
</details>

**标签**: `#PII detection`, `#open-weights`, `#benchmark`, `#RoBERTa`, `#privacy`

---

<a id="item-13"></a>
## [OpenAI 指控《纽约时报》索要 2000 万条 ChatGPT 对话侵犯用户隐私](https://t.me/zaihuapd/44875) ⭐️ 7.0/10

2025 年 11 月，OpenAI 发布声明，指责《纽约时报》在其版权诉讼中要求交出 2000 万条 ChatGPT 用户对话，称这是对用户隐私的侵犯。OpenAI 表示此前已多次拒绝类似要求，其中包括索取 14 亿条聊天记录的请求，并强调用户托付给 ChatGPT 的聊天、文件与账号信息属于最敏感的数据。 这场争执为法院在涉及训练数据的诉讼中能在多大程度上强制 AI 公司交出用户对话设定了重要先例，其结果可能影响数亿 ChatGPT 用户对隐私的预期。这也表明 OpenAI 正把隐私当作应对版权索赔的法律与舆论屏障。 OpenAI 首席信息安全官表示，公司正通过数据去标识化与加密措施保护用户，并计划推出客户端端到端加密以及自动安全检测系统。不过去标识化只能降低而非消除重识别风险，而端到端加密也可能与服务器侧的滥用检测以及配合法律要求的能力产生冲突。

telegram · zaihuapd · 11月3日 06:50

**背景**: 《纽约时报》于 2023 年底起诉 OpenAI 与微软，指称 ChatGPT 会复制其文章内容，并认为用其新闻内容训练模型构成版权侵权。在美国民事诉讼中，证据开示规则允许双方相互索取文件与数据，而围绕索取范围的争议十分常见。去标识化指移除或遮蔽可识别个人身份的信息，从而在保留数据用途的同时降低隐私风险；端到端加密则意味着只有通信双方而非服务提供商持有解密密钥。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/De-identification">De - identification - Wikipedia</a></li>
<li><a href="https://mohashari.github.io/end-to-end-encryption-chat-applications/">Implementing End-to-End Encryption (E2EE) in Web Chat ...</a></li>
<li><a href="https://plurilock.com/consulting/data-protection-and-dlp/chat-application-monitoring/">Chat App Security Monitoring | Data Protection | Plurilock</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#New York Times`, `#privacy`, `#AI litigation`, `#user data`

---

<a id="item-14"></a>
## [字节跳动火山引擎发布 Seedance 2.5 4K 视频模型，主打大荧幕质感](https://t.me/zaihuapd/44880) ⭐️ 7.0/10

字节跳动旗下火山引擎正式发布 Seedance 2.5 4K 模型，这是 Seedance 视频生成系列迄今最强的一个版本。该模型经过专项训练，能更充分地学习人物表情、细微动作与画面细节，并支持 Draft 模式：先用 480P 样片快速验证分镜，满意后再生成 4K 正片。 字节跳动推出支持 4K 与 10-bit 色深的生成模型，意味着 AI 视频正向广播与院线级制作流程靠拢，而色深和细腻的面部表演恰恰是过去的主要门槛。若实际效果经得起检验，影视与广告团队的分镜、预演（previz）工作或将部分从传统渲染转向生成式工具。 该模型具备 10-bit 色深，色彩层次更丰富、过渡更平滑；字节方面称，在影视文戏测试中，4K 版本对人物细微反应的呈现更充分、表演更有层次。目前模型仅供部分企业客户试用，后续或将逐步扩大开放范围，但官方尚未公布定价、基准测试数据或公开 API 接入方式。

telegram · zaihuapd · 11月3日 09:36

**背景**: Seedance 是字节跳动的 AI 视频生成模型系列，通常通过火山引擎对外提供——这是字节面向企业客户的云与 AI 服务平台，负责把集团内部技术进行 B2B 输出。早前版本的 Seedance（如 2.0、2.5）多以 API 形式在第三方模型平台上提供文生视频、图生视频能力。色深（bit depth）指每个色彩通道可表示的取值数量，10-bit 每通道有 1024 级，而 8-bit 只有 256 级，因此 10-bit 是专业影视与 HDR 工作流的标准要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/en/item/Volcano+Engine/1423148">Volcano Engine（ByteDance's cloud service platform）_Baiduwiki</a></li>
<li><a href="https://www.volcengine.com/lang/en">Volcano Engine</a></li>
<li><a href="https://wavespeed.ai/models/bytedance/seedance-2.5/image-to-video">Seedance 2 . 5 Image to Video API on WaveSpeedAI</a></li>

</ul>
</details>

**标签**: `#AI video generation`, `#ByteDance`, `#generative AI`, `#4K`, `#model release`

---

<a id="item-15"></a>
## [普京要求俄私营数据中心预留 10%算力供政府征用](https://www.reuters.com/technology/putin-orders-private-data-centres-set-aside-10-capacity-support-it-2026-11-02/) ⭐️ 7.0/10

俄罗斯总统普京签署总统令，要求俄罗斯境内的非国有数据中心预留 10%的场地和计算能力供政府征用，运营商须在接到通知后 24 小时内提供使用权限。 该总统令将私营数据中心的预留资源变为政府可调用的资源，直接影响俄罗斯境内的数据中心运营商和云基础设施提供商，也表明政府对关键计算基础设施的控制进一步加强。 俄罗斯数字发展部须对全国私营数据中心的可用场地和计算能力进行清查，政府将成立专门委员会，有权要求运营商释放预留资源。经俄罗斯联邦安全局（FSB）批准，政府还可临时调用位于境外的数据中心资源。

telegram · zaihuapd · 11月3日 10:58

**背景**: 数据中心承载着支撑云服务、网站和其他信息系统的服务器与存储设备，因此预留一部分容量可使政府在发生中断或紧急情况时获得备用计算资源。该总统令将国家监管从网络基础设施延伸到私营计算能力，反映出对 IT 主权更广泛的重视。

**标签**: `#data centers`, `#cloud infrastructure`, `#regulation`, `#Russia`, `#IT sovereignty`

---

<a id="item-16"></a>
## [传英伟达要求全球数据中心将中国企业业务占比限制在 49%以内](https://www.tomshardware.com/tech-industry/data-centers/nvidia-tells-data-center-operators-to-limit-business-from-chinese-customers-with-new-global-restrictions-report-claims-allegedly-restricted-to-49-percent-of-the-total-ensuring-51-percent-are-non-chinese-outfits) ⭐️ 7.0/10

据《金融时报》报道，英伟达已要求全球数据中心运营商将来自中国企业的业务占比控制在 49%以内，确保至少 51%的业务来自非中国企业。该要求据称仅适用于新签和未来合同，不影响已签订的租赁协议，并且由销售团队和区域团队口头传达，并未发布正式文件。 如果消息属实，这将是美中科技脱钩的一次明显升级：管制逻辑从芯片销售延伸到了数据中心租户层面，可能重塑全球云服务商与托管数据中心运营商分配 GPU 算力的方式。依赖海外数据中心算力的中国 AI 企业，以及为其提供服务的运营商，都可能面临新的合规负担和更高的成本。 该限制被描述为口头指导而非正式公布的规则，且据称只覆盖新签和未来合同，不影响已有租约。英伟达的回应以“美国基础设施是美国模型与应用厂商参与全球竞争的基础”为框架来解释这一政策；由于消息依赖匿名信源，具体适用范围与可执行性仍不明确。

telegram · zaihuapd · 11月3日 16:19

**背景**: 多年来，美国以国家安全为由限制向中国出口英伟达高端数据中心 GPU 等先进 AI 芯片，并推动马来西亚、新加坡、台湾等盟友加强转口管制。由于中国企业仍可在海外租用算力，外界开始关注为这些企业提供服务的数据中心运营商是否会成为变相漏洞。与此同时，数据中心租约期限正在拉长，近期签订的合同往往超过十年，因此对新签合同的任何限制都可能在未来数年锁定市场格局。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/data-centers/nvidia-tells-data-center-operators-to-limit-business-from-chinese-customers-with-new-global-restrictions-report-claims-allegedly-restricted-to-49-percent-of-the-total-ensuring-51-percent-are-non-chinese-outfits">Nvidia tells data center operators to limit business from Chinese ...</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/policy/malaysia-seizes-usd12-million-worth-of-advanced-ai-chips-hidden-inside-30-servers-customs-says-suspected-smuggling-network-used-the-country-as-a-transit-hub">Malaysia seizes $12 million worth of advanced AI chips hidden inside...</a></li>

</ul>
</details>

**标签**: `#nvidia`, `#export-controls`, `#us-china-tech`, `#ai-infrastructure`, `#data-centers`

---

<a id="item-17"></a>
## [Atlas 将 10.9 万篇机器学习会议论文整理成 1260 个主题页面](https://www.reddit.com/r/MachineLearning/comments/1xmk8rx/we_turned_10_years_of_ml_papers_into_one_page_per/) ⭐️ 6.0/10

一个团队（Reddit 用户 /u/latenticlabs）发布了 Atlas 工具：它收录了 2016 年以来 ICML、NeurIPS、ICLR、CVPR 和 AAAI 约 10.9 万篇被接收论文，将其归入约 1260 个主题，并从其中 7.9 万篇的全文里抽取了结果表格与消融实验。每个主题页面展示了随时间变化的最佳基准记录及对应论文、近期论文中的消融实验（包括那些使效果变差的设置）、近期工作所对比的基线方法，以及相关 arXiv 预印本和 BibTeX 文件。 研究者通常要读几十篇 PDF 才能拼出某个子领域的基准演进、基线惯例和常见消融要求；Atlas 把这一切压缩到每个主题一页，对需要挑选基线的新人以及需要预判审稿人问题的作者尤其有用。由于它覆盖五大顶会长达十年，还能直观呈现领域级趋势——例如紧凑/高效高斯泼溅主题的论文数从 2023-24 年的 29 篇增长到 2025-26 年的 240 篇。 这些页面由抽取出的数字自动计算生成，每个数值都可链接回原论文，但作者明确提醒抽取并不完美、不同论文的数字也未必可比，因此应把它当作起点而非排行榜。2026 年论文的基准数字与消融实验尚未纳入，所以记录主要反映 2025 年及之前的工作；作者也呼吁熟悉某一主题的专家指出页面中的错误。

reddit · r/MachineLearning · /u/latenticlabs · 11月3日 05:09

**背景**: 机器学习发展极快，导致基准最优结果、标准基线和常规消融分散在成千上万篇 PDF 中，往往只有子领域内的研究者心照不宣。文献挖掘流水线试图通过解析论文中的表格和文本来自动化这一过程，但结果表格的格式千差万别，可靠抽取并不容易。文中的示例主题“3D 高斯泼溅”是一种 2023 年复兴的实时新视角合成技术，衍生出 Scaffold-GS、2DGS 等大量后续工作，其 Deep Blending PSNR 基准是常被引用的渲染质量指标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/3D_Gaussian_splatting">3D Gaussian splatting</a></li>
<li><a href="https://github.com/city-super/Scaffold-GS">GitHub - city-super/Scaffold-GS: [CVPR 2024 Highlight ...</a></li>
<li><a href="https://github.com/Phog/DeepBlending">Deep Blending for Free-Viewpoint Image-Based Rendering Deep Blending | SOTA | HyperAI DeepBlending Dataset Results | noodle-lab/GaussianSpa | DeepWiki Deep Blending (DrJohnson + Playroom NVS) — papers and ... NerfBaselines: Dataset Mip-NeRF 360</a></li>

</ul>
</details>

**标签**: `#machine-learning`, `#literature-mining`, `#research-tools`, `#information-extraction`, `#benchmarks`

---