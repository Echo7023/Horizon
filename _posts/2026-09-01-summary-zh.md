---
layout: default
title: "Horizon Summary: 2026-09-01 (ZH)"
date: 2026-09-01
lang: zh
---

> 从 39 条内容中筛选出 25 条重要资讯。

---

1. [文件遮蔽攻击破解 Claude Code 自动模式](#item-1) ⭐️ 9.0/10
2. [谷歌将 Manifest V2 扩展（如 uBlock Origin）从 Chrome 网上应用店移除](#item-2) ⭐️ 8.0/10
3. [ChatGPT Work 技能参考：自我文档化的 Playwright 浏览器控制](#item-3) ⭐️ 8.0/10
4. [文章将 NAT 视为互联网中心化的‘原罪’](#item-4) ⭐️ 8.0/10
5. [OpenShot 4.0 发布：支持 AI 物体遮罩，界面焕然一新](#item-5) ⭐️ 8.0/10
6. [解读 ChatGPT Work：一个名字，两个产品](#item-6) ⭐️ 8.0/10
7. [动态图上的 GNN 常泄露未来边；SynthFin-AML 强制因果切分](#item-7) ⭐️ 8.0/10
8. [Claude 共享链接遭搜索引擎索引，用户数据外泄](#item-8) ⭐️ 8.0/10
9. [苹果低估 AI 对 Mac Mini 和 Mac Studio 的需求](#item-9) ⭐️ 7.0/10
10. [滑动窗口注意力在长上下文推理上胜过线性注意力](#item-10) ⭐️ 7.0/10
11. [OpenClaw 发布里程碑式 2.0 更新，汇集逾 1.6 万个拉取请求](#item-11) ⭐️ 7.0/10
12. [苹果宣布库克卸任 CEO，特努斯 2026 年接任](#item-12) ⭐️ 7.0/10
13. [DeepSeek 在 API 上线 v4-flash-vision-exp 多模态模型](#item-13) ⭐️ 7.0/10
14. [MiniMax 与智谱发布中期业绩：营收大增但仍亏损](#item-14) ⭐️ 7.0/10
15. [欧盟将 ChatGPT、Reddit、Roblox 认定为超大型服务，适用更严监管](#item-15) ⭐️ 7.0/10
16. [小米发布玄戒 O3、O100 和 D100 三款新芯片](#item-16) ⭐️ 7.0/10
17. [一个 HTML 文件构建的可步行 ASCII 赛博朋克城市](#item-17) ⭐️ 6.0/10
18. [教授对博士申请冷邮件的建议](#item-18) ⭐️ 6.0/10
19. [Entropic Scree：基于互信息的脏表格数据诊断工具](#item-19) ⭐️ 6.0/10
20. [OpenAI Codex 测试新上下文窗口策略：以换窗替代摘要压缩](#item-20) ⭐️ 6.0/10
21. [黄仁勋：AI 推动美国再工业化，初创融资 4000 亿美元](#item-21) ⭐️ 6.0/10
22. [二审维持原判：爱奇艺须为老会员恢复高清投屏](#item-22) ⭐️ 6.0/10
23. [泰国推出免费 AI 平台，开放 33 款模型，目标 500 万用户](#item-23) ⭐️ 6.0/10
24. [闻泰依据《反外国制裁法》起诉安世荷兰](#item-24) ⭐️ 6.0/10
25. [寒序科技公布 MRAM 推理产品路线，uHBM 片内带宽 24 TB/s](#item-25) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [文件遮蔽攻击破解 Claude Code 自动模式](https://embracethered.com/blog/posts/2026/breaking-claude-code-opus-5-and-automode/) ⭐️ 9.0/10

安全研究员演示了一种针对 Claude Code Opus 5 自动模式的特洛伊木马式攻击，利用文件遮蔽在攻击者控制的目录中替换标准 Python 模块。该攻击利用代理可预测的工具使用习惯（如调用 `python -c`）静默执行恶意代码。 这项研究揭示了 AI 代理执行中的一个重大安全缺陷：工作目录中的文件可能劫持受信任的工具。它强调了在 AI 编程助手中采用沙箱和更强保护措施的必要性，影响依赖自主代理模式的开发者。 该攻击利用文件遮蔽，当代码在攻击者控制的目录中运行时，恶意 `struct.py`（或类似文件）会遮蔽 Python 标准库模块。它专门针对 Claude 已知的行为模式，例如倾向于使用相同的工具和指令短语，而非一般的提示注入。

hackernews · Recursing · 8月31日 07:49 · [社区讨论](https://news.ycombinator.com/item?id=49506819)

**背景**: Claude Code 是 Anthropic 推出的代理式编程工具，能够理解代码库、编辑文件并运行命令以帮助开发者更快交付。自动模式是让代理更自主地执行任务的功能。文件遮蔽是一种技术，目录中的文件会覆盖同名模块或可执行文件，代理可能会在不知情的情况下导入或执行它们。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，该攻击利用了 Claude 特定的工具使用习惯，更像是针对 Claude 的特洛伊木马而非经典的提示注入。一些人强调沙箱是关键缓解措施，并分享了代理意外行为的轶事。还有评论者称赞攻击设计巧妙，但质疑它与自动模式的直接关联。

**标签**: `#AI safety`, `#LLM agents`, `#prompt injection`, `#security`, `#Claude Code`

---

<a id="item-2"></a>
## [谷歌将 Manifest V2 扩展（如 uBlock Origin）从 Chrome 网上应用店移除](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

谷歌已从 Chrome 网上应用店移除所有剩余的 Manifest V2 扩展，包括广受欢迎的广告拦截工具 uBlock Origin。因此，这些扩展无法再被新安装，已安装的版本也将无法获得更新。 此举影响了数百万依赖 Manifest V2 广告拦截扩展的用户，因为旧框架下的拦截效果更强。随着谷歌力推 Manifest V3，许多用户预计将迁移到 Firefox 等浏览器，以保留广告拦截能力。 Manifest V3 (MV3) 禁止远程托管代码，并引入了削弱广告和跟踪器拦截能力的限制，相比 MV2 功能有所缩减。此次从 Chrome 网上应用店移除标志着谷歌 MV2 弃用计划的最后阶段，该计划早在多年前就已分阶段推进。

hackernews · twapi · 8月31日 21:10 · [社区讨论](https://news.ycombinator.com/item?id=49514878)

**背景**: Chrome 扩展的 manifest 是一个 JSON 文件，用于定义扩展的名称、权限和功能。Manifest V2 是长期使用的旧规范，而 Manifest V3 是谷歌为提升安全性而进行的架构革新，但它移除了广告拦截器常用的某些 API 和远程代码执行能力。谷歌一直在逐步弃用 MV2，此次从应用商店移除是该过渡的高潮。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline">Manifest V2 support timeline | Chrome for Developers</a></li>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3">Extensions / Manifest V3 | Chrome for Developers</a></li>
<li><a href="https://www.theverge.com/2024/5/30/24168057/google-chrome-extension-change-manifest-v3-ad-blockers">Google will roll out Chrome’s new extension spec on June 3rd | The Verge</a></li>

</ul>
</details>

**社区讨论**: 评论者绝大多数支持转向 Firefox，称赞 uBlock Origin 在 Firefox 上的表现，并批评谷歌对互联网的控制。多名用户表示自己早已换用 Firefox，几乎没有遇到什么问题；还有人表达了对 Chrome 发展方向及谷歌单方面决策的不满。

**标签**: `#Chrome`, `#Manifest V3`, `#uBlock Origin`, `#Firefox`, `#Ad Blocking`

---

<a id="item-3"></a>
## [ChatGPT Work 技能参考：自我文档化的 Playwright 浏览器控制](https://codex-tool-reference.simonw.chatgpt.site/) ⭐️ 8.0/10

新上线的参考站点整理了 ChatGPT Work 的工具与技能；其中最引人注目的 control-browser 技能会让智能体通过 Node.js REPL 启动 Playwright，并运行 nodeRepl.write(await browser.documentation()) 在运行时获取使用说明。 这为使用 ChatGPT Work 的团队提供了实用的可复用智能体技能目录，而“自我读取文档”的浏览器控制模式也为减少 AI 浏览器自动化中的幻觉步骤提供了模板。在 OpenAI 大力推广智能体式 ChatGPT Work 功能的当下，这一参考很有价值。 该 control-browser 技能被设计为一个“驱动程序”，在用户可见的浏览器中执行确定的 Playwright 代码，而不是完全自主规划的智能体；browser.documentation() 会按需返回完整的使用说明。参考站点托管在 codex-tool-reference.simonw.chatgpt.site。

hackernews · ijidak · 8月31日 14:07 · [社区讨论](https://news.ycombinator.com/item?id=49510000)

**背景**: ChatGPT Work 是 OpenAI 推出的智能体产品，基于 GPT-5.6，通过连接工具和自动化任务帮助团队把目标转化为可交付成果。Playwright 是微软开发的浏览器自动化库，常用于测试和脚本化操作浏览器；这类 browser-control 技能通常更接近“驱动程序”，在用户可见的浏览器中执行确定的 Playwright 代码，而不是完全自主的智能体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/chatgpt-work/">ChatGPT Work for every team | OpenAI</a></li>
<li><a href="https://learn.chatgpt.com/docs/get-started-with-work">Get started with ChatGPT Work | ChatGPT Learn</a></li>
<li><a href="https://www.skills.sh/anomalyco/browser-control/browser-control">browser - control — anomalyco/ browser - control</a></li>

</ul>
</details>

**社区讨论**: 评论中，simonw 认为 control-browser 技能最有趣，尤其是它运行时自我读取文档的设计；satvikpendem 质疑它与 Codex 有何本质区别，montroser 则抱怨网站在普通尺寸屏幕上侧边栏难以滚动。enraged_camel 提出元层面的观察：AI 生成的网站似乎都有相似的视觉风格，让人想起 Bootstrap 时代的“千站一面”现象。

**标签**: `#chatgpt`, `#ai-tools`, `#browser-automation`, `#playwright`, `#llm-agents`

---

<a id="item-4"></a>
## [文章将 NAT 视为互联网中心化的‘原罪’](https://dreamstation.systems/personal/ntppost.html) ⭐️ 8.0/10

dreamstation.systems 上的一篇新文章认为，NAT 是互联网中心化最早的推手之一，因为它让客户端-服务器架构变得普遍，并使人们觉得这种模式理所当然。该文在 Hacker News 上引发热议，Linux NAT 实现者 Rusty Russell 也参与了讨论。 这篇文章挑战了‘中心化主要由商业平台造成’的常见叙事，将矛头指向一项基础网络技术。如果其观点成立，将促使工程师重新思考 IPv6 普及、点对点协议以及公共可达端点的持久价值。 作者认为，NAT 不仅让搭建服务器变得更难，还在心理上让用户接受了‘设备与云端对话’而非彼此直连的世界。评论者反驳称，普通 NAT 尚可管理，甚至可能保护了数以百万计的不安全设备，真正有害的是运营商级 NAT（CGNAT）。

hackernews · robinpie · 8月31日 02:23 · [社区讨论](https://news.ycombinator.com/item?id=49504905)

**背景**: 网络地址转换（NAT）将多个私有 IP 地址映射到一个公共 IP 地址，使许多设备可以共享同一个公网地址。由于最初的 IPv4 协议仅提供约 40 亿个地址，无法满足现代互联网的需求，NAT 因而普及。NAT 破坏了互联网原始的‘端到端’原则，使外部对等方难以主动连接 NAT 后面的设备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Network_address_translation">Network address translation - Wikipedia</a></li>
<li><a href="https://www.cisco.com/site/us/en/learn/topics/networking/what-is-network-address-translation-nat.html">What Is Network Address Translation (NAT)? - Cisco</a></li>
<li><a href="https://www.geeksforgeeks.org/computer-networks/network-address-translation-nat/">Network Address Translation (NAT) - GeeksforGeeks</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：有人同意 NAT 是开放互联网的早期杀手，也是自建服务器的体验灾难；也有人认为普通 NAT 可以接受，真正的祸害是 CGNAT。Rusty Russell 承认，他在 Linux 中的 NAT 实现优先考虑把更多连接塞进一个 IP，无意中削弱了公共端点。还有评论者指责互联网最初的设计把现实世界的安全假设套用到了网络空间。

**标签**: `#NAT`, `#Internet architecture`, `#centralization`, `#networking`, `#IPv4`

---

<a id="item-5"></a>
## [OpenShot 4.0 发布：支持 AI 物体遮罩，界面焕然一新](https://www.openshot.org/blog/2026/08/30/openshot-40-record-edit-color-like-never-before/) ⭐️ 8.0/10

开源视频编辑器 OpenShot 4.0 正式发布，引入基于 ONNX 模型的 AI 物体遮罩功能，并焕新了用户界面。此次发布表明该项目仍在持续活跃开发中。 此次发布为免费开源工具带来了先进的 AI 辅助剪辑能力，让无法负担高端付费编辑器的用户也能使用物体遮罩等功能。这也表明开源视频编辑器正紧跟行业向 AI 驱动工作流发展的趋势。 AI 物体遮罩功能依赖 ONNX 模型，并通过 OpenShot/openshot-onnx 仓库提供。界面更新使剪辑体验更加现代化，项目仍在积极维护中，拥有强大的社区支持。

hackernews · metrofun · 8月31日 09:59 · [社区讨论](https://news.ycombinator.com/item?id=49507822)

**背景**: ONNX（开放神经网络交换格式）是一种开放的机器学习模型表示格式，允许在不同框架中训练的模型在各种硬件上运行。基于 AI 的物体遮罩可自动识别并分离视频帧中的物体或人物，这一功能越来越多地出现在 Adobe Premiere 和 VEGAS Pro 等商业编辑器中。OpenShot 是一款广受欢迎的自由开源视频编辑器，已经发展了多年。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://onnx.ai/">ONNX | Home</a></li>
<li><a href="https://helpx.adobe.com/premiere/desktop/add-video-effects/work-with-masks/object-masking.html">Object Masking in Premiere (beta) | Premiere</a></li>
<li><a href="https://www.vegascreativesoftware.com/blog/smart-mask/">Smart Mask in VEGAS Pro│AI Masking and Video Editing Tool</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍欢迎此次发布，称赞界面改进以及基于 ONNX 的 AI 遮罩集成。一些用户提到了 LosslessCut、Shortcut、Blick 和 Shotstack Studio SDK 等替代工具，还有评论者表示更希望默认采用无损剪辑方式。

**标签**: `#video editing`, `#open source`, `#release`, `#AI`, `#ONNX`

---

<a id="item-6"></a>
## [解读 ChatGPT Work：一个名字，两个产品](https://simonwillison.net/2026/Aug/30/understanding-chatgpt-work/) ⭐️ 8.0/10

西蒙·威利森发表了一篇关于 OpenAI ChatGPT Work 的专家分析，澄清它实际上是两个不同的产品：通过 chatgpt.com 和移动应用访问的 Work Cloud，以及通过前身为 Codex 的桌面应用使用的 Work Local。分析还详细介绍了 Work 独有的功能，如模型选择、带互联网访问的代码执行和持久文件系统。 这很重要，因为 ChatGPT Work 被广泛认为功能强大但令人困惑，而这篇分析为开发者与高级用户提供了一张具体的地图，说明它能做什么以及何时使用。它帮助 AI 与软件工程社区理解 OpenAI 这一重要新产品，并厘清它与现有 ChatGPT 和 Codex 生态的关系。 Work 仅面向每月 20 美元及以上的付费订阅用户，其独有功能包括 GPT-5.6 Luna/Terra/Sol 模型选择、带互联网访问的代码执行环境、无头 Chrome 浏览器、持久共享文件系统、ChatGPT 站点发布和子代理会话。桌面版'Work Local'则像是为非开发者重新包装、降低门槛的 Codex。

rss · Simon Willison · 8月30日 23:59

**背景**: 2026 年 7 月，OpenAI 推出了 ChatGPT Work，这是一个可以根据连接应用和文件中的信息创建演示文稿、电子表格和其他文档的 AI 代理。Codex 是 OpenAI 的编程代理，提供 CLI、IDE 扩展、macOS 桌面应用和云运行等多种形态；如今其桌面应用已被整合进 ChatGPT Work 产品中。文章中提到的 GPT-5.6 Sol、Luna 和 Terra 等未来模型名称，似乎与 OpenAI API 中可用的模型相同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ChatGPT">ChatGPT - Wikipedia</a></li>
<li><a href="https://goodtransformer.ai/insights/what-is-chatgpt-work/">What is ChatGPT Work, and why did the launch confuse everyone? | Good Transformer</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai / codex : Lightweight coding agent that runs in your...</a></li>

</ul>
</details>

**标签**: `#ChatGPT`, `#OpenAI`, `#AI tools`, `#Product analysis`, `#Software engineering`

---

<a id="item-7"></a>
## [动态图上的 GNN 常泄露未来边；SynthFin-AML 强制因果切分](https://www.reddit.com/r/MachineLearning/comments/1w3imxy/your_gnn_is_probably_just_an_overcomplicated_mlp/) ⭐️ 8.0/10

作者发布了 SynthFin-AML v10.0——一个包含 10 万个节点、120 万条边的合成图数据集，通过严格的 3 快照因果切分使模型无法看到未来边。在严格时间切分基准上，归纳式 GraphSAGE 的 PR-AUC 达到 0.881，而调参后的 LightGBM 为 0.848。 这揭示了一个关键评估缺陷：许多在动态图上的 GNN 结果因时间泄露而被高估——模型在训练时‘看到’了未来的边。该数据集和基准提供了一种强制因果边界的方法，对于欺诈检测、金融网络和可复现的图研究至关重要。 3 快照切分将训练边限定在第 7 天之前、验证边在第 8 天之前、测试边在第 10 天之前，从而在物理上约束 GNN 的感受野。为消除表格泄露，欺诈与正常交易金额共享相同的对数正态分布（μ=8.517，σ=0.8）；该基准已作为 PyTorch Geometric PR #10774 提交上游。

reddit · r/MachineLearning · /u/Glabmayt2075 · 8月31日 16:21

**背景**: 图神经网络（GNN）通过聚合邻居的消息来更新节点嵌入；如果动态图被转成静态快照，消息传递步骤可能会把预测时间之后才出现的边纳入训练，从而泄露未来信息。这种时间泄露在金融交易网络中尤其严重，因为资金流动的方向和时序定义了因果关系。因果/时点切分可防止模型使用未来边，PyTorch Geometric 等框架在时间图场景中也推荐这种做法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kumo.ai/pyg/production/temporal-graphs/">Handling Time in Graph Neural Networks | PyG Guide | Kumo.ai</a></li>
<li><a href="https://arxiv.org/pdf/2510.25348">Beyond Leakage and Complexity: Towards Realistic and Efficient...</a></li>
<li><a href="https://github.com/valiyevoktay-cmd/synthfin-aml-">GitHub - valiyevoktay-cmd/ synthfin - aml -: A graph-native Anti-Money...</a></li>

</ul>
</details>

**标签**: `#GNN`, `#temporal leakage`, `#anti-money laundering`, `#dataset`, `#evaluation`

---

<a id="item-8"></a>
## [Claude 共享链接遭搜索引擎索引，用户数据外泄](https://t.me/zaihuapd/43511) ⭐️ 8.0/10

Claude 的共享对话功能存在严重隐私漏洞：生成的公开链接未设置禁止索引标签，导致 Google 等搜索引擎收录了大量对话页面，敏感用户数据随之暴露。Anthropic 尚未修复该问题，建议用户手动删除涉及隐私的共享记录。 这是一起影响 Claude 用户的重大隐私泄露事件，API 密钥、加密货币钱包、个人记录和机密材料均可被任何人通过搜索看到。这也凸显了 AI 平台必须默认对用户共享内容启用禁止索引策略。 泄露的信息包括 API 密钥、加密货币钱包、个人简历、律师咨询记录、公司内部项目资料及社会安全号码等敏感内容。大约一年前 ChatGPT 曾出现同类问题并迅速修复，但 Anthropic 目前尚未解决。

telegram · zaihuapd · 8月31日 03:22

**背景**: Claude 是 Anthropic 开发的一系列大语言模型及 AI 聊天机器人，于 2023 年 3 月发布。在网页发布中，noindex meta 标签或 X-Robots-Tag 响应头可告知搜索引擎不要收录页面；如果没有该标签，公开链接一旦被发现或被引用，就可能被爬取并出现在搜索结果中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI)</a></li>
<li><a href="https://www.techmagnate.com/blog/meta-robots-tag-x-robots-tag-explained/">Meta Robots Tag vs X- Robots -Tag, Key SEO Use Cases & Impact</a></li>

</ul>
</details>

**标签**: `#privacy`, `#security`, `#Claude`, `#data-leak`, `#AI`

---

<a id="item-9"></a>
## [苹果低估 AI 对 Mac Mini 和 Mac Studio 的需求](https://www.macrumors.com/2026/08/30/apple-unexpected-mac-mini-and-studio-demand/) ⭐️ 7.0/10

据一份新报道，苹果对 Mac Mini 和 Mac Studio 电脑因 AI 工作负载而出现的意外强劲需求感到措手不及。该公司低估了开发者和研究人员为本地 AI 推理和训练购买这些机器的数量。 这表明本地 AI 推理正在成为 PC 市场的重要推动力，用户开始优先考虑隐私、速度和成本控制，而非云端的便利性。同时也显示即使是大型科技公司也可能误判新兴的产品市场契合度，这可能影响苹果的供应链和未来产品方向。 该文章指出，据报道苹果没有专门面向商业客户的工程团队，没有开发者关系人员，也没有企业 AI 战略。需求激增归因于开发者和研究人员使用这些机器进行本地训练和推理工作负载，包括强化学习项目。

hackernews · thm · 8月31日 12:41 · [社区讨论](https://news.ycombinator.com/item?id=49508982)

**背景**: 本地 AI 推理是指在用户自己的设备上运行 AI 模型，而不是将数据发送到云端服务，这样可以在隐私、延迟和长期成本方面获得优势。配备 Apple 芯片和大统一内存的 Mac 尤其适合这一点，因为它们可以在没有昂贵 GPU 的情况下高效运行 LLM 等模型。然而，最强大的模型仍需要数十 GB 的存储和强大的计算能力，这意味着并非所有使用场景都能在本地处理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.merciaai.com/post/what-is-local-ai-inference-and-why-it-might-change-how-you-use-ai">What Is Local AI Inference ? (Privacy, Speed, Cost) - Mercia AI</a></li>
<li><a href="https://www.fourfoldai.com/post/on-device-ai-explained-how-ai-runs-locally-on-devices-2026-guide">On - Device AI Explained: How AI Runs Locally on Devices (2026 Guide)</a></li>
<li><a href="https://www.linkedin.com/pulse/rise-local-ai-inference-why-2026-year-move-beyond-alexander-chamandy-pdu5e">The Rise of Local AI Inference : Why 2026 Is the Year to Move Beyond...</a></li>

</ul>
</details>

**社区讨论**: 评论者的看法存在分歧：一些人强调本地硬件在强化学习等迭代工作中的价值，避免了云端准备延迟，而另一些人则怀疑当前的消费级硬件能否在一般使用中匹敌廉价的云端订阅。批评者指出，AI 驱动的需求挤占了家庭影院 PC 等其他用途，并警告一些买家可能会对模型质量问题感到失望。

**标签**: `#Apple`, `#AI hardware`, `#local inference`, `#Mac Studio`, `#developer trends`

---

<a id="item-10"></a>
## [滑动窗口注意力在长上下文推理上胜过线性注意力](https://www.reddit.com/r/MachineLearning/comments/1w3j1vw/slidingwindow_attention_beats_linear_on/) ⭐️ 7.0/10

Alexia Jolicoeur-Martineau 等人的新 arXiv 预印本(2608.28444)表明，带汇点的滑动窗口注意力(SWA)在长上下文推理任务上的表现不逊于甚至优于后训练的线性注意力模型。作者报告，在 Needle-in-a-Haystack 和 BABILong 基准上，SWA 的性能高出 2 到 10 倍。 这一结果挑战了当前通过后训练线性注意力来提升长上下文效率的研究方向，认为一个简单基线被忽视了。这可能节省大量算力，并促使业界重新评估基准和模型设计。 作者强调，带汇点的 SWA 无需后训练、运行速度快且内存占用低。他们强烈建议改用 SWA 而非后训练的线性模型，并指出线性注意力可能需要从头训练或大量后训练才能赶上 SWA。

reddit · r/MachineLearning · /u/Justgototheeffinmoon · 8月31日 16:35

**背景**: 滑动窗口注意力(SWA)通过让每个 token 只关注附近固定大小的窗口，将 Transformer 的复杂度从二次降为线性；加入注意力汇点(attention sinks)保留早期 token 以稳定生成。线性注意力方法同样追求 O(N)复杂度，但通常需要后训练或特殊内核。BABILong 是一个长上下文推理基准，用于测试模型能否在很长的干扰文本中跨分散事实进行推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.28444v1">Sliding - window beats linear attention</a></li>
<li><a href="https://www.abhik.ai/concepts/transformers/sliding-window-attention">Sliding Window Attention | Abhik Sarkar</a></li>
<li><a href="https://arxiv.org/abs/2406.10149">[2406.10149] BABILong : Testing the Limits of LLMs with Long ...</a></li>

</ul>
</details>

**标签**: `#attention mechanisms`, `#long-context`, `#LLM efficiency`, `#machine learning research`

---

<a id="item-11"></a>
## [OpenClaw 发布里程碑式 2.0 更新，汇集逾 1.6 万个拉取请求](https://openclaw.ai/blog/openclaw-2-accidentally) ⭐️ 7.0/10

OpenClaw 于 8 月 30 日发布史上最大更新 2.0，汇集了来自 933 名贡献者（其中 569 人为首次参与）的逾 1.6 万个拉取请求。此次更新覆盖安装、消息、记忆、技能、模型、浏览器、插件与安全等全部环节。 这次由社区驱动的大型发布表明 OpenClaw 开源 AI 代理生态系统的快速成长和强大参与度。简化的安装流程、重建的浏览器端体验以及新增的共享云端会话（支持多人协作）使自主 AI 助手更容易上手，并更适合广泛采用。 团队为此近七周未发布新版本以整合改动，而这 1.6 万多个拉取请求约占项目迄今全部拉取请求的一半。公告中未提供各项功能的具体技术细节。

telegram · zaihuapd · 8月31日 04:38

**背景**: OpenClaw 是一款免费开源、自主运行的 AI 代理，通过大型语言模型（LLM）执行任务，并以 WhatsApp、Telegram、Discord 等消息平台作为主要用户界面。拉取请求（Pull Request）是 GitHub 上的一种协作机制，开发者提交的代码改动会在合并前经过审查和讨论；1.6 万个拉取请求体现了极其庞大的社区贡献。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenClaw">OpenClaw - Wikipedia</a></li>
<li><a href="https://openclaw.ai/">OpenClaw — Open -Source AI Assistant</a></li>
<li><a href="https://www.hostinger.com/tutorials/what-is-github/">What Is GitHub, and How to Use It?</a></li>

</ul>
</details>

**标签**: `#OpenClaw`, `#major-release`, `#open-source`, `#community`, `#software-update`

---

<a id="item-12"></a>
## [苹果宣布库克卸任 CEO，特努斯 2026 年接任](https://t.me/zaihuapd/43516) ⭐️ 7.0/10

苹果宣布管理层交接：蒂姆·库克将于 2026 年 9 月卸任 CEO 并出任执行董事长，硬件工程高级副总裁约翰·特努斯将接任 CEO。 这是苹果自 2011 年库克接替乔布斯以来的首次 CEO 更迭，将影响公司未来十年的产品与战略方向。选择硬件高管接任，显示苹果仍将硬件创新视为核心。 董事会已一致批准该计划。现任董事长阿瑟·莱文森将于 2026 年 9 月 1 日转任首席独立董事，特努斯同日加入董事会；库克将在整个夏天继续担任 CEO，以完成过渡。

telegram · zaihuapd · 8月31日 10:21

**背景**: 苹果是全球市值最高的科技公司之一，以 iPhone、Mac 和 iPad 等产品闻名。蒂姆·库克自 2011 年起担任 CEO，接替公司联合创始人史蒂夫·乔布斯，并带领苹果发展为服务业务占比更高的企业。约翰·特努斯于 2001 年加入苹果，2013 年升任硬件工程副总裁，2021 年进入高管团队，负责 iPhone、Mac、iPad 和 AirPods 等产品的硬件研发。

**标签**: `#Apple`, `#CEO transition`, `#Tim Cook`, `#John Ternus`, `#tech industry`

---

<a id="item-13"></a>
## [DeepSeek 在 API 上线 v4-flash-vision-exp 多模态模型](https://t.me/zaihuapd/43518) ⭐️ 7.0/10

DeepSeek 已在 DeepSeek API 上线 deepseek-v4-flash-vision-exp，这是 V4 系列中首个实验性多模态视觉模型。官方文档和定价也已同步更新。 此次发布弥补了开发者通过原有文本 API 端点直接输入图像的需求缺口，使 DeepSeek 在多模态 AI 领域更具竞争力。这对依赖 DeepSeek 处理视觉-语言任务的 AI/ML 从业者尤为重要。 该模型为实验性版本，通过设置 model='deepseek-v4-flash-vision-exp' 即可调用。与 DeepSeek-V4-Flash-0731 相比，它在多模态智能体能力上取得显著提升，同时在纯文本智能体任务上保持相当的表现。

telegram · zaihuapd · 8月31日 11:41

**背景**: DeepSeek-V4-Flash-Vision-Exp 基于 DeepSeek-V4-Flash 架构，通过引入视觉模块并进行持续训练，从而获得视觉理解能力。它是 DeepSeek V4 系列中首个实验性多模态模型，开发者可直接通过原有 API 端点发送图像。该模型定位为早期实验版本，官方 DeepSeek API 平台已更新其文档和定价。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp">deepseek -ai/ DeepSeek - V 4 - Flash - Vision - Exp · Hugging Face</a></li>
<li><a href="https://api-docs.deepseek.com/updates/">DeepSeek API Docs</a></li>
<li><a href="https://zenn.dev/neotechpark/articles/ded1c59067e6ed">DeepSeek V 4 - Flash - Vision - Exp : Image Input Finally Hits the API</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#API`, `#AI`, `#Model Release`, `#Vision`

---

<a id="item-14"></a>
## [MiniMax 与智谱发布中期业绩：营收大增但仍亏损](https://ir-upload.realxen.net/iis/0100/uploads/iis/2026/12300095-0.PDF) ⭐️ 7.0/10

MiniMax 与智谱（Z.AI）发布了 2026 年上半年业绩：MiniMax 收入 1.17 亿元，同比增长 283.1%；智谱营业收入 9.54 亿元，同比增长 399.7%。两家公司目前仍处于亏损状态，但净亏损同比均有所收窄。 这两份业绩显示，中国领先的 AI 创业公司正在通过 MaaS 和 API 服务快速商业化，同时仍在大量投入。收入与 API 业务的爆发式增长表明中国企业级市场对国产大模型的采用在增加，也意味着全球 AI 市场竞争进一步加剧。 智谱云端部署收入占比提升至 86.5%，开放平台及 API 业务收入同比增长超 27 倍；MaaS 平台用户数超 740 万，较年初增长 144%，付费日活用户增长 603%。MiniMax 期内亏损 3.58 亿元，同比收窄 11%；智谱归母净亏损 20.71 亿元，同比收窄 12.1%，经调整净亏损率同比收窄 3.5 倍。

telegram · zaihuapd · 8月31日 13:11

**背景**: MaaS（模型即服务）通过云端 serverless API 和按量付费方式提供 AI 模型，企业无需管理底层基础设施即可集成 AI。MiniMax、智谱等中国 AI 创业公司正越来越多地依靠 MaaS 和 API 收入来实现大模型商业化，但由于模型训练和部署投入巨大，目前仍处于亏损状态。这两份 2026 年上半年业绩正体现了中国 AI 行业的商业化趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-models-as-a-service-maas">What is Model as a Service (MaaS)? - Microsoft Azure</a></li>
<li><a href="https://www.redhat.com/en/topics/ai/what-is-models-as-a-service">What is Model-as-a-Service? - Red Hat</a></li>

</ul>
</details>

**标签**: `#AI industry`, `#financial results`, `#MiniMax`, `#Zhipu`, `#MaaS`

---

<a id="item-15"></a>
## [欧盟将 ChatGPT、Reddit、Roblox 认定为超大型服务，适用更严监管](https://www.euronews.com/next/2026/08/31/eu-places-chatgpt-reddit-and-roblox-under-strictest-digital-safety-rules) ⭐️ 7.0/10

2026 年 8 月 31 日，欧盟委员会依据《数字服务法》将 ChatGPT 认定为超大型在线搜索引擎，并将 Reddit 和 Roblox 认定为超大型在线平台，原因是三者在欧盟的月均活跃用户均超过 4500 万。三者现在面临更严格的安全和透明度义务，并有四个月的过渡期来合规。 此举将欧盟数字监管扩展至 AI 驱动的服务和大型社区平台，开创了将具备联网搜索功能的 AI 聊天机器人视为搜索引擎的先例。同时，它迫使 ChatGPT、Reddit 和 Roblox 主动处理非法内容、未成年人保护和用户身心健康问题，影响其在欧洲的产品设计和运营。 这三项服务有四个月时间开展年度系统性风险评估、接受独立审计，并与监管机构及经审核的研究人员共享数据，重点涉及非法内容、未成年人保护和用户心理健康。欧盟委员会还将监督其合规情况，且这些 DSA 义务是在 GDPR 和《人工智能法案》等其他适用欧盟规则之外的附加要求。

telegram · zaihuapd · 8月31日 14:39

**背景**: 《数字服务法》（DSA）是欧盟针对在线平台制定的统一规则，其中对每月欧盟用户超过 4500 万的超大型在线平台（VLOPs）和超大型在线搜索引擎（VLOSEs）规定了额外义务。这些义务包括系统性风险评估、透明度报告，以及降低虚假信息和危害未成年人等风险的措施。由于 ChatGPT 的实时联网功能让用户能像使用传统搜索引擎一样获取信息，因此被归类为搜索引擎。欧盟此前已认定谷歌、Meta 和亚马逊等主要服务属于 DSA 监管范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://digital-strategy.ec.europa.eu/en/faqs/digital-services-act-questions-and-answers">Digital Services Act: Questions and Answers | Shaping Europe’s digital...</a></li>
<li><a href="https://www.theverge.com/23845672/eu-digital-services-act-explained">The EU’s Digital Services Act is now in effect... | The Verge</a></li>
<li><a href="https://arxiv.org/pdf/2601.17064">Between search and platform: ChatGPT under the DSA</a></li>

</ul>
</details>

**标签**: `#DSA`, `#EU regulation`, `#ChatGPT`, `#Reddit`, `#Roblox`

---

<a id="item-16"></a>
## [小米发布玄戒 O3、O100 和 D100 三款新芯片](https://t.me/zaihuapd/43524) ⭐️ 7.0/10

小米发布了三款新的玄戒芯片：AI 旗舰 SoC 玄戒 O3、带宽达 1.22 TB/s 的高带宽 AI 加速芯片玄戒 O100，以及国内首款 3nm 智驾 AI 芯片玄戒 D100。三款芯片均完成回片验证，覆盖人车家全生态的端侧 AI 算力需求。 这标志着小米从智能手机向定制 AI 加速芯片和自动驾驶芯片的拓展，增强了其垂直整合能力，以及相对于其他移动和汽车芯片厂商的竞争力。玄戒 O3 全球首发支持 LPDDR6，以及采用 3nm 工艺的 D100，也凸显了中国在先进半导体设计上的快速进步。 玄戒 O3 采用十核全大核 CPU，多核跑分突破 15000 分，并首发 G2-Ultra NX GPU，官方称性能提升 85%、功耗降低 64%。它还是全球首款支持 LPDDR6 内存的移动处理器；O100 加速芯片采用面向端侧大模型的 6nm 晶圆级架构。

telegram · zaihuapd · 8月31日 15:15

**背景**: 玄戒是小米自研芯片系列，用于手机、汽车和 AI 终端设备。O3 的 GPU G2-Ultra NX 被描述为 16 核 Arm Mali-G2 Ultra NX，支持 AI 超分和帧生成；其 LPDDR6 支持与 JEDEC 发布的新内存标准一致，该标准旨在提升移动设备和 AI 的内存性能。D100 是国内首款 3nm 自动驾驶 AI 芯片，体现了国产芯片设计的进一步突破。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.jedec.org/news/pressreleases/jedec®-releases-new-lpddr6-standard-enhance-mobile-and-ai-memory-performance">JEDEC® Releases New LPDDR6 Standard to Enhance Mobile and AI Memory Performance | JEDEC</a></li>
<li><a href="https://gadgets.beebom.com/guides/xiaomi-xring-o3-benchmark-specs">Xiaomi Xring O3: Benchmarks and Specs | Beebom Gadgets</a></li>
<li><a href="https://www.aibase.com/news/30572">Xiaomi Releases Xuanjie O100 Chip , With the Highest Edge-side...</a></li>

</ul>
</details>

**标签**: `#Xiaomi`, `#SoC`, `#AI chip`, `#semiconductor`, `#autonomous driving`

---

<a id="item-17"></a>
## [一个 HTML 文件构建的可步行 ASCII 赛博朋克城市](https://www.youtube.com/watch?v=3YtygAx_C6A) ⭐️ 6.0/10

一段新视频展示了一个完全包含在单个 HTML 文件中的、可步行的第一人称 ASCII 赛博朋克城市。该项目使用种子化的 2.5D 纹理 DDA 光线投射引擎，以字符作为霓虹黑底画面中的纹素。 这凸显了基于浏览器的等宽字符艺术和光线投射技术的创造潜力。它可能激励其他开发者仅用 HTML 文件就能构建复古风格的 3D 体验，并随处运行。 该城市是种子化的，因此布局是可复现的，光线投射引擎使用 DDA 算法进行 2.5D 渲染。视频本身展示了最近的更新，包括交通、室内、海拔和高层建筑，但一些观众报告说实际运行效果与视频中不同。

hackernews · keithcarolus · 8月31日 18:21 · [社区讨论](https://news.ycombinator.com/item?id=49512975)

**背景**: ASCII 艺术使用 ASCII 标准中的字符来创作图像，当动画化或实时渲染时，可以模拟 3D 环境。光线投射是一种渲染技术，它从观察者出发，穿过网格追踪光线，将 3D 场景投影到 2D 屏幕上，从而实现高效的伪 3D 效果，类似早期游戏如《德军总部 3D》中的效果。在浏览器中实现这一点，可以让创作者精确控制字体和布局，而且结果无需安装即可运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=3YtygAx_C6A">A Walkable ASCII Cyberpunk City in One HTML File - YouTube</a></li>
<li><a href="https://github.com/ludthor/ascii-city">GitHub - ludthor/ ascii - city : Seeded walkable first-person ASCII ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ray_casting">Ray casting - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体持积极态度，有人称赞浏览器是制作等宽字符艺术的更优平台，也有人对索尼克的星光地带感到怀旧。然而，有用户报告实际版本与视频效果不符，还有人对 GitHub 项目与视频是否同步提出疑问；另有一条评论指出该帖子是重复内容。

**标签**: `#ASCII art`, `#creative coding`, `#browser graphics`, `#cyberpunk`, `#HTML`

---

<a id="item-18"></a>
## [教授对博士申请冷邮件的建议](https://www.reddit.com/r/MachineLearning/comments/1w3bwci/cold_emailing_profs_about_phd_positions_read_this/) ⭐️ 6.0/10

一位机器学习教授在 Reddit 上分享了关于博士申请者冷邮件常见错误的建议，包括群发邮件、列出泛泛的研究兴趣、将 workshop 论文冒充会议论文，以及过度使用 LLM 进行研究思考。 这些建议对准备申请博士的学生和教授都很有意义，因为它反映了人们对 AI 生成申请材料的担忧日益增加，以及精准、诚实沟通的重要性。学生遵循这些指南可以提高成功率，教授也能减少筛选不合适邮件的时间。 这位教授特别提醒不要将 workshop 论文冒充会议论文、不要用 LLM 生成研究方向，也不要忽视导师网站上的联系指示。相反，建议展示你如何在其研究基础上进行拓展，而不是复述论文内容。

reddit · r/MachineLearning · /u/tariban · 8月31日 12:09

**标签**: `#PhD applications`, `#cold emailing`, `#machine learning`, `#academic career`, `#advice`

---

<a id="item-19"></a>
## [Entropic Scree：基于互信息的脏表格数据诊断工具](https://www.reddit.com/r/MachineLearning/comments/1w3br9c/how_to_assess_if_there_is_a_strong_signal_in_your/) ⭐️ 6.0/10

这篇 Reddit 帖子介绍了 Entropic Scree，一种新的诊断工具，它使用转换后的互信息度量来估计高维真实表格数据中的信号强度、信噪比、内在秩和线性度。目前 R 函数已可用，后续将发布 Python 和 R 包。 标准 PCA 和基于方差的诊断在高维脏数据上往往失效，因为它们依赖线性假设和距离度量。通过提供一种对假设要求更低的信号质量测量方法，Entropic Scree 可帮助从业者判断未清洗的数据何时仍可用于预测建模，并与“从垃圾到黄金”（From Garbage to Gold）框架互补。 该方法评估的是转换后的互信息度量，而非线性方差、秩次或欧氏距离，并且能生成识别变量解耦子网络的探索性图谱。完整技术细节见预印本（DOI 10.5281/zenodo.22028087），R 函数现已在 GitHub 上提供。

reddit · r/MachineLearning · /u/Chocolate_Milk_Son · 8月31日 12:02

**背景**: 互信息衡量知道一个变量能在多大程度上减少对另一个变量的不确定性，能够捕捉相关性无法体现的非线性关系。相比之下，主成分分析（PCA）假设重要结构是线性方差，因此在数据包含错误、离群值或混合尺度时很脆弱。Entropic Scree 建立在“从垃圾到黄金”框架之上，该框架研究何时嘈杂、未经整理的数据仍可用于构建准确的预测模型。该工具专为建模前的探索性数据分析设计，可快速判断数据集是否具有足够的信号。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/tjleestjohn/Entropic-Scree">GitHub - tjleestjohn/ Entropic - Scree : Overcome the limits of standard...</a></li>
<li><a href="https://arxiv.org/html/2603.12288">From Garbage to Gold : A Data-Architectural Theory of Predictive...</a></li>

</ul>
</details>

**标签**: `#data diagnostics`, `#mutual information`, `#tabular data`, `#signal-to-noise`, `#PCA`

---

<a id="item-20"></a>
## [OpenAI Codex 测试新上下文窗口策略：以换窗替代摘要压缩](https://github.com/openai/codex/pull/27488) ⭐️ 6.0/10

OpenAI 正在 Codex 中测试一种新的上下文窗口管理方案：不再用摘要压缩历史，而是直接切换到全新窗口，并借助历史记录与笔记保持连续性。相关改动出现在 PR #27488、#29743 和 #39827 中，目前仍在开发阶段。 这有望减少长编码会话中的 token 消耗和细节丢失，解决基于 LLM 的智能体面临的一个关键瓶颈。如果成功，可能会影响其他编程助手处理上下文限制的方式。 在新方案下，模型可以主动申请换窗，手动/自动清理也统一走新窗口流程，不再生成摘要。配套的历史记录与笔记功能使模型在换窗后能按需找回此前内容、延续工作状态，避免任务中断。

telegram · zaihuapd · 8月31日 00:02

**背景**: LLM 的上下文窗口是指模型在单次输入中最多能处理的文本量（以 token 计）。传统的摘要式压缩会把对话历史浓缩成摘要，但这会消耗 token 且可能丢失重要细节。Codex 是 OpenAI 的编程智能体，它正在尝试一种不同策略：结束当前窗口并开启新窗口，同时借助外部历史记录和笔记来保持连续性。这也是改进 LLM 工具长上下文处理的更广泛尝试之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@tahirbalarabe2/what-is-llms-context-window-understanding-and-working-with-the-context-window-641b6d4f811f">What is LLM ’s Context Window ?:Understanding and... | Medium</a></li>
<li><a href="https://www.emergentmind.com/topics/context-compression-techniques">Context Compression Techniques</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Codex`, `#context window`, `#LLM`, `#coding agent`

---

<a id="item-21"></a>
## [黄仁勋：AI 推动美国再工业化，初创融资 4000 亿美元](https://x.com/JensenHuang/status/2094173025881272408) ⭐️ 6.0/10

黄仁勋在 X 上发文称，AI 正把制造业带回美国，推动美国在数十年外包后重新工业化。他还提到，过去六个月 AI 初创企业获得了 4000 亿美元投资。 这一表态反映出 AI 行业领袖正将 AI 塑造为工业政策的核心驱动力，并将其与电网、芯片厂和数据中心领域的投资联系起来。对政策制定者、建设者和社区而言，这意味着 AI 发展将与本土就业和基础设施建设紧密挂钩。 帖文称，AI 驱动的需求正带动老化电网和可持续能源投资，并催生能源、芯片和数据中心相关的建设与制造岗位。帖文未提供 4000 亿美元这一数字的详细来源或统计方法。

telegram · zaihuapd · 8月31日 01:00

**背景**: 几十年来，美国将大量制造业外包到海外。AI 的快速发展需要庞大的计算基础设施，包括芯片制造厂和数据中心，而这些设施需要大量电力，因此推动了新建能源产能和电网升级的需求。黄仁勋是 AI 芯片领军企业 NVIDIA 的 CEO，他的言论反映了行业对 AI 带动实体基础设施投资的预期。

**标签**: `#AI`, `#制造业`, `#投资`, `#NVIDIA`, `#再工业化`

---

<a id="item-22"></a>
## [二审维持原判：爱奇艺须为老会员恢复高清投屏](https://t.me/zaihuapd/43510) ⭐️ 6.0/10

11 月 6 日，爱奇艺限制投屏案二审维持原判。爱奇艺须在老会员有效期内持续提供高清投屏服务，并补偿 41 天黄金会员时长。 该裁决为中国流媒体平台用户权益确立了法律先例，确认平台不能单方面降低对现有付费会员的服务质量。这可能促使其他受影响用户寻求类似补偿，并推动平台遵守最初的服务承诺。 原告朱元指出，虽然该判决是针对他的个案，但作为平台方的爱奇艺面向的是全体同等情形的会员。他希望爱奇艺能在判决生效后以公告方式对全体受损会员作出同等补偿。

telegram · zaihuapd · 8月31日 02:41

**背景**: 投屏技术允许用户通过专门的应用程序（如 LetsView、DouWan）或内置协议将手机或电脑屏幕镜像到电视等更大的显示屏上。爱奇艺等流媒体平台曾对部分用户限制高清投屏功能，从而引发消费者诉讼。该案突显了中国数字市场中平台削减成本与消费者权益之间的持续矛盾。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://letsview.com/screen-mirroring">LetsView | Free Screen Mirroring App</a></li>
<li><a href="https://douwan.tv/">DouWan - Plug and Play Screen Mirroring for Your Phone</a></li>

</ul>
</details>

**标签**: `#iQIYI`, `#legal ruling`, `#consumer rights`, `#streaming platform`, `#China`

---

<a id="item-23"></a>
## [泰国推出免费 AI 平台，开放 33 款模型，目标 500 万用户](https://thethaiger.com/hot-news/technology/thailand-ai-passport-launches-today) ⭐️ 6.0/10

泰国数字经济与社会部于 8 月 31 日上午 9 时正式上线 TH-AI 通平台，免费向用户提供来自 14 家服务商的 33 款 AI 模型，并设定 500 万注册用户的目标。 这标志着国家层面大力推动 AI 普及，可能加快泰国全民的 AI 素养和应用水平。同时，也为其他希望利用 AI 服务公众的新兴经济体提供了范例。 该平台仅面向年满 15 岁的泰国公民开放。这 33 款模型覆盖图像生成、视频创作、音乐制作、编程与建站等应用场景。

telegram · zaihuapd · 8月31日 07:55

**背景**: 泰国政府一直在推动人工智能的采用，将其作为数字经济战略的一部分。泰国首部《人工智能法》草案目前正公开征求意见。业内估计泰国 AI 市场规模约为 500 亿泰铢，其中超过 400 亿泰铢依赖外国技术。

**标签**: `#AI`, `#Thailand`, `#Government Platform`, `#AI Adoption`, `#Policy`

---

<a id="item-24"></a>
## [闻泰依据《反外国制裁法》起诉安世荷兰](https://t.me/zaihuapd/43519) ⭐️ 6.0/10

闻泰科技已向广东省东莞市中级人民法院起诉安世荷兰，法院已正式立案。该公司依据《反外国制裁法》提出反制裁诉讼，要求确认对方行为违法、恢复核心资产控制权，并提出损害赔偿请求。 此案是《反外国制裁法》能否被用于中国母公司与其外国子公司之间的民事诉讼的一次重要检验，可能为跨境科技治理树立先例。同时，它也凸显了半导体供应链日益加剧的地缘政治压力，因为安世的元器件对全球汽车行业至关重要。 诉讼在广东省法院提起，核心针对闻泰所称安世荷兰的“不当干预”，具体行为尚未披露。闻泰主要诉求包括请求法院确认对方行为违法、恢复对核心资产的控制权，以及赔偿损失。

telegram · zaihuapd · 8月31日 12:26

**背景**: 安世半导体是一家总部位于荷兰奈梅亨的半导体制造商，产品包括晶体管、二极管和 MOSFET 等汽车电子中广泛使用的关键元器件。中国的《反外国制裁法》于 2021 年 6 月通过，为反制外国制裁和歧视性措施建立了法律框架，但该法主要由国家机构实施。闻泰科技是一家中国上市公司，与安世半导体存在股权关联，因此这起民事诉讼是该法一次非同寻常的应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anti-Foreign_Sanctions_Law">Anti-Foreign Sanctions Law</a></li>
<li><a href="https://www.nexperia.com/">Nexperia : Global semiconductor company</a></li>
<li><a href="https://boardor.com/blog/discussing-chips-through-the-nexperia-incident">Discussing Chips through the " Nexperia Incident" - Boardor</a></li>

</ul>
</details>

**标签**: `#legal dispute`, `#semiconductor`, `#anti-sanctions law`, `#business conflict`, `#tech company`

---

<a id="item-25"></a>
## [寒序科技公布 MRAM 推理产品路线，uHBM 片内带宽 24 TB/s](https://mp.weixin.qq.com/s/adyFanNueXUHKnxr9m64kg) ⭐️ 6.0/10

寒序科技自称国内首家 MRAM 磁计算公司，公布了 uHBM 与 uLPU 推理计算架构。首代 uHBM 的片内读带宽设计值为 24 TB/s，uLPU 面向 4B 多模态模型提出超过 2000 tokens/s 的解码目标。 该路线提出了一种以存储为中心的推理方案，将模型权重常驻于持久性 MRAM，避免权重重复搬运，有望替代 GPU 为主的推理路线。若实现，可降低 AI 推理的功耗和时延，尤其适用于边缘和数据中心场景，并强化国内 MRAM 供应链。 模型权重驻留在 Persistent MRAM 阵列中，并在同片完成矩阵-向量运算，减少权重重复搬运。验证芯片 SpinPU-ED01 已通过第三方检测和 24 小时稳定运行验证，产品路线覆盖芯片、2U Tray 及 Rack 整机。

telegram · zaihuapd · 8月31日 13:41

**背景**: MRAM（磁阻随机存取存储器）通过磁性状态而非电荷存储数据，具有非易失性，并可在片上集成时提供比 DRAM 更高的带宽和更低的时延。已有研究探索将片上 MRAM 作为 DRAM 物理内存的高带宽替代方案。持久性 MRAM 还被用于 CXL 内存池和边缘 AI 硬件，可将模型权重与中间状态直接存储在 MRAM 中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Magnetoresistive_RAM">Magnetoresistive RAM - Wikipedia</a></li>
<li><a href="https://user.it.uu.se/~erikhage/courses/tic/Papers/Lecture2/Extra:Desikan02.pdf">mram _techrep.dvi</a></li>
<li><a href="https://www.prodigitalweb.com/beginner-guide-to-magnetoresistive-ram-mram/">Beginner Guide To Magnetoresistive RAM ( MRAM )... | ProDigitalWeb</a></li>

</ul>
</details>

**标签**: `#MRAM`, `#AI Inference`, `#Hardware`, `#uHBM`, `#uLPU`

---