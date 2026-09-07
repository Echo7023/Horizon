---
layout: default
title: "Horizon Summary: 2026-09-08 (ZH)"
date: 2026-09-08
lang: zh
---

> 从 30 条内容中筛选出 18 条重要资讯。

---

1. [LLM 引导的程序进化打破 Packomania 圆堆积基准上的 10 项纪录](#item-1) ⭐️ 9.0/10
2. [华为 Mate XT 2 首发逻辑折叠芯片麒麟 9050 Pro](#item-2) ⭐️ 9.0/10
3. [LG 智能电视被曝录音并扫描家庭网络](#item-3) ⭐️ 8.0/10
4. [OpenAI 披露编码智能体与 RSI 如何加速研究、通向 AGI](#item-4) ⭐️ 8.0/10
5. [KV 缓存作为智能体运行时：让 LLM 更互动](#item-5) ⭐️ 8.0/10
6. [基于 31,352 次 LLM 基准测试的研究发现显著日间性能漂移](#item-6) ⭐️ 8.0/10
7. [最高法发布 AI 纠纷司法解释 换脸与算法杀熟责任明确](#item-7) ⭐️ 8.0/10
8. [加州理工 Mathathon：首个专注负责任 AI 的研究级数学黑客松](#item-8) ⭐️ 7.0/10
9. [TPU 推理外部化全面加速，正在削弱 CUDA 护城河](#item-9) ⭐️ 7.0/10
10. [工信部规划适时启动 6G 商用，推进 eSIM 与无网通信](#item-10) ⭐️ 7.0/10
11. [bzip3 压缩工具引发基准测试方法争论](#item-11) ⭐️ 6.0/10
12. [互联网档案馆 9 月定期捐赠享 3 倍匹配](#item-12) ⭐️ 6.0/10
13. [泄露邮件揭示比尔·盖茨安装 Movie Maker 屡屡受挫](#item-13) ⭐️ 6.0/10
14. [Rustuna：用 Rust 打造的高性能 Optuna 实现已发布](#item-14) ⭐️ 6.0/10
15. [PINNStudio：用于物理信息神经网络的免费开源无代码图形界面](#item-15) ⭐️ 6.0/10
16. [苹果调整欧盟替代应用商店收费：替代支付佣金最高 20%](#item-16) ⭐️ 6.0/10
17. [国内首份办公 Agent 用户行为报告：前 20%用户消耗 87.4%算力](#item-17) ⭐️ 6.0/10
18. [ChatGPT 重创内罗毕论文代写业，4 万人受影响](#item-18) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [LLM 引导的程序进化打破 Packomania 圆堆积基准上的 10 项纪录](https://www.reddit.com/r/MachineLearning/comments/1w9xlyi/llmguided_program_evolution_improves_10_bestknown/) ⭐️ 9.0/10

研究者使用 LLM 迭代式地进化优化程序，而非直接求解圆堆积实例。在 Packomania csqv 基准上，他们的 Discovery Loop 系统在 15 次迭代中，以总计 27.72 美元的 LLM 成本，改进了 N=101 至 114 区间内 10 个数值的最佳已知半径和，提升幅度为 2.4%–5.4%，且结果被 Packomania 独立接受。 这一结果表明，LLM 驱动的程序进化能以不到 30 美元的成本，在公认的数学优化基准上取得实质性进展。它预示着更广泛的范式转变：基础模型不只是优化提示词或代码片段，而是帮助发现全新的算法。 该系统从简单的种子求解器开始；LLM 根据结果记分牌和先前尝试历史来提出算法修改，每个候选由独立验证器评分，因此只保留改进。论文（arXiv:2609.05093）还邀请学界检验其“平台期检测停止规则”，作者认为这是最需要推敲的部分。

reddit · r/MachineLearning · /u/SIGH_I_CALL · 9月7日 16:54

**背景**: “圆堆积”问题研究如何在正方形中无重叠地放置圆以最大化某个目标；Packomania 上的 csqv 变体要求最大化 N 个可变半径圆在单位正方形中的半径总和。这是一个公认的困难非凸优化问题，存在大量局部最优解。Packomania 维护着最佳已知堆积列表，传统求解通常依赖人工设计的启发式算法或数值优化。LLM 引导的进化式搜索则反复让语言模型修改求解器代码，评估变体并保留成功结果，这一思路受到 AlphaEvolve 等系统启发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.05093">[2609.05093] LLM-Guided Program Evolution for Circle Packing: Breaking 10 Packomania Records for $28</a></li>
<li><a href="https://arxiv.org/html/2609.05093">LLM-Guided Program Evolution for Circle Packing:Breaking 10 Packomania Records for $28</a></li>
<li><a href="https://packomania.com/csqv/csqv.html">The best known packings of unequal circles in a square</a></li>

</ul>
</details>

**标签**: `#LLM`, `#program evolution`, `#optimization`, `#circle packing`, `#AI research`

---

<a id="item-2"></a>
## [华为 Mate XT 2 首发逻辑折叠芯片麒麟 9050 Pro](https://www.news.cn/20260907/adf46c5c003240d28cc3cf6de54f9b5f/c.html) ⭐️ 9.0/10

华为在广州发布了搭载新款麒麟 9050 Pro 芯片的三折叠手机 Mate XT 2。这是华为自 Mate 40 时代以来首款旗舰级麒麟芯片，也是首款采用逻辑折叠技术的高性能芯片。 逻辑折叠通过垂直堆叠晶体管，可能让华为在无法使用最先进光刻设备的情况下继续提升芯片性能和集成度。如果这款芯片的实际表现与宣传吻合，或将改变高端智能手机市场的竞争格局，并推动绕过摩尔定律的新技术路线。 麒麟 9050 Pro 的逻辑折叠设计在单芯片内将逻辑单元分层排布，并增加垂直互联通道（华为将其比作复式楼里的“电梯”），以缩短信号传输路径、降低时延。华为称这是一种涉及系统、芯片、器件和电路的多层次协同优化方案；有报道称该技术可为 AI 计算带来约 53% 的晶体管密度提升，但官方详细参数和独立验证仍然有限。

telegram · zaihuapd · 9月7日 08:20

**背景**: 传统芯片微缩遵循摩尔定律，在平面的硅片上集成更多晶体管，这一过程越来越依赖先进光刻设备，并面临物理极限。逻辑折叠则是在垂直方向上堆叠电路，利用垂直互联通道缩短布线距离、降低电阻电容延迟。这种思路希望在不必继续缩小晶体管的前提下提高密度和性能，从而有效“绕过”摩尔定律。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geeky-gadgets.com/huawei-logic-folding-moores-law/">Huawei Logic Folding: A New Approach to Moore's Law - Geeky ...</a></li>
<li><a href="https://www.huaweicentral.com/huawei-logicfolding-architecture-everything-you-need-to-know/">Huawei LogicFolding Architecture: Everything you need to know</a></li>
<li><a href="https://skynexttech.com/huawei-logic-folding-chip-breakthrough/">Huawei Logic Folding Breakthrough Could Rewrite the Future of ...</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#semiconductor`, `#chip-design`, `#Kirin`, `#technology`

---

<a id="item-3"></a>
## [LG 智能电视被曝录音并扫描家庭网络](https://www.youtube.com/watch?v=6IFVTcM28KA) ⭐️ 8.0/10

Gamers Nexus、Level1Techs 和独立研究人员的调查发现，运行 webOS 的 LG 智能电视即使在屏幕关闭时也会以明文记录语音提示和其他音频，并主动扫描本地网络以探测附近的手机、智能手表等设备。该行为影响到包括 G5 OLED 在内的数百万台 LG 电视。 由于超过 2.16 亿台 LG 智能电视在使用，这实际上将客厅变成潜在的监控环境，并严重削弱了用户对联网家电的信任。同时，这也凸显了更广泛的行业问题：消费者对智能设备中内嵌的、渴求数据的功能几乎无法控制。 电视以明文记录捕获的音频，并在网络条件允许时上传数据，即使在待机状态下也会执行网络扫描。据报道，LG 的服务条款要求机主告知家庭成员和客人其声音可能会被捕获和处理，这使用户面临合同层面的监控义务。

hackernews · treve · 9月7日 00:22 · [社区讨论](https://news.ycombinator.com/item?id=49592375)

**背景**: 现代智能电视运行完整的操作系统，如 LG 的 webOS，支持流媒体应用、语音助手和自动内容识别。与手机或电脑不同，电视是客厅中的共用设备，通常一直开机并配备始终聆听的麦克风，因此其追踪行为可能暴露家中所有人的私密活动。此前 RTINGS 等机构的调查已显示智能电视会收集观看数据，但新发现揭示了更具侵入性的行为：在待机状态下捕获音频并绘制整个本地网络拓扑。这种网络扫描使电视能够构建联网设备的画像，将家庭网络变成实质上的监控目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.notebookcheck.net/LG-smart-TVs-caught-logging-audio-with-screen-off-and-snooping-on-local-devices.1391214.0.html">LG smart TVs caught logging audio with screen off and snooping on...</a></li>
<li><a href="https://news.ycombinator.com/item?id=49594878">LG smart TVs caught logging audio with screen off ... | Hacker News</a></li>
<li><a href="https://cyberinsider.com/lg-smart-tvs-found-scanning-home-networks-for-nearby-devices/">LG Smart TVs found scanning home networks for nearby devices</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了愤怒和‘果然如此’的心情，有人指出自己当初因关闭智能电视联网功能而被嘲笑，现在觉得自己是正确的。还有人强调 LG 服务条款的苛刻——要求用户告知电视附近的所有人可能被窃听，同时有人感叹现在很难买到‘笨电视’和注重隐私的流媒体盒子。总体上，评论对 LG 以及整个行业向监控驱动商业模式发展的趋势持强烈批评态度。

**标签**: `#privacy`, `#smart-tv`, `#surveillance`, `#security`, `#lg`

---

<a id="item-4"></a>
## [OpenAI 披露编码智能体与 RSI 如何加速研究、通向 AGI](https://simonwillison.net/2026/Sep/6/research-acceleration-the-view-inside-openai/) ⭐️ 8.0/10

Simon Willison 报道了 OpenAI 的新文章《研究加速：OpenAI 内部视角》，其中展示了编码智能体如何重塑 OpenAI 研究人员的日常工作。研究人员的日均 AI 支出从 2026 年 2 月的接近零上涨到 8 月下旬的约 600 美元。 这条新闻的意义在于，它罕见地公开了 OpenAI 内部的智能体工程实践，并将其与递归自我改进（RSI）联系起来，作为公司迈向 AGI 的路径之一。在 2026 年这个智能体工程真正起飞的年份，它表明 AI 研究本身也在被这些研究者参与创造的工具加速。 Willison 注意到文中直接使用缩写 RSI 而未展开，并推测 7 月下旬开始的人均支出陡增，是因为内部员工获得了后来以 GPT-6 Astra 名义发布的模型访问权限。这篇报告还搭配了首席科学家 Jakub Pachocki 的署名文章《An Alien Mind》。

rss · Simon Willison · 9月6日 23:57

**背景**: 编码智能体是指能够独立编写、调试和重构代码的 AI 工具；2026 年，通过指挥这类智能体来开发软件的智能体工程已成为行业主流实践。递归自我改进（RSI）指的是 AI 系统参与改进自身的过程，这个概念与 OpenAI 在 AGI 路线上追求更快进展密切相关。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://datasciencedojo.com/blog/recursive-self-improvement-agentic-ai/">Recursive Self - Improvement in Agentic AI (2026 Guide)</a></li>
<li><a href="https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/">What is agentic engineering? - Agentic Engineering Patterns - Simon Willison's Weblog</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-engineering">What is Agentic Engineering? | IBM</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#coding agents`, `#AI research`, `#agentic engineering`, `#RSI`

---

<a id="item-5"></a>
## [KV 缓存作为智能体运行时：让 LLM 更互动](https://www.reddit.com/r/MachineLearning/comments/1w9myqc/kv_cache_as_an_agent_runtime_r/) ⭐️ 8.0/10

Yandex 研究人员提出将 KV 缓存用作智能体运行时（agent runtime），通过修改模型推理状态来实现更具交互性的 LLM。该思路建立在实验室此前的 Hogwild! Inference 和 AsyncReasoning 工作之上，并预展了 Qwen3.8-27B 智能体在 DOOM 环境中进行交互式游玩。 这一思路将推理与运行时设计重新定位为智能体能力中一条尚未被充分探索的轴线，独立于模型权重和外部 harness（调度框架）。如果顺利推进，它有望让智能体无需昂贵重训即可实时响应和适应新信息，惠及语音助手、具身智能体等交互系统。 Hogwild! Inference 利用旋转位置编码（RoPE）让多个 LLM 实例并行共享同一注意力缓存，而 AsyncReasoning 无需额外训练即可并发处理多条 token 流。博客文章展示的是未来工作预览（一个由 Qwen3.8-27B 驱动的智能体在 DOOM 中交互式游玩），并非已发布的可运行 demo。

reddit · r/MachineLearning · /u/_puhsu · 9月7日 09:03

**背景**: KV 缓存保存了模型前序 token 计算得到的键（key）和值（value）张量，使 LLM 在逐 token 生成时无需重算整个对话。标准推理是串行的：模型必须先完成当前输出才能处理新输入，这限制了实时交互。这一研究方向通过修改推理状态，让思考、输出与新输入能够重叠进行，相当于把运行时本身用作承载 LLM 智能体的基座。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms">Understanding and Coding the KV Cache in LLMs from Scratch</a></li>
<li><a href="https://arxiv.org/html/2504.06261v1">Hogwild! Inference: Parallel LLM Generation via Concurrent ...</a></li>
<li><a href="https://arxiv.org/abs/2512.10931">[2512.10931] Asynchronous Reasoning: Training-Free ... GitHub - yandex-research/AsyncReasoning Asynchronous Reasoning in LLMs | PDF | Thought | Computing (PDF) Asynchronous Reasoning: Training-Free Interactive ... Architecting Asynchronous Inference Engines for Real‑Time ... Async LLM Inference Patterns That Scale - Medium</a></li>

</ul>
</details>

**标签**: `#KV cache`, `#LLM agents`, `#interactive inference`, `#systems for ML`, `#agent runtime`

---

<a id="item-6"></a>
## [基于 31,352 次 LLM 基准测试的研究发现显著日间性能漂移](https://www.reddit.com/r/MachineLearning/comments/1w9llr4/measuring_llm_performance_drift_observations_and/) ⭐️ 8.0/10

一项大规模研究分析了 49 个模型的 31,352 次重复基准测试测量，发现日间中位数分数波动幅度约为日内变动的三倍（标准差分别为 8.43 和 2.80 分）。作者提出一种纵向基准测试方法论，强调随时间追踪模型行为，而非依赖快照式排行榜分数。 由于通过 API 提供的模型可能在版本未发布的情况下改变行为，静态基准分数会误导模型选择与监控。随着 LLM 评估成为生产可靠性问题，这项工作凸显了持续漂移检测的必要性。 日内分数的标准差为 2.80 分，而日间每日中位数的标准差为 8.43 分，两者之比约为 3:1。作者采用版本化的基准配置、重复的基于执行的评估、单独记录可用性故障，并有意不公开完整实时任务库以减少污染。

reddit · r/MachineLearning · /u/ionutvi · 9月7日 07:44

**背景**: LLM 基准分数通常被视为模型名称的稳定属性，但商业模型常通过 API 访问，其底层权重、基础设施和提供方配置可能随时间变化。这会导致看似普通噪声的真实性能漂移。相关研究——如 HAPI 纵向数据集以及 ReasonBENCH 等研究——已经表明，LLM 行为在重复运行中和不同时间点都可能出现显著差异。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.logicmonitor.com/blog/llms-dont-stand-still-how-to-monitor-and-trust-the-models-powering-your-ai">How to Monitor and Trust the LLMs Powering Your AI | LogicMonitor</a></li>
<li><a href="https://people.eecs.berkeley.edu/~matei/papers/2022/neurips_hapi.pdf">HAPI: A Large-scale Longitudinal Dataset of Commercial ML API Predictions</a></li>
<li><a href="https://arxiv.org/html/2512.07795v1">ReasonBENCH: Benchmarking the (In)Stability of LLM Reasoning</a></li>

</ul>
</details>

**标签**: `#LLM`, `#benchmarking`, `#performance drift`, `#evaluation methodology`, `#API models`

---

<a id="item-7"></a>
## [最高法发布 AI 纠纷司法解释 换脸与算法杀熟责任明确](https://www.cnr.cn/news/20260907/t20260907_527806795.shtml) ⭐️ 8.0/10

9 月 7 日，最高人民法院发布人工智能纠纷案件司法解释，共 24 条，明确了未经同意用 AI 制作用户可识别人脸、声音等可能构成人格权侵权，算法价格歧视侵害权益应承担法律责任。 这一解释为法院处理人工智能相关侵权提供了具体法律依据，直接影响 AI 开发者、平台运营者和消费者。它标志着人工智能监管走向细化，为行业确立了更明确的合规预期。 该解释分为 5 部分共 24 条，涉及 AI 换脸、算法杀熟、冒充他人代言、自动驾驶和知识产权等议题。解释同时依法规制利用人工智能实施“网络开盒”“人肉搜索”等侵害隐私权的行为，并支持对 AI 冒充他人代言诱导消费适用惩罚性赔偿。

telegram · zaihuapd · 9月7日 09:32

**背景**: 算法杀熟（俗称“大数据杀熟”）指平台利用个人数据对不同用户设置不同价格，中国法律将其视为禁止的不合理差别待遇。所谓“网络开盒”是新型“人肉搜索”式侵权，不法分子通过非法手段获取并在网上公开曝光他人姓名、住址、电话等隐私信息。此次司法解释在个人信息保护法等法律基础上，使 AI 相关侵权案件中的法律适用更具操作性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/item/网络开盒/67437911">网络开盒 - 百度百科</a></li>
<li><a href="https://m.thepaper.cn/newsDetail_forward_29760319">鲍翔 文学国｜大数据杀熟的法律性质与责任分析</a></li>
<li><a href="http://www.shfzb.com.cn/shfzb/html/2024-12/18/content_150505_1652847.htm">上海法治报数字报-禁止“利用算法杀熟”，监管如何破局</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#deepfakes`, `#algorithmic pricing`, `#law`, `#China`

---

<a id="item-8"></a>
## [加州理工 Mathathon：首个专注负责任 AI 的研究级数学黑客松](https://mathathonchallenge.com/index.html) ⭐️ 7.0/10

加州理工学院的本科生正在组织 Caltech Mathathon，号称有史以来第一个专注于研究级数学的黑客松。活动强调负责任地使用 AI，并接受团队报名参加。 它将 AI 辅助发现与研究级数学这两个新兴趋势结合成一种新颖的比赛形式。其结果或可揭示，在短期高强度环境中，LLM 能否在开放数学问题上取得有意义的进展。 组织者是加州理工本科生，独立行动，不代表 Caltech 或赞助商，也不领取报酬；募集的资金用于支付评委和参赛者。FAQ 页面列出了他们对负责任 AI 的承诺。

hackernews · astroanax · 9月7日 09:26 · [社区讨论](https://news.ycombinator.com/item?id=49596055)

**背景**: 黑客松通常是短时高强度活动，团队在数天内构建软件原型。而本次活动要求参与者使用 AI 工具解决研究级数学问题，反映出人们对将大语言模型用于数学推理的兴趣日增。

**社区讨论**: 评论者普遍感到好奇但不乏怀疑：有人质疑连续 40 小时等待 LLM 输出是否还能保留传统黑客松的吸引力；组织者则强调目标是促进负责任 AI 使用，并帮助学生在 Caltech 较弱的 CS 系之外获得机器学习上的认可。一位申请者希望该活动成为测试最大化 LLM 推理能力的平台。

**标签**: `#AI`, `#mathematics`, `#hackathon`, `#Caltech`, `#research`

---

<a id="item-9"></a>
## [TPU 推理外部化全面加速，正在削弱 CUDA 护城河](https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam) ⭐️ 7.0/10

SemiAnalysis 的新报告指出，Google 的 TPU 推理外部化正在全速推进，InferenceX 基准测试显示其性价比最高可提升 50%。报告还指出，客户群体不断增长，以及即将推出的 Ironwood TPU（报告中称为 TPUv8i）将进一步推动这一趋势。 Nvidia 的 CUDA 软件生态长期发挥着锁定效应，因此在推理领域出现一个性价比更高的非 Nvidia 路线，将直接威胁这一优势。如果 Google 的 TPU 技术栈继续突破内部使用范围并向外部扩张，Google Cloud 将能承接更多 AI 推理工作负载，加剧 AI 基础设施领域的竞争。 InferenceX 是 SemiAnalysis 推出的开放式 AI 推理基准测试，覆盖不同芯片和服务栈的固定序列推理，以及智能体式长上下文编码场景。报告重点强调 TPU 软件栈的外部化速度加快和客户采用规模增长，而专为“推理时代”打造的 Ironwood 将成为下一个催化剂。

rss · Semianalysis · 9月7日 20:00

**背景**: TPU 是 Google 为 AI 工作负载自研的张量处理器；多年来主要服务于 Google 内部业务，后来才在 Google Cloud 上更广泛地提供。SemiAnalysis 的 InferenceX 同时衡量常规推理与智能体推理，让 TPU 与 GPU 的对比更加直观。所谓 CUDA 护城河，指的是 Nvidia 庞大而成熟的软件生态，使开发者持续绑定在其 GPU 之上。Ironwood 是 Google 最新一代 TPU，专为 AI 推理场景而设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://inferencex.semianalysis.com/about">About | InferenceX by SemiAnalysis</a></li>
<li><a href="https://blog.google/innovation-and-ai/infrastructure-and-cloud/google-cloud/ironwood-tpu-age-of-inference/">Ironwood : The first Google TPU for the age of inference</a></li>
<li><a href="https://multigrid.ai/learn/cuda-moat">CUDA and the Software Moat : What It Is Actually Made Of · Multigrid</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#TPU`, `#Google Cloud`, `#Inference`, `#CUDA`

---

<a id="item-10"></a>
## [工信部规划适时启动 6G 商用，推进 eSIM 与无网通信](https://36kr.com/newsflashes/3973030022541575) ⭐️ 7.0/10

工业和信息化部印发《信息通信行业发展“十五五”规划》，提出适时启动 6G 商用，有序推进 eSIM、无网通信等新技术应用和 5G-A 网络覆盖扩展。 这份顶层政策规划为中国电信行业未来五年指明了方向，将影响设备商、运营商和终端厂商。适时启动 6G 商用和新技术应用将影响下一代通信领域的全球竞争格局。 规划提出推进城市及热点区域网络向“双万兆”演进，深化 5G-A 在县级以上城区连续覆盖并向重点乡镇延伸，实现城市热点区域万兆下行、千兆上行峰值速率。还要求建立卫星互联网设备联网境内规则，组织开展新一代移动智能终端现网试验。

telegram · zaihuapd · 9月7日 07:58

**背景**: 5G-A（5G-Advanced）是 5G 的演进增强版本，与 5G 并行工作，支持 3D 化、云化、万物互联、通信感知一体化等更高要求的应用场景。无网通信指的是不依赖蜂窝基站的设备间直接通信（D2D），华为 Mate 80 首发的 700M 无网应急通信即是此类能力。所谓“双万兆”指的是 5G-A 无线与 F5G-A 有线光网的技术能力均接近万兆。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.iot101.com/mobile/news/10119.html">被华为Mate 80带火的“ 无 网 通 信 ” 是 什 么</a></li>
<li><a href="https://baike.baidu.com/item/5G-A/63815414">5G-A_百度百科</a></li>
<li><a href="https://www.cww.net.cn/article?id=140048A6C42D41319C6FB0EF88F673ED">北京移动启动“ 双 万 兆 ”计划 将建设1000个 万 兆 社区_ 通 信 世界网</a></li>

</ul>
</details>

**标签**: `#6G`, `#telecom policy`, `#eSIM`, `#5G-A`, `#China`

---

<a id="item-11"></a>
## [bzip3 压缩工具引发基准测试方法争论](https://github.com/iczelia/bzip3) ⭐️ 6.0/10

开源压缩工具 bzip3 将自己定位为 bzip2 的精神继承者，宣称借助现代化 Burrows-Wheeler 变换实现更高的压缩率和更快的解压速度，由此引发关注。社区评测者开始质疑官方基准图表，指出 bzip3 测试使用了 512 MiB 的块大小，而 zstd 仍采用约 8 MiB 的默认窗口大小。 压缩工具的选择直接影响存储成本、归档工作负载和软件互操作性，因此可信的基准测试对用户非常重要。这场讨论同时也表明，基于 BWT 的压缩器可以利用源代码语料中的长距离冗余，而中，窗口足够大的 zstd 也可能缩小这种表面上的差距。 bzip3 与 bzip2 不兼容；它结合了基于后缀数组的快速 BWT、LZP（Lempel-Ziv + Prediction）处理以及 order-0 上下文混合熵编码器。其运行速度在很大程度上取决于编译器和平台，Windows 与 32 位构建通常比优化后的 x64 Linux clang 构建慢得多。

hackernews · tosh · 9月7日 13:35 · [社区讨论](https://news.ycombinator.com/item?id=49598291)

**背景**: bzip2 于 1996 年首次发布，它将 Burrows-Wheeler 变换（BWT）、move-to-front 变换和 Huffman 编码应用于 100–900 kB 的数据块；它处理文本和源代码尤其有效，但比 gzip 和现代编解码器慢。bzip3 对这一思路进行了现代化改造：使用后缀数组来计算 BWT，加入 LZP 预处理，并采用上下文混合进行熵编码，目标是同时获得更高的压缩比和更快的解压速度。zstd 等通用压缩器使用基于 LZ77 的匹配和熵编码，并通过窗口大小参数控制压缩器在查找重复数据时可以回溯多远。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bzip2">Bzip2</a></li>
<li><a href="https://github.com/ShawSumma/bzip-three-for-you-and-me">ShawSumma/bzip-three-for-you-and-me - GitHub BZip3: Compresses More, Decompresses Faster Than BZip2 bzip3 man - Linux Command Library Software:Bzip3 - HandWiki bzip3 - an efficient statistical file compressor and ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者普遍对 bzip3 持欢迎态度，有人贴出作者关于 Burrows-Wheeler 变换的详细解释，并指出该工具已进入大型文本压缩基准榜。主要批评意见是官方基准看起来有失公平：bzip3 使用了 512 MiB 的块大小，而 zstd 的窗口仍保持默认值；由多个 Perl 源码版本串成的语料也恰好是 BWT 类压缩器最擅长的情况。还有用户建议用更大的 zstd 窗口和 long-range 模式重新测试；另一些评论则讨论实际归档中的取舍，例如 LZMA 压缩 JSONL 比 gzip 更好，但缺少通用软件的透明支持。

**标签**: `#compression`, `#bzip3`, `#zstd`, `#benchmarks`, `#open-source`

---

<a id="item-12"></a>
## [互联网档案馆 9 月定期捐赠享 3 倍匹配](https://blog.archive.org/2026/09/01/keep-our-servers-running-your-recurring-donation-goes-3x-this-september/) ⭐️ 6.0/10

2026 年 9 月，互联网档案馆发起题为“保持我们的服务器运行”的募捐呼吁，承诺当月定期捐赠将获得 3 倍匹配。该活动鼓励支持者设置月度经常性捐款，以帮助支付该非营利组织的服务器和数字保存工作。 互联网档案馆是数字保存的重要基础设施，托管着数十亿网页、书籍和媒体，依赖公众支持维持运营。针对定期捐赠的 3 倍匹配能显著增强该组织可预测的长期资金，最终使 archive.org 和 Open Library 的用户受益。 评论者指出，匹配捐赠机制可能与 501(c)(3)公共支持比例要求有关：小额捐赠者的捐款使慈善机构能够接受相应的大额匹配捐赠，一位评论者称这一比例为 1:2 匹配。他们还提出了实际顾虑，例如没有人工邮件请求就很难取消定期捐赠、缺少欧盟地区的捐赠收据选项，以及长期存在的技术问题，如收藏上传系统泄露电子邮件地址和 Open Library 的 Solr 性能问题。

hackernews · sonicrocketman · 9月7日 03:29 · [社区讨论](https://news.ycombinator.com/item?id=49593563)

**背景**: 互联网档案馆是一个非营利数字图书馆，免费提供存档网页、书籍、音频和软件，包括著名的 Wayback Machine（网页时光机）。Open Library 是互联网档案馆旗下的可编辑在线目录项目，目标是“为每本出版过的书创建一个网页”，目前提供超过 300 万本书供阅读、借阅和发现。作为一个非营利组织，互联网档案馆依靠公众捐款和资助，本月活动利用了匹配捐赠承诺来倍增定期捐赠。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open_Library">Open Library</a></li>
<li><a href="https://openlibrary.org/">Welcome to Open Library | Open Library</a></li>

</ul>
</details>

**社区讨论**: 总体而言，评论者对互联网档案馆表示支持，许多人定期捐款，但也表达了对取消捐赠困难、缺少欧盟捐赠收据选项以及长期技术问题削弱信任的担忧。一位长期在 Open Library 做志愿者的用户鼓励有经验的专业人士加入，指出特别需要帮助改进 Solr 性能等项目。另一位评论者解释称，匹配机制与 501(c)(3)“公共支持”规则有关，即使运作机制间接，匹配仍然是真实的。

**标签**: `#Internet Archive`, `#digital preservation`, `#fundraising`, `#open library`, `#non-profit`

---

<a id="item-13"></a>
## [泄露邮件揭示比尔·盖茨安装 Movie Maker 屡屡受挫](https://www.techemails.com/p/bill-gates-tries-to-install-movie-maker) ⭐️ 6.0/10

TechEmails 曝光的一封 2003 年邮件链显示，比尔·盖茨在安装 Windows Movie Maker 时屡屡失败，引发内部争论，暴露出微软在易用性上的严重问题以及高管之间互相推诿。 此事的意义在于，连微软最高领导人当时都无法顺利完成自家产品的安装，说明问题并非个别缺陷，而是系统性的设计与组织文化失败。它印证了外界长期以来对微软用户体验差和内部各自为政的批评，在讨论科技公司问责文化时仍具有现实意义。 在邮件链中，高管们没有直接解决问题，而是互相推责并提出成立委员会。评论区认为这体现了零问责、零担责和零后果的文化，并指出这正是优秀产品走向失败或沦为噩梦的原因。

hackernews · highfrequency · 9月7日 15:27 · [社区讨论](https://news.ycombinator.com/item?id=49599481)

**背景**: Windows Movie Maker 是微软面向 Windows 桌面个人电脑用户的消费级视频编辑软件。它曾因简单易用而广受欢迎，但如今已经过时、不再受支持，下载使用也不够安全。微软已于 2017 年正式停止支持 Movie Maker，并用此前名为 Microsoft Story Remix 的 Video Editor（视频编辑器）取代了它。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.movavi.com/windows-movie-maker-review.html">Windows Movie Maker Review 2026 – Pros and Cons, Pricing</a></li>
<li><a href="https://www.anymp4.com/video-editing/windows-movie-maker-review.html">A Comprehensive Windows Movie Maker Review in 2026</a></li>
<li><a href="https://www.wikihow.com/Use-Windows-Movie-Maker">How to Download & Use Windows Movie Maker on any PC</a></li>

</ul>
</details>

**社区讨论**: Hacker News 评论区普遍认为这封邮件链是“零问责”的典型：高管们四处推责、提议成立委员会而不是解决问题。还有评论将批评延伸到今天的微软，提到使用 Azure 时遇到的困惑与报错；也有人认为盖茨本人难辞其咎，并指出邮件中的 Mike Beckerman 后来成为 TikTok 说客的讽刺之处。

**标签**: `#Microsoft`, `#design`, `#usability`, `#tech-culture`, `#email-history`

---

<a id="item-14"></a>
## [Rustuna：用 Rust 打造的高性能 Optuna 实现已发布](https://www.reddit.com/r/MachineLearning/comments/1w9nyhz/rustuna_a_highperformance_rust_implementation_of/) ⭐️ 6.0/10

Optuna 团队发布了 Rustuna——一个用 Rust 原生编写的高性能、低内存占用的 Optuna 实现。它保留了 Optuna 熟悉的 API 和概念，同时消除 Python 依赖以降低供应链风险。 此次发布为超参数优化生态带来了 Rust 在性能和安全性方面的优势，有望推动更高效、更安全的机器学习基础设施。对于希望在 Rust 系统中嵌入优化功能或担忧 Python 供应链风险的用户来说，这一发布尤其意义重大。 Rustuna 托管在 GitHub（github.com/optuna/rustuna）上，并通过 Medium 博客文章正式发布。它被设计为兼容 Optuna 的重写实现，利用 Rust 原生内存管理进行优化，但公告中未提供具体的基准测试数据或详细的功能对照清单。

reddit · r/MachineLearning · /u/c-bata · 9月7日 10:01

**背景**: Optuna 是一款面向机器学习的自动超参数优化框架，以其 define-by-run API 著称，用户可以动态构建搜索空间。超参数优化是指调整模型训练前设置（如学习率）这类无法从数据中直接学习到的参数的过程。Rustuna 在保留 Optuna 接口和设计理念的基础上用 Rust 重写，旨在提升速度、内存效率，并通过不依赖 Python 来增强供应链安全。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://optuna.org/">Optuna - A hyperparameter optimization framework</a></li>
<li><a href="https://github.com/optuna/optuna">Optuna: A hyperparameter optimization framework - GitHub Optuna: A hyperparameter optimization framework — Optuna 4.9. ... Optuna: A hyperparameter optimization framework — Optuna 3.6. ... Optuna: A hyperparameter optimization framework - GitHub [1907.10902] Optuna: A Next-generation Hyperparameter ... Optuna | Proceedings of the 25th ACM SIGKDD International ...</a></li>

</ul>
</details>

**标签**: `#Rust`, `#Hyperparameter Optimization`, `#Optuna`, `#Machine Learning Infrastructure`, `#Performance`

---

<a id="item-15"></a>
## [PINNStudio：用于物理信息神经网络的免费开源无代码图形界面](https://www.reddit.com/r/MachineLearning/comments/1w9a2i7/pinnstudio_a_free_opensource_nocode_gui_for/) ⭐️ 6.0/10

一位开发者发布了 PINNStudio，这是一个免费开源的无代码图形界面，用户无需编写样板代码即可定义、训练和可视化物理信息神经网络。该工具会自动生成基于 DeepXDE 的代码、运行模型，并在应用内实时展示损失曲线和解图像。 这件事很重要，因为它降低了学生和科研人员在科学机器学习领域的编程门槛，让他们专注于物理问题而非代码实现细节。它有望加快 PINN 的实验迭代，并帮助这一方法在经验丰富的程序员之外获得更广泛的应用。 主要功能包括 PDE 定义、1D 或 2D 域上的耦合多输出 PDE 方程组、边界与初始条件、自定义网络架构与训练计划，并支持正问题和反问题。内置模板涵盖 Heat、Allen-Cahn 和 Cahn-Hilliard 等经典方程，用户可通过 pip install pinnstudio 进行安装。

reddit · r/MachineLearning · /u/Impossible-Jello2749 · 9月6日 22:19

**背景**: 物理信息神经网络（PINN）是一种在训练时遵守偏微分方程所描述的物理规律的神经网络，用于求解监督学习任务。通过把物理知识作为正则化项嵌入，PINN 即便在训练数据较少时也能很好地泛化，因此在数据稀缺的工程和生物问题中很有价值。科学机器学习（SciML）将领域科学与机器学习相结合，但传统上搭建一个新的 PINN 问题需要编写 PDE、边界条件、网络架构和训练计划等代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Physics-informed_neural_networks">Physics-informed neural networks</a></li>
<li><a href="https://www.sciencedirect.com/science/article/pii/S0021999118307125">Physics-informed neural networks: A deep learning framework ...</a></li>

</ul>
</details>

**标签**: `#PINNs`, `#open-source`, `#scientific machine learning`, `#GUI`, `#deep learning`

---

<a id="item-16"></a>
## [苹果调整欧盟替代应用商店收费：替代支付佣金最高 20%](https://t.me/zaihuapd/43648) ⭐️ 6.0/10

苹果宣布自 10 月 1 日起修订欧盟开发者条款，将按安装次数收取的核心技术费改为对通过 App Store 以外渠道分发的应用内数字交易收取 5%核心技术佣金。在 App Store 内使用替代支付方式的应用需缴纳 20%佣金，小企业计划下可降至 10%，并取消原有初始获取费和商店服务费。 此举是苹果为遵守欧盟《数字市场法》而做出的调整，此前收费结构一直受到欧盟委员会审查。新收费可能显著降低以 App Store 外部分发为主的开发者的成本，同时苹果仍从替代支付中保留佣金。 5%核心技术佣金仅适用于通过替代应用市场或网页分发的应用内的数字交易，取代了原先针对达到极大规模开发者的按安装次数收取的核心技术费。新条款取消了初始获取费和商店服务费，自 10 月 1 日起生效。

telegram · zaihuapd · 9月7日 02:24

**背景**: 欧盟《数字市场法》（DMA）将苹果等大型平台列为“守门人”，要求其允许 iOS 上使用替代应用商店和替代支付方式。此前苹果在欧盟条款中设置了“核心技术费”，即对达到极大规模开发者按每次安装收费，这一结构曾受到批评。苹果称，新的 5%统一佣金更加简单，认了其工具和服务提供的价值，同时更好地满足 DMA 的要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.apple.com/newsroom/2026/08/apple-announces-changes-for-apps-in-the-european-union/">Apple announces changes for apps in the European Union</a></li>
<li><a href="https://applemagazine.com/core-technology-fee-ends-five-percent-eu-commission/">Apple Ends Core Technology Fee With New 5% EU Commission ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/EU_Digital_Markets_Act">EU Digital Markets Act</a></li>

</ul>
</details>

**标签**: `#Apple`, `#EU`, `#App Store`, `#Developer Fees`, `#Digital Markets Act`

---

<a id="item-17"></a>
## [国内首份办公 Agent 用户行为报告：前 20%用户消耗 87.4%算力](https://36kr.com/newsflashes/3972905839227142) ⭐️ 6.0/10

今天发布的国内首份《中国办公 Agent 用户行为不完全报告》显示明显的“头部效应”：前 20% 的用户消耗了 87.4% 的算力，其中前 5% 的用户独占 53.5% 的 token 消耗。该数据基于网易 LobsterAI 的真实用户行为。 这是首批基于真实数据刻画办公 AI Agent 实际使用情况的报告之一，揭示了少数重度用户贡献大部分算力并推动付费转化的幂律分布特征。这些发现为企业级 AI 厂商在快速增长的 Agent 市场中制定定价、容量规划和功能设计提供了现实依据。 付费用户表现出极高的黏性：其在 token 消耗、任务量和月活跃天数上分别达到免费用户的 6.2 倍、5.2 倍和 3.0 倍，表明重度使用是付费的主要驱动力。此外，单次任务规模在 5 个月内增长 3.1 倍，8 月环比增幅达 53%。

telegram · zaihuapd · 9月7日 06:18

**背景**: 办公 Agent 产品（如网易有道的 LobsterAI）是基于 OpenClaw 生态构建的桌面级 AI 助手，可以在真实桌面上运行工具，并通过微信、飞书、钉钉和 Telegram 等应用从手机远程下达指令，完成数据分析、PPT、文档、视频和网页研究等任务。Token 消耗是大语言模型的基本计费和使用单位，因此 token 使用的高度集中意味着少数重度用户贡献了绝大部分算力负载。《中国办公 Agent 用户行为不完全报告》是国内首批基于真实用户行为数据的办公 Agent 采用情况快照，而非问卷调查结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lobsterai.youdao.com/">LobsterAI（有道龙虾）- 网易有道全场景办公助手 Agent</a></li>
<li><a href="https://github.com/netease-youdao/LobsterAI">GitHub - netease-youdao/LobsterAI: Open-source, desktop-grade ...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#user behavior`, `#enterprise AI`, `#compute usage`, `#China tech`

---

<a id="item-18"></a>
## [ChatGPT 重创内罗毕论文代写业，4 万人受影响](https://the-decoder.com/how-ai-wiped-out-an-entire-industry-in-nairobi/) ⭐️ 6.0/10

The Decoder 的一篇报道显示，ChatGPT 已严重冲击肯尼亚内罗毕的论文代写行业；该行业曾至少有 4 万人为美国和英国大学的海外学生代写论文。自 2022 年 ChatGPT 推出以来，订单量与价格大幅下跌，部分从业者转而从事“降查重”服务，试图让 AI 文本绕过检测。 这表明生成式 AI 对全球零工经济中的特定领域造成了切实的社会经济冲击，数万名依赖学术代写的从业者受到波及。同时，它也凸显了 AI 文本生成与 AI 检测之间不断升级的博弈，对学术诚信和数字劳动力市场都有深远影响。 报道称，代写论文涉及医学、计算机科学和工程等领域。部分原代写者现在转向将 AI 文本“人性化”或绕开 AI 检测，而内罗毕的转录、数据标注和内容审核等其它线上工作机会也在减少。

telegram · zaihuapd · 9月7日 14:24

**背景**: ChatGPT 是一种生成式 AI 聊天机器人，可按需生成接近人类写作的文本；2022 年发布后，它迅速成为定制学术论文的廉价替代品。AI 检测工具通过扫描文本的困惑度、突发性、用词风格的规律性以及词概率分布等信号，判断内容是否由 AI 生成。作为回应，AI“人性化”工具会将 AI 文本改写得更自然，因此一些原代写者转而提供“人性化”AI 论文、绕过查重软件的服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gptinf.com/blog/how-do-ai-detectors-work-understanding-the-methods-and-accuracy">How Do AI Detectors Work ? Understanding the Methods and Accuracy</a></li>
<li><a href="https://quillbot.com/ai-humanizer">Humanize AI Text: Free AI Humanizer by Quillbot</a></li>

</ul>
</details>

**标签**: `#ChatGPT`, `#AI Impact`, `#Employment`, `#Kenya`, `#Academic Integrity`

---