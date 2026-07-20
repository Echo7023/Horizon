---
layout: default
title: "Horizon Summary: 2026-07-21 (ZH)"
date: 2026-07-21
lang: zh
---

> 从 33 条内容中筛选出 13 条重要资讯。

---

1. [泄露的 Altman 邮件：OpenAI 曾考虑发布本地 GPT-3 以打击竞争对手](#item-1) ⭐️ 9.0/10
2. [Fastjson 1.x 无 gadget 高危 RCE 漏洞](#item-2) ⭐️ 9.0/10
3. [中国开源权重 AI 策略占据优势](#item-3) ⭐️ 8.0/10
4. [黑客清空罗马尼亚土地登记数据库](#item-4) ⭐️ 8.0/10
5. [arXiv 上 AI 写作检测：准确性与局限性](#item-5) ⭐️ 8.0/10
6. [不良 LED 设计加剧光污染，浪费夜空潜力](#item-6) ⭐️ 8.0/10
7. [欧盟向美国共享生物识别数据以换取免签旅行引发隐私争议](#item-7) ⭐️ 8.0/10
8. [Kimi K3 与 Qwen 3.8 开源发布；Anthropic 关系紧张](#item-8) ⭐️ 8.0/10
9. [本·汤普森提议为 AI 训练设立合理使用法律](#item-9) ⭐️ 8.0/10
10. [Hugging Face 披露 AI 智能体攻击，商业大模型拒绝协助取证](#item-10) ⭐️ 8.0/10
11. [美国或限制企业使用中国开放权重 AI 模型](#item-11) ⭐️ 8.0/10
12. [美军应用被发现嵌入中俄代码](#item-12) ⭐️ 8.0/10
13. [智谱建成全国产芯片数据中心](#item-13) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [泄露的 Altman 邮件：OpenAI 曾考虑发布本地 GPT-3 以打击竞争对手](https://simonwillison.net/2026/Jul/20/sam-altman/#atom-everything) ⭐️ 9.0/10

一封 Sam Altman 于 2022 年 10 月 1 日发给 OpenAI 董事会的泄露邮件显示，OpenAI 曾考虑发布一个能在消费级硬件上本地运行的、能力接近 GPT-3 的模型，以阻止 Stability AI 等竞争对手资助类似的开源努力。 这封邮件罕见地直接揭示了 OpenAI 关于开源模型作为竞争策略的战略思考，突显了主要 AI 实验室如何将开源发布视为塑造市场和削弱竞争对手资金的手段。 该邮件在 2026 年 Musk 诉 Altman 案中被曝光，其中特别提到要在'Stability 或其他公司之前'发布模型，以使新项目更难获得资金。

rss · Simon Willison · 7月20日 03:47

**背景**: Stability AI 是一家以开源模型（如 Stable Diffusion）闻名的英国公司，其模型对 OpenAI 的专有 AI 构成挑战。当时，开源 AI 模型的能力不断增强，OpenAI 等实验室将其视为机遇和威胁。本地运行模型的想法允许用户在没有云依赖的情况下运行强大 AI。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Stability_AI">Stability AI</a></li>
<li><a href="https://github.com/PromtEngineer/localGPT">PromtEngineer/localGPT: Chat with your documents on your local ...</a></li>

</ul>
</details>

**标签**: `#openai`, `#sam-altman`, `#ai open source`, `#gpt-3`, `#ai strategy`

---

<a id="item-2"></a>
## [Fastjson 1.x 无 gadget 高危 RCE 漏洞](https://x.com/k_firsov/status/2078872293745570032) ⭐️ 9.0/10

安全研究员 Kirill Firsov 披露了一个高危远程代码执行漏洞，影响 Fastjson 1.2.68 至 1.2.83 版本，该漏洞无需启用 autoType 或依赖 classpath gadget，可在 JDK 8、17、21 上利用。 该漏洞严重性高，因为无需 gadget 链即可利用，降低了攻击门槛，且影响已停止维护的 Fastjson 1.x 版本，官方大概率不会发布补丁，用户必须紧急迁移到 Fastjson2 或启用 SafeMode。 该漏洞在 Fastjson 1.x 于 2024 年 10 月停止维护后披露。缓解措施包括升级到 Fastjson2，或通过 JVM 参数 -Dfastjson.parser.safeMode=true 或配置 ParserConfig 启用 SafeMode。

telegram · zaihuapd · 7月20日 14:32

**背景**: Fastjson 是 Java 中广泛使用的 JSON 库，其 autoType 功能会在序列化数据中包含类型信息，但历史上已导致多次反序列化漏洞。SafeMode 自 1.2.68 版本引入，用于完全禁用 autoType 以防止攻击。此次披露的漏洞无需任何特定 classpath gadget 即可绕过现有限制，极为危险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/alibaba/fastjson/wiki/fastjson_safemode_en">fastjson_safemode_en · alibaba/fastjson Wiki</a></li>
<li><a href="https://github.com/alibaba/fastjson/wiki/enable_autotype">enable_autotype · alibaba/fastjson Wiki · GitHub</a></li>
<li><a href="https://www.huaweicloud.com/intl/en-us/notice/20220523153626935.html">Fastjson <= 1.2.80 Deserialization Remote Code Execution Vulnerability_HUAWEI CLOUD</a></li>

</ul>
</details>

**标签**: `#security`, `#fastjson`, `#rce`, `#vulnerability`, `#java`

---

<a id="item-3"></a>
## [中国开源权重 AI 策略占据优势](https://werd.io/american-ai-is-locked-down-and-proprietary-its-losing/) ⭐️ 8.0/10

近期一篇文章指出，中国的开源权重 AI 模型正相对于美国专有模型获得竞争优势，并以历史上开放和低成本解决方案最终主导市场的模式作为类比。 这一趋势可能通过降低强大模型的使用门槛重塑全球 AI 格局，可能削弱美国科技巨头的市场地位，并加速 AI 在成本敏感型应用中的普及。 文章声称 80%的初创公司使用中国模型，但评论者对此数据存疑。领先的开源权重模型如 Qwen 和 DeepSeek 在多项 AI 排行榜上名列前茅。

hackernews · benwerd · 7月20日 14:21 · [社区讨论](https://news.ycombinator.com/item?id=48979269)

**背景**: 开源权重模型将训练好的神经网络权重公开，允许微调和部署，但训练数据或代码未必完全透明。这与 GPT-4 等通过 API 访问的专有模型形成对比。历史上，低成本或免费解决方案（如个人电脑对大型机、Linux 对 Unix）往往在市场中胜出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@aruna.kolluru/exploring-the-world-of-open-source-and-open-weights-ai-aa09707b69fc">Exploring the World of Open Source and Open Weights AI | Medium</a></li>
<li><a href="https://llm-stats.com/">AI Leaderboard 2026: Compare & Rank 300+ Top AI Models by...</a></li>
<li><a href="https://artificialanalysis.ai/models">Comparison of AI Models across Intelligence, Performance, and Price</a></li>

</ul>
</details>

**社区讨论**: 评论者对“80%初创公司使用中国模型”的说法表示怀疑，并引用自己使用美国模型的经历。一些人指出，企业更看重数据留存和供应商关系而非模型开放性。

**标签**: `#AI`, `#open-source`, `#China`, `#machine learning`, `#industry trends`

---

<a id="item-4"></a>
## [黑客清空罗马尼亚土地登记数据库](https://news.risky.biz/risky-bulletin-hacker-wipes-romanias-entire-land-registry-database/) ⭐️ 8.0/10

一名黑客入侵并清空了罗马尼亚土地登记数据库，声称已删除备份，但官方表示有一个离线副本幸存，并正在将系统迁移至政府云基础设施。 此事件可能破坏土地所有权验证，从而威胁社会稳定，并凸显了政府 IT 安全中的关键漏洞，特别是在密码实践和备份策略方面。 攻击者据称使用诸如'P@ssw0rd'之类的弱密码获得访问权限，安全公司 KELA 将黑客识别为阿尔及利亚的 Zakaria Mahdjoub。一个离线数据副本使官方避免了彻底损失。

hackernews · speckx · 7月20日 13:28 · [社区讨论](https://news.ycombinator.com/item?id=48978605)

**背景**: 土地登记对于证明财产所有权至关重要，其受损可能导致法律混乱。据报道，罗马尼亚政府 IT 长期遭受腐败和不良安全实践的影响，合同被授予裙带关系者，他们忽视了适当的保护措施。

**社区讨论**: 社区评论强调腐败是根本原因，合同被授予忽视安全的裙带关系者。虽然对存在离线备份感到欣慰，但对政府的应对和长期安全改进仍持怀疑态度。

**标签**: `#cybersecurity`, `#data breach`, `#land registry`, `#Romania`, `#security incident`

---

<a id="item-5"></a>
## [arXiv 上 AI 写作检测：准确性与局限性](https://unslop.run/blog/measuring-ai-writing-on-arxiv) ⭐️ 8.0/10

一项对 2021 至 2026 年间超过 12,000 篇 arXiv 论文的分析发现，截至 2026 年 1 月，约 39%的论文被标记为 AI 撰写，其中计算机科学领域高达 65%。作者调整了检测器以减少误报，同时指出了测量方法的局限性，尤其是旧的人类撰写论文也可能被误判为 AI 撰写。 该分析量化了学术论文中 AI 撰写内容的快速增长，引发了对检测方法可靠性的担忧，并影响学术出版、同行评审及对科学文献的信任。 该检测器实现了非常低的误报率（ChatGPT 之前为 0.4%），但仍将一些旧论文标记为 AI 撰写——例如 2011 年的论文被检测出 27%，2015 年的论文被检测出 74%——表明人类写作可能与 LLM 模式重叠。分析还显示显著的学科差异，计算机科学论文的 AI 撰写检测率高达 65%，而数学领域几乎无变化。

hackernews · dopamine_daddy · 7月20日 16:36 · [社区讨论](https://news.ycombinator.com/item?id=48981206)

**背景**: LLM 生成的文本检测通常采用黑盒或白盒方法，分析词汇选择、困惑度和突发性等统计模式。然而，这些检测器常出现假阳性，尤其是在高度技术性或非母语英语写作中，并且可以通过有针对性的编辑来规避。LLM 在学术写作中的日益融入促使人们尝试测量和检测 AI 生成的内容，但此类检测的准确性和可靠性仍是争论和研究的热点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cacm.acm.org/research/the-science-of-detecting-llm-generated-text/">The Science of Detecting LLM -Generated Text – Communications of...</a></li>
<li><a href="https://www.linkedin.com/pulse/limitations-ai-detection-academic-writing-maindze-mphil-mbcs--0olfe">The Limitations of AI Detection in Academic Writing .</a></li>
<li><a href="https://arxiv.org/pdf/2406.09056">Towards Reliable Detection of LLM -Generated Texts...</a></li>

</ul>
</details>

**社区讨论**: 社区评论对检测方法表示强烈怀疑。用户报告称自己 2010 年之前的论文也被标记为 AI 撰写，表明误报普遍存在。有人认为问题可能被夸大，也有人讨论 LLM 在企业和学术环境中使用的策略意义。

**标签**: `#AI writing`, `#arXiv`, `#LLM detection`, `#academic publishing`, `#measurement`

---

<a id="item-6"></a>
## [不良 LED 设计加剧光污染，浪费夜空潜力](https://spectrum.ieee.org/led-light-pollution) ⭐️ 8.0/10

IEEE Spectrum 上的一篇文章指出，设计不良的 LED 照明因注重成本最小化和简单的地面照度测量，产生眩光和天空辉光，加剧了光污染，违背了 LED 保护夜空的潜力。 这很重要，因为光污染破坏生态系统、妨碍天文观测，并削弱人类对夜空的文化连接；更好的工程标准可以在提供有效户外照明的同时减轻这些影响。 文章强调，安装在高处的裸露灯泡产生强烈眩光，加剧夜盲，而通常的“补救”是增加更多光线；正确的设计应遮蔽灯泡使其不被直接看到，并使用存在传感器实现自适应照明。

hackernews · defrost · 7月20日 13:07 · [社区讨论](https://news.ycombinator.com/item?id=48978350)

**背景**: LED 是一种节能且可精确控制的照明技术，但不良的实施往往导致富含蓝光的光线在大气中散射，产生天空辉光。国际暗夜协会与照明工程学会制定了示范法规和标准来解决光污染，但许多城市缺乏更新的规范。社区评论中提到的存在感应灯可以在需要时才照明，从而减少能源消耗和光污染。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mrsc.org/explore-topics/code-enforcement/nuisances/light-nuisances">MRSC - Light Nuisances - Ambient Light, Light Pollution, Glare</a></li>
<li><a href="https://www.ekinex.com/en/ekinex-solutions-for-smart-lighting-control/presence-sensors.html">Presence sensors | Smartlighting | Ekinex</a></li>

</ul>
</details>

**社区讨论**: 评论表达了对社会对夜空漠不关心的担忧，有用户指出不列颠哥伦比亚省的温室造成严重光污染。另一用户称赞公园中的存在感应灯，只在有人经过时才亮起，保护了野生动物的黑暗环境。用户还呼吁更好的工程标准，认为通过避免视线直接接触光源可以减少裸露灯泡的眩光。

**标签**: `#light pollution`, `#LED lighting`, `#astronomy`, `#urban planning`, `#environmental impact`

---

<a id="item-7"></a>
## [欧盟向美国共享生物识别数据以换取免签旅行引发隐私争议](https://edri.org/our-work/the-eu-is-about-to-sell-our-most-sensitive-data-to-the-us-for-visa-free-travel/) ⭐️ 8.0/10

欧盟正在推进与美国共享旅行者的生物识别数据，以维持免签证旅行安排，此举引发了隐私担忧。 这一决定可能为大规模跨境共享敏感生物识别数据开创先例，影响数百万旅行者，并可能削弱欧盟的隐私保护。 这些数据包括面部图像和指纹，这些信息已在美国边境对签证申请人收集，并在欧盟新的出入境系统（EES）下在边境收集。

hackernews · rapnie · 7月20日 12:14 · [社区讨论](https://news.ycombinator.com/item?id=48977711)

**背景**: 免签证计划允许参与国公民无需签证即可前往美国停留最多 90 天，但要求旅行者在线获得 ESTA 授权。目前，大多数旅行者在抵达美国时需采集生物识别数据（指纹和照片）。欧盟提议提前共享这些数据，可能减少边境处理时间，但引发了隐私担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fastercapital.com/content/Data-sharing--Data-Sharing-Agreements-and-Protocols-for-Business-Data-Privacy.html">Data sharing : Data Sharing Agreements and... - FasterCapital</a></li>
<li><a href="https://www.travelandtourworld.com/news/article/uk-tourists-to-face-biometric-registration-in-italy-greece-france-spain-and-portugal-as-new-border-rules-take-effect/">UK Tourists To Face Biometric Registration... - Travel And Tour World</a></li>
<li><a href="https://www.hindustantimes.com/world/eu-threatens-to-suspend-data-sharing-with-us/story-y0vazdh1OzoDn7jDTx1mjI.html">EU threatens to suspend data - sharing with US - Hindustan Times</a></li>

</ul>
</details>

**社区讨论**: 评论指出，生物识别数据已在边境收集，辩论焦点在于便利性与隐私的权衡。一些人质疑数据共享的范围及其与现行做法的区别，而另一些人则认为免签旅行已要求大量信息披露。

**标签**: `#privacy`, `#EU-US data sharing`, `#biometric data`, `#travel policy`, `#surveillance`

---

<a id="item-8"></a>
## [Kimi K3 与 Qwen 3.8 开源发布；Anthropic 关系紧张](https://www.emergingtrajectories.com/lh/frontier-lab-economics/) ⭐️ 8.0/10

Moonshot AI 发布了拥有 2.8 万亿参数的开源模型 Kimi K3，阿里云也发布了拥有 2.4 万亿参数的多模态模型 Qwen 3.8，两者相隔仅数天。与此同时，Anthropic 因其首席产品官从 Figma 董事会辞职，且随后发布竞争工具而陷入争议。 这些发布表明，前沿级别的开放权重模型正变得免费可用，加剧了竞争，并可能使 AI 能力商品化。Anthropic 与 Figma 的事件突显了 AI 行业中围绕产品策略和信任的日益紧张关系。 Kimi K3 是迄今为止最大的开源模型，拥有 2.8 万亿参数；Qwen 3.8 采用稀疏混合专家架构，支持文本、图像、视频和文档。两者均拥有 100 万 token 的上下文窗口，可与顶级专有模型媲美。

hackernews · cl42 · 7月20日 15:13 · [社区讨论](https://news.ycombinator.com/item?id=48980019)

**背景**: 开放权重模型是指参数公开的人工智能模型，任何人都可以下载、微调和部署。前沿 AI 实验室一直在争论是否要开源其最强大的模型，而中国公司往往采取更开放的态度。Anthropic 与 Figma 的争议涉及董事会成员在竞争产品发布前辞职可能引发的利益冲突。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://venturebeat.com/technology/chinas-moonshot-ai-releases-kimi-k3-the-largest-open-source-model-ever-rivaling-top-u-s-systems">China’s Moonshot AI releases Kimi K3, the largest open-source model ever, rivaling top U.S. systems | VentureBeat</a></li>
<li><a href="https://the-decoder.com/alibabas-qwen-takes-on-kimi-k3-with-open-weight-qwen-3-8-says-model-is-second-only-to-fable-5/">Alibaba's Qwen takes on Kimi K3 with open-weight Qwen 3.8, says model is "second only to Fable 5"</a></li>
<li><a href="https://mlq.ai/news/alibaba-launches-qwen-38-with-24-trillion-parameters-claims-near-frontier-performance/">Alibaba Launches Qwen 3.8 With 2.4 Trillion Parameters, Claims Near-Frontier Performance | MLQ News</a></li>

</ul>
</details>

**社区讨论**: 社区评论指出，专门化 ASIC 可能成为关键差异化因素，大型语言模型可辅助芯片设计。其他人则讨论 Figma 争议是信任的背叛，而一些人认为前沿模型的价值证明了其成本合理，并且炒作周期正在缩短，可能预示着平台期。

**标签**: `#AI`, `#open-source`, `#frontier labs`, `#business strategy`, `#community discussion`

---

<a id="item-9"></a>
## [本·汤普森提议为 AI 训练设立合理使用法律](https://simonwillison.net/2026/Jul/20/afraid-of-chinese-models/#atom-everything) ⭐️ 8.0/10

本·汤普森提议美国通过一项法律，明确将收集数据用于 AI 训练视为合理使用，并禁止服务条款中禁止模型蒸馏的条款，旨在帮助美国的开放权重模型与中国模型竞争。 该提案解决了 AI 实验室禁止对其模型进行蒸馏却使用未经许可数据训练的双重标准问题，并可能通过促进开放权重模型创新来创造公平竞争环境，影响中美全球 AI 竞争格局。 本·汤普森还推测，阿里巴巴改变决定、开放 Qwen 3.8 Max 的权重可能受到了习近平最近鼓励开源、开放与合作分享的讲话影响。

rss · Simon Willison · 7月20日 17:09

**背景**: 模型蒸馏是一种将知识从大型'教师'模型转移到较小'学生'模型的技术，通常通过查询教师模型的 API 实现。使用受版权保护的数据进行 AI 训练是否属于合理使用，目前法律上存在争议。开放权重模型允许任何人下载并运行模型，从而普及 AI 的使用。该提案旨在平衡版权问题与 AI 创新的需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>
<li><a href="https://www.skadden.com/insights/publications/2025/05/copyright-office-report">Copyright Office Weighs In on AI Training and Fair Use | Skadden, Arps, Slate, Meagher & Flom LLP</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#open weights`, `#distillation`, `#fair use`, `#Chinese AI models`

---

<a id="item-10"></a>
## [Hugging Face 披露 AI 智能体攻击，商业大模型拒绝协助取证](https://huggingface.co/blog/security-incident-july-2026) ⭐️ 8.0/10

Hugging Face 披露了 2026 年 7 月的一起安全事件，攻击者利用数据集处理流程中的代码执行漏洞，通过自主 AI 智能体框架横向移动并窃取了凭证和数据集。在事件响应中，商业大模型 API 因安全护栏拒绝协助取证分析，Hugging Face 转而使用本地部署的 GLM 5.2 模型，成功分析了超过 1.7 万条攻击记录。 此次事件凸显了 AI 智能体驱动攻击对 AI 基础设施的新兴威胁，以及闭源商业大模型在安全取证关键任务中的局限性。它强调了开源模型的重要性，这些模型可以本地部署用于敏感操作，而不受限制性安全护栏的约束。 攻击利用了 Hugging Face 数据集处理流程中的两处代码执行漏洞，在周末期间执行了数万次操作，并窃取了部分内部数据集和服务凭证。Hugging Face 确认面向公众的模型、数据集和 Spaces 未被篡改，软件供应链无异常。

telegram · zaihuapd · 7月20日 10:41

**背景**: Hugging Face 是一个托管和共享机器学习模型与数据集的主要平台。AI 智能体是可以执行网页浏览或 API 调用等任务的自主系统，它们面临提示注入等新型攻击面。GLM 5.2 是智谱 AI（现 Z.ai）开发的大语言模型，采用 MIT 许可证发布，支持 100 万 token 上下文，专为长周期任务设计。此次事件表明，当商业 API 施加限制时，开源模型在取证分析中至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GLM_5.2">GLM 5.2</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/GLM-5.2 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI安全`, `#Hugging Face`, `#安全事件`, `#大模型`, `#取证`

---

<a id="item-11"></a>
## [美国或限制企业使用中国开放权重 AI 模型](https://www.axios.com/2026/07/20/ai-us-china-open-source-kimi) ⭐️ 8.0/10

据 Axios 报道，因 Kimi K3 模型表现强劲，特朗普政府正在考虑重新推动限制美国企业使用性价比高的中国开放权重 AI 模型。 这可能重塑全球 AI 竞争格局，迫使美国企业放弃物美价廉的开放权重模型，巩固 OpenAI 和 Anthropic 等闭源供应商的主导地位。 政府可能采用采购规则、实体清单威胁和舆论压力等软性措施而非硬性封禁；白宫 AI 顾问 David Sacks 批评此举是闭源巨头试图消灭开源竞争。

telegram · zaihuapd · 7月20日 11:49

**背景**: 开放权重 AI 模型提供访问训练权重的权限，比完全闭源模型更具可控性和成本效益，但并非完全开源。中国的 Kimi K3 模型拥有近 3 万亿参数和 100 万 token 上下文，以较低成本展现出前沿性能，媲美美国模型。美中科技竞争持续升温，此前限制中国 AI 的尝试曾被主张放松监管的官员阻止。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/open-weight-ai-what-we-finally-opened-bonnet-nicolas-pistorio-n3ulf">Open - weight AI : what if we finally opened the bonnet ?</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2025/04/open-weight-models/">What are Open Source and Open Weight Models ? | Analytics Vidhya</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/worlds-largest-agent-from-china-challenge-us">World's first 3-trillion model from China does weeks of work in hours</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#open-source models`, `#geopolitics`, `#Kimi K3`, `#US-China tech rivalry`

---

<a id="item-12"></a>
## [美军应用被发现嵌入中俄代码](https://www.wired.com/story/apps-marketed-to-us-troops-are-shipping-chinese-and-russian-code/) ⭐️ 8.0/10

普渡大学等机构的一项新研究发现，在面向美军推广的 220 多款应用中，近三分之二嵌入了来自中国和俄罗斯的第三方代码，其中包括华为 SDK，引发了国家安全担忧。 这暴露了军事相关应用中的软件供应链漏洞，可能使对手获取敏感数据或远程激活隐藏代码，威胁作战安全。 该研究分析了 220 多款应用，包括基地评价、制服指南、银行及约会等类型。虽然尚未观察到数据流向华为服务器，但该 SDK 可接收远程更新，可能激活潜伏的恶意代码。

telegram · zaihuapd · 7月20日 13:42

**背景**: 软件供应链安全涉及确保整合到应用程序中的第三方组件不会引入漏洞。美国军方此前曾报告对手利用商业位置数据监视中东的美军人员。华为 SDK 尤其令人担忧，因为华为已被美国政府认定为国家安全威胁。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.darkreading.com/vulnerabilities-threats/rising-tide-of-software-supply-chain-attacks">The Rising Tide of Software Supply Chain Attacks</a></li>
<li><a href="https://developer.huawei.com/consumer/en/">HUAWEI Developers</a></li>

</ul>
</details>

**标签**: `#supply chain security`, `#national security`, `#mobile apps`, `#Huawei SDK`, `#software vulnerabilities`

---

<a id="item-13"></a>
## [智谱建成全国产芯片数据中心](https://www.bloomberg.com/news/articles/2026-07-20/z-ai-completes-giant-data-center-with-chinese-chips-to-train-ai) ⭐️ 8.0/10

智谱 AI 完成了一座全部采用国产芯片、功率达 1 吉瓦的数据中心建设，这是中国 AI 实验室建造的最大规模设施之一，现已开始部分运营。 这一里程碑表明中国在无需依赖外国芯片的情况下，建设大型 AI 基础设施的能力不断增强，从而降低了对出口限制的脆弱性，并推动了国内 AI 的自给自足。 该数据中心功率达 1 吉瓦，足以供约 75 万户家庭用电，将用于支持智谱 GLM 模型系列的开发。智谱 AI 已运营多个各拥有超万枚芯片的计算集群。

telegram · zaihuapd · 7月20日 15:43

**背景**: 智谱 AI 是中国领先的人工智能公司，推出了 GLM 系列大语言模型，包括开源的 GLM-4.5 和拥有 7450 亿参数的 GLM-5。美国的制裁限制了对中国出口先进芯片（如 NVIDIA GPU），促使中国 AI 实验室使用华为昇腾、寒武纪等国产处理器开发替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Z.ai">Z. ai - Wikipedia</a></li>
<li><a href="https://glm5.ai/">GLM -5 - Zhipu AI 's Flagship Foundation Model</a></li>
<li><a href="https://glm45.org/">GLM -4.5 - by Zhipu AI</a></li>

</ul>
</details>

**标签**: `#AI`, `#datacenter`, `#domestic chips`, `#China`, `#infrastructure`

---