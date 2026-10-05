---
layout: default
title: "Horizon Summary: 2026-10-06 (ZH)"
date: 2026-10-06
lang: zh
---

> 从 30 条内容中筛选出 16 条重要资讯。

---

1. [vLLM v0.31.0 发布：717 次提交带来推理加速与快速重启守护进程](#item-1) ⭐️ 8.0/10
2. [Reflection AI 发布 Beam：501B 参数开源权重 MoE 模型](#item-2) ⭐️ 8.0/10
3. [Anthropic 将用户 Claude 私密日记上报警方，女子被控重罪](#item-3) ⭐️ 8.0/10
4. [苹果的隐私模式对上黑客友好型 Agentic AI 未来](#item-4) ⭐️ 8.0/10
5. [高通与华为达成广泛专利协议，获 LogicFolding 芯片技术许可](#item-5) ⭐️ 8.0/10
6. [Yandex Music 的 Sona：一个 Transformer 取代 15+ 推荐组件](#item-6) ⭐️ 8.0/10
7. [2026 年诺贝尔生理学或医学奖授予光遗传学发现者](#item-7) ⭐️ 8.0/10
8. [Opus 5.5 智能体宣称筛出两种室温磁性半导体候选材料](#item-8) ⭐️ 7.0/10
9. [Cloudflare 推出面向 AI 智能体的 Web Search API](#item-9) ⭐️ 7.0/10
10. [Chunkr：号称比 Python 工具快约 20 倍的 Rust 文本分块库](#item-10) ⭐️ 7.0/10
11. [用 10 亿局面蒸馏 Stockfish 价值函数，并公开 39 亿局面数据集](#item-11) ⭐️ 7.0/10
12. [Quad9 拒绝法国 DNS 封锁令，面临每日最高 58 万欧元罚款](#item-12) ⭐️ 7.0/10
13. [OpenAI 将在欧盟为 AI 生成文本添加隐形水印](#item-13) ⭐️ 7.0/10
14. [SemiAnalysis：Anthropic 订阅价值是 OpenAI 的 5 倍以上](#item-14) ⭐️ 6.0/10
15. [开发者训练 3.1 万参数 Transformer 预测血糖，并在真实 CGM 数据上做零样本测试](#item-15) ⭐️ 6.0/10
16. [OpenAI 将在 ChatGPT 生成图片时展示视觉广告](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [vLLM v0.31.0 发布：717 次提交带来推理加速与快速重启守护进程](https://github.com/vllm-project/vllm/releases/tag/v0.31.0) ⭐️ 8.0/10

vLLM 发布了 v0.31.0，本次版本包含来自 307 位贡献者（其中 96 位是新贡献者）的 717 次提交，重点是为 DeepSeek-V4.1-Flash 推出一系列融合注意力与 MoE 内核、MXFP8 量化融合路径，以及新的 `vllm preload` CLI 守护进程，可在引擎重启期间把量化后的权重常驻于 GPU 显存。此外还加入了 Model Runner V2 的投机解码、MoonEP 等大规模专家并行后端、新的调度控制项、HiSparse 加固，以及多项安全与破坏性变更。 这些改动是面向生产级 LLM 服务的实质性吞吐与延迟优化，而非小修小补，会直接影响所有使用 vLLM 部署大模型的团队。尤其是融合内核与快速重启的权重缓存守护进程，分别针对服务中的两大运维痛点：单 token 推理成本，以及重启或重新量化后漫长的冷启动时间。 重点包括：在 SM100 上默认启用带 V4.1 NVFP4 压缩 KV 缓存的 FlashMLA mega attention、为 indexer 使用 DeepGEMM 稀疏 MQA logits、把张量并行 all-reduce 与 MoE finalize 及 mHC 输入准备融合、将 MXFP8 `wo_b` GEMM 与序列并行 reduce-scatter 融合，以及为视觉塔引入 CUDA graphs。需要注意的破坏性变更包括：逐请求的多模态 kwargs 现在必须设置 `--trust-request-mm-kwargs`；`tokenizer_mode="slow"` 被移除；`--enable-mamba-fine-grained-prefix-cache` 更名为 `--enable-mamba-shared-prefix-checkpoint`；通过 `quantization="fp8"` 进行的在线量化被 `fp8_per_tensor` 简写取代；`--enforce-eager` 现在也会禁用 JIT 内核预热。

github · khluu · 10月5日 06:44

**背景**: vLLM 是目前最广泛使用的开源大语言模型服务引擎之一，以 PagedAttention 风格的 KV 缓存管理著称，能让大量请求高效共享 GPU 显存。这类现代服务栈依赖多种技术：内核融合（把多个小型 GPU 操作合并成一个以减少显存访问）、量化（用 FP8/MXFP8 等低精度格式存储权重与激活以节省显存和带宽）、混合专家（MoE，每个 token 只激活部分专家），以及投机解码（由小草稿模型提出候选 token，再由大模型校验）。FlashMLA 是 DeepSeek 的优化注意力内核库，本次发布还涉及 Engram——vLLM 中基于 n-gram 查找的条件记忆特性。快速重启之所以重要，是因为重启后恢复量化模型通常需要重跑整个量化和加载流程，可能耗时数分钟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/FlashMLA">GitHub - deepseek-ai/ FlashMLA : FlashMLA : Efficient Multi-head...</a></li>
<li><a href="https://docs.vllm.ai/en/latest/api/vllm/models/deepseek_v41/nvidia/flash_mla_mega_attn/">flash _ mla _ mega _attn - vLLM</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/engram/">Engram : conditional memory via n-gram lookups - vLLM</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#model serving`, `#kernel fusion`, `#quantization`

---

<a id="item-2"></a>
## [Reflection AI 发布 Beam：501B 参数开源权重 MoE 模型](https://reflection.ai/blog/introducing-beam) ⭐️ 8.0/10

Reflection AI 发布了 Beam，这是一个开放权重的稀疏混合专家（MoE）模型，总参数 5010 亿、激活参数 230 亿，面向编程、推理和智能体（agentic）任务，预训练使用了 23.8 万亿条经过筛选的高质量 token。官方表示 Beam 的表现与同规模开源基座模型相当或更优，并称其基准测试结果足以与前沿模型竞争。 这为开源权重阵营再添一个接近前沿水平、可自行部署的模型，也表明相对年轻的西方实验室 Reflection AI 已具备 5000 亿参数级别的训练能力。对于希望把强力的编程与智能体模型跑在自己基础设施上、而不愿依赖少数闭源 API 供应商的开发者和企业而言，更多开放权重选项意味着在成本、隐私和供应商风险上拥有更大的议价空间。 由于采用稀疏 MoE 设计，虽然总参数为 5010 亿，但每个 token 只激活 230 亿参数，因此实际推理算力需求远低于原始参数量所暗示的水平。社区中流传的对比表格把 Beam 与 DeepSeek V4.1 Flash（总参数 5520 亿，预填充激活 80 亿、解码激活 160 亿，另有 1960 亿 n-gram/PLE 参数，预训练 45 万亿 token）并列，指出 Beam 所用训练 token 更少；也有评论者质疑这些基准提升在实际使用中是否成立。

hackernews · Philpax · 10月5日 19:16 · [社区讨论](https://news.ycombinator.com/item?id=49969183)

**背景**: 混合专家（MoE）模型把前馈层拆分成许多专门的“专家”子网络，每个 token 只被路由到其中少数几个，从而使模型总容量与单 token 所需算力解耦——这正是 5010 亿参数模型能按 230 亿参数的成本运行的原因。“开放权重”指训练好的参数可以下载并自行部署，但与完全开源项目不同，训练数据和代码通常并不公开。此类前沿规模的开放权重发布通常会在编程、数学、推理和长上下文基准上与竞品对比，几个百分点的差距往往会被大量宣传。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://xonoai.com/mixture-of-experts-moe-architecture-sparse-inference-guide/">Mixture - of - Experts ( MoE ) Architecture : How Sparsely ... | XonoAI</a></li>
<li><a href="https://philarchive.org/archive/JOSASO-5">A Survey of Mixture of Experts Models: Architectures and...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上相关讨论约有 270 分、72 条评论，整体对又一个开放权重发布表示欢迎。有评论者特别指出一张演示图声称 Beam 在一道几天前才出现的“陆地还是海洋”泛化测试题上取得了 95.5% 的覆盖率，介于 Opus 5（92.5%）和得分更高的模型之间。也有人持怀疑态度，认为 Beam 参数更大却在表现上不如更小的中文免费模型；还有用户贴出与 DeepSeek V4.1 Flash 的详细参数与 token 对比表以提供参照，多位评论者表示希望出现更多欧美及中国以外的模型供应商，以降低对单一国家模型的依赖。

**标签**: `#open-weight-models`, `#llm`, `#mixture-of-experts`, `#ai-research`, `#model-release`

---

<a id="item-3"></a>
## [Anthropic 将用户 Claude 私密日记上报警方，女子被控重罪](https://www.techspot.com/news/114091-florida-woman-used-claude-diary-anthropic-reported-shoot.html) ⭐️ 8.0/10

佛罗里达州一名女子在其 Claude 聊天机器人中写下的日记内容被 Anthropic 标记并上报执法部门后，被以二级重罪起诉。这些内容从未发送给任何第三方，如今却成为刑事指控的依据，也引发了关于 AI 服务商实际上充当监控渠道的激烈争论。 此案为 AI 公司在多大程度上应当扫描用户对话树立了一个令人不安的先例，而当下各大实验室正面临两面夹击：OpenAI 曾因未上报一名枪手而受批评，Anthropic 如今又因上报一名从未联系任何人的用户而受指责。这影响到每一个把聊天机器人当作私密空间的人，也促使注重隐私的用户转向本地部署或去审查的开源模型。 评论者援引佛罗里达州法规 836.10 条，该条规定发送、发布或传输威胁杀害或伤害他人的书面或电子记录构成二级重罪，但要求该通信是以他人可能看到的方式进行——而本案恐怕并非如此。核心法律争议在于：仅因服务商自行审查私密草稿而获得的威胁内容，是否满足该法条中“传输”这一要件。

hackernews · emptybits · 10月5日 05:37 · [社区讨论](https://news.ycombinator.com/item?id=49961057)

**背景**: Anthropic 是一家总部位于旧金山的 AI 安全公司，由 OpenAI 前员工于 2021 年创立，Claude 是其旗舰大语言模型，可通过聊天机器人、API 以及智能体编程工具访问。与其他云端托管的 LLM 一样，Claude 运行在 Anthropic 的服务器上，用户输入的提示词会经过公司基础设施，可能依据服务商的使用与安全政策被审查、过滤或上报。由于这类系统是集中式的，它们并不天然等同于只有作者本人能读取的本地文本文件，这也正是本案中隐私期待存在争议的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者观点严重分化：许多人认为该指控在法律上站不住脚，因为威胁内容从未传输给任何人，只是通过服务商监控被发现；另一些人则对 Anthropic 表示同情，指出 OpenAI 曾因未上报枪手而遭抨击，这形成了“做也不是、不做也不是”的两难。还有一派主张用户应集资在本地硬件上运行去审查（abliterated）的开源模型，使私人写作不再受企业审查。

**标签**: `#AI Ethics`, `#Privacy`, `#LLM Surveillance`, `#Free Speech`, `#Anthropic`

---

<a id="item-4"></a>
## [苹果的隐私模式对上黑客友好型 Agentic AI 未来](https://stratechery.com/2026/apple-and-a-hackers-future/) ⭐️ 8.0/10

Ben Thompson 在 Stratechery 发表文章，认为苹果以隐私和安全为先的产品理念，可能与他自己正在迈向的那种自由奔放、由 Agentic AI 驱动的未来存在根本性冲突。该文在 Hacker News 上引发热烈讨论（193 分、177 条评论），围绕全盘访问权限、远程访问安全以及 Meta 的 AI 代理 Muse 展开辩论。 苹果的差异化竞争力建立在隐私与安全之上，因此如果下一波 Agentic AI 若要真正有用就需要广泛的系统与数据访问权限，那么这种围墙花园式的立场就有可能从优势变成竞争劣势。这会影响所有开发或购买 AI 代理的人，也迫使用户在便利与生产力同无处不在的窥探风险之间做出权衡。 讨论揭示了一个具体的安全反差：评论者指出 Thompson 将 VNC／Apple Remote Desktop 无过滤地开放到公网，据称被 Claude 发现，同时他们批评 Meta 的 Muse 在据称从未获授权读取的情况下，发送了一条引用某人私有 Apple Messages 会话的未经请求通知。这些案例凸显了黑客式开放与苹果试图提供的自动保护之间的张力。

hackernews · maguay · 10月5日 10:05 · [社区讨论](https://news.ycombinator.com/item?id=49962857)

**背景**: Stratechery 是分析师 Ben Thompson 广受关注的科技战略博客，以剖析平台与生态动态著称。Agentic AI 指的是能够追求目标、调用外部工具并以一定自主性执行多步骤操作的 AI 程序，通常由大语言模型驱动，这与 2023 年常见的、仅针对狭窄任务的工具型聊天机器人形成对比。苹果的核心营销与设计标识建立在强大的设备端隐私和封闭式安全之上，因此需要深度系统访问的代理的兴起，给公司带来了直接的战略问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Agentic_AI">Agentic AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apple_Inc.">Apple Inc. - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同苹果的主张正面临真实压力：有人把文章比作窥见一道“AI 鸿沟”，即人们即使牺牲隐私也要采用代理；也有人认为 Thompson 将 VNC／ARD 暴露在公网是“近乎犯罪式的安全意识缺失”。另一些人则反驳说，苹果虽不完美，但“一直努力做正确的事”，还有数人认为更大的风险在于用户会逐渐习惯像 Muse 这类产品所带来的自由与无处不在的窥探。

**标签**: `#Apple`, `#AI agents`, `#privacy`, `#security`, `#platform strategy`

---

<a id="item-5"></a>
## [高通与华为达成广泛专利协议，获 LogicFolding 芯片技术许可](https://www.bloomberg.com/news/articles/2026-10-05/qualcomm-licenses-patents-on-huawei-s-logicfolding-chip-tech) ⭐️ 8.0/10

华为与高通宣布达成一项为期多年、范围广泛的专利交叉许可协议，覆盖 5G、计算、人工智能和网络等多个领域；高通还将获得华为 LogicFolding 芯片制造技术相关专利的许可，并购买华为部分美国专利。该交易尚需获得必要的监管批准，华为称其专利许可协议的累计预期合同价值预计将超过 69 亿美元（约合 463.02 亿元人民币）。 这笔交易标志着半导体知识产权流动方向的一次罕见逆转——由中国通信巨头向美国主要芯片厂商授权先进芯片技术，而非相反，这在美中技术摩擦持续的大背景下意义突出。它可能改变业界对先进封装 IP 主导权的预期，并影响爱立信、诺基亚等竞争对手在 5G 与 AI 基础设施领域的竞争格局。 LogicFolding 是华为的先进 3D 封装方案，采用两个逻辑层面对面的堆叠、混合键合以及高密度垂直互连，取代较长的水平布线；它被定位为华为“Tau 缩放定律”的一部分，目标是在不使用 EUV 光刻的情况下于 2031 年实现 1.4nm 级芯片密度。社区讨论指出，尽管该设计涉及多层晶圆，但由于信号在层间空间中传输距离更短、无需横穿整块芯片，实际上反而能降低整体发热。

hackernews · 0xedb · 10月5日 07:46 · [社区讨论](https://news.ycombinator.com/item?id=49961861)

**背景**: 数十年来，半导体产业依赖摩尔定律——通过不断缩小晶体管来让芯片更快更便宜；但随着制程微缩放缓、出口管制又使中国企业难以获得 EUV 光刻设备，厂商越来越多转向先进封装和 3D 堆叠来提升性能。LogicFolding 是华为几个月前才发布的技术，将首发于 Mate 90 系列的麒麟处理器，通过垂直堆叠逻辑层来缩短布线、改善功耗与散热表现。华为目前仍在美方的实体清单上，因此这笔交易引发了关于高通如何能达成此类协议的法律疑问，并预计需要获得监管批准才能完成。此类专利交叉许可在电信行业并不少见，但由中国企业向美国芯片巨头提供技术则打破了以往的惯例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://insightsintegration.com/logic-folding-explained-huaweis-chip-packaging-breakthrough-that-could-redefine-the-ai-race/">Logic Folding Explained : Huawei 's Chip ... - Insights Integration</a></li>
<li><a href="https://www.kad8.com/hardware/huawei-tau-scaling-how-logicfolding-targets-chip-power-and-heat/">Huawei Tau Scaling: How LogicFolding Targets Chip Power and Heat</a></li>
<li><a href="https://timesofindia.indiatimes.com/technology/tech-news/explained-what-is-huaweis-logicfolding-tau-scaling-law-and-how-it-plans-to-build-1-4nm-chips-without-asml/articleshow/131314122.cms">Explained: What is Huawei's LogicFolding , Tau... - The Times of India</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍把“角色逆转”视为核心看点：有人提到一位中国评论人士称华为此次将从高通获得净收入，从而从被许可方变成许可方，但也提醒该消息源常常有选择性地呈现事实。其他人则认为 LogicFolding 通过缩短信号路径来降低发热的思路十分巧妙，同时质疑在高通面对实体清单限制的情况下如何能签署这样的协议，也有人好奇爱立信会作何反应，并讽刺美国如今似乎把当年宣称至关重要的 5G 领先地位拱手让出。

**标签**: `#Semiconductors`, `#Huawei`, `#Qualcomm`, `#Patent Licensing`, `#Geopolitics`

---

<a id="item-6"></a>
## [Yandex Music 的 Sona：一个 Transformer 取代 15+ 推荐组件](https://www.reddit.com/r/MachineLearning/comments/1wy4qxm/sona_one_transformer_replaced_our_15_candidate/) ⭐️ 8.0/10

Yandex Music 介绍了 Sona——一个端到端 Transformer，在音乐推荐生产系统中取代了 15 个以上的候选生成器、粗排模型和精排模型，并采用了一种名为 History Compression 的新注意力方案。在智能音箱上为期 7 天、每组覆盖 15% 用户的 A/B 测试中，Sona 相比生产对照组取得 +4.53% 活跃用户和 +6.30% 总收听时长，二者均在 p < 0.01 下显著，但目前尚未全量上线。 对于正在兴起的单模型生成式推荐趋势（可参照 HSTU、OneRec）而言，这是一个来自大规模生产环境的可信 A/B 结果，说明经典的多阶段“召回—粗排—精排”链路可以被压缩进一个 Transformer，而不牺牲业务指标。如果更长期的测试能持续验证，这将指向显著更简单的推荐架构、更少的独立训练与维护组件，从而影响推荐团队设计与运维整个链路的方式。 History Compression 把 8,192 条事件的历史切成较旧的 6,144 条与最近的 2,048 条两个块，两块通过交叉注意力以及一层全历史自注意力交换信息，随后仅对最近的 2,048 条运行 7 层堆叠，从而将推理成本大致减半，同时保留全注意力的大部分质量。候选项以 Semantic ID 形式由 beam search 生成并随即打分；由于解码器与 Ranking Module 读取同一份编码器输出，编码器每个请求只运行一次。需要注意的是：其类目覆盖率低于现有生产链路（原因仍在排查），且更长期的 A/B 测试正在进行中。

reddit · r/MachineLearning · /u/SettingAccording8986 · 10月5日 10:07

**背景**: 大型推荐系统传统上以流水线形式搭建：多个候选生成器（召回器）各自提出物品，粗排模型低成本地裁剪列表，随后由使用数百个特征、计算更重的精排模型对存活项排序。生成式推荐则把推荐视为序列生成问题，训练 Transformer 直接从用户历史中生成物品标识符（通常是 Semantic ID，即代表每个物品的紧凑学习编码），生成式检索方向的研究即属此类。其最大障碍是成本：标准自注意力的开销随历史长度呈二次增长，因此压缩或重组长历史的方法，才是让长上下文推荐 Transformer 真正可用的关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2305.05065">Recommender Systems with Generative Retrieval</a></li>
<li><a href="https://www.emergentmind.com/topics/compressed-attention-ca">Compressed Attention Techniques</a></li>
<li><a href="https://en.wikipedia.org/wiki/Recommender_system">Recommender system - Wikipedia</a></li>

</ul>
</details>

**标签**: `#recommender-systems`, `#transformers`, `#attention-mechanisms`, `#production-ml`, `#generative-recommendation`

---

<a id="item-7"></a>
## [2026 年诺贝尔生理学或医学奖授予光遗传学发现者](https://www.nobelprize.org/all-nobel-prizes-2026/) ⭐️ 8.0/10

2026 年诺贝尔生理学或医学奖授予卡尔·戴瑟罗特（Karl Deisseroth）、彼得·赫格曼（Peter Hegemann）和格奥尔格·纳格尔（Georg Nagel），以表彰他们发现光控离子通道并开创光遗传学——这项技术能让活体大脑中单个神经细胞被光开启或关闭。该奖项是 2026 年诺贝尔奖季公布的首批奖项之一。 光遗传学让神经科学第一次拥有了在行为中的动物体内精确开启或关闭特定神经元的工具，取代了粗糙得多的电刺激和损毁方法。此次获奖确立了这项如今已被全球数千个实验室用于解析记忆、恐惧、奖赏和运动等神经环路的技术地位，也凸显出对藻类蛋白的基础研究如何成长为现代脑科学的重要支柱。 该技术的原理是把微生物视蛋白基因——例如来自绿藻的光门控阳离子通道 channelrhodopsin 以及 halorhodopsin——导入神经元，使特定波长的光照能在毫秒级时间尺度上兴奋或抑制这些细胞。需要指出的是，光遗传学目前主要仍是动物模型中的研究工具，因为它需要基因改造和植入式光传输装置，在人类身上的常规治疗应用尚未确立。

telegram · zaihuapd · 10月5日 09:33

**背景**: 光遗传学把光学与遗传学结合起来：先在选定的细胞中表达一种光敏蛋白，再用光束控制这些细胞的电活动。赫格曼和纳格尔在绿藻（衣藻，Chlamydomonas）中鉴定出 channelrhodopsin 是一种光门控离子通道，随后戴瑟罗特在斯坦福的团队于 2005 年证明，将其表达在哺乳动物神经元中可以用光脉冲可靠地驱动神经放电，由此开创了这一领域。诺贝尔生理学或医学奖每年 10 月公布，表彰那些从根本上改变了某个研究领域的发现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.dw.com/zh/美国和德国科学家获得今年度诺贝尔生理学或医学奖/a-79547816">美国和德国科 学 家获得今年度诺贝尔生理 学 或医 学 奖</a></li>
<li><a href="https://www.fmmu.edu.cn/neuron/info/1047/1195.htm">光 遗 传 学 （ optogenetics ...</a></li>
<li><a href="https://cj.sina.com.cn/articles/view/5803416260/159e91ac4001013d0x">Nature：斯坦福骆利群/ Karl Deisseroth 团队强强联合</a></li>

</ul>
</details>

**标签**: `#neuroscience`, `#optogenetics`, `#Nobel Prize`, `#science-news`, `#bioengineering`

---

<a id="item-8"></a>
## [Opus 5.5 智能体宣称筛出两种室温磁性半导体候选材料](https://www.vals.ai/blogs/room-temperature-magnetic-semiconductors) ⭐️ 7.0/10

据 Vals.ai 的一篇博客文章，基于 Claude Opus 5.5 的智能体系统通过自动化密度泛函理论（DFT）筛选，找到了两种室温磁性半导体候选材料。该流程在两个近似层级上评估晶体结构：较快的 PBE+U 和较慢但通常更精确的 HSE06，而报告中给出的带隙与自旋窗口数据来自 HSE06 计算。 这一说法处在“AI for Science”与材料发现的交叉点上，暗示由大模型驱动的智能体有可能压缩寻找新型功能材料时昂贵的前期筛选阶段。如果这些候选材料能通过实验验证，室温磁性半导体对自旋电子学（spintronics）将很有价值；但目前结果纯粹是计算层面的，因此实际影响仍属推测。 这项工作本质上是一次计算筛选，文章并未报告任何实验合成、表征或测量，因此这两个候选材料仍属未经证实的假设，而非已被验证的材料。技术读者应注意，DFT 计算的带隙与磁有序温度对所用的交换关联泛函非常敏感，因此 PBE+U 与 HSE06 结果一致虽然有积极意义，但并不能保证预测的磁有序在真实晶体中于 300 K 下依然存在。

hackernews · outlier99 · 10月5日 21:00 · [社区讨论](https://news.ycombinator.com/item?id=49970667)

**背景**: DFT 是根据原子排布预测材料电子结构的标准量子力学方法；PBE+U 是一种较快的近似，对强关联电子加了修正项，而 HSE06 是计算代价更高、通常被认为更可靠的杂化泛函。磁性半导体指的是既具有半导体性质、又具备稳定磁有序的材料，“室温”之所以关键，是因为这类材料的磁有序往往在低于室温时就消失，从而限制了器件应用。LLM 智能体是把大语言模型与工具调用、记忆和多步自主推理结合起来的 AI 系统，正因如此它们才能无需人类逐条编写输入文件就自动运行此类模拟流程。社区的反应部分受到 LK-99 事件影响——那是 2023 年一项宣称实现室温常压超导的结果，在重复实验中被推翻。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://neomanex.com/models/claude-opus-5-5">Claude Opus 5 . 5 | AI Model Review | Neomanex</a></li>
<li><a href="https://collectdebt.ai/blog/llm-agents-business-automation-guide">LLM agent definition and implementation guide for AI systems</a></li>
<li><a href="https://platform.experientiallabs.ai/models/claude-opus-5.5">Model · Experiential</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论帖（约 173 分、131 条评论）既有真实的好奇，也有强烈的怀疑：有评论者搬出 LK-99 事件，表示要“带着一卡车盐”来看待这一声明；也有人质疑这些智能体除了运行常规 DFT 模拟之外究竟做了什么新东西。多位读者对文章的叙述框架提出反驳，指出抗磁性物质和顺磁性物质其实比反铁磁体更常见，而且强调“室温”具有误导性——如今使用的硅和砷化镓半导体本来就在室温下工作，这让人怀疑该词是从超导宣传中借来的。也有更乐观的观点认为，随着 AI 智能体大规模探索可参数化、可检索的科学空间，这类发现会越来越频繁，新颖性的门槛也会随之提高。

**标签**: `#AI for Science`, `#Materials Discovery`, `#LLM Agents`, `#DFT Simulation`, `#Magnetic Semiconductors`

---

<a id="item-9"></a>
## [Cloudflare 推出面向 AI 智能体的 Web Search API](https://developers.cloudflare.com/changelog/post/2026-10-02-introducing-web-search-api/) ⭐️ 7.0/10

2026 年 10 月 2 日，Cloudflare 推出了 Web Search API，为 AI 智能体提供一个统一入口来检索实时网页，请求会被转发给 Ceramic.ai、Linkup、Exa 等第三方搜索提供商，Cloudflare 自身不加价。发布后在 Hacker News 上引发激烈讨论（472 分、214 条评论），话题集中在定价、搜索结果存储条款以及 Cloudflare 日益膨胀的机器人守门人角色上。 Cloudflare 位于互联网流量的关键位置，它推出搜索 API 既为 AI 智能体开发者提供了便捷、统一计费的网页获取途径，也进一步强化了它作为‘决定哪些自动化客户端可以读取网页’的中间人地位。对于正在构建智能体的团队来说，这既是捷径，也是一种集中化风险，需要与直接使用搜索提供商的方式权衡。 定价按用量计费，价格由底层提供商决定并原样透传：通过 Ceramic.ai 约每 1000 次请求 0.25 美元，Linkup 为 5 美元，Exa 为 7 美元，Cloudflare 不额外加价。开发者指出最关键的注意点不在技术层面而在合同层面——通过该 API 返回的结果能否存储、缓存或再分发，条款埋得很深，而据称 Ceramic 的条款禁止收集和聚合搜索结果。

hackernews · tosh · 10月5日 10:47 · [社区讨论](https://news.ycombinator.com/item?id=49963171)

**背景**: Cloudflare 是重要的内容分发网络、DNS 服务商和 DDoS 防护服务提供商，其机器人管理功能实际上已经决定了大量自动化爬虫能否访问某个网站。AI 智能体是能够自主追求目标、调用外部工具并执行多步任务的程序，通常由大语言模型驱动，其中很多需要获取最新的网页结果来支撑回答。为满足这一需求，Brave、Tavily、Exa 等一批搜索 API 应运而生，专门向基于大语言模型的应用出售网页搜索能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.creativeainews.com/articles/cloudflare-web-search-api-agent-search-prices-2026/">Cloudflare Web Search API vs Exa, Brave, Tavily: Prices</a></li>
<li><a href="https://developers.cloudflare.com/ai-gateway/usage/web-search/">Web Search · Cloudflare AI Gateway docs</a></li>
<li><a href="https://securityexpress.info/cloudflare-web-search-api/">Cloudflare Web Search API : Real-Time Browsing for AI</a></li>

</ul>
</details>

**社区讨论**: 讨论中最主要的担忧由 Simon Willison 首先提出：开发者是否被允许存储和再分发搜索结果——如果不行，类似‘分享对话记录’这样的智能体功能就会大打折扣。其他人则拿它与 Google 的 Gemini Flash Lite 2.5 做价格对比，后者每天提供 1000 次免费 Google 搜索，明显更有吸引力；还有多位评论者批评 Cloudflare 在网页抓取上日益强势的守门人角色，质疑开发者为何不直接对接 Exa、Linkup 等提供商。

**标签**: `#cloudflare`, `#web-search-api`, `#ai-agents`, `#api-pricing`, `#infrastructure`

---

<a id="item-10"></a>
## [Chunkr：号称比 Python 工具快约 20 倍的 Rust 文本分块库](https://www.reddit.com/r/MachineLearning/comments/1wyfruw/a_chunking_lib_in_rust_that_is_20x_faster_p/) ⭐️ 7.0/10

一位开发者发布了开源 Rust 文本分块库 Chunkr（github.com/d1pankarmedhi/chunkr），支持字符分块、递归分块、Markdown 标题分块、late chunking、层次化分块等多种策略，并内置原生 PDF 加载器。在 MacBook Air M4 16GB 上测得的基准显示，递归分块吞吐约 2,264 MB/s，而 LangChain 为 769 MB/s、LlamaIndex 仅 10 MB/s；其 PDF 处理流水线比 pypdf 快约 15.9 倍。 文本分块是检索增强生成（RAG）流水线和大规模文档处理中必不可少的环节，常常成为性能瓶颈，因此一个快一个数量级、可无缝替换的分块库能显著缩短数据导入时间并降低算力成本。这也反映出当前的一个趋势：把对延迟敏感的 LLM 数据处理组件用 Rust 重写，再暴露给 Python 使用。 这些数据来自 Reddit 上的自述帖，未经过第三方验证，而且提升并不一致：在 BPE token 分块场景下 Chunkr 只有 38 MB/s，比 LangChain 的 43 MB/s 更慢，也远低于 Chonkie 的 151 MB/s，说明受 tokenizer 制约的工作负载未必受益。所有基准都在同一台 Apple Silicon 机器（M4 Air，16GB）上运行，并采用了匹配参数，例如 1000 字符分块、200 字符重叠。

reddit · r/MachineLearning · /u/Ok_Cartographer5609 · 10月5日 18:11

**背景**: 分块指的是在把文档写入向量数据库或送入大语言模型之前，先将长文档切分成较短的片段，因为模型和检索器都受限于上下文窗口。LangChain、LlamaIndex、semchunk 等 Python 库是常见选择，但它们由纯 Python 实现，在导入大规模语料时往往较慢。Rust 库可以规避大量解释器开销——通常借助 PyO3 包装给 Python 调用——而 'late chunking' 是一种较新的策略：先对整个文档做嵌入，再把 token 级向量池化成块级向量，以保留上下文。基准中提到的 cl100k_base 是 OpenAI GPT-3.5/GPT-4 系列嵌入与对话模型使用的字节对编码（BPE）词表。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/isaacus-dev/semchunk">GitHub - isaacus-dev/ semchunk : A fast, lightweight and easy-to-use...</a></li>
<li><a href="https://huggingface.co/mahnerak/cl100k_base/blob/main/tokenizer.json">tokenizer .json · mahnerak/ cl 100 k _ base at main</a></li>

</ul>
</details>

**标签**: `#Rust`, `#chunking`, `#RAG`, `#performance`, `#LLM`

---

<a id="item-11"></a>
## [用 10 亿局面蒸馏 Stockfish 价值函数，并公开 39 亿局面数据集](https://www.reddit.com/r/MachineLearning/comments/1wxz5qq/distilling_stockfish_on_a_billion_positions_full/) ⭐️ 7.0/10

一位开发者利用 Gigafish 数据集中的 10 亿个国际象棋局面，将 Stockfish 的价值函数蒸馏进 ResNet/ViT 模型中，并在 Hugging Face 上公开了一个包含 39 亿个局面的数据集，这些局面取自 37 个月的 Lichess 对局。该项目的目标是训练出一个能比 Stockfish 自身更快逼近有限深度搜索结果的网络。 国际象棋引擎长期以来是搜索与评估方法的试验场，因此一个由 Stockfish 评估、可免费获取的大规模局面数据集，降低了研究者和爱好者训练自己评估网络的门槛。关于 CNN 与视觉 Transformer 各自优势的发现，对其它棋盘类、网格结构类任务也具有借鉴意义。 搜索深度被刻意固定（公开的数据集是 d10 版本），因为该项目的假设是：限定深度的价值函数实际上是在逼近其下方的搜索树，若能以更快速度复现这一完整搜索结果，模型就能与 Stockfish 现有的小型手工神经网络 NNUE 相竞争。实验中，视觉 Transformer 学习棋盘结构的速度很慢，而 CNN 在训练早期凭借其固有的几何归纳偏置表现更好，两者结合时取得了最佳效果。

reddit · r/MachineLearning · /u/microscope1024 · 10月5日 04:11

**背景**: Stockfish 是最强的开源国际象棋引擎之一，其现代版本依赖 NNUE——一种用于评估局面、配合搜索算法探索着法的小型高效神经网络。知识蒸馏是一种让较小的“学生”模型去模仿更大或更昂贵的“教师”模型输出的技术，从而在几乎不损失精度的情况下实现更快、更廉价的推理。这里的价值函数指的是对某一局面中哪一方占优的估计，而 Lichess 是一个流行的免费在线国际象棋平台，其公开对局库提供了海量真实局面。ResNet 是一种带跳跃连接的卷积网络架构，而 ViT（视觉 Transformer）则将 Transformer 注意力机制应用于棋盘这类类图像输入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation</a></li>
<li><a href="https://huggingface.co/datasets/lukesalamone/gigafish-3.8b-d10">lukesalamone/ gigafish -3.8b-d10 · Datasets at Hugging Face</a></li>

</ul>
</details>

**标签**: `#chess`, `#knowledge-distillation`, `#neural-networks`, `#dataset`, `#reinforcement-learning`

---

<a id="item-12"></a>
## [Quad9 拒绝法国 DNS 封锁令，面临每日最高 58 万欧元罚款](https://torrentfreak.com/dns-resolver-quad9-rejects-french-piracy-blocks-weighs-exit-as-bein-seeks-up-to-e580k-a-day/) ⭐️ 7.0/10

瑞士非营利 DNS 解析服务商 Quad9 拒绝执行法国法院要求其封锁 58 个盗版体育直播相关域名的裁决，版权方 beIN Sports 要求按每域名每日 1 万欧元罚款，合计每日最高 58 万欧元。巴黎法院已于上周四开庭审理，预计三周内作出裁决。 此案检验了一个中立、注重隐私的公共 DNS 解析器是否会被迫执行单一国家的内容封锁制度；若 Quad9 退出法国，可能使数以百万计的用户失去该服务，而这一先例还可能鼓励其他地区提出类似的 DNS 层审查要求。该事件处于互联网治理、反盗版执法与用户隐私的交汇点。 Quad9 表示其从未封锁过任何域名，并且由于其刻意不收集用户数据，无法只针对法国用户实施地域化封锁，因此只能在“全球封锁”和“彻底退出法国市场”之间二选一。它还批评法国 7 月通过的可近乎实时自动将域名列入黑名单的法律“鲁莽且危险”。

telegram · zaihuapd · 10月5日 08:05

**背景**: DNS 解析器负责把人类可读的域名转换为 IP 地址，因此控制解析器的一方只要返回错误或错误地址，就能让某个网站无法访问，这种手段被称为 DNS 封锁。Quad9 是总部位于苏黎世的免费非营利公共递归解析器，专门拦截与恶意软件和钓鱼相关的域名，并受瑞士隐私法管辖，该法律对其全球用户同样提供保护。法国近年来不断扩大反盗版措施，包括网站封锁以及允许自动将域名列入黑名单的新法律，这正是 beIN Sports 与 Quad9 对簿公堂的背景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Quad9">Quad9</a></li>
<li><a href="https://en.wikipedia.org/wiki/DNS_blocking">DNS blocking</a></li>

</ul>
</details>

**标签**: `#DNS`, `#Internet Censorship`, `#Privacy`, `#Internet Governance`, `#France`

---

<a id="item-13"></a>
## [OpenAI 将在欧盟为 AI 生成文本添加隐形水印](https://openai.com/index/eu-text-provenance/) ⭐️ 7.0/10

OpenAI 宣布将在未来几周内，为欧盟地区符合条件的 ChatGPT 和 Codex 文本输出嵌入机器可识别的隐形水印，以满足《欧盟人工智能法案》的内容透明要求。API 用户可为部分模型选择开启水印（默认关闭），同时 OpenAI 开放研究人员和专业机构申请使用文本水印检测器。 这是领先 AI 实验室首批为应对监管而大规模落地文本水印的案例之一，可能为生成式 AI 厂商在《欧盟人工智能法案》下证明内容来源树立事实标准。它影响欧盟的 ChatGPT 与 Codex 用户、API 开发者、研究 AI 检测的学者，以及未来可能面临同样合规压力的其他模型厂商。 该水印对读者不可见但可被机器检测；API 水印对部分模型为可选项而非默认开启，因此非欧盟开发者不会自动受到覆盖。检测器访问权限需通过申请，仅面向研究人员和专业机构；水印也只适用于符合条件模型的输出，而非全部 AI 生成内容。

telegram · zaihuapd · 10月5日 15:25

**背景**: 文本水印通常通过微妙地调整语言模型生成时所偏好的 token（词或子词）来实现，从而嵌入一种统计模式，供配套检测器日后识别。《欧盟人工智能法案》是欧盟的综合性 AI 监管法规，其透明度条款要求对某些 AI 生成或被操纵的内容进行标记或披露，以便人们将其与人工创作内容区分开来。更广义的“内容来源（content provenance）”指对内容来源及生产过程的可记录、可审查追踪，而水印正是为支持这一点而设计的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.brookings.edu/articles/detecting-ai-fingerprints-a-guide-to-watermarking-and-beyond/">Detecting AI fingerprints: A guide to watermarking and... | Brookings</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai">AI Act | Shaping Europe ’s digital future</a></li>
<li><a href="https://grokipedia.com/page/content-provenance-in-ai-publishing">Content Provenance in AI Publishing</a></li>

</ul>
</details>

**标签**: `#AI watermarking`, `#EU AI Act`, `#content provenance`, `#OpenAI`, `#AI regulation`

---

<a id="item-14"></a>
## [SemiAnalysis：Anthropic 订阅价值是 OpenAI 的 5 倍以上](https://newsletter.semianalysis.com/p/anthropic-subscriptions-offer-5x) ⭐️ 6.0/10

SemiAnalysis 发布了一份针对 AI 订阅套餐的限流压测报告，覆盖 Anthropic、OpenAI、Meta、SpaceXSI、MiniMax、Moonshot、Z.ai、Cursor 和 Cognition 等厂商，结论是 Anthropic 的套餐每美元所提供的实际价值至少是 OpenAI 的 5 倍以上。该分析并非单纯对比标价，而是主动把各套餐的使用上限打满，以衡量订阅者真正能获得多少可用容量。 对个人开发者、小团队以及正在挑选 AI 工具的企业来说，这类实测价值对比会直接影响预算与选型；如果某家厂商每美元能提供 5 倍以上的可用容量，就可能推动用户迁移，并迫使竞争对手重新考虑定价与限流策略。这也说明在 LLM 市场中，标价很难反映“每单位有效产出”的真实成本。 其方法是“限流压测”（limit testing），即刻意把每个套餐的额度打满，这比单纯比较价目表更贴近真实使用体验；但各家对限流的定义并不一致（例如按小时的消息数、按天的 token 数、按模型区分的配额），因此绝对数值只能视为近似。还需注意，这是一份偏向消费者与定价层面的分析，而非技术突破，且结论很大程度上取决于用来探测各套餐的具体工作负载。

rss · Semianalysis · 10月5日 20:01

**背景**: SemiAnalysis 是由 Dylan Patel 创立的 AI 基础设施研究与咨询机构，以对芯片供应链、数据中心以及 AI 建设经济性的量化拆解而知名。几乎所有 AI 订阅服务——Anthropic 的 Claude、OpenAI 的 ChatGPT、Meta 的模型，以及 MiniMax、Moonshot、Z.ai、Cursor、Cognition 和源自 xAI 的 SpaceXSI——都设有速率限制（rate limit），也就是在特定时间窗口内限制用户可消耗的额度，因此套餐的真实“价值”取决于它实际能提供多少可用容量。由于厂商会公布月费却很少给出可横向比较的吞吐量数据，第三方限流压测便成为少有的可比对手段。测试名单中出现的 SpaceXSI，是 Elon Musk 于 2026 年 10 月表示要为原 xAI（Grok 系列模型开发商）启用的新名称。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=TIGZdRqi7Ec">Dylan Patel | Lost in Life to Founding SemiAnalysis - YouTube</a></li>
<li><a href="https://en.wikipedia.org/wiki/MiniMax_Group">MiniMax Group</a></li>
<li><a href="https://www.reuters.com/business/media-telecom/musk-says-he-will-rename-spacexai-spacexsi-2026-10-04/">Musk says he will rename SpaceXAI to SpaceXSI | Reuters</a></li>

</ul>
</details>

**标签**: `#AI subscriptions`, `#Anthropic`, `#OpenAI`, `#LLM pricing`, `#benchmarking`

---

<a id="item-15"></a>
## [开发者训练 3.1 万参数 Transformer 预测血糖，并在真实 CGM 数据上做零样本测试](https://www.reddit.com/r/MachineLearning/comments/1wy99gd/i_have_trained_a_model_to_predict_my_blood_sugar/) ⭐️ 6.0/10

一位 Reddit 用户（0xdeadf1sh）训练了一个仅有 31,251 个参数的仅编码器（encoder-only）Transformer——16 层、每层 1 个注意力头、隐藏维度为 16——训练数据全部来自其自制的 1 型糖尿病（T1DM）患者模拟器，随后在自己 30 天的真实连续血糖监测（CGM）数据上做了零样本测试。训练在一块 NVIDIA DGX Spark 上耗时不到 60 分钟，模型通过 ExecuTorch 后端在 Android 应用中运行，并针对三款不同的 CGM 设备（Libre 3 Plus、Anytime CT5 和 Linx 传感器）进行了验证。 这项实验具体展示了：一个小到可以跑在手机上的模型，仅靠合成患者模拟器数据训练，也能在没有见过本人任何血糖读数的情况下迁移到真实血糖曲线上，这为隐私友好的端侧个人健康预测提供了思路。如果这种“合成到真实”的迁移在单个用户之外也能成立，就有可能降低血糖预测研究目前对大型集中式临床数据集的依赖与隐私门槛。 该基础模型预测未来 2 小时，并且可以自回归方式用于更长时段的预测（例如 8 小时夜间血糖）；作者明确表示模型针对反事实推理（counterfactual reasoning）进行了专门训练，图中所示结果均来自未挂载 LoRA 适配器的基础模型，尽管其 App 支持在真实 CGM 曲线上做轻量 LoRA 微调。主要局限在于：这是单用户实验、验证规模有限、训练数据全部为合成数据；作者将模型、模拟器和 Android 应用分别开源为 T1DMAI、T1DMSIM 和 T1DMDROID 三个 GitHub 仓库。

reddit · r/MachineLearning · /u/0xdeadf1sh · 10月5日 13:58

**背景**: 1 型糖尿病（T1DM）是一种自身免疫性疾病，患者的胰腺几乎不产生胰岛素，因此血糖必须持续管理。CGM（连续血糖监测）是一种贴在身上的小型传感器系统，会把血糖读数自动发送到手机 App，这也正是为什么“预测未来血糖”的模型可以直接部署在移动设备上。仅编码器（encoder-only）Transformer 是 BERT 所代表的架构家族，其注意力在输入序列上是双向的，而不是只从左到右；这类模型通常用于理解与表示任务，在这里则被用于时间序列预测。所谓“零样本”，指的是模型在评估前从未用该用户的真实血糖数据做过训练或微调。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.freestyle.abbott/us-en/what-is-cgm.html">What is Continuous Glucose Monitoring ( CGM )? | FreeStyle Libre US</a></li>
<li><a href="https://www.nutrisense.io/what-is-a-cgm">What is a CGM | Continuous Glucose Monitoring Definition and Purpose</a></li>
<li><a href="https://magazine.sebastianraschka.com/p/understanding-encoder-and-decoder">Understanding Encoder And Decoder LLMs</a></li>

</ul>
</details>

**标签**: `#Machine Learning`, `#Healthcare`, `#Time Series Forecasting`, `#Transformer`, `#Diabetes`

---

<a id="item-16"></a>
## [OpenAI 将在 ChatGPT 生成图片时展示视觉广告](https://www.bleepingcomputer.com/news/artificial-intelligence/openai-will-show-visual-ads-in-chatgpt-while-you-generate-images/) ⭐️ 6.0/10

OpenAI 已开始在 ChatGPT 中测试明确标注的视觉广告，广告会在用户生成图片时展示，本月起面向美国首批广告主开放。公司表示广告会有清晰标识，与生成的图片分开呈现，并且不会影响 ChatGPT 的回答内容。 ChatGPT 每周用户约达 12 亿，为 OpenAI 提供了庞大的广告库存，而广告正成为其从免费非订阅用户身上获取收入的重要渠道，不再只依赖付费订阅。这标志着 AI 助手向广告支持模式迈出的重要一步，也可能影响其他 AI 聊天产品的商业模式。 这批广告面向美国首批广告主测试，并且被刻意与图片输出分开放置，以免干扰模型生成的结果；OpenAI 同时配套推出转化衡量工具和品牌安全工具。由于目前报道仅为简短转载，广告定价、具体形式与投放资格等细节尚未得到确认。

telegram · zaihuapd · 10月5日 10:53

**背景**: ChatGPT 是 OpenAI 推出的对话式 AI 助手，也能根据用户要求生成图片。此前它的主要收入来自付费订阅而非广告，因此引入广告对产品而言是一项明显变化。转化衡量指的是追踪广告是否带来购买等目标行为的工具，而品牌安全工具则用于避免品牌广告与有害、冒犯性或不符合品牌调性的内容同时出现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/chatgpt/">Introducing ChatGPT - OpenAI</a></li>
<li><a href="https://vistasocial.com/insights/brand-safety-tools/">Top 12 Brand Safety Tools to Protect Your Reputation | Vista Social</a></li>
<li><a href="https://business.adobe.com/co/products/advertising/brand-safety-tools.html">Brand safety tools help keep your reputation positive</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#ChatGPT`, `#Advertising`, `#Monetization`, `#AI Industry`

---