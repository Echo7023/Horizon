---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 23 条内容中筛选出 12 条重要资讯。

---

1. [Lean 社区宣布黎曼猜想的机器验证完成，据称有 AI 参与](#item-1) ⭐️ 9.0/10
2. [浙江大学在超导芯片上首次真机实现量子随机存储器 QRAM](#item-2) ⭐️ 9.0/10
3. [GnuPG 披露 GPGME 内存安全漏洞，波及大量应用](#item-3) ⭐️ 8.0/10
4. [谷歌据称发布 Gemini 4 Neon，主打智能体编程](#item-4) ⭐️ 8.0/10
5. [微软为 Windows 引入 RDMA over USB4，多台 PC 可合跑一个大模型](#item-5) ⭐️ 8.0/10
6. [显示器 USB 集线器让以太网下载速度下降 75%](#item-6) ⭐️ 7.0/10
7. [15 年经验的高级工程师失业两年，在 HN 发帖求助](#item-7) ⭐️ 7.0/10
8. [daraxonrasib 一线数据：未经治疗的转移性胰腺癌客观缓解率达 60.7%](#item-8) ⭐️ 7.0/10
9. [美国陆军将在爱荷华州引爆巨量降解叠氮化铅](#item-9) ⭐️ 6.0/10
10. [OpenAI 指控 DeepSeek「蒸馏」美国模型，并游说国会限制中国 AI 企业](#item-10) ⭐️ 6.0/10
11. [美国收紧对马来西亚、泰国、新加坡先进芯片出口，印度欲承接外溢需求](#item-11) ⭐️ 6.0/10
12. [特朗普：建数据中心的企业应向当地社区缴纳「分红」](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Lean 社区宣布黎曼猜想的机器验证完成，据称有 AI 参与](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 9.0/10

11 月 20 日，Anthropic 的数学家 Levent Alpöge 声称借助 Claude 证明了黎曼猜想，并以 Lean 证明助手可校验的形式发布了证明，配套文稿据称超过 25 万页，他还称该证明确立了广义黎曼猜想。随后 Lean 证明器社区宣布该结果已完成形式化验证。 黎曼猜想自 1859 年提出以来一直是数学界最著名的未解难题，一旦证明通过验证，将重塑数论以及依赖素数分布的大量数学领域。由于这项工作据称需要在 Lean 中形式化现代数学的很大一部分，它对形式化验证和“AI 辅助定理证明”能否真正落地同样具有里程碑意义。 结果的可信度完全依赖于证明内核的正确性，社区给出的辩护是：如今存在多个用不同语言实现的独立内核，尤其是带有自身一致性证明的 con-leche 与 con-ron，要让黎曼猜想为假，就必须存在一个同时影响这些一致性证明和 RH 证明本身的共同缺陷。由于过程中始终有真人专家在环，AI 在无人察觉的情况下“绕过”问题的可能性大大降低，但整条流程仍待独立复核。

hackernews · g-b-r · 11月21日 14:36 · [社区讨论](https://news.ycombinator.com/item?id=50589618)

**背景**: Lean 这类证明助手是用形式化语言书写数学证明的软件，由一个很小的核心程序——内核——机械地逐步校验证明，因此信任一份形式化证明就等于信任该内核。过去机器校验的证明主要由人类交互式完成，而 LeanDojo、Lean Copilot 等近期工作则致力于让大语言模型在 Lean 内部提出证明步骤，错误步骤会被自动拒绝。黎曼猜想涉及黎曼 ζ 函数零点所在的位置，若成立将严格约束素数的分布规律；它的推广形式 GRH 把同一结论扩展到更广泛的一类函数上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://seclists.org/oss-sec/2026/q3/381">oss-sec: Lean 4 kernel soundness bug: forging proofs via nested...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_assistant">Proof assistant - Wikipedia</a></li>
<li><a href="https://leandojo.org/leandojo">LeanDojo: AI-Assisted Theorem Proving in Lean</a></li>

</ul>
</details>

**社区讨论**: 评论者认真对待这一结果，但关注点集中在信任链上：有人认为在多个带自洽性证明的独立内核面前，“内核 bug”这一解释已几乎不可能；也有人提醒，此前一个伪造的 Collatz 反例曾骗过某个号称独立的检查器，因此这些检查器的独立性没有宣传的那么强。不少人强调 Claude 在此过程中形式化了现代数学的一大块内容，使这成为超越 GRH 的基础性成果；还有很多人坚持认为 Levent Alpöge 功不可没，是他把模型的能力压榨到了极致，也有人开玩笑说该猜想应改名为“黎曼–Alpöge 定理”。

**标签**: `#formal-verification`, `#lean-prover`, `#riemann-hypothesis`, `#mathematics`, `#ai-assisted-proofs`

---

<a id="item-2"></a>
## [浙江大学在超导芯片上首次真机实现量子随机存储器 QRAM](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 9.0/10

浙江大学团队在自主制备的超导量子芯片「天目 2 号」上，全球首次于真机上实现了量子随机存储器（QRAM），成果发表于《自然·物理》。芯片上成功运行了可调取 4 位和 8 位数据的原型，准确率分别为 80.9% 和 60.4%，线路深度较未优化方案降低 30% 以上，并首次验证该架构具备局部抗噪特性。 QRAM 是让量子算法把经典数据以叠加态载入的关键硬件原语，被视为量子机器学习、量子线性代数和数据库搜索等加速方案的前提条件。此次从理论与小规模光学实验走向超导芯片，是迈向实用量子存储器的一步；不过准确率仍不高，说明距离大规模可用还有很长的路。 该器件仍属小规模原型：8 位取数 60.4% 的准确率远低于容错量子算法所需水平；而线路深度降低 30% 以上的优化十分关键，因为超导量子比特会随线路深度增加而丧失相干性。团队称首次通过实验确认该 QRAM 架构具备局部抗噪能力——即错误被限制在局部而不会扩散至整个存储阵列，并表示下一步将推进 QRAM 的规模化研究。

telegram · zaihuapd · 11月21日 08:31

**背景**: 经典 RAM 按需返回某个地址的内容；QRAM 则以量子叠加的方式完成同样的工作，一次纠缠查询即可取回多个地址的内容，「桶旅」（bucket-brigade）等架构正是为此类器件提出的设计路线。超导量子比特是目前主流的量子计算平台，本质是在接近绝对零度下运行、与谐振腔耦合的微波电路，其相干时间较短，使得深线路代价高昂。由于数据载入是大多数量子加速方案中的瓶颈，可用的 QRAM 长期被视为量子计算技术栈中缺失的重要一环。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/quantum-ram-qram">Quantum RAM : Bucket-Brigade Approach</a></li>
<li><a href="https://hub.valency.io/works/W_q6h5tdeb">Architectures for a quantum random access memory — Valency Hub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Superconducting_quantum_computing">Superconducting quantum computing - Wikipedia</a></li>

</ul>
</details>

**标签**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#quantum hardware`, `#Nature Physics`

---

<a id="item-3"></a>
## [GnuPG 披露 GPGME 内存安全漏洞，波及大量应用](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) ⭐️ 8.0/10

GnuPG 项目于 2026 年 11 月 20 日披露了编号为 CVE-2026-129975 的 GPGME 严重漏洞，并发布了修复版本。该漏洞由 Johan Carlsson 发现，于 2026 年 11 月 12 日通过 GitLab 上报；无论是作为共享库、DLL 还是静态链接使用受影响版本 GPGME 的软件都会受到影响。 GPGME 是多数邮件客户端、Gpg4win、Samba、Flatpak、众多 XMPP 客户端以及 GitLab 签名提交验证流程所依赖的高层加密 API，因此其中单个内存安全缺陷会传导到极其庞大的下游软件面。这会迫使众多项目同时进行协同重建与更新，而对 GitLab 而言，问题出在签名提交处理路径上尤其严重。 关于严重程度存在争议：有评论者认为这是一个双重释放（double free）缺陷，而非完整的远程代码执行利用链，并质疑此类报告是否被刻意夸大。披露日期因 GitLab 需要与另外的 Ruby2Shell 漏洞一起发布更新，而从 2026 年 11 月 25 日提前到 11 月 20 日；另有评论者指出，Red Hat 的 CentOS Stream GPGME 软件包似乎在五年前就已包含修复，但上游一直未采纳。

hackernews · gdgghhhhh · 11月21日 08:32 · [社区讨论](https://news.ycombinator.com/item?id=50587208)

**背景**: GPGME（GnuPG Made Easy）是一个 C 语言库，在 GnuPG 的 OpenPGP 后端之上提供加密、解密、签名、签名验证与密钥管理的高层加密 API，并提供 C++、Qt 与 Python 绑定。双重释放（double free）是一种内存安全缺陷，同一块已分配内存被释放两次，会破坏堆状态，并可能让攻击者影响后续的内存分配。广泛被链接的 C 库中的内存安全缺陷尤其危险，因为一个缺陷会影响到每一个链接该库的应用程序。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/gnupg-warns-critical-gpgme-flaw-could.html">GnuPG Warns Critical GPGME Flaw Could Expose App Data via...</a></li>
<li><a href="https://www.phoronix.com/news/GnuPG-GPGME-Critical">GnuPG 's GPGME Affected By Critical Security Bug In Turn... - Phoronix</a></li>
<li><a href="https://www.gnupg.org/software/gpgme/index.html">GPGME - GNU Privacy Guard</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者对“远程代码执行”的说法提出异议，其中一位认为这是双重释放而非完整 RCE 利用链，并质疑漏洞报告是否被夸大。其他人指出 Red Hat 多年前就已修复而上游未跟进，认为 C 与 C++ 需要 Rust 级别的工具链来防止此类缺陷，还有人希望确认该漏洞仅限于 GPGME，不会影响 apt 等工具。

**标签**: `#security`, `#gpgme`, `#vulnerability`, `#open-source`, `#memory-safety`

---

<a id="item-4"></a>
## [谷歌据称发布 Gemini 4 Neon，主打智能体编程](https://t.me/zaihuapd/45267) ⭐️ 8.0/10

据报道，谷歌发布了 Gemini 4 Neon 模型，主打在复杂软件工程、知识工作与科研工作流中实现快速的端到端执行，并已向开发者、企业用户以及 Google AI Pro/Ultra 订阅用户开放。其据称定价为每百万输入 token 3 美元（缓存输入 0.15 美元）、每百万输出 token 15 美元，支持 100 万 token 的上下文窗口。 如果这些基准成绩属实，谷歌将在智能体编程评测中登顶，而这一领域近期一直由 Anthropic 和 OpenAI 主导，并且直接关系到企业对 AI 编程工具的采购决策。与此同时，较低的缓存输入价格与 100 万 token 上下文，也会给竞争对手在长周期、代码仓库级别的智能体任务上带来更大压力。 该帖称 Gemini 4 Neon 以 58.6 分登顶 Artificial Analysis 编程智能体指数，并在智能指数 xhigh 档以 61 分位列总榜第三，同时还提到 Terminal-Bench 成绩，但原文在此处被截断。这些说法仅来自一条 Telegram 帖子，没有附上模型卡、官方博客公告或独立验证，因此相关数字应视为尚未证实。

telegram · zaihuapd · 11月21日 01:09

**背景**: Artificial Analysis 编程智能体指数用于衡量编程智能体在真实软件工程任务中的实际表现，除准确率外还会考察成本、token 消耗和执行时间。Terminal-Bench 则是另一套基准，考察智能体能否在终端中完成端到端的多步骤命令行任务。所谓“缓存输入”定价指的是提示词缓存机制：服务商会保存已处理 token 的 KV Cache，使重复出现的上下文（例如大型代码库）无需重新计算，并对这部分 token 按大幅折扣计费。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/agents/coding-agents">AI Coding Agent Benchmarks & Leaderboard | Artificial Analysis</a></li>
<li><a href="https://www.tbench.ai/">TERMINAL - BENCH</a></li>
<li><a href="https://faichou.com/posts/llm-cache/">LLM 缓 存 机制：从计费到 原 理 • FaiChou's blog</a></li>

</ul>
</details>

**标签**: `#Google Gemini`, `#LLM release`, `#AI agents`, `#software engineering`, `#benchmarks`

---

<a id="item-5"></a>
## [微软为 Windows 引入 RDMA over USB4，多台 PC 可合跑一个大模型](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

微软发布了 Windows 上 RDMA over USB4 的开发者预览版，用户只需用普通 USB4 线缆连接两台或多台支持 USB4 的 PC，就能把一个本地 AI 模型拆分到多台机器上运行，共享内存与 GPU 算力。演示中三台搭载 AMD Ryzen AI Max+ 395 的机器以 4-bit 量化运行 Qwen3-235B-A22B，速度约为每秒 18.5 个 token，该功能将通过 Windows Insider 渠道推送。 这意味着普通用户和小型工作室无需购买专用网络设备（如雷雳集群、InfiniBand 或高速以太网交换机），就能运行远超单台消费级 PC 显存容量的大模型。它降低了本地私有化 AI 推理的硬件门槛，也预示着桌面 PC 未来可以像小型集群一样被池化使用。 RDMA（远程直接内存访问）允许一台系统读写另一台机器上已注册的内存区域，相比传统网络方式所需的操作系统与 CPU 参与要少得多；微软为此将 Windows 的 NetworkDirect API 适配到 USB4 链路，每台 PC 各自构成独立的 USB4 域，并通过点对点隧道相连。该功能目前仍是通过 Windows Insider 分发的开发者预览版，约每秒 18.5 token 的速度很大程度上取决于具体硬件、模型规模和所使用的 4-bit 量化方式。

telegram · zaihuapd · 11月21日 06:13

**背景**: RDMA 是数据中心网络中长期使用的技术，它在数据传输时绕过 CPU 和操作系统内核，从而大幅降低延迟与开销；这次它被用于两台 PC 之间的普通 USB4 线缆连接。Qwen3-235B-A22B 是阿里巴巴开源的混合专家（MoE）模型，总参数约 2350 亿，但每次前向计算仅激活约 220 亿参数，效率较高，可整体规模仍远大于单块消费级 GPU 的显存容量。4-bit 量化把模型权重压缩到每个约 4 比特，使显存需求大幅下降，从而让如此大的模型可以在本地硬件上运行，代价是精度会有所损失。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/microsoftusbblog/introducing-rdma-over-usb4®-on-windows-run-larger-local-ai-models-across-pcs/4574602">Introducing RDMA over USB 4 ® on Windows : run larger local AI...</a></li>
<li><a href="https://www.techpowerup.com/355062/microsoft-brings-rdma-over-usb4-to-windows-11-for-daisy-chained-pcs">Microsoft Brings RDMA over USB 4 to Windows 11 for... | TechPowerUp</a></li>
<li><a href="https://openmodeldrops.com/models/Qwen/Qwen3-235B-A22B/">Qwen 3 - 235 B - A 22 B by Qwen · facts, where to run, lineage</a></li>

</ul>
</details>

**标签**: `#RDMA`, `#USB4`, `#local AI`, `#Windows`, `#distributed inference`

---

<a id="item-6"></a>
## [显示器 USB 集线器让以太网下载速度下降 75%](https://blog.tymscar.com/posts/studiodisplayethernet/) ⭐️ 7.0/10

tymscar 的一篇排错博文记录了这样一件事：把以太网通过其 Studio Display 内置的 USB 集线器转接后，网络链路上增加的延迟足以让下载速度下降约 75%。罪魁祸首并不是显示器本身，而是集线器背后那块 USB 网卡——当笔记本无法足够快地确认数据包时，这块网卡会先缓存、继而丢包。 这是一个具体且可复现的案例，说明一个看似无害的配件——显示器的 USB 集线器——会悄悄拖垮网络性能，对任何通过扩展坞、集线器或 USB 网卡接入有线网络的人都很有参考价值。这篇文章把一种难以归因、行为不透明的降速现象，转化为可诊断的延迟与缓冲问题，而 Hacker News 上热烈的讨论也说明这类情况相当普遍、值得了解。 经由显示器的额外一跳增加了往返延迟，导致 TCP 确认返回过慢，以太网适配器中的缓冲区被填满，随后开始丢包；换用一块需要更少确认频率的适配器后问题解决。评论者还指出，USB 集线器必须对所有下行端口到达的数据包进行缓存与转发，这正是该路径会产生额外延迟的原因。

hackernews · soheilpro · 11月21日 10:36 · [社区讨论](https://news.ycombinator.com/item?id=50587875)

**背景**: TCP 是一种可靠的、面向连接的协议：接收方必须对数据做出确认，而发送方同时只能在途保留有限的数据量，因此吞吐量不仅取决于链路带宽，也同样取决于往返时间。USB 以太网适配器不走 PCIe 总线，而是挂在 USB 集线器控制器之后，因此通常延迟更高并依赖内部缓冲；当集线器加适配器的链路拖慢了 ACK，缓冲区就会溢出，随之而来的丢包会让 TCP 大幅退让。这就是为什么即使线路很快，高延迟或丢包仍会让它显得很慢。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50587875">My monitor was cutting my download speed by 75% | Hacker News</a></li>
<li><a href="https://superuser.com/questions/1592635/does-a-usb-c-ethernet-adapter-have-a-higher-latency-than-a-regular-ethernet-port">networking - Does a USB -C ethernet adapter have a higher latency ...</a></li>
<li><a href="https://assets.ctfassets.net/wcxs9ap8i19s/43yhFzdBFqdhC4WeAsxT5e/b6900fa2bacebb45c6ebe248739a358d/TCP_Network-Latency-and-Throughput_WhitePaper.pdf">TCP Network Latency and Throughput - assets.ctfassets.net</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者大多称赞这篇排错文章，但也对标题的表述提出异议：有人认为更准确的说法应是“我的 USB 网卡在削减我的下载速度”，显示器只是偶然因素。其他人则澄清了机制——额外延迟导致 ACK 不及时、适配器缓冲被填满并丢包——还分享了类似的离奇故障，例如 Ghostty 使用 io_uring 被计为 I/O 压力，从而限制了《博德之门 3》的 Vulkan 着色器编译；以及某款多千兆 SFP+ 模块向网卡宣称 10Gbps、却在铜缆侧协商到更低速率并悄悄丢包的情况。

**标签**: `#networking`, `#usb`, `#debugging`, `#hardware`, `#latency`

---

<a id="item-7"></a>
## [15 年经验的高级工程师失业两年，在 HN 发帖求助](https://news.ycombinator.com/item?id=50583761) ⭐️ 7.0/10

一位拥有 15 年经验、曾任职于《财富》50 强公司并掌握 C#/.NET/AWS 的美国高级软件工程师在 Hacker News 发帖求助：自 2025 年 1 月从一家中型保险科技公司离职后，他两年间求职屡屡碰壁，积蓄仅够支撑家庭 4 到 5 个月。他目前靠辅导数学维持生计，即将去披萨店做经理，因此向社区询问如何解释越来越长的履历空窗期，以及是否存在软件工程之外的“高薪”替代路径。 这条帖子以第一视角说明，即使是资深工程师，长期失业也可能持续很久，并暴露出多位评论者所说的“招聘正门已经坏掉”——投出数百份简历却几乎收不到回复。对求职者和招聘方而言，这说明 15 年经验和知名雇主背景已不再是面试机会的保证，而内推和如何叙述空窗期可能比技术能力本身更关键。 该工程师在得知这家 1000 多人的保险科技公司即将裁员后于 2025 年 1 月主动辞职，多位评论者指出这让他白白放弃了遣散费和失业救济，却什么也没换到。他表示自己仍能写代码并自学了 AI 工具，但认为招聘者看到最后任职日期就不再往下读；帖子中的建议从把他包装成 AI 产品的独立创始人，到把空窗期讲述为中性且面向未来的经历。

hackernews · LetThingsBeDiff · 11月20日 23:18

**背景**: “Ask HN”是 Hacker News 上的求助帖类型，通常能吸引大量在职工程师回复。在美国科技行业招聘中，几个月甚至数年的“履历空窗期”常被招聘人员和自动筛选系统视为负面信号，尽管裁员和照护家人都是常见原因；从离职到失业的这段经历往往会引来“为什么离开”的追问。“DMV 地区”指华盛顿特区—马里兰—弗吉尼亚一带，而“《财富》50 强”则指按营收计美国规模最大的企业之一的工作经历。

**社区讨论**: 主流观点认为，在裁员前主动辞职是一个代价高昂的错误，有评论者提醒后来者：如果怀疑自己可能被裁，千万不要直接辞职。也有人反对“必须解释空窗期”的前提，认为把它当作负面信息反而会招致怀疑，资深工程师更应把它叙述为自主项目或中性的生活事件。还有人描述了招聘“正门”失灵的现实：数百份申请几乎换不来回复，一位离开行业四年后回归的工程师最终只通过人脉拿到了录用通知。

**标签**: `#tech careers`, `#unemployment`, `#software engineering`, `#hiring`, `#HN discussion`

---

<a id="item-8"></a>
## [daraxonrasib 一线数据：未经治疗的转移性胰腺癌客观缓解率达 60.7%](https://event.eortc.org/ena2026/2026/11/20/metastatic-pancreatic-cancer-responds-well-to-initial-treatment/) ⭐️ 7.0/10

11 月 20 日，在巴塞罗那举行的 EORTC-NCI-AACR（ENA 2026）大会上，一项 late-breaking 口头报告显示：61 例既往未经治疗的转移性胰腺导管腺癌患者接受口服 daraxonrasib 200 mg 每日一次联合吉西他滨/白蛋白紫杉醇治疗后，确认客观缓解率为 60.7%，完全缓解率 8.2%，疾病控制率 90.2%，中位无进展生存 12.8 个月，12 个月总生存率 76.6%，中位随访 18.3 个月。该药是口服 RAS(ON) 多选择性抑制剂，而非仅针对单一突变的 KRAS G12C 药物。 转移性胰腺癌是最致命的实体瘤之一，单纯化疗下很少有患者能活过一年，因此一款一线口服靶向方案能取得两位数的完全缓解率，确实是一个值得关注的信号。若正在进行的 III 期试验能够验证这一获益，daraxonrasib 有望从后线治疗选项前移为一线联合治疗，覆盖大量携带 RAS 突变的患者。 该研究为单臂 I/II 期试验，没有化疗对照组，主要研究者明确表示疗效对比需要等待正在进行的 III 期试验结果；化疗的历史参照区间是 1 年生存率约 22%–48%（MPACT 试验 35%，mFOLFIRINOX 48%），因此 76.6% 这一数字不宜简单描述为“远高于化疗”。daraxonrasib 口服给药，剂量为 200 mg 每日一次，与仅针对 G12C 的抑制剂不同，它作用于活跃态（结合 GTP）的多种 KRAS/NRAS 突变蛋白以及野生型 RAS。

telegram · zaihuapd · 11月21日 11:24

**背景**: daraxonrasib（RMC-6236）由 Revolution Medicines 开发，是一种口服、非共价的“三复合物”抑制剂，作用于 KRAS、HRAS 和 NRAS 的活跃态（结合 GTP 的 RAS(ON) 形式），而不是失活的 GDP 结合状态。该药已于 2026 年 8 月 26 日获 FDA 批准，商品名 RASONQUE，用于既往接受过治疗的转移性胰腺癌，依据是 III 期 RASolute 302 试验中位总生存 13.2 个月对比 6.7 个月的结果。胰腺导管腺癌绝大多数病例由 RAS 突变驱动，这也是多选择性 RAS 抑制剂无需限定特定分子亚组即可广泛试验的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Daraxonrasib">Daraxonrasib</a></li>
<li><a href="https://www.drugs.com/rasonque.html">Rasonque ( daraxonrasib ): Uses, Dosage, Side Effects</a></li>
<li><a href="https://www.dana-farber.org/clinical-trials/24-533">RASolute 302: A Phase 3 Multicenter, Open-label, Randomized ...</a></li>

</ul>
</details>

**标签**: `#oncology`, `#pancreatic-cancer`, `#KRAS-inhibitor`, `#clinical-trials`, `#drug-approval`

---

<a id="item-9"></a>
## [美国陆军将在爱荷华州引爆巨量降解叠氮化铅](https://www.science.org/content/blog-post/detonating-huge-pile-lead-azide-really) ⭐️ 6.0/10

美国陆军正在爱荷华州米德尔敦（Middletown）的爱荷华陆军弹药厂分批次实施受控引爆，以销毁一大批已经降解的叠氮化铅；该厂属于“政府所有、承包商运营”（GOCO）模式，由 American Ordnance 负责日常运营。附近居民被建议撤离，并被警告爆炸可能扬起含铅颗粒的尘羽；science.org 的一篇化学博客文章报道了这次行动，在 Hacker News 上引发了关于这批危险物资为何会恶化到如此地步的热烈讨论。 这起事件是研究“老化弹药库存 + GOCO 承包模式”如何制造出一旦劣化便几乎无法安全补救的危险的典型案例。它的意义不限于这一座工厂：军事和工业场址中还存在类似的不稳定起爆药库存，而剩下的唯一选项往往就是让周边社区撤离、就地销毁。 叠氮化铅是用于起爆炸药雷管的起爆药，劣化后的材料对冲击和摩擦会变得敏感得多，因此这些容器无法在不冒整体殉爆风险的情况下被搬动、由机器人转移或化学中和。陆军最终选择就地销毁，并公开发布含铅粉尘警告和对附近居民的撤离建议。

hackernews · beginning_end · 11月21日 13:23 · [社区讨论](https://news.ycombinator.com/item?id=50588982)

**背景**: 叠氮化铅（Pb(N₃)₂）是一种白色结晶盐，通常由叠氮化钠与硝酸铅反应沉淀制得；由于能把很小的刺激可靠地放大为爆轰，它被广泛用作雷管中的起爆药。爱荷华陆军弹药厂属于“政府所有、承包商运营”（GOCO）设施——政府拥有厂区，私营公司依据绩效合同负责日常运营——其历史可追溯至二战，这意味着部分材料已在仓库中存放了数十年。起爆药会因受潮、温度循环和晶体生长而随时间劣化，使陈年库存的感度远高于新制备的材料。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lead(II)_azide">Lead (II) azide - Wikipedia</a></li>
<li><a href="https://hhs.iowa.gov/media/19822/download?inline">PLANNED LEAD AZIDE DETONATION FACT SHEET - hhs.iowa.gov</a></li>
<li><a href="https://en.wikipedia.org/wiki/Government-owned,_contractor-operated">Government - owned , contractor - operated - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上批评相关机构的管理方式：有人梳理了该厂从二战时期的政府设施到 1998 年转为承包商运营的历史，并将问题归咎于拿着高额合同却偷工减料的承包商；也有人反驳“派机器人搬走”的想当然建议，指出在炸药实验室里，标准做法是叫拆弹小组来就地销毁不稳定物料。另有评论以讽刺口吻将此比作现代社会机构“把问题藏到无可挽回、才在无解中等待意外发生”的通病，还有人质疑危险究竟何时被发现，与更早的中和合同时间线对不上。

**标签**: `#chemistry`, `#industrial-safety`, `#explosives`, `#military-contracting`, `#hacker-news-discussion`

---

<a id="item-10"></a>
## [OpenAI 指控 DeepSeek「蒸馏」美国模型，并游说国会限制中国 AI 企业](https://t.me/zaihuapd/45268) ⭐️ 6.0/10

OpenAI 在上周发给美国众议院「对华战略竞争」特别委员会的一份备忘录中称，中国 AI 初创公司 DeepSeek 通过「蒸馏」手法获取美国前沿模型的输出，用来训练其 R1 等模型，并将这种做法描述为对 OpenAI 等公司的「搭便车」。据报道 OpenAI 还称发现与 DeepSeek 员工相关的账号试图绕过访问限制，并正推动白宫和国会限制中国 AI 公司——这距离其向白宫提交类似政策提案、请求禁止 DeepSeek 等中国 AI 公司的产品在美国等地使用，大约过去了一年。 这一指控把中美 AI 竞争从模型能力比拼升级为政策层面的博弈，因为 OpenAI 不只是提出技术指控，而是在积极游说国会和白宫对中国 AI 公司施加限制。若这类主张获得支持，可能影响出口管制、API 访问规则以及美国实验室对模型的开放方式，进而波及全球依赖前沿 API 做开发的开发者。 这里的「蒸馏」指的是用另一个模型的输出（通常是其输出概率或生成的回答）而非原始数据来训练模型，从而得到更廉价、却能模仿更强教师模型的学生模型，这类做法在技术上很难被检测或封堵。该备忘录属于二手报道，未附原始文件，OpenAI 关于「与 DeepSeek 相关账号绕过访问限制」的说法也尚未得到独立核实。

telegram · zaihuapd · 11月21日 01:30

**背景**: 知识蒸馏是一种由来已久的机器学习技术，用于将大型「教师」模型的知识迁移到较小的「学生」模型；在大模型时代，它也包含用竞争对手模型生成的回答来训练模型。DeepSeek 发布了其第一代推理模型系列 R1（包括 R1-Zero 和 R1），凭借低成本下的强劲推理能力受到广泛关注；此外，基于其他开源模型构建的较小规模 R1「蒸馏版」也在 Hugging Face 和 Ollama 上分发。美国实验室的服务条款通常禁止利用其输出训练竞争模型，但由于输出可通过公开 API 和聊天界面广泛获取，实际执行起来相当困难。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://www.scientificamerican.com/article/what-is-ai-model-distillation-and-why-is-it-so-hard-to-stop/">What is AI model distillation, and why is it so hard to stop?</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-R1">deepseek -ai/ DeepSeek - R 1 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#OpenAI`, `#DeepSeek`, `#model distillation`, `#US-China tech competition`

---

<a id="item-11"></a>
## [美国收紧对马来西亚、泰国、新加坡先进芯片出口，印度欲承接外溢需求](https://t.me/zaihuapd/45269) ⭐️ 6.0/10

美国对出口至马来西亚、泰国和新加坡（以及印度尼西亚、巴西）的先进半导体新增了基于目的地的许可证要求，目的是防止 AI 芯片被转运至受限制的实体。与此同时，印度 AI 业界正把自己定位为这部分外溢需求的承接方：数据中心厂商 Yotta 称将在未来一年新增约 10 万块 GPU，相当于在印度现有算力基础上再增加约 10%。 此举封堵了中国企业获取英伟达高端加速器所剩的主要通道之一，进一步收紧了全球 AI 算力的地缘分布。它同时改变了算力建设选址的激励机制，让不在受限名单上的国家——其中最突出的是印度——有机会吸引原本会落地东南亚的投资与算力需求。 这些管制通过新增的基于目的地的许可证要求以及对混合货物的限制来实施，而非全面禁售，因此获得许可的出货仍可进行。印度的雄心面临现实约束：该国目前拥有 153 个数据中心，位居全球第 14；Yotta 计划的 10 万块 GPU 只能让全国算力提升约十分之一，而信实承诺投入至多 1100 亿美元、阿达尼承诺 1000 亿美元用于 AI 基础设施。

telegram · zaihuapd · 11月21日 02:01

**背景**: 美国商务部的出口管制框架按国家安全风险把国家分级：对中国、俄罗斯、伊朗实行严格的许可制度，对马来西亚等中间层级国家则相对宽松——马来西亚既承载了处于先进层级的美国阵营企业，也承载了主要处于成熟制程层级的中国企业。此次针对东南亚转运枢纽新增的基于目的地的许可证，意在阻止先进芯片被转道运往受关注的实体。Yotta 是印度的一家超大规模数据中心与云服务商，提供具备印度数据驻留能力的英伟达 H100 和 A100 实例，此前曾表示计划到 2025 年底扩展到 32768 块 GPU。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wccftech.com/the-u-s-shuts-chinas-access-to-advanced-chips-via-singapore-brazil-indonesia-malaysia-and-thailand-as-scott-bessent-gives-nvidia-10-days-to-show-it-did-not-goose-its-revenues/">The U . S . Shuts China's Access To Advanced Chips Via Singapore ...</a></li>
<li><a href="https://www.iseas.edu.sg/articles-commentaries/iseas-perspective/2026-37-neutrality-by-sector-malaysias-geoeconomic-alignment-under-anwar-by-amalina-anuar/">2026/37 “Neutrality by Sector: Malaysia ’s Geoeconomic Alignment...”</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#semiconductor export controls`, `#India`, `#GPU compute`, `#geopolitics`

---

<a id="item-12"></a>
## [特朗普：建数据中心的企业应向当地社区缴纳「分红」](https://t.me/zaihuapd/45272) ⭐️ 6.0/10

10 月 21 日，特朗普在 Truth Social 上表示，建设数据中心的企业若想获得当地欢迎，应向所在社区缴纳「分红」；他称曾极不受欢迎的数据中心在达成财务协议后变得极受欢迎。他还表示，大型数据中心必须自建发电设施，多余的电力应免费送给或卖给当地社区。 这番表态把数据中心选址问题推入全美政治议题，而此时 AI 基础设施扩张正与当地对电力、水资源的担忧发生碰撞，可能为「社区受益协议」、自建发电要求以及运营商成本上升定下基调。计划在美国建设大型 AI 数据中心园区的企业，若不作出类似让步，可能面临更严的审批和更强烈的本地反对。 该帖更像政治信号而非具体政策方案：其中没有说明「分红」的机制、比例或法律依据，也不清楚他指的是自愿的社区回馈金、税收协议，还是强制性要求。报道还提到相关企业的承诺——Anthropic 承诺将 5% 的股份投入公益基金，马斯克则承诺给每个美国孩子一股 SpaceX 股票。

telegram · zaihuapd · 11月21日 03:26

**背景**: AI 数据中心耗电量巨大，冷却也需要大量水资源，美国各地快速建设已引发围绕电网容量、电费和供水的本地争议。作为回应，一些运营商签署了社区受益协议、出资建设当地基础设施，或寻求自建或专属发电（包括天然气电厂和核电协议），以避免给公共电网带来压力。特朗普的表态正是在呼应这一趋势：把自建电力加上给社区分钱，说成是换取当地接纳的代价。

**标签**: `#data centers`, `#AI infrastructure`, `#energy policy`, `#tech regulation`, `#Trump`

---