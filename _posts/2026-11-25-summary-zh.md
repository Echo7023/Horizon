---
layout: default
title: "Horizon Summary: 2026-11-25 (ZH)"
date: 2026-11-25
lang: zh
---

> 从 30 条内容中筛选出 19 条重要资讯。

---

1. [Anthropic 称内部 Claude 模型发现 VP≠VNP 证明并给出 Lean 4 形式化](#item-1) ⭐️ 9.0/10
2. [Ternary Bonsai 2.5 27B：仅 5.9GB 的三元量化模型宣称接近前沿编程水平](#item-2) ⭐️ 8.0/10
3. [OpenAI 称 GPT-6 模型能通过写代码设计蛋白质微结合体](#item-3) ⭐️ 8.0/10
4. [GreyNoise 披露：攻击者利用 V8 伪随机数破解 Check Point 管理服务器并伪造管理员 Cookie](#item-4) ⭐️ 8.0/10
5. [Quad9 因法律限制撤出法国公共 DNS 服务](#item-5) ⭐️ 8.0/10
6. [Simon Willison 梳理十二个月内 LLM 的三大拐点](#item-6) ⭐️ 8.0/10
7. [GPT-6.2 Astra 自主破解 1808 年耶鲁素描本作者之谜](#item-7) ⭐️ 8.0/10
8. [vCenter 再曝 9.8 分免鉴权漏洞，此前已被零日利用](#item-8) ⭐️ 8.0/10
9. [泄露的 GTA 6 Xbox 版本借助 Wine 式重编译在 Windows 上运行](#item-9) ⭐️ 7.0/10
10. [Songe：用闲置算力持续训练本地 LLM 智能体的开源引擎](#item-10) ⭐️ 7.0/10
11. [火焰图与确定性虚拟机在性能分析中的争议](#item-11) ⭐️ 7.0/10
12. [博主称闭源 LLM 智能体服务于厂商而非用户](#item-12) ⭐️ 7.0/10
13. [GTA 6「Leonida」PC 重编译项目被 GitHub 下架](#item-13) ⭐️ 7.0/10
14. [开发者称 T3 Code 默认开启遥测并读取本机 Codex 与 Claude 凭证](#item-14) ⭐️ 7.0/10
15. [华为与高通达成覆盖 5G 与人工智能的多年广泛专利交叉许可协议](#item-15) ⭐️ 7.0/10
16. [SpaceX 与特斯拉董事会分别设立特别委员会审议合并事宜](#item-16) ⭐️ 7.0/10
17. [Anthropic 股价跌破 83 美元发行价，引发 AI 经济性争论](#item-17) ⭐️ 6.0/10
18. [李彦宏内部讲话：大模型开源意义不大，百度绝不抢开发者饭碗](#item-18) ⭐️ 6.0/10
19. [Anthropic CEO Dario Amodei 预测：AI 有望 10 年内攻克癌症等疑难病症](#item-19) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Anthropic 称内部 Claude 模型发现 VP≠VNP 证明并给出 Lean 4 形式化](https://t.me/zaihuapd/45345) ⭐️ 9.0/10

据报道，Anthropic 于 11 月 24 日公开了题为《VP ≠ VNP over every field》的论文及 Lean 4 形式化证明仓库，并称该结果由内部研究用 Claude 模型发现，论文与代码均由 AI 撰写。论文声称给出了哈密顿圈多项式的超多项式算术电路下界，据此推出 VP 是 VNP 的真子类，从而解决 Valiant 1979 年提出的代数复杂度猜想。 若该结果被验证，它将成为计算复杂性领域的里程碑，同时也是 AI 定理证明能力的有力展示，因为由机器发现一个悬置数十年的公开猜想证明，将改变研究界使用 AI 做数学的方式。同时，由于消息经由二手的 Telegram 频道传播而非同行评审渠道，这也会加剧外界对 AI 生成数学结论的审视。 该结论仅针对算术电路模型，因此并不解决经典的 P 与 NP 问题；仓库还称通过了三条标准公理的审计以及独立内核检查。关键在于，这一声明极为重大且目前仅来自 Telegram 单一来源，因此仍需复杂性理论学者的独立验证以及从零开始成功构建 Lean 4 证明。

telegram · zaihuapd · 11月24日 12:18

**背景**: 算术电路是计算多项式的标准模型：电路以变量或数值为输入，并通过加法与乘法组合已计算出的表达式。1979 年 Valiant 引入了 VP 与 VNP 这两个代数复杂性类，作为 P 与 NP 的类比，并猜想 VP 是 VNP 的真子类，同时证明永久式（以及有向哈密顿圈多项式）在投影归约下是 VNP 完全的。Lean 4 是基于依赖类型论的证明助手，证明的每一步都必须经内核机械检验，因此一个能够通过编译的形式化证明不会留下含糊其辞的空间。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Arithmetic_circuit_complexity">Arithmetic circuit complexity - Wikipedia</a></li>
<li><a href="https://mathworld.wolfram.com/ValiantsConjecture.html">Valiant's Conjecture -- from Wolfram MathWorld</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean ( proof assistant ) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI for science`, `#theorem proving`, `#computational complexity`, `#Lean 4`, `#Anthropic`

---

<a id="item-2"></a>
## [Ternary Bonsai 2.5 27B：仅 5.9GB 的三元量化模型宣称接近前沿编程水平](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 8.0/10

PrismML 发布了 Ternary Bonsai 2.5 27B，这是 Bonsai 系列中最大的模型，它是一个由 Qwen3.8-27B 衍生而来的三元（约 1-bit/Q2 GGUF）量化模型，架构保持不变，体积仅 5.9GB。官方称其在该体积下显著增强了智能体编程、多轮工具调用和多步任务执行能力，用户则报告其在 SWE-bench Verified 上接近前沿模型的表现。 如果这些说法成立，那么一个约 6GB、可轻松装进 24GB 统一内存的模型，就意味着普通 Mac Mini 或笔记本也能离线运行真正可用的编程智能体，这将动摇“智能体编程必须依赖数据中心级硬件”的假设。同时，它也让“小模型的进步是真实能力提升还是针对基准的定向优化”这一争论更加尖锐。 该模型保留了 Qwen3.8-27B 的混合注意力架构，并以 Q2 GGUF 量化格式分发；一位社区测试者在配备 24GB 内存的 Mac Mini M5 Pro 上测得生成速度约 22–25 tokens/s、提示处理速度 222.9 tokens/s、首 token 延迟 2.12 秒，并且内存还能轻松容纳约 128k 上下文。需要注意的是，SWE-bench Verified 只覆盖一小部分 Python 仓库问题，而且其对比对象是规模大得多的前沿模型，而非同等体量的量化基线模型。

hackernews · b0m · 11月24日 20:08 · [社区讨论](https://news.ycombinator.com/item?id=50633922)

**背景**: 三元量化是一种极端的权重压缩方式，每个权重只取三个值（−1、0、+1），有时被称为 1.58-bit，它能大幅降低内存占用，但由于权重和激活值中的离群点会损害精度，实际应用难度很大。SWE-bench Verified 是 AI 编程智能体领域被引用最多的基准，它给出 Python 仓库中的真实 GitHub issue，要求模型生成能通过项目测试套件的补丁。Bonsai 是 PrismML 推出的这类激进量化模型系列，其中 27B 版本专门面向长时间运行的智能体工作流。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.prismml.com/models/bonsai-2-5-27b">Ternary Bonsai 2.5 27B - Bonsai - docs.prismml.com</a></li>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2.5 27B: Powering ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/1.58-bit_large_language_model">1.58-bit large language model - Wikipedia</a></li>
<li><a href="https://www.swebench.com/">SWE-bench Leaderboards</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论兼具实测热情与理性怀疑：一位评论者贴出了具体吞吐数据，并展示了在 8GB 内存级别的 M3 MacBook Air 上运行 1-bit 模型生成的“鹈鹕”示例；另一位则认为其 SWE-bench Verified 得分大致相当于某个大得多的前沿模型，并追问这其中有多少是刷榜、有多少是基准本身在移动、又有多少是小模型能力滞后约半年后的真实进步。还有人直接要求给出与同等规模的热门模型量化版本的正面对比。

**标签**: `#LLM quantization`, `#ternary models`, `#local inference`, `#small language models`, `#SWE-bench`

---

<a id="item-3"></a>
## [OpenAI 称 GPT-6 模型能通过写代码设计蛋白质微结合体](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) ⭐️ 8.0/10

OpenAI 报告称，在给定五个靶标蛋白的三维结构并标注期望的结合位点后，GPT-6.2 能够自行编写代码生成候选微结合体（minibinder）的三维设计，且未使用专门的蛋白质 AI 模型；实验室测试在全部五个靶标上都观察到了结合的迹象。OpenAI 将这一结果描述为通用模型自发涌现出的蛋白质设计能力，而非依赖专门构建的结构生物学系统。 如果通用大语言模型仅靠编写代码就能完成有意义的蛋白质从头设计，将显著降低 AI 辅助生物药与药物发现研究的门槛，并模糊通用推理模型与领域专用结构预测工具之间的界限。这也引发了另一层疑问：这类成果究竟应归功于语言模型本身，还是仍离不开下游使用的专用模型。 GPT-6.2 只负责生成三维骨架设计，氨基酸序列由专用模型 SolubleMPNN 给出，随后还用其他蛋白质模型筛选出预测能按设计折叠并在预期位点结合的候选。相关证据来自 OpenAI 单方面发布的一篇报告，仅显示五个靶标上的实验室结合信号，并非经过同行评审、与现有设计流程对照的基准测试。

hackernews · acossta · 11月24日 21:02 · [社区讨论](https://news.ycombinator.com/item?id=50634658)

**背景**: 微结合体（minibinder）是通过从头设计得到的小型蛋白质，能够紧密结合特定靶标蛋白，因其在治疗药物和科研试剂方面的潜力而成为 AI 蛋白质设计的常见目标。主流流程通常把问题拆成两步：先用 RFdiffusion 之类的结构生成模型提出三维骨架，再用 ProteinMPNN 或其可溶性变体 SolubleMPNN 等序列设计网络为该骨架分配合适的氨基酸。领域专用模型还被用于按预测的折叠稳定性和结合能力筛选设计，这正是 OpenAI 报告中“分工”问题成为争议焦点的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/">GPT-6 models demonstrate intrinsic protein-design ... - OpenAI</a></li>
<li><a href="https://elifesciences.org/reviewed-preprints/96154">De novo- designed minibinders expand the synthetic biology sensing...</a></li>
<li><a href="https://www.nature.com/articles/s44222-025-00349-8">AI-driven protein design - Nature Reviews Bioengineering</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论意见分歧明显：一位曾在 Baker 实验室攻读博士的研究者认为这完全合理，并把蛋白质与语言模型的“原生”融合视为必然趋势；但也有人指出，序列即结构，因此 GPT-6.2 主要贡献的是脚手架和代码，真正的蛋白质设计是 SolubleMPNN 完成的。还有人因 OpenAI 的推广立场而质疑其表述，并提到存在竞争性的开放权重生物学模型，以及有报道称 Claude 曾在大规模蛋白质序列上训练。

**标签**: `#AI for biology`, `#protein design`, `#LLMs`, `#OpenAI`, `#scientific research`

---

<a id="item-4"></a>
## [GreyNoise 披露：攻击者利用 V8 伪随机数破解 Check Point 管理服务器并伪造管理员 Cookie](https://www.greynoise.io/blog/check-point-security-management-servers-intrusion-campaign) ⭐️ 8.0/10

GreyNoise 发布研究，记录了一场针对 Check Point 安全管理服务器的持续入侵活动（编号 GT13）。攻击者随后转向一台已被攻陷的 HFS 服务器，滥用其 loginSrp1 登录端点——该端点返回的签名会话 Cookie 中的“sid”值取自 JavaScript 的 Math.random()。攻击者通过连续多次登录收集到足够多的输出，重建了 Node.js V8 伪随机数生成器的内部状态，从而还原出 HFS 会话 Cookie 的签名密钥，并伪造出签名的管理员会话 Cookie。 Check Point 安全管理服务器是组织防火墙策略、网关配置与日志的中央控制点，因此一旦攻击者持有一个伪造的管理员会话，就相当于掌控了整个安全边界。这一案例也典型地说明：当非密码学安全的伪随机数被用于承载安全敏感数值时，攻击者仅凭观测到的输出即可反推其状态，无需内存泄漏或密钥泄露。 GreyNoise 表示，攻击者在攻陷 HFS 服务器之前就已获得对受害 Check Point 安全管理服务器的访问权限，但无法确定其初始入侵的时间与方式；报告还提到多个受害客户之间可能存在与 CVE-2026-16232 的关联。该攻击之所以成立，是因为 V8 的 Math.random()采用的是快速但非密码学安全的算法，其状态可由少量连续输出重建——问题并非出在伪随机数本身，而在于用它来生成会话标识和签名材料。

hackernews · louiereederson · 11月24日 16:32 · [社区讨论](https://news.ycombinator.com/item?id=50630594)

**背景**: Check Point 安全管理服务器是管理员用来定义防火墙规则并向各网关下发策略的设备，攻陷它的价值远高于攻陷单台防火墙。JavaScript 的 Math.random()在规范中被明确定义为返回一个由具体实现决定的伪随机数，而 V8 使用 xorshift128+实现，这是一种速度快但并不以抗预测为目标的生成器。Web 应用常因便利而用 Math.random()生成令牌、会话 ID 或密钥，这使得能够观测到足够多输出的攻击者可以重建生成器的内部状态，并预测其后的全部输出——包括用于签名的密钥。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.greynoise.io/blog/check-point-security-management-servers-intrusion-campaign">An Active Intrusion Campaign Against Check Point Security ...</a></li>
<li><a href="https://v8.dev/blog/math-random">There’s Math . random (), and then there’s Math . random () · V 8</a></li>
<li><a href="https://tech.yahoo.com/cybersecurity/articles/control-tower-left-unguarded-check-094326324.html">The Control Tower Left Unguarded: Check Point ’s Management ...</a></li>

</ul>
</details>

**社区讨论**: 评论者对这次重建伪随机数状态的技术深度印象深刻，不少人认为这是关于“非密码学随机数”的一个古老却反复出现的教训。一种得到广泛认同的观点是：与其指望成千上万个应用都正确使用 Math.random()，不如让这个函数本身至少具备一定的安全性；也有人推测，LLM 驱动的自动化很快会让技术能力远不如国家级攻击者的犯罪分子也能发起此类攻击；还有读者质疑，为何这些受害组织的管理服务器会暴露在互联网上。

**标签**: `#security`, `#vulnerability-exploitation`, `#prng`, `#nodejs`, `#check-point`

---

<a id="item-5"></a>
## [Quad9 因法律限制撤出法国公共 DNS 服务](https://quad9.net/news/blog/quad9-service-deactivation-in-france/) ⭐️ 8.0/10

Quad9 已停止为法国用户提供公共 DNS 服务，来自法国网络发往其 9.9.9.9 解析器的查询现在会返回 REFUSED 响应，并附带扩展 DNS 错误，称该服务因法国法律限制而不可用。 这使一个广受欢迎、以安全和隐私为重点的解析器退出一个主要欧盟国家，表明国家法律命令可能迫使全球公共 DNS 提供商在合规与退出之间做出选择。依赖 Quad9 的法国用户将失去其恶意软件过滤和加密 DNS 选项，除非改用其他解析器或使用变通方案。 Quad9 通过不同地址和主机名提供过滤与未过滤服务，并支持明文 DNS、DoT 和 DoH；一位社区成员已搭建代理，为法国用户通过上述协议将查询转发至 Quad9，并同时支持 IPv4 和 IPv6。该拒绝响应由 Quad9 自己的解析器通过 REFUSED 和 EDE 代码 18 生成，而非本地网络拦截，且有报道将该争议与法国的网站封锁和盗版执法联系起来。

hackernews · farrokhi · 11月24日 08:33 · [社区讨论](https://news.ycombinator.com/item?id=50625384)

**背景**: DNS 是互联网的命名系统：解析器把 example.com 这样的域名转换为 IP 地址，大多数在线活动都依赖它。Quad9 是一款免费的公共递归解析器，以拦截已知恶意域名的查询而闻名，并提供 DoH 和 DoT 等加密 DNS 传输，以保护查询免受篡改和监视。由于公共解析器跨境运营却必须服从当地法律，各国可以强制它们封锁域名或停止为当地用户服务；法国拥有活跃的网站封锁制度。这一事件契合了围绕 DNS 隐私、抗审查能力以及谁控制公共解析基础设施的更大争论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Quad9">Quad9 - Wikipedia</a></li>
<li><a href="https://quad9.net/service/service-addresses-and-features/">Service Addresses & Features | Quad9</a></li>
<li><a href="https://www.bleepingcomputer.com/news/technology/google-unveils-dns-over-https-doh-plan-mozillas-faces-criticism/">Google Unveils DNS -over-HTTPS (DoH) Plan, Mozilla's Faces Criticism</a></li>

</ul>
</details>

**社区讨论**: Hacker News 评论者用 dig 输出确认了服务中断，显示 REFUSED 以及提及法国法律限制的 EDE 消息，还有一位用户为法国用户提供了可作为即插即用替代的开放代理。其他人则质疑，如果 Quad9 在法国没有办公室或人员，为何还要遵守要求；同时，指向早前讨论和 TorrentFreak 更新的链接将该事件置于更广泛的盗版封锁与审查争论之中。

**标签**: `#DNS`, `#privacy`, `#internet censorship`, `#France`, `#Quad9`

---

<a id="item-6"></a>
## [Simon Willison 梳理十二个月内 LLM 的三大拐点](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 8.0/10

Simon Willison 发布了一篇随笔，延伸自他在 AI Engineer Code Summit 的主题演讲，认为在 2025 年 11 月至 2026 年 11 月之间，LLM 与编码智能体的能力跨越了三个明显的拐点。他把时间线锚定在 2026 年 11 月 24 日，即 Claude Opus 4.5 发布一周年；他称这是一个“具有分量的模型”，因为它是第一个在 Claude Code 中默认输出基本正确的模型。 这篇文章没有停留在又一张基准测试表，而是为过去一年划出了分期：哪些模型代际真正改变了日常编码工作流，以及各自出现的时间点。这种框架能帮助团队判断可靠性与自主性提升的速度，并对下一代编码智能体形成合理预期。 第一个拐点是 2025 年 11 月：Claude Opus 4.5 与 OpenAI 的 GPT-5.1 Instant、GPT-5.1 Thinking、GPT-5.1-Codex 及 Codex-Max 相继发布，使 Claude Code 和 Codex 双双变得可靠好用。第二个拐点是 2026 年中期出现的“Fable 级模型”：Claude Fable 5 是被“去锋芒化”的 Claude Mythos，曾因美国出口管制被短暂下架直至 7 月 1 日；Willison 将其定义为只要你能定义目标并提供必要工具、就能靠蛮力解决问题的模型。这篇摘录在第三个拐点揭晓前就中断了，而更广的搜索结果也显示，Opus 4.5 现已在 Claude API 上被弃用，由 Opus 5.5 取代。

rss · Simon Willison · 11月24日 23:02

**背景**: 编码智能体指的是被赋予了工具（文件系统、shell、测试运行器、浏览器等）的大语言模型，因此它能在代码库上执行多步操作，而不只是给出代码片段。Claude Code 是 Anthropic 的智能体式命令行工具，于 2025 年 2 月 24 日随 Claude 3.7 Sonnet 一同推出，到 Opus 4.5 发布时大约只有九个月大。Simon Willison 是资深开发者，也是 LLM 工具领域的高产作者；AI Engineer Code Summit 是旧金山的一场会议，其 2026 年的演讲录像于 2026 年 11 月 10 日发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.engineer/code/2026">AI Engineer Code Summit 2026 Recordings: AI Engineering ...</a></li>
<li><a href="https://www.anthropic.com/news/claude-opus-4-5">Introducing Claude Opus 4.5 \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/models/opus-4-5/overview">Claude Opus 4.5 - Claude Platform Docs</a></li>

</ul>
</details>

**标签**: `#LLM`, `#coding agents`, `#AI engineering`, `#Claude Opus`, `#developer tools`

---

<a id="item-7"></a>
## [GPT-6.2 Astra 自主破解 1808 年耶鲁素描本作者之谜](https://simonwillison.net/2026/Nov/24/astra-historical-mystery/) ⭐️ 8.0/10

历史学教授 Mark Humphries 记录称，GPT-6.2 Astra 在极少提示下，仅用 22 分钟便利用公开的一手和二手资料，自主确认了耶鲁大学拜内克图书馆所藏一本 1808 年匿名素描本的作者。它还在此过程中发现了一份鲜为人知的纸质档案来源，而这份来源本身对加拿大史和毛皮贸易史研究具有重要价值。 这提供了一个由历史学教授记录的具體案例，说明 LLM 智能体能够开展真正的新颖研究并产出新的史料，而不只是辅助检索或写作。对 AI 研究工具开发者和历史学者而言，这是一个信号：能够以人类难以企及的速度完成档案工作的智能体可能很快出现。 Astra 发现了一则日记记载：沙博子爵（vicomte de Chabot）曾在素描本所提日期前五天到访附近一条河流，并据此推测，只能向克利夫兰州立大学订购的沙博旅行日志可以证明素描本出自其手。该叙述是 Humphries 发布在 Substack 上的单一案例研究，而非经过同行评审的论文；Humphries 认为，历史学者面临的“深蓝时刻”危机可能较温和，因为历史学强调随时代不断重新解释过去，且历史写作更接近哲学与文学，而非数学那样追求单一普遍真理。

rss · Simon Willison · 11月24日 16:53

**背景**: GPT-6.2 Astra 是 OpenAI 于 2026 年 11 月 17 日发布的前沿模型，同日还发布了更高效的 GPT-6.2 Sol；OpenAI 将 Astra 定位为处理最困难项目的模型，能力涵盖浏览和计算机使用。自主智能体是指能够在极少人工输入下感知环境、采取行动并追求目标的系统，这正是 Humphries 所描述的工作模式。这本 1808 年素描本藏于耶鲁大学拜内克图书馆，并已被数字化；“深蓝”则指 IBM 在 1997 年击败加里·卡斯帕罗夫的计算机，常被用作机器在某一领域超越人类的代称。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-2-astra-sol/">Introducing GPT-6.2 Astra and Sol | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Autonomous_agent">Autonomous agent - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI research agents`, `#LLM applications`, `#autonomous agents`, `#historical research`, `#GPT-6.2`

---

<a id="item-8"></a>
## [vCenter 再曝 9.8 分免鉴权漏洞，此前已被零日利用](https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html) ⭐️ 8.0/10

Broadcom 为 VMware 产品线的 23 个漏洞发布补丁，其中最严重的是 vCenter 目录服务（vmdir）中的鉴权绕过漏洞 CVE-2026-123903，CVSS 评分高达 9.8：只要攻击者能通过网络访问 vCenter，就能绕过认证、未授权进入系统。该漏洞在补丁发布前几天就已经被作为零日漏洞在野利用。 vCenter 是 VMware 虚拟化环境的中央控制平面，一旦在此处出现免鉴权绕过，攻击者就可能触及该数据中心内所有受管的 ESXi 主机、虚拟机和存储的凭据。由于该漏洞已被实际利用且无需任何凭据，运行 vCenter 的防守方（包括大量企业和政府环境）必须立即修补，而不能等待例行维护窗口。 该漏洞位于 vmdir 组件中，按照 Broadcom 公告的说法，任何能通过网络访问 vCenter 的恶意行为者都可以利用它；修复补丁是作为 23 个 VMware 漏洞补丁批次的一部分发布的，而非单独发布。它也是 2026 年披露的一系列 vCenter 鉴权绕过漏洞中的最新一个，此前还有 CVE-2026-123890 和更早的 CVE-2026-59309，这表明攻击者正在持续针对同一攻击面进行挖掘。

telegram · zaihuapd · 11月24日 14:50

**背景**: vCenter Server 是 VMware 的虚拟基础设施管理平台，管理员通过它配置 ESXi 主机、创建虚拟机、管理集群并处理单点登录，因此攻陷 vCenter 基本等同于攻陷整个虚拟化环境。VMware Directory Service（vmdir）是支撑 vCenter 内嵌身份体系（例如 vsphere.local 域）的基于 LDAP 的目录服务，鉴权与单点登录都依赖它，因此它成了攻击者寻找鉴权绕过漏洞的高价值目标。鉴权绕过漏洞是指攻击者无需窃取口令即可完全跳过登录校验的缺陷；零日漏洞则是指在厂商提供补丁之前就已被利用的漏洞，这正是本次披露格外紧急的原因。CVSS 9.8 属于“严重”区间，意味着该漏洞可远程触达、利用复杂度低且无需认证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html">VMware vCenter Hit by Another Critical 9.8-Rated Auth Bypass ...</a></li>
<li><a href="https://www.rapid7.com/blog/post/etr-cve-2026-123890-critical-authentication-bypass-vmware-vcenter/">CVE-2026-123890: Critical Authentication Bypass in VMware vCenter</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zero-day_exploit">Zero-day exploit</a></li>
<li><a href="https://knowledge.broadcom.com/external/article/326305/how-to-export-vmdir-information-from-vce.html">How to export VMDir information from vCenter Server Appliance</a></li>

</ul>
</details>

**标签**: `#security`, `#vmware`, `#vcenter`, `#vulnerability`, `#zero-day`

---

<a id="item-9"></a>
## [泄露的 GTA 6 Xbox 版本借助 Wine 式重编译在 Windows 上运行](https://twitter.com/raul_bs3/status/2125213756238291075) ⭐️ 7.0/10

社区逆向工程项目（主要是 xcl 和 Victory）据称已利用类似 Wine 的重编译与兼容层技术，让泄露的 GTA 6 Xbox 版本在 Windows PC 上运行起来。相关帖子获得约 290 分和 367 条评论，评论者认为这是一次真实但尚粗糙的兼容性尝试，而非骗局。 这一成果说明现代 Xbox 主机与 Windows PC 之间的界限已非常模糊，从而降低了把主机独占游戏做成非官方原生移植版本的技术门槛。它也加剧了发行商面临的法律与商业难题：一份泄露且未加保护的二进制文件，可能在官方 PC 版上市前很久就能在 PC 上运行。 据评论者介绍，泄露的 Xbox 二进制文件没有特殊的 DRM 或混淆保护，因此难点在于兼容层与图形转译，而非代码保护。这些项目采用类似 Wine 的思路；类似的 Xbox2Windows 研究则把选定的 x64 机器码翻译成 C++，并把 gfx1013 着色器转译为桌面端 DXIL。

hackernews · andrem · 11月24日 13:19 · [社区讨论](https://news.ycombinator.com/item?id=50627783)

**背景**: 静态重编译是一种逆向工程技术：把游戏的原始机器码翻译成 C 或 C++ 源码，再编译成面向另一平台的原生可执行文件；它与模拟器不同，运行时不需要解释器。相比之下，Wine 是一个兼容层，通过重新实现 Windows API 让 Windows 二进制程序能在其他系统上运行。现代 Xbox Series X|S 主机采用 x64 AMD 处理器和 AMD RDNA 2 图形硬件，与 PC 硬件非常接近，这正是 Xbox 游戏二进制比 PlayStation 或更早世代主机游戏更容易搬到 Windows 上的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/R0Y00/Xbox2Windows">GitHub - R0Y00/Xbox2Windows: Static recompilation research for...</a></li>
<li><a href="https://www.denis-iakimenko.com/blog/reverse-engineering-decompilation-ports">Reverse Engineering Games — Decompilation and Static ...</a></li>
<li><a href="https://recompendium.com/en/consola/xbox/">Xbox games on PC: recompilations, native ports, and ...</a></li>

</ul>
</details>

**社区讨论**: 评论者深入讨论了技术路径：由于现代 Xbox 硬件接近 PC，且泄露的二进制没有 DRM 或混淆，剩余工作主要是兼容性与图形，这正是 xcl 和 Victory 在做的事。也有人争论其后果——一方认为考虑到 GTA 6 巨额盈利以及官方 PC 版终将推出，此事不会严重冲击游戏制作；另一方则担忧未来游戏会把关键组件放在云端，专门用来阻止反编译。

**标签**: `#game-reverse-engineering`, `#compatibility-layers`, `#wine`, `#recompilation`, `#gta-6`

---

<a id="item-10"></a>
## [Songe：用闲置算力持续训练本地 LLM 智能体的开源引擎](https://github.com/sous-labs/songe) ⭐️ 7.0/10

Songe 是 sous-labs 组织下的一个 GitHub 项目，定位为训练引擎，目标是利用机器上原本闲置的算力来持续改进本地 LLM 智能体。它本身既不是模型也不是运行时，而是作为训练层与用户已在本地运行的智能体配合使用。 目前大多数本地智能体方案都是静态的：下载一个模型，通过 Ollama 之类的工具运行，它永远不会从自己的失败中学习。如果一套轻量的后台训练循环能在消费级硬件上奏效，个人开发者和小团队就无需租用云端 GPU 也能改进智能体，这也正好呼应了当前关于智能体自我进化系统的研究热潮。 该项目仍处于早期阶段，公开信息很少：没有公布基准测试结果，没有说明硬件要求，文档也尚未明确改进效果如何衡量，以及采用的是哪种训练方式（微调、偏好优化还是基于回放的纠错）。"闲置算力"这一表述也暗示训练是在后台以数小时甚至数天的跨度进行，而非一次性集中完成。

hackernews · bluepeter · 11月24日 15:03 · [社区讨论](https://news.ycombinator.com/item?id=50629231)

**背景**: 本地 LLM 智能体指的是完全在你自己的机器上运行大模型的系统——通常通过 Ollama、llama.cpp 之类的运行时——并用它来调用工具、编辑文件或控制电脑。由于模型权重就在本地磁盘上，理论上你可以自行微调或改造它，这正是 Songe 这类"训练引擎"的用武之地。这类自我改进循环的基本思路是：捕获智能体的错误或成功案例，把它们转化为训练信号并反馈回去，使模型下次遇到类似情况时能正确处理。过去这通常意味着需要专属 GPU 时间和机器学习专业知识，因此"利用空闲算力顺手完成"这一卖点才是真正新颖之处。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/sous-labs/songe/tree/main/.github">songe/.github at main · sous-labs/songe · GitHub</a></li>
<li><a href="https://githubsignals.io/repo/sous-labs/songe/">sous-labs/songe — GitHub Signals</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2026/06/self-improving-loops/">Self-Improving Loop: How to Build AI Agents That Actually Learn</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论者既有兴趣也持怀疑态度，帖子获得 182 分和 59 条评论。不少人要求给出具体数字——周末训练一次或每个"dream epoch"能带来多少提升；也有人希望文档中能附上一个完整的改进判定案例，说明系统究竟如何评估改进，以及它是从自我纠正还是从用户纠正中学习。一位评论者询问它能否在没有 GPU、通过 Ollama 运行小型 Qwen 模型的普通 Windows 机器上工作，还有人提出了类似 SETI@home 的分布式版本设想。

**标签**: `#local-llm`, `#training-engine`, `#idle-compute`, `#open-source-tools`, `#agent-self-improvement`

---

<a id="item-11"></a>
## [火焰图与确定性虚拟机在性能分析中的争议](https://fzakaria.com/2026/11/12/worshipping-at-the-altar-of-brendan-gregg) ⭐️ 7.0/10

2026 年 11 月 12 日发布的一篇技术博客及随后的 Hacker News 讨论重新审视了火焰图和确定性虚拟机作为性能分析工具的价值，评论者对其在多线程和异步系统中的适用性提出质疑。 火焰图是 CPU 性能分析的常用可视化手段，但它在跨线程依赖和异步关键路径上的盲区可能误导调试高吞吐服务的工程师；这场讨论指向记录回放、追踪和请求上下文等补充手段。 评论者指出，所讨论的确定性虚拟机是单线程的，这可能限制其对高并发流水线的保真度，并将其与 rr 记录回放工具进行比较；还有人询问，若不把请求上下文嵌入框架代码，这类分析如何还原 C++ 协程、纤程或 future 的关键路径。

hackernews · kqr · 11月24日 10:50 · [社区讨论](https://news.ycombinator.com/item?id=50626413)

**背景**: 火焰图由 Brendan Gregg 发明，用于可视化采样得到的调用栈：每个矩形代表一个栈帧，其宽度反映该栈帧在样本中出现的频率，而不是经过的时间。确定性虚拟机和记录回放系统旨在让执行过程可复现，从而能够可靠地重跑并检查性能问题和缺陷；讨论中提到的 Antithesis 和 rr 就是这类系统的例子。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.brendangregg.com/flamegraphs.html">Flame Graphs - Brendan Gregg Analyze Java performance on Arm servers using flame graphs Flamegraph handles multi-thread program abnormality Generate Java flame graphs using async-profiler | Arm ... What Is Flamegraph? Definition & Examples - nhimg.org Java Async Profiler Flame Graph - Stack Overflow</a></li>
<li><a href="https://dl.acm.org/doi/10.1145/2007477.1952686">Performance profiling of virtual machines | ACM SIGPLAN Notices</a></li>

</ul>
</details>

**社区讨论**: 讨论整体上对确定性虚拟机和可复现分析抱有兴趣，但多位评论者对火焰图用于多线程分析持怀疑态度，并担心单线程虚拟机会遗漏跨线程效应。还有人将其与 rr 和 Antithesis 类比，询问异步关键路径分析，并讨论了 Nvidia 的“光速”性能文化以及睡眠/停顿剖析的权衡。

**标签**: `#performance-analysis`, `#flamegraphs`, `#deterministic-vm`, `#observability`, `#systems-profiling`

---

<a id="item-12"></a>
## [博主称闭源 LLM 智能体服务于厂商而非用户](https://michaelharley.net/posts/2026/11/01/llm-agents-work-for-their-parent-companies-not-for-you/) ⭐️ 7.0/10

michaelharley.net 上的一篇博文指出，闭源 LLM 智能体最终服从的是其母公司制定的政策，而不是付费使用它们的用户；作者用一个具体例子说明：Claude 拒绝绕过 Bandcamp 的反爬虫限制，却仍然愿意下载 YouTube 上的歌曲。该文在 Hacker News 上获得 912 分和 386 条评论，成为近期讨论最激烈的 AI 政策话题之一。 这篇文章触及智能体生态中的核心矛盾：用户希望智能体像忠诚的代理人一样行事，而厂商必须执行使用政策、遵守网站服务条款并管控法律与声誉风险。这一矛盾的解决方式将决定商业智能体在开放网络上能做什么，并影响用户信任、产品普及以及围绕智能体义务的新兴监管讨论。 文章举出的具体案例被批评者认为自相矛盾：一方面尊重 Bandcamp 明确的反 LLM 意愿，另一方面却愿意抓取不会给艺术家带来任何收益的 YouTube 歌曲。评论者还指出，如果模型只要用户要求就无视网站规则，长期来看很可能招致封禁、法律诉讼，反而削弱其对用户的实际价值。

hackernews · surprisetalk · 11月24日 12:40 · [社区讨论](https://news.ycombinator.com/item?id=50627340)

**背景**: LLM 智能体是指在语言模型之外附加工具调用与规划能力的系统，可以代替用户浏览网页、调用 API 并完成多步骤任务。由于这类智能体是自主行动的，“它究竟听谁的”就成了现实问题：是听用户的、听模型厂商的使用政策，还是听目标网站的服务条款。此语境下的“AI 对齐”指的是让这类系统真正遵循其开发者与用户所意图的目标和约束；也有评论者建议借用律师、医生和财务顾问对客户所负的受托责任（fiduciary duty）标准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_alignment">AI alignment - Wikipedia</a></li>
<li><a href="https://developer.nvidia.com/blog/building-your-first-llm-agent-application/">Building Your First LLM Agent Application | NVIDIA Technical Blog</a></li>
<li><a href="https://terms.law/Trading-Legal/guides/ai-fiduciary-duty.html">AI Fiduciary Duty: SEC Robo-Adviser Compliance | Terms.Law</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论呈两极分化：多位评论者认为拒绝是正确的，理由是违反 Bandcamp 服务条款去抓取数据本身就是明确的越界行为，而一个“人人自由抓取”的智能体互联网只会更加垃圾化和欺诈化。另一些人则认为作者的论证牵强且带有私利倾向；还有一位评论者（Lerc）主张以法律形式要求 AI 顾问为客户的最大利益行事，像法律、金融和医疗顾问一样受不得违法的约束，并且绝不能声称自己在为并非客户的一方行事。

**标签**: `#LLM agents`, `#AI alignment`, `#AI policy`, `#terms of service`, `#web scraping`

---

<a id="item-13"></a>
## [GTA 6「Leonida」PC 重编译项目被 GitHub 下架](https://github.com/ItsNotRexed/Leonida/issues) ⭐️ 7.0/10

社区驱动的「Leonida」项目曾把 GTA 6 的 Xbox Series X 版本静态重编译为原生 PC 可执行文件，如今该项目在 GitHub 上被下架，而当时项目主开发者还在上学。这次下架发生在此前 Hacker News 上对该项目的一轮讨论之后，并已成为围绕 AI 辅助逆向工程的一个争议焦点。 这说明借助大语言模型辅助的逆向工程能以多快的速度把一款主机独占作品变成可玩的 PC 版本，从而削弱限时平台独占的价值。此次下架也考验着版权方愿意对从未分发游戏素材的社区重编译项目追究到什么程度。 Leonida 是一个开源静态重编译框架，目标是泄露的 GTA 6 Xbox Series X 版本（Build 1.0.2.1），它把 RAGE 引擎的主机代码翻译成原生 x86-64 PC 二进制文件，而不是进行模拟。由于项目本身不托管任何受版权保护的素材，这类项目通常只要求用户自备原版游戏文件；而 GitHub 上此类删除一般源于版权方发出的 DMCA 通知。

hackernews · smuhakg · 11月24日 02:08 · [社区讨论](https://news.ycombinator.com/item?id=50622638)

**背景**: 静态重编译是一种把主机游戏的机器码直接转换为另一平台原生代码的技术，产物无需模拟器即可运行。过去这需要多年手工劳动以及对目标引擎的深入了解，但近年基于大语言模型的工具极大加速了反编译与逆向工程工作——一个社区目录在 300 个 AI 辅助项目中统计出 151 个静态重编译项目，其中 275 个使用了 Claude。Rockstar 的母公司 Take-Two 以强硬维权著称，因此任何与 GTA 相关的逆向工程都面临显著法律风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gta6recomp.com/leonida">Leonida — GTA 6 PC Static Recompilation Project Tracker & Source</a></li>
<li><a href="https://www.retroreversing.com/source-code/decompiled-retail-console-games">Decompiled Retail Console Games - Retro Reversing ...</a></li>
<li><a href="https://reversedwithai.com/ai-game-decompilation">AI reverse engineered games : decompiled and ported with AI</a></li>

</ul>
</details>

**社区讨论**: 评论者意见分歧，但总体上对项目抱有同情：不少人表示愿意为游戏付费，却不愿为玩它而额外购买 500 欧元以上的主机；还有人预测，本会在 Steam 上购买的玩家反而会去盗版这个移植版本。另一些人对大语言模型让此事迅速变得可行感到惊讶，一位开发者承认自己曾断定这是需要多年的巨大工程，也有多人认为在当下仍推迟 PC 版发布显得不合时宜。

**标签**: `#reverse-engineering`, `#game-preservation`, `#AI-assisted-development`, `#platform-exclusivity`, `#github-takedown`

---

<a id="item-14"></a>
## [开发者称 T3 Code 默认开启遥测并读取本机 Codex 与 Claude 凭证](https://x.com/realchendahuang/status/2125153472450527440) ⭐️ 7.0/10

11 月 24 日，X 用户 @realchendahuang 发文称，Theo 的 T3 Code 自 3 月合并 PR #174 起就默认开启 PostHog 遥测；10 月合并的 PR #21506 还会读取 ~/.codex/auth.json 与 ~/.claude.json，并将 Codex 的 user_id、Claude 的 accountUuid 连同设备 ID 以无盐 SHA-256 哈希后上传。该帖附带了代码引用链接，但 Theo 本人与项目方均未回应。 如果属实，这意味着一个被广泛讨论的 AI 编程工具正在悄悄采集来自其他厂商开发者工具的标识信息，对所有在本机使用 Codex 或 Claude Code 的开发者都构成同意权与供应链安全方面的担忧。这也让 AI 开发者工具默认如何处理遥测、以及是否应跨工具读取凭证的争论进一步升温。 帖文称上传的只是标识符的无盐 SHA-256 哈希值，但无盐哈希只属于假名化而非匿名化：稳定的每用户哈希在多个事件之间仍可关联，一旦原始 ID 空间可枚举就能被反推比对。发帖者还称有四个试图关闭遥测的 PR 被拒绝，且官方文档承认浏览器与移动端的中继诊断追踪无法关闭；不过该指控目前仍只是一条未经证实的社交媒体说法。

telegram · zaihuapd · 11月24日 10:58

**背景**: PostHog 是一个开源的产品分析平台，许多开发者工具会嵌入它来收集功能采用率、崩溃报告等使用事件。Codex 把登录会话保存在 ~/.codex/auth.json，Claude Code 则使用 ~/.claude.json，这些文件里存放的是认证材料和账户标识而非明文密码，因此任何读取它们的库都格外敏感。上传前对标识符做哈希是常见的隐私做法，但其保护强度很大程度上取决于是否加盐。T3 Code 是开发者兼内容创作者 Theo 推出的 AI 编程工具，其源码通过 PR 方式公开开发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://posthog.com/docs/product-analytics/privacy">Privacy controls - Docs - PostHog</a></li>
<li><a href="https://aicodewith.ai/zh/blog/codex-auth-json">Codex auth . json 是什么：位置、风险与安全排错 | AI Code With</a></li>

</ul>
</details>

**标签**: `#privacy`, `#telemetry`, `#AI developer tools`, `#security`, `#open source governance`

---

<a id="item-15"></a>
## [华为与高通达成覆盖 5G 与人工智能的多年广泛专利交叉许可协议](https://t.me/zaihuapd/45344) ⭐️ 7.0/10

华为官方宣布与高通达成一项为期多年、范围广泛的专利许可协议，涵盖双方在 5G、计算、人工智能和网络等领域的专利组合交叉许可，同时高通将购买华为部分美国专利。彭博社援引华为发言人的说法称，高通还同意获得华为"逻辑折叠"芯片制造技术相关专利的许可，该交易将在获得必要监管批准后完成。 该协议正式确立了两大无线标准必要专利持有方之间的知识产权关系，降低了诉讼风险，并使高通得以获得华为芯片制造相关的知识产权。这同时强化了华为快速增长的专利许可业务——华为称其自 2021 年起已实现正向收入，也表明尽管面临美国限制，华为在全球 5G 与人工智能专利许可中仍是核心参与者。 华为表示，交易完成后其专利许可协议的累计预期合同价值预计将超过 69 亿美元（约合 463.02 亿元人民币），且协议仍需获得监管批准后方可生效。具体的许可费率、付款安排以及高通将购买哪些美国专利均未披露。

telegram · zaihuapd · 11月24日 11:38

**背景**: 专利交叉许可让两家公司可以互相使用对方的专利技术，而无需另行谈判许可费，这在各自持有 5G 标准必要专利（SEP）的主要厂商之间十分常见——任何实施 5G 技术的企业都必须以公平、合理、无歧视（FRAND）条款获得这些专利授权。华为自 2021 年起建立了正式的专利许可业务，向手机厂商收取许可费，而高通的许可部门则是其重要利润来源。"逻辑折叠"是华为近期在麒麟芯片宣传中使用的说法，通常与先进封装和堆叠式芯片架构相关，这类方案可在不完全依赖更先进制程的情况下提升性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ithome.com/1/031/517.htm">华为 Mate X8 大 折 旗舰机发布：麒麟 9050 Pro...</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#Qualcomm`, `#patent-licensing`, `#5G`, `#AI`

---

<a id="item-16"></a>
## [SpaceX 与特斯拉董事会分别设立特别委员会审议合并事宜](https://t.me/zaihuapd/45351) ⭐️ 7.0/10

SpaceX 与特斯拉的董事会各自成立了由独立董事组成的特别委员会，负责审议两家公司可能的合并事宜。马斯克表示，这两个委员会是应股东要求设立的，他因存在利益冲突不会参与相关讨论，并强调双方目前尚未就任何交易条款达成一致。 若合并成行，将把全球估值最高的私营火箭公司与美国最大的电动车制造商合为一体，进一步集中马斯克的商业版图，并重塑航天、电动车及 AI 机器人领域的格局。由于特斯拉是上市公司，任何交易都需获得全体股东中过半数的赞成票，因此这将成为涉及利益冲突控股方交易的公司治理标志性案例。 马斯克支持合并构想，但表示交易并非板上钉钉，最终仍需股东支持。SpaceX 一侧的股东投票预计相对容易通过，而特斯拉则需要获得全体股东中 50% 的赞成票，这一门槛明显高于按实际投票数计算的简单多数。

telegram · zaihuapd · 11月25日 00:41

**背景**: 由独立董事组成的特别委员会，是公司在审议涉及内部人（如控股股东或 CEO）的交易时常用的治理机制，目的是让存在利益冲突的各方回避谈判。马斯克既是上市公司特斯拉的 CEO 和大股东，也是仍为私营公司的 SpaceX 的 CEO 和大股东，因此在任何潜在交易中都同时站在交易双方的位置上。特斯拉的公司章程和类似特拉华州的公司法惯例，通常要求进行独立审查，并在部分交易中要求绝对多数或全体股东过半数的批准，以保护中小股东利益。

**标签**: `#SpaceX`, `#Tesla`, `#merger`, `#Elon Musk`, `#corporate governance`

---

<a id="item-17"></a>
## [Anthropic 股价跌破 83 美元发行价，引发 AI 经济性争论](https://www.bloomberg.com/news/articles/2026-11-24/anthropic-breaks-below-83-ipo-price-in-premarket-trading) ⭐️ 6.0/10

据彭博报道，Anthropic 的股价在盘前交易中跌破 83 美元的 IPO 发行价，使这家 AI 实验室的股价低于其上市时的定价水平。这一下跌在 Hacker News 上引发热议，一条 692 条评论的讨论帖主要剖析的是 AI 商业模式的经济性，而非公司的技术本身。 当一家领先的前沿 AI 实验室股价跌破发行价时，就会动摇“站在技术前沿就必然带来优异股权回报”这一被广泛接受的假设，并可能影响员工、后期投资者和竞争对手对 AI 公司的估值方式。这同样重要，因为当前 AI 资本开支越来越依赖预期回报来支撑，公开市场对某一家实验室的怀疑情绪会波及整个行业的融资与估值叙事。 彭博的报道本身缺乏技术与财务细节，因此价值主要来自讨论：一位评论者称其运行一套模型无关的持续开发流水线，每周 AI 预算约 1 万美元，其中约 65% 的模型开销流向 Anthropic，并指出随着新模型发布，这一构成会不断变化。其他人则指出，跌破发行价是上市后的常见现象，并以亚马逊、Netflix、特斯拉和 Meta 作为先例。

hackernews · Betelbuddy · 11月24日 13:23 · [社区讨论](https://news.ycombinator.com/item?id=50627836)

**背景**: IPO 发行价是公司首次向公众投资者出售股票时的定价；一旦开始交易，股价便可自由浮动，并经常跌破发行价，这通常被视为一种象征性而非根本性的判断。Anthropic 是一家在前沿大语言模型领域竞争的重要 AI 实验室，该领域的训练与推理成本极高，且客户可以在不同厂商的模型之间切换。所谓“开放权重”（open weight）指的是训练后参数可公开下载的模型，团队可自行部署而无需按 token 支付 API 费用，这正是讨论中成本争论的核心。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://applied-llms.org/">What We’ve Learned From A Year of Building with LLMs – Applied LLMs</a></li>

</ul>
</details>

**社区讨论**: 讨论情绪分化。一位评论者给出具体的单位经济数据：每周约 1 万美元的模型无关流水线中，约 65% 花在 Anthropic 上；另一位则认为，AI 完全可能既具变革性又利润丰厚，但 Anthropic 的股票仍可能是一笔糟糕的投资。还有悲观者声称增长已尽、股价应像传统车企那样定价（约 10 美元），但有人反驳说上市后回落属于教科书式的常态，并举出亚马逊、Netflix、特斯拉和 Meta 为例。

**标签**: `#anthropic`, `#ai-industry`, `#ipo`, `#llm-economics`, `#market-analysis`

---

<a id="item-18"></a>
## [李彦宏内部讲话：大模型开源意义不大，百度绝不抢开发者饭碗](https://t.me/zaihuapd/45334) ⭐️ 6.0/10

百度 CEO 李彦宏的一段内部讲话被曝光，他在其中表示大模型开源的意义不大，闭源模型会在能力上持续领先，并在推理成本和响应速度上占优。他还强调百度“绝不抢开发者饭碗”，即公司定位为模型提供方而非与应用开发者争夺市场。 这一表态来自中国头部 AI 公司的 CEO，在开源与闭源大模型的路线之争中鲜明地站在闭源一边，可能影响国内企业和开发者对模型技术栈的选择。这也表明百度希望围绕自研的文心一言系列构建生态，而不是通过开放权重把模型变成通用商品。 李彦宏认为大模型开源与 Linux、安卓等传统软件开源有本质不同，并非“众人拾柴火焰高”，社区贡献无法让模型迭代更快。他还称只有能赚钱的闭源商业模式才能持续聚集算力和人才，并且在同等能力下闭源模型的推理成本一定更低、响应速度一定更快。

telegram · zaihuapd · 11月24日 07:32

**背景**: 大模型可以选择开放权重，让任何人下载、修改并自行部署（如 Meta 的 Llama 系列），也可以保持闭源、仅通过 API 提供服务（如 OpenAI 的 GPT-4 和百度的文心一言）。开源模型降低了使用门槛，并让企业掌控数据和部署环境；闭源模型则被认为性能更强、维护更简单，对开发方而言商业模式也更清晰。在中国，两条路线都有代表：阿里通义千问和 DeepSeek 开放了模型权重，而百度旗舰的文心系列一直坚持闭源。

**标签**: `#LLM`, `#open-source`, `#closed-source`, `#Baidu`, `#AI industry`

---

<a id="item-19"></a>
## [Anthropic CEO Dario Amodei 预测：AI 有望 10 年内攻克癌症等疑难病症](https://t.me/zaihuapd/45336) ⭐️ 6.0/10

Anthropic CEO Dario Amodei 预测，AI 的进步有望在约 10 年内让癌症、阿尔茨海默病、心脏病和精神类疾病成为“历史遗迹”。这一表态伴随着一系列实际动作：Anthropic 近期收购了多家生物技术初创企业，上月披露已启动内部新药研发项目，并在旧金山设立实验室，研究 AI 如何支撑基础生物学研究。 一家头部前沿 AI 实验室公开把新药研发和攻克疾病定位为下一个前沿方向，说明 AI 公司与制药行业正在加速融合，这可能重塑药物研发周期，并为“AI 原生”生物科技带来新的资金和科研人才。这同时也抬高了 Anthropic 的声誉风险：此类说法会引来外界追问，AI 生成的生物学洞见究竟能否转化为经过验证的药物。 这一说法属于前瞻性预测，而非经过同行评议的研究成果——文中并未披露具体的研发管线、时间表或临床数据，目前可佐证的只有收购动作、内部新药研发项目以及旧金山的研究实验室。Amodei 今年 8 月曾在 X 上表示，说服 AI 怀疑者的最好方式就是真正治愈癌症，将该说法定位为一种自我问责的承诺。

telegram · zaihuapd · 11月24日 08:54

**背景**: AI 药物发现利用机器学习模型分析生物学和化学数据，例如预测蛋白质结构、筛选候选化合物、对靶点排序，从而让研究者能够探索远比单纯实验室实验更多的假设。代表性案例包括由 Demis Hassabis 领导、从 Google DeepMind 分拆出来的药物发现公司 Isomorphic Labs，以及以 AI 驱动药物发现流程的 Recursion。这一方向受制于生物数据的稀疏性与噪声，因此像 Biohub 这样的机构认为，更优质的数据与模型是 AI 真正加速基础生物学研究的前提。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Isomorphic_Labs">Isomorphic Labs - Wikipedia</a></li>
<li><a href="https://www.recursion.com/">Pioneering AI Drug Discovery | Recursion</a></li>
<li><a href="https://biohub.org/">Biohub - Leading the new era of AI -powered biology</a></li>

</ul>
</details>

**标签**: `#AI`, `#Anthropic`, `#biotech`, `#drug discovery`, `#healthcare`

---