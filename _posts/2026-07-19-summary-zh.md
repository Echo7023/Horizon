---
layout: default
title: "Horizon Summary: 2026-07-19 (ZH)"
date: 2026-07-19
lang: zh
---

> 从 32 条内容中筛选出 10 条重要资讯。

---

1. [GPT-5.6 通过提示解决了凸优化领域 30 年的难题](#item-1) ⭐️ 9.0/10
2. [LG 显示器通过 Windows Update 静默安装软件](#item-2) ⭐️ 9.0/10
3. [SpaceX 与五角大楼谈判提供 AI 算力](#item-3) ⭐️ 9.0/10
4. [特朗普政府拟设类似 FINRA 的独立 AI 监管机构](#item-4) ⭐️ 9.0/10
5. [Anthropic 撤销移除 Claude Fable 5 计划，保留但降低限额](#item-5) ⭐️ 8.0/10
6. [AI 垃圾被指赢得 DeepMind Kaggle 2.5 万美元大奖](#item-6) ⭐️ 8.0/10
7. [Stereo2Spatial: 扩散模型将立体声转为双耳空间混音](#item-7) ⭐️ 8.0/10
8. [Meta 拟向 Anthropic 出租 AI 算力，潜在交易额百亿美元](#item-8) ⭐️ 8.0/10
9. [Kimi K3：开源 2.8 万亿参数模型，登顶前端编程竞技场](#item-9) ⭐️ 8.0/10
10. [SK 海力士 CEO 警告 2027 年将出现最严重内存短缺](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GPT-5.6 通过提示解决了凸优化领域 30 年的难题](https://old.reddit.com/r/math/comments/1uxj3cy/after_openais_cdc_proof_announcement_gpt56_used_a/) ⭐️ 9.0/10

GPT-5.6 通过单个提示成功解决了凸优化中一个长期未决的难题，填补了长达 30 年的空白。该成就通过一篇引发大量技术讨论的 Reddit 帖子得到确认。 这标志着 AI 驱动数学研究的重大里程碑，表明大型语言模型能够对高级理论问题做出贡献。它可能加速优化理论的进展，并激发解决其他长期未解猜想的新方法。 解决的问题涉及在球形域上优化凸 Lipschitz 函数的时间复杂度上界。使用的模型是 GPT-5.6 Sol Pro，而非更强大的 Ultra 版本。

hackernews · mbustamanter · 7月18日 13:00 · [社区讨论](https://news.ycombinator.com/item?id=48957779)

**背景**: 凸优化是数学优化的一个子领域，研究在凸集上最小化凸函数的问题，广泛应用于工程、机器学习和经济学。30 年的空白指的是关于凸优化中一阶方法最优收敛速度的一个长期猜想，该猜想此前一直未被人类解决。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Convex_optimization">Convex optimization</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的评论者表达了兴奋和怀疑，一些人指出尽管这一结果是真正的贡献，但它可能促使研究人员转向更具创新性的问题，而非低垂的果实。还有讨论使用 LLM 处理其他难以理解的证明，例如 abc 猜想。

**标签**: `#AI`, `#convex optimization`, `#mathematics`, `#research breakthrough`, `#GPT-5.6`

---

<a id="item-2"></a>
## [LG 显示器通过 Windows Update 静默安装软件](https://videocardz.com/newz/lg-monitors-silently-install-software-through-windows-update-without-user-consent) ⭐️ 9.0/10

LG 显示器利用 Windows Update 的设备元数据功能，在用户插入显示器时自动静默安装一个显示 McAfee 广告的配套应用，无需用户同意。 这种做法在用户不知情的情况下安装了具有完全系统访问权限和网络连接的软件，带来了严重的安全和隐私风险，可能使用户暴露于广告软件或恶意软件之中，破坏了用户对 Windows 更新和硬件生态系统的信任。 该安装的软件随系统每次启动而运行，具有互联网和完全系统访问权限，且无沙箱隔离，影响新老 LG 显示器。解决方法包括通过组策略或设备安装设置禁用制造商应用的自动下载。

hackernews · baranul · 7月18日 10:21 · [社区讨论](https://news.ycombinator.com/item?id=48956688)

**背景**: Windows 更新可以为硬件设备提供驱动程序和配套软件，通常需要用户同意。LG 的应用本应是用于色彩模式、屏幕控制或固件交付的显示器配套软件，但同时也推送 McAfee 广告。这种静默安装利用了 Windows 的设备元数据功能，该功能本用于合法的外设软件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/windows-update-installs-lg-monitor-app-pushes-mcafee-ads/">Windows Update Silently Installs LG Monitor App That Pushes ...</a></li>
<li><a href="https://cybersecuritytimes.com/lg-monitor-app-windows-metadata-adware/">LG Monitor App Installer Turns Windows Hardware Metadata Feature Into Adware Delivery Channel</a></li>
<li><a href="https://windowsforum.com/threads/lg-monitor-app-installer-pushes-mcafee-ads-on-windows-11.439030/">LG Monitor App Installer Pushes McAfee Ads on Windows 11</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了愤怒，称其行为类似恶意软件。用户提供了通过组策略或设备安装设置的解决方法。一些人指出，问题比标题所述更严重，因为它静默发生，拥有完全系统访问权限，且影响所有 LG 显示器，而不仅仅是新的。

**标签**: `#security`, `#privacy`, `#windows`, `#lg`, `#malware`

---

<a id="item-3"></a>
## [SpaceX 与五角大楼谈判提供 AI 算力](https://www.wsj.com/tech/ai/spacex-in-talks-to-provide-computing-power-for-pentagons-ai-push-15e752e4) ⭐️ 9.0/10

SpaceX 正与美国国防部谈判，拟提供用于运行 AI 模型的数据中心算力，交易金额可能高达数十亿美元。 这一潜在交易将加深 SpaceX 与五角大楼的关系，并显著增强军方的 AI 能力，对国家安全和云计算市场产生深远影响。 谈判仍在进行中，存在破裂可能；SpaceX 近期已与 Anthropic 和谷歌签署了类似算力协议，并计划扩展其云计算业务。

telegram · zaihuapd · 7月18日 01:44

**背景**: 五角大楼正加速获取云计算能力，以支持国家安全和日常作战中的 AI 应用。该部门近期已批准 SpaceX、亚马逊、谷歌、微软和甲骨文等公司在机密环境中使用 AI 模型。

**标签**: `#AI算力`, `#SpaceX`, `#五角大楼`, `#云计算`, `#国家安全`

---

<a id="item-4"></a>
## [特朗普政府拟设类似 FINRA 的独立 AI 监管机构](https://www.bloomberg.com/news/articles/2026-07-17/us-considers-creating-finra-like-watchdog-to-vet-top-ai-models) ⭐️ 9.0/10

特朗普政府正考虑设立一个类似金融业监管局（FINRA）的独立机构，负责审查顶尖 AI 模型的安全性，以回应华尔街对网络安全的担忧以及硅谷对政府临时管控措施的不满。 此举可能重塑 AI 治理格局，让行业领袖在制定安全标准方面拥有更大话语权，并可能为全球 AI 监管树立先例，直接影响 OpenAI 和 Anthropic 等关键公司。 该计划由财政部长斯科特·贝森特牵头制定，目前正由白宫幕僚长苏茜·威尔斯审阅，尚未提交总统特朗普。此前，Anthropic 和 OpenAI 均因美国政府要求修改或延迟发布模型而提出异议。

telegram · zaihuapd · 7月18日 05:45

**背景**: FINRA（金融业监管局）是一家私人自律监管组织，负责监管美国证券经纪商和交易所。拟议中的 AI 监管机构将是一个由行业资助但获得政府支持的自律组织，类似于 FINRA 在 SEC 监督下的运作模式。Google DeepMind 首席执行官德米斯·哈萨比斯本周也提出了类似建议，即建立行业资助的独立监管机构来审查前沿 AI 模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Financial_Industry_Regulatory_Authority">Financial Industry Regulatory Authority - Wikipedia</a></li>
<li><a href="https://news.skrew.ai/us-finra-style-agency-review-ai-models/">US Weighs Finra-Style Agency to Vet AI Models</a></li>
<li><a href="https://logicity.in/en/blog/deepmind-ceo-proposes-finra-style-body-for-ai-regulation">DeepMind CEO proposes FINRA-style body for AI regulation | Logicity</a></li>

</ul>
</details>

**标签**: `#AI监管`, `#政策`, `#特朗普`, `#人工智能`, `#网络安全`

---

<a id="item-5"></a>
## [Anthropic 撤销移除 Claude Fable 5 计划，保留但降低限额](https://simonwillison.net/2026/Jul/18/claude-make-fable-5-permanent/#atom-everything) ⭐️ 8.0/10

Anthropic 在推特上宣布，从 7 月 20 日起，Claude Fable 5 将保留在 Max 和 Team Premium 套餐中，限额为原来的 50%，而 Pro 和 Team Standard 用户可通过使用额度获得访问权限，并获一次性 100 美元额度，这推翻了此前将模型完全从订阅中移除的计划。 这一反转凸显了 AI 模型市场激烈的竞争态势——Anthropic 因 OpenAI 的 GPT-5.6 Sol 和 Kimi 3 而被迫让步，同时确保订阅用户仍能访问 Anthropic 的顶级模型，维护了订阅价值。 最初移除 Fable 5 订阅的计划源于算力容量担忧，但竞争压力使其无法维持；每月 20 美元套餐的用户仍无法访问。该变更于 2026 年 7 月 20 日生效。

rss · Simon Willison · 7月18日 06:00

**背景**: Claude Fable 5 是 Anthropic 最先进的大型语言模型，属于 Claude Mythos 系列，以强大的编码和软件漏洞检测能力著称。竞品如 OpenAI 的 GPT-5.6 Sol 和 Kimi 3（即 Kimi K3）近期在性能上达到或超越它，给 Anthropic 的定价策略带来压力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6 - Wikipedia</a></li>
<li><a href="https://platform.kimi.ai/">Kimi API Platform</a></li>

</ul>
</details>

**标签**: `#AI`, `#Anthropic`, `#Claude`, `#pricing`, `#competition`

---

<a id="item-6"></a>
## [AI 垃圾被指赢得 DeepMind Kaggle 2.5 万美元大奖](https://www.reddit.com/r/MachineLearning/comments/1uzyf66/did_blatant_ai_slop_just_win_a_25k_usd_deepmind/) ⭐️ 8.0/10

一位 Reddit 用户出示证据，表明一个被描述为“乱炖意面”的无意义 AI 提交方案，在谷歌 DeepMind 赞助的 Kaggle 竞赛“衡量 AGI 进展——认知能力”中赢得了 2.5 万美元大奖。 这一指控挑战了重大 AI 竞赛的诚信，引发了对研究验证质量和评审标准的担忧，可能影响社区驱动的 AI 基准测试工作的信任度。 获胜提交方案据称包含毫无根据的主张和一个数字生成机器，远超要求的格式，评委据报未能进行粗略阅读。组织者坚持认为评审是恰当的，批评是主观的。

reddit · r/MachineLearning · /u/TheWerkmeister · 7月18日 15:10

**背景**: AI 垃圾指由生成式 AI 大量生产的低质量数字内容，通常缺乏努力或意义。该 Kaggle 竞赛要求参与者设计基于认知科学的新型 AI 基准，旨在从多个认知维度衡量 AGI 进展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_slop">AI slop - Wikipedia</a></li>
<li><a href="https://www.mindstudio.ai/blog/google-agi-benchmark-10-cognitive-dimensions">How Google's New AGI Benchmark Measures Intelligence Across 10 Cognitive Dimensions | MindStudio</a></li>
<li><a href="https://oecs.mit.edu/pub/dtatgf1j">AI Model Evaluation · Open Encyclopedia of Cognitive Science</a></li>

</ul>
</details>

**社区讨论**: Reddit 社区对获胜提交方案普遍持怀疑态度，许多用户表示愤怒，并呼吁对评审过程进行深入调查。一些用户认为，没有代码或数据，批评仍属推测。

**标签**: `#Kaggle`, `#DeepMind`, `#AI ethics`, `#research integrity`, `#competition`

---

<a id="item-7"></a>
## [Stereo2Spatial: 扩散模型将立体声转为双耳空间混音](https://www.reddit.com/r/MachineLearning/comments/1uzevbg/stereo2spatial_convert_stereo_music_tracks_to/) ⭐️ 8.0/10

作者发布了 Stereo2Spatial，一种扩散模型，可将立体声音乐曲目转换为空间化双耳混音。该模型最初使用 VAE 进行潜在编码，后改为原始波形处理并采用振幅提升技术以保证稳定性。 该项目通过将现有立体声音乐转换为沉浸式双耳格式，无需多声道录音，从而实现了空间音频的普及。它使空间音乐可以应用于庞大的立体声内容库，可能改变听众用耳机体验音乐的方式。 波形模型在 7,669 首曲目上使用两块 A6000 GPU 训练了 20 天，采用来自 WavFlow 论文的振幅提升技术以稳定训练。它支持可控的混音风格条件输入并直接输出双耳音频，还提供了一个 Windows 桌面应用进行推理。

reddit · r/MachineLearning · /u/kittenkrazy · 7月17日 22:55

**背景**: 空间音频（包括双耳渲染）能够创建三维声场，模拟人类在真实环境中感知声音的方式。传统的立体声转空间音频通常需要手动混音或复杂的多声道设置。扩散模型是一类生成模型，通过逐步去噪随机噪声来生成高质量输出，已成功应用于语音合成和音乐生成等音频任务。该模型使用了类似 EAR-VAE 的变分自编码器（VAE）将音频编码至压缩的潜在空间后再进行处理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/earlab/EAR_VAE">earlab/EAR_VAE · Hugging Face</a></li>
<li><a href="https://arxiv.org/html/2601.19657v4">One Token Is Enough: Improving Diffusion Language Models with a Sink Token</a></li>

</ul>
</details>

**标签**: `#audio processing`, `#spatial audio`, `#diffusion models`, `#machine learning`

---

<a id="item-8"></a>
## [Meta 拟向 Anthropic 出租 AI 算力，潜在交易额百亿美元](https://www.nytimes.com/2026/07/17/technology/meta-anthropic-ai-computing-power.html) ⭐️ 8.0/10

Meta 正与 AI 初创公司 Anthropic 进行早期谈判，拟将其 AI 数据中心算力租予对方，潜在交易规模高达两年 100 亿美元。 这笔交易凸显了 AI 算力的严重稀缺性，同时 Meta 可借此从其巨额基础设施投资中获得新收入，并可能缓解投资者对其资本支出的担忧。 Anthropic 于 2026 年 6 月提出该方案；协议下 Anthropic 将按月付款，双方均可提前退出。谈判尚处早期阶段，未必能最终成交。

telegram · zaihuapd · 7月18日 01:14

**背景**: 像 Anthropic 这样的 AI 公司需要大量算力来训练和运行大型语言模型，但专用硬件（如 GPU）供应紧缺。Meta 今年计划投入高达 1450 亿美元，主要用于 AI 和数据中心建设，已建立多余算力可供对外租赁。

**标签**: `#AI`, `#Compute`, `#Meta`, `#Anthropic`, `#Business`

---

<a id="item-9"></a>
## [Kimi K3：开源 2.8 万亿参数模型，登顶前端编程竞技场](https://t.me/zaihuapd/42637) ⭐️ 8.0/10

月之暗面发布了 Kimi K3，这是全球首个开源的 2.8 万亿参数模型，在 Frontend Code Arena 中以 1679 分排名第一，超越了 Claude Fable 5 和 GPT-5.6 Sol。 这一里程碑表明，超大规模开源模型能够在代码生成等领域与闭源领先者竞争，可能加速开源 AI 发展并加剧竞争。 Kimi K3 采用了 Kimi Delta Attention 和 Attention Residuals 架构，具备原生视觉能力和 100 万 token 上下文窗口，在 Frontend Code Arena 中从第 18 名（Kimi k2.6）跃升至第 1 名。

telegram · zaihuapd · 7月18日 02:29

**背景**: 大型语言模型通常为闭源，开源模型规模较小。Kimi Delta Attention 是一种线性注意力机制，用于高效长上下文处理；Attention Residuals 则用基于深度的学习注意力替代标准加法残差，提高训练稳定性和表示能力。Frontend Code Arena 用于评测 AI 模型的前端代码生成任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.26692">[2510.26692] Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://arxiv.org/abs/2603.15031">[2603.15031] Attention Residuals - arXiv.org GitHub - MoonshotAI/Attention-Residuals Attention Residuals - arXiv.org Attention Residuals - Papers with Code Attention Residuals Explained: Rethinking Transformer Depth Open Attention Residuals: Replacing Additive Residuals with ... Attention Residuals: When Residuals Start Attending To ...</a></li>
<li><a href="https://www.frontendarena.online/">Home | Frontend Arena</a></li>
<li><a href="https://officechai.com/ai/kimi-k3-beats-fable-5-gpt-5-6-sol-on-frontend-code-arena/">Kimi K3 Beats Fable 5, GPT 5.6 Sol On Frontend Code Arena</a></li>

</ul>
</details>

**标签**: `#AI`, `#Open Source`, `#Large Language Model`, `#Benchmarks`

---

<a id="item-10"></a>
## [SK 海力士 CEO 警告 2027 年将出现最严重内存短缺](https://t.me/zaihuapd/42645) ⭐️ 8.0/10

SK 海力士 CEO 郭鲁正警告，全球内存行业将在 2027 年面临史上最严重的供应短缺，即使积极扩产，客户需求在 2030 年后仍将超过供应能力。 这一来自领先内存制造商的警告预示着 HBM 和 DDR5 等关键组件将长期供应紧张，影响全球 AI、数据中心和消费电子市场。 SK 海力士正在考虑在美国、日本和东南亚设立海外晶圆厂，优先选择土地、电力和人力成本最具优势的地区。该公司 2025 年营业利润达创纪录的 47 万亿韩元（约 310 亿美元），2026 年第二季度预计进一步增至 65.5 万亿韩元。

telegram · zaihuapd · 7月18日 06:30

**背景**: 内存芯片包括 DRAM 和 NAND 闪存，是计算设备的关键组件。HBM（高带宽内存）对于 AI 加速器至关重要。供应短缺可能由于产能限制以及来自 AI 和云计算的需求激增而发生。

**标签**: `#semiconductor`, `#memory`, `#supply chain`, `#SK Hynix`, `#industry forecast`

---