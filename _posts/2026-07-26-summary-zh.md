---
layout: default
title: "Horizon Summary: 2026-07-26 (ZH)"
date: 2026-07-26
lang: zh
---

> 从 24 条内容中筛选出 9 条重要资讯。

---

1. [SGLang v0.5.16：DSpark 投机解码与 Inkling MoE 支持](#item-1) ⭐️ 9.0/10
2. [vLLM v0.26.0 新增 Inkling 支持，提升 DeepSeek-V4 性能](#item-2) ⭐️ 8.0/10
3. [开放权重 AI 正经历其 Kubernetes 时刻](#item-3) ⭐️ 8.0/10
4. [Android 可能限制设备端 ADB](#item-4) ⭐️ 8.0/10
5. [介绍 Claude Opus 5](#item-5) ⭐️ 8.0/10
6. [AMD 用 MI455X 和智能内核生成挑战 CUDA 壁垒](#item-6) ⭐️ 8.0/10
7. [中国发布离岸信托个税新规](#item-7) ⭐️ 8.0/10
8. [市场监管总局对携程罚款 51.79 亿元](#item-8) ⭐️ 8.0/10
9. [微软将用 TPM 芯片封堵盗版 Windows 激活](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.16：DSpark 投机解码与 Inkling MoE 支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 9.0/10

SGLang v0.5.16 引入了 DSpark，一种基于置信度的投机解码算法，达到 383.7 tok/s，并新增了对 9750 亿参数多模态 MoE 模型 Inkling 的支持。 此版本显著提升了推理吞吐量，为大型模型提供了更快的生成速度。DSpark 的自适应验证和 Inkling 的巨大规模展示了多模态和 MoE 架构在高效推理方面的进展。 DSpark 采用半自回归草稿生成和基于置信度的验证窗口大小调整。Inkling 结合了滑动窗口、全注意力和 Mamba2 线性注意力，支持 NVFP4 量化，并处理 100 万 tokens 的上下文。该版本还移除了实验性的 QServe 和 FBGEMM FP8 路径。

github · Qiaolin-Yu · 7月25日 00:13

**背景**: 投机解码通过一个小型草稿模型生成候选 tokens，再由目标模型验证，从而加速 LLM 推理。MoE（混合专家）模型每个 token 只激活一部分参数，在高效计算的同时实现大模型容量。SGLang 是一个针对大型语言和视觉模型优化的开源推理引擎。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative ...</a></li>
<li><a href="https://www.marktechpost.com/2026/06/27/deepseek-releases-dspark-a-speculative-decoding-framework-that-accelerates-deepseek-v4-per-user-generation-60-85-over-mtp-1/">DeepSeek Releases DSpark, a Speculative Decoding Framework ...</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#MoE`, `#large language models`, `#inference optimization`, `#SGLang`

---

<a id="item-2"></a>
## [vLLM v0.26.0 新增 Inkling 支持，提升 DeepSeek-V4 性能](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 为 TML Inkling 多模态模型系列提供了首发支持，通过专用内核和路由优化显著提升了 DeepSeek-V4 的性能，并新增了按 KV 缓存组选择注意力后端等多项增强。 此版本展示了 vLLM 作为前沿 LLM 高性能推理引擎的持续作用：为首个主要新模型系列（Inkling）提供了首发支持，并对流行的 DeepSeek-V4 模型进行了深度优化，使研究人员和产品用户都受益。 Inkling 支持包括分片 CUDA 图、Hopper FA4 相对注意力、MTP=1 推测解码、LoRA 和 ModelOpt NVFP4 量化。对于 DeepSeek-V4，专用路由内核实现了 2.94% 的端到端 TPOT 提升，fused_topk_bias 实现了 1.5–2 倍的内核加速。新的 head_dtype 选项支持 fp32 lm_head，提高了生成精度。

github · khluu · 7月25日 10:38

**背景**: vLLM 是由加州大学伯克利分校和社区贡献者开发的开源高吞吐量 LLM 推理引擎。TML Inkling 是 Thinking Machines Lab 推出的 1 万亿参数多模态模型，支持文本、图像和音频输入。DeepSeek-V4 是 DeepSeek 开源权重 LLM 系列的最新版本，以其经济高效的训练和具有竞争力的性能而闻名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-07-15-inkling">TML Inkling on vLLM: Day-0 Support with Optimized Performance</a></li>
<li><a href="https://docs.vllm.ai/en/latest/api/vllm/models/inkling/">inkling - vLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#performance optimization`, `#release notes`

---

<a id="item-3"></a>
## [开放权重 AI 正经历其 Kubernetes 时刻](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 8.0/10

2026 年 7 月 25 日发布的这篇文章，直接将开放权重 AI 模型的崛起与 Kubernetes 的发展轨迹进行类比，认为开放权重 AI 正成为防止厂商锁定并降低成本的互操作标准。 这一类比具有重要意义，因为它表明开放权重 AI 可能重塑 AI 基础设施格局，减少对封闭 API 提供商的依赖，并像 Kubernetes 标准化云原生计算一样，促进更具竞争力的生态系统。 开放权重模型允许用户下载模型的学习参数进行定制和本地部署，但与完全开源的 AI 不同，训练数据和代码并不总是包含在内。文章强调，这种权衡类似于 Kubernetes 作为可移植抽象层的作用，而不暴露所有底层细节。

hackernews · tknaup · 7月25日 14:49 · [社区讨论](https://news.ycombinator.com/item?id=49048034)

**背景**: 开放权重 AI 模型将其内部参数（权重）开放下载，使用户能够在自己的硬件上运行和微调模型，但可能不符合开源软件的所有标准。Kubernetes 最初由谷歌开发，后来成为容器编排的事实标准，防止了云部署中的厂商锁定。云原生计算基金会（CNCF）的成立是为了以中立开源项目的形式管理 Kubernetes。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/open-weight-ai-what-we-finally-opened-bonnet-nicolas-pistorio-n3ulf">Open - weight AI : what if we finally opened the bonnet ?</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kubernetes">Kubernetes - Wikipedia</a></li>
<li><a href="https://kingy.ai/blog/open-models-vs-closed-models/">Open Models vs Closed Models: The 2026 AI Verdict</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍赞同这一类比，用户指出开放权重模型为推理定价（代币经济学）提供了合理的基线，并可能实现类似 Linux 的协作式模型开发。但也有人对硬件成本以及完全实现这种类比所需的真正开放训练数据表示担忧。还有评论称赞通过政府采购推动对可互操作系统需求的想法。

**标签**: `#AI`, `#open-source`, `#industry-trends`, `#analogy`, `#infrastructure`

---

<a id="item-4"></a>
## [Android 可能限制设备端 ADB](https://kitsumed.github.io/blog/posts/android-may-soon-restrict-on-device-adb/) ⭐️ 8.0/10

Google 正在考虑限制设备端 ADB 访问，可能要求额外身份验证或限制可连接的 IP 地址，该变更源自 Android 问题追踪器中的一个功能请求。 这一变更可能影响依赖 ADB 进行调试和侧载的 Android 开发者，虽然可能减少攻击面，但也限制了开发者的控制权和自由。 提议的限制主要针对设备端 ADB（无线调试），而非基于 USB 的 ADB；一些建议包括仅允许来自特定 IP 地址的连接，或要求确认对话框。

hackernews · shscs911 · 7月25日 06:57 · [社区讨论](https://news.ycombinator.com/item?id=49045159)

**背景**: ADB（Android 调试桥）是一种命令行工具，允许开发者与 Android 设备通信以进行调试和应用安装。设备端 ADB 支持无需电脑的无线调试，方便开发者和高级用户。该功能常用于侧载应用和访问高级设置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Android_Debug_Bridge">Android Debug Bridge - Wikipedia</a></li>
<li><a href="https://developer.android.com/tools/adb">Android Debug Bridge (adb) | Android Studio | Android Developers</a></li>
<li><a href="https://medium.com/@EazSoftware/a-comprehensive-guide-to-adb-android-debug-bridge-the-unsung-hero-for-android-developers-28b349037436">A Comprehensive Guide to ADB (Android Debug Bridge): The ...</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：有人认为该变更没有必要，因为启用 ADB 已需用户同意；而另一些人则认为这是 Google 逐步收紧 Android 控制的一部分，使 Android 不再比 iOS 更开放。多位评论者担忧未来对侧载和开发者自主权的进一步限制。

**标签**: `#Android`, `#ADB`, `#security`, `#developer tools`, `#Google`

---

<a id="item-5"></a>
## [介绍 Claude Opus 5](https://simonwillison.net/2026/Jul/24/introducing-claude-opus-5/#atom-everything) ⭐️ 8.0/10

Anthropic 推出 Claude Opus 5，这是一款成本效益高、可与前沿智能相媲美的模型。

rss · Simon Willison · 7月24日 23:48

**标签**: `#AI`, `#large language models`, `#Claude`, `#Anthropic`

---

<a id="item-6"></a>
## [AMD 用 MI455X 和智能内核生成挑战 CUDA 壁垒](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

在 Advancing AI 2026 上，AMD 推出了 Instinct MI455X GPU 和 Helios 机架级系统，同时披露了一项名为“智能内核生成”的新软件计划，旨在利用强化学习自动优化 CUDA 内核。 AMD 的努力可能通过改进 ROCm 软件栈并提供有竞争力的硬件来削弱 Nvidia 的 CUDA 垄断，从而降低 AI 基础设施成本并增加选择。 MI455X 采用 2nm 工艺，配备 432GB HBM4 内存，在 MXFP8/MXFP4 上性能可达 MI355X 的 4 倍；Helios 机架通过 UALink 连接 72 块这种 GPU。智能内核生成使用大规模强化学习来生成高性能 CUDA 内核，直接攻击 Nvidia 的软件优势。

rss · Semianalysis · 7月25日 00:33

**背景**: Nvidia 的 CUDA 生态系统长期以来是一道主要壁垒，其专有库和工具将开发者锁定在 Nvidia 硬件上。AMD 的 ROCm 旨在提供开放的替代方案，但在性能和开发者采用方面一直落后。MI455X 和智能内核生成代表了 AMD 克服这些障碍的最新努力，结合新硬件与自动化软件优化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.phoronix.com/news/AMD-Instinct-MI455X-Helios">AMD Launches Instinct MI455X, Helios AI Rack - Phoronix</a></li>
<li><a href="https://arxiv.org/abs/2602.24286">[2602.24286] CUDA Agent: Large-Scale Agentic RL for High-Performance CUDA Kernel Generation</a></li>

</ul>
</details>

**标签**: `#AMD`, `#CUDA`, `#AI hardware`, `#software ecosystem`, `#GPU`

---

<a id="item-7"></a>
## [中国发布离岸信托个税新规](https://liaoning.chinatax.gov.cn/art/2026/7/24/art_5869_7823.html) ⭐️ 8.0/10

2026 年 7 月 24 日，财政部和国家税务总局联合发布规定，要求中国税务居民对转入离岸信托的财产及年度信托收益进行申报纳税，规定自发布之日起施行。 该规定通过穿透式征税原则堵塞避税漏洞，将未分配的信托收益视为每年应税所得，对高净值人群和财富规划产生重大影响。 全流程按增值额（现值减原值和费用）适用 20%固定税率，2023 至 2025 年期间需在 90 天内补缴申报，不加收滞纳金。

telegram · zaihuapd · 7月25日 00:31

**背景**: 离岸信托是依据境外法律设立持有资产的法律安排，常用于遗产规划和税收优化。此前信托内留存收益在分配前不征税，允许递延。中国现采用穿透式征税，每年直接对居民委托人（受益人）就信托所得征税。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.shui5.cn/article/c6/12399.html">shui5.cn/article/c6/12399.html</a></li>
<li><a href="https://www.bjnews.com.cn/detail/1784880489129754.html">bjnews.com.cn/detail/1784880489129754.html</a></li>
<li><a href="https://www.zenind.com/zh-CHS/help/post/pass-through-taxation-for-small-business-owners-how-it-works-and-which-entities-qualify">小企业主的穿透式征税：运作方式及适用实体类型</a></li>

</ul>
</details>

**标签**: `#tax regulation`, `#offshore trust`, `#China`, `#personal income tax`, `#wealth management`

---

<a id="item-8"></a>
## [市场监管总局对携程罚款 51.79 亿元](https://t.me/zaihuapd/42767) ⭐️ 8.0/10

7 月 25 日，国家市场监督管理总局因携程集团滥用市场支配地位，对其罚没共计 51.79 亿元，其中包括没收违法所得 16.58 亿元和罚款 35.21 亿元。 这是中国科技行业最大的反垄断处罚之一，表明监管机构对平台经济的审查趋严，并强化了维护公平竞争的决心。 监管还责令携程全额退还强制扣除酒店经营者的 1.22 亿元订单储备金，并要求全面整改并公开整改措施。

telegram · zaihuapd · 7月25日 11:56

**背景**: 中国反垄断法禁止具有市场支配地位的企业滥用其地位，例如通过不公平定价或排他性交易。携程作为中国领先的在线旅游平台，被指控强制酒店签订排他性协议并收取过高佣金。

**标签**: `#antitrust`, `#regulation`, `#tech industry`, `#China`

---

<a id="item-9"></a>
## [微软将用 TPM 芯片封堵盗版 Windows 激活](https://www.techspot.com/news/113232-microsoft-using-tpm-chips-crack-down-pirated-windows.html) ⭐️ 8.0/10

微软宣布为其密钥管理服务（KMS）新增基于 TPM 芯片的硬件安全验证机制，在允许批量激活 Windows 前先确认激活服务器的硬件身份是否经过微软认证且未被篡改，从而封堵盗版用户长期滥用的伪造 KMS 服务器。该功能将从下一版 Windows Server 起成为强制要求，并自 2026 年 8 月起在 Windows Server 2025 中推送准备提示。 此举标志着微软反盗版行动的重大升级，直指盗版群体多年来广泛利用的 KMS 激活漏洞。该措施可能使许多现有激活工具失效，但盗版社区随即推出 TSforge 等新破解方法，这场攻防战仍在继续。 这项新功能名为“KMS 硬件安全”（KMS Hardware-Secured），利用 TPM 证明机制确保激活服务器运行在可信硬件上。微软已于 2025 年封堵了 KMS38 漏洞，新的 TPM 验证旨在阻止需要定期连接伪造服务器的 Online KMS 工具（如 Massgrave 的工具）。

telegram · zaihuapd · 7月25日 15:55

**背景**: 密钥管理服务（KMS）是微软用于企业和批量激活 Windows 及 Office 的技术，允许组织通过本地服务器激活多台设备。盗版者长期滥用 KMS，运行伪造的激活服务器。可信平台模块（TPM）是一种安全硬件芯片，提供加密功能，包括验证系统完整性的证明能力。之前的 KMS38 漏洞可离线激活至 2038 年，而最新的 TSforge 方法号称能绕过整个软件保护平台（SPP）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techspot.com/news/113232-microsoft-using-tpm-chips-crack-down-pirated-windows.html">Microsoft is using TPM chips to crack down on pirated Windows ...</a></li>
<li><a href="https://petri.com/microsoft-secure-windows-kms-tpm-attestation/">Microsoft to Secure Windows KMS With TPM Attestation</a></li>
<li><a href="https://massgrave.dev/blog/tsforge">TSforge | MAS</a></li>

</ul>
</details>

**标签**: `#Windows`, `#security`, `#DRM`, `#anti-piracy`, `#TPM`

---