---
layout: default
title: "Horizon Summary: 2026-07-17 (ZH)"
date: 2026-07-17
lang: zh
---

> 从 40 条内容中筛选出 13 条重要资讯。

---

1. [Kimi K3：拥有百万上下文和前沿性能的开源权重大语言模型](#item-1) ⭐️ 9.0/10
2. [从 Rust 重写到 Zig：安全性与性能的权衡](#item-2) ⭐️ 8.0/10
3. [索尼再次从用户'购买'的库中删除电影](#item-3) ⭐️ 8.0/10
4. [GPT-5.6 Codex 漏洞可删除 $HOME 目录](#item-4) ⭐️ 8.0/10
5. [思考机器实验室发布 Inkling 开源权重 MoE 模型](#item-5) ⭐️ 8.0/10
6. [Linus Torvalds 声明 Linux 不反 AI](#item-6) ⭐️ 8.0/10
7. [xAI 在隐私争议后开源 Grok Build](#item-7) ⭐️ 8.0/10
8. [ExTernD：扩展秩三元分解实现 LLM 量化](#item-8) ⭐️ 8.0/10
9. [PnP-CoSMo：无需原始 K 空间数据的即插即用多对比度 MRI 重建](#item-9) ⭐️ 8.0/10
10. [xAI 起诉 Grok 用户生成儿童性虐待深度伪造](#item-10) ⭐️ 8.0/10
11. [长鑫存储将在 2026 年追上美光 DRAM 产能](#item-11) ⭐️ 8.0/10
12. [日本购入 2.75 万块英伟达 Rubin 芯片打造自主机器人 AI](#item-12) ⭐️ 8.0/10
13. [台积电再投千亿美元赴美，Q2 利润飙升 77%](#item-13) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Kimi K3：拥有百万上下文和前沿性能的开源权重大语言模型](https://www.kimi.com/en) ⭐️ 9.0/10

Moonshot AI 发布了 Kimi K3，这是一款新的开源权重大语言模型，拥有 100 万 token 的上下文窗口，定价为每百万 token 3/15 美元（缓存为 0.3 美元），并声称其性能仅次于 Claude Fable 5 和 GPT-5.6 Sol，达到前沿水平。完整模型权重将于 2026 年 7 月 27 日发布，同时附带技术报告。 如果得到验证，Kimi K3 将成为开源权重大语言模型的一个重要里程碑，以前沿性能和有竞争力的价格提供对先进 AI 能力的广泛访问。其百万级的上下文窗口和原生视觉支持使其适用于复杂的长期任务，对 Anthropic 的 Sonnet 系列等专有模型构成挑战。 Kimi K3 是一个 2.5 万亿参数的混合专家（MoE）模型，其定价与 Anthropic 的 Sonnet 系列（1:1）相匹配，但对于中国开源权重模型来说价格较高。该模型默认启用最大思考努力，未来计划推出低/高努力模式；早期的 Kimi K3 配置显示，在 Allegretto 及更高等级的套餐上支持高达 100 万 token 的上下文。

hackernews · vincent_s · 7月16日 14:46 · [社区讨论](https://news.ycombinator.com/item?id=48935342)

**背景**: 开源权重大语言模型将其预训练参数公开，允许他人使用、修改或在此基础上构建。这与 GPT-4 等仅通过 API 访问的专有模型形成对比。大语言模型的前沿领域一直由闭源模型主导，但近期 Llama 和 Qwen 等开源权重发布缩小了差距；Kimi K3 旨在进一步推动这一进展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/open-weights-llms-in-depth-analysis-adoption-usage-performance-jha-kymhc">Open - Weights LLMs: In-Depth Analysis of Adoption, Usage, and...</a></li>
<li><a href="https://kie.ai/blog/what-is-kimi-k3">What Is Kimi K3? Moonshot's 2.5T, 1M-Context Flagship</a></li>
<li><a href="https://kimi-k2.org/kimi-k3-status">Kimi K3 Status - Release Date, Official Updates and 2026 News</a></li>

</ul>
</details>

**社区讨论**: 社区评论显示出很高的参与度，用户指出该模型对于中国开源权重模型来说定价极高，但如果性能确实能与 Sonnet 等前沿模型媲美，则价格合理。一些用户测试了该模型并报告了高成本，而另一些用户则强调了即将发布的权重和技术报告，表达了谨慎乐观的态度。

**标签**: `#AI`, `#large language models`, `#open-source`, `#context window`, `#benchmarks`

---

<a id="item-2"></a>
## [从 Rust 重写到 Zig：安全性与性能的权衡](https://rtfeldman.com/rust-to-zig) ⭐️ 8.0/10

Richard Feldman 详细介绍了将 Roc 编译器从 Rust 重写为 Zig 的决定，理由包括更好的增量编译和对内存的更多控制，同时承认内存安全性方面的权衡。 这一实验突显了系统编程中安全性（Rust）与底层控制（Zig）之间的实际冲突，将影响未来在编译器这类性能关键工具中语言的选择。 重写对象是 Roc 编译器；Zig 提供更快的增量编译和精确的内存控制，但缺乏 Rust 的编译时安全保证，而是依赖 ReleaseSafe 模式下的运行时检查。

hackernews · jorangreef · 7月16日 11:39 · [社区讨论](https://news.ycombinator.com/item?id=48933149)

**背景**: Rust 是一种系统语言，通过其所有权模型在不使用垃圾回收的情况下实现内存安全，但某些任务如二进制补丁需要不安全代码。Zig 是一种较新的语言，优先考虑简单性和手动内存管理，在调试模式下提供运行时安全检查，但在发布构建中则将安全性交由程序员负责。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>
<li><a href="https://doc.rust-lang.org/nomicon/meet-safe-and-unsafe.html">Meet Safe and Unsafe - The Rustonomicon</a></li>
<li><a href="https://ziglang.org/">Home ⚡ Zig Programming Language</a></li>

</ul>
</details>

**社区讨论**: 评论中，steveklabnik 质疑编译器经常需要不安全代码的说法，landr0id 对 Zig 检测释放后使用的功能表示怀疑，arthurbrown 想知道为什么没有选择 OCaml，而 onlyrealcuzzo 称赞了 Zig 的增量编译，但希望 Rust 也能添加类似功能。

**标签**: `#zig`, `#rust`, `#compilers`, `#systems-programming`, `#memory-safety`

---

<a id="item-3"></a>
## [索尼再次从用户'购买'的库中删除电影](https://www.techdirt.com/2026/07/15/sony-deletes-a-bunch-more-movies-from-the-accounts-of-people-who-bought-them/) ⭐️ 8.0/10

索尼再次从用户的 PlayStation Store 库中删除了多部电影，而这些影片是客户之前花钱购买的，这再次引发了关于数字所有权的争议。这是该公司在用户购买后撤销访问权限的又一例证。 这种持续的做法削弱了数字所有权的概念，凸显了针对数字购买制定更强消费者保护法律的必要性。它影响了数百万 PlayStation 用户，并侵蚀了对数字商店的信任。 删除操作通过数字版权管理（DRM）技术实现，该技术赋予发行商在销售后对内容的持续控制权。用户实际上并不拥有数字媒体，而是持有一个可撤销的许可证。

hackernews · nekusar · 7月16日 12:13 · [社区讨论](https://news.ycombinator.com/item?id=48933419)

**背景**: 数字版权管理（DRM）结合了加密、许可和设备认证，用于控制内容的访问和共享方式。当用户'购买'数字电影时，他们实际上购买的是有限许可证，而非内容本身。这使得像索尼这样的公司可以在许可协议变更或其他商业原因下撤销访问权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_rights_management">Digital rights management - Wikipedia</a></li>
<li><a href="https://www.fortinet.com/resources/cyberglossary/digital-rights-management-drm">What Is DRM? Digital Rights Management Explained | Fortinet</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了沮丧，有人呼吁对误导性的'购买'按钮采取法律行动。其他人指出这是一个反复出现的问题，并主张使用离线物理媒体或盗版作为替代方案。少数用户推测，随着玩家转向 PC，主机时代可能即将结束。

**标签**: `#digital rights`, `#consumer protection`, `#Sony`, `#digital media`, `#ownership`

---

<a id="item-4"></a>
## [GPT-5.6 Codex 漏洞可删除 $HOME 目录](https://simonwillison.net/2026/Jul/16/bad-codex-bug/#atom-everything) ⭐️ 8.0/10

根据 Thibault Sottiaux 在 2026 年 7 月 16 日的确认，当启用完整访问模式且未开启沙盒保护或自动审查时，GPT-5.6 Codex 的一个漏洞可能意外删除用户的 $HOME 目录。 此漏洞凸显了 AI 编程代理中的关键安全风险，可能导致信任这些工具并授予完全系统访问权限的开发者遭受不可逆的数据丢失。这凸显了在 AI 辅助开发中需要强大的沙盒和审查机制。 该漏洞发生在启用完整访问模式且 Codex 在没有沙盒或自动审查的情况下运行时；模型尝试覆盖 $HOME 环境变量以定义临时目录，但错误地删除了 $HOME 本身。

rss · Simon Willison · 7月16日 17:45

**背景**: 像 Codex 这样的 AI 编程代理通常需要文件系统访问权限来编写代码和管理文件。沙盒技术将代理的环境与主机系统隔离以防止损害，而完整访问模式则授予不受限的权限。没有这些保护措施，模型错误可能导致破坏性操作，如删除关键目录。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.explainx.ai/blog/openai-codex-gpt-5-6-home-deletion-full-access-july-2026">Codex GPT-5.6 $HOME Deletion — Full Access | explainx.ai Blog</a></li>
<li><a href="https://www.bunnyshell.com/guides/sandboxed-environments-ai-coding/">Sandboxed Environments for AI Coding: The Complete Guide | Bunnyshell</a></li>

</ul>
</details>

**标签**: `#codex`, `#gpt-5`, `#ai-safety`, `#coding-agents`, `#generative-ai`

---

<a id="item-5"></a>
## [思考机器实验室发布 Inkling 开源权重 MoE 模型](https://simonwillison.net/2026/Jul/16/inkling/#atom-everything) ⭐️ 8.0/10

由前 OpenAI CTO Mira Murati 领导的思考机器实验室发布了 Inkling，这是一个开源权重的混合专家多模态模型，总参数量 975B（活跃参数 41B），采用 Apache 2.0 许可证。 此次发布为开源权重生态系统增添了一名强劲的美国竞争者，为中国开源模型和 NVIDIA 的 Nemotron 提供了替代方案。其 Apache 2.0 许可证以及对通过 Tinker 平台进行微调的专注使其适合定制化。 Inkling 并非前沿模型，而是一个用于微调的强大基础模型，在 45 万亿文本、图像、音频和视频标记上训练。更小的 Inkling-Small（总参数量 276B，活跃参数 12B）已承诺但尚未发布。

rss · Simon Willison · 7月16日 15:35

**背景**: 混合专家（MoE）是一种架构，使用多个专门的子模型（“专家”）和一个门控网络，每个输入仅激活相关专家，从而提高效率。开源权重模型公开发布训练后的参数，允许下载、研究和修改，但不包括完整的训练代码或数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**标签**: `#open-weights`, `#multimodal`, `#Mixture-of-Experts`, `#AI model release`

---

<a id="item-6"></a>
## [Linus Torvalds 声明 Linux 不反 AI](https://simonwillison.net/2026/Jul/16/linus-torvalds/#atom-everything) ⭐️ 8.0/10

Linux 创始人兼顶级维护者 Linus Torvalds 在 Linux Media 邮件列表中声明，Linux 不是一个反 AI 项目，AI 是一个明确有用的工具，挑战了社区内的任何反对意见。 Linux 领导者的这一高调背书标志着 AI 在内核开发中得到了官方认可，可能影响行业实践，并鼓励在开源项目中更广泛地采用 AI 工具。 Torvalds 承认 AI 的用处一年前尚有疑问，但如今已毋庸置疑，不过他指出其经济影响等问题仍未解决。

rss · Simon Willison · 7月16日 13:26

**背景**: Linus Torvalds 是 Linux 内核的创建者和主要维护者，Linux 内核是全球最大的开源项目之一。他的声明在开发者社区中具有重要影响力。关于 AI 在软件开发中的角色的争论日益激烈，一些项目采取了严格的反 AI 政策。

**标签**: `#Linux`, `#AI`, `#Kernel Development`, `#Linus Torvalds`

---

<a id="item-7"></a>
## [xAI 在隐私争议后开源 Grok Build](https://simonwillison.net/2026/Jul/15/grok-build/#atom-everything) ⭐️ 8.0/10

在发生 grok CLI 工具将整个目录上传至 xAI 服务器的严重隐私事件后，xAI 已将整个 Grok Build 代码库以 Apache 2.0 许可证开源。该公司还禁用了默认数据保留，并删除了所有先前保留的编码数据。 此举旨在通过提供工具运行方式的完全透明来恢复用户信任，允许用户审计或本地运行。它为 AI 编码工具在处理数据时更加开放树立了先例。 该代码库包含 844,530 行 Rust 代码（仅约 3% 为第三方），并以单个提交发布，没有提交历史。值得注意的组件包括终端中的 Mermaid 图表渲染器，以及模仿其他编码代理（如 Codex 和 OpenCode）的工具实现。

rss · Simon Willison · 7月15日 23:59

**背景**: grok CLI 是 xAI 开发的一个基于终端的 AI 编码代理，可以编辑文件、运行命令和管理任务。此前，用户发现运行 CLI 时会将该目录完整上传至 xAI 的 Google Cloud 存储桶，引发隐私抗议。作为回应，xAI 禁用了上传功能，删除了已保留的数据，并将代码开源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/xai-org/grok-build">GitHub - xai-org/grok-build: SpaceXAI's coding agent harness ...</a></li>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://github.com/Norlem/grok-cli">GitHub - Norlem/ grok - cli : A terminal UI for xAI 's Grok models...</a></li>

</ul>
</details>

**社区讨论**: 社区最初的情绪非常负面，用户报告上传了 SSH 密钥和密码管理器等敏感数据。开源发布后，反应不一——有些人赞赏这种透明度，而另一些人则对过去的数据处理持怀疑态度。

**标签**: `#open source`, `#security`, `#AI`, `#xAI`, `#privacy`

---

<a id="item-8"></a>
## [ExTernD：扩展秩三元分解实现 LLM 量化](https://www.reddit.com/r/MachineLearning/comments/1uy2zb3/externd_expandedrank_ternary_decomposition/) ⭐️ 8.0/10

一种名为 ExTernD 的新后训练量化方法将 LLM 权重矩阵分解为两个三元矩阵和一个对角缩放矩阵，通过扩展内部秩实现任意精度。 该技术弥补了低位三元量化与高位方法之间的精度差距，使得 LLM 部署在几乎不损失模型质量且仅略微增加显存占用的情况下更加高效。 ExTernD 将每个权重矩阵分解为 A ≈ D1 * T1 * D2 * T2，其中 T1 和 T2 为三元矩阵，D1 和 D2 为对角缩放矩阵，从而在存储与计算之间提供连续可控的权衡。

reddit · r/MachineLearning · /u/LMTLS5 · 7月16日 13:31

**背景**: 大型语言模型通常通过量化来降低存储和计算成本。三元量化将权重限制在{-1, 0, +1}范围内，效率极高但常导致显著的精度损失。后训练量化（PTQ）在训练后直接应用量化，无需重新训练。固定秩的三元分解因无法准确表示全精度矩阵而陷入瓶颈；ExTernD 通过扩展分解秩克服了这一局限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2607.13511v1">ExTernD: Expanded-Rank Ternary Decomposition Ternary LLM PTQ ...</a></li>
<li><a href="https://papers.cool/arxiv/2607.13511">ExTernD: Expanded-Rank Ternary Decomposition Ternary LLM PTQ ...</a></li>
<li><a href="https://aipapers.ai/paper/26889608">ExTernD: Expanded-Rank Ternary Decomposition Ternary LLM PTQ ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#quantization`, `#ternary decomposition`, `#post-training quantization`, `#model efficiency`

---

<a id="item-9"></a>
## [PnP-CoSMo：无需原始 K 空间数据的即插即用多对比度 MRI 重建](https://www.reddit.com/r/MachineLearning/comments/1uy2h66/pnpcosmo_a_multicontrast_mri_reconstruction/) ⭐️ 8.0/10

研究人员提出了 PnP-CoSMo，一种用于多对比度 MRI 重建的即插即用框架，它从纯图像域数据中学习内容/风格模型，并将其作为先验应用于迭代重建，无需原始 K 空间训练数据。 该框架通过消除对难以获取的原始 K 空间数据的需求，解决了基于机器学习的 MRI 重建中的一个主要数据瓶颈。它还能泛化到不同的 MR 对比度和前向算子，有望在临床中实现更灵活、更易获取的重建。 PnP-CoSMo 包含两个阶段：首先，它从图像域数据中学习内容/风格模型；然后，冻结该模型并将其作为即插即用先验用于迭代重建算法。该方法在公共 NYU fastMRI DICOM 数据集上得到验证，与端到端方法相比质量相当或更优。

reddit · r/MachineLearning · /u/void_gear · 7月16日 13:10

**背景**: 多对比度 MRI 通过不同的对比机制（如 T1 加权、T2 加权）获取图像，以突出不同组织特性。用于 MRI 重建的机器学习方法通常需要原始 K 空间数据，但这并不总是可得。即插即用先验将去噪器与迭代重建相结合，但通常需要为每种对比度单独训练。内容/风格建模将图像分离为共享的内容（解剖结构）和对比度特定的风格，从而实现跨对比度学习。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sciencedirect.com/science/article/pii/S136184152600229X">A plug-and-play method for guided multi-contrast MRI ...</a></li>
<li><a href="https://arxiv.org/html/2409.13477v3">A Plug-and-Play Method for Guided Multi-contrast MRI ...</a></li>
<li><a href="https://github.com/cnmy-ro/pnp-cosmo">GitHub - cnmy-ro/pnp-cosmo: PnP-CoSMo algorithm for multi ...</a></li>

</ul>
</details>

**标签**: `#MRI reconstruction`, `#machine learning`, `#medical imaging`, `#plug-and-play`, `#content/style model`

---

<a id="item-10"></a>
## [xAI 起诉 Grok 用户生成儿童性虐待深度伪造](https://www.reuters.com/legal/litigation/musks-xai-sues-grok-user-over-sexualized-deepfakes-2026-07-15/) ⭐️ 8.0/10

马斯克的 xAI 公司起诉南卡罗来纳州男子 Terry Harwood，指控其利用 Grok 聊天机器人生成儿童性虐待材料和非自愿成人深度伪造，违反了服务条款。 这是首批 AI 公司因用户生成非法深度伪造内容而起诉用户的案件之一，为 AI 平台责任树立了先例，并凸显了 AI 治理中关键的伦理与法律问题。 xAI 要求法院永久禁止 Harwood 使用 Grok，并索赔。该公司称，2026 年已暂停 52,222 个账户，向国家失踪与受虐儿童中心举报 73,604 次，促成至少 244 人被捕。

telegram · zaihuapd · 7月16日 01:45

**背景**: Grok 是 xAI 开发的生成式 AI 聊天机器人，于 2023 年 11 月推出。深度伪造是利用 AI 创建的合成媒体，常被用于在虚假场景中描绘真实人物。这起诉讼针对的是滥用 AI 工具生成非法内容的行为，这是 AI 行业日益严重的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_(chatbot)">Grok ( chatbot ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Deepfake">Deepfake - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI ethics`, `#legal`, `#Grok`, `#deepfake`, `#child safety`

---

<a id="item-11"></a>
## [长鑫存储将在 2026 年追上美光 DRAM 产能](https://www.tomshardware.com/pc-components/dram/cxmt-close-to-matching-microns-memory-capacity-in-2026-research-claims-would-put-china-on-track-to-become-worlds-second-largest-dram-producer) ⭐️ 8.0/10

据 Citrini Research 预测，中国 DRAM 制造商长鑫存储将在 2026 年底达到每月 35 万片晶圆的产能，逼近美光的每月 37.5 万片。 这一扩张可能使中国成为全球第二大 DRAM 生产国，挑战三星和 SK 海力士的主导地位，并可能在地缘政治紧张局势下重塑全球内存供应链。 包括昇维旭、晋华集成等在内的中国企业总 DRAM 产能可能超过每月 60 万片，但美国 MATCH 法案可能限制对华出口用于扩大生产的关键浸没式 DUV 光刻设备。

telegram · zaihuapd · 7月16日 02:30

**背景**: DRAM 是一种广泛应用于计算机和服务器的易失性存储器。先进的浸没式 DUV 光刻技术通过在镜头和晶圆之间使用水来改善分辨率，对于制造高密度 DRAM 至关重要。美国 2026 年的 MATCH 法案旨在限制此类半导体制造设备对华出口，以遏制其技术发展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography - Wikipedia</a></li>
<li><a href="https://informedclearly.com/en/trade-war/52262/match-act-chip-export-controls-us-china-2026">MATCH Act: 2026's Toughest Chip Export Controls Reshape US ...</a></li>
<li><a href="https://www.govtrack.us/congress/bills/119/hr8170">H.R. 8170: MATCH Act - GovTrack.us</a></li>

</ul>
</details>

**标签**: `#DRAM`, `#semiconductor`, `#China`, `#memory`, `#supply chain`

---

<a id="item-12"></a>
## [日本购入 2.75 万块英伟达 Rubin 芯片打造自主机器人 AI](https://www.bloomberg.com/news/articles/2026-07-16/japan-to-buy-nvidia-rubin-chips-to-build-sovereign-ai-for-robots) ⭐️ 8.0/10

日本计划由新成立的 Noetra 公司牵头，购入 27,500 块英伟达下一代 Rubin 芯片，建设大型数据中心并开发面向机器人的本土基础 AI 模型，项目获得政府 3873 亿日元（约 24 亿美元）拨款。 这是一项由政府支持的主权 AI 基础设施重大投资，旨在减少对美中技术的依赖，并力争到 2040 年占据全球机器人市场 30%以上的份额，标志着日本在 AI 自主性和竞争力方面的战略推进。 该项目涉及软银、丰田支持的 Preferred Networks 以及 NEC 等企业。Noetra 总裁田场广信计划在 2027 年 3 月前发布首个 AI 模型，并在数年内推出机器人专用版本。

telegram · zaihuapd · 7月16日 10:59

**背景**: 主权 AI 是指国家利用本地基础设施、数据和模型，独立开发、部署和管理人工智能，以减少对外国供应商的依赖。英伟达 Rubin 是继 Blackwell 之后的下一代 AI 芯片架构，在 2026 年 CES 上发布，计算性能和效率大幅提升。日本的这一举措反映了全球各国寻求构建自主 AI 能力的趋势，特别是在机器人等关键领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sovereign_AI">Sovereign AI</a></li>
<li><a href="https://www.mckinsey.com/featured-insights/mckinsey-explainers/what-is-sovereign-ai">What is sovereign AI? | McKinsey</a></li>
<li><a href="https://www.linkedin.com/posts/theodoreaggelopoulos_nvidia-launches-powerful-new-rubin-chip-architecture-activity-7414286177656119296-o6T0">Nvidia launches powerful new Rubin chip architecture | TechCrunch</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#Nvidia`, `#robotics`, `#sovereign AI`, `#Japan`

---

<a id="item-13"></a>
## [台积电再投千亿美元赴美，Q2 利润飙升 77%](https://www.reuters.com/world/asia-pacific/tsmcs-second-quarter-profit-seen-hitting-record-ai-boom-2026-07-15/) ⭐️ 8.0/10

台积电宣布再向美国亚利桑那州投资 1000 亿美元，并公布第二季度净利润达 7066 亿新台币，同比增长 77%，创历史新高，远超市场预期。 此次扩产强化了台积电在 AI 需求旺盛之际对美国芯片制造的承诺，可能重塑全球半导体供应链，并减少对台湾的依赖。 新增的 1000 亿美元是在此前已宣布的 1650 亿美元之上，使台积电在美总投资规划达到 2650 亿美元，亚利桑那州已有 8 座工厂在建或规划中。

telegram · zaihuapd · 7月16日 12:29

**背景**: 台积电是全球最大的专业半导体代工厂，为苹果、英伟达、AMD 等公司生产芯片。美国政府正通过《芯片法案》推动先进芯片制造回流本土，以保障供应链安全。

**标签**: `#semiconductors`, `#AI`, `#manufacturing`, `#TSMC`, `#business`

---