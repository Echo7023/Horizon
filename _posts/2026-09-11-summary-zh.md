---
layout: default
title: "Horizon Summary: 2026-09-11 (ZH)"
date: 2026-09-11
lang: zh
---

> 从 35 条内容中筛选出 21 条重要资讯。

---

1. [微软将 Rust 提升为一级（Tier-1）语言](#item-1) ⭐️ 9.0/10
2. [DeepSeek 发布 V4.1 Flash：详尽技术报告加持，缓存命中价格低至惊人](#item-2) ⭐️ 9.0/10
3. [Calif Research 演示 WeWorm：首个通过微信通话传播的零点击蠕虫](#item-3) ⭐️ 9.0/10
4. [研究者质疑能否放心将未发表的数学成果交给 OpenAI](#item-4) ⭐️ 8.0/10
5. [Shopify 将移动应用从 React Native 迁回完全原生开发](#item-5) ⭐️ 8.0/10
6. [索尼 PlayStation 数字游戏所有权诉讼引发关注](#item-6) ⭐️ 8.0/10
7. [DeepSeek 发布 MIT 协议 Harness 框架，并开放 V4-Pro-0813 权重](#item-7) ⭐️ 8.0/10
8. [一篇随笔提出软件开发会把人逼疯的理论](#item-8) ⭐️ 7.0/10
9. [Cognition 发布 SWE-2 编程模型，宣称比肩 Fable 5.1 与 GPT-Astra](#item-9) ⭐️ 7.0/10
10. [NASA 为火星开发的假彩色技术如今用于揭示地球上的隐藏岩画](#item-10) ⭐️ 7.0/10
11. [Raymond Chen 揭秘 Windows XP 如何为你的初始用户头像挑选图片](#item-11) ⭐️ 7.0/10
12. [SemiAnalysis 解析数据中心表后供电难题](#item-12) ⭐️ 7.0/10
13. [真实果蝇连接组学不会打乒乓球，审计揭出流水线缺陷](#item-13) ⭐️ 7.0/10
14. [蚂蚁国际联合 Visa 与 Mastercard 制定 AI 代理支付标准](#item-14) ⭐️ 7.0/10
15. [月之暗面（Kimi）保密递交港股 IPO 申请，投前估值 500 亿美元](#item-15) ⭐️ 7.0/10
16. [腾讯混元开源统一音频编辑模型 AuK](#item-16) ⭐️ 7.0/10
17. [PlanetScale 推出闭源 Postgres 分片产品 Neki](#item-17) ⭐️ 6.0/10
18. [.blend URL Viewer：在浏览器中直接预览 Blender 文件](#item-18) ⭐️ 6.0/10
19. [348M 参数模型仅用 22.7B token 训练，靠展示运算步骤完成 14 位算术](#item-19) ⭐️ 6.0/10
20. [ChatGPT 语音模式新增 GPT-5.6 Sol 与 GPT-6 Astra 模型选择](#item-20) ⭐️ 6.0/10
21. [HBM 短缺致中国 AI 芯片涨价 20%—50%](#item-21) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [微软将 Rust 提升为一级（Tier-1）语言](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 9.0/10

在 Rust 基金会发布的一篇客座文章中，微软确认已将 Rust 视为一级（tier-1）语言，与 C、C++、C#等长期使用的主力语言并列用于内部系统级开发。这一称号意味着 Rust 将在微软各平台上获得一流的工具链、工程投入与官方支持，而不再只是实验性或边缘化的选择。 微软是全球最大的操作系统与开发者工具供应商之一，它的正式背书为 Rust 在系统编程领域提供了强有力的合法性信号，也可能推动其他大型操作系统与平台厂商在全新（greenfield）项目中拓宽语言选择。这同样关乎安全：内存安全类漏洞历来约占微软 CVE 的 70%，而 Rust 的所有权模型正是为消除这类缺陷而设计的。 这条新闻标题背后的一些细节来自相关讨论而非公告本身：评论者提到微软的目标是在 2030 年前通过自动化工具把 10 亿行代码转换为 Rust，效率指标为“1 名工程师、1 个月、100 万行代码”；此外还有 DARPA 资助的项目，由 6 个团队用不同方法推进 C 到 Rust 的自动化转换。仍待明确的问题包括一级语言地位究竟覆盖到何种程度，尤其是 Visual Studio 是否会提供一流的 Rust 调试支持，以及关于 MSVC 集成的传闻最终会落实到什么程度。

hackernews · mmastrac · 9月10日 13:39 · [社区讨论](https://news.ycombinator.com/item?id=49643546)

**背景**: 系统编程指的是编写让计算机运转起来的底层软件——操作系统、设备驱动、内存管理与网络层——这些领域对性能和直接控制硬件有很高要求，几十年来一直由 C 和 C++主导。Rust 是一门相对较新的语言，目标是在性能上匹敌 C/C++，同时通过编译期的“所有权”规则防止缓冲区溢出、释放后使用（use-after-free）等内存安全错误。许多公司会给内部语言划分“层级”，其中一级（tier-1）意味着获得完整支持、被推荐用于生产环境且有官方工具链支撑，与实验性层级相对。全新开发（greenfield）指从零开始构建、不受遗留代码约束的新项目，这通常也是像 Rust 这样的语言最容易被引入、且无需付出高昂重写成本的场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=49643546">Rust Is Tier - 1 Language at Microsoft | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Systems_programming">Systems programming - Wikipedia</a></li>
<li><a href="https://qarea.com/blog/difference-between-brownfield-and-greenfield-software-development">Difference between Brownfield and Greenfield Software Development</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（509 分、279 条评论）总体积极，评论者称这是重大消息——如今所有在 C/C++工具链中占有一席之地的主流操作系统厂商，都在为全新项目多元化其系统编程语言选择。有人表示这表明 Rust 不再是“快速迭代、边跑边坏”的稚嫩语言，而是能成熟地与 C++和 C#竞争的对手，且相比 Zig、Odin 这些更新的“更好的 C/C++”替代品棱角更少；也有人欢迎关于 MSVC 集成这一期待已久的公开消息。质疑同样存在：有评论者打趣说既然采用 Rust，微软的天气应用就该停止占用超过 1GB 内存，还有人追问 Visual Studio 的一级调试支持究竟何时能落地。

**标签**: `#Rust`, `#Microsoft`, `#programming languages`, `#systems programming`, `#software engineering`

---

<a id="item-2"></a>
## [DeepSeek 发布 V4.1 Flash：详尽技术报告加持，缓存命中价格低至惊人](https://twitter.com/deepseek_ai/status/2097930608790167907) ⭐️ 9.0/10

DeepSeek 发布了 DeepSeek-V4.1-Flash，在 Hugging Face 上公开了模型权重并附上一份内容详尽的技术报告。新模型参数规模扩大到 552B，几乎是初代 V4 Flash（284B）的两倍，并宣称缓存命中的输入价格仅为每百万 token 0.003 美元。该发布在 Hacker News 上迅速获得 886 分和 495 条评论。 DeepSeek 一边坚持接近前沿规模的训练，一边公开异常详尽的研究细节，这与美国实验室常见的以安全内容为主的系统卡形成鲜明对比。极低的缓存命中价格也引出一个更深层的问题：随着复用缓存上下文的成本可能低于网络传输成本，推理经济学或将重塑 agent 和聊天 API 的构建方式。 有评论者指出，该模型已达 552B 参数，所谓 “Flash” 级别已名不副实，本地部署难度远高于此前的 284B 版本，并提醒基准分数的提升可能部分来自 “刷榜” 而非真实能力。每百万 token 0.003 美元的缓存命中价仅适用于被重复使用、按缓存费率而非完整未命中费率计费的输入 token，因此实际成本高度依赖具体工作负载模式和缓存命中率。

hackernews · Liwink · 9月10日 06:11 · [社区讨论](https://news.ycombinator.com/item?id=49639090)

**背景**: 缓存命中定价是 LLM API 中常见的机制：被重复使用的提示 token（通常是系统提示或代码库上下文这类稳定的长前缀）按较低的缓存费率而非完整输入费率计费；OpenAI 等竞争对手的缓存输入折扣通常约为 50%，这使得 DeepSeek 的费率显得格外激进。整体来看 LLM 推理价格下降极为迅速，有估算认为三年内降幅达约 1000 倍，因此定价结构正日益成为竞争差异化因素而非细枝末节。参数量之所以重要，是因为更大的模型在本地服务时需要成比例的更多 GPU 显存，这正是从 284B 跃升到 552B 会改变自托管用户部署逻辑的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rephrase-it.com/blog/deepseek-v4-cache-pricing-changes-agents">DeepSeek V4 Cache Pricing Changes Agents | Rephrase</a></li>
<li><a href="https://epoch.ai/data-insights/llm-inference-price-trends">LLM inference prices have fallen rapidly but unequally... | Epoch AI</a></li>
<li><a href="https://tkmxai.it.com/openai-vs-anthropic-vs-google">OpenAI vs Anthropic vs Google - ai inference - LLM Gateway Daily</a></li>

</ul>
</details>

**社区讨论**: 整体氛围积极且偏重技术分析：评论者称赞 DeepSeek 的技术报告充满工程细节，与他们认为安全内容占比过高的系统卡形成对比，并钦佩该团队敢于在接近前沿的规模上押注大胆的研究想法。一些评论者聚焦经济性，思考若通过网络传输上下文的成本高于缓存 token 本身，0.003 美元/百万缓存命中 token 是否会让聊天补全 API 走向过时；另一些人则指出 552B 的体量已让 “Flash” 的定位名不副实，并大幅提高了本地部署门槛。

**标签**: `#LLM`, `#DeepSeek`, `#model release`, `#AI research`, `#inference pricing`

---

<a id="item-3"></a>
## [Calif Research 演示 WeWorm：首个通过微信通话传播的零点击蠕虫](https://simonwillison.net/2026/Sep/10/calif-research/) ⭐️ 9.0/10

Calif Research 于 2026 年 9 月 8 日发布了 WeWorm 的演示，称其为首个可通过微信通话在 iOS 和 Android 上传播的零点击蠕虫，并在三台测试手机上演示了其自我传播过程。该团队表示，借助 AI，他们在约两天内就找到了漏洞并写出了首个远程代码执行（RCE）利用程序，随后又用一周时间构建出完整的蠕虫。 微信拥有远超十亿的用户规模，而一个仅凭普通来电、无需受害者任何交互即可自我传播的蠕虫，意味着极其庞大的潜在攻击面。更广泛地说，该团队声称 AI 将原本需要更大团队耗费数月的攻击性安全工作压缩到约九天，这标志着漏洞被发现和武器化的速度正在发生重大变化。 据 Calif Research 称，受害者无需接听电话，也无需对手机做任何操作，即便接听也听不到任何声音，而利用程序依然能够成功。目前公开的只是一个演示而非完整的技术披露，演示涉及三台测试手机，并被归入该公司标记为 Android 的研究条目中。

rss · Simon Willison · 9月10日 00:56

**背景**: 所谓“零点击”漏洞利用，是指无需受害者做任何操作即可运行的攻击，因此比需要打开文件或点击链接的攻击更难防御。蠕虫是一种能够自动从一台设备复制传播到另一台设备的恶意软件，而远程代码执行（RCE）意味着攻击者可以通过网络在目标设备上运行任意代码。微信通话在 iOS 和 Android 上均由庞大而复杂的客户端处理；Calif Research 想强调的更广泛意义在于，AI 辅助的漏洞发现已经在加快此类漏洞被发现并转化为可用利用程序的速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/09/wechat-zero-click-worm-took-over.html">WeChat Zero-Click Worm Took Over Accounts on iPhone and Android via Incoming Calls</a></li>
<li><a href="https://www.helpnetsecurity.com/2026/09/08/wechat-weworm-vulnerability-exploit-account-hijacking/">"Zero-click" WeChat worm could hijack accounts and spread via a single call - Help Net Security</a></li>
<li><a href="https://www.vulncheck.com/blog/ai-assisted-vulnerability-discovery">The First CVE Wave: Signs That AI-Assisted Vulnerability Discovery Is Reshaping Disclosure Volumes | Blog | VulnCheck</a></li>

</ul>
</details>

**标签**: `#security`, `#AI`, `#WeChat`, `#zero-click`, `#RCE`

---

<a id="item-4"></a>
## [研究者质疑能否放心将未发表的数学成果交给 OpenAI](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

Hacker News 上的一则讨论帖（约 373 分、466 条评论）围绕一个争议展开：有报道称 OpenAI 在私下与数学家合作时获取了思路，随后发表相关成果却未给予这些研究者署名，因此人们质疑是否还能信任 OpenAI。该讨论由 Mathstodon、X 和 Bluesky 上的帖子引发，其中包括 OpenAI 内部模型正快速解决开放问题、而与之交互的研究者却未获任何署名的说法。 署名与信任是学术合作的基础，如果研究者认为前沿实验室可以无偿汲取他们未发表的想法且不予署名，许多人可能会停止与 AI 模型或背后的实验室分享尚未完成的工作。这可能会重塑 AI 公司与科学界的合作方式，并加剧外界对更清晰的数据使用与信息披露政策的呼声。 争议的核心之一在于 OpenAI 据称声称产出该结果的模型并未在这些合作聊天记录上训练；有评论者认为两种说法可以同时成立：大模型可能在预训练阶段记住并内化了来自聊天的直觉，而针对可验证数学问题的强化学习则可能独立发现真正新颖的方法。另一些人则指出信息极度不对称——OpenAI 据称向大量研究者提供了免费模型访问权限，却对其内部模型和训练细节秘而不宣。

hackernews · pred_ · 9月10日 06:49 · [社区讨论](https://news.ycombinator.com/item?id=49639408)

**背景**: 大语言模型通常会先在海量文本（其中可能包含用户与聊天机器人的对话）上进行预训练，然后再用诸如“在答案可自动验证的问题（例如数学）上做强化学习”之类的技术进行优化。在学术界，未经署名使用他人未发表的想法被视为严重的不端行为，因此这场争论的关键在于：AI 系统是否算作合作者，以及模型能力的提升究竟来自记住的用户数据，还是来自模型自行发现的推理方法。

**社区讨论**: 整体情绪偏向对 OpenAI 的怀疑：nezi 等评论者将其类比为一位人类合作者，从同事那里获取想法、据此发表成果却不予署名，并称这种行为极不道德。sashank_1509 等人则认为两种解释可以并存——预训练可能内化了来自聊天的直觉，而在可验证数学问题上的强化学习也能发现与具体聊天无关的超人技巧；bertonvv 则公开质疑，考虑到研究者不断向其投喂新鲜数据，AI 究竟是真的在加速解决开放问题，还是只给人这种错觉。

**标签**: `#AI ethics`, `#OpenAI`, `#research attribution`, `#LLM training data`, `#AI policy`

---

<a id="item-5"></a>
## [Shopify 将移动应用从 React Native 迁回完全原生开发](https://shopify.engineering/back-to-native) ⭐️ 8.0/10

Shopify 工程团队发布文章宣布，将其移动应用从 React Native 迁回为 iOS 和 Android 分别进行的完全原生开发。这一决定发表在 shopify.engineering/back-to-native 上，随即成为当天 Hacker News 上讨论最激烈的工程类话题之一。 Shopify 是一家知名公司，它的这一“反向操作”与行业广泛采用跨平台框架的趋势相悖，因此成为观察 React Native 与原生开发真实取舍的重要案例。这也推动了一场更广泛的讨论：在 AI 生成原生代码的今天，跨平台框架原本承诺的成本优势是否依然成立。 Shopify 自身的文章侧重于工程层面的权衡，而非某个单一技术缺陷；而围绕它的讨论则强调，AI 辅助代码生成工具正越来越多地被用于把一个平台的移动应用改写到另一个平台。社区成员称，借助 Codex、Maestro 等工具可以很快完成中等规模应用（约 15 到 20 个页面）的迁移，但也指出最后的打磨环节仍需要人工投入。

hackernews · fnthawar2 · 9月10日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49643982)

**背景**: React Native 是由 Meta（当时的 Facebook）开发的开源 UI 框架，允许开发者用 JavaScript 和 React 为 iOS 与 Android 构建应用，并在两个平台间共享大部分代码。原生开发则意味着为每个平台分别编写代码，iOS 通常用 Swift 或 Objective-C，Android 通常用 Kotlin 或 Java，这能带来更好的性能和平台特性贴合度，但代价是要维护两套代码库。AI 辅助代码迁移利用大语言模型和编程智能体在不同语言与框架之间转换或重写代码，有望大幅减少这类改写所需的人工投入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/React_Native">React Native - Wikipedia</a></li>
<li><a href="https://reactnative.dev/">React Native · Learn once, write anywhere</a></li>
<li><a href="https://www.patternfly.org/ai/ai-assisted-development/ai-assisted-code-migration/">PatternFly • AI - assisted code migration</a></li>

</ul>
</details>

**社区讨论**: 该话题获得 573 分和 395 条评论，整体对 Shopify 的理由持接受态度：许多人认为跨平台还是原生的选择本质上取决于资源，属于普通工程决策，而非意识形态之争。有评论者指出，AI 代码生成削弱了 React Native 让 Web 开发者转做移动开发这一核心卖点；也有人分享了自己用 AI 辅助迁移的亲身经历，还有人提醒说这场争论已循环近二十年，始终没有放之四海而皆准的答案。

**标签**: `#React Native`, `#mobile development`, `#native apps`, `#Shopify`, `#engineering decisions`

---

<a id="item-6"></a>
## [索尼 PlayStation 数字游戏所有权诉讼引发关注](https://consumerrights.wiki/w/Sony_PlayStation_digital_game_ownership_lawsuit) ⭐️ 8.0/10

consumerrights.wiki 上一个记录索尼 PlayStation 数字游戏所有权诉讼的参考页面在 Hacker News 上引发大量讨论（302 分、99 条评论）。该页面转述的诉讼文件引用了 PlayStation 服务条款：第 14 节规定了强制仲裁协议和集体诉讼弃权条款，并要求不愿受其约束的用户在同意协议后 30 天内以书面形式通知索尼。 这场争议触及一个核心问题：当消费者在数字商店点击“购买”时，实际得到的究竟是什么；同时也考验仲裁条款能否在游戏行业中有效阻断集体法律救济。若索尼败诉，可能会推动主机平台在更广泛的数字媒体市场上给出更清晰的所有权表述或退款义务。 30 天的退出窗口期要求用户以书面形式通知索尼，这意味着绝大多数玩家在毫不知情的情况下就被默认约束，而仲裁同时也剥夺了陪审团审判权和参与集体诉讼的权利。诉讼文件还提出了一个引人注目的论点：两位原告分别在不同日期以 69.99 美元从 PlayStation Store 购买了同一款游戏《Resident Evil Requiem》，这与“购买即转让一份独占副本”的说法相矛盾。

hackernews · haunter · 9月10日 12:18 · [社区讨论](https://news.ycombinator.com/item?id=49642531)

**背景**: 数字商店出售的一般是使用许可而非实体副本，因此买方的权利由最终用户许可协议和服务条款界定，而不是由传统物权法决定。自 2011 年美国最高法院对 AT&T Mobility 诉 Concepcion 案作出判决以来，带有集体诉讼弃权的仲裁条款已成为科技与游戏行业服务条款的标准配置，使消费者极难提起集体诉讼。本案的核心问题在于：把交易标注为“购买”却在法律上将其视为可撤销的许可，是否构成欺骗。

**社区讨论**: 评论区普遍批评强制仲裁，有人认为它应当被彻底禁止，因为其唯一用途就是剥夺消费者和劳动者的权利。也有人用图书作类比，指出两个人各自拥有一本自己的书，但并非拥有同一本书；还有评论者认为索尼的辩护可能打开一扇索尼宁愿关着的法律大门。另有评论者对索尼态度矛盾，并以 2005 年的 rootkit 事件为例，认为这是一家庞大而笨拙、容易做出糟糕决定的公司。

**标签**: `#digital ownership`, `#consumer rights`, `#Sony PlayStation`, `#class action lawsuit`, `#arbitration clauses`

---

<a id="item-7"></a>
## [DeepSeek 发布 MIT 协议 Harness 框架，并开放 V4-Pro-0813 权重](https://t.me/zaihuapd/43738) ⭐️ 8.0/10

DeepSeek 发布了以 MIT 协议开源的智能体运行框架 DeepSeek Harness（dsh），其模型、工具、技能、会话、沙箱、存储、调度和 UI 全部实现为可替换插件；同时 DeepSeek-V4-Pro-0813 的权重也已在 Hugging Face 上开放。Harness 提供标准、PTC、极简和创造四种运行模式，并通过 npm 与 GitHub 分发。 这次发布为开发者提供了一套厂商中立、完全模块化的智能体构建栈，使 DeepSeek 直接对标 Claude Code 等成熟的编码智能体框架，同时允许团队自行替换模型、沙箱或 UI 层。在此基础上开放旗舰 V4-Pro 权重，进一步降低了自托管生产级智能体的门槛，也壮大了大型混合专家模型的开放权重生态。 在 PTC 模式下，Harness 保留标准模式的完整工具集，但通过生成的 SDK 和预留的 run_code 通道来暴露工具：嵌套调用会重新进入带完整保护的工具管线，安全调用可以并行重叠，独占调用充当顺序屏障，且副作用不会被回滚，因此 token 节省幅度取决于具体工作负载。根据 OpenRouter 的信息，DeepSeek-V4-Pro-0813 是一个大型混合专家模型，上下文窗口为 1,048,576 token，最大输出 393,216 token，价格约为每百万输入 token 0.99 美元、每百万输出 token 2.97 美元。

telegram · zaihuapd · 9月10日 07:28

**背景**: 所谓“智能体运行框架”（agent harness），是围绕语言模型的一层编排系统，负责决定模型如何调用工具、执行代码、管理会话以及对执行过程进行沙箱隔离——它正是“原始模型 API”与“可用的编码助手”之间的差别。DeepSeek Harness 采用“一切皆插件”的设计，上述每项能力都可以被替换或重新组合，而不是固化在框架里。所谓“开放权重”，是指训练好的参数被发布到 Hugging Face，任何人都可以下载、微调或自托管，而不必只能通过 API 调用。DeepSeek-V4-Pro-0813 是 V4-Pro 系列的正式版本，取代了此前的预览版，并着重强化了智能体能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">GitHub - deepseek-ai/deepseek-harness: DeepSeek Harness: Everything is a Plugin. · GitHub</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro-0813">deepseek-ai/DeepSeek-V4-Pro-0813 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#open-source`, `#LLM`, `#model-release`, `#AI-agents`

---

<a id="item-8"></a>
## [一篇随笔提出软件开发会把人逼疯的理论](https://graybeard.ing/software-drives-people-insane/) ⭐️ 7.0/10

博客 graybeard.ing 上发表的一篇随笔提出，软件开发这一工作本身就会把人逼疯，把日常工程中的种种痛苦描述为一种心理层面的伤害，而不仅仅是流程问题。这篇文章登上了 Hacker News 首页，获得约 350 分和 131 条评论。 这篇文章及其反响触及了整个行业更广泛的议题：开发者的职业倦怠、心理健康，以及随着团队扩张、与用户距离拉远而导致的工程文化退化。它的意义在于说出了许多工程师能感受到却很少表达出来的挫败感，同时评论区的讨论也给出了关于这份工作为何令人感到失衡的几种相互竞争的解释。 这篇随笔是观察性和轶事性的，而非实证研究，因此它所谓的“理论”更像是一种修辞框架，而不是可检验的论断；讨论中还补充了具体对比，例如 20 年前由二十多名开发者构建的关键任务实时交易系统，而其核心交易内核仅由四个人负责。评论者还引入了文章所低估的因素，包括自尊心（Ego）、管理结构，以及项目经理所扮演的中介角色。

hackernews · rglover · 9月10日 16:13 · [社区讨论](https://news.ycombinator.com/item?id=49646181)

**背景**: Hacker News 是一个读者众多的技术论坛，关于工程文化的随笔经常在这里成为讨论中心，而“这份工作让人发疯”这类文章也是一种反复出现的题材，常常引发关于开发者生活的争论。软件开发具有反馈周期长、进展不可见以及需求频繁变化等特点，这些条件在行业写作中常被与职业倦怠和压力联系起来。讨论还反映了关于团队规模的持续争论，因为许多工程师觉得，现代组织为同类项目配备的开发者人数远多于过去。

**社区讨论**: 评论者大体上接受这一前提，但对根源看法不一：bob1029 认为真正的推手是开发工作与用户脱节，因为与用户经常接触会大幅抑制这种“疯狂”，尤其是在团队被隔离在项目经理身后时。tcdent 认为其底层机制是人的自尊心（Ego）通过软件表现出来，并建议以还原论的禅宗态度对待职业创造力；hliyan 则指出，与 20 年前二十多名开发者就能构建关键任务实时交易系统的时代相比，如今的团队规模已大幅膨胀。anigbrowl 反驳说问题不在于软件，而在于大多数管理者并非开发者，这使他们处于和客户一样的位置——在不理解工作本身的情况下要求各种功能。

**标签**: `#software-engineering`, `#developer-culture`, `#mental-health`, `#burnout`, `#industry-commentary`

---

<a id="item-9"></a>
## [Cognition 发布 SWE-2 编程模型，宣称比肩 Fable 5.1 与 GPT-Astra](https://cognition.com/blog/swe-2) ⭐️ 7.0/10

Cognition 发布了编程专用模型 SWE-2，声称其能力可与 Anthropic 的 Fable 5.1 和 OpenAI 的 GPT-Astra 相抗衡，并说明该模型是在 Kimi K3 基座模型上进行后训练得到的。此次发布在 Hacker News 上引发大量关注（228 分、109 条评论），讨论焦点集中在所公布的基准分数究竟反映真实能力，还是属于对基准的过拟合。 这次发布在原本已十分拥挤的编程模型市场里又添了一个闭源权重的新玩家；而厂商可以仅通过在 Kimi K3 这类已有开放权重基座上做后训练，就宣称达到前沿级编程能力，说明开源与闭源模型之间的能力差距正在迅速收窄。这一趋势将对整个生态的定价、访问条件以及厂商自报基准的可信度形成压力。 最常被提及的疑点是两个基准之间的巨大分数落差：据称 SWE-2 在 Terminal Bench 2.1 上得分 92.8%，但在仅发布数周的 Terminal Bench 4 上只有 27.3%，这暗示其对新任务的泛化能力有限。该模型为闭源权重，除了「基于 Kimi K3 后训练」这一说明外，并未公开参数量或训练细节。

hackernews · seelos · 9月10日 15:29 · [社区讨论](https://news.ycombinator.com/item?id=49645443)

**背景**: SWE-bench 系列和 Terminal Bench 等编程基准用来衡量模型在沙箱环境中完成真实软件工程任务的能力；由于这些基准公开可用，模型可以针对它们专门调优，评论者将这种做法称为「刷榜」（benchmaxxing）。Fable 5.1 是 Anthropic 面向大型编程项目的旗舰模型，GPT-Astra 则是 OpenAI 的最新一代模型，二者已成为衡量新编程模型的参照物。开放权重与闭源权重的区别在此很关键：像 Kimi K3 这样的开放权重模型会公开可下载的参数，而闭源权重模型只能通过厂商托管的 API 访问；Cognition 用前者作基座、却以闭源形式交付，正是争议的来源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT -6 Astra - Wikipedia</a></li>
<li><a href="https://openk3.org/blog/open-weight-vs-closed-weight-models">Open Weight vs Closed-Weight Models: Key Differences | OpenK3</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论整体偏向怀疑：最主要的质疑是 Terminal Bench 2.1 与 Terminal Bench 4 上 92.8% 对 27.3% 的落差，被视为刷榜的证据；其次是没有任何迹象表明 SWE-2 是开放权重，有评论者质问既然如此为何不直接用 DeepSeek Flash 4.1。也有人提到 Cognition 过去演示的「自主完成 Upwork 任务」编程机器人经不起细看，但也承认基于本身已相当强大的 Kimi K3 做后训练，模型「不会差到哪里去」。另有一派批评则针对 Cognition 的 Devin 产品，称其是自己用过最一贯令人失望的工具。

**标签**: `#AI coding models`, `#LLM benchmarks`, `#closed-weight models`, `#Cognition`, `#HN discussion`

---

<a id="item-10"></a>
## [NASA 为火星开发的假彩色技术如今用于揭示地球上的隐藏岩画](https://gizmodo.com/this-nasa-color-trick-was-meant-for-mars-now-its-unveiling-rock-art-on-earth-2000809844) ⭐️ 7.0/10

一项最初为 NASA 火星探测任务开发的假彩色图像增强技术，如今被重新用于揭示地球上因风化而变得模糊的岩画，相关细节出自评论者所链接的一篇 NASA Spinoff 文章。该方法属于去相关拉伸（decorrelation stretch），能够放大肉眼无法察觉的细微颜色差异，使几乎看不清的岩刻变得清晰可辨。 这一跨界应用表明，行星科学中的成像处理流程可以被复用于地球上的考古与文化遗产保护，使研究人员无需接触遗址即可记录脆弱或偏远地点的岩画。它还降低了使用门槛，因为同样的效果可以在 GIMP 等免费工具中近似实现，从而鼓励更多人在遥感和图像分析领域进行尝试。 其核心算法是建立在主成分分析基础上的去相关拉伸，它消除通道之间的相关性并重新缩放方差，从而让颜色差异更加突出。有评论者指出，在 GIMP 中也能得到类似效果：先将图像分解为 LAB 分量，对 A、B 色度通道使用自动输入色阶以最大化对比度，然后再重新合成。

hackernews · gumby · 9月10日 15:29 · [社区讨论](https://news.ycombinator.com/item?id=49645437)

**背景**: 假彩色是一类渲染方法，它把在人眼可见光谱之外记录的数据映射为可见颜色，或重新组合可见光波段，使反射率存在差异的地物变得一目了然。NASA 长期以来将其用于火星图像处理，因为火星表面的细微变化在单一波段中很难被发现。去相关拉伸正是让这些差异凸显出来的具体增强手段，而多光谱卫星考古也基于同样的原理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/False_color">False color - Wikipedia</a></li>
<li><a href="https://www.mdpi.com/2227-7390/13/20/3297">Numerical Methods for Decorrelation Stretch - MDPI</a></li>
<li><a href="https://www.dstretch.com/DecorrelationStretch.pdf">Algorithm Theoretical Basis Document for Decorrelation ...</a></li>

</ul>
</details>

**社区讨论**: 评论者反应热烈，有人回忆说假彩色合成是自己理解信号与传感器时的一次“顿悟”时刻，并指出在这类图像中植被呈现红色而非绿色。不少人分享了实用技巧，包括一步步的 GIMP 操作流程、希望有可直接放入流水线的 ImageMagick 实现，以及一位用户讲述自己在吴哥窟用带通滤镜寻找隐藏岩画却未能成功、还因换滤镜用三脚架而被守卫阻止的经历。

**标签**: `#remote sensing`, `#image processing`, `#archaeology`, `#false color`, `#NASA`

---

<a id="item-11"></a>
## [Raymond Chen 揭秘 Windows XP 如何为你的初始用户头像挑选图片](https://devblogs.microsoft.com/oldnewthing/20260909-00/?p=112683) ⭐️ 7.0/10

在 2026 年 9 月发表于其 Old New Thing 博客的一篇文章中，微软工程师 Raymond Chen 解释说，Windows XP 并不是简单地取 Default Pictures 目录里的第一个文件，而是对目录列表执行了一次单遍随机选择例程。该代码使用以 GetTickCount() 当前值为种子的 RtlRandomEx 随机数生成器，并把扫描上限设为 100 张图片作为安全兜底。 这篇文章罕见地记录了一处未被文档化的 Windows 内部实现，也说明一个看似微不足道的功能背后仍需要围绕随机性和文件系统行为做出刻意的工程取舍。它的价值不在于改变今天的什么，而在于作为一个案例，展示已发布操作系统内部那些微小决策是如何做出、又如何被遗忘的。 Chen 指出该例程是一种单遍随机选择算法，因此无需先枚举并保存整个目录再挑选。它还会在抽样 100 张图片后停止，从而避免有人往 Default Pictures 目录里塞入上百万个文件时出现的病态行为；社区成员还贴出了 GitHub 上疑似对应的 Windows 泄露源码。

hackernews · soheilpro · 9月10日 09:04 · [社区讨论](https://news.ycombinator.com/item?id=49640646)

**背景**: Windows XP 引入了欢迎屏幕，每个用户账户都会配一张图片，而新建账户会自动从 Default Pictures 文件夹中随附的图片里分配一张。The Old New Thing 是 Raymond Chen 长期运营的微软博客，专门讲述 Windows 背后的历史与设计理由，这类文章面向的是那些好奇已发布软件为何如此行为的开发者。RtlRandomEx 是 Windows 运行时库中的伪随机数生成器，而 GetTickCount() 返回自系统启动以来经过的毫秒数，因此是一个方便但熵值很低的种子。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://devblogs.microsoft.com/oldnewthing/20260909-00/?p=112683">What algorithm did Windows XP use to choose your initial user picture ?</a></li>
<li><a href="https://aicrier.com/post/ttwhpyi9i21yl5cdxocy">Raymond Chen reveals Windows XP avatar algorithm — AICrier</a></li>

</ul>
</details>

**社区讨论**: 评论者大多把这篇帖子当成一份小惊喜：有人称赞 Raymond Chen 的 Windows 内幕文章犹如“小小的圣诞节”，也有人贴出了实际代码的 GitHub 链接。一个反复出现的主题是编程所需的思维转换——对人类而言随机挑一个东西轻而易举，对计算机却需要刻意的算法设计；还有读者感叹日常任务的压力会侵蚀那种能注意到此类细微问题的意识。

**标签**: `#Windows internals`, `#algorithms`, `#randomness`, `#software history`, `#Hacker News`

---

<a id="item-12"></a>
## [SemiAnalysis 解析数据中心表后供电难题](https://newsletter.semianalysis.com/p/what-is-so-hard-about-behind-the) ⭐️ 7.0/10

SemiAnalysis 发布了系列文章《What is So Hard About Behind-The-Meter Power For Datacenters?》的第一部分，探讨数据中心表后供电的技术与经济挑战。文章预告提到，2026 年迄今为止微软已签署超过 5GW 的表后铭牌容量，其中 2.7GW 来自雪佛龙（Chevron），另有远超 2GW 来自与 Crusoe 等公司签订的交钥匙数据中心租约。 AI 数据中心正消耗前所未有的电力，而电网并网延迟正推动运营商转向表后发电，以快速锁定容量。这一转变可能重塑能源采购、公用事业关系和数据中心运营，影响微软等超大规模企业、电力设备供应商以及本地电网。 文章指出，现场发电需要新的技能、运营模式和风险框架，而表后微电网往往先作为“过渡电力”运行，直到永久性电网互联可用。微软这 5GW 组合的完整拆解仅向 SemiAnalysis Energy Model 订阅者开放，且第一部分预告并未包含完整分析。

rss · Semianalysis · 9月10日 14:28

**背景**: 表后供电（behind-the-meter）是指电力在用户侧电表之后产生并消耗，不经过公共输配电网络。数据中心传统上依赖电网供电加备用发电机，但 AI 工作负载需要大规模、持续稳定的容量，而紧张的电网未必能按时提供。因此，运营商越来越多地与能源和基础设施公司签署现场天然气、燃料电池、微电网以及交钥匙供电安排。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/what-is-so-hard-about-behind-the">What is So Hard About Behind-The-Meter Power For Datacenters ...</a></li>
<li><a href="https://www.datacenterknowledge.com/energy-power-supply/why-data-centers-produce-their-own-power">Why Data Centers Are Turning to Behind-the-Meter Power</a></li>
<li><a href="https://www.williams.com/2026/03/17/powering-data-centers-behind-the-meter-power-explained/">Powering data centers: behind-the-meter power, explained</a></li>

</ul>
</details>

**标签**: `#datacenters`, `#energy`, `#power infrastructure`, `#AI infrastructure`, `#behind-the-meter`

---

<a id="item-13"></a>
## [真实果蝇连接组学不会打乒乓球，审计揭出流水线缺陷](https://www.reddit.com/r/MachineLearning/comments/1wc67ci/i_tried_to_make_a_real_fly_connectome_learn_to/) ⭐️ 7.0/10

一位机器学习实践者尝试用类多巴胺可塑性，让真实 MaleCNS v1.0 果蝇连接组（16.6 万个电子显微镜重建神经元）的一个小子图学会追踪乒乓球，结果完全没有学会——在多个随机种子下，开启学习与关闭学习的运行结果逐比特完全一致。追查原因时发现了 neuPrint 的正则匹配缺陷（全匹配与子串语义混淆），它静默地把两个完整神经元群清零；原始神经元选择中从光感受器到其他节点根本不存在通路；并且在 4 个可用运动神经元中，有一半与任何感觉通路之间的突触数为零。 经过细致审计的负面结果既稀缺又有价值，这一案例是对近期病毒式传播的“果蝇大脑玩《毁灭战士》/《我的世界》/《节奏光剑》”演示的直接反例——据作者所述，这些项目自己的仓库就承认未通过验证门槛、真实运动检测通路保持静默、行为是手工注入的，以及过拟合到单条曲目。它提醒人们，基于连接组的智能体需要可复现性检验，而不能只看在宽容的游戏引擎里看起来像那么回事的运动输出。 被数据证伪的电路假设是一条与求偶追逐相关的视觉目标追踪通路；在改为围绕一个真正端到端连通的下降神经元重建电路后，开启与关闭学习的结果终于出现分叉——但效果更像是学习规则把整个系统整体“压静”，因为失误多于命中，惩罚项占主导，从而压缩了运动响应，而不是产生任何技能提升。作者也指出，实验范围只是一个小子图，并非可泛化的结论，并邀请其他人认真模拟中央复合体与转向回路。

reddit · r/MachineLearning · /u/oPeraza2007 · 9月10日 02:28

**背景**: 连接组（connectome）是从电子显微镜图像中逐神经元重建出的接线图；MaleCNS v1.0 是 Janelia FlyEM 发布的完整成年雄性果蝇中枢神经系统，包含约 16.6 万个神经元，通过 natverse 的 malecns R 包分发，并可通过 Janelia 的连接组学查询工具 neuPrint 的网页界面与 API 访问。类多巴胺可塑性指的是由奖励或惩罚信号门控的突触权重更新，类似强化学习。之所以选择乒乓球作为测试平台，正是因为其“命中/未命中”的二值信号让人无处掩藏无效结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://male-cns.janelia.org/">Male CNS Connectome - MaleCNS connectome</a></li>
<li><a href="https://github.com/natverse/malecns">GitHub - natverse/malecns: Access to the latest 'Janelia ...</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC9350508/">neuPrint: An open access tool for EM connectomics - PMC</a></li>

</ul>
</details>

**标签**: `#connectome`, `#computational-neuroscience`, `#reinforcement-learning`, `#reproducibility`, `#negative-results`

---

<a id="item-14"></a>
## [蚂蚁国际联合 Visa 与 Mastercard 制定 AI 代理支付标准](https://www.cnbc.com/2026/09/10/ant-international-visa-mastercard-ai-agent-payment-standard.html) ⭐️ 7.0/10

蚂蚁国际宣布与 Visa、Mastercard 展开合作，共同为 AI 代理支付制定通用标准，并建立“了解你的代理”（Know Your Agent，KYA）机制，将代理与有效的法律实体关联、评估其行为并监测风险。三方援引麦肯锡的预测称，到 2030 年 AI 代理可能处理全球消费者商业交易中的 3 万亿至 5 万亿美元。 如果全球最大的三家支付参与方能够就同一套规则达成一致，那么在某一支付机构注册的 AI 代理就可以跨机构完成交易而无需重复注册，这将消除自主商业的一大摩擦点。这也表明传统卡组织希望主导代理支付的发展方向，而不是把这一领域让给加密原生或单一平台自有的协议。 这一消息属于标准与合作伙伴层面的倡议，而非已落地的产品，目前尚未公布技术规范、时间表或治理结构。互操作性被描述为让已在某家支付机构注册的代理无需在其他机构重复注册；KYA 则被定位为与面向人类的 KYC、反洗钱等合规体系并行的机制。

telegram · zaihuapd · 9月10日 03:00

**背景**: AI 代理是指能够代替用户浏览、议价并完成支付的软件程序，但与真人不同，它们没有护照、出生证明或地址，因此商户和支付网络缺乏明确手段来确认某个代理是否合法且获得授权。“了解你的代理”（KYA）正是为此兴起的身份标准：在授权支付之前，核实代理的身份、回溯到控制它的人类或组织的委托链路，以及它被授予的消费额度。目前已有多个竞争性方案，例如 Google 于 2025 年 9 月发布的代理支付协议 AP2，以及 Chainlink 面向跨网络代理交易的互操作性方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.cryptonomist.ch/2026/09/10/ai-agent-payment-standards/">AI Agent Payment Standards Set by Visa, Mastercard, Ant</a></li>
<li><a href="https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol">Announcing Agent Payments Protocol (AP2) | Google Cloud Blog</a></li>
<li><a href="https://skyfire.xyz/know-your-agent-kya/">Know Your Agent ( KYA ) - Skyfire</a></li>

</ul>
</details>

**标签**: `#AI Agents`, `#Payments`, `#Fintech`, `#Standards`, `#Industry News`

---

<a id="item-15"></a>
## [月之暗面（Kimi）保密递交港股 IPO 申请，投前估值 500 亿美元](https://t.me/zaihuapd/43743) ⭐️ 7.0/10

Kimi 的开发商月之暗面已以保密形式向港交所递交 A1 文件，正式启动港股 IPO，公司回应称暂无信息可披露。与此同时，公司正以 500 亿美元投前估值推进新一轮融资，这可能是其 IPO 前的最后一轮融资。 若成功上市，月之暗面将成为首批登陆公开市场的中国大模型独角兽之一，为投资者评估中国大模型创业公司提供一个难得的公开估值标尺。其估值在半年内暴涨约 8 倍也推高了同行的竞争门槛，外界预计另一家头部大模型公司 DeepSeek 可能于明年上半年上市。 A1 文件是赴港上市的首份申请文件，由于此次为保密递交，详细财务数据并未公开，月之暗面也拒绝置评。据该报道，公司估值从 2025 年底约 43 亿美元升至今年 7 月投后 350 亿美元，同时其在 1 至 7 月先后上线 K2.5、K2.6、K3，保持约三个月一次的迭代节奏。

telegram · zaihuapd · 9月10日 10:58

**背景**: 月之暗面是中国一家人工智能公司，开发 Kimi 助手以及 Kimi 系列开源权重（open weights）大语言模型，其模型支持图像与视频多模态输入，并提供 Swarm 多子智能体等智能体功能。在香港，企业需向港交所递交 A1 文件才能正式启动上市申请，而保密递交允许公司在细节公开前先试探市场反应；“投前估值”指在新资金注入之前公司的估值。DeepSeek 是另一家中国开源权重前沿模型开发商，总部位于杭州、由对冲基金幻方量化（High-Flyer）支持，被普遍视为下一家可能上市的中国头部大模型公司。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_(AI)">Kimi (AI) - Wikipedia</a></li>
<li><a href="https://www.kimi.com/">Kimi AI 官网- K3 上线，专为智能体编程与知识工作打造</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek</a></li>

</ul>
</details>

**标签**: `#AI Industry`, `#IPO`, `#Moonshot AI/Kimi`, `#LLM`, `#China Tech`

---

<a id="item-16"></a>
## [腾讯混元开源统一音频编辑模型 AuK](https://x.com/TencentHunyuan/status/2097996926876795197) ⭐️ 7.0/10

腾讯混元正式发布开源音频编辑模型 AuK，通过统一的自然语言指令接口完成零样本文本转语音、音色/风格/情绪编辑、去口音以及多人语音分离等任务。同时还发布了 AuK-Flash 蒸馏版本，采用 4 步推理，官方称在匹配条件下速度约提升 4.5 倍，代码、模型权重和演示均已上线。 AuK 把过去彼此独立的 TTS、音色转换、语音增强与音源分离等多个语音工具整合进同一个开源权重模型，降低了开发者原本需要拼接多家闭源 API 的门槛。来自大厂、采用宽松许可证且可本地部署的模型，也会进一步加剧与闭源语音厂商以及其他开源语音项目的竞争。 AuK 是一个参数规模约 1.5B 的紧凑模型，采用 MIT 许可证发布；其蒸馏版 AuK-Flash 不使用无分类器引导（classifier-free guidance），以此实现 4 步生成。模型检查点包含扩散 Transformer 与层融合权重，而 MLLM 编码器和 VAE 在运行时从单独文件加载，因此检查点加载时出现 text_encoder.* 键缺失属于预期现象，并非错误。

telegram · zaihuapd · 9月10日 11:56

**背景**: 零样本 TTS 指模型无需针对特定说话人做微调，仅凭一小段参考音频即可克隆或合成其声音。基于扩散的语音模型通常需要数十步去噪才能生成音频，速度较慢；蒸馏则把这一过程压缩到几步，用一定的质量损失换取低延迟。过去，语音生成、编辑、增强、分离这些能力分属不同的专用模型，各自拥有独立的接口与权重。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Tencent-Hunyuan/AuK">Tencent-Hunyuan/AuK: AuK: An Open-Source Foundational Model for...</a></li>
<li><a href="https://auk-project.github.io/">AuK — An Open-Source Foundational Model for Speech Generation...</a></li>
<li><a href="https://www.orcarouter.ai/blog/auk-flash-open-source-release">AuK-Flash & AuK: Tencent's Quiet Open-Source Speech Model</a></li>

</ul>
</details>

**标签**: `#audio-editing`, `#text-to-speech`, `#open-source-models`, `#Tencent-Hunyuan`, `#speech-generation`

---

<a id="item-17"></a>
## [PlanetScale 推出闭源 Postgres 分片产品 Neki](https://planetscale.com/blog/introducing-neki) ⭐️ 6.0/10

PlanetScale 在其官网博客发文推出了面向 Postgres 的数据库分片方案 Neki。但这一发布引发了社区的两极反应，主要原因在于文章始终没有清楚说明 Neki 到底是什么、用来做什么，而且该产品是闭源的。 PlanetScale 是知名度很高的托管数据库厂商，它进军 Postgres 分片领域，说明让 Postgres 突破单节点上限的工具正在成为竞争热点。而 Neki 选择闭源，与 Supabase 开源的 multigres 形成鲜明对立，使这次发布成为开源与专有数据库基础设施之争的一个焦点事件。 根据 PlanetScale 的文档，Neki 为 Postgres 提供水平分片，并附带零停机运维、在线 DDL、复制工作流和集群管理能力，且运行的是原生 Postgres 而非分支版本。关键的注意事项在于可用性与授权：Neki 是闭源的，评论者还指出，其发布策略似乎已从此前暗示会开源的立场发生了变化。

hackernews · simon_weber · 9月10日 15:43 · [社区讨论](https://news.ycombinator.com/item?id=49645686)

**背景**: PlanetScale 是一个关系型数据库平台，以基于 Vitess 分片系统构建的无服务器 MySQL 服务而知名，近年也扩展到了 Postgres。分片是一种数据库架构模式，把庞大的数据集切分成称为“分片”的小块并分布到多台机器上，从而让系统突破单节点数据库的处理上限。手工实现分片出了名的困难，这也是托管式分片产品对运行大规模 Postgres 的团队很有价值的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://planetscale.com/docs/neki">Neki - PlanetScale</a></li>
<li><a href="https://planetscale.com/docs/postgres/sharding">Horizontal sharding for Postgres - PlanetScale</a></li>
<li><a href="https://aws.amazon.com/what-is/database-sharding/">What is Sharding? - Database Sharding Explained - AWS</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（155 分、62 条评论）更多是针对发布方式本身的批评，而非技术讨论。评论者抱怨整篇发布文章始终没说清楚 Neki 是什么，指责 CEO 一边贬低 Supabase 开源的 multigres、一边推出闭源竞品，并反复追问 Neki 是否会开源；也有人批评 CEO 的语气。

**标签**: `#databases`, `#sharding`, `#PlanetScale`, `#open-source`, `#distributed-systems`

---

<a id="item-18"></a>
## [.blend URL Viewer：在浏览器中直接预览 Blender 文件](https://simonwillison.net/2026/Sep/9/blender-viewer/) ⭐️ 6.0/10

Simon Willison 发布了一个名为“.blend URL Viewer”的网页工具，用户只需粘贴一个支持 CORS 的链接或 GitHub 链接，就能在浏览器里直接渲染 Blender 的 .blend 文件；同时他还展示了配套实验：先用 ChatGPT Images 2.5 生成一张以美剧《Pluribus》为主题的法贝热彩蛋图片，再让 Codex 中的 GPT-6 Astra 把它转成 Blender 模型，整个过程耗时 17 分 51 秒。 这个工具把 .blend 文件变成任何人都能用一条链接打开的网页内容，无需安装 Blender，从而降低了 3D 资产的分享门槛；而配套实验则显示，智能体式大模型工作流已经能够仅凭一段提示词加一张图片，产出可用的 3D 内容。 该查看器对 Blender 5.x 文件支持最好，能渲染网格几何体以及近似材质、灯光和已保存的相机机位，并提供环绕控制、线框模式和“适配视图”按钮，但会忽略未应用的修改器、文字也仅为近似显示；GitHub 链接通过 jsDelivr 解析，演示用的 Pluribus 彩蛋模型为 7.2 MB，包含 387 个网格、783,764 个顶点、1,446,560 个三角面和 17 种材质。

rss · Simon Willison · 9月9日 23:58

**背景**: .blend 是 Blender 的原生工程文件格式，通常必须用桌面版软件才能打开，因此浏览器端查看器需要借助 WebGL 之类的渲染技术来直接显示几何体。GPT-6 Astra 是 OpenAI 于 2026 年 9 月 3 日发布的大语言模型，ChatGPT Images 2.5 则是 OpenAI 在 2026 年 9 月 8 日推出的图像生成升级版本。Willison 的这套流程还依赖一个智能体“技能（skill）”文件，即一份可复用的说明文档，用来告诉编码智能体如何在本地操作 Blender。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Sep/9/blender-viewer/">Tool: .blend URL Viewer</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra - Wikipedia</a></li>
<li><a href="https://9to5mac.com/2026/09/08/openai-releases-chatgpt-images-2-5-with-sharper-details-and-more-precise-editing/">OpenAI releases ChatGPT Images 2.5 with ‘sharper ... - 9to5Mac</a></li>

</ul>
</details>

**标签**: `#Blender`, `#3D modeling`, `#AI image generation`, `#web tools`, `#Simon Willison`

---

<a id="item-19"></a>
## [348M 参数模型仅用 22.7B token 训练，靠展示运算步骤完成 14 位算术](https://www.reddit.com/r/MachineLearning/comments/1wc7hmu/i_trained_a_348m_model_trained_from_scratch_on/) ⭐️ 6.0/10

一位个人开发者发布了其第五个从零训练的小型语言模型：348M 参数、22.7B token，随后被微调成一个数学模型，通过显式输出逐列运算步骤（进位、借位链、部分积）来解题。该模型在 GPT-3 的九个算术子任务上平均得分 99.4%，其中 5 位数加法和 2 位数乘法达到 100%，而 GPT-3 175B 在少样本直接作答下的成绩分别只有 9.3% 和 29.2%。 这是一个很有说服力的数据点：参数规模约为 GPT-3 175B 五百分之一的 348M 模型，竟能在纯算术任务上全面碾压前者——靠的不是规模，而是把解题步骤直接训练进模型，而非在推理时依赖少样本提示。这进一步支持了「推理轨迹（chain-of-thought）对小型模型是关键承重结构」的观点，也说明算术能力与更广泛的应用题推理能力是彼此分离的。 报告称，仅把位值名称表从 6 项（`ones`…`hundred-thousands`）扩展到 19 项，干净加法的上限就从 8 位数提升到 14 位数；模型此前已自行泛化出 `millions` 和 `ten-millions`，而这两个名称在训练样本中出现次数为零，且在 9 位数时它并非算错，而是直接漏掉了一整列。局限包括：必须使用贪婪解码（采样会在链条中途破坏列式计算流程）、完全不支持除法、4×4 乘法是硬性天花板、应用题表现很差（GSM8K 仅 4%，ASDiv 16.5%），失败原因在于「运算选择」而非计算本身，作者也主动指出其算术测试框架对减法操作数做了排序处理。

reddit · r/MachineLearning · /u/nkthebass · 9月10日 03:28

**背景**: GPT-3 算术基准由九个子任务组成（不同位数的加法、减法和乘法），模型只看到少量示例就必须直接给出答案，既不能用计算器，也不能写中间步骤；在这种设定下，大模型一旦超过 3–4 位数就常常性能断崖式下跌。2022 年流行起来的 chain-of-thought（思维链）提示则鼓励模型在作答前先输出中间推理步骤，从而显著提升多步推理能力。这个项目把该思路又推进了一步：不是靠提示临时激发，而是把逐列算术步骤直接训练进一个小模型里。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chain-of-thought_prompting">Chain-of-thought prompting</a></li>
<li><a href="https://www.promptingguide.ai/techniques/cot">Chain-of-Thought Prompting | Prompt Engineering Guide</a></li>
<li><a href="https://llm-stats.com/benchmarks">AI & LLM Benchmarks 2026: Rankings, Scores & Results</a></li>

</ul>
</details>

**标签**: `#LLM`, `#arithmetic reasoning`, `#small language models`, `#chain-of-thought`, `#benchmarks`

---

<a id="item-20"></a>
## [ChatGPT 语音模式新增 GPT-5.6 Sol 与 GPT-6 Astra 模型选择](https://x.com/athyuttamre/status/2097761052939125132) ⭐️ 6.0/10

一条转述 OpenAI 的 Atty Eleti 消息的 Telegram 帖文称，ChatGPT 语音模式现已支持用户手动选择 GPT-5.6 Sol 或 GPT-6 Astra 模型，并可配置 effort 档位。该转述称 Pro 用户可使用这两个选项，语音在需要搜索或推理时会调用所选模型。 语音模式此前是单一模型、不可见的体验，开放模型选择与 effort 控制意味着用户在免手操作的界面里也能获得与文本对话相同的调节能力。这也表明 OpenAI 愿意把 Pro 档的语音流量路由到最新、成本最高的前沿模型，从而影响人们对新模型多快覆盖所有入口的预期。 该消息只是简短的二手转述，没有基准测试、延迟数据、上线时间或覆盖地区，因此两个模型在语音场景下的实际差异并未被量化。它描述的是对已有模型的分级访问而非新模型发布；在 OpenAI 的 API 中，底层的 reasoning effort 参数按模型不同可取值 none、minimal、low、medium、high、xhigh 和 max。

telegram · zaihuapd · 9月10日 00:20

**背景**: GPT-5.6 Sol 是 OpenAI GPT-5.6 系列中能力最强的版本，该系列还包括 Luna 和 Terra，在面向可信合作伙伴的有限预览之后于 2026 年 7 月 9 日正式发布。GPT-6 Astra 于 2026 年 9 月 3 日发布，是 OpenAI 的下一代旗舰模型，官方称其在电脑操作、浏览、软件工程、网络安全、科学和专业工作等方面达到业界领先水平。推理强度（reasoning effort）是告诉模型在一项任务上投入多少内部思考的设置，用于在延迟与成本和回答质量之间做权衡；而 Sol 与 Astra 这类能力档位则决定由哪个模型来完成任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6_Sol">GPT-5.6 Sol</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra - Wikipedia</a></li>
<li><a href="https://developers.openai.com/api/docs/guides/reasoning">Reasoning models | OpenAI API</a></li>

</ul>
</details>

**标签**: `#ChatGPT`, `#OpenAI`, `#语音模式`, `#模型选择`, `#AI产品更新`

---

<a id="item-21"></a>
## [HBM 短缺致中国 AI 芯片涨价 20%—50%](https://www.reuters.com/world/asia-pacific/chinas-ai-chipmakers-raise-prices-high-bandwidth-memory-shortage-bites-2026-09-10/) ⭐️ 6.0/10

受全球高带宽存储器（HBM）供应紧张影响，华为、寒武纪等中国 AI 芯片厂商已开始上调产品价格。华为昇腾 950DT 的报价较两个月前上涨约 20%—50%，部分老款芯片涨幅约 30%；寒武纪新一代思元 690 的价格也预计上涨约 20%—30%。 这轮涨价说明制约中国国产 AI 算力扩张的关键瓶颈已从计算逻辑芯片转向存储器，直接推高了训练与推理集群的建设成本。同时也凸显美国出口限制的连带效应：中国企业无法自由采购 SK 海力士、三星、美光的 HBM，只能转向成熟度较低的国产替代方案。 HBM 是通过 3D 堆叠 DRAM 实现的高带宽内存，用于为 AI 加速器的计算单元持续供数。值得注意的是，有报道称华为昇腾 950DT 采用自家设计的 HBM，容量 144 GB、带宽接近 4 TB/s，这一规格高度依赖国产存储的良率与产能。

telegram · zaihuapd · 9月10日 09:29

**背景**: 高带宽存储器（HBM）是一种先进内存接口，将多颗 DRAM 芯片垂直堆叠并通过硅通孔互连，最初由三星、AMD 和 SK 海力士联合开发。它诞生的原因是传统内存带宽无法跟上 GPU、NPU 等 AI 加速器的数据吞吐需求。HBM 目前仅由 SK 海力士、三星和美光三家供应，是 AI 供应链中集中度最高的环节之一。因此，华为昇腾、寒武纪思元等中国 AI 芯片设计厂商既要面对来自英伟达的全球 HBM 需求竞争，又要承受限制其获取先进存储的美国出口管制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://www.techpowerup.com/forums/threads/huawei-prepares-160-000-ascend-950dt-accelerators-for-deepseek-data-center.352416/">Huawei Prepares 160,000 Ascend 950 DT ... | TechPowerUp Forums</a></li>
<li><a href="https://www.techradar.com/pro/could-cambricon-create-a-deepseek-moment-in-ai-hardware-the-rise-of-chinas-answer-to-nvidia-has-been-nothing-short-of-meteoric-but-is-it-too-good-to-be-true">Cambricon’s Siyuan 690 is designed to rival Nvidia’s H100 but ...</a></li>

</ul>
</details>

**标签**: `#HBM`, `#AI chips`, `#semiconductor supply chain`, `#China tech`, `#Huawei Ascend`

---