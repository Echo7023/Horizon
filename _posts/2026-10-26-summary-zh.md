---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 28 条内容中筛选出 15 条重要资讯。

---

1. [PHP 紧急发布补丁，修复两项严重未授权远程代码执行漏洞](#item-1) ⭐️ 9.0/10
2. [十年前的 Inception 卷积网络在皮肤癌诊断上胜过前沿大模型](#item-2) ⭐️ 8.0/10
3. [Dan Luu 呼吁开发者构建更有野心的软件](#item-3) ⭐️ 8.0/10
4. [Cerebras 在晶圆级硬件上部署万亿参数模型](#item-4) ⭐️ 8.0/10
5. [memt-1.0 用门控 DeltaNet-2 内化智能体记忆，存储缩减 66 倍](#item-5) ⭐️ 7.0/10
6. [搜狗输入法 OPPO 定制版被 Google Play 保护机制标记为风险应用](#item-6) ⭐️ 7.0/10
7. [苹果将于周三发布首款触屏 MacBook Pro，搭载 OLED 屏幕](#item-7) ⭐️ 7.0/10
8. [演讲者呼吁抵制互联网审查，将在 FOSDEM 发表演讲](#item-8) ⭐️ 6.0/10
9. [Show HN 项目把员工“小人”放进标普 500 市值气泡图](#item-9) ⭐️ 6.0/10
10. [开源《魔法门之英雄无敌 2》引擎 fheroes2 登上 Hacker News，引发怀旧讨论](#item-10) ⭐️ 6.0/10
11. [Nanbeige 发布 Nanbeige4.3-33B：面向小型智能体的 Apache 2.0 教师模型](#item-11) ⭐️ 6.0/10
12. [工信部拟推汽车灯光强制性国标：智驾小蓝灯统一为蓝绿色](#item-12) ⭐️ 6.0/10
13. [GPU 租赁价格全面上涨，老款 A100 也不例外](#item-13) ⭐️ 6.0/10
14. [特斯拉自研 AI 地图将随 FSD v15 推送](#item-14) ⭐️ 6.0/10
15. [GEEKCON 上海站无人机攻防赛题引发厂商报警，赛事一度暂停](#item-15) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [PHP 紧急发布补丁，修复两项严重未授权远程代码执行漏洞](https://t.me/zaihuapd/44678) ⭐️ 9.0/10

PHP 团队紧急发布安全更新，包括 PHP 8.5.12、8.4.27、8.3.36 和 8.2.35，修复两项允许攻击者在无需登录的情况下远程执行任意代码的漏洞，两项漏洞的 CVSS 4.0 评分均为 9.2 分。所有处理网页请求的 PHP 部署均受影响，涵盖 PHP-FPM、Apache 的 mod_php、php-cgi、FrankenPHP 和 LiteSpeed。 PHP 支撑着互联网的庞大份额——WordPress、Drupal、Laravel 以及无数自建应用——因此运行时本身出现未授权远程代码执行漏洞属于范式级别的安全事件：即使应用代码毫无缺陷也必须打补丁。由于已证实 mod_php 场景下攻击可在网站业务代码运行前触发，主机服务商、系统管理员以及所有通过 Web 服务器运行 PHP 的用户都必须立即升级。 mod_php 风险最高，已有验证表明攻击可在网站业务代码运行前触发，也就是说仅凭存在漏洞的模块就足以被攻陷。修复覆盖四个受支持的分支，因此管理员需要确认自己所用的具体小版本号，而不能想当然认为装得较新就安全。

telegram · zaihuapd · 10月25日 02:42

**背景**: PHP 是一种服务端脚本语言，通常通过 SAPI（服务器应用编程接口）层运行在 Web 服务器之后。PHP-FPM 是一个 FastCGI 进程管理器，维护一组工作进程并从 Web 服务器接收请求；mod_php 则把 PHP 解释器直接嵌入 Apache；php-cgi 是较早的 CGI 方式；FrankenPHP 是构建于 Caddy 之上的新型应用服务器，将 PHP 嵌入 Go 进程，无需 PHP-FPM。由于这些层位于应用代码之前，运行时或 SAPI 中的缺陷可以被精心构造的请求触发，且无需任何有效凭证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.php.net/manual/en/install.fpm.php">PHP: FastCGI Process Manager (FPM) - Manual</a></li>
<li><a href="https://www.zend.com/blog/apache-phpfpm-modphp">Configuring Apache HTTPD With PHP - FPM and mod _ php | Zend</a></li>
<li><a href="https://frankenphp.dev/">FrankenPHP : the modern PHP app server</a></li>

</ul>
</details>

**标签**: `#security`, `#php`, `#vulnerability`, `#remote-code-execution`, `#patching`

---

<a id="item-2"></a>
## [十年前的 Inception 卷积网络在皮肤癌诊断上胜过前沿大模型](https://lynchlab.net/llm-skin-cancer) ⭐️ 8.0/10

皮肤科医生 Magnus Lynch 用 200 个经活检确认的皮肤病变，对比了 GPT-6 Astra、Claude Fable 5.1 与一个微调过的 Inception v3，结果这个十年前的卷积网络对 125 个病变给出了正确诊断（62%），而前沿大模型约为 42%。该 CNN 在单块 H100 GPU 上用 ISIC Archive 的 68,011 张皮肤镜与临床图像训练，训练前已剔除全部测试病变以及同一病变或同一患者的任何其他图像。 这一结果挑战了“越来越大的通用模型终将取代专用系统”的假设，并表明在医学影像这类狭窄而高风险的任务上，小型专用分类器仍可能更准确、运行成本也低得多。它还促使人们重新审视多模态大模型基准的构建方式，以及所谓“临床能力”究竟意味着什么。 标题中的对比是 200 个病变测试集上的 top-1 诊断准确率，样本量偏小、置信区间很宽；评论者指出该模型经过严格的数据隔离与阈值设定流程——做法规范，但也可以说是一个为基准量身打造的设置。批评者还指出，网络架构虽已十年，但训练是近期完成的，因此标题略微夸大了“老模型取胜”的意味。

hackernews · sungam · 10月25日 17:15 · [社区讨论](https://news.ycombinator.com/item?id=50233779)

**背景**: Inception 由 Google 研究人员于 2014 年以 GoogLeNet 之名提出，是一系列用于计算机视觉的卷积神经网络，其 Inception 模块并行使用多种尺寸的卷积核，从而以较低算力高效提取特征。微调指的是取一个已在普通照片上预训练好的网络，继续用特定领域的数据训练其全部层，这里的领域数据是来自 ISIC Archive 的皮肤镜图像——该档案是皮肤科 AI 研究中广泛使用的大型公开皮肤病变图像库。前沿大模型则是在互联网规模通用数据上训练的多模态模型，因此这项对比是“窄领域专家”与“通才”之间的较量，而非同类模型的两代之争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lynchlab.net/llm-skin-cancer">A 10-year-old CNN outperforms frontier LLMs for skin cancer ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Inception_(deep_learning_architecture)">Inception (deep learning architecture) - Wikipedia</a></li>
<li><a href="https://explainx.ai/blog/cnn-beats-gpt-6-astra-claude-fable-5-1-skin-cancer-diagnosis-lynch-2026">CNN vs GPT-6 Astra vs Fable 5.1: Skin Cancer, 62% vs 42% ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者大多并不惊讶专用分类器能胜过通用模型，不少人认为真正的启示是用大模型低成本地构建窄领域、高精度的模型，而不是在大规模应用中直接部署大模型。也有人反驳这种叙事，称该实验属于“刷榜”（benchmaxxing），并指出架构虽老但训练是新的；还有一派认为这种比较忽视了大模型真正的潜力——结合临床病历、主动追问患者信息，以及处理杂乱、分布外的图像。

**标签**: `#medical-ai`, `#LLMs`, `#CNNs`, `#benchmarking`, `#model-specialization`

---

<a id="item-3"></a>
## [Dan Luu 呼吁开发者构建更有野心的软件](https://danluu.com/ambitious/) ⭐️ 8.0/10

Dan Luu 发表了题为《We should be more ambitious with the software we build》的文章，主张开发者应当追求真正有野心的软件，而不是满足于渐进式改进或局部优化的工作。该文登上 Hacker News 首页，获得约 707 分和 645 条评论。 这篇文章及其引发的讨论折射出一场日益扩大的争论：AI 辅助编程究竟是在产出浅层的局部优化工作，还是真正的工程成果，而这一问题直接影响团队如何评估大语言模型带来的生产力提升。文章同时也对业界一种常见做法提出质疑，即把狭窄的性能提升（更快的数据库或正则引擎）当作衡量进步的主要标准。 该文属于观点评论，而非技术发布或基准测试，因此其论断本质上带有论辩色彩，其价值很大一部分来自它激发的社区回应。评论者分成两派：一方认为 AI 代码生成让长期搁置的副业项目终于得以实现；另一方则反映 LLM 生成的代码往往过拟合于测试过的用例，性能上难以泛化到其他场景，后续维护也很困难。

hackernews · ltratt · 10月24日 21:47 · [社区讨论](https://news.ycombinator.com/item?id=50225695)

**背景**: Dan Luu 是一位软件工程师兼长期博客作者，以注重实证的文章著称，内容涵盖软件性能、工程生产力研究，以及业界对质量的谈论与实际构建系统之间的落差。Hacker News 是由 Y Combinator 运营的技术链接分享社区，投稿按点赞和分数排名，其评论区常常演变为围绕某篇文章的实质性辩论。社区中提到的“更快的马”典故源自关于 Henry Ford 的一段传说：如果他问顾客想要什么，顾客只会说想要更快的马，这里用来论证优化现有工具只是替代了重新思考问题本身。

**社区讨论**: 整体讨论参与度很高，但观点分歧明显。一些评论者认为 AI 辅助编程容易产出杂乱且过拟合的代码，性能上无法泛化，也难以应对未来变更；另一些人则反驳说真正的收益在于“野心”——一位开发者描述自己借助 AI 为 Kobo 阅读器构建了电子墨水 SDK 与应用生态，而这类工作过去一直没有时间去做。还有讨论指出“更快的 Postgres／正则引擎”恰恰就是“更快的马”这一谬误，另有评论者观察到在技术圈之外，现实世界的软件质量依然糟糕，例如消费级热泵的固件。

**标签**: `#software-engineering`, `#essay`, `#developer-culture`, `#AI-code-generation`, `#hackernews-discussion`

---

<a id="item-4"></a>
## [Cerebras 在晶圆级硬件上部署万亿参数模型](https://www.cerebras.ai/blog/how-we-deploy-trillion-parameter-frontier-models-on-cerebras) ⭐️ 8.0/10

Cerebras 发布技术博客，详细介绍了它如何在自家晶圆级硬件上部署并提供万亿参数级前沿模型的推理服务，该文章在 Hacker News 上引发热议，获得 337 分和 119 条评论。公司借此表明其 CS-3 级系统能够承载当前最大规模的模型推理，而不仅限于较小的开源模型。 万亿参数模型的推理通常是系统级难题，需要大规模多 GPU 集群以及复杂的张量与流水线并行，因此用单块晶圆级引擎完成这一任务是一项有意义的基础设施里程碑。这在商业上同样重要：如果 Cerebras 能以远超 GPU 的 token 吞吐量提供前沿级质量，它就会成为延迟敏感型工作负载中 GPU 推理服务商的可靠替代方案。 Cerebras 的优势来自 WSE-3 代芯片，它在单块晶圆上集成了约 4 万亿个晶体管和 90 万个面向 AI 优化的核心，并配备片上内存与极高的内部带宽，从而避免了集群 GPU 之间的互连瓶颈。评论者提出的主要顾虑是模型的新鲜度与质量：普通用户实际能访问的多是较小的开源模型，且至少有一位测试者反馈 tokens 每秒极高但经常答错。

hackernews · gmays · 10月25日 01:33 · [社区讨论](https://news.ycombinator.com/item?id=50227356)

**背景**: 晶圆级集成（WSI）指的是不把硅晶圆切割成许多小芯片，而是直接用整片晶圆做成一颗巨型芯片，以制造难度换取极大的片上带宽与内存容量。Cerebras 是最知名的商业化实践者，将 WSE 芯片封装在 CS-3 系统中，作为成排 GPU 的替代方案出售。万亿参数模型是大型语言模型中规模最大的一类，参数量在 1 万亿左右或以上，为其提供推理服务需要在快速内存中容纳海量权重，同时让计算单元保持忙碌。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Wafer-scale_integration">Wafer-scale integration</a></li>
<li><a href="https://www.cerebras.ai/chip">Cerebras WSE-3 Turbo | Wafer-Scale AI Chip</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的情绪褒贬不一且明显偏批判：有人认为 Cerebras 比前沿实验室落后约 6 至 9 个月，但仍能以低得多的成本、快得多的速度提供接近前沿的模型；另一些人则反驳说晶圆产能有限使其无法满足需求，且可访问的 GPT-OSS-120B 等模型虽快却容易出错。一位有实际合作经验的评论者称其技术非凡但团队能力不足，还有人从技术角度追问数据如何在芯片的二维处理单元网格中流动。

**标签**: `#cerebras`, `#wafer-scale`, `#llm-inference`, `#ai-infrastructure`, `#model-serving`

---

<a id="item-5"></a>
## [memt-1.0 用门控 DeltaNet-2 内化智能体记忆，存储缩减 66 倍](https://www.reddit.com/r/MachineLearning/comments/1xeu0ht/memt10_architecture_breakdown_gated_deltanet2/) ⭐️ 7.0/10

r/MachineLearning 上的一篇技术拆解介绍了 memt-1.0 的记忆原生架构：它通过门控 DeltaNet-2 和 mixture-of-storage（MoS）层，把智能体记忆内化到模型计算中，而不是依赖追加式提示或外部 RAG 流水线。在 128k token 历史长度下，memt-1.0-nano 相比完整上下文 KV cache 方案据称实现约 1.86 倍端到端推理加速和 66 倍持久存储缩减。 长程智能体正日益受到上下文膨胀和 KV cache 内存瓶颈的困扰，因此架构级记忆内化可能为提示堆叠和外部检索提供更可扩展的替代方案。如果所报告的收益能够泛化，将影响智能体框架、长上下文推理系统和记忆层的开发团队。 该帖称 memt-1.0 使用门控 DeltaNet-2，在每一轮内进行稳定的 token 级记忆更新，并借助 mixture-of-storage 层扩展容量；其继续预训练加后训练、总计 34B token 的两阶段流程据称能让通用推理能力与参数化记忆基线相比保持竞争力。这些数字来自单篇技术拆解，且对应 128k 上下文下的 memt-1.0-nano 变体，仍需独立验证。

reddit · r/MachineLearning · /u/Mrs-Grumpy23 · 10月25日 05:31

**背景**: 智能体记忆系统通常要么把过往交互保留在提示/上下文窗口中，这会增大 KV cache；要么通过 RAG 检索外部文档，这会增加延迟和流水线复杂度。参数化记忆则把信息编码进模型权重或循环状态中；DeltaNet 这类线性注意力架构维护的是紧凑的循环状态，而不是完整的注意力缓存。门控 DeltaNet-2 通过分离的擦除门和写入门来更精细地控制记忆保留内容，而 mixture-of-storage 是 memt-1.0 扩展这种原生记忆容量的方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2610.26825">MemT-1.0: Towards Memory -Native Evolution</a></li>
<li><a href="https://www.emergentmind.com/topics/gated-deltanet-2-architecture">Gated DeltaNet - 2 : Advanced Memory Architecture</a></li>
<li><a href="https://arxiv.org/abs/2605.22791">Gated DeltaNet - 2 : Decoupling Erase and Write in Linear Attention</a></li>

</ul>
</details>

**标签**: `#agent-memory`, `#efficient-inference`, `#DeltaNet`, `#KV-cache`, `#model-architecture`

---

<a id="item-6"></a>
## [搜狗输入法 OPPO 定制版被 Google Play 保护机制标记为风险应用](https://t.me/zaihuapd/44689) ⭐️ 7.0/10

近日有多名 ColorOS 用户反馈，OPPO 定制的搜狗输入法被 Google Play 保护机制判定为有害应用，安全防护组件自动移除了该应用的敏感权限并将其停用，同时弹出提示警告其存在窥探短信、照片、录音、通话记录等个人隐私数据的风险。OPPO 客服回应称正在积极解决中，并建议用户可暂时关闭 Play 保护机制。 这一事件把厂商预装应用与 Google 安全服务之间的信任链问题推到了台前：一款通过手机厂商渠道预装的常用输入法，竟在用户自己的设备上被判定为有害应用。让用户关闭 Play 保护机制是一种颇具争议的处置方式，因为这会削弱整个系统对真正恶意应用的防护，而受影响的正是所有依赖该预装键盘的 ColorOS 用户。 Play 保护机制并不只是弹窗警告，而是直接移除了该应用的敏感权限并将其停用，因此在修复版本推送前用户可能会发现键盘无法使用。具体触发原因尚不明确，但被点名的短信、照片、麦克风、通话记录等权限远超一款输入法的功能所需；而且这是一款由 OPPO 二次定制的第三方应用与 Google 自动扫描机制之间的冲突，与 Play 商店上架审核无关。

telegram · zaihuapd · 10月25日 09:59

**背景**: Google Play 保护机制是 Android 内置的恶意软件扫描服务，会对设备上的应用（包括侧载和预装应用）进行检查，并可对判定为有害的应用发出警告、撤销权限或直接停用。输入法类应用在隐私上格外敏感，因为它能看到用户在手机上输入的一切内容，而在 Android 上这类应用往往申请范围很广的权限，国内多家输入法此前也曾因数据收集问题受到安全研究者批评。在中国市场，热门应用由手机厂商二次定制的版本十分常见，这类应用不经 Play 商店分发，因此不经过 Google 的正常审核流程，但仍可能被设备端的扫描机制标记。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.google.com/android/answer/2812853?hl=zh-Hans">利 用 Google Play 保 护 机 制 保 障 应 用 的安全性和数据的私密性 - Android...</a></li>
<li><a href="https://www.getdeng.net/blog/input-method-risk.html">getdeng.net/blog/input-method-risk.html</a></li>
<li><a href="http://www.jiguo.com/article/article/99975.html">大意了！ “窃取”聊天记 录 真凶竟是手机 输 入 法 ，会这四招防 隐 私 泄露-极果</a></li>

</ul>
</details>

**标签**: `#Android`, `#privacy`, `#security`, `#Google Play Protect`, `#Sogou`

---

<a id="item-7"></a>
## [苹果将于周三发布首款触屏 MacBook Pro，搭载 OLED 屏幕](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 7.0/10

据报道，苹果将于本周三推出首款触屏 MacBook Pro，这是 Mac 首次支持触摸操作和 OLED 屏幕，并引入灵动岛设计，提供 14 英寸与 16 英寸两个版本。其售价预计将高于现款 2499 美元的起售价。 这推翻了苹果长期以来的立场——高管们曾多次以人体工学为由否定触屏笔记本——是 Mac 输入方式多年来最重大的变化之一。这也显示苹果变得更务实，愿意反思和调整自身路线，而非坚持让行业跟随自己，并可能对已经在笔记本上提供触控和 OLED 面板的 Windows 阵营厂商形成压力。 据报道，触控将被定位为键盘和触控板的补充，而非替代方案，这一转变更多被解读为出于营收与营销考量，而非技术突破。该消息源自 Bloomberg 的报道，苹果尚未予以确认，因此具体规格和售价仍未经证实。

telegram · zaihuapd · 10月25日 14:25

**背景**: 灵动岛是苹果 2022 年在 iPhone 14 Pro 系列上引入的交互界面设计，它会围绕屏幕挖孔区域自动改变大小和形状，用于显示通知、媒体播放和实时活动，模糊了软件与硬件的界限。OLED 面板的每个像素自行发光，能呈现纯黑和极高对比度，而现款 MacBook Pro 使用的是 mini-LED 背光 LCD 屏幕，亮度很高但无法让单个像素完全熄灭。多年来苹果一直主张，伸手去触摸竖直放置的笔记本屏幕在人体工学上并不理想，这也是 Mac 一直只保留键盘和触控板的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/item/灵动岛/61968459">灵动岛（苹果公司应用于手机上的交互UI）_百度百科</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/563292350">灵动岛是什么？灵动岛功能详细解析 - 知乎</a></li>
<li><a href="https://post.smzdm.com/p/aomon7z9/">笔 记 本 屏 幕 选 OLED 还是 LCD ...</a></li>

</ul>
</details>

**标签**: `#Apple`, `#MacBook Pro`, `#touchscreen`, `#OLED`, `#hardware`

---

<a id="item-8"></a>
## [演讲者呼吁抵制互联网审查，将在 FOSDEM 发表演讲](https://talkweb.eu/openweb/4558/) ⭐️ 6.0/10

一位演讲者发表了题为《我拒绝接受一个被审查的互联网，来 FOSDEM 27 与我相聚》的号召性文章，呼吁读者抵制互联网审查，并为即将在 FOSDEM 举行的演讲做宣传。该文本质上是一篇演讲预告而非技术发布，但它在 Hacker News 上引发了热烈讨论（255 分、122 条评论），争议焦点是“无审查的互联网”是否真的可能存在。 这篇文章出现在一个敏感时刻：互联网的控制权正从开放协议转向少数几家公司和基础设施提供商，使“开放网络”的讨论从抽象理念变成现实问题。它也凸显了自由软件社区内部日益加深的分歧——内容审核与审查的边界究竟在哪里，以及在讨论审查时究竟该点名哪些国家。 文章本身技术内容不多，主要是演讲宣传，因此大部分价值来自随之而来的讨论。评论者指出，任何所谓“无审查”的网络仍然运行在由企业和国家控制的基础设施之上，这意味着加密覆盖层可能在路由或服务商层面被切断。

hackernews · Tomte · 10月25日 17:30 · [社区讨论](https://news.ycombinator.com/item?id=50233929)

**背景**: FOSDEM（自由及开源软件开发者欧洲会议）是一年一度在布鲁塞尔举办的非商业性、由志愿者组织的会议，通常在冬末举行，被普遍认为是欧洲规模最大的开源开发者聚会。“开放网络”指的是建立在 HTTP、HTML、RSS 等共享、无需许可的标准之上的那部分互联网，与把守内容入口的封闭平台形成对照。而区分内容审核（平台或社区执行规则）与审查（通常指国家主导的言论压制），一直是网络社区治理中的长期争论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/FOSDEM">FOSDEM - Wikipedia</a></li>
<li><a href="https://www.drupal.org/association/open-web-manifesto">Open Web Manifesto | Drupal.org</a></li>
<li><a href="https://www.conectys.com/blog/posts/content-moderation-vs-censorship-how-to-tell-the-difference/page/11/">Content Moderation vs Censorship | Blog | Conectys | BPO</a></li>

</ul>
</details>

**社区讨论**: 整体情绪理性但偏向怀疑：多位评论者认为真正无审查的互联网并不存在，因为它仍要通过受审查的基础设施路由，而企业只要付钱给服务商就能让其配合。也有人区分“审核”与“审查”，但承认任何在线讨论都需要某种形式的审核；还有评论者认为，如今多数用户只要审查符合自身政治立场就会接受它。另一条批评线索则指责 FOSDEM 这类场合只点名俄罗斯、中国和伊朗，却无视更靠近自身的审查；也有评论者单纯称赞 FOSDEM 是一场少有推销、非常值得参加的好会议。

**标签**: `#internet-censorship`, `#fosdem`, `#content-moderation`, `#privacy`, `#open-web`

---

<a id="item-9"></a>
## [Show HN 项目把员工“小人”放进标普 500 市值气泡图](https://bigwhalehunting.com/workforce/) ⭐️ 6.0/10

一位开发者在 Hacker News 的 Show HN 板块发布了可视化项目，把标普 500 指数中的每家公司画成一个按市值大小缩放的气泡，并在气泡内每 1 万名员工画一个小人。作者特别点出了英伟达与埃森哲的反差：英伟达市值约 5.2 万亿美元却只有 4.2 万名员工，相当于每名员工对应约 1.24 亿美元市值；而埃森哲拥有 81.4 万名员工，市值仅 1460 亿美元。 这张图把一个抽象的估值指标变成了直观画面，清楚展示了轻资产的 AI 与软件公司同劳动密集型服务企业在“把人变成市值”上的巨大差异。与此同时，它也暴露出底层员工人数数据并不可靠，这对任何想用“人均指标”判断生产率或经营效率的人来说都很关键。 图中每个小人代表 1 万名员工，可视化支持缩放，用户可以逐个查看具体公司。员工人数来自企业披露的口径，通常只统计直接雇佣的员工，因此对于大量使用外包、季节工或加盟模式的公司，这一数字会明显低估其实际用工规模。

hackernews · vfxGer · 10月25日 15:05 · [社区讨论](https://news.ycombinator.com/item?id=50232312)

**背景**: 市值等于股价乘以流通股数，标普 500 指数按市值加权，因此大公司主导了指数走势。用市值除以员工人数，就得到一个粗略衡量“市场给每名员工定价多少”的指标，常被用来解释无形资产密集型企业的商业模式。公司会在年度 10-K 报告中披露员工人数，美国证券交易委员会自 2020 年起还要求披露人力资本相关信息，但各家公司采用的口径差异很大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/Employee.html">Employee Metrics by Sector (US) - New York University</a></li>
<li><a href="https://www.sec.gov/files/spotlight/iac/20230921-recommendation-regarding-hcm.pdf">Human Capital Management Disclosure - SEC.gov</a></li>
<li><a href="https://note.com/manndoru/n/n04aabd88adcd?hl=en">How to use 'Market Capitalization per Employee' in corporate ...</a></li>

</ul>
</details>

**社区讨论**: 评论者质疑的重点多在数据而非可视化本身：有人指出兼职、季节工和外包人员（如亚马逊、沃尔玛）会让员工数失真；加盟模式导致口径不一致（万豪列出的 41.4 万人并非全部由公司直接雇佣，而麦当劳却只统计总部员工）；还有人认为行业分类有误，例如 Alphabet 和 Meta 被归为信息技术、特斯拉应归入工业，以及 NetApp 被纳入而规模相近的同业却缺席。也有评论者说，看到那些几乎被小人填满的气泡，会对这些公司的员工生出几分同情。

**标签**: `#data-visualization`, `#finance`, `#S&P 500`, `#Show HN`, `#workforce-analytics`

---

<a id="item-10"></a>
## [开源《魔法门之英雄无敌 2》引擎 fheroes2 登上 Hacker News，引发怀旧讨论](https://github.com/ihhub/fheroes2) ⭐️ 6.0/10

开源项目 fheroes2（托管在 GitHub 的 ihhub 组织下，用于重新实现《魔法门之英雄无敌 2》的游戏引擎）登上了 Hacker News 首页，获得约 184 分和 65 条评论。该讨论帖并未发布新版本公告，而是围绕该项目本身、同类项目 VCMI，以及这款老游戏今天是否依然好玩展开交流。 像 fheroes2 这样的引擎重实现项目，使几十年前的商业游戏在原版程序和发行商早已不再维护之后，仍能在现代操作系统与硬件上运行，从而起到游戏保存的作用。这也说明复古策略游戏的玩家群体依然活跃且具备技术能力，只不过这次讨论偏向闲聊，而非深入剖析引擎架构。 fheroes2 是一个从零编写的引擎，但仍需要原版游戏的数据文件才能游玩；其开发指南指出，一份可下载的原版试玩版是进行开发构建的最低要求。项目面向多平台，既提供 Visual Studio 2019 工程文件以支持 Windows，也支持 macOS 和 Linux；它与 VCMI 是两个独立项目，后者为《魔法门之英雄无敌 3》做同样的事情。

hackernews · tosh · 10月25日 11:09 · [社区讨论](https://news.ycombinator.com/item?id=50230384)

**背景**: 《魔法门之英雄无敌 2》是 New World Computing 于 1996 年推出的回合制策略游戏，玩家在其中建设城镇、招募奇幻兵种，并在六边形网格上进行战术战斗；该系列目前归育碧所有。“引擎重实现”指的是开发者从零重写游戏代码，让原始素材能在现代机器上原生运行，从而解决原版可执行文件无法应对的兼容性、分辨率与缺陷问题。这类项目通常要求玩家自备原版游戏，因此更像是游戏保存与现代化改造，而不是免费再分发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ihhub/fheroes2">GitHub - ihhub/fheroes2: fheroes2 is a recreation of Heroes ...</a></li>
<li><a href="https://ihhub.github.io/fheroes2/DEVELOPMENT.html">fheroes2 build and contribution guide | fheroes2</a></li>
<li><a href="https://github.com/vcmi/vcmi">vcmi / vcmi : Open-source engine for Heroes of Might and Magic III ...</a></li>

</ul>
</details>

**社区讨论**: 评论者大多带着怀旧情绪：有人分享了自己把 Claude Code 接入《魔法门之英雄无敌 3》的实验，称模型玩得很差而且非常慢；有人推荐了适合 Linux 的《英雄无敌 3》引擎 VCMI；还有人推荐了较新的《魔法门之英雄无敌：Olden Era》。也有怀疑的声音认为，像《英雄无敌》这样的童年挚爱，成年后重玩往往难以忍受；还有粉丝希望能有一款新作，把《英雄无敌 2》的美术风格与《英雄无敌 3》的机制结合起来。

**标签**: `#game-engine`, `#open-source`, `#reverse-engineering`, `#game-preservation`, `#retro-gaming`

---

<a id="item-11"></a>
## [Nanbeige 发布 Nanbeige4.3-33B：面向小型智能体的 Apache 2.0 教师模型](https://www.reddit.com/r/MachineLearning/comments/1xf6x35/nanbeige_releases_nanbeige4333b_an_apache_20/) ⭐️ 6.0/10

Nanbeige 以 Apache 2.0 许可证发布了 Nanbeige4.3-33B，该模型拥有 512K token 的上下文窗口，定位是公司后续更小型智能体（包括一款即将推出的 3B 模型）的教师模型。团队自报其在 Terminal-Bench 2.1 上取得 80.9 分，而 Qwen3.8-27B 为 73.0 分，且在每个基准内部使用相同的 harness 与推理设置进行评测。 一个以智能体工具使用为目标、采用宽松许可证的 33B 教师模型，为团队提供了一个可用于蒸馏小型、低成本推理智能体的潜在来源；在推理成本主导部署预算的当下，这也是开源权重社区大力投入的方向。512K 上下文窗口与 Apache 2.0 条款还使其能用于商业产品，而不受某些开放权重许可证常见限制的约束。 该模型并非全面领先：在 SWE-Bench Pro 上其自报得分为 60.3，而作为对比的 Qwen 为 61.7，且所有数字均来自发布团队本身，未经独立复现。智能体评测是在 preserve_thinking=true 的设置下进行的，模型卡建议在多轮工具调用中启用该设置，但不建议用于普通对话；因此，在该设置固定的前提下同时比较任务成功率与总生成 token 数，比把头部分数当作部署排名更有参考价值。

reddit · r/MachineLearning · /u/jatingargiitk · 10月25日 16:32

**背景**: 教师—学生蒸馏是构建小型高速模型的常见路径：由大模型生成高质量推理轨迹，再让较小的模型去模仿，因此一个强力的 33B 模型可以为 3B 智能体提供起步能力。Terminal-Bench 2.1 衡量智能体能否在终端环境中完成真实的命令行任务，而 SWE-Bench Pro 评测的是更长周期的软件工程工作，例如在真实代码仓库中解决问题。preserve_thinking 这一开关决定模型的先前推理轨迹是否被保留并带入多轮对话的后续轮次，这对需要反复调用工具、并需记住此前为何采取某一步骤的智能体尤为关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aiiq.org/benchmarks/terminal-bench-2-1/">Terminal - Bench 2 . 1 Benchmark — AI IQ</a></li>
<li><a href="https://labs.scale.com/leaderboard/swe_bench_pro_public_v2">SWE-Bench Pro V2 - labs.scale.com</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp/issues/22615">Documentation: `preserve_thinking=true` preserves reasoning ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#open-weights`, `#AI-agents`, `#benchmarking`, `#model-release`

---

<a id="item-12"></a>
## [工信部拟推汽车灯光强制性国标：智驾小蓝灯统一为蓝绿色](https://t.me/zaihuapd/44677) ⭐️ 6.0/10

工信部今日就汽车灯光强制性国家标准公开征求意见，新增小蓝灯（ADS 标志灯）的专用蓝绿色要求，并规定车灯各功能不得显示文字。征求意见稿同时禁止用语音关闭车灯、用手势控制灯具，并要求转向灯不得与制动灯和后雾灯混合。 此前各家车企的智驾“小蓝灯”各自为政，统一为国标颜色和规则后，其他道路使用者、交警和监管机构就有了判断车辆自动驾驶系统是否激活的一致外部信号。由于该灯与 L3 及以上自动驾驶绑定，这项标准实际上是自动驾驶责任划分监管体系的一部分。 该标准建议自 2028 年 1 月起实施，已获批车型享有 4 年宽限期，因此存量车型无需立即改装。禁止车灯显示文字以及禁止语音、手势控制灯具，针对的是部分厂商作为灯光秀或人车交互卖点宣传的功能。

telegram · zaihuapd · 10月25日 01:35

**背景**: ADS 标志灯是一种对外指示灯，用于向车外人员传递车辆自动驾驶系统是否处于激活状态；由于早期实现多用蓝色，在国内被俗称为“小蓝灯”。在中国自动驾驶分级中，L3 意味着在特定条件下由系统而非驾驶员负责监测路况，这正是监管机构希望有明确视觉提示的原因。在工信部将其写入强制性国标之前，国内已有部分城市和试点规则要求 L3 级车型安装此类灯具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.toutiao.com/article/7698628794709590566/">不再乱蓝！智驾ADS标志灯敲定蓝绿色，L3时代灯光规则落地</a></li>
<li><a href="https://finance.sina.com.cn/roll/2026-10-20/doc-inivwitm5795852.shtml">L3自动驾驶放开前夕：拟启用“蓝绿色”标志灯，灯亮则责变！</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/1920572045470705569">七月开始，注意车上蓝色小灯！自动驾驶新纪元来了！ - 知乎</a></li>

</ul>
</details>

**标签**: `#automotive`, `#regulation`, `#ADAS`, `#autonomous-driving`, `#safety`

---

<a id="item-13"></a>
## [GPU 租赁价格全面上涨，老款 A100 也不例外](https://x.com/a16z/status/2113741008550990191) ⭐️ 6.0/10

一份由 a16z 提供、以 2026 年 1 月 1 日为 100 的 GPU 租价指数显示，截至 10 月 19 日，七日移动平均值已升至 H200 约 265、B200 约 225、RTX PRO 6000 工作站版约 165、H100 SXM 约 137、A100 SXM4 约 102。折算成累计涨幅约为 H200 上涨 160%、B200 上涨 120%、RTX PRO 6000 上涨 65%、H100 上涨 35%，就连 2020 年发布的 A100 也略高于年初水平。 从最新一代到上一代 H100 乃至发布四年的 A100 全线上涨，说明供应紧张到买家不得不退而求其次选择旧卡，而不是只抢最新型号，这是典型的算力稀缺信号。由于 GPU 租价直接影响模型训练与推理的单位成本，若涨势持续，将抬高 AI 创业公司的支出，并让手握长期合约容量的厂商与云商获得更强议价权。 该数据是以 2026 年 1 月 1 日为基期的租价七日移动平均值，虽能平滑日常波动，但并未披露绝对的每 GPU 小时美元价格、供应商构成、合约期限，也未说明采样区域与实例类型。涨幅最陡的是最新的 Blackwell 代产品——H200 约为基期的 2.65 倍、B200 约为 2.25 倍——而 A100 十个月仅上涨约 2%，说明涨价集中在高端，并非全面等比例上行。

telegram · zaihuapd · 10月25日 06:39

**背景**: GPU 租价指数追踪的是云服务商与新型云厂商每 GPU 小时的收费水平，思路类似 Ornn 计算价格指数（OCPI）——后者基于实际成交而非挂牌价构建——此类指数被视为观察 AI 算力供需松紧的实时指标。涉及的芯片横跨 NVIDIA 数代产品：A100（2020 年，Ampere 架构）与 H100（Hopper 架构）是上一代主力，H200 是提升高带宽内存容量的 Hopper  refresh，B200 则属于 Blackwell 代，NVIDIA 宣称其在 AI 性能与总体拥有成本上远优于 HGX H100 系统。RTX PRO 6000 Blackwell 工作站版是 NVIDIA 的旗舰级桌面专业显卡，配备 96GB 显存，常被租用于不依赖数据中心级互联的 AI 工作负载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vast.ai/article/nvidia-h200-vs-b200-comparing-datacenter-grade-accelerators">NVIDIA H200 vs. B200: Comparing Datacenter-Grade Accelerators</a></li>
<li><a href="https://www.nvidia.com/en-us/products/workstations/professional-desktop-gpus/rtx-pro-6000/">NVIDIA RTX PRO 6000 Blackwell Workstation Edition</a></li>
<li><a href="https://data.ornn.com/markets">GPU Market Prices : Compute Price Index (OCPI) | Ornn Data</a></li>

</ul>
</details>

**标签**: `#GPU pricing`, `#AI infrastructure`, `#compute scarcity`, `#cloud economics`, `#hardware market`

---

<a id="item-14"></a>
## [特斯拉自研 AI 地图将随 FSD v15 推送](https://www.digitaltoday.co.kr/en/view/118497/tesla-to-build-in-house-maps-and-navigation-to-address-fsd-limits) ⭐️ 6.0/10

特斯拉正在开发一套基于 AI 的自研地图与导航系统，将首先随 FSD v15 推送，最初用于行程的出发与到达阶段，随后在数月内逐步扩展到完整导航和泊车场景。该系统将利用特斯拉车队众包采集的道路数据，改善限速识别、泊车和路线选择，并支持语音指令与个性化路线偏好。 这标志着特斯拉对“自动驾驶不应依赖地图”这一长期立场的反转，而该立场此前是其纯视觉、无图 FSD 路线的标志性主张。若特斯拉真把车队驱动的图栈落地，两大自动驾驶技术阵营的界限将变得模糊，其纯视觉方案也有望获得一种数据驱动的先验信息——而这通常是竞争对手依靠高精地图才能得到的能力。 这是一次分阶段推送而非一次性替换导航：v15 初期只覆盖行程起点与终点的路径规划，导航和泊车功能要到数月之后才跟进。特斯拉尚未公布地图格式、更新频率以及车队数据层如何与车端视觉网络融合等技术细节，而报道中提到的推动因素是股东对 FSD 在限速识别、泊车和路线选择方面的批评。

telegram · zaihuapd · 10月25日 10:57

**背景**: 特斯拉 FSD 一直采用纯视觉方案，实时从摄像头推断车道、标志和道路几何，这与 Waymo 及中国车企依赖高精地图（预先测绘的、高度精细的道路三维地图）的做法形成对比。近年行业整体转向“无图”自动驾驶，因为它被视为把自动驾驶功能快速扩展到新城市、无需重测每条道路的关键，CVPR 2024 甚至专门设立了无图自动驾驶挑战赛。特斯拉的折中之处在于：不从供应商购买地图，而是用自家用户车队已采集的传感器数据合成一层地图。值得一提的是，特斯拉 AI 团队的工程师 Phil Duan 已公开表示导航与坑洼检测的改进即将到来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.notateslaapp.com/news/4761/tesla-fsd-to-get-navigation-improvements-and-pothole-detection">Tesla FSD to Get Navigation Improvements and... - Not a Tesla App</a></li>
<li><a href="https://www.themoonlight.io/zh/review/mapvision-cvpr-2024-autonomous-grand-challenge-mapless-driving-tech-report">[论文评述] MapVision: CVPR 2024 Autonomous Grand Challenge...</a></li>
<li><a href="https://www.cnbeta.com.tw/articles/tech/1435590.htm">AI顶会 自 动 驾 驶 挑战赛：“ 无 图 ”小米全球第二 - 科技与交通 - cnBeta.COM</a></li>

</ul>
</details>

**标签**: `#tesla`, `#fsd`, `#autonomous-driving`, `#ai-mapping`, `#navigation`

---

<a id="item-15"></a>
## [GEEKCON 上海站无人机攻防赛题引发厂商报警，赛事一度暂停](https://tech.ifeng.com/c/8xSZe56UAz6) ⭐️ 6.0/10

10 月 24 日晚闭幕的上海 GEEKCON 安全极客活动上，一项无人机攻防赛题据称触发了某头部无人机厂商报警，相关人员被带走，赛事一度暂停。该赛题要求选手突破基于 GPS 的禁飞限制，并夺取无人机的完整控制权。 这起事件凸显出在中国，获授权的白帽竞赛与真实世界风险之间的界线非常脆弱——即便赛题发生在黑客赛事内部，厂商仍可能直接报警处理。它可能对漏洞研究与协同披露实践产生寒蝉效应，尤其是无人机等联网硬件领域，同时也让外界质疑赛事主办方应如何就敏感攻击场景事先与厂商沟通。 据报道，该赛题结合了两项敏感能力：突破依赖 GPS 定位、用于阻止无人机进入禁飞区的地理围栏系统，以及实现对飞行器的完整接管。不过该消息仅为简短媒体摘要，没有一手信源、没有技术细节，也未确认涉及的具体厂商或被抓人员的法律状态，因此细节仍待核实。

telegram · zaihuapd · 10月25日 13:29

**背景**: 主流厂商的消费级无人机内置地理围栏系统，依靠 GPS 判断飞行器是否处于禁飞区，一旦检测到禁飞状态就限制起飞。绕过这些限制（市面上常被称为“破限”或“解锁”）在国内属于灰色乃至违法的生意，因此在公开场合现场演示此类攻击在法律上相当敏感。GEEKCON 是每年 10 月 24 日举办的安全极客大会，长期由华为、腾讯安全、蚂蚁等大厂赞助，2025 年新增了“低空经济与机器人安全”板块，无人机议题正是在此背景下出现。协同漏洞披露（CVD）是研究者先向厂商报告漏洞、再对外公开的行业惯例，而未经沟通的现场演示往往会打破这一流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.4hou.com/posts/Bv4n">记 GEEKCON 2025...</a></li>
<li><a href="https://www.hnyundian.com/xingyexinwen/174.html">无 人 机 “破 限 ”黑产揭秘：你的“自由 飞 行”可能已触犯刑法</a></li>
<li><a href="https://www.geekpark.net/news/326450">GEEKCON ...</a></li>

</ul>
</details>

**标签**: `#security-research`, `#drone-security`, `#coordinated-disclosure`, `#china-tech-policy`, `#hacking-contests`

---