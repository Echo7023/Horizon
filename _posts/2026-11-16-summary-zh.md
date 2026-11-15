---
layout: default
title: "Horizon Summary: 2026-11-16 (ZH)"
date: 2026-11-16
lang: zh
---

> 从 31 条内容中筛选出 18 条重要资讯。

---

1. [Meta FAIR 与 NYU：视觉编码器预训练可选，但视觉专属参数不可省](#item-1) ⭐️ 8.0/10
2. [开源工具让 B300 GPU 上的 pageable cudaMemcpy 提速约 5 倍](#item-2) ⭐️ 8.0/10
3. [多人游戏用每位玩家 GPU 上的本地世界模型生成各自画面](#item-3) ⭐️ 8.0/10
4. [MacBook Pro 的 OLED PWM 频闪引发可用性担忧](#item-4) ⭐️ 7.0/10
5. [微软 365 服务中断致酒店 15 名客人氯气中毒](#item-5) ⭐️ 7.0/10
6. [Sebastian Raschka 详解现代 LLM 的位置嵌入，引发群论层面的讨论](#item-6) ⭐️ 7.0/10
7. [博主主张所有 AI 生成的代码都应开源](#item-7) ⭐️ 7.0/10
8. [报道称卢特尼克推动放宽与其家族企业相关的芯片出口规则](#item-8) ⭐️ 7.0/10
9. [免训练早退：改输出层单行权重](#item-9) ⭐️ 7.0/10
10. [FAA 全国停飞起因查明：换铜线升级后路由器故障](#item-10) ⭐️ 7.0/10
11. [Telegram 小组件被指存在沙箱逃逸与远程代码执行漏洞](#item-11) ⭐️ 7.0/10
12. [研究称六款中国 AI 模型权重中留有 Blackwell 芯片指纹](#item-12) ⭐️ 7.0/10
13. [华为云 MaaS 平台正式上线开源盘古模型 openPangu-2.1-Pro](#item-13) ⭐️ 7.0/10
14. [回顾：Turbo Pascal 的极小体积与现代软件膨胀之对比](#item-14) ⭐️ 6.0/10
15. [博主用 Emacs 的 eww 取代传统浏览器，引发 Hacker News 热议](#item-15) ⭐️ 6.0/10
16. [Marimba：基于冻结版 Qwen3-ASR 构建的开源权重“System One”语音模型](#item-16) ⭐️ 6.0/10
17. [特斯拉宣布年底前开卖双座 Cybercab，首批优先供给自家车队](#item-17) ⭐️ 6.0/10
18. [美法官驳回美光、三星、SK 海力士撤销 DRAM 价格操纵诉讼的动议](#item-18) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Meta FAIR 与 NYU：视觉编码器预训练可选，但视觉专属参数不可省](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR 与 NYU 的研究者完全从零训练了 200 多个多模态大模型（连语言主干也从头训练），使用相同数据，并把编码器预训练所耗的算力计入同一份“生命周期总算力”预算，从而把标准视觉编码器通常捆绑在一起的三个设计选择拆开：是否单独预训练、是否使用视觉专属参数、以及是否把视觉容量放在 LLM 之前。结论是：单独的编码器预训练是可选的（在算力对齐的情况下，预训练编码器最多只能与从零训练的编码器打平），视觉专属参数在 0.6B 到 6.4B 的各个规模上都必不可少，而“置于 LLM 之前”这一位置选择也是可选的——一种“in-fusion”方案把零初始化的视觉专属权重注入 LLM 的前 8 层，效果与前置编码器相当，同时首 token 时延降低约 13%。 这是一项大规模、控制严格的消融研究，直接挑战了一个广泛接受的假设——多模态大模型必须配一个单独预训练好的视觉编码器（如 CLIP 或 SigLIP）。而当前已发布模型的做法分歧明显：Gemma 4 12B 去掉了编码器，Kimi K3 从零训练自己的编码器，Inkling 2 Small 又把编码器加了回来。由于已发布模型在数据、架构和算力上都不同，横向比较无法隔离其中任何一个变量，因此这项拆解研究为多模态大模型的设计者给出了明确答案：视觉专属容量要保留，但编码器预训练这笔预算可以省下，并且可以把视觉融合搬到主干网络内部。 主要对比实验使用 Qwen3-1.7B 与 4B 配置、0.4B 参数的视觉容量，并搭建了从 0.6B 到 6.4B 主干的规模阶梯，评测覆盖 Cambrian 的 16 个 448 像素 VQA 基准和 12 个语言基准。无编码器模型在所有规模上都落后，需要约 3 倍算力才能追上；而把编码器的参数让给 LLM 只会提升文本能力、并不提升 VQA。值得注意的是，把 MetaCLIP 预训练延长到 6.5 倍可将 ImageNet 线性探测准确率从 80.4% 提升到 84.4%，却对 VQA 毫无帮助；在 1.7B 规模下，位于第 1–8 层的 in-fusion 视觉专属分支达到 45.0 VQA，前置编码器为 44.4，文本共享这些参数时降至 42.3，而放在最后 8 层仅为 35.1。

reddit · r/MachineLearning · /u/trungh98 · 11月15日 17:38

**背景**: 大多数多模态大模型（MLLM）遵循这样一套范式：由一个视觉编码器（通常是 CLIP 或 SigLIP 风格、在数亿图文对上预训练过的模型）把图像转成 token，再由语言模型与文本一起读取。由于几乎所有强力的多模态大模型都使用这样的编码器，人们普遍认为正是这段上游视觉预训练赋予了模型视觉能力；同时编码器的参数通常单独训练、独占一个模块，并放在 LLM 之前。问题在于这三个属性总是捆绑出现，因此仅比较已发布模型无法判断究竟是预训练、专属参数还是位置安排在起作用。这篇论文把它们“解绑”：把编码器预训练所耗算力计入与多模态训练相同的总生命周期预算，于是预训练编码器必须证明自己多花的那部分算力是值得的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.17334">[2611.17334] Unbundling Multimodal Vision Encoding - arXiv.org</a></li>
<li><a href="https://huggingface.co/papers/2611.17334">Paper page - Unbundling Multimodal Vision Encoding</a></li>
<li><a href="https://magazine.sebastianraschka.com/p/understanding-multimodal-llms">Understanding Multimodal LLMs - by Sebastian Raschka, PhD</a></li>

</ul>
</details>

**标签**: `#multimodal-llm`, `#vision-encoder`, `#pretraining`, `#model-architecture`, `#scaling-experiments`

---

<a id="item-2"></a>
## [开源工具让 B300 GPU 上的 pageable cudaMemcpy 提速约 5 倍](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 8.0/10

一位开发者发布了 cudamemcpy-tuner 工具，通过 `cmt tune` 包装命令，把在 NVIDIA B300 上拷贝 1 GB uint8 PyTorch 张量时的 pageable CPU→GPU 带宽从 10.2 GB/s 提升到 51.5 GB/s，约 5 倍加速。该项目同时提供了基准测试脚本、讲解原理的技术博客以及 GitHub 上的开源代码。 主机到设备的数据传输往往是 GPU 工作流中最慢的一环，因此一个即插即用、能把 pageable 拷贝带宽成倍提升的调优工具，可以让所有使用默认（非固定）张量的用户在不改写模型代码的情况下加速数据加载与预处理。如果这种提升在其他 GPU 和负载上同样成立，可能会动摇长期以来“必须手动管理固定内存才能获得良好传输吞吐”的开发建议。 所公布的数据来自一个简单的微基准测试：把 1 GB 张量拷贝到 GPU 再拷回，取 5 次迭代的平均值，因此实际收益会取决于传输大小、主机内存布局以及 PCIe 代际。该工具以命令包装器的形式使用（`cmt tune -- python bench.py`），即透明地调优拷贝路径而无需修改代码，但目前公布的结果仅覆盖 B300（Blackwell Ultra）平台。

reddit · r/MachineLearning · /u/makneeee · 11月15日 18:20

**背景**: NumPy 或 PyTorch 等程序默认分配的主机内存是“可分页（pageable）”的，操作系统可以将其换出或搬移，因此 GPU 无法直接从其中做 DMA 传输。当对 pageable 内存调用 cudaMemcpy 时，CUDA 驱动必须先把数据复制到一个临时的页锁定（“固定/pinned”）暂存缓冲区，再传输到设备，这多出来的一次主机到主机拷贝会显著压低有效带宽。固定内存可以省去这一步，通常是被推荐的解决方案，但它分配开销大、还会减少操作系统可用内存——正因如此，一个能缩小普通 pageable 缓冲区差距的工具才值得关注。B300 是 NVIDIA 于 2025 年 3 月 GTC 上发布的 Blackwell Ultra 数据中心 GPU，配备 288 GB HBM3e，其主机互连速度极快，拷贝开销也因此更容易暴露出来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/how-optimize-data-transfers-cuda-cc/">How to Optimize Data Transfers in CUDA C/C++ | NVIDIA ... What is the difference between pinned memory and pageable ... Pinned vs. Pageable Memory | drkennetz/cuda_examples | DeepWiki Pinned and Pageable memory - CUDA Programming and Performance ... cuda_examples/MemoryAndStructureExamples/pinned_vs_pageable ... CUDA Pinned vs Pageable Memory: Faster Host-to-Device Transfers</a></li>
<li><a href="https://stackoverflow.com/questions/50184146/cuda-pinned-memory-vs-pageable-memory-tradeoffs">optimization - CUDA - Pinned Memory vs. Pageable Memory ... Code sample</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/dgx-b300/">An AI Factory for AI Reasoning NVIDIA DGX B 300</a></li>

</ul>
</details>

**标签**: `#CUDA`, `#GPU memory transfer`, `#performance optimization`, `#PyTorch`, `#systems`

---

<a id="item-3"></a>
## [多人游戏用每位玩家 GPU 上的本地世界模型生成各自画面](https://www.reddit.com/r/MachineLearning/comments/1xx4ta3/we_made_a_multiplayer_game_where_each_players/) ⭐️ 8.0/10

一个团队在约 3,958 小时的 10 人 CS:GO 机器人对局数据上训练了扩散 Transformer 世界模型，所有视角与输入均以 16 Hz 对齐，并推出了免费开放的多人游戏 beta：轻量服务器同步游戏状态，每位玩家用自己的 GPU 实时生成各自的画面。该 beta 需要 RTX 3080 或更高规格的显卡，同时提供实验性的 Mac 版本。 它把神经世界模型从单人演示推进到网络同步的多人可玩原型，展示了一条“画面由每位玩家本地生成而非传输像素”的渲染路径。同时发布的约 4,000 小时对齐数据集也对游戏 AI、动作条件视频生成和世界模型研究有直接价值。 该原型目前仍受限于一张小地图、仅手枪以及细节保真度不足。服务器状态、玩家动作与前一帧会被输入扩散 Transformer 以绘制下一帧，训练数据集已发布在 Hugging Face 上。

reddit · r/MachineLearning · /u/bengal7ion · 11月15日 19:46

**背景**: 世界模型是一种学习得到的模型，它根据当前游戏状态和玩家动作预测未来的观测——在这里就是下一帧渲染画面——而不是回放传统的 3D 引擎。扩散 Transformer（DiT）是一类生成模型，它用基于 Transformer 的主干取代扩散模型常用的 U-Net，在潜空间 patch 上运行，因而具备良好的可扩展性，已成为高质量图像与视频生成的常见架构。实时运行这类模型并不容易，因为扩散通常需要每帧多步去噪；能在消费级 GPU 上做到这一点并保持多人状态同步，正是这项工作的核心技术难点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2212.09748">[2212.09748] Scalable Diffusion Models with Transformers Diffusion Transformer Explained | Towards Data Science What Are Diffusion Transformers (DiTs)? The Architecture ... Diffusion Transformer (DiT) Architecture - emergentmind.com Diffusion Transformer Architectures (DiT) - emergentmind.com Diffusion Transformers (DiT) Architecture - apxml.com</a></li>
<li><a href="https://towardsdatascience.com/diffusion-transformer-explained-e603c4770f7e/">Diffusion Transformer Explained | Towards Data Science</a></li>

</ul>
</details>

**标签**: `#world-models`, `#diffusion-transformers`, `#game-ai`, `#real-time-rendering`, `#multiplayer-systems`

---

<a id="item-4"></a>
## [MacBook Pro 的 OLED PWM 频闪引发可用性担忧](https://macanorak.com/the-macbook-pros-oled-pwm-problem-when-a-better-display-becomes-worse-to-use/) ⭐️ 7.0/10

一篇技术文章指出，MacBook Pro 的 OLED 显示屏虽然技术上更优，却可能因 PWM 频闪让敏感用户感到不适；Hacker News 上的讨论则对报道中的 240Hz PWM 频率提出质疑。 这件事的重要性在于，显示质量不只是对比度和色彩；频闪会影响光敏感人群、偏头痛或脑震荡史用户的眼部舒适度、注意力和可用性，也可能影响消费者的购买决策以及对未来 Apple 显示屏的期待。 PWM 调光通过快速开关显示屏的光输出来调节亮度，而低于约 1000Hz 的频率通常被认为可能让敏感用户不适；评论者认为，tandem OLED 可能让两层各自以 480Hz、180 度反相运行，从而形成等效 960Hz，因此 240Hz 这一数字可能是测量或谐波造成的假象。

hackernews · MacAnorak · 11月15日 13:15 · [社区讨论](https://news.ycombinator.com/item?id=50506719)

**背景**: PWM（脉冲宽度调制）是一种常见的显示屏亮度控制方式，它通过极快地开关光源来调光；在一个周期内亮的时间占比越高，人眼感知到的亮度就越高。OLED 面板没有独立背光，因此许多 OLED 屏幕通过调制像素本身的发光来降低亮度，这在某些条件下会产生可见频闪。部分用户对这类频闪敏感，即使显示屏的色彩、对比度和运动表现都很出色，也可能出现眼疲劳、头痛或眩晕。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://daylightcomputer.com/blog/screen-flicker-101">Daylight | Light Flicker — Why your screen turning on & off 500 times...</a></li>
<li><a href="https://discussions.apple.com/thread/254749941">Severe Eye Strain due to OLED PWM Dimming - Apple Community</a></li>
<li><a href="https://circadianshield.com/guides/oled-pwm-flicker-eye-strain/">OLED PWM Dimming and Eye Strain : Why OLED ... | Circadian Shield</a></li>

</ul>
</details>

**社区讨论**: 评论者欢迎文章关注频闪敏感问题，但不认同 240Hz 的说法，认为 tandem OLED 可能每层以 480Hz 运行、反相时等效约 960Hz；也有人补充说，CRI、运动模糊、脑震荡相关的屏幕敏感以及高于屏幕刷新率的频闪感知同样是重要因素。

**标签**: `#OLED`, `#PWM flicker`, `#display technology`, `#eye strain`, `#Apple`

---

<a id="item-5"></a>
## [微软 365 服务中断致酒店 15 名客人氯气中毒](https://www1.wdr.de/nrw/rheinland/rhein-erft-kreis/technischer-defekt-chlor-phantasialand-100.html) ⭐️ 7.0/10

由于微软 365 服务中断，德国莱茵-埃尔夫特县 Phantasialand 度假区的一家酒店未能收到桑拿/泳池区维护安全系统自动发出的电子邮件警报，因此无人察觉自动加氯系统向泳池中投放了过量的氯。最终导致 15 名客人氯气中毒，酒店运营方向德国广播机构 WDR 证实了这一关联。 这起事件生动展示了当安全关键警报链路依赖于没有备用方案的通用云服务时会发生什么：一次普通的生产力套件故障最终升级为人身伤害。它很可能促使酒店、水上乐园等公共设施重新审视其监控与告警架构，也为关于云与第三方依赖所带来韧性缺口的更广泛讨论提供了现实案例。 据报道，泳池的自动加药系统使水中余氯超标，而维护安全系统仅通过电子邮件发出警报，没有短信、电话、警铃或现场声光报警作为第二通道。因此失效点并非加药硬件本身，而是一条单一、无冗余的通知路径，它在第三方服务中断期间悄无声息地吞掉了这条警告。

hackernews · DeepLogin · 11月15日 18:36 · [社区讨论](https://news.ycombinator.com/item?id=50509411)

**背景**: 微软 365 是微软的云订阅套件，其中包含 Exchange Online——许多组织用它取代本地邮件服务器；当该服务发生中断时，邮件可能延迟数小时甚至丢失。商业泳池和桑拿通常使用自动加氯系统，由传感器测量消毒剂或氧化还原电位水平并控制泵注入氯，现代控制器还能在加药超出范围时发出警报。在安全工程中，这类警报被视为安全关键环节：应当具备相互独立、独立供电的冗余通道，并触发本地可听见的报警，而不是依赖单一的消息系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.atlanticcouncil.org/in-depth-research-reports/report/critical-infrastructure-and-the-cloud-policy-for-emerging-risk/">Critical infrastructure and the cloud: Policy for emerging risk</a></li>
<li><a href="https://www.bdo.com.au/en-au/insights/cyber-security/managing-third-party-and-cloud-dependency-risks-strategies-for-stronger-resilience">Managing third-party and cloud dependency risks - BDO</a></li>
<li><a href="https://chloroklean.com/auto-dosing">Auto- Dosing ClO2 for Holiday Parks | ChloroKlean</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论几乎一致认为责任在于酒店的系统设计而非微软，有人直言：如此危险的事情仅靠电子邮件告警、且没有备份或二次核验，是不可接受的。其他评论者强调，任何可能造成此类伤害的系统都需要更具韧性、具备冗余的架构；一位自称在 Azure 工作的评论者还明确表示，该帖并非为这次中断辩护。另有讨论强调了氯气暴露的严重性，有人讲述了亲属因吸入家中自制氯气而需急诊治疗的经历。

**标签**: `#cloud-dependency`, `#safety-critical-systems`, `#reliability`, `#incident-analysis`, `#Microsoft 365`

---

<a id="item-6"></a>
## [Sebastian Raschka 详解现代 LLM 的位置嵌入，引发群论层面的讨论](https://magazine.sebastianraschka.com/p/understanding-positional-embeddings) ⭐️ 7.0/10

Sebastian Raschka 在其专栏发布了一篇技术解读文章，系统讲解现代大语言模型如何编码和处理 token 的位置信息，既涵盖经典的绝对位置/正弦位置编码方案，也介绍了 RoPE 等当代方法以及近期开源模型实际采用的做法。该文在 Hacker News 上获得大量关注（183 分、23 条评论），评论者 programjames 指出文章停留在实现层面，忽略了「位置嵌入本质上是群的表示」这一更深层的理论视角。 位置编码是 Transformer 的核心架构选择之一，它直接决定了模型在超出训练上下文长度时的外推能力，因此一份清晰的跨模型对比对构建或微调 LLM 的开发者具有实际价值。围绕该文的讨论也折射出该领域一个长期存在的张力：一边是行之有效的工程配方，另一边是解释这些配方为何有效的数学基础。 文章对比了相加式的绝对位置嵌入与 RoPE 这类基于旋转的相对位置方案——后者用旋转矩阵编码绝对位置，同时在自注意力计算中引入显式的相对位置依赖。评论者的批评在于：仅从实现层面讨论，无法解释为什么某些参数化形式天然可微、可学习，而这个问题通常要靠单参数群及其不可约表示来回答。

hackernews · vismit2000 · 11月15日 12:14 · [社区讨论](https://news.ycombinator.com/item?id=50506376)

**背景**: Transformer 并行处理所有 token，因此不像循环网络那样自带顺序概念，必须显式地注入位置信息。早期模型将固定的正弦向量加到 token 嵌入上；后来的方法（尤其是 2021 年随 RoFormer 提出的旋转位置嵌入 RoPE）改为按与位置成正比的角度旋转 query 和 key 向量，使注意力分数自然依赖于相对距离。群论之所以介入，是因为满足平移一致性的位置编码可以被描述为单参数群，而关于这类群的已知结论会严格限制哪些编码形式在数学上可行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/understanding-positional-embeddings">Understanding Positional Embeddings in Modern LLMs</a></li>
<li><a href="https://arxiv.org/abs/2104.09864">RoFormer: Enhanced Transformer with Rotary Position Embedding</a></li>
<li><a href="https://blog.janestreet.com/using-group-theory-to-explore-positional-encodings-attention/">Using group theory to explore the space of positional ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论整体认可这篇解读，但对其覆盖面提出了质疑：programjames 认为位置嵌入本质上是群的表示，而正是这一框架决定了如何发现它们、以及如何参数化才能使其可微、可学习，并以旋转位置嵌入作为阿贝尔平移群 ℝⁿ 的表示为例。总体情绪是：实现层面的讲解固然有用，但缺少理论视角就不够完整。

**标签**: `#LLMs`, `#positional-embeddings`, `#transformers`, `#group-theory`, `#machine-learning`

---

<a id="item-7"></a>
## [博主主张所有 AI 生成的代码都应开源](https://jakub.jankiewicz.org/blog/ai-code-open-source/) ⭐️ 7.0/10

Jakub Jankiewicz 发表了一篇博客文章，主张凡是借助 AI 生成的代码都应以开源许可证或知识共享零协议（CC0）发布，理由是这些模型本身就是在自 GNU 计划启动以来积累的海量开源代码语料上训练出来的。该文登上 Hacker News 首页，获得 1000 多个赞同和约 550 条评论。 这一主张直击 AI 编程助手背后的核心商业假设：企业可以将继续由 AI 辅助产出的代码保持专有。若该规范被广泛接受，将重塑企业使用 Copilot、Cursor 等工具构建软件时的许可方式，并进一步卷入围绕训练数据、版权与开源互惠的更大范围、尚无定论的争论。 其核心论据是关于训练数据的互惠主张，而非严格的法律论证；评论者指出，美国版权局的指导意见认为，将 AI 用于辅助而非取代人类创造力，本身并不妨碍产出获得版权保护。也有人指出，即便纯 AI 生成的代码不受版权保护，这一点本身也不会赋予第三方要求获得该代码的任何权利。

hackernews · jcubic · 11月15日 14:46 · [社区讨论](https://news.ycombinator.com/item?id=50507303)

**背景**: 现代 AI 编程助手是在大量公开源代码上训练的，其中许多采用宽松型或传染型开源许可证，这引发了其产出是否继承任何许可义务的疑问。与此同时，美国版权局正在陆续发布关于 AI 的多部分报告：2025 年 1 月的第二部分讨论生成式 AI 产出的可版权性，而 2023 年 3 月的登记指南要求申请人披露 AI 生成内容，并排除超出最低限度（de minimis）的部分。文章作者 Jakub Jankiewicz 将该问题定位为对提供了训练数据的开源生态是否公平的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.copyright.gov/ai/">Copyright and Artificial Intelligence | U.S. Copyright Office</a></li>
<li><a href="https://jakub.jankiewicz.org/blog/ai-code-open-source/">All AI - generated code should be Open Source</a></li>

</ul>
</details>

**社区讨论**: 评论区观点明显分裂而非一边倒：一方援引美国版权局指导意见，认为现有法律已足以解决 AI 可版权性问题，且 AI 辅助产出仍受保护；另一方则认为 AI 不过像编译器一样是工具，数月来在方向把控、反复打磨和工程投入上的人类作者身份依然充分。一个反复出现的反驳是：按该文逻辑，使用开源框架或从 Stack Overflow 学来的代码也应当被强制开源，而把写代码等同于软件工程则忽视了所有权与商业风险；还有一个务实观点是，真正让专有代码保持专有的并非版权这道法律屏障，而是从公司内部把代码拿走的难度。

**标签**: `#ai`, `#open-source`, `#copyright`, `#licensing`, `#software-engineering`

---

<a id="item-8"></a>
## [报道称卢特尼克推动放宽与其家族企业相关的芯片出口规则](https://www.nytimes.com/2026/11/15/us/politics/lutnick-pushed-to-weaken-chip-rules-that-overlap-with-his-family-business.html) ⭐️ 7.0/10

《纽约时报》2026 年 11 月 15 日的一篇报道称，美国商务部长霍华德·卢特尼克（Howard Lutnick）推动放宽部分美国芯片出口规则，而这些规则所涉领域与其家族企业的商业利益存在重叠。报道认为，这一举动在人工智能硬件政策的制定过程中同时引发了利益冲突与国家安全方面的质疑。 出口管制是华盛顿控制先进人工智能加速器获取渠道的主要手段，因此任何被视为放松管制的举动，都可能直接影响哪些国家和客户能够获得最先进的芯片。若在任商务部长被指在其家族经济利益相关的领域采取行动，可能削弱出口管制体系的可信度，并招致国会的审查。 报道的核心是卢特尼克的公职决策与其家族企业 Cantor Fitzgerald（他在进入政府前曾执掌该公司）的利益之间的重叠；但此处提供的摘要并未具体说明究竟涉及哪些规则。相关说法属于新闻报道中的指控，社区讨论中还提到了一笔马来西亚数据中心投资以及英伟达的 Blackwell GPU，这些细节并未被现有材料独立证实。

hackernews · JumpCrisscross · 11月15日 11:40 · [社区讨论](https://news.ycombinator.com/item?id=50506180)

**背景**: 美国对先进半导体的出口管制由商务部工业与安全局（BIS）负责执行，该机构维护受限技术和实体清单，决定美国设计的芯片可以销往何处，尤其是对华出口。由于人工智能训练集群依赖少数几款高端 GPU，这些规则构成了全球人工智能硬件供应链上的主要卡点。霍华德·卢特尼克原为金融服务公司 Cantor Fitzgerald 的首席执行官，于 2025 年出任商务部长，从而主管负责这些管制措施的机构。

**社区讨论**: Hacker News 上的讨论（约 435 分、188 条评论）几乎一边倒地持批评态度，有评论者称卢特尼克在华尔街生涯中就已存在道德问题，还有人指责他把公司利益置于国家安全之上。也有少数回复把话题引向对人工智能硬件政策中腐败问题的更广泛冷嘲，一位评论者指出开放权重模型是在中国公司拥有的英伟达 GPU 上训练出来的，并追问如果不存在这些腐败会是什么局面。

**标签**: `#AI chips`, `#export controls`, `#technology policy`, `#national security`, `#conflicts of interest`

---

<a id="item-9"></a>
## [免训练早退：改输出层单行权重](https://www.reddit.com/r/MachineLearning/comments/1xx1xdm/trainingfree_early_exit_for_reasoning_models_a/) ⭐️ 7.0/10

一个 Reddit 项目提出了一种免训练的推理模型早退方法：把探针方向乘以 14 后加到输出层中 </think> token 对应的权重行，使模型更早停止思考。作者报告 Qwen3.5-4B 在 8 道未见过的 MATH-500 题上保持相同准确率并减少 54% token，DeepSeek V4.1 Flash 在数学题上以少 40% token 达到 7/7，而原模型为 6/7。 如果该方法能够泛化，它有望在推理阶段削减推理模型代价高昂的“过度思考”阶段，而且无需重新训练、额外运行时代码或专用推理栈，因为产物只是一个普通权重文件。对于部署长链式思维模型、且延迟和 token 成本主要被冗余复查占据的团队，这一点很重要。 该探针用线性判别分析在 24 道数学题的隐藏状态上拟合，把正确答案出现后段落结尾标为“已完成”；由于只改变 </think> 行，作者可以从记录的隐藏状态离线模拟编辑后的模型行为。作者承认此前已有基于探针的提前停止工作（Zhang et al. 2025, arXiv 2504.05419），并列出局限：样本小、每种设置只跑一次、探针仅在数学数据上拟合，以及 AIME 2025 对比使用 32k token 预算，低于 Qwen 建议的 81,920。

reddit · r/MachineLearning · /u/Good-Presentation-23 · 11月15日 17:52

**背景**: 早退是一种通用的推理效率思路：不总是把模型跑到固定深度或完整生成长度，而是在中间信号表明答案已经足够好时让其停止。线性探针是一种简单的线性分类器，拟合模型内部隐藏状态来检测某种属性，例如模型仍在解题还是只是在复查。DeepSeek、Qwen 等推理模型会先写一段草稿再作答，并以特殊 token </think> 结束草稿；其输出层用当前隐藏状态与每个词表 token 的权重行相乘来打分。该帖子把这些思路结合起来，只编辑 </think> 对应的输出层权重行，这是一种无需重新训练的轻量模型编辑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://intellabs.github.io/distiller/algo_earlyexit.html">Early Exit - Neural Network Distiller</a></li>
<li><a href="https://deepwiki.com/guijiejie/Attention-driven-Masking-and-Throwing/5.3-linear-probing">Linear Probing | DeepWiki</a></li>
<li><a href="https://www.researchgate.net/publication/386121431_A_Survey_on_Knowledge_Editing_of_Neural_Networks">(PDF) A Survey on Knowledge Editing of Neural Networks</a></li>

</ul>
</details>

**标签**: `#LLM reasoning`, `#early exit`, `#model editing`, `#inference efficiency`, `#machine learning`

---

<a id="item-10"></a>
## [FAA 全国停飞起因查明：换铜线升级后路由器故障](https://www.theverge.com/transportation/1033898/faa-ground-stop-sean-duffy-faa-copper-wire) ⭐️ 7.0/10

美国交通部长 Sean Duffy 于 11 月 14 日表示，FAA 周五下令的全国停飞源于一处偏远设施的例行维护——把老旧铜线更换为光纤，随后新装的路由器开始以每 4 到 5 秒逾千次连接请求冲击其他路由器。这一故障干扰了雷达信号与飞机通信，导致数千架次航班停飞；Duffy 称根本原因尚未确定，可能是硬件故障、配置错误，也可能是承包商 L3Harris 的失误。 该事件表明，在例行推进遗留系统现代化时引入的单个异常设备，可能级联演变为安全关键系统的全国性中断，造成数千架次航班停飞，甚至促使欧洲方面暂停飞往美国的航班。这也为 FAA 耗资数十亿美元的空管系统改造增添了理由，并为可靠性工程领域提供了一个关于在关键网络中把铜线换成光纤所伴随风险的具体案例。 触发故障的路由器以每四到五秒超过一千次的频率向其他路由器发送连接请求，压垮了承载雷达数据与空地通信的网络。Duffy 表示调查人员尚未确定问题出在硬件、配置还是承包商的施工执行上，并借此次发布会呼吁国会批准追加空管现代化资金。

telegram · zaihuapd · 11月15日 02:10

**背景**: 作为 FAA 电信基础设施（FTI）计划的一部分，FAA 正在把各设施——从大型航路管制中心到偏远雷达站和气象站——沿用了数十年的铜线更换为高速光纤，相关工作由承包商 L3Harris 承担。这项现代化改造服务于更宏大的“全新空中交通管制系统”（BNATCS）计划，目标是在 2028 年底前替换老旧的雷达、软件、硬件与电信网络。由于这些站点中不少无人值守且地处偏远，其中单个出问题的设备仍会处于全国空中交通管理的关键路径上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/2026_FAA_nationwide_ground_stop">2026 FAA nationwide ground stop - Wikipedia</a></li>
<li><a href="https://www.republicworld.com/world-news/us-air-travel-should-normalise-sunday-after-ground-stop-triggers-mass-cancellations-faa-2026-11-15-141088">US Air Travel Should Normalise Sunday After Ground... | Republic World</a></li>
<li><a href="https://www.l3harris.com/all-capabilities/faa-telecommunications-infrastructure-fti">FAA Telecommunications Infrastructure (FTI) - L3Harris</a></li>

</ul>
</details>

**标签**: `#aviation`, `#network-outage`, `#infrastructure`, `#systems-reliability`, `#legacy-modernization`

---

<a id="item-11"></a>
## [Telegram 小组件被指存在沙箱逃逸与远程代码执行漏洞](https://t.me/zaihuapd/45139) ⭐️ 7.0/10

一个 Telegram 频道帖子警告称，2026 年 11 月 9 日在 Bot API 10.4 中引入的 Telegram 小组件存在沙箱逃逸漏洞，可能导致远程代码执行，并呼吁用户不要点击来路不明的机器人。 如果属实，恶意机器人只需在聊天中展示小组件，就可能在用户设备上执行代码，危及 Telegram 庞大的用户群和机器人生态。 小组件是内嵌 CSS 和 JavaScript 的独立 HTML 文档，上限为 32 KB（压缩后 4 KB），本应在无网络访问的沙箱中运行；但该帖未提供 CVE 编号、受影响客户端版本或概念验证，因此该说法尚未得到证实。

telegram · zaihuapd · 11月15日 10:51

**背景**: Telegram 的 Bot API 允许第三方机器人在聊天中发送消息、按钮和其他交互内容。Bot API 10.4 新增了小组件（Widgets），即直接渲染在消息气泡中的小型交互式 HTML 块。由于小组件包含 JavaScript，Telegram 客户端必须用沙箱将其隔离；沙箱逃逸意味着恶意小组件代码突破了这层隔离。这类漏洞之所以严重，是因为小组件通过普通聊天消息投递，用户可能无需安装额外应用就会接触到。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://core.telegram.org/bots/widgets">Telegram Widgets</a></li>
<li><a href="https://core.telegram.org/bots/api-changelog">Bot API changelog - Telegram APIs Telegram Bot API 10.4 Explained: HTML Widgets and TON Wallet Telegram Bot API 10.4 introduces Interactive Message Widgets ... Telegram's Bot API 10.4 adds interactive mini-apps in chats Telegram обновил Bot API до версии 10.4: что нового Telegram widgets (Bot API 10.4): interactive cards inside ...</a></li>

</ul>
</details>

**标签**: `#Telegram`, `#security vulnerability`, `#RCE`, `#Bot API`, `#JavaScript sandbox`

---

<a id="item-12"></a>
## [研究称六款中国 AI 模型权重中留有 Blackwell 芯片指纹](https://t.me/zaihuapd/45140) ⭐️ 7.0/10

Unemployment Labs 发布分析称，DeepSeek、月之暗面、MiniMax 和蚂蚁集团共六款公开模型权重，其初始参数布局与在英伟达 Blackwell 芯片上初始化相吻合。研究者表示，DeepSeek-V4-Flash 的结果已在 B300 实机上复现，Kimi K3 也在 GB200 上获得高度相关的匹配。 如果仅凭公开模型权重就能推断所用硬件，外部研究者便获得了一种判断前沿模型由何种 GPU 构建的手段，这对出口管制的执行和 AI 供应链透明度都有直接影响。这也将打破“中国实验室内部使用何种芯片对外界不可见”的假设。 该结论完全建立在事后对公开模型权重的分析之上，而非来自任何实验室的披露；目前所谓复现也只是在 B300 和 GB200 机器上得到相关性匹配，并非经过同行评审的证明。作者推断这些模型是在 Blackwell 硬件上完成初始化，并进一步推测相关芯片也参与了训练，而后一步已超出单纯的初始化指纹所能证实的范围。

telegram · zaihuapd · 11月15日 11:08

**背景**: 模型指纹识别是一类通过比对参数统计、内部表征或诱导行为等内在证据与已知参照，来判断模型来源的技术，此前主要用于所有权与出处验证，而非硬件溯源。Blackwell 是英伟达接替 Hopper 的 GPU 微架构，以 B200、B300 以及 GB200/GB300 等 Grace-Blackwell 模块形式出货，也正是美国出口管制所限制的硬件类别。被点名的 DeepSeek-V4-Flash、Kimi K3 等均为近期发布的开放权重中国模型，正是权重公开才使这种权重层面的检查成为可能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2605.29245">Implicit Identity Technologies for LLMs: Fingerprinting and ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Blackwell_(microarchitecture)">Blackwell (microarchitecture) - Wikipedia</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI models`, `#hardware fingerprinting`, `#Nvidia Blackwell`, `#export controls`, `#model weights`

---

<a id="item-13"></a>
## [华为云 MaaS 平台正式上线开源盘古模型 openPangu-2.1-Pro](https://mp.weixin.qq.com/s/8JfFmscBTDl_mPQMycD8Nw) ⭐️ 7.0/10

11 月 15 日，华为云在 MaaS（模型即服务）平台正式上线开源盘古模型 openPangu-2.1-Pro，围绕 Agent 开发、AI 编码和推理优化三大方向进行能力升级。该模型基于 10 万余条专项数据优化 Skills 触发与工具调用，重点适配鸿蒙 ArkTS 开发与昇腾算子生成。 这让鸿蒙与昇腾开发者拥有了一个针对自家工具链而非通用编码任务调优的第一方模型，有望显著加快鸿蒙原生应用开发与昇腾算子编写效率。缓存命中输入价格低至每百万 tokens 0.016 元，也使大规模 Agent 调用在华为云上更具成本可行性。 定价为输入 0.8 元/百万 tokens、输出 3.2 元/百万 tokens，缓存命中输入仅需 0.016 元/百万 tokens。该模型已接入智果 AgentArts、码道 CodeArts、果办 OfficeAce 等产品，但本次发布并未公布独立的基准测试对比或模型参数规模等细节。

telegram · zaihuapd · 11月15日 16:03

**背景**: 华为云 MaaS（模型即服务）平台提供文本生成、代码生成、问答、翻译等预训练模型的一键调用能力，开发者通过 API 使用模型而无需自行部署基础设施。ArkTS 是华为为鸿蒙生态打造的应用开发语言，基于 TypeScript 语法并强化了静态检查；昇腾则是华为自研的 AI 加速芯片产品线，其算子往往需要专门优化。盘古是华为自研的大模型系列，其中带 "open" 前缀的开源版本以公开权重形式提供，同时也可在华为云上托管调用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://1y.hk/en/post/11-15-openpangu-2-1-2jsl">Huawei Cloud to Launch openPangu - 2 . 1 - Pro on November 15 · AI Brief</a></li>
<li><a href="https://www.huaweicloud.com/intl/en-us/product/maas.html">Huawei Cloud MaaS - HUAWEI CLOUD</a></li>
<li><a href="https://developer.huawei.com/consumer/en/arkts/">ArkTS - HUAWEI Developers</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#Pangu`, `#LLM`, `#open-source AI`, `#Huawei Cloud`

---

<a id="item-14"></a>
## [回顾：Turbo Pascal 的极小体积与现代软件膨胀之对比](https://prog21.dadgum.com/116.html) ⭐️ 6.0/10

prog21.dadgum.com 于 2011 年发表的一篇博客文章再次引发关注，该文以 Borland 出品的紧凑型 Pascal 编译器与 IDE——Turbo Pascal 作为标尺，指出如今许多现代程序的二进制文件（甚至包括 Unix `touch` 这类功能极简的命令）都比 1980 年代的一整套开发环境大得多。这篇文章在 Hacker News 上重新被讨论，评论区围绕这种逐字节比较是否有意义展开了争论。 这场讨论触及了关于软件膨胀的长期争论：随着硬件性能大幅提升，开发者越来越倾向于用二进制体积和运行效率换取生产力、抽象层与功能特性。对于从事嵌入式系统、精简容器镜像或安全敏感代码的工程师来说，究竟需要多少复杂度才算合理，依然是一个具有现实意义的问题。 Turbo Pascal 以极快的单遍编译著称，其发行包是一个紧凑的 IDE 加编译器；出于历史价值考虑，Borland 后来免费发布了 DOS 下的 1.0、3.02 和 5.5 版本。讨论中的批评者指出，单纯的字节数比较忽略了功能差异、平台惯例，以及自 1980 年代以来在创建、存储和传输成本方面发生的巨大变化。

hackernews · ksec · 11月15日 13:44 · [社区讨论](https://news.ycombinator.com/item?id=50506894)

**背景**: Turbo Pascal 是运行于 CP/M 和 MS-DOS 上的 Pascal 语言编译器与集成开发环境，最初由 Anders Hejlsberg 在 Borland 开发，于 1983 年首次发布；它凭借速度和体积优势使 Borland 成为 PC 开发工具领域的领导者。软件膨胀指的是程序 successive 版本占用越来越多磁盘空间、内存和 CPU，而质量却停滞甚至下降的现象，通常由功能蔓延、新增抽象层或忽视优化所导致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Turbo_Pascal">Turbo Pascal - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Software_bloat">Software bloat</a></li>

</ul>
</details>

**社区讨论**: 有评论者盛赞 Anders Hejlsberg 是最伟大的语言设计者之一，列举了 Turbo Pascal、Delphi、C# 和 TypeScript，也有人质疑为何 Pascal 影响深远却几乎消亡。一些人认为连 `touch` 这样的简单工具都不应比 Turbo Pascal 更大，并将原因归咎于重复的样板代码与开发者的惰性；而持怀疑态度的人则认为这类比较毫无意义，因为字节在不同历史背景下的用途和成本各不相同。

**标签**: `#software-bloat`, `#turbo-pascal`, `#programming-languages`, `#software-history`, `#hacker-news-discussion`

---

<a id="item-15"></a>
## [博主用 Emacs 的 eww 取代传统浏览器，引发 Hacker News 热议](https://joshblais.com/blog/emacs-as-my-browser/) ⭐️ 6.0/10

Josh Blais 在 joshblais.com 发表了一篇题为《Emacs Is My Browser》的博文，讲述他如何用 Emacs 内置的文本浏览器 eww 代替传统浏览器来日常阅读网页。该文在 Hacker News 上引来约 80 条实质性评论，读者们既交流使用技巧，也争论这种做法的局限。 这篇博文是“极简、键盘驱动式计算”的一个具体案例，而围绕它的讨论也清楚地暴露出这种理念与当今重度依赖 JavaScript 的商业网页之间的冲突。它对 Emacs 用户，以及那些正在权衡“自己到底需要完整浏览器才能阅读多少现代网页”的开发者最有参考价值。 eww 会把 HTML 渲染成纯文本的 Emacs 缓冲区，并且不执行 JavaScript，因此静态 HTML 和博客用起来很顺畅，而 Reddit 及大多数商业网站则会出错或严重退化。评论者提到了一些折中办法，例如通过 Emacs 的 xwidget 支持嵌入 WebKit，或退而使用 Dillo、w3m-mode 这类轻量浏览器。

hackernews · nyc111 · 11月15日 15:21 · [社区讨论](https://news.ycombinator.com/item?id=50507553)

**背景**: Emacs 是一款高度可扩展、可脚本化的文本编辑器，许多程序员把它当作编辑代码、收发邮件、运行终端等工作的完整环境。eww（“Emacs Web Wowser”）是内置于 Emacs 的浏览器，它抓取网页后会把 HTML 渲染成 Emacs 缓冲区中带格式的文本，而不是显示在图形浏览器窗口中。由于它运行在编辑器内部，因此很受那些希望待在一个以键盘为中心的环境里、不愿再开一个独立程序的用户青睐——这与 Richard Stallman 倡导的自由软件极简理念一脉相承，只不过 Stallman 本人回避浏览器的动机是意识形态而非专注度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://planet.emacslife.com/">Planet Emacslife</a></li>
<li><a href="https://en.wikipedia.org/wiki/Richard_Stallman">Richard Stallman - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者的态度总体同情但很务实：Arubis 强调现代商业网页与这套方案“合不来”，用于静态 HTML 和博客没问题，但 Reddit 和商业网站就不行。其他人则分享了实用技巧——kmstout 推荐了基于 follow-mode 的分栏显示以在屏幕上塞下更多文字，krylon 讲述如何用 w3m-mode 让一台旧笔记本重获新生来读维基百科，jll29 指出 Stallman 出于意识形态原因让人把网页截图邮件发给他；leoc 则认为真正急需的是可内容寻址的 HTTP(S) 替代方案。

**标签**: `#emacs`, `#web-browsing`, `#eww`, `#developer-tooling`, `#hackernews-discussion`

---

<a id="item-16"></a>
## [Marimba：基于冻结版 Qwen3-ASR 构建的开源权重“System One”语音模型](https://www.reddit.com/r/MachineLearning/comments/1xwzsm4/marimba_a_system_one_model_for_speech_r/) ⭐️ 6.0/10

一位开发者发布了 Marimba，这是一个采用 Apache-2.0 协议、可通过 pip 安装（marimba-audio）的开源权重模型，它构建在冻结的 Qwen3-ASR-0.6B 之上，输出的是结构化决策——是/否、某个选项或一个分数——而不是转写文本。词级与语种级问题通过 ASR 解码器假设的零样本分数加校准来回答，而语音活动检测、话轮结束、说话人切换和说话人数量则依靠冻结编码器上的小型读出层处理；作者称论文将在本周发布于 arXiv。 它展示了一条实用路径：无需重新训练主干，就能从现有小型 ASR 检查点中榨取出多种轻量级语音决策能力，从而降低构建常驻语音交互（如 VAD、话轮切换、语种路由）的成本与门槛。开源权重加上 pip 安装包也让其他人易于复现和扩展，尽管目前验证工作仍然有限。 由于主干被冻结，所有适配都发生在校准环节或小型读出头上，而非 ASR 模型本身，这让系统保持轻量，但在偏离转写任务的场景上可能限制准确率上限。由于论文尚未发布，基准测试数值、延迟以及在噪声条件下的鲁棒性等细节还没有完整披露，而且该项目由单人开发。

reddit · r/MachineLearning · /u/solanotodesch · 11月15日 16:30

**背景**: Qwen3-ASR-0.6B 是 Qwen3-ASR 系列中的一款紧凑型开源语音识别模型，该系列还包含 1.7B 版本，支持多语种转写与语种识别，并基于 Qwen3-Omni 的音频理解能力构建。“System One”这一说法来自 TypeSafe AI 的 Jev，用来描述一类专为做出软件可直接使用的快速结构化判断而设计的模型，与较慢的深思式推理相对。Marimba 把这一思路迁移到音频领域，同时也借鉴了线性探针这一常见技术——即在冻结的激活上训练简单分类器，以检验某个概念是否可被线性解码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3-ASR-0.6B">Qwen/Qwen3-ASR-0.6B · Hugging Face</a></li>
<li><a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">Introducing System One Models & Jev - TypeSafe AI Blog</a></li>
<li><a href="https://ai-math-map.vercel.app/methods/linear-probing">Linear probing — Math in LLMs Research Map</a></li>

</ul>
</details>

**标签**: `#speech-recognition`, `#asr`, `#small-models`, `#open-weights`, `#audio-classification`

---

<a id="item-17"></a>
## [特斯拉宣布年底前开卖双座 Cybercab，首批优先供给自家车队](https://t.me/zaihuapd/45131) ⭐️ 6.0/10

特斯拉在周三的第三季度财报电话会上表示，将在今年年底前开始向客户出售 Cybercab。工程副总裁 Lars Moravy 称，当前产量全部供给自家 robotaxi 车队，之后才会小规模向客户交付全自动驾驶车辆。 这是特斯拉首次为这款专为无人驾驶设计的车型给出对外销售时间表，意味着没有方向盘的产品正从概念走向商业化。与此同时，其 robotaxi 服务规模仍然有限、无监督自动驾驶软件尚未完成，这一销售计划也将让特斯拉与联邦安全监管机构正面交锋。 这款双座 Cybercab 没有方向盘和踏板，采用纯视觉自动驾驶方案，目前正被 NHTSA 调查是否符合联邦安全标准。马斯克称 Cybercab 主要作为出行服务而非个人购买，无监督版 FSD 的推送则推迟到明年第二季度。

telegram · zaihuapd · 11月15日 01:10

**背景**: 按照美国法律，车企需自行认证其车辆符合《联邦机动车安全标准》，NHTSA 事后可以对该认证依据进行审查——特斯拉这款没有驾驶员操控装置的车型正面临这一审查。特斯拉于 2024 年 10 月发布 Cybercab，它是专为无人驾驶出租车打造的车型，与需要驾驶员监控“FSD（监督版）”的消费级车型不同。此前特斯拉的付费 robotaxi 服务一直由公司自营车队提供，而非通过卖给个人的车辆完成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tesla_Cybercab">Tesla Cybercab</a></li>
<li><a href="https://www.nhtsa.gov/vehicle-safety/automated-vehicle-safety">Automated Vehicle Safety - NHTSA</a></li>
<li><a href="https://electrek.co/2026/04/22/tesla-elon-musk-unsupervised-fsd-consumer-cars-q4-delay-again/">Elon Musk pushes unsupervised FSD for consumer Teslas — again</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#Cybercab`, `#autonomous driving`, `#robotaxi`, `#regulation`

---

<a id="item-18"></a>
## [美法官驳回美光、三星、SK 海力士撤销 DRAM 价格操纵诉讼的动议](https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge) ⭐️ 6.0/10

美国地区法官 Noël Wise 驳回了美光、三星和 SK 海力士要求撤销 DRAM 价格操纵集体诉讼的动议，认定原告提出的新证据足以支撑共谋指控成立的可能性。原告为 17 名个人和小企业，指控这三家芯片厂商在一年内采取四次平行行动限制 DRAM 供应，导致价格上涨最多达 500%。 这一裁决使案件越过最初的法律障碍进入证据开示阶段，三家几乎掌控全球 DRAM 产量的公司的内部定价与供应规划通信可能被公开。由于 DRAM 几乎用于所有个人电脑、手机和服务器，一旦认定存在共谋，可能重塑内存定价、采购合同以及整个科技行业的反垄断监管格局。 Wise 法官将三家公司的同步行为形容为「更像编队飞行」，而非各自独立的决策；这一点颇为关键，因为按照美国法律，单纯的平行行为通常不足以证明存在垄断协议。被告须在 12 月 7 日前作出回应，案件管理会议定于 2027 年 1 月举行，而驳回撤诉动议只是程序性一步，并不等同于认定其承担责任。

telegram · zaihuapd · 11月15日 16:39

**背景**: DRAM（动态随机存取存储器）是主流的半导体存储器，用作计算机、手机和服务器的主要工作内存，而这一市场已基本整合为三星、SK 海力士和美光三家供应商。美国反垄断法要求证明存在实际的协议，而非仅仅是有意识的平行行为，因此原告通常需要提供同步削减产能或可疑通信等额外的「附加因素」。撤诉动议是诉讼早期请求法院在证据开示前驳回案件的程序性申请，驳回它只意味着原告的指控具备合理的证据支撑，并不代表违法行为已被证实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/动态随机存储器">动态随机存储器 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.fapingedu.com/sys-nd/11907.html">法律英语知识之 Motion （ 动 议 ） - 法平教育</a></li>

</ul>
</details>

**标签**: `#DRAM`, `#semiconductors`, `#antitrust`, `#hardware-supply-chain`, `#legal`

---