---
layout: default
title: "Horizon Summary: 2026-09-23 (ZH)"
date: 2026-09-23
lang: zh
---

> 从 39 条内容中筛选出 25 条重要资讯。

---

1. [OpenAI 发布 GPT-6 Sol 与 Luna，API 价格几乎腰斩](#item-1) ⭐️ 9.0/10
2. [Anthropic 发布 Claude Opus 5.5，token 定价全面下调](#item-2) ⭐️ 9.0/10
3. [五角大楼：过度依赖 AI 是伊朗学校遭导弹袭击的部分原因](#item-3) ⭐️ 9.0/10
4. [vLLM v0.30.0 发布：Fast Start IPC 权重缓存与大量新模型支持](#item-4) ⭐️ 8.0/10
5. [Claude Opus 5.5 基准评测分析：成本下降与可靠性担忧并存](#item-5) ⭐️ 8.0/10
6. [25 位菲尔兹奖得主警告 AI 或偏离数学研究目标](#item-6) ⭐️ 8.0/10
7. [OpenAI 开启 GPT-5.6 系列有限预览：Sol、Terra 与 Luna](#item-7) ⭐️ 8.0/10
8. [苹果在 iOS 中植入常驻广告，引发用户不满](#item-8) ⭐️ 7.0/10
9. [TypeSafe AI 发布 Jev：输出结构化概率决策而非文本的“决策模型”](#item-9) ⭐️ 7.0/10
10. [Cloudflare Python Workers 结束两年预览期正式全面可用](#item-10) ⭐️ 7.0/10
11. [小米发布 MiMo-V2.6 全模态模型，RL 训练成本仅 350 万美元](#item-11) ⭐️ 7.0/10
12. [Complex KDA：扩展 Kimi Delta Attention 的表达能力](#item-12) ⭐️ 7.0/10
13. [Qonto 发布 QontoFAQ 检索基准与相关性指标](#item-13) ⭐️ 7.0/10
14. [抖音上线理财板块，支持购买基金与券商开户](#item-14) ⭐️ 7.0/10
15. [阿里发布真武 V900 AI 芯片，宣称算力达 M890 三倍](#item-15) ⭐️ 7.0/10
16. [DeepSeek 发布 DSec 沙箱平台技术报告：每日 300 万沙箱支撑智能体训练](#item-16) ⭐️ 7.0/10
17. [Mimo CLI 被曝存在潜在数据收集功能](#item-17) ⭐️ 7.0/10
18. [中国监管机构调查 DeepSeek 与月之暗面数据泄露指控](#item-18) ⭐️ 7.0/10
19. [DeepSeek 本周将向联合国安理会通报 AI 风险](#item-19) ⭐️ 7.0/10
20. [报告称 GPT-6 "Astra" 破解自 2005 年悬而未决的 Enigma 电文，引发争议](#item-20) ⭐️ 6.0/10
21. [GrapheneOS 暗示最早 2027 年将有预装该系统的设备出货](#item-21) ⭐️ 6.0/10
22. [LinearSolveBench：评估 AI 编写 C 语言稀疏线性求解器的新基准](#item-22) ⭐️ 6.0/10
23. [Templar 用「阶段跳过」模拟流水线并行预训练的容错能力](#item-23) ⭐️ 6.0/10
24. [美国提议与中方建立 AI 事件通报渠道](#item-24) ⭐️ 6.0/10
25. [iOS 27.2 Beta 2 疑似新增中国大陆特供传感器权限](#item-25) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6 Sol 与 Luna，API 价格几乎腰斩](https://openai.com/index/introducing-gpt-6-sol-and-luna/) ⭐️ 9.0/10

OpenAI 发布了 GPT-6 模型家族——GPT-6 Sol 与 GPT-6 Luna，即日起在 ChatGPT Work 和 Codex 中面向所有 Plus、Pro、Business、Enterprise 和 Edu 用户开放，Free 和 Go 用户可在桌面应用中访问 GPT-6 Luna（这两个模型暂未上线 Chat）。它们在 API 中的名称是 gpt-6-sol 和 gpt-6-luna，其中 Sol 面向复杂编程与智能体（agentic）工作流，Luna 则定位为处理高并发、聚焦型任务时最高效的模型。 OpenAI 将 token 价格相对 5.6 代下调了一半甚至更多，这直接改变了开发者运行长时间智能体编程循环时的单任务成本结构，官方将降价归因于缓存与推理效率的改进。Sol 的定价为每百万输入/输出 token 2 美元/10 美元，而 Claude Opus 5.5 的费率要高得多，因此这次发布加剧了前沿模型厂商之间的价格战，尽管它在顶端编程基准上略逊于自家上一代模型。 GPT-6 Sol 的价格为每百万输入/输出 token 2 美元/10 美元，而 GPT-5.6 Sol 为 4 美元/20 美元；GPT-6 Luna 的输入价格比 GPT-5.6 Luna（0.20 美元/1.20 美元）低 50%，输出价格低 58.3%。代价也是实实在在的：相比 GPT-5.6 Sol，Sol 在顶端 DeepSWE 性能上大约让出 4 分，换来单任务成本降低 58%；在 OpenAI 内部的真实性评估中，它的错误量约为前代的一半，以低得多的成本达到 Astra 级别的可靠性。

hackernews · OfficialTurkey · 9月22日 18:00 · [社区讨论](https://news.ycombinator.com/item?id=49805509)

**背景**: 大语言模型厂商通常按每百万 token 计费，分为输入（你发送的内容）和输出（模型生成的内容），而输出 token 的价格往往是输入的数倍。"Sol" 和 "Luna" 是 OpenAI 6 系列的两个档位：前者更大更强，用于高强度的编程和智能体任务；后者更便宜更快，用于高并发场景。Codex 和 ChatGPT Work 是 OpenAI 面向开发者和企业的产品界面，在这些场景中，智能体编程（模型自主修改文件、运行测试并迭代）已让推理成本成为首要考量。OpenAI 还公布了一项提示注入（prompt injection）安全结果：在一个人为植入未授权指令的模拟留言板上，Sol 在发现该留言板的运行中有 11.3% 执行了指定操作，而上一代模型为 51.9%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-sol-and-luna/">Introducing GPT-6 Sol and Luna | OpenAI</a></li>
<li><a href="https://techcrunch.com/2026/09/22/openai-launches-gpt-6-sol-and-luna/">OpenAI launches GPT-6 Sol and Luna, boasting lower cost and fewer mistakes | TechCrunch</a></li>
<li><a href="https://venturebeat.com/technology/openai-releases-gpt-6-sol-and-luna-models-slashing-api-costs-50-or-more">OpenAI releases GPT-6 Sol and Luna models, slashing API costs 50% or more | VentureBeat</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者高度聚焦定价：simonw 称 GPT-6 Luna 只要 GPT-5.6 Luna 一半的价格"是件大事"，并贴出 Sol、Luna 和 Astra 生成的 SVG 鹈鹕对比图；pookieinc 则认为与 OpenAI 的新产品相比，Claude 的 Opus 定价已显得缺乏竞争力。jeffnash 表示在 Claude Code 20x 与 Codex Pro 20x 之间做选择，决定性因素是使用额度与重置窗口，目前 Codex 遥遥领先；m_fayer 则表达了更感性的顾虑——他已经对 5.6 Sol 的沟通风格和工程直觉产生依赖，担心技术上更强的后继模型用起来不会那么顺手。

**标签**: `#OpenAI`, `#GPT-6`, `#LLM`, `#AI models`, `#pricing`

---

<a id="item-2"></a>
## [Anthropic 发布 Claude Opus 5.5，token 定价全面下调](https://www.anthropic.com/claude-opus-5-5) ⭐️ 9.0/10

Anthropic 发布了新一代前沿模型 Claude Opus 5.5，相比 Opus 5 全面下调了 API 的 token 价格：每百万 token 的缓存读取从 0.50 美元降至 0.20 美元，输入 token 从 5 美元降至 4 美元，输出 token 从 25 美元降至 20 美元，缓存写入从 6.25 美元降至 5 美元。Anthropic 还表示 Opus 5.5 的沟通表达比前代更自然，会把最重要的信息放在前面，使其更适合长时间协作。 此次降价针对的可能是 OpenRouter 上支出最高的模型，因此更便宜的 Opus token 会直接降低重度 agent 与编程工作负载的成本，并加剧与 DeepSeek 等“便宜但能干”的对手之间的价格竞争。这件事在象征意义上同样重要：Anthropic 将该版本称为其公开发出“为前沿减速”呼吁之后的首次发布，而这一矛盾立即被社区抓住。 发布说明的第一句就是“Claude Opus 5.5 是我们呼吁为前沿减速以来的首个发布”，而 Anthropic 所宣称的表达改进也得到了早期测试者的背书，有人说“它写东西就像我自己在写”。有评论者指出，Opus 5 在 OpenRouter 的任务支出榜上排名第一，说明真正的战场是实际花费，而不仅仅是基准测试分数。

hackernews · km144 · 9月22日 16:29 · [社区讨论](https://news.ycombinator.com/item?id=49803892)

**背景**: 所谓“前沿模型”，指的是在某一时刻最先进的一批 AI 模型，它们用海量数据和巨大算力训练，能在众多任务上达到最领先的水平。由于这类模型按 token 计费——输入、输出和缓存上下文分别定价，缓存读取通常远低于新输入——因此即便每个 token 只降一点点，在大规模使用下也能省下可观成本。“为前沿减速”（pacing the frontier）则来自 Anthropic CEO Dario Amodei 在 2026 年 9 月发表的《We Must Pace the Frontier》一文，主张业界应有意放缓最强系统的研发速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>
<li><a href="https://www.pacingthefrontier.com/">Pacing the Frontier</a></li>

</ul>
</details>

**社区讨论**: 这条拥有 662 条评论的 Hacker News 讨论主要围绕两个主题：对降价的欢迎，以及对 Anthropic 叙事的质疑。最尖锐的批评是，发布说明第一句搬出“为前沿减速”，而后面却用非常具体的数据证明 Anthropic 恰恰在做相反的事；也有评论者表示自己乐于继续使用 DeepSeek v4.1 这类便宜得多的替代品，还有人调侃了例行的“鹈鹕图”基准测试。

**标签**: `#AI`, `#LLM`, `#Anthropic`, `#Claude`, `#Pricing`

---

<a id="item-3"></a>
## [五角大楼：过度依赖 AI 是伊朗学校遭导弹袭击的部分原因](https://www.bloomberg.com/graphics/2026-iran-school-attack/) ⭐️ 9.0/10

五角大楼的一份报告认定，美国“未能履行一切可行手段去核实”伊朗米纳布一所学校属于军事目标的义务，且这一失误“超出了单纯疏忽的范畴”，并将此次致命打击部分归因于对 Project Maven 等 AI 目标筛选工具的过度依赖。报告称，米纳布这处地点因数据过时而被标注为伊斯兰革命卫队设施，与其他候选目标一并输入 Maven 后，被列为建议的首日打击目标。 这是首批将致命平民伤亡事件直接与 AI 辅助目标筛选联系起来的官方结论之一，动摇了“只要保留人类在环（human-in-the-loop）就能满足战争法律与伦理义务”的假设。此事很可能加严对军事 AI 供应商的审查，并推动对 AI 驱动杀伤链速度以及自主武器国际监管的讨论。 报告指出，过去需要数小时的目标清单工作被压缩到几分钟内完成，而部分用户以为 Maven 会自行标记情报中的过时记录或矛盾之处——不过官员表示，不清楚他们为何会这么认为。五角大楼与 Palantir 似乎在相互推责，一方指向软件，另一方指向糟糕的输入数据，而该地点被错误标注的根源则来自一条过时的目录记录。

hackernews · devonnull · 9月22日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49806430)

**背景**: Project Maven（Maven Smart System）是美国国防部的一项 AI 决策支持项目，它摄取情报并帮助分析人员和操作员汇总、排序潜在目标，这类工具也被称为 AI 决策支持系统（AI-DSS）。在标准的“人类在环”模式下，任何打击都必须由人类授权，各国政府据此认为国际人道法下的法律责任得以保留，而该法要求区分民用与军事目标并采取可行预防措施。批评者则反驳说，随着 AI 将目标筛选周期从数天压缩到数分钟，人类可能只是对机器建议盖章放行，而非真正核实，这也是全球围绕致命性自主武器系统（LAWS）争论的核心问题之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://onthewire.ai/article/human-in-the-loop-or-loophole">Human in the loop , or loophole? The phrase holding up the AI -war...</a></li>
<li><a href="https://opiniojuris.org/2026/04/13/beyond-anthropics-red-line-human-in-the-loop-and-the-illusion-of-legitimacy-in-ai-decision-support-systems/">Beyond Anthropic’s Red Line: Human - in - the - Loop and... - Opinio Juris</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lethal_autonomous_weapon">Lethal autonomous weapon - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者大多不认同把 AI 当作罪魁祸首，他们认为过时的数据和人类下放决策权的决定才是真正的根源——“AI 无法在法庭上受审”，因此每一项行动都必须有可追责的人类。有评论批评这是在优化错误的指标（即目标清单生成速度），并指出五角大楼与 Palantir 之间存在明显的相互推责；也有人表示，那些不了解 AI 盲区的人本就不该对系统抱有全盘信任。

**标签**: `#AI Ethics`, `#Military AI`, `#AI Accountability`, `#Autonomous Systems`, `#AI Limitations`

---

<a id="item-4"></a>
## [vLLM v0.30.0 发布：Fast Start IPC 权重缓存与大量新模型支持](https://github.com/vllm-project/vllm/releases/tag/v0.30.0) ⭐️ 8.0/10

vLLM 发布了 v0.30.0，这是一个包含 315 位贡献者（其中 104 位是新贡献者）提交的 762 个 commit 的大型版本，新增支持包括 DeepSeek-V4.1-Flash、DeepSeek-V4-Flash-Vision-Exp、GLM-5.3-Flash、K2-Horizon、Cohere Compass、Bailing V3 VL 和 Nanbeige4.2 在内的众多新模型。本次最核心的基础设施变更是 "Fast Start"：一个常驻的每 GPU 权重缓存守护进程，把量化后、按张量并行（TP）切分好的权重保留在 GPU 显存中，引擎重启时可通过 `--load-format ipc_cache` 走 CUDA IPC 直接映射，而不再从磁盘重新加载；该能力现已扩展到 FP4 checkpoint 和多节点 TP 场景。 vLLM 是目前部署最广泛的开源 LLM 推理与服务引擎之一，因此它的版本更新会直接影响自建 AI 基础设施的成本与延迟表现。Fast Start 针对的是一个真实痛点——引擎重启耗时过长，会拖慢强化学习 rollout、自动扩缩容以及集群重配置；而大量新模型的支持则有助于让 vLLM 继续充当新发布开放权重模型的默认服务层。 除新模型外，该版本还加入了针对生成文本的 Gumbel-max 水印（支持按请求关闭，且采用双密钥以便兼容投机解码）；新增 "HiSparse"——面向稀疏 MLA 解码的宿主内存分层机制，在 GPU 显存紧张时把 KV 页溢出到锁页主机内存，并通过 `HiSparseConnector` 用每请求的 GPU 热缓冲区服务 top-k 未命中。Model Runner V2 也有大量改进，其中在 CUDA graph 捕获期间冻结垃圾回收后，H200 上的捕获时间从 12 秒降到 2 秒、引擎初始化从 28.9 秒降到 8.2 秒。针对 Qwen3.8-Flash-Next 和 Kimi K3 的性能优化同样可观，例如分组 FP8 MLA 缓存插入带来 4-6 倍 kernel 加速，DSV3 低延迟 GEMM 在跨步张量上提速 12-81%。

github · khluu · 9月22日 05:20

**背景**: vLLM 是面向大语言模型的开源推理与服务引擎，以高效显存管理（KV cache）和高吞吐批处理著称。此类版本往往把社区贡献与底层 GPU kernel 工作打包在一起：MXFP8 是一种微缩放块浮点格式，让一组 8 位数值共享同一个指数以节省显存；FlashMLA 是针对 NVIDIA GPU 优化的 Multi-Latent Attention 解码 kernel；DeepGEMM 则是 DeepSeek 的高性能 FP8/FP4/BF16 GEMM kernel 库，用于大模型的训练与推理。权重加载和引擎启动往往受限于读取并重新量化数 GB 的 checkpoint，而这正是新的 IPC 权重缓存想要避免的开销。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MXFP8">MXFP8</a></li>
<li><a href="https://github.com/deepseek-ai/DeepGEMM">GitHub - deepseek-ai/ DeepGEMM : DeepGEMM : clean and efficient...</a></li>
<li><a href="https://www.deepep.org/en/flashmla">FlashMLA</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#model serving`, `#AI infrastructure`, `#release`

---

<a id="item-5"></a>
## [Claude Opus 5.5 基准评测分析：成本下降与可靠性担忧并存](https://artificialanalysis.ai/models/claude-opus-5-5) ⭐️ 8.0/10

Artificial Analysis 发布了针对 Anthropic 的 Claude Opus 5.5 在“max”推理档位下的专门评测页面，从智能水平、输出速度/延迟以及价格等维度对该模型进行基准测试。该站同时提供“xhigh”档位的页面，而“medium”档位是该模型的默认设置。 这类独立基准测试是开发者和团队选择将生产负载交给哪个模型的重要依据，因此报告中相对 Opus 5 每任务成本减半的结论，可能直接影响他们转向 Anthropic 最新旗舰模型的采购决策。随附的 Hacker News 讨论还反映出更广泛的行业担忧：发布初期的基准成绩在数周后未必还能维持。 有评论者指出“max”并非默认档位，并且至少一位用户报告称，一个简单提示（“生成一只骑自行车的鹈鹕的 SVG”）两次失败，原因是模型在仍在推理时就用尽了 128,000 token 的预算。在成本方面，一位评论者提到，在高投入档位对高投入档位的比较中，每任务成本约为 Opus 5 的一半。

hackernews · theanonymousone · 9月22日 16:51 · [社区讨论](https://news.ycombinator.com/item?id=49804316)

**背景**: Artificial Analysis 是一个独立基准测试网站，它汇总数学、科学、编程和推理等多类评测，为各类 AI 模型与 API 提供商生成可比较的智能水平、速度、延迟和价格指标。像 Claude Opus 这类现代推理模型会提供可调节的“推理强度（reasoning effort）”档位（例如 medium、xhigh 和 max），用更多内部思考 token 换取更高的准确率。由于更高强度会消耗更多 token，token 预算和每任务价格都成为开发者必须权衡的实际约束。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models">Comparison of AI Models across Intelligence, Performance, and Price | Artificial Analysis</a></li>
<li><a href="https://artificialanalysis.ai/evaluations">AI Model Evaluations | Artificial Analysis</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论更偏实用而非赞美：simonw 报告说 max 档位消耗了 128,000 个 token 却仍未完成一个简单的 SVG 任务；breckenedge 质疑评测是否会在发布数周后重跑，并称内部复测显示某模型出现性能回退；linuxrebe1 则表示自己已回退到 Opus 4.8，因为它在遵循指令和保持任务专注方面优于 Opus 5。正面意见方面，hglaser 强调其每任务成本比 Opus 5 低约 50%，但 khalic 认为相较于同价位模型它依然显得昂贵。

**标签**: `#Claude Opus`, `#AI model evaluation`, `#Anthropic`, `#LLM performance`, `#AI pricing`

---

<a id="item-6"></a>
## [25 位菲尔兹奖得主警告 AI 或偏离数学研究目标](https://t.me/zaihuapd/43973) ⭐️ 8.0/10

包括陶哲轩、邓煜在内的 25 位菲尔兹奖得主发表联合声明，警告将 AI 迅速用于解决数学问题，可能导致 AI 发展目标与数学研究目标出现“严重错位”。声明指出，大型语言模型解决重大数学问题的能力近年大幅提升，但把数学解题当作衡量 AI 能力的基准存在风险。 联署者均为数学界最具权威的学者之一，他们的共同警告很可能影响 AI 实验室、学术期刊与资助机构评估机器数学能力的方式，以及成果署名的规则。这促使 AI 界反思那些只奖励“给出答案”而非真正概念理解的评测基准，其影响波及科研评价、学术出版，以及更广泛的 AI 对齐讨论。 声明强调，数学研究的核心是形成概念理解与新洞见，而非单纯获得答案，并警告 AI 批量生成成果可能压缩用于验证、交流与引用前人成果的时间，同时引发署名和抄袭等问题。声明也承认 AI 有望提升数学研究效率，最终影响取决于人们如何使用这项技术。

telegram · zaihuapd · 9月22日 03:00

**背景**: 菲尔兹奖被普遍视为数学界的最高荣誉，每四年颁发一次，每次最多授予四位通常不满 40 岁的数学家，因此由 25 位得主联署发声是相当罕见的集体表态。近年来，大型语言模型在竞赛类和研究级数学问题上取得显著进展，AI 实验室常以此作为通用推理能力的证据。AI 对齐指研究如何确保 AI 系统的行为与人类价值观和意图保持一致，这份声明把该关切具体落到了数学领域。它是一份关于规范与激励机制的立场性声明，而非新的技术成果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://juejin.cn/post/7328766815101337619">第十六天： 对 齐 （Alignment）人工智能 对 齐 ： AI Alignment AI ...</a></li>
<li><a href="https://llmbook-zh.github.io/LLMBook.pdf">The chinese book</a></li>

</ul>
</details>

**标签**: `#AI and Mathematics`, `#Research Ethics`, `#Large Language Models`, `#Academic Publishing`, `#AI Alignment`

---

<a id="item-7"></a>
## [OpenAI 开启 GPT-5.6 系列有限预览：Sol、Terra 与 Luna](https://t.me/zaihuapd/43990) ⭐️ 8.0/10

据报道，OpenAI 已开始对 GPT-5.6 系列进行有限预览，该系列包括旗舰模型 Sol、均衡型 Terra 和低成本 Luna，先通过 API 和 Codex 面向少数可信合作伙伴提供。Sol 主打更强的编码、生物与网络安全能力，并新增 max 推理强度和 ultra 模式；Terra 性能据称接近 GPT-5.5 而价格约便宜一半，Luna 则定位为成本最低的选择。 这体现了 OpenAI 在 2026 年的分层模型策略：一端是带有昂贵高算力模式的顶级旗舰，另一端是主打价格竞争力的中低端模型，直接对标其他实验室。正在规划 API 预算的开发者和企业可能需要重新考虑自己以哪一档模型为标准；而“应美国政府要求”而设的受限发布，也让外界开始关注前沿模型访问权正如何被监管方介入。 根据第三方整理，ultra 模式并非更大的模型，而是悄悄并行运行约四个智能体并按四个计费，据称在 Terminal-Bench 2.1 上得分 91.9%，而单智能体 Sol 为 88.8%；max 推理强度则是为难题分配更多推理期算力。一个关键提醒是：该消息仅来自一条 Telegram 帖子，没有任何讨论或独立信源佐证，因此模型命名、定价和可用性细节都应视为未经证实。

telegram · zaihuapd · 9月22日 18:04

**背景**: GPT-5.6 被视为 OpenAI GPT-5.x 系列的下一步，采用三档命名：Sol 为旗舰，Terra 为均衡中档，Luna 为廉价低延迟档，大致相当于在前沿质量、通用性价比与大批量低成本之间做选择。max 之类的“推理强度”设置会让模型在作答前投入更多算力思考，通常能以更高成本提升高难度编码或研究任务的表现，而 ultra 模式则把多个智能体串联起来进一步推高基准分数。文中提到的 Codex 是 OpenAI 面向开发者的 AI 编码智能体套件，用于委派软件工程任务，因此优先在 Codex 上开放意味着这些模型首先在最看重编码质量的地方接受检验。所谓“应美国政府要求的短期步骤”，意味着预览先面向经过审核的合作伙伴，而非全面开放。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://emergent.sh/learn/gpt-5-6-sol-vs-terra-vs-luna">GPT - 5 . 6 Sol vs Terra vs Luna: Which Model Should You Use?</a></li>
<li><a href="https://tosea.ai/blog/gpt-5-6-sol-terra-luna-complete-guide">GPT - 5 . 6 Sol, Terra & Luna: Complete Guide to... | Tosea.ai</a></li>
<li><a href="https://www.eesel.ai/blog/gpt-5-6-sol">What is GPT - 5 . 6 Sol? OpenAI's flagship model explained | eesel AI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-5.6`, `#LLM`, `#AI模型发布`, `#API`

---

<a id="item-8"></a>
## [苹果在 iOS 中植入常驻广告，引发用户不满](https://www.techradar.com/phones/iphone/i-wish-apple-would-just-stop-that-crap-apple-has-added-persistent-ads-to-ios-and-its-driving-users-crazy) ⭐️ 7.0/10

苹果在 iOS 界面中引入了常驻广告，最明显的是 App Store：首页和搜索结果如今充斥着推广位，而不再只是更新页面相对干净。这一变化在 Hacker News 上引发大规模讨论（509 分、391 条评论），用户把广告、更新催促和激进的付费引导视为平台质量下滑的证据。 苹果长期把自己定位为相较 Android、Google 等广告驱动平台更高端、更注重隐私的选择，因此在核心系统界面植入常驻广告会侵蚀这一差异化优势以及用户对第一方应用的信任。考虑到 iOS 掌握了大量高消费移动用户，这一转变会影响开发者、广告主，以及所有认为“花钱买苹果硬件就该没有广告”的人。 抱怨主要集中在 App Store：用户指出首页和搜索页变成“广告灾难”，而应用更新页相对干净，只能通过长按 App Store 图标进入。评论者还把广告问题与 macOS/iOS 的更新行为相提并论，称苹果会显示常驻红点并反复弹窗催促，如果用户没有及时再次拒绝，系统甚至会覆盖其非同意而强行更新。

hackernews · MC995 · 9月22日 14:30 · [社区讨论](https://news.ycombinator.com/item?id=49801939)

**背景**: App Store 自 2016 年起就有搜索广告，但过去主要局限于搜索结果和“Today”标签页，大多数第一方界面没有推广内容。iOS 更新也通过系统通知和“设置”红点推送，苹果并未提供永久“永不更新”的开关，只有推迟或关闭自动安装的选项。这条新闻反映了更广泛的行业趋势：在硬件销售增长放缓时，厂商转向高利润的服务与广告收入。

**社区讨论**: 评论者普遍认同苹果的广告泛滥标志着其设计品味的退步，有人指出任何领导层更替都会被解读为在推翻 Tim Cook 时期加入的广告。其他人把批评延伸到强制更新催促、臃肿的原生应用和 iCloud 存储付费引导，还有用户表示在一台旧 M1 MacBook Air 上转投 Fedora Asahi Remix 作为出路——说明不满已不止于广告本身。

**标签**: `#Apple`, `#iOS`, `#Advertising`, `#User Experience`, `#Platform Policy`

---

<a id="item-9"></a>
## [TypeSafe AI 发布 Jev：输出结构化概率决策而非文本的“决策模型”](https://simonwillison.net/2026/Sep/21/jev/) ⭐️ 7.0/10

TypeSafe AI 发布了 Jev，这是其所谓“System One 模型”的第一个实例——这类模型接受文本或半结构化输入（由字符串、字符串数组或键值对组成的“state”对象），但输出的不是生成的文本，而是带类型的概率决策。它支持三类提问：是/否问题（称为“Noul”，即伯努利问题），返回 0 到 1 的置信度；选择问题，返回各选项上的概率分布；以及评分问题，返回某个数值区间内的浮点数评分。 如果决策模型被证明可靠，它们将指向一种不同的 LLM 部署模式：不再把文本生成器硬套到分类、排序或优先级判断任务上再解析其自然语言输出，而是让软件直接拿到一个带类型的数值。其经济性尤为突出——Jev 只对输入计费，价格为每百万 token 0.042 美元，输出免费——这比 OpenAI 的 GPT-5 Nano 更便宜，可能让大规模文档打分与重排序在经济上变得微不足道。 Jev 会对附在同一个 state 上的所有问题并行评估，因此问很多问题的延迟大致与只问一个问题相当，并且只按输入 token 计费。根据 TypeSafe 自己针对 Jev 1.13 的“jaggedness（参差不齐的能力边界）”文档，该模型目前在数字、日期和对抗性内容上表现不佳，这限制了它能安全承担的决策环节范围。

rss · Simon Willison · 9月21日 23:09

**背景**: “System One”借用了心理学家丹尼尔·卡尼曼对人类思维的划分：快速、自动、直觉式的“系统 1”与缓慢、审慎推理的“系统 2”。TypeSafe 把 Jev 定位为这对组合中快速、廉价、随时可用的那一半。传统 LLM 是自回归的 token 生成器：它们输出一段文本流，并分别按输入与输出 token 计费，这正是长回答昂贵的原因。而决策模型的行为更像经典的概率分类器——文本输入，输出经过校准的分数或标签分布——这正是它快速、便宜且便于普通软件直接消费的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">Introducing System One Models & Jev - TypeSafe AI Blog</a></li>
<li><a href="https://docs.typesafe.ai/concepts/system-one">System One - TypeSafe AI</a></li>
<li><a href="https://www.datacamp.com/blog/system-one-models-jev">Jev: TypeSafe's System One Model Explained | DataCamp</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上认可这一概念，但对命名提出了异议：Maggie Appleton 认为“决策模型（decision models）”比“System One 模型”更清晰，Simon Willison 也赞同这一看法。在 Hacker News 上，TypeSafe 的 CEO 确认“Noul”这一称呼来自伯努利（Bernoulli），而反复出现的担忧则是可解释性问题——Jev 只返回一个浮点数，因此无法追问输入中的哪些内容促成了垃圾邮件或相关性判断。

**标签**: `#LLM`, `#AI models`, `#decision models`, `#probabilistic inference`, `#model architecture`

---

<a id="item-10"></a>
## [Cloudflare Python Workers 结束两年预览期正式全面可用](https://simonwillison.net/2026/Sep/21/cloudflare-python-worker/) ⭐️ 7.0/10

9 月 21 日，Cloudflare 宣布 Python Workers 正式全面可用（GA），Python 由此成为 Cloudflare 开发者平台上的一级支持语言。此次发布原生支持 FastAPI、Django、Flask 等框架，并让 Python 代码可以直接接入 Workers AI、R2、D1 等平台服务。 Python 是全球使用最广泛的编程语言之一，一级支持为大量希望部署到边缘和 Serverless 环境的 Python 开发者清除了主要障碍。这也体现了 Cloudflare 对 Python 生态的长期投入——发布公告的署名者包括 Pyodide 核心维护者 Gyeongjae Choi 和 Hood Chatham。 Python 代码通过 Pyodide 编译为 WebAssembly，并在 Cloudflare 基于 V8 的 workerd 运行时中执行，因此 threading 和 multiprocessing 在 WebAssembly 虚拟机中无法工作。本地开发由 pywrangler 工具负责（在 PyPI 上以 workers-py 之名发布），它使用约 123MB 的 workerd 二进制文件在本地完整模拟整套技术栈。

rss · Simon Willison · 9月21日 22:25

**背景**: Pyodide 是将 CPython 移植到 WebAssembly/Emscripten 的产物，使 Python 包能够在类浏览器环境中安装和运行。workerd 是 Cloudflare 开源的、面向服务端的 JavaScript 与 WebAssembly 运行时，驱动着其 Serverless 边缘平台 Cloudflare Workers，同时也被 Wrangler 用于本地开发。将两者结合，Cloudflare 无需维护一套独立的原生 Python 解释器，就能在全球边缘网络上运行 Python。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pyodide.com/">Home - Pyodide</a></li>
<li><a href="https://flaviocopes.com/workerd/">How workerd , the Cloudflare Workers runtime, is built</a></li>
<li><a href="https://blog.cloudflare.com/workerd-open-source-workers-runtime/?ref=console.dev/">Introducing workerd : the Open Source Workers runtime</a></li>

</ul>
</details>

**标签**: `#cloudflare`, `#python`, `#webassembly`, `#serverless`, `#edge-computing`

---

<a id="item-11"></a>
## [小米发布 MiMo-V2.6 全模态模型，RL 训练成本仅 350 万美元](https://www.reddit.com/r/MachineLearning/comments/1wn36d4/xiaomi_releases_mimov26_frontier_intelligence_all/) ⭐️ 7.0/10

小米发布了 MiMo-V2.6，这是一款以强化学习为核心训练范式的全模态前沿模型，官方披露的 RL 训练总成本为 350 万美元，并同步上线了一个公开的“benchmaxxing”看板，实时追踪其各项基准测试成绩。MiMo-V2.6 系列共带来三款新模型，已上线小米 MiMo 开放平台，API 价格与 V2.5 保持一致。 一家消费硬件公司以如此低的 RL 训练成本推出前沿多模态模型，挑战了“只有资金雄厚的少数实验室才能在前沿竞争”的固有认知，也会对闭源 API 和其他开源权重模型形成价格压力。实时 benchmaxxing 看板是一次颇具新意的透明度实验，但同时也容易引发“针对基准过度优化而非真实能力提升”的质疑。 MiMo-V2.6 被描述为一款支持 100 万 token 上下文的全模态模型，采用 MIT 许可开放权重，并提供 Transformers、vLLM、SGLang 和 Docker 等部署路径，另有 Pro 版本可开启“UltraSpeed”模式，输出速度最高提升 20 倍。需要留意的是，350 万美元这一数字仅指强化学习阶段的开销，并不包含预训练的总算力成本，因此不能等同于模型的全部研发投入。

reddit · r/MachineLearning · /u/we_are_mammals · 9月22日 07:56

**背景**: “Benchmaxxing”指的是针对公开排行榜和基准测试进行专门优化的做法，这会让分数看起来很漂亮，却未必反映模型在日常使用中的真实能力——随着 OpenAI、Google、Anthropic 和 Meta 的基准表格层出不穷，这一担忧正日益普遍。强化学习已成为推动基础模型自我提升的主流后训练范式，而多模态（或称全模态）模型则指能在同一系统中处理文本、图像、音频等多种输入。小米以智能手机和 IoT 硬件厂商著称，因此发布前沿规模的 AI 模型标志着其向基础模型业务的重要扩张。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mimo.xiaomi.com/mimo-v2-6">MiMo - V 2 . 6 | Xiaomi</a></li>
<li><a href="https://notesgallery.in/ai-benchmark-scores-agentic-benchmaxxing/">AI Benchmark Scores Are Getting Harder to Trust. Here's Why</a></li>
<li><a href="https://kie.ai/blog/what-is-xiaomi-mimo-v2-6">Meet Xiaomi MiMo V 2 . 6 , the 1M-Token Omnimodal Model</a></li>

</ul>
</details>

**标签**: `#LLM`, `#multimodal`, `#model-release`, `#reinforcement-learning`, `#benchmarks`

---

<a id="item-12"></a>
## [Complex KDA：扩展 Kimi Delta Attention 的表达能力](https://www.reddit.com/r/MachineLearning/comments/1wn5uv9/understanding_and_enhancing_kimi_delta_attention_r/) ⭐️ 7.0/10

一篇 Reddit 帖子提出了 Complex KDA（CKDA），这是对 Kimi Delta Attention 的改进：将对角门的取值范围扩展到 [-1,1]，并把 delta 规则的学习率扩展到 [0,2]，使完整对角门可以充当反射，从而在单步内完成 2D 旋转。作者证明该形式能够表示任意正交的对角加秩一矩阵，并可跟踪 S3、S4 和 A5 群（但不包括 S5），实验显示 CKDA 能学会 S3/S4，在语言建模上可与标准 KDA 竞争，并在音频续写任务上展现出潜力。 它明确指出了 Gated DeltaNet 与 Kimi Delta Attention 之间表达能力差距的来源，并表明只需小幅调整门与学习率的取值范围就能解锁类旋转变换。这对研究线性注意力架构、需要在效率与状态跟踪能力之间权衡的研究者具有参考价值。 该理论只保证能跟踪到 S4/A5 级别的有限群，对 S5 则失败；取值范围的扩展也改变了门的语义，使其从衰减/遗忘门转向带符号的反射操作。实验结果被描述为“有前景”而非达到最先进水平，且该工作目前还是预印本/社区帖子，尚未经过同行评审。

reddit · r/MachineLearning · /u/Yossarian_1234 · 9月22日 10:34

**背景**: Kimi Delta Attention（KDA）是 Kimi Linear 架构的核心，一种线性注意力模块，它在 Gated DeltaNet（GDN）基础上把标量遗忘门换成更细粒度的向量化衰减。Gated DeltaNet 则是在 Mamba2 基础上引入 delta 规则——一种带误差修正的记忆更新方式——并结合输入相关的门控，以提升记忆保持与选择性。线性注意力方法旨在降低标准 softmax 注意力随序列长度二次增长的开销，但通常表达能力较弱，而这项工作正是在探究这一差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jianyuh.github.io/attention/2025/12/13/KDA.html">Linear Attention : Kimi Delta Attention | Jianyu Huang</a></li>
<li><a href="https://arxiv.org/pdf/2510.26692">Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://arxiv.org/abs/2412.06464">[2412.06464] Gated Delta Networks: Improving Mamba2 with Delta Rule</a></li>

</ul>
</details>

**标签**: `#machine-learning`, `#attention-mechanisms`, `#linear-attention`, `#expressivity`, `#group-theory`

---

<a id="item-13"></a>
## [Qonto 发布 QontoFAQ 检索基准与相关性指标](https://www.reddit.com/r/MachineLearning/comments/1wn9xqk/qontofaq_a_better_information_retrieval_benchmark/) ⭐️ 7.0/10

Qonto 发布了 QontoFAQ——一套新的信息检索基准以及配套的相关性指标，该指标的设计目标是让评分与文档相关性更加成比例，同时在 GitHub 上开源了基准数据集与代码。该项目在 Qonto 工程博客的 Medium 文章中详细说明，并由用户 /u/espadrine 在 r/MachineLearning 板块公布。 嵌入模型越来越依赖检索排行榜来评判，而构建搜索或 RAG 系统的团队对可能被模型针对性调优的基准已日益怀疑。一个紧扣具体实用目标的基准——找出真正能回答产品问题的文章——能为从业者选择和验证嵌入模型提供更可信的信号。 该指标的设计意图是让得分随检索文档的相关程度成比例变化，而不是把检索简化为在某个截断位置上的命中与否。数据集基于 Qonto 自身的产品 FAQ 语料构建，因此其向其他领域或语言的迁移能力尚未得到验证；这次发布属于实用性的评测贡献，而非研究层面的重大突破。

reddit · r/MachineLearning · /u/espadrine · 9月22日 13:45

**背景**: 嵌入模型将文本转换为稠密向量，使语义相近的段落映射到向量空间中相近的位置，这正是语义搜索与检索增强生成（RAG）背后的机制。检索基准通常衡量对于一组查询，正确的文档是否出现在返回结果的前 k 名之中。由于模型可以针对与基准相邻的数据进行优化——这种做法常被称为“benchmaxxing”（刷榜）——排行榜分数未必能反映真实场景下的检索质量，而这正是 QontoFAQ 试图解决的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://adipod.ai/glossary/benchmaxxed/">Benchmaxxed — ADI Pod</a></li>
<li><a href="https://medium.com/@Nexumo_/the-8-retrieval-benchmarks-lying-to-your-rag-5811ca3ee057">The 8 Retrieval Benchmarks Lying to Your RAG | by Nexumo | Medium</a></li>

</ul>
</details>

**标签**: `#information-retrieval`, `#benchmark`, `#embeddings`, `#evaluation`, `#nlp`

---

<a id="item-14"></a>
## [抖音上线理财板块，支持购买基金与券商开户](https://finance.jrj.com.cn/2026/09/21194458502389.shtml) ⭐️ 7.0/10

抖音正式开通买基金功能：用户打开“我的钱包”进入理财页面，最下方已出现基金入口，点入后可见活期理财、银行存单、稳健理财、红利基金、追求收益五个栏目，分别对应货币基金、债券基金、固收+、主动权益基金、QDII 等公募产品。该板块同时支持券商开户，而上线时间点恰在《金融产品网络营销管理办法》2026 年 9 月 30 日施行之前。 拥有数亿日活用户的抖音切入基金销售与券商开户，可能明显改变中国普通投资者的触达方式，并与蚂蚁支付宝、腾讯理财通以及传统银行、券商形成直接竞争。同时，抖音也成为检验新规如何约束大型第三方平台的重要样本——这类平台只能在持牌机构委托下开展金融产品网络营销。 这五个栏目对应不同的风险收益特征：低风险端是接近现金管理的货币基金与银行存单，高风险端则是主动权益基金和涉及海外市场敞口、受外汇额度约束的 QDII 基金。需要留意的关键约束来自监管：新办法要求除金融机构和受托第三方平台以外的组织或个人（明确包括网络大 V、理财博主）不得开展或变相开展金融产品网络营销，因此抖音生态内的推广只能由持牌主体进行。

telegram · zaihuapd · 9月22日 01:56

**背景**: 抖音是字节跳动旗下的短视频应用，也是中国规模最大的消费互联网平台之一，“我的钱包”则是其内置的支付与金融服务入口。页面中列出的产品属于公募基金：货币基金主要投资短期货币工具，债券基金以债券为主，“固收+”以债券打底、少量配置权益或衍生品以增厚收益，主动权益基金由基金经理选股，QDII 基金则让境内投资者通过国内基金公司在国家外汇管理局核定的额度内投资海外股票和债券。《金融产品网络营销管理办法》由央行等八部门于 2026 年 4 月 21 日联合发布、2026 年 9 月 30 日起施行，强化了金融产品网络营销的资质与内容要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://m.ce.cn/bwzg/202605/t20260506_2947459.shtml">严 管 金 融 产 品 网 络 营 销 守好百姓“钱袋子”_中国经济 网</a></li>
<li><a href="https://cj.sina.com.cn/articles/view/5044281310/12ca99fde02002i8r8">cj.sina.com.cn/articles/view/5044281310/12ca99fde02002i8r8</a></li>
<li><a href="https://k.sina.com.cn/article_7879922977_1d5ae152101901amwc.html">带你一文读懂 QDII 基 金 | 新浪网</a></li>
<li><a href="https://www.21jingji.com/article/20230630/herald/c3917e4a261b435cb3d60d640b3178b0.html">近八成年内 收 益为正！ 震荡市下这类 基 金 “大回血”，还能上车吗？ - 21...</a></li>

</ul>
</details>

**标签**: `#fintech`, `#Douyin`, `#wealth management`, `#China tech`, `#financial regulation`

---

<a id="item-15"></a>
## [阿里发布真武 V900 AI 芯片，宣称算力达 M890 三倍](https://finance.sina.com.cn/stock/bxjj/2026-09-22/doc-inissitf7048094.shtml) ⭐️ 7.0/10

在 2026 云栖大会上，阿里平头哥发布新一代 AI 芯片真武 V900，宣称算力达到上一代真武 M890 的 3 倍，单一集群可扩展至 50 万卡。CEO 吴泳铭表示，自研 M890 超节点已支撑 2 万亿参数大模型推理，本季度将在阿里云规模化上架，同时宣布计划训练 5 至 10T 参数的新 Qwen 模型，并力争到 2032 年阿里云全球数据中心规模超过 20GW。 这一发布让阿里成为少数同时自研芯片、云平台和前沿大模型的“全栈”玩家，直接挑战英伟达在 AI 加速器市场的主导地位。在美国对华高端芯片出口管制持续的背景下，一款可用的国产加速器路线图不仅关系到阿里自身 Qwen 模型的训练计划，也关系到整个中国 AI 产业能否在不依赖海外硬件的情况下继续扩大算力规模。 据媒体报道，真武 V900 单卡显存为 216GB，而 50 万卡的集群规模属于可扩展性目标，并非已经落地的部署。目前所有性能数字均来自阿里官方，尚无第三方基准测试或能效数据披露；5 至 10T 参数 Qwen 模型与 20GW 数据中心容量也都是面向 2032 年的多年期目标，而非近期可交付的成果。

telegram · zaihuapd · 9月22日 03:30

**背景**: 平头哥是阿里的自研芯片设计部门，真武是其 AI 加速器产品线，M890 为上一代产品；“超节点”指将大量加速器高速互联、以支撑超大模型运行的紧耦合集群。参数规模是衡量模型体量与能力的粗略指标——2 万亿参数模型在推理时需要极大的显存和互联带宽，这也是芯片厂商强调单集群可连接多少张卡的原因。Qwen（通义千问）是阿里的大模型系列，而用吉瓦（GW）衡量的数据中心容量，则是业界常用的指标，用来表示运营商计划建设多少耗电巨大的 AI 基础设施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://easternherald.com/2026/09/22/alibaba-zhenwu-v900-china-ai-chip/">Alibaba Unveils Zhenwu V 900 : China's Most Powerful AI Chip</a></li>
<li><a href="https://cryptobriefing.com/alibaba-ai-model-zhenwu-v900-chip/">Alibaba plans AI model with 5-10 trillion parameters, unveils Zhenwu ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#Alibaba`, `#semiconductors`, `#LLM infrastructure`, `#data centers`

---

<a id="item-16"></a>
## [DeepSeek 发布 DSec 沙箱平台技术报告：每日 300 万沙箱支撑智能体训练](https://arxiv.org/abs/2609.22978) ⭐️ 7.0/10

DeepSeek-AI 与清华大学联合发布技术报告《DeepSeek Elastic Compute（DSec）》，公开了每天服务约 300 万个沙箱实例、用于支撑大规模智能体训练与评测的生产级沙箱基础设施。DSec 通过统一 SDK 提供 FnCall、容器、Firecracker microVM 和完整 VM 四种后端，并将有状态的 rollout 执行与可抢占的 GPU 训练解耦。 智能体训练与强化学习越来越依赖在超大规模下安全执行不可信、有状态的代码，而 DSec 展示了生产级方案在实践中的样子。其披露的数据——每天约 300 万个沙箱、峰值并发超 38 万、创建速度超每秒 5000 个——为 AI 基础设施与系统工程师自建智能体沙箱层提供了具体参照。 DSec 单个生产单元约 160 个节点，单节点可高密度承载 3200 个容器或 800 个 microVM；基于 3FS 分布式文件系统按需加载 EROFS 镜像，相比传统 Docker 全量拉取，任务完成时间快 1.7 倍、磁盘写入减少 57%，内存共享与回收机制使峰值内存占用下降约 40%。平台覆盖 OJ 判题、软件工程、安全渗透、电脑操作等各类负载。

telegram · zaihuapd · 9月22日 04:45

**背景**: AI 智能体通常需要通过真实执行代码、浏览网页或操作电脑来训练和评测，这就要求把每次运行隔离开来，避免其破坏宿主机或其他运行实例，这类技术被称为沙箱。Firecracker 是 AWS 开源的虚拟化技术，可创建轻量的 microVM，兼具硬件级隔离与快速启动；EROFS 则是华为最初开发的只读 Linux 文件系统，专为紧凑高性能的镜像分发而优化。面向智能体的强化学习流程需要同时运行海量这类隔离环境，因此这一规模的基础设施已成为工程竞争的热点领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/firecracker-microvm/firecracker">GitHub - firecracker - microvm / firecracker : Secure and fast microVMs...</a></li>
<li><a href="https://en.wikipedia.org/wiki/EROFS">EROFS - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI Infrastructure`, `#Agent Training`, `#Sandboxing/MicroVMs`, `#Reinforcement Learning`, `#Distributed Systems`

---

<a id="item-17"></a>
## [Mimo CLI 被曝存在潜在数据收集功能](https://linux.do/t/topic/2935748) ⭐️ 7.0/10

有用户在 LINUX DO 发布逆向分析称，Mimo CLI 默认可能上传当前项目的 Git 仓库地址、提交哈希和分支信息，可通过设置 MIMOCODE_ENABLE_ANALYSIS=false 关闭。同一分析还发现，Mimo CLI 的闭源扩展 trajectory-bundle 和 codebase-bundle 中包含一个未被调用的 collectCodebase() 函数，具备枚举 Git 仓库文件、读取源代码并压缩打包的能力。 对开发者而言，AI 编程 CLI 经常直接在私有代码仓库中运行，因此默认上传仓库元数据以及闭源扩展中隐藏的代码打包能力，会引发严重的隐私和供应链信任问题。如果这些发现得到证实，可能会阻碍团队采用 Mimo Code，并迫使厂商披露遥测行为并提供可审计的开源组件。 披露者强调，相关结论尚未得到官方确认，目前也没有证据表明 collectCodebase() 被实际调用，或打包后的源代码被上传至外部。相关功能据称仅存在于闭源的 trajectory-bundle 和 codebase-bundle 扩展中，并不包含在 Mimo CLI 的官方开源仓库内，且遥测可通过环境变量选择关闭。

telegram · zaihuapd · 9月22日 08:18

**背景**: Mimo CLI 也被称为 MiMo Code，是小米推出的 AI 编程助手，以终端 CLI 工具形式分发，类别上类似 Claude Code 和 Gemini CLI。AI 编程代理通常会收集遥测数据以改进产品质量，但仓库地址、提交哈希、分支名称和源代码远比普通使用指标敏感。由于 Mimo CLI 的部分组件是闭源扩展，开发者通过逆向工程进行检查，往往是了解该工具能访问哪些数据的唯一方式。MIMOCODE_ENABLE_ANALYSIS 环境变量表明该工具存在可由用户开关的分析或遥测功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mimo.xiaomi.com/mimocode/install">Install MiMo Code and launch it in your terminal.</a></li>
<li><a href="https://mimo.mi.com/docs/en-US/tokenplan/integration/mimo-code">Xiaomi MiMo Home</a></li>
<li><a href="https://mimocode.org/">Mimo Code Guide — Install, Compare, Configure & AI Coding Agent...</a></li>

</ul>
</details>

**标签**: `#privacy`, `#security`, `#reverse-engineering`, `#developer-tools`, `#data-collection`

---

<a id="item-18"></a>
## [中国监管机构调查 DeepSeek 与月之暗面数据泄露指控](https://www.theinformation.com/articles/china-probes-deepseek-moonshot-potential-data-leaks-anthropic) ⭐️ 7.0/10

据知情人士透露，中国互联网监管机构正在调查 DeepSeek 和月之暗面（Moonshot AI），起因是 Anthropic 于 9 月 10 日发布了一份 154 页的报告，指控 7 家中国公司大规模违规将敏感用户数据转发给其 Claude 模型。报告特别举例称，DeepSeek 曾把一名从事警方监控系统开发的工程师的请求转发给 Claude。 这一事件处于 AI 治理、数据隐私与中美科技博弈的交汇点，也表明中国监管机构愿意就跨境数据处理问题审查本国的头部 AI 实验室。这可能促使国内厂商收紧数据流转与第三方模型调用策略，同时也为本已激烈的中美大模型竞争增添了合规层面的新变量。 事件的导火索是 Anthropic 那份 154 页报告，其中声称有 7 家中国公司不当使用 Claude，DeepSeek 的案例则涉及与警方监控系统开发相关的请求。该调查消息由 The Information 援引知情人士报道，DeepSeek 与月之暗面均未公开证实被调查一事，因此调查范围与可能处罚仍不明确。

telegram · zaihuapd · 9月22日 14:37

**背景**: DeepSeek 是一家位于杭州的 AI 公司，由对冲基金幻方量化（High-Flyer）出资支持，以发布开放权重的大语言模型著称；月之暗面（Moonshot AI）的名字源自 Pink Floyd 的专辑，是中国开发 Kimi 系列模型的实验室。Claude 则是 Anthropic 推出的商用大语言模型，通常通过 API 访问，其服务条款对使用用途和数据处理有所限制。在实际开发中，开发者有时会把一个模型的请求转发给另一个模型，这正是本次被指控的“数据转发”模式所涉及的情形。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_(Company)">DeepSeek (Company)</a></li>
<li><a href="https://www.moonshot.ai/">Welcome to Moonshot AI . Our mission is to seek the optimal...</a></li>

</ul>
</details>

**标签**: `#AI Regulation`, `#Data Privacy`, `#DeepSeek`, `#Anthropic`, `#China Tech`

---

<a id="item-19"></a>
## [DeepSeek 本周将向联合国安理会通报 AI 风险](https://t.me/zaihuapd/43989) ⭐️ 7.0/10

两名知情人士称，中国 AI 初创公司 DeepSeek 将在本周向联合国安理会通报人工智能带来的风险；由 15 个成员组成的安理会定于周三开会讨论 AI 与国际安全。OpenAI 首席执行官 Sam Altman 计划出席简报，Anthropic 高层代表预计也将参加，DeepSeek 和月之暗面（Moonshot）等中国 AI 公司均受邀发言，但 DeepSeek 创始人梁文锋不打算出席，相关安排仍可能临时变动。 这标志着中美前沿 AI 实验室罕见地在正式的多边安全场合同台，说明前沿 AI 风险正被视为地缘政治与国际安全问题，而不再只是纯技术议题。其进展可能影响各国政府对 AI 治理、出口管制及未来国际规则的取向，从而直接波及全球的 AI 企业、开发者与用户。 此次通报对应安理会关于 AI 与国际安全的会议，参与者同时涵盖美国实验室（OpenAI、Anthropic）与中国实验室（DeepSeek、月之暗面），在中美科技关系紧张的背景下这一组合并不常见。值得注意的是，DeepSeek 创始人梁文锋预计不会亲自出席，消息人士也提醒日程仍可能临时调整。

telegram · zaihuapd · 9月22日 17:39

**背景**: DeepSeek 是一家总部位于杭州的中国 AI 公司，由对冲基金幻方量化（High-Flyer）拥有和出资，主要开发开放权重的大语言模型，并因以极低成本发布有竞争力的模型而受到全球关注。Anthropic 是专注于 AI 安全的美国实验室，开发 Claude 系列模型；OpenAI 则是 ChatGPT 与 GPT 系列模型的开发者，两家公司都曾公开强调先进 AI 的危险性。联合国安理会由 15 个成员组成，其中五个常任理事国拥有否决权，此前已就 AI 作为国际和平与安全的新兴威胁进行过讨论，但由前沿 AI 企业亲自通报仍是一种较新且偏象征性的接触形式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_(Company)">DeepSeek (Company)</a></li>
<li><a href="https://huggingface.co/Anthropic">Org profile for Anthropic on Hugging Face, the AI community building...</a></li>
<li><a href="https://tracxn.com/d/companies/moonshot-ai/__wZzU6o3CAntBLbB5MXh7XINvgyVvzhQb4DNTaMgBTp4">Moonshot AI - 2026 Company Profile, Team, Funding... - Tracxn</a></li>

</ul>
</details>

**标签**: `#AI governance`, `#AI safety`, `#DeepSeek`, `#UN Security Council`, `#geopolitics`

---

<a id="item-20"></a>
## [报告称 GPT-6 "Astra" 破解自 2005 年悬而未决的 Enigma 电文，引发争议](https://www.cryptocellar.org/bgac/the-mvueh-break.html) ⭐️ 6.0/10

据称，一个名为 "GPT-6 Astra" 的 OpenAI 模型破解了 1941 年德国陆军的一封 Enigma 电报，而这封电报自 2005 年起一直收录在 CryptoCellar 档案库中、从未被解出；据报道该模型还自行编写了 Python 和 C++ 的 Enigma 模拟器。此事在 Hacker News 上获得 486 分、341 条评论，多位评论者指出其他工具（包括被称作 "gemini 3.8 flash" 的模型）也在几十分钟内解出了同一封电报。 如果这一说法得到验证，它将成为一个引人注目的案例：大语言模型自主构建领域专用工具，并攻克了人类研究者搁置约二十年的历史密码分析难题，这直接推动了关于"AI 能否作为独立研究代理"的讨论。与此同时，它也凸显出当突破依赖模型自生成的模拟器以及此前人类的密码分析成果时，功劳归属有多难界定。 解出的明文为 "BTTE UM ANGABE DES MARSQWEGES X BEFINDE MIQ IN X ROSENOW ROSENOW X SOFORT FUNKANTWORT X WASCHBBSCH"，考虑到其中的拼写错误，大意是"请说明行军路线。我在 Rosenow，Rosenow。请立即用无线电回复。Waschbusch。"需要注意几点："GPT-6 Astra" 和 "gemini 3.8 flash" 这样的模型名称显得不寻常；据称此次破解依赖对一封相邻电报（SIPVX 第 173 号）的比对，而那封电报早在 2017 年就由人类研究者解出；此外，Enigma 的密钥若短于电报本身，理论上也可能产出看似合理却错误的明文。

hackernews · sohkamyung · 9月22日 13:52 · [社区讨论](https://news.ycombinator.com/item?id=49801324)

**背景**: Enigma 是二战期间德国用于军事通信的转子密码机，布莱切利园破解它的过程是计算史上的奠基性事件。CryptoCellar 是一个在线 Enigma 截获电文档案库，其中一些电文自 2005 年前后公布以来始终未被破解。破解这类电文通常需要"crib"（猜测的明文片段）、对每日密钥设置与报务员习惯的了解，以及大量试错搜索——而这正是程序（无论由人类还是模型编写）能够自动化的重复性工作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://forklog.com/news/ai/gpt-6-astra-rasshifrovala-radiogrammu-enigma-1941-goda">GPT-6 Astra расшифровала радиограмму Enigma 1941... - ForkLog</a></li>
<li><a href="https://habr.com/ru/news/1084042/">GPT-6 Astra помогла прочесть зашифрованную Enigma ... / Хабр</a></li>

</ul>
</details>

**社区讨论**: 评论者大多对功劳归属持怀疑态度：tantalor 认为"完全靠自己完成"与模型自行编写 Python 和 C++ 的 Enigma 模拟器软件自相矛盾，并追问这些代码有多少是新东西、破解过程又有多少只是外包给了它。podgorniy 称 "gemini 3.8 flash" 在约 45 分钟内一次性解出，而 Opus 当时仍在运行，说明这一成果并非 Astra 独有。还有人给出了德文明文、质疑错误的密钥是否也可能产出看似有效的明文，并希望类似方法最终能破解 Kryptos 的第四段。

**标签**: `#ai`, `#cryptography`, `#enigma`, `#llm`, `#hackernews`

---

<a id="item-21"></a>
## [GrapheneOS 暗示最早 2027 年将有预装该系统的设备出货](https://grapheneos.social/@GrapheneOS/117299954135808210) ⭐️ 6.0/10

GrapheneOS 项目在其官方社交账号上表示，2027 年很有可能出现预装 GrapheneOS 的设备在售，社区成员推测硬件合作方很可能是摩托罗拉。评论者澄清，这里指的是计划中机型的出厂预装，而非改变现有 Pixel 设备上用户自行安装的方式。据称这些预装设备将由直接从厂商获得机器的第三方公司提供，而不是通过摩托罗拉自家的销售渠道。 如果成真，这将是强化版、去谷歌化的 Android 发行版第一次真正走向普通消费者，而无需用户自行解锁引导程序并手动刷写固件。这一转变可能促使其他手机厂商推出更多尊重隐私的版本，也让企业用户和普通用户获得一个替代原生 Android 的正当选择。 该时间表仍然遥远且带有推测性，GrapheneOS 自己也将其表述为“很可能”而非已确认的结果。一个关键悬而未决的问题是应用兼容性：许多银行类应用和企业 BYOD 应用依赖谷歌的 Play Integrity API 以及经谷歌认证的设备，因此即便应用能装上，未认证系统也可能无法通过完整性验证。社区成员还讨论了价格，指出摩托罗拉 Signature 系列根据不同地区售价约 1230 至 1460 美元，与 Pixel 的价格区间接近。

hackernews · Cider9986 · 9月22日 17:12 · [社区讨论](https://news.ycombinator.com/item?id=49804683)

**背景**: GrapheneOS 是 Android（AOSP）的一个开源分支，以强化安全与隐私著称，目前最广为人知的是运行在谷歌 Pixel 手机上，用户通过网页端刷机工具自行安装。它并非删减 Android 功能，而是强化沙箱隔离、增加权限控制，并减少系统向应用和谷歌服务暴露的数据。若厂商要预装该做系统，就必须愿意销售一款没有谷歌移动服务（GMS）认证的设备，而这正是移动银行等依赖完整性验证的应用出现兼容问题的根源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://privsec.dev/posts/android/banking-applications-compatibility-with-grapheneos/">Banking Applications Compatibility with GrapheneOS</a></li>
<li><a href="https://sy.st/blog/my-1-year-experience-of-using-grapheneos/">My 1 year experience of using GrapheneOS - Syst(em)</a></li>
<li><a href="https://developer.android.com/google/play/integrity/setup">Setup | Play Integrity | Android Developers</a></li>

</ul>
</details>

**社区讨论**: 这 91 条评论的讨论以澄清为主而非否定：用户强调这只是针对特定新机型的预装，计划中的硬件仍应支持自行安装，而且销售方很可能是第三方而非摩托罗拉官方商店。讨论的主要担忧集中在实用性上——企业 BYOD 和银行类应用能否通过完整性检查——同时也比较了与 Pixel 的价格，并有人半开玩笑地呼吁推出 100 美元的 GrapheneOS 手机。

**标签**: `#GrapheneOS`, `#Mobile Security`, `#Privacy`, `#Android`, `#Motorola`

---

<a id="item-22"></a>
## [LinearSolveBench：评估 AI 编写 C 语言稀疏线性求解器的新基准](https://www.reddit.com/r/MachineLearning/comments/1wnctam/linearsolvebench_new_benchmark_for_linear_solvers/) ⭐️ 6.0/10

r/MachineLearning 上（由 /u/hgarud 提交，代码位于 github.com/hgarud/LinearSolveBench）发布了一个名为 LinearSolveBench 的新基准，用于衡量模型或 harness 编写快速、准确且通用的 C 语言大规模稀疏线性系统数值求解器的能力。其目标是推动求解线性方程组数值方法方面的算法进步。 大多数代码生成基准只考察日常软件任务中功能正确的代码，而数值求解器要按渐进复杂度性能、数值稳定性和跨问题类的通用性来评判，这对代码生成模型来说难度大得多。如果该基准获得关注，它可能成为衡量“AI 用于科学计算”以及智能体能否产出高性能数值内核（而非仅仅能编译的代码）的一个有用标尺。 任务被刻意限定为用 C 实现大规模稀疏系统的求解器，并从速度、准确性和通用性三个维度评估，这种组合会抑制针对单一矩阵族硬编码或过度调参的做法。公开说明相当简短：仓库是新建立的，帖子中没有给出排行榜、基线结果、测试矩阵集细节或版本信息，因此确切的评分方法与问题分布仍需查看仓库加以确认。

reddit · r/MachineLearning · /u/hgarud · 9月22日 15:34

**背景**: 求解稀疏线性系统就是要找到满足 Ax = b 的向量 x，其中矩阵 A 规模很大但绝大多数元素为零，有限元仿真、计算流体力学、结构分析和图问题中都会出现这种情况。方法大致分两类：一类是稀疏 LU 或 Cholesky 分解等直接法，另一类是共轭梯度、GMRES 等迭代法，后者通常需要配合预条件子才能快速收敛；如何选择并实现合适的组合是数值分析的核心技能。由于稀疏求解器受内存带宽限制、需要精心设计数据结构（如压缩稀疏行格式），而且对数值条件数十分敏感，要写出同时兼顾速度、精度和通用性的求解器远比写普通应用代码困难——这正是该基准想要衡量的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://amcs.kaust.edu.sa/topics/sparse-linear-systems">sparse linear systems | Applied Mathematics and Computational...</a></li>
<li><a href="https://gitlab.mn.tu-dresden.de/teaching/sparse_linear_systems">sparse _ linear _ systems · GitLab</a></li>
<li><a href="https://link.springer.com/article/10.1007/s11075-026-02463-z">On the adaptive-momentum variant for maximal weighted residual...</a></li>

</ul>
</details>

**标签**: `#benchmark`, `#linear solvers`, `#numerical methods`, `#scientific computing`, `#code generation`

---

<a id="item-23"></a>
## [Templar 用「阶段跳过」模拟流水线并行预训练的容错能力](https://www.reddit.com/r/MachineLearning/comments/1wnd5ys/simulating_fault_tolerance_with_stage_skipping_in/) ⭐️ 6.0/10

Templar 发布了一项模拟研究，展示其分布式预训练平台 Crucible 在某个流水线阶段掉线时，可以让健康的 worker 继续训练：做法是让激活值和梯度在若干步内直接绕过失效阶段。实验采用 1.78 亿参数模型、8 个数据并行副本、每个副本 4 个阶段，并设定每个副本在每个全局步有 1% 的失效概率；尽管每次模拟故障都会让某个阶段缺席 6 个全局步，验证损失仍与各配置自身的「无故障」基线非常接近。 如果这些学习动态层面的结果在真实部署中依然成立，大规模预训练就不必因为硬件故障而停顿或重启，从而可以使用更便宜的 spot 实例以及更广泛、更异构的算力资源。这将直接缓解当前大规模分布式训练中最突出的成本与调度瓶颈。 该研究明确是对阶段失效所造成的学习效果的模拟，而非对物理 worker 替换、恢复时间或生产环境成本节省的实测，因此实际的系统开销尚未被量化。作者还报告称，在使用流水线压缩时，跨层共享的固定投影（fixed projections）能进一步提升鲁棒性，并推测共享投影器会让跨阶段边界的表示更对齐，从而让绕过操作破坏性更小；但他们强调这一「对齐」解释目前还只是假设，并非已被证实的机制。

reddit · r/MachineLearning · /u/covenant_ai · 9月22日 15:47

**背景**: 流水线并行（pipeline parallelism）把模型切分成按顺序排列的若干阶段并放在不同 worker 上，每个 worker 只保存并计算网络的一部分；数据并行（data parallelism）则是在多份独立副本中复制整个模型。由于一个阶段必须等前一阶段产出激活值才能继续，单个 worker 失效就可能让整条流水线停滞，这也是大规模训练传统上依赖「检查点 + 重启」恢复、并因此浪费大量时间的原因。SparseLoCo 通过交换高度压缩的伪梯度（例如 top-k 稀疏化）来降低副本之间的通信量，流水线压缩则减少每个副本内部跨阶段边界的通信；阶段跳过正是在这一基础上，让缺失阶段被绕过时其余阶段仍能继续处理 token。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/one-covenant/SparseLoCo">GitHub - one-covenant/ SparseLoCo : CCLoco: Scaling Up Top-K Error...</a></li>
<li><a href="https://deepwiki.com/one-covenant/SparseLoCo/4.2-distributed-training-setup">Distributed Training Setup | one-covenant/ SparseLoCo | DeepWiki</a></li>
<li><a href="https://arxiv.org/pdf/2110.02781">FTPipeHD: A Fault - Tolerant Pipeline - Parallel</a></li>

</ul>
</details>

**标签**: `#distributed-training`, `#fault-tolerance`, `#pipeline-parallelism`, `#machine-learning-systems`, `#pre-training`

---

<a id="item-24"></a>
## [美国提议与中方建立 AI 事件通报渠道](https://x.com/rohanpaul_ai/status/2102254209597157548) ⭐️ 6.0/10

美方向中方提议建立人工智能事件通报渠道，用于就达到国家安全门槛的 AI 相关事件相互通报，该提议出自 9 月 20 日在纽约举行的美国财长贝塞特与中国副总理何立峰的会谈。双方还计划围绕共同风险建立定期的美中 AI 对话，但中方官方声明仅确认双方讨论了 AI 相关议题，并未明确表示接受这一具体机制，目前该提议尚未成为双边协议或条约。 如果这一设想落地，它将成为全球两大 AI 强国之间首个专门针对 AI 的双边危机沟通渠道，有望在先进 AI 系统引发涉安全事件时降低误判风险。这也表明 AI 安全与风险管理正从单纯的国内监管议题上升到大国外交层面，将影响两国的 AI 实验室、云服务商与政策制定者。 该提议仅针对达到特定国家安全门槛的事件，而非所有 AI 事件，并且目前仍停留在提议阶段，尚未就正式机制、时间表或执行架构达成一致。相关讨论发生在 9 月 24 日特朗普与习近平白宫会晤之前，说明该渠道更多被定位为建立互信的举措，而非具有约束力的条约。

telegram · zaihuapd · 9月22日 06:48

**背景**: AI 事件通报框架是一种治理机制，用于捕捉和管理 AI 系统出现异常行为、造成损害或违反政策的情况，通常会界定需要上报的内容、上报对象以及时限。双边版本与国内制度不同，因为它要求两个相互竞争的国家政府就共同定义、门槛标准和保密规则达成一致。美中此前曾建立军事热线与对话渠道以避免局势升级，这一提议实质上是把同样的危机沟通逻辑应用到 AI 风险领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/09/20/business/us-china-ai-warning-system-national-security.html">U.S. and China Discuss System to Warn of A . I . National Security Issues</a></li>
<li><a href="https://nationalcioreview.com/articles-insights/extra-bytes/the-u-s-and-china-want-a-crisis-hotline-for-the-ai-race/">The U.S. and China Want a Crisis Hotline... - The National CIO Review</a></li>

</ul>
</details>

**标签**: `#AI Governance`, `#AI Policy`, `#US-China Relations`, `#AI Safety`, `#Geopolitics`

---

<a id="item-25"></a>
## [iOS 27.2 Beta 2 疑似新增中国大陆特供传感器权限](https://t.me/zaihuapd/43986) ⭐️ 6.0/10

据报道，iOS 27.2 beta 2 疑似新增了一个中国大陆地区特供的权限选项「Restrict Motion Data」（限制動作資料），位于「设置——隐私和安全——运动与健身」中，开启后会对指定的第三方 App 屏蔽加速度计、陀螺仪等传感器数据。群友测试发现，只有使用中国内地 Apple ID 登录 App Store 时才会出现该设置，未来不排除扩展到其他地区。 如果消息属实，这将是平台层面首次允许用户直接切断第三方 App 对原始运动传感器数据的访问，比起现有的「运动与健身」权限是更彻底的一步。由于该设置与 Apple ID 地区绑定，这也暗示中国市场可能存在特定的隐私或监管要求，正在影响 iOS 功能的落地方式。 据描述，该开关位于「设置——隐私和安全——运动与健身」下，简体中文系统显示为「Restrict Motion Data」，繁体中文显示为「限制動作資料」。目前这只是一个来自 Telegram 投稿的未经证实观察，没有 Apple 官方文档、开发者说明或 API 细节来解释该限制如何生效，也没有说明除加速度计和陀螺仪外还涉及哪些传感器。

telegram · zaihuapd · 9月22日 12:37

**背景**: iOS 应用通常通过 Apple 的 Core Motion 框架获取设备运动数据，其数据来源是加速度计（测量线性加速度）和陀螺仪（测量旋转速率）——这两种 MEMS 传感器如今已是智能手机的标配。以往这类访问由「运动与健身」权限管控，开发者依赖它实现计步、健身追踪，以及像 MapMyFitness 那样用运动数据校验和补全 GPS 距离。因此，若在权限或系统层面屏蔽原始运动数据，影响范围将远超健身功能，可能波及手势控制、游戏以及防抖稳定等场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gyroscopic_sensor">Gyroscopic sensor</a></li>
<li><a href="https://developer.apple.com/forums/thread/60341">Misleading info on Motion data per… | Apple Developer Forums</a></li>
<li><a href="https://support.mapmyfitness.com/hc/en-us/articles/1500009118022-iOS-Motion-Sensor">iOS Motion Sensor – MapMyFitness</a></li>

</ul>
</details>

**标签**: `#iOS`, `#privacy`, `#sensors`, `#Apple`, `#China`

---