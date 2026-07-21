---
layout: default
title: "Horizon Summary: 2026-07-22 (ZH)"
date: 2026-07-22
lang: zh
---

> 从 29 条内容中筛选出 4 条重要资讯。

---

1. [苹果赢得 CSAM 责任案，法官批评判决](#item-1) ⭐️ 8.0/10
2. [炉边谈话揭示 Claude Code 团队内部实践](#item-2) ⭐️ 8.0/10
3. [谷歌被曝开发 Frozen v2 芯片提高 Gemini 效率](#item-3) ⭐️ 8.0/10
4. [谷歌推出具备智能体能力的 Gemini 3.5 Flash](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [苹果赢得 CSAM 责任案，法官批评判决](https://blog.ericgoldman.org/archives/2026/07/apple-defeats-liability-for-not-scanning-icloud-for-csam-but-the-judge-was-not-pleased-amy-v-apple.htm) ⭐️ 8.0/10

一名联邦法官裁定，苹果无需为未扫描 iCloud 中的儿童性虐待材料（CSAM）承担责任，同时称该结果“令人不安”，并指出儿童成为隐私保护的“附带损害”。 该裁决为科技公司无需主动扫描加密云数据中的 CSAM 树立了法律先例，可能影响未来立法以及用户隐私与儿童安全之间的持续辩论。 该案由一名儿童性虐待受害者提起，她认为苹果未扫描 iCloud 导致 CSAM 进一步传播。苹果此前曾尝试使用 NeuralHash 进行客户端扫描，但因隐私争议而放弃。

hackernews · speckx · 7月21日 14:31 · [社区讨论](https://news.ycombinator.com/item?id=48992870)

**背景**: 客户端扫描（CSS）在文件上传到云端之前在设备上检查文件，使用已知哈希数据库检测 CSAM。苹果提出的 NeuralHash 系统在设备上完成匹配而不向苹果透露内容，但批评者担心它可能被滥用于大规模监控。法律问题是公司是否有义务实施此类系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://apple.fandom.com/wiki/NeuralHash">NeuralHash | Apple Wiki | Fandom</a></li>
<li><a href="https://www.lawfaremedia.org/article/apple-client-side-scanning-system">The Apple Client-Side Scanning System | Lawfare</a></li>

</ul>
</details>

**社区讨论**: 评论者大多支持苹果的隐私立场，有人指出苹果与其他大型科技公司相比“处于另一个水平”。其他人则辩论 CSAM 扫描与预防实际虐待之间的权衡，一些人质疑闭源端到端加密系统的真正隐私性。法官的批评被视为一种不幸但必要的权衡。

**标签**: `#Apple`, `#CSAM`, `#Privacy`, `#Encryption`, `#Legal`

---

<a id="item-2"></a>
## [炉边谈话揭示 Claude Code 团队内部实践](https://simonwillison.net/2026/Jul/21/cat-and-thariq/#atom-everything) ⭐️ 8.0/10

在 AI 工程师世界博览会的炉边谈话中，Anthropic 的 Cat Wu 和 Thariq Shihipar 分享道，Claude Tag（一种协作式 Slack 集成）现已为 Claude Code 团队完成了 65%的产品工程 PR，并且 Claude Code 的系统提示已缩减 80%，因为对于 Fable 5 等模型而言，添加示例已不再是最佳实践。 这些见解揭示了前沿 AI 团队如何在内部利用自己的工具，为编码代理大幅减少人工监督并重塑开发工作流程提供了真实证据。 Claude Code 的关键更改仍需人工审查，但团队越来越依赖自动化代码审查来处理外层。Anthropic 的内部发布政策（称为“蚂蚁试吃”）要求功能在向公众发布前，需在员工中展示用户留存率。

rss · Simon Willison · 7月21日 12:54

**背景**: Claude Code 是一款基于 Anthropic 的 Claude 系列大语言模型的 AI 辅助软件开发工具。Claude Tag 是一种协作式 Slack 集成，允许团队在共享频道中与 Claude 协作。Fable 是 Anthropic 最新的高级模型，能够完成一次性功能实现和视频编辑等任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/introducing-claude-tag">Introducing Claude Tag \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI)</a></li>
<li><a href="https://support.claude.com/en/articles/15594475-what-is-claude-tag">What is Claude Tag? | Claude Help Center</a></li>

</ul>
</details>

**标签**: `#AI engineering`, `#Claude Code`, `#Anthropic`, `#developer tools`, `#AI assistants`

---

<a id="item-3"></a>
## [谷歌被曝开发 Frozen v2 芯片提高 Gemini 效率](https://www.quiverquant.com/news/Google+Reportedly+Developing+%E2%80%98Frozen+v2%E2%80%99+AI+Chip+to+Boost+Gemini+Efficiency) ⭐️ 8.0/10

据报道，谷歌正在开发一款内部代号为'Frozen v2'的 AI 服务器芯片，将 Gemini 模型的部分能力直接写入硬件，旨在将推理效率提升至当前 TPU 的 6 到 10 倍，计划于 2028 年部署。 该芯片可能大幅降低运行 Gemini 的推理成本和能耗，帮助谷歌缓解内部算力短缺并扩展云服务。这也标志着将 AI 能力直接嵌入芯片的模型专用硬件趋势。 Frozen v2 旨在补充而非取代谷歌的 TPU 产品线。该芯片将 Gemini 部分架构永久嵌入硅片中，减少了数据移动和计算开销。

telegram · zaihuapd · 7月21日 01:01

**背景**: AI 推理效率是一个关键挑战，运行大型模型需要大量电力和算力。将模型能力写入硬件可以减少冗余和能耗，但这种芯片是专用化的，开发周期长。谷歌的 TPU 系列一直是其主要 AI 加速器，而 Frozen v2 代表了向模型专用硬件的转变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/07/20/google-is-working-on-a-new-ai-chip-designed-to-make-gemini-more-efficient/">Google is working on a new AI chip designed to make Gemini more efficient | TechCrunch</a></li>
<li><a href="https://www.cnbc.com/2026/07/20/alphabet-googl-stock-ai-chip-report.html">Alphabet stock pops on report it's developing a more efficient AI chip</a></li>
<li><a href="https://qz.com/google-gemini-chip-frozen-tpu-efficiency-072026">Google developing Gemini-specific chip called Frozen v2</a></li>

</ul>
</details>

**标签**: `#AI chip`, `#Gemini`, `#hardware acceleration`, `#TPU`, `#inference efficiency`

---

<a id="item-4"></a>
## [谷歌推出具备智能体能力的 Gemini 3.5 Flash](https://t.me/zaihuapd/42699) ⭐️ 8.0/10

谷歌宣布推出 Gemini 3.5 Flash 模型，该模型具备智能体能力，输出速度比前代快 4 倍，且成本大幅降低。性能更强的 Gemini 3.5 Pro 预计于下个月推出。 此次发布标志着 AI 模型发展的重要一步，将高效率与智能体能力相结合，能够实现更自主的多步骤任务执行。降低的成本和提升的速度使先进 AI 对开发者和企业更加可及。 Gemini 3.5 Flash 支持文本、图像、视频、音频和 PDF 输入，并针对编程和并行智能体执行循环进行了优化。根据基准测试，它在企业工作评估集上比 Gemini 3 Flash 提升了 19.6%。

telegram · zaihuapd · 7月21日 15:23

**背景**: 智能体 AI 指的是能够在最少人工干预下设定目标、规划和执行任务的系统，模仿人类决策过程。Gemini 3.5 Flash 是一款多模态模型，旨在以较低成本提供接近 Pro 级别的推理能力，推动了每美元智能水平的边界。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3 . 5 Flash — Google DeepMind</a></li>
<li><a href="https://cloud.google.com/discover/what-is-agentic-ai">What is agentic AI? Definition and differentiators | Google Cloud</a></li>
<li><a href="https://openrouter.ai/google/gemini-3.5-flash">Gemini 3 . 5 Flash - API Pricing & Benchmarks | OpenRouter</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google`, `#Gemini`, `#LLM`, `#machine learning`

---