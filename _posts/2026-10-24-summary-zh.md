---
layout: default
title: "Horizon Summary: 2026-10-24 (ZH)"
date: 2026-10-24
lang: zh
---

> 从 34 条内容中筛选出 13 条重要资讯。

---

1. [月之暗面发布 Kimi K3.1 Pro 与 Highspeed，权重将于 11 月 4 日开放](#item-1) ⭐️ 8.0/10
2. [安全研究团队演示可用的 iPhone 漏洞利用](#item-2) ⭐️ 8.0/10
3. [SemiAnalysis：AWS Trainium 从推理芯片转型为可信的 AI 训练平台](#item-3) ⭐️ 8.0/10
4. [PHP 紧急发布补丁，修复两个 CVSS 9.2 级远程代码执行漏洞](#item-4) ⭐️ 8.0/10
5. [本地维基百科：维基百科，但只涵盖距你步行半小时内的事物](#item-5) ⭐️ 7.0/10
6. [EFF 警告：加拿大人反对 C-22 法案的时间所剩无几](#item-6) ⭐️ 7.0/10
7. [群体模仿被证明等价于单个带臂老虎机学习智能体](#item-7) ⭐️ 7.0/10
8. [字节跳动发布 Seedance 2.5 视频模型，单次可生成 30 秒](#item-8) ⭐️ 7.0/10
9. [据称 iPhone 18 Pro 实现重启后仍保留的非绑定越狱](#item-9) ⭐️ 7.0/10
10. [国办发文：要求减缓人工智能应用对就业的替代影响](#item-10) ⭐️ 7.0/10
11. [失业与可的松引发的躁狂：一篇引发共鸣的个人随笔](#item-11) ⭐️ 6.0/10
12. [LLM 记忆或许更需要遗忘而非更大回忆容量](#item-12) ⭐️ 6.0/10
13. [微软悄然测试 Project Pantheon：用户自选记忆的 Recall 替代品](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [月之暗面发布 Kimi K3.1 Pro 与 Highspeed，权重将于 11 月 4 日开放](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

月之暗面于 2026 年 10 月 24 日发布 Kimi K3.1 Pro，这是全新 K3.1 系列的首款模型，同时还推出了速度更快的伴生版本 Kimi K3.1 Pro Highspeed。两款模型即日起在 Kimi.ai、Kimi Work、Kimi Code 和 Kimi API 上线，完整模型权重承诺将在 11 月 4 日前开放。 Kimi K3.1 Pro 在 Artificial Analysis 智能指数上取得 55 分，位列总榜第四，超过 GPT-6 Astra 与 Fable 5.1 且速度更快，使一款中国开源权重模型真正跻身前沿竞争者行列。计划中的权重开放也加剧了开源与闭源之争：一款接近前沿水平的模型可供下载，将重塑开发者可自行部署的能力边界以及安全框架需要应对的风险。 K3.1 Pro 是在 Kimi K3 基础上经过后训练得到的版本，后训练算力大幅增加；月之暗面表示其攻击性网络能力被有意控制在自身流水线可达到的水平之下，并落后于前沿闭源模型，未来将逐步提升开放权重中的网络能力。在智能指数评测中它生成了 1.5 亿 token，而中位数仅为 8700 万，说明其推理风格明显更为冗长。

hackernews · Jowsey · 10月23日 16:59 · [社区讨论](https://news.ycombinator.com/item?id=50212065)

**背景**: Kimi 是中国 AI 公司月之暗面（Moonshot AI）的模型系列，该公司早期以长上下文模型著称，近来越来越聚焦于编程与智能体（agent）任务。后训练指基础预训练之后的微调与强化学习阶段，近期推理与工具调用能力的提升大多来自这一阶段。开放权重模型指参数可以下载并在本地运行的模型，一旦发布，安全护栏便难以强制执行。讨论中反复出现的模型蒸馏，是指用更大教师模型的输出或信号训练一个更小的学生模型，以便以更低成本模仿其行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.unite.ai/moonshot-ai-releases-kimi-k3-1-pro-first-model-in-new-k3-1-series/">Moonshot AI Releases Kimi K3.1 Pro, First Model in New K3.1 ...</a></li>
<li><a href="https://www.kimi.ai/blog/kimi-k3-1-pro">Kimi K3.1 Pro Tech Blog: Advancing Open Intelligence</a></li>
<li><a href="https://snorkel.ai/blog/llm-distillation-demystified-a-complete-guide/">LLM distillation demystified: a complete guide | Snorkel AI</a></li>

</ul>
</details>

**社区讨论**: 评论者的态度在热情与质疑之间分化：一位用户质疑现实中如何蒸馏一个 1–2TB 的闭源前沿模型，另一位则称自己订阅的每月 99 美元套餐在单次会话开始 47 分钟内就触发了 5 小时配额上限。还有人聚焦安全策略，指出月之暗面承认自己有能力构建更强的网络能力却选择不发布，并称赞其逐步提升开放权重网络能力的“温水慢煮”式做法。

**标签**: `#AI models`, `#Kimi`, `#open weights`, `#AI safety`, `#LLM`

---

<a id="item-2"></a>
## [安全研究团队演示可用的 iPhone 漏洞利用](https://blog.calif.io/p/iphone) ⭐️ 8.0/10

一支安全研究团队发布了题为《今天，我们攻破了原本就想攻破的目标：iPhone》的文章，展示了一条针对苹果 iOS 的完整漏洞利用链。该帖在 Hacker News 上获得约 587 分和近 400 条评论，从内容看更像是一次概念验证演示，而非释放可直接武器化的攻击工具。 iOS 是受到最严密审计和加固的消费级平台之一，因此一条被成功演示的漏洞利用链对评估移动安全现状具有重要参考价值。围绕它的讨论还涉及：AI 辅助漏洞发现是否正在成为那些能负担前沿模型的实验室与厂商的决定性优势。 已公开的内容属于演示性质，并非已发布的产品，也未见对应 CVE 编号；摘要还指出，这项工作中至少有一部分可能依赖了 AI 辅助的漏洞发现。评论者特别追问，苹果的 Lockdown 模式（会限制信息附件、网页技术和有线连接）能否真正阻断演示中所用的手法，而原文似乎并未给出明确答案。

hackernews · pavel_lishin · 10月23日 16:21 · [社区讨论](https://news.ycombinator.com/item?id=50211474)

**背景**: Lockdown 模式是 iOS 上一个需要用户主动开启的可选设置，它大幅压缩攻击面，例如拦截大多数信息附件类型、在 Safari 中禁用 JavaScript 即时编译、并拒绝通过有线连接外设，目的是抵御 Pegasus 这类高度定向的间谍软件。此前的 iOS 漏洞利用链——尤其是 Project Zero 披露的 ForcedEntry——往往把恶意 PDF 或图片解析漏洞与沙箱逃逸串联起来，这也是评论者把 PDF 视作反复出现的薄弱环节的原因。与此同时，前沿 AI 实验室越来越多地通过“可信网络访问”或红队项目来限制最强模型的可用范围，这直接决定了谁能开展此类研究。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.apple.com/en-us/105120">About Lockdown Mode - Apple Support</a></li>
<li><a href="https://www.bitdefender.com/en-us/blog/hotforsecurity/what-is-lockdown-mode-iphone-mac-spyware-when-use-it">Apple’s Lockdown Mode Explained: What It Does, Who Needs It ...</a></li>
<li><a href="https://cloud.google.com/blog/topics/threat-intelligence/vulnerability-discovery-and-exploitation-trends-in-the-ai-era">Vulnerability Discovery and Exploitation Trends in the AI Era</a></li>

</ul>
</details>

**社区讨论**: 社区情绪既有对演示的赞叹，也有对生态现状的不满。多位评论者惋惜折腾文化的消逝，指出如今越狱可能导致被 iCloud 和 iMessage 拒之门外；也有人认为，把前沿模型的访问权限只开放给“圈内人”，使这些项目变成了“护城河而非安全保障”。一个反复出现的问题是 Lockdown 模式能否有效缓解这类攻击；还有评论者打趣说，视频里少了跳舞的动漫女孩和电子舞曲，观感大打折扣。

**标签**: `#security`, `#iOS`, `#exploit-research`, `#AI-red-teaming`, `#mobile-security`

---

<a id="item-3"></a>
## [SemiAnalysis：AWS Trainium 从推理芯片转型为可信的 AI 训练平台](https://newsletter.semianalysis.com/p/amazons-trainium-takes-a-strike-at) ⭐️ 8.0/10

SemiAnalysis 发布深度分析文章，认为亚马逊的 Trainium 已从以推理为主的加速器，演进为一个可信的 AI 训练平台。文章重点提到了 Trainium 上的原生 PyTorch 支持、高质量的持续集成（CI）、与 TorchTitan 的集成，以及被作者称为“GPU 不可能实现”的性能剖析工具。 训练是 AI 加速器市场中要求最高、利润最丰厚的环节，而英伟达在该领域的统治地位不仅靠芯片，也靠软件生态（CUDA、PyTorch 工具链）。如果 Trainium 真能凭借完善的工具链顺畅运行主流 PyTorch 训练负载，AWS 就能在成本上对英伟达 GPU 形成更有力的竞争说辞，并为大型云客户提供真正可选的第二家训练算力供应商。 其核心主张是 Trainium 现在可以原生支持 PyTorch，而无需大量重写计算图，并辅以完善的 CI 以避免框架和算子悄然失效，同时提供基于 TorchTitan 的大规模分布式训练方案。由于目前只有简短的摘要，具体的基准测试数字、支持的模型规模以及与英伟达硬件相比仍存在的局限，在现有内容中并未详细说明。

rss · Semianalysis · 10月23日 19:06

**背景**: Trainium 是亚马逊自研的 AI 芯片系列，目标是在 AWS 数据中心内的训练和推理场景中提供优于 GPU 实例的性价比；亚马逊宣称相比同类 EC2 实例最多可节省约 50% 的训练成本，并将其用于与 Anthropic 的合作中。从历史上看，自研加速器的短板往往不在算力，而在软件：开发者希望自己的 PyTorch 代码能原样运行，任何缺失的算子或孱弱的性能剖析工具都可能导致其无人采用。TorchTitan 是一个 PyTorch 原生的参考平台，用于大规模生成式模型训练，集成了三维并行、训练优化和可扩展的分布式检查点，因此常被用来检验新加速器的软件栈是否已达到生产可用水平。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aws.amazon.com/ai/machine-learning/trainium/">AI Accelerator - AWS Trainium - AWS | Amazon Web Services, Inc.</a></li>
<li><a href="https://www.aboutamazon.com/news/aws/what-you-need-to-know-about-the-aws-ai-chips-powering-amazons-partnership-with-anthropic">AWS AI chips powering Amazon 's partnership with Anthropic</a></li>
<li><a href="https://github.com/pytorch/torchtitan">GitHub - pytorch/ torchtitan : A PyTorch native platform for training...</a></li>

</ul>
</details>

**标签**: `#AWS Trainium`, `#AI hardware`, `#ML training`, `#PyTorch`, `#SemiAnalysis`

---

<a id="item-4"></a>
## [PHP 紧急发布补丁，修复两个 CVSS 9.2 级远程代码执行漏洞](https://t.me/zaihuapd/44647) ⭐️ 8.0/10

PHP 团队发布带外安全更新，推出 PHP 8.5.12、8.4.27、8.3.36 和 8.2.35，修复两个在 CVSS 4.0 标准下均评为 9.2 分的严重漏洞，攻击者可未经身份验证远程执行任意代码，官方敦促所有用户立即升级。 PHP 支撑着互联网上极大比例的网站，而这两个漏洞几乎影响所有处理 HTTP 请求的部署形态——PHP-FPM、Apache 的 mod_php、php-cgi、FrankenPHP 以及 LiteSpeed，因此任何尚未打补丁、暴露在公网的服务器都可能被匿名攻击者利用，对运维人员和主机托管商而言属于必须立刻处置的事件。 mod_php 的风险最高：已有验证表明攻击可以在网站自身业务代码运行之前就被触发，因此 PHP 代码层面的应用防御和输入过滤无法阻止它。升级到四个已修复版本之一是目前唯一可靠的补救手段；由于这是紧急补丁而非详细的技术分析，管理员应确认其实际使用的 Web 服务器 SAPI（FPM、mod_php、CGI、FrankenPHP 或 LiteSpeed）运行的确实是已修补的二进制文件，而不能只看软件包版本号。

telegram · zaihuapd · 10月23日 13:46

**背景**: PHP 是一种由服务端组件（SAPI）代表 Web 服务器执行的脚本语言。最常见的部署方式是 PHP-FPM，它是一个 FastCGI 进程管理器，把 PHP 工作进程与 Web 服务器分离运行，常用于高负载站点；更传统的方式是 mod_php，它将 PHP 解释器直接嵌入 Apache 进程之中，而 FrankenPHP 等新方案则把 PHP 嵌入基于 Go 和 Caddy 的应用服务器内。由 FIRST 维护的 CVSS 4.0 评分体系以 0 到 10 分衡量漏洞严重程度，其中 9.0–10.0 属于“严重”级别，因此一个无需认证即可利用的 9.2 分漏洞应被视为现实威胁而非理论风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.php.net/manual/en/install.fpm.php">PHP: FastCGI Process Manager (FPM) - Manual</a></li>
<li><a href="https://frankenphp.dev/">FrankenPHP : the modern PHP app server</a></li>
<li><a href="https://php2shell.io/">PHP2Shell: Fix CVE-2026-109618 & CVE-2026-109619</a></li>

</ul>
</details>

**标签**: `#security`, `#php`, `#vulnerability`, `#remote-code-execution`, `#patching`

---

<a id="item-5"></a>
## [本地维基百科：维基百科，但只涵盖距你步行半小时内的事物](https://edjefferson.com/localwiki/) ⭐️ 7.0/10

Local Wikipedia 是一款超本地化的维基百科浏览器，只显示关于步行可达地点的条目，引发了关于知识策展和基于邻近度的相关性的讨论。

hackernews · sohkamyung · 10月22日 23:01 · [社区讨论](https://news.ycombinator.com/item?id=50202285)

**标签**: `#Wikipedia`, `#hyperlocal`, `#geolocation`, `#knowledge curation`, `#web tools`

---

<a id="item-6"></a>
## [EFF 警告：加拿大人反对 C-22 法案的时间所剩无几](https://www.eff.org/deeplinks/2026/10/canadians-are-running-out-time-oppose-dangerous-c-22-surveillance-bill) ⭐️ 7.0/10

EFF 发布警告称，加拿大人反对 C-22 法案的时间已经不多；该监控法案将扩大与外国执法机构的数据共享，并威胁即时通讯隐私。 若该法案通过，加拿大用户的数据可能暴露给外国执法机构，端到端加密可能被削弱，大型即时通讯服务也可能封锁或退出加拿大。 该法案将要求电信运营商、即时通讯应用以及其他潜在的数字服务为警方和加拿大安全情报局（CSIS）建立监控能力，并将用户元数据保留最多一年；法案已在众议院通过，目前提交参议院审议。

hackernews · hn_acker · 10月22日 22:43 · [社区讨论](https://news.ycombinator.com/item?id=50202114)

**背景**: C-22 法案又称《合法访问法》，是一项加拿大监控法案，将修订《刑法》、《加拿大安全情报局法》及相关法律，赋予警方和情报机构新的调查权力。批评者认为，其元数据保留和系统改造要求相当于监控后门，会削弱加密。该法案还扩大跨境数据共享，而加拿大与美国一直在云数据法律框架下谈判互惠访问协议，因此这一问题尤为敏感。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.le-vpn.com/canada-bill-c-22-lawful-access-vpn/">Canada Bill C - 22 Explained: Lawful Access and VPNs | Le VPN</a></li>
<li><a href="https://reclaimthenet.org/even-google-warns-canada-bill-c-22-creates-surveillance-backdoors">Even Google Warns Canada Bill C - 22 Creates Surveillance Backdoors</a></li>
<li><a href="https://www.accessnow.org/press-release/encryption-and-privacy-threats-in-canadas-bill-c-22/">Open letter from European civil society organisations on encryption ...</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一但普遍怀疑：一些人认为请愿和公众参与是唯一真正的制衡手段，并敦促加拿大人采取行动；另一些人则表示参议院很少否决法案，这场斗争可能已经失败。还有人警告，如果法案维持不变，大型即时通讯服务将封锁加拿大，并批评加美数据共享安排可能让美国警方在未经加拿大法院监督的情况下获取信息。

**标签**: `#privacy`, `#surveillance`, `#Canada`, `#encryption`, `#tech policy`

---

<a id="item-7"></a>
## [群体模仿被证明等价于单个带臂老虎机学习智能体](https://www.reddit.com/r/MachineLearning/comments/1xdhf7r/r_the_hive_mind_is_a_single_reinforcement/) ⭐️ 7.0/10

一篇发布在 Reddit r/MachineLearning 的帖子（由 /u/mistlab 提交）给出了一个证明：大规模群体中的去中心化局部模仿——包括蜜蜂摇摆舞的“加权投票者”模型——在数学上等价于多臂老虎机中单智能体的强化学习更新。作者据此推导出一种新的宏观层面算法，命名为 Maynard-Cross Learning（MCL），其中 N 个不具备学习能力的个体各自充当一条并行的环境采样轨迹，从而使每个样本的有效步长为 alpha = 1/N。 如果该等价关系成立，它就为“蜂群思维”式的集体智能如何从只会盲目模仿邻居、既不学习也不比较收益的个体中涌现提供了形式化机制，从而把群体智能与演化博弈论同标准的强化学习理论连接起来。这对研究集体认知的生物学家，以及设计依赖简单局部规则实现协调的可扩展去中心化群体机器人算法的工程师，都具有重要意义。 该证明首先表明，经典的“模仿成功者”协议——以与邻居收益成正比的概率复制其策略——其演化过程与 Cross Learning 老虎机算法的期望更新完全一致，随后将其推广到不看收益的摇摆舞模仿规则，从而得到 MCL。这一结论目前只是发布在 Reddit 上的未经同行评审的预印本级别成果，其主要局限在于：等价性是在平均场式的复制子动力学下针对宏观种群分布成立的，而非针对有限规模、具有结构或空间异质性的种群。

reddit · r/MachineLearning · /u/mistlab · 10月23日 15:37

**背景**: 多臂老虎机是强化学习中的经典问题：智能体反复从若干“摇臂”中选择一个，每个摇臂从未知分布中返回随机奖励，智能体必须在利用当前最优摇臂与探索其他摇臂之间取得平衡。Cross Learning 是一种早期而简单的老虎机算法，直接用观测到的奖励来更新动作概率。演化博弈论通过复制子动力学描述种群中策略频率随时间的变化，而蜜蜂选择巢址正是教科书式的生物学案例——侦察蜂用摇摆舞宣传巢址，舞蹈时长与巢址质量成正比，跟随者则不加评估地复制被宣传的巢址。该论文的主张是：这两种描述——种群层面的模仿与单智能体的学习——在数学上是同一个对象。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Multi-armed_bandit">Multi-armed bandit - Wikipedia</a></li>
<li><a href="https://content.ces.ncsu.edu/honey-bee-dance-language">The Honey Bee Dance Language - NC State Extension Publications What Is the Waggle Dance? How Honey Bees Communicate Distance ... The evolution of honey bee dance communication: a mechanistic ... Frontiers | Why, when and where did honey bee dance ... Foraging distance distributions reveal how honeybee waggle ...</a></li>

</ul>
</details>

**标签**: `#reinforcement-learning`, `#swarm-intelligence`, `#multi-armed-bandits`, `#evolutionary-game-theory`, `#collective-decision-making`

---

<a id="item-8"></a>
## [字节跳动发布 Seedance 2.5 视频模型，单次可生成 30 秒](https://t.me/zaihuapd/44639) ⭐️ 7.0/10

字节跳动于 7 月 31 日正式发布新一代音视频联合生成模型 Seedance 2.5，将单次生成时长从上一代的 15 秒翻倍提升至 30 秒。新版本支持多轮延长以产出数分钟的高质量连贯视频，单次最多可输入 30 张图片、10 段视频和 10 段音频作为参考素材，并能通过时间戳精准控制画面与节奏。 更长的单次生成时长、多轮延长以及大规模参考素材输入，使 AI 视频生成从几秒的演示片段迈向可用的叙事序列，这对广告、短剧等内容制作团队意义重大。该模型先在即梦 AI 和豆包专业版上线、随后接入火山方舟 API，意味着字节跳动几乎同步把这一能力推给了普通用户和企业开发者。 此次发布重点强调长叙事、多模态参考与编辑能力，用户可通过时间戳对单个片段进行控制，而无需重新生成整段视频。该消息未披露基准测试、分辨率或定价信息，且可用模式、时长和价格预计会因 Seedance.tv、即梦 AI、火山方舟 API 等入口不同而有所差异。

telegram · zaihuapd · 10月23日 08:27

**背景**: Seedance 是字节跳动的视频生成模型系列，此前的 2.0 版本奠定了原始的多模态生成系统，而 2.5 则定位于更长叙事、更大规模参考素材集和更高级的视频编辑。即梦 AI（海外曾以 Dreamina 名义推出）是字节跳动旗下的一站式 AI 创作平台，用户可输入文字或上传图片生成图像和短视频；豆包则是其面向消费者的 AI 助手品牌。火山方舟是字节跳动旗下火山引擎推出的一站式大模型服务平台，提供推理、精调到部署的全链路服务，其 API 与 OpenAI 协议兼容，方便开发者迁移已有 SDK 代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://seed.bytedance.com/en/seedance2_5">Seedance 2.5 - seed.bytedance.com</a></li>
<li><a href="https://moge.ai/zh/product/jimeng-ai">Jimeng AI : 字 节 跳 动 推出的 AI ... - MOGE</a></li>
<li><a href="https://www.huasheng.ai/insights/volcengine-ark-api-guide/">火山引擎方舟 API 平台深度调研 | 花叔 火山方舟 - 首页 - ark.volcengine.com SDK中心 - api.volcengine.com 安装及升级 SDK - 火山方舟 - 火山引擎</a></li>

</ul>
</details>

**标签**: `#AI video generation`, `#ByteDance`, `#Seedance`, `#multimodal`, `#generative AI`

---

<a id="item-9"></a>
## [据称 iPhone 18 Pro 实现重启后仍保留的非绑定越狱](https://t.me/zaihuapd/44644) ⭐️ 7.0/10

一个 Telegram 频道爆料称，研究者 @calif_io 在 iPhone 18 Pro 上演示了非绑定（untethered）越狱：设备重启后越狱状态依然保留，且全程无需连接电脑，若属实这将是自 iOS 9 以来首个公开展示的完整非绑定越狱。据称攻击链分为三层：滥用 cryptex 子系统、伪造 TSS 票签签名，以及绕过 PAC（指针认证码）保护。 如果得到证实，在当代硬件上实现重启后依然存活的越狱，将是 iOS 安全研究的一个重大里程碑，说明苹果的多层防御——签名系统卷、服务器端签名校验和硬件级指针认证——依然可能被串联攻破。这也会影响整个生态：越狱技术往往预示着商业间谍软件所使用的攻击链类型，并影响 iOS 后续加固的优先级。 该说法仅来自一条简短的 Telegram 帖子，没有公开的技术文章、PoC 代码或第三方独立验证；时间点也值得注意——苹果据称在 9 月 14 日修补了 273 个漏洞，意味着这条攻击链所依赖的缺陷可能并未被该次更新覆盖。受影响的具体 iOS 版本、设备所用的 A 系列芯片型号，以及完整重启后是否真正实现用户态持久化等细节，目前均未得到验证。

telegram · zaihuapd · 10月23日 11:43

**背景**: 越狱是指解除苹果的软件限制，使设备能够运行 App Store 之外的代码和应用；“绑定（tethered）”越狱在每次重启后失效，必须用电脑重新施加，而“非绑定（untethered）”越狱能在重启后自行保留，实现难度高得多。cryptex 子系统是苹果用来以个性化磁盘映像分发加密签名辅助软件的机制，由于它掌控这些映像的发布位置与挂载方式，因而成为绕过签名校验的诱人目标。TSS（票签签名系统）是苹果的服务器，负责签发授权安装特定固件的“票签”，伪造票签就意味着骗过设备去接受苹果从未批准过的代码。PAC（指针认证码）自 A12（iPhone XS）及之后的芯片起为指针附加密码学签名，被篡改的指针会因签名校验失败而崩溃，而不是带来代码执行，因此绕过 PAC 是当代 iPhone 上取得内核控制权的关键最后一步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://keith.github.io/xcode-man-pages/cryptex.5.html">cryptex (5)</a></li>
<li><a href="https://tin-z.github.io/ios-exploit-starterpack/en/pac/">PAC -- Pointer Authentication Code | iOS Exploit Starterpack</a></li>
<li><a href="https://eclecticlight.co/2022/11/16/cryptex-how-a-custom-iphone-is-changing-macos-updates/">Cryptex : how a custom iPhone is changing macOS updates</a></li>

</ul>
</details>

**标签**: `#iOS jailbreak`, `#mobile security`, `#exploit chain`, `#PAC bypass`, `#Apple`

---

<a id="item-10"></a>
## [国办发文：要求减缓人工智能应用对就业的替代影响](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 7.0/10

10 月 23 日，国务院办公厅公布《关于适应人工智能技术发展助力构建就业友好型发展方式的意见》（国办发〔2026〕29 号），明确提出减缓人工智能应用对就业的替代影响。文件要求优先在劳动力紧缺、环境高危等岗位推广 AI，稳慎把握其在劳动密集型行业应用的范围、力度和节奏，并鼓励企业探索建立失业缓冲期制度，提前告知受影响劳动者并提供转型转岗就业支持。 这是较早由国务院层面正式把 AI 就业替代作为治理议题、而非仅视为效率机遇的政策文件之一，意味着中国推进 AI 应用时将越来越多地权衡就业稳定因素。它可能影响制造业、物流、客服、内容运营等劳动密集型行业企业安排自动化落地的节奏，也为地方政府建设再培训与转岗支持体系提供了政策依据。 该文件属于“意见”而非具有强制约束力的法律，其效力主要通过地方落实和后续配套措施体现；文件强调要放大 AI 创造就业、赋能传统岗位、提升就业质量的正面效应，同时抑制替代效应。“失业缓冲期制度”被表述为鼓励企业探索，属于自愿性安排，而非强制性的裁员补偿或提前通知义务。

telegram · zaihuapd · 10月23日 12:54

**背景**: 国务院办公厅是中央政府的日常办事机构，其以“国办发”编号印发的文件（此处为 2026 年第 29 号）通常为各部委和省级政府后续落实定下政策方向。“就业友好型发展方式”是一个政策概念，核心是以能否扩大或保住体面就业来衡量经济与技术发展。随着生成式 AI 向白领和服务类岗位扩散，中国政策制定者愈发将推动 AI 与稳就业举措并列，此前国家发展改革委等机构也曾就 AI“赋能”而非“替代”劳动者发表解读文章。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www1.xinhuanet.com/politics/20261023/f21a5777774749daa0eed451c81f4002/c.html">国务院办公厅印发《关于适应人工智能技术发展助力构建就业友好型发展...</a></li>
<li><a href="https://www.stdaily.com/web/2026-10/23/content_601752.html">国务院办公厅关于适应人工智能技术发展助力构建就业友好型发展方式的...</a></li>
<li><a href="https://finance.eastmoney.com/a/202610243906815770.html">国务院办公厅公布《关于适应人工智能技术发展助力构建就业友好型发展...</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#employment`, `#China`, `#AI governance`, `#labor market`

---

<a id="item-11"></a>
## [失业与可的松引发的躁狂：一篇引发共鸣的个人随笔](https://tilschuenemann.de/job-loss-cortisone-mania) ⭐️ 6.0/10

博客 tilschuenemann.de 的作者发表了一篇第一人称自述，讲述自己先失去工作、随后接受可的松（糖皮质激素）治疗后陷入躁狂发作的经历。这篇文章登上了 Hacker News 首页，获得约 156 分和 89 条评论，作者本人也出现在讨论中致谢，并说明自己目前正在逐步减量，整个疗程约六周。 糖皮质激素引起的精神症状在医学文献中早有记载，但在普通技术读者中很少被谈及；这样一篇坦诚的自述有助于患者及家属认识到躁狂、轻躁狂和精神病性症状可能是药物副作用，而非纯粹的心理问题。讨论还延伸到人们在多大程度上把身份认同与人生意义寄托在工作上这一更广泛的话题。 作者提到自己享有德国公共医疗保险并能获得优质医疗资源，目前正从约六周的疗程中逐步减少可的松用量。评论者的经历表明，即使是因癌症治疗或免疫治疗等非精神科原因用药的患者，也可能出现精神与身体方面的不良反应。

hackernews · speckx · 10月23日 10:31 · [社区讨论](https://news.ycombinator.com/item?id=50206840)

**背景**: 可的松属于糖皮质激素类药物（与泼尼松、泼尼松龙同类），作为强效的抗炎和免疫抑制药物被广泛用于过敏、自身免疫病以及肿瘤治疗辅助等场景。其精神方面的副作用虽被医学界承认，却常被低估：综述文献描述了情绪紊乱、焦虑、失眠，部分病例还会出现明显的躁狂或精神病性症状，其中欣快感和轻躁狂是最常见的短期反应。相关机制被认为与下丘脑—垂体—肾上腺（HPA）轴失调有关，病例报告显示即使在低剂量下也可能出现躁狂症状。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11675195/">Corticosteroid-Induced Psychiatric Disorders: Mechanisms ...</a></li>
<li><a href="https://www.mayoclinicproceedings.org/article/S0025-6196(11)61160-9/fulltext">Psychiatric Adverse Effects of Corticosteroids - Mayo Clinic ...</a></li>
<li><a href="https://www.frontiersin.org/journals/pharmacology/articles/10.3389/fphar.2025.1628765/full">Frontiers | Corticosteroid - induced manic and /or psychotic symptoms...</a></li>

</ul>
</details>

**社区讨论**: 讨论整体充满支持，作者对如此热烈的回应表示意外与感激。评论者分享了严肃的亲历经验——其中一位讲述自己在胸腺癌治疗后因免疫治疗出现严重肌肉无力和炎症，呼应了文章主题——也有人从哲理角度感慨现代生活在工作之外几乎难以获得满足感，而失业反而可能带来某种解脱。

**标签**: `#mental-health`, `#corticosteroids`, `#job-loss`, `#work-life-balance`, `#personal-essay`

---

<a id="item-12"></a>
## [LLM 记忆或许更需要遗忘而非更大回忆容量](https://www.reddit.com/r/MachineLearning/comments/1xdpek9/are_we_solving_llm_memory_by_remembering_more/) ⭐️ 6.0/10

一篇发布在 Reddit r/MachineLearning 的帖子认为，LLM 记忆研究过度关注回忆容量，而忽视了更新或遗忘过时知识这一更难的问题。帖子比较了 Transformer、RAG、线性注意力、DeltaNet 和 BDH 如何处理新旧信息冲突，并举例说编码智能体在文档把 API 超时从 30 秒改为 5 秒后仍继续使用旧值。 随着长上下文模型达到数十万甚至数百万 token，单纯保留更多信息并不能保证智能体使用事实的最新版本。这对编码智能体、RAG 系统以及任何会因过时知识导致错误操作的应用都很重要。 帖子区分了存储信息与更新信息，并追问核心困难在于记忆的存储/更新机制，还是在于对矛盾信息进行推理。它指出 DeltaNet 使用基于预测误差的更新，BDH 使用 Hebbian 式突触可塑性，但提出何时更新、何时保留以及如何避免破坏无关记忆等问题；帖子建议采用基于矛盾信息的评测，但没有给出实验或基准结果。

reddit · r/MachineLearning · /u/Prestigious-Tip6030 · 10月23日 20:39

**背景**: 长上下文 LLM 的设计目标是在推理时保留大量文本，但多数评测检验的是模型能否检索某个事实，而不是在新证据出现时能否修正该事实。在标准 Transformer 或 RAG 流程中，新旧段落可以同时存在于上下文中，由模型在读取时解决冲突。线性注意力把历史压缩进固定大小的状态，DeltaNet 式更新利用预测值与观测值之间的差异来擦除并重写关联。BDH（Dragon Hatchling）则探索 Hebbian 式突触可塑性，把记忆与连接权重的变化联系起来，而不是依赖显式的 token 缓冲区。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sustcsonglin.github.io/blog/2024/deltanet-3/">DeltaNet Explained (Part III) | Songlin Yang</a></li>
<li><a href="https://www.crvscience.com/post/the-dragon-hatchling-a-bio-physical-paradigm-for-post-transformer-artificial-intelligence">The Dragon Hatchling : A Bio-Physical Paradigm for Post-Transformer...</a></li>
<li><a href="https://arxiv.org/pdf/2507.19595">Efficient Attention Mechanisms for Large Language Models: A ...</a></li>

</ul>
</details>

**标签**: `#LLM memory`, `#long-context`, `#DeltaNet`, `#RAG`, `#machine-learning`

---

<a id="item-13"></a>
## [微软悄然测试 Project Pantheon：用户自选记忆的 Recall 替代品](https://www.windowslatest.com/2026/10/23/microsoft-is-quietly-testing-another-recall-for-windows-11-but-this-one-doesnt-record-your-screen/) ⭐️ 6.0/10

微软据报正在 Windows 11 上悄然测试一款名为 Project Pantheon 的 AI 记忆应用，其中一个名为 Context Vault 的版本只把用户主动选择的网页、文件、截图、文本和音视频保存为“记忆”。用户可就这些记忆提问，应用还通过 MCP 服务器把它们提供给 Claude、Cursor 等 AI 工具调用，这与 Recall 的自动截屏方式不同。 如果最终发布，这将为 Windows 提供一个比 Recall 更强调用户同意的记忆层，并可能通过 MCP 让 PC 成为第三方 AI 智能体共享的上下文来源。这也表明，尽管 Recall 公布后遭遇隐私争议，微软仍在继续试验类 Recall 功能。 该应用需单独下载，据报依赖云端模型而非端侧处理；微软尚未公布或承诺发布，并据报正在考虑加密、Windows Hello 身份验证和 IT 管控措施。由于消息并非官方且未获证实，其可用性、定价和隐私保障目前仍不清楚。

telegram · zaihuapd · 10月23日 07:42

**背景**: Windows Recall 于 2024 年公布，会定期截取用户活动屏幕截图以便回溯搜索，但因自动记录屏幕且最初要求配备专用 NPU 的 Copilot+ PC 而引发批评。MCP（Model Context Protocol）是 Anthropic 推出的开放标准，让 AI 应用通过通用接口连接外部数据源和工具，因此 Claude 或 Cursor 等客户端可以调用本地或远程服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/gadgets/2025/04/in-depth-with-windows-11-recall-and-what-microsoft-has-and-hasnt-fixed/">In depth with Windows 11 Recall —and what Microsoft... - Ars Technica</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>

</ul>
</details>

**标签**: `#Microsoft`, `#Windows 11`, `#AI memory`, `#MCP`, `#Privacy`

---