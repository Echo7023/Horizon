---
layout: default
title: "Horizon Summary: 2026-07-28 (ZH)"
date: 2026-07-28
lang: zh
---

> 从 29 条内容中筛选出 7 条重要资讯。

---

1. [月之暗面发布开源权重 3 万亿参数模型 Kimi-K3](#item-1) ⭐️ 9.0/10
2. [Fastjson 1.x 现无需 gadget 的严重 RCE 漏洞](#item-2) ⭐️ 9.0/10
3. [vLLM v0.26.0 发布，新增模型系列并优化 DeepSeek-V4 性能](#item-3) ⭐️ 8.0/10
4. [Bun 的 Rust 重写进展顺利，发布推迟](#item-4) ⭐️ 8.0/10
5. [中国 DRAM 制造商长鑫科技科创板上市首日暴涨 471%](#item-5) ⭐️ 8.0/10
6. [谷歌预告 Gemini 4：最雄心预训练，年底发布](#item-6) ⭐️ 8.0/10
7. [中芯国际测试中国首台国产 DUV 光刻机](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [月之暗面发布开源权重 3 万亿参数模型 Kimi-K3](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 9.0/10

月之暗面（Moonshot AI）在 HuggingFace 上发布了 3000 亿参数（3T 参数）的混合专家（MoE）模型 Kimi-K3，附带详细技术报告，采用开放权重许可。 此次发布为社区提供了研究并微调如此大规模模型的罕见机会，讨论焦点集中在服务 3T 模型的成本、定制潜力，以及要求大规模商业用户签署单独协议的许可条款。 该模型原生采用 mxfp4 精度，推理时需约 1.5 TB 显存，刚好达到 8×B200 配置的极限，实际吞吐量优化可能需要 16×B200。初始 API 定价为：未缓存输入$3.00/M token，缓存输入$0.30/M token，输出$15.00/M token。

hackernews · nateb2022 · 7月27日 06:18 · [社区讨论](https://news.ycombinator.com/item?id=49065752)

**背景**: Kimi-K3 是北京人工智能公司月之暗面（Moonshot AI）开发的混合专家（MoE）大型语言模型。其开放权重发布允许开发者下载、定制并微调模型用于特定场景，但许可条款要求：若被许可方及其关联方连续 12 个月合计营收超过 2000 万美元，则需与月之暗面另行签署商业协议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://kimi-ai.chat/models/kimi-k3/">Kimi K 3 : 1M Context, API Pricing & Limits</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反响热烈，主要讨论集中在服务 3T 模型的高昂成本（需约 1.5TB 显存）、开放权重带来的定制化与 IP 主权优势，以及针对大型商业实体的许可限制。有评论者还感叹缺乏具备足够显存的准专业级 GPU 来运行此类模型。

**标签**: `#AI`, `#Open Weights`, `#Large Language Model`, `#Kimi-K3`, `#HuggingFace`

---

<a id="item-2"></a>
## [Fastjson 1.x 现无需 gadget 的严重 RCE 漏洞](https://t.me/zaihuapd/42797) ⭐️ 9.0/10

安全研究员 Kirill Firsov 披露了 Fastjson 1.2.68 至 1.2.83 版本中存在严重远程代码执行漏洞，该漏洞无需 gadget 链或开启 autoTypeSupport，影响 JDK 8、17 和 21。 该漏洞尤其危险，因为它绕过了常见的缓解措施且影响多个 JDK 版本，而 Fastjson 1.x 已停止维护，无官方补丁。用户必须紧急升级到 Fastjson 2 或采取临时缓解措施。 该漏洞无需任何 classpath gadget 或开启 autoType 即可利用，使其更容易武器化。Fastjson 1.x 自 2024 年 10 月起已停止维护，因此唯一缓解措施是升级到 Fastjson 2 或按照研究人员的建议应用配置临时方案。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson 是阿里巴巴维护的 Java 常用 JSON 解析库，广泛用于企业应用。Java 反序列化中的 'gadget 链' 是指 classpath 上可用的一系列类，可以串联起来实现任意代码执行。'autoTypeSupport' 是 Fastjson 的一个特性，允许反序列化任意类，通常在安全配置中被禁用。这个漏洞的显著之处在于它不需要这两者，因此更严重且更易利用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://threatbook.io/blog/fastjson-rce-1.2.83-active-exploitation-detected-detection-mitigation">Fastjson RCE ( 1.2.83): Active Exploitation Detected — Detection...</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#fastjson`, `#java`, `#rce`

---

<a id="item-3"></a>
## [vLLM v0.26.0 发布，新增模型系列并优化 DeepSeek-V4 性能](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 引入了 Inkling 模型系列，提供了包括分段 CUDA 图和 NVFP4 量化在内的完整支持，并为 DeepSeek-V4 带来了显著性能优化，如专用路由内核和 fused_topk_bias。此版本还增加了 fp32 lm_head 支持、灵活的注意力后端以及成熟的 KV 卸载功能，共有 212 位贡献者提交了 411 个提交。 此版本增强了对 DeepSeek-V4 和新 Inkling 系列等前沿模型的支持，提升了 LLM 社区的推理效率和准确性。大量贡献者的参与反映了优化推理框架在生产级 AI 部署中日益增长的重要性。 Inkling 模型系列包括分段 CUDA 图支持、Hopper FA4 相对注意力、MTP=1 推测解码、LoRA 和标准 ModelOpt NVFP4 量化。DeepSeek-V4 优化通过专用路由内核实现了 2.94% 的端到端 TPOT 提升，fused_topk_bias 内核加速达 1.5–2 倍。fp32 lm_head 通过 head_dtype 提高了生成头的准确性，并扩展到了 LoRA 和 ROCm 路径。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个高吞吐量、内存高效的大语言模型推理引擎，广泛应用于生产环境。DeepSeek-V4 是一个支持 1M 上下文的混合专家模型，而 Inkling 系列利用 Hopper FA4 和 NVFP4 量化等先进技术来提升推理性能。此版本延续了 vLLM 支持多样化模型架构和硬件后端的持续努力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2603.05451v1">FlashAttention-4: Algorithm and Kernel Pipelining Co-Design for Asymmetric Hardware Scaling</a></li>
<li><a href="https://docs.vllm.ai/projects/vllm-omni/en/latest/user_guide/quantization/modelopt/">ModelOpt - vLLM-Omni</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#model optimization`, `#release`, `#deep learning`

---

<a id="item-4"></a>
## [Bun 的 Rust 重写进展顺利，发布推迟](https://lockwood.dev/ai/2026/07/27/how-is-the-bun-rewrite-in-rust-going.html) ⭐️ 8.0/10

Bun 从 Zig 到 Rust 的重写已在 Claude Code 中发布，但下一个版本 (1.4) 被推迟，直到达到新通过的 Node.js 兼容性测试的目标数量。 这一重写对 Bun 的性能和可维护性至关重要，其在 Claude Code 中的集成展示了实际部署。推迟表明优先考虑兼容性而非速度。 Rust 版本一个多月前已在 Claude Code 中发布。Bun v1.4 发布推迟，直到特定数量的新通过的 Node.js 测试达标，PR 已提交但尚未合并，预计下周二发布。

hackernews · tomlockwood · 7月27日 11:12 · [社区讨论](https://news.ycombinator.com/item?id=49067854)

**背景**: Bun 是一个快速的一体化 JavaScript 运行时，可打包、安装和运行 JavaScript 和 TypeScript。它最初用 Zig 编写，但宣布用 Rust 重写以利用 Rust 的生态系统和安全性。Claude Code 是 Anthropic 开发的 AI 编程工具，运行在终端中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bun.sh/">Bun — A fast all-in-one JavaScript runtime</a></li>
<li><a href="https://github.com/oven-sh/bun">GitHub - oven-sh/ bun : Incredibly fast JavaScript runtime , bundler...</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**社区讨论**: Jarred 确认了进展和延迟，强调兼容性。一些评论者指出重构后速度放缓是预期的，而另一些则质疑使用 LLM 翻译代码库，认为原来的 Zig 问题是可以修复的。

**标签**: `#Bun`, `#Rust`, `#rewrite`, `#JavaScript runtime`, `#software engineering`

---

<a id="item-5"></a>
## [中国 DRAM 制造商长鑫科技科创板上市首日暴涨 471%](https://www.stcn.com/article/detail/4042119.html) ⭐️ 8.0/10

长鑫科技（CXMT）于 7 月 27 日在科创板上市，开盘价 49.5 元/股，较发行价 8.66 元大幅上涨 471.59%。本次募集资金约 579 亿元，成为科创板史上最大 IPO。 作为国产 DRAM 龙头，长鑫科技的成功上市和巨额募资凸显资本市场对半导体国产替代的强力支持。此次 IPO 超越中芯国际此前纪录，表明存储芯片在中国科技生态系统中的重要性日益提升。 若超额配售选择权全额行使，预计募资总额约 666 亿元。公司预计 2026 年上半年归母净利润 500 至 570 亿元，同比大幅扭亏。

telegram · zaihuapd · 7月27日 01:29

**背景**: 长鑫科技是中国主要的 DRAM（动态随机存取存储器）生产商，产品广泛应用于电脑、智能手机和服务器。科创板是中国版的纳斯达克，面向科技企业。在中美科技紧张局势下，长鑫科技的 IPO 是国内存储行业的一个重要里程碑。

**标签**: `#半导体`, `#国产替代`, `#IPO`, `#存储芯片`, `#科创板`

---

<a id="item-6"></a>
## [谷歌预告 Gemini 4：最雄心预训练，年底发布](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

谷歌 CEO Sundar Pichai 在 Alphabet 2026 年第二季度财报会上宣布，下一代大模型 Gemini 4 正在训练中，这是该公司迄今最具雄心的预训练项目，目标于 2026 年底发布。 这显示谷歌致力于保持前沿 AI 领导地位，因为更大规模的预训练对提升能力至关重要。该模型的发布可能显著影响 AI 格局，在推理、编程和多模态任务等方面树立新标杆。 Pichai 强调谷歌将优先将算力分配给前沿 AGI 研发，以确保 Gemini 4 发布时仍处于最前沿。此外，Gemini 3.x Flash 系列将继续保持几乎每月一次的更新，重点提升智能编码等能力。

telegram · zaihuapd · 7月27日 04:06

**背景**: 预训练是大语言模型的第一阶段，模型在一个庞大的文本（通常还包括多模态数据）语料库上训练，通过预测下一个 token 来奠定其知识和能力基础。根据近期趋势，前沿模型通常在上万亿 tokens 上预训练，并包含多模态扩展，使得每次预训练都是一个巨大的工程和研究挑战。谷歌 Gemini 4 的预训练正是顺应这一趋势，旨在推动规模和性能的边界。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3 .6 Flash — Google DeepMind</a></li>
<li><a href="https://medium.com/@nursena_kok/pre-training-phase-of-large-language-models-the-foundation-of-modern-ai-111b377f0a33">Pre-training Phase of Large Language Models: The Foundation of Modern AI | by Nursena Kok | Medium</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google`, `#Gemini`, `#large language models`, `#pre-training`

---

<a id="item-7"></a>
## [中芯国际测试中国首台国产 DUV 光刻机](https://t.me/zaihuapd/42800) ⭐️ 8.0/10

中芯国际正在试运行中国首台由上海初创公司宇量昇研发的国产 DUV 光刻机，目标是生产 28 纳米芯片，并尝试通过多重图形化实现 7 纳米，预计 2027 年量产。 这一进展标志着中国半导体自给自足的关键一步，可能减少对荷兰 ASML 的依赖，并重塑全球芯片供应链。 该设备大部分零部件已国产化，但仍依赖部分进口。中芯国际还在探索通过多重图形化达到 7 纳米甚至 5 纳米，但良率可能较低。

telegram · zaihuapd · 7月27日 14:10

**背景**: DUV 光刻利用深紫外光（193nm 或 248nm）在硅片上印制电路图案。多重图形化是一种提升分辨率的技术，可超越单次曝光的极限，常用于 10 纳米和 7 纳米节点。目前，中国最先进的芯片仍依赖 ASML 的 DUV 设备，而 EUV 光刻机因美国出口管制被禁止对华销售。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multiple_patterning">Multiple patterning - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Extreme_ultraviolet_lithography">EUV lithography - Wikipedia</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#lithography`, `#China`, `#SMIC`, `#DUV`

---