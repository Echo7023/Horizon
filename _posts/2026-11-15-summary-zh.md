---
layout: default
title: "Horizon Summary: 2026-11-15 (ZH)"
date: 2026-11-15
lang: zh
---

> 从 29 条内容中筛选出 14 条重要资讯。

---

1. [Lovable 生成的应用因 Supabase 默认配置泄露护照信息与 20 多万条私信](#item-1) ⭐️ 8.0/10
2. [SpaceX 在星舰第 15 次飞行收官时成功用机械臂捕获超重型助推器](#item-2) ⭐️ 8.0/10
3. [PyPI 推出重新设计的项目页面，安全与来源信号更清晰](#item-3) ⭐️ 7.0/10
4. [《猴岛小英雄》全部 13 个版本同屏对比](#item-4) ⭐️ 7.0/10
5. [EFF 警告：科技公司再次试图重新定义“隐私”](#item-5) ⭐️ 7.0/10
6. [SpaceX 下月将首次尝试完整回收星舰与超级重型助推器](#item-6) ⭐️ 7.0/10
7. [Cloudflare 开源面向 AI 代理的无状态浏览器 Kitesurf](#item-7) ⭐️ 7.0/10
8. [意大利隐私监管机构以违规读取相册为由对 Meta 罚款 8.05 亿欧元](#item-8) ⭐️ 7.0/10
9. [纪录片回顾 KDE 三十年的志愿者桌面项目历程](#item-9) ⭐️ 6.0/10
10. [Reddit 用户按所属高校对 ICLR 2027 初审评分进行排名](#item-10) ⭐️ 6.0/10
11. [Reddit 讨论：短期价格预测论文应以市场隐含预测为基准](#item-11) ⭐️ 6.0/10
12. [全球最大无人货机 W5000 完成首次技术验证试飞](#item-12) ⭐️ 6.0/10
13. [新西兰仓库工人抗议 AI 监控如厕时间](#item-13) ⭐️ 6.0/10
14. [谷歌 AI Studio 设计师借助 WindowsiOS 在折叠 iPhone 上运行 Windows 11](#item-14) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Lovable 生成的应用因 Supabase 默认配置泄露护照信息与 20 多万条私信](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

化名 neathack 的安全研究者（crissyfield.de）发布研究指出，使用 AI 应用生成器 Lovable 搭建、后端由 Supabase 提供且默认未开启行级安全（RLS）的应用，已公开泄露包括护照信息在内的敏感数据以及超过 20 万条私信。攻击者只需在浏览器中查看网络请求，并复用打包在前端里的公开 anon key，就可在不需要任何高深黑客技术的情况下读取这些数据。 这一披露把讨论从单一厂商的漏洞上升到整个行业的默认配置问题：当 AI 工具让非开发者也能在几分钟内上线全栈应用时，宽松的数据库默认设置就变成了影响大量普通用户隐私的系统性风险。同时，这也给 Supabase 和 Lovable 这类平台施加了压力，要求它们转向“默认拒绝”的安全策略。 通过 SQL 创建的 Supabase 数据表默认不启用行级安全，因此打包进浏览器端的 anon key 可以读取表中所有行；Supabase 表示已于 10 月 30 日修复该默认行为，但有评论者称已有项目可能仍沿用旧的宽松设置。此次事件中的利用方式不需要任何超出浏览器开发者工具的手段，而随着越来越多人用提示词生成应用，这类应用的数量每天都在增长。

hackernews · armcat · 11月14日 17:43 · [社区讨论](https://news.ycombinator.com/item?id=50499017)

**背景**: Lovable 是一款 AI 应用生成器，可以根据自然语言提示生成界面、数据库和业务逻辑，属于“氛围编程”（vibe coding）潮流的一部分——用户只需描述想要什么，而不用自己写代码。Supabase 是流行的开源 Firebase 替代方案，提供 Postgres 数据库和自动生成的 API，其行级安全（RLS）功能用于限制某个用户的密钥能访问哪些数据行。如果没有开启 RLS 并编写策略，Supabase 必须放在客户端代码里的公开 anon key 实际上就等于赋予了读取整张表的权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://amabrik.com/blog/supabase-row-level-security/">Supabase Row Level Security (RLS) Explained | Amabrik</a></li>
<li><a href="https://supabase.com/docs/guides/api/securing-your-api">Securing your API | Supabase Docs</a></li>
<li><a href="https://lovable.dev/">App & Website Builder | Build Software in Minutes | Lovable</a></li>

</ul>
</details>

**社区讨论**: 评论者大多把矛头指向 Supabase，引用 GitHub 讨论 #4547 指出该宽松默认值据称已在 10 月 30 日修复，但对已有项目可能仍然生效，并认为这是多年前为降低上手门槛而做出的有意取舍。也有人认为 AI 生成的应用属于数量庞大、易于攻击的目标，其用户根本不了解风险，并呼吁采用默认拒绝的数据库、最小权限 API 和自动化鉴权测试，让不安全部署变得困难而非容易。文章作者也参与了讨论，提到该文两周前在 Hacker News 首发时并未获得多少关注。

**标签**: `#security`, `#supabase`, `#AI-generated-code`, `#data-privacy`, `#vibe-coding`

---

<a id="item-2"></a>
## [SpaceX 在星舰第 15 次飞行收官时成功用机械臂捕获超重型助推器](https://x.com/i/broadcasts/2brajgZlOKRMka) ⭐️ 8.0/10

SpaceX 对星舰第 15 次飞行的直播以超重型助推器被发射塔机械臂在半空中捕获而结束，而不是落入海中溅落。这次捕获为本次试飞画上句号，也被视为该公司推进完全可重复使用运载硬件进程中的又一步。 能够常态化地捕获助推器是实现快速复用的关键前提：它让这一级箭体保持完整、落在陆地上并靠近发射场，从而可以被快速检查并再次飞行。因此每一次成功捕获不仅关系到 SpaceX 的火星雄心，也关系到整个超重型运载发射的经济性。 捕获由发射塔上所谓的“筷子”机械臂完成，它必须在几秒内拦停带着约 100 兆焦耳动能的下降助推器，依赖精准的时机把握以及助推器剩余发动机和栅格舵的配合。能否成功取决于助推器在着陆时是否状态良好，这也是更早的几次飞行不得不改为海上溅落的原因。

hackernews · ls612 · 11月14日 21:22 · [社区讨论](https://news.ycombinator.com/item?id=50500963)

**背景**: 超重型助推器（Super Heavy）是 SpaceX 星舰的可重复使用一级，星舰是由该助推器与星舰上面级组成的超重型运载火箭，十余年来作为 SpaceX 火星计划的一部分持续研制。发射塔上的机械捕获系统被昵称为“Mechazilla”；它在 2024 年 10 月的第 5 次飞行中首次成功捕获助推器，这一里程碑让“塔架捕获”成为替代着陆腿的可行方案。此后 SpaceX 在后续试飞中不断打磨这一操作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SpaceX_Super_Heavy">SpaceX Super Heavy - Wikipedia</a></li>
<li><a href="https://www.universetoday.com/articles/spacexs-mechazilla-catches-starship-booster">SpaceX's Mechazilla Catches a Starship Booster on First Try</a></li>
<li><a href="https://www.linkedin.com/posts/waseem-rehmancpengcmrppmp_spacexs-launch-tower-catching-super-heavy-activity-7436278279784812544-qO2E">SpaceX's Super Heavy Booster Catch Mechanism ... | LinkedIn</a></li>

</ul>
</details>

**社区讨论**: 评论者几乎一边倒地表达兴奋，称这次捕获“不可思议”、是十余年积累换来的新时代开端，还有不少人表示这一工程壮举可能激励数百万年轻人投身工程领域。也有人注意到轻松有趣的细节，比如箭体上一个 S42 标识上方写着“don't panic”；还有人打趣说这次捕获“精确得几乎有点无聊”，这其实是在称赞该操作已开始显得驾轻就熟。

**标签**: `#SpaceX`, `#Starship`, `#aerospace engineering`, `#reusable rockets`, `#engineering milestone`

---

<a id="item-3"></a>
## [PyPI 推出重新设计的项目页面，安全与来源信号更清晰](https://blog.pypi.org/posts/2026-11-06-ui-updates-complete/) ⭐️ 7.0/10

2026 年 11 月 6 日，PyPI 完成了项目页面的重新设计，新增了独立的“安全”标签页、按文件展示的来源证明（provenance attestation），以及更醒目的提示——当发布元数据缺失、不完整或与项目历史冲突时会给出警告。除界面改动外，PyPI 还扩充了用户文档，新增软件包安全指南，内容涵盖源代码评估、来源核查、完整性校验与攻击上报。 这一改动把供应链证据直接呈现在用户决定是否安装某个软件包的关键时刻，使被入侵或被劫持的发布更难蒙混过关。由于 PyPI 是 Python 生态的默认分发渠道，即便是小幅的可见性提升，也可能推动成千上万个项目在发布环节向来源证明和 Trusted Publishing 靠拢。 来源证明警告的设计目标是标记那些元数据缺失或与项目历史不一致的发布，因此有助于发现原本良性、但 PyPI 凭据被盗用的项目——但它无法识别从一开始就恶意的软件包。此外，Trusted Publishing 目前仍不支持 GitHub 可复用工作流（reusable workflows），这一限制记录在 warehouse 仓库的 #11096 号议题中。

hackernews · rbanffy · 11月14日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50497892)

**背景**: 来源证明（provenance attestation）是一种机器可读的签名记录，用于描述软件构件的来源与构建方式；在 PyPI 上，当软件包通过 CI/CD 系统的 Trusted Publishing 发布时，这类证明通常会自动生成。Sigstore 是支撑这一机制的开源项目，它提供“无密钥”（keyless）签名：用与 OIDC 身份（例如某个 GitHub Actions 工作流）绑定的短期证书取代长期私钥。这一点很重要，因为传统签名密钥容易泄露或丢失，而无密钥签名能把某次发布牢牢绑定到产生它的具体流水线与提交上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.pypi.org/using-pypi/package-security/provenance/">Checking Provenance (package origin) - PyPI Docs</a></li>
<li><a href="https://www.sigstore.dev/">Home · Sigstore</a></li>
<li><a href="https://daysec.org/pypi-security-tab-provenance-warnings-guide/">Read PyPI’s New Security Signals Before Installing a Release</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍欢迎 PyPI 展示来源信息，有人用 Datasette（有来源证明）与 dlt（无来源证明）作为直观对比示例，也有人希望 Sigstore 式的无密钥签名进一步普及，促使更多 CI/CD 服务商支持所需的 OIDC 处理。疑虑主要集中在中心化问题上：一位评论者认为该信任模型实际上依赖“大型云厂商”并助长锁定效应，这有违 Python 的精神；另一位则指出这些信号能发现被劫持的原本良性项目，却无法识别从一开始就恶意的项目。

**标签**: `#PyPI`, `#software supply chain security`, `#provenance`, `#Sigstore`, `#Python packaging`

---

<a id="item-4"></a>
## [《猴岛小英雄》全部 13 个版本同屏对比](https://monkeyisland.pages.dev/) ⭐️ 7.0/10

一个位于 monkeyisland.pages.dev 的网站把 Lucasfilm Games 1990 年的冒险游戏经典《猴岛小英雄》（The Secret of Monkey Island）的全部 13 个版本并排放在一起做视觉对比，让访客能直观看到同样的场景在不同平台和不同图形模式下是如何呈现的。该项目登上 Hacker News 首页，获得约 440 分和 141 条评论。 这个对比直观展示了一款游戏如何被迫为十几种不同的显示与硬件标准重新制作美术资源，而这正是软件保存与复古计算研究试图记录的内容。它之所以引发共鸣，还因为许多玩家第一次接触冒险游戏，就是通过这款作品某个画面限制极为严苛的特定版本。 对比涵盖 4 色的 CGA、16 色的 EGA 和 256 色的 VGA 版 DOS 版本以及 Amiga 版，因此各移植版之间的调色板与分辨率差异是直接可见的，而不是靠文字描述。网站本身的界面刻意模仿 Borland Turbo Vision，也就是当时大量 DOS 应用程序共有的文本模式窗口外观。

hackernews · maximilianburke · 11月14日 04:23 · [社区讨论](https://news.ycombinator.com/item?id=50493904)

**背景**: 《猴岛小英雄》建立在 SCUMM 引擎之上，Lucasfilm Games 最初为《疯狂大楼》（Maniac Mansion，1987）开发该引擎，目的是让地点、物品和对话无需编写引擎层代码即可定义。由于 SCUMM 让游戏脚本和数据文件保持跨平台可复用，同一款游戏可以移植到众多系统上，这也是它会有如此多不同版本的原因。在那个年代，PC 所配备的图形标准互不兼容——CGA 只能在 320x200 下显示 4 种颜色，EGA 为 16 色，VGA 为 256 色——因此美术师必须为每一种目标机型重新绘制或重新抖动处理同样的场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SCUMM_engine">SCUMM engine</a></li>
<li><a href="https://en.wikipedia.org/wiki/ScummVM">ScummVM - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论充满怀旧情绪，但对 CGA 的评价出现分歧：一些评论者说青、品红、黑、白这套配色让人感觉“冷”，自己始终无法适应；另一些人则对当年仅用四种或更少颜色就能画出可辨识场景的美术师深表敬意。还有人回忆起 Amiga 版《猴岛小英雄 2》装在约 13 张软盘上、带有拷贝保护，玩家往往玩到中途才被卡住；多位评论者称赞网站模仿 Turbo Vision 的界面，并感叹那个年代冒险游戏的魔力至今未被重现。

**标签**: `#retro-computing`, `#game-development`, `#graphics`, `#software-preservation`, `#adventure-games`

---

<a id="item-5"></a>
## [EFF 警告：科技公司再次试图重新定义“隐私”](https://www.eff.org/deeplinks/2026/11/tech-companies-are-trying-shift-entire-concept-privacy-again) ⭐️ 7.0/10

电子前哨基金会（EFF）发布了一篇新的分析文章，指出科技公司正再次试图按照自身商业模式的需要，重新定义整个“隐私”概念。文章发表之际，职场中 AI 会议记录工具和其他监控手段的部署正日益普及，文中同时给出了个人如何自我保护的建议。 隐私如何被定义，决定了哪些数据收集会被视为“正常”，因此由产业界推动的概念重塑会悄然改变数以亿计普通用户和员工的默认规则。这一争论在职场尤为紧迫——有员工表示，若想拒绝 AI 会议记录工具，几乎等于拿自己的饭碗冒险。 该文章属于政策评论而非技术披露，因此并未提供新的产品或漏洞细节，其价值在于议题框架以及对个人层面缓解措施的建议。随后的 Hacker News 讨论（约 395 分、151 条评论）大量聚焦于 AI 会议转写，认为它是这一趋势最具体的日常体现。

hackernews · gslin · 11月14日 12:45 · [社区讨论](https://news.ycombinator.com/item?id=50496602)

**背景**: 电子前哨基金会（EFF）是一家总部位于旧金山的非营利数字权利组织，成立于 1990 年，宗旨是推动互联网公民自由，并以通过诉讼、倡导以及 Privacy Badger 等工具捍卫数字隐私、言论自由与创新而闻名。它所说的企业“重新定义隐私概念”，指的是产业界一种由来已久的做法：把隐私重新解释为例如用户对设置的掌控权，或“告知—同意”流程，而不是对数据收集本身的限制。这一点很关键，因为政策辩论中采用的定义，往往会变成监管者实际执行的定义。当前的焦点是职场 AI 监控：常开的会议记录工具、屏幕与活动追踪，甚至面部情绪分析，正越来越多地被推销给雇主。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Electronic_Frontier_Foundation">Electronic Frontier Foundation - Wikipedia</a></li>
<li><a href="https://www.eff.org/">Electronic Frontier Foundation | Defending your rights in the digital...</a></li>
<li><a href="https://www.inc.com/chloe-rosenberg/is-your-boss-watching-your-face-the-next-frontier-of-workplace-surveillance/91393352">Is Your Boss Watching Your Face? The Next Frontier of Workplace ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对“监控成为新常态”持敌视态度：有人提问，能否把“这次会议不需要转写，请关闭 AI 记录工具”变成一种被接受的惯例，因为目前拒绝似乎会损害职业前途。也有人援引《世界人权宣言》第 12 条关于禁止任意干涉隐私的规定，主张将真实身份与一次性身份分隔使用并辅以物理隔离（air gap），并呼吁支持 EFF 等提起诉讼的组织；还有人尖锐地把现状与当年 Google Glass 遭遇的抵制相提并论。

**标签**: `#privacy`, `#surveillance`, `#AI`, `#tech-policy`, `#EFF`

---

<a id="item-6"></a>
## [SpaceX 下月将首次尝试完整回收星舰与超级重型助推器](https://t.me/zaihuapd/45117) ⭐️ 7.0/10

马斯克在财报电话会上宣布，SpaceX 将于下月首次尝试在同一飞行中同时回收星舰飞船与超级重型助推器。他坦言此次尝试不保证成功，但表示成功率比上一次飞行更高。 若成功，这将是人类首次完整回收轨道运载系统，是迈向马斯克所追求的快速、低成本复用目标的关键一步，而这一目标关系到星舰在 NASA 登月计划中的角色以及 SpaceX 的星链扩张。两级全部复用，才能让 SpaceX 快速翻修并重新发射，而不是每次新建一枚火箭。 上一次飞行因一台发动机提前关机，任务被缩短至约 3 小时，助推器与飞船均未回收；超级重型助推器通常由发射塔的机械臂“夹住”，而飞船则需返回发射场被接住。马斯克没有给出具体的飞行日期或火箭构型，该计划目前仍只是宣布的意向，而非已完成的里程碑。

telegram · zaihuapd · 11月14日 03:03

**背景**: 星舰是 SpaceX 研制的全复用两级运载系统：超级重型助推器是第一级，由 33 台使用过冷液态甲烷与液氧的猛禽发动机驱动；星舰则是上面级兼飞船。SpaceX 通过发射塔上巨大的“筷子”机械臂夹住返回的助推器来完成回收，并计划以同样方式回收飞船。在同一次飞行中把两者都收回来，就是 SpaceX 所称的“首次完整回收轨道运载系统”，而在此之前，这两个飞行器要么分开回收，要么未能回收。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Super_Heavy_Booster_10">Super Heavy Booster 10</a></li>
<li><a href="https://www.zerohedge.com/technology/watch-live-spacex-targets-historic-starship-booster-double-chopsticks-catch">SpaceX Aborts Starship /Booster 'Double Chopsticks' Recovery <!-- --&...</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Starship`, `#spaceflight`, `#reusable rockets`, `#technology news`

---

<a id="item-7"></a>
## [Cloudflare 开源面向 AI 代理的无状态浏览器 Kitesurf](https://www.phoronix.com/news/Cloudflare-Kitesurf-Open-Source) ⭐️ 7.0/10

Cloudflare 以 Apache 2.0 协议开源了 Kitesurf，这是一款专为 AI 代理设计、完全运行在 Cloudflare Workers 之上的无状态浏览器。它无需完整的 Chromium 容器即可解析 HTML、处理 CSS 并执行 JavaScript，相关代码已发布在 GitHub 上。 AI 代理的工作负载通常突发且短暂，为每个任务启动完整浏览器容器会浪费大量 CPU 和内存；而基于 Workers 的原生浏览器可以显著降低这类任务成本，并让代理按需在全球范围内扩展。如果获得广泛采用，它有望成为面向网页的 AI 代理的标准轻量执行层。 Cloudflare 表示，在截图、HTML 提取等常见代理任务上，Kitesurf 相比 Chromium 消耗的 CPU 和内存要少得多，因此可以支持更多并发会话。由于它是无状态且完全隔离的，主要面向短暂的一次性会话而非长时间交互式浏览，并且只能在 Cloudflare Workers 生态内运行。

telegram · zaihuapd · 11月14日 09:33

**背景**: 像 Chromium 这样的无头浏览器需要在容器中运行完整的渲染引擎以及独立的驱动（例如 Chrome DevTools Protocol），功能强大但笨重、启动缓慢。Cloudflare Workers 是一种无服务器运行时，可以在全球数百个城市边缘节点执行 JavaScript 而无需管理服务器，非常适合短时、高并发的请求。Kitesurf 将这两者结合：一个直接在 Workers 上解析页面并执行脚本的类浏览器引擎，彻底避免了容器带来的额外开销。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.cloudflare.com/browser-run/kitesurf/">Kitesurf · Cloudflare Browser Run docs</a></li>
<li><a href="https://kitesurf.cloudflare.app/">Kitesurf - stateless browser running entirely on Workers</a></li>
<li><a href="https://developers.cloudflare.com/workers/">Overview · Cloudflare Workers docs</a></li>

</ul>
</details>

**标签**: `#Cloudflare`, `#AI agents`, `#browser`, `#serverless`, `#open source`

---

<a id="item-8"></a>
## [意大利隐私监管机构以违规读取相册为由对 Meta 罚款 8.05 亿欧元](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10321080) ⭐️ 7.0/10

意大利隐私监管机构 Garante Privacy 对 Meta 开出 8.05 亿欧元罚单，原因是 Facebook Android 应用于 2023 年上线的相册推荐功能默认开启，并在未取得具体同意的情况下读取了约 2000 万意大利用户的照片、视频及元数据。Meta 须在 60 天内将该功能改为默认关闭并单独征得用户明确同意，否则不得向未有效授权的用户提供该功能。 这是针对大型平台开出的规模最大的 GDPR 相关罚单之一，也再次表明：默认勾选或默认开启并要求访问设备媒体的设置，很难满足欧洲对“同意”的标准。这显示出各国监管机构持续强硬的执法态势，或将影响 Meta 及其他大型科技公司在整个欧盟范围内设计权限申请流程的方式。 监管机构的核心异议在于授权提示过于笼统，不构成针对访问设备相册的“具体同意”，且处罚针对的是 Android 应用的媒体与元数据访问行为，而非 Facebook 核心服务。Meta 面临 60 天的整改期限，命令要求其采用默认关闭、单独征得同意的机制，而不是一次性打包授权。

telegram · zaihuapd · 11月14日 14:37

**背景**: GDPR 是欧盟的数据保护框架，要求企业在处理个人数据时必须具备合法依据，通常是用户明确、具体的同意；意大利的 Garante Privacy 是欧盟内执法最活跃的监管机构之一。照片及其内嵌元数据（如时间戳、设备信息和位置数据）都属于个人数据，因此扫描用户相册需要清晰的法律依据。各国监管机构可对企业处以最高相当于其全球年营业额 4% 的罚款，这也是针对 Meta 等平台的罚单动辄数亿欧元的原因。

**标签**: `#privacy`, `#Meta`, `#GDPR`, `#regulation`, `#Italy`

---

<a id="item-9"></a>
## [纪录片回顾 KDE 三十年的志愿者桌面项目历程](https://tube.kockatoo.org/w/fFinNHfanLT7aBEb2B8y4c) ⭐️ 6.0/10

一部讲述 KDE 历史与影响力的纪录片被发布在 PeerTube 实例 tube.kockatoo.org 上，并在 Hacker News 引发讨论，获得 322 分和 70 条评论。影片记录了志愿者社区如何用 C++ 和 Qt 工具包构建自由桌面环境，并在多次重大重写中将其延续至今。 KDE 是运行时间最长的自由软件桌面项目之一，其代码如今出现在从巴西学校电脑到 Steam Deck 的各种设备上，因此这部纪录片同时也是一份关于如何让庞大志愿者代码库延续数十年的案例研究。对开发者而言，相关讨论揭示了 C++ 维护负担、社区治理以及像 KDE 4 那样颠覆性重构所付出代价的深刻教训。 该片通过 PeerTube 而非 YouTube 分发，而讨论串的驱动力更多来自老用户讲述自己使用 KDE 3.x 时代工具（如 Amarok 1.4、k3b 以及 Konqueror 的 KIO slaves）的个人经历，而非影片本身。评论者指出，即便是转向 AwesomeWM 等平铺式窗口管理器的用户，往往仍继续使用 Dolphin 和 Konsole，这说明即使整个桌面被弃用，单个 KDE 应用依然具有很强的黏性。

hackernews · mrkn1 · 11月14日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=50496976)

**背景**: KDE 是一个国际性的自由软件社区，产出 Plasma —— 一个面向 Linux 和 BSD 的图形外壳，负责管理窗口、面板、小部件和系统设置 —— 以及包括 Kdenlive 视频编辑器、Krita 数字绘画工具在内的大量应用。大多数 KDE 软件使用 C++ 编写并基于 Qt 框架，后者是一套可用单一代码库构建跨平台图形界面的工具包。KDE 软件拥有数百万用户，并被部署在学校、政府和商业产品中，仅巴西就有数千万学童使用基于 KDE 的软件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kde.org/">Home - KDE Community</a></li>
<li><a href="https://en.wikipedia.org/wiki/KDE_Plasma">KDE Plasma - Wikipedia</a></li>
<li><a href="https://www.qt.io/development/qt-framework">Qt Framework – Build Fast, Scalable Cross-Platform Software | Qt</a></li>

</ul>
</details>

**社区讨论**: 讨论氛围充满感情但也很清醒：评论者称 KDE 是一个引人入胜的研究样本，展示了用 C++ 打造出适合大多数人的软件有多么困难，并称赞社区能够消化错误、把文化、品味和需求各异的贡献者凝聚在一起。多位老用户把自己的经历追溯到当年在 Usenet 上招募志愿者构建“Kool Desktop Environment”的原始帖子和 KDE 3.x 时代；也有人表示 KDE 4 的不稳定让他们离开，但至今仍依赖 Dolphin、Konsole 等单个应用。

**标签**: `#KDE`, `#open source`, `#Linux desktop`, `#documentary`, `#community`

---

<a id="item-10"></a>
## [Reddit 用户按所属高校对 ICLR 2027 初审评分进行排名](https://www.reddit.com/r/MachineLearning/comments/1xwcjuq/iclr_2027_initial_review_scores_ranked_by/) ⭐️ 6.0/10

Reddit 用户 /u/No-Lab4175 发布了一份按作者所属高校汇总的 ICLR 2027 初审评分排名，其数据通过抓取 OpenReview、将论文标题与 arXiv 匹配、再借助 OpenAlex 归属机构的方式构建而成。 由于 ICLR 采用开放同行评审，评审分数是公开可见的，因此人们可以按投稿所获评价而非仅按录用数量来衡量机构表现；这类排名正越来越多地被潜在学生和招聘委员会当作科研实力的粗略信号，尽管其方法学上相当脆弱。 该数据流程依赖 OpenReview 投稿与 arXiv 预印本之间的标题匹配以及 OpenAlex 的机构记录，因此容易受到标题匹配错误、无 arXiv 版本的论文以及作者机构归属模糊或存在多机构署名等问题的影响；Reddit 原帖仅用一句话描述方法，并未给出误差分析或按投稿量做归一化处理。

reddit · r/MachineLearning · /u/No-Lab4175 · 11月14日 20:33

**背景**: ICLR（国际学习表征会议）是深度学习领域的顶级会议之一，它把所有投稿、评审意见和评分都公布在 OpenReview 上——这是一个旨在让同行评审透明化的免费开源平台。OpenAlex 则是一个免费的开放文献目录，收录数亿篇学术成果、作者与机构信息，由 OurResearch 于 2022 年推出，用以接替终止服务的 Microsoft Academic Graph。把这两类数据结合起来，任何人都可以重建“哪些机构投了哪些论文、评审给了什么分数”的图景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open_reviewing">Open reviewing</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAlex">OpenAlex</a></li>
<li><a href="https://openreview.net/about">About | OpenReview</a></li>

</ul>
</details>

**标签**: `#ICLR`, `#peer-review`, `#bibliometrics`, `#machine-learning-research`, `#academic-rankings`

---

<a id="item-11"></a>
## [Reddit 讨论：短期价格预测论文应以市场隐含预测为基准](https://www.reddit.com/r/MachineLearning/comments/1xw6fk9/should_shorthorizon_price_forecasting_papers/) ⭐️ 6.0/10

Reddit 的 r/MachineLearning 版块上，用户 /u/happypeanut-t 发帖指出，大多数短期加密货币与大宗商品价格预测论文（Transformer、LSTM 等）只与 ARIMA、随机游走或简单 LSTM 比较并报告更低的 RMSE，却很少与市场已经预期的结果对标，例如期权隐含波动率或预测市场这类需要真金白银下注的群体预测。该帖还指出论文通常只评估点预测，并追问：对于 BTC 这类资产，为何 80% 预测区间的实际覆盖率没有成为标准评估指标，是否是因为数据获取困难。 这一批评之所以重要，是因为市场隐含预测已经聚合了大量公开信息，一旦把它纳入对比，“跑赢随机游走”就是很弱的结论；如果一个模型连市场自身的预期都赢不了，其实际价值就很有限。同时，强调区间覆盖率而非 RMSE，会把评估重心转向交易员和风险管理者真正关心的不确定性与风险量化，从而影响机器学习与量化研究者设计和报告预测结果的方式。 该帖是一个讨论性提问，而非完整的实证分析；它把数据获取列为造成这一差距的一种可能原因，并询问是否已有相关论文这样做了。帖子还特别区分了期权隐含波动率（描述市场预期的价格区间而非单一的点预测）和参与者用真金白银对结果下注的预测市场。

reddit · r/MachineLearning · /u/happypeanut-t · 11月14日 16:23

**背景**: 在时间序列预测论文中，随机游走（直接预测最后一个观测值）和 ARIMA 是标准的朴素基线，因此报告比它们更低的 RMSE 是一种常见但很弱的基准。期权隐含波动率由期权价格推导而来，反映市场对未来价格波动的估计，实质上是对未来价格区间的市场隐含预测。预测市场是交易所化的市场，其合约价格体现群体对某一事件发生概率的判断。区间覆盖率衡量实际结果落入预测名义区间的频率，因此一个 80% 区间如果只有 50% 的情况下包含真实结果，即便 RMSE 看起来不错，其校准也是很差的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fidelity.com/viewpoints/active-investor/implied-volatility">Implied volatility | Fidelity</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prediction_market">Prediction market</a></li>
<li><a href="https://r-statistics.co/Checking-Prediction-Interval-Coverage.html">The Expert Edge in Forecasting Like a Pro Lesson 7: Checking ...</a></li>

</ul>
</details>

**标签**: `#financial-forecasting`, `#evaluation-methodology`, `#machine-learning`, `#quantitative-finance`, `#prediction-markets`

---

<a id="item-12"></a>
## [全球最大无人货机 W5000 完成首次技术验证试飞](https://www.ithome.com/1/027/068.htm) ⭐️ 6.0/10

白鲸航线 11 月 14 日宣布，W5000 大型无人货运飞机在内蒙古鄂托克前旗完成技术验证试飞，爬升、平飞、转弯、下降、进近着陆等全部科目均按计划完成。公司预计将在 2027 年上半年完成适航取证。 凭借 5 吨最大业载和 2600 公里设计航程，W5000 指向一种机上完全无飞行员的货运模式，有望削减机组成本，并开通传统货机难以覆盖的稀薄或偏远航线。若 2027 年顺利取证，它将成为最早投入商业物流运营的大型无人货机之一，也是中国低空经济布局中的一个标志性节点。 该机最大起飞重量 10.8 吨，最大业载 5 吨，设计航程 2600 公里，相当于一次把一辆中型卡车的货物直送 2600 公里之外。飞机采用涡桨动力与自主驾驶、地面监控的运行模式，按设计一个机组可同时监控 6 至 7 架飞机。

telegram · zaihuapd · 11月14日 05:00

**背景**: W5000 由中国初创公司白鲸航线自主研发，项目于 2021 年启动，首架机已于去年 10 月在常州生产基地总装下线。此类大型货运无人机处于与消费级无人机完全不同的监管类别：在中国，起飞重量 25 公斤以上的无人机需按 CCAR-92 部规章进行适航审定，因此 2027 年的目标意味着要完成设计、试飞与生产等全链条的民航认证。涡桨动力（由燃气涡轮驱动螺旋桨）在中速、中空巡航时燃油效率较高，因而常被视为货运飞机的合适选择。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260321A0615B00">全球最大 无 人 货 运飞 机 ， 白 鲸 航 线 W 5000 ...</a></li>
<li><a href="https://www.163.com/dy/article/K886ASET05149OCK.html">平安产险护 航 白 鲸 启 航 ： W 5000 无 人 货 运 机 首飞开启 航 空新篇</a></li>
<li><a href="https://www.cnblogs.com/sweetheart-sole/p/21043927">2026...</a></li>

</ul>
</details>

**标签**: `#unmanned aviation`, `#autonomous cargo`, `#logistics`, `#China tech`, `#test flight`

---

<a id="item-13"></a>
## [新西兰仓库工人抗议 AI 监控如厕时间](https://www.independent.co.uk/news/world/australasia/new-zealand-workers-ai-bathroom-breaks-b3084317.html) ⭐️ 6.0/10

新西兰最大零售商 The Warehouse 集团位于奥克兰和基督城的配送中心本周有 300 多名工人抗议，Worker First 联盟指控管理层针对被系统追踪的如厕时间训斥员工，并有员工因强忍如厕而发生意外。公司首席人力官否认了最严重的指控，称所使用的扫描技术并非 AI、与如厕无关，也没有因引入库存无人机而裁撤岗位。 这场纠纷是 AI 驱动的职场监控从理论走向日常劳资冲突的一个具体而受关注的案例，说明以提升效率为名的追踪工具很容易演变为隐私与尊严问题，从而引发有组织的反弹。它也很可能被纳入更广泛的讨论：企业在部署自动化与监控系统前，必须向员工和工会披露哪些信息。 工会还称公司引入了大型机器人拣货设备和 AI 无人机，替代了部分库存团队的工作；公司则表示无人机并未裁撤任何岗位，但拒绝保证未来的职位安排，只承诺尽量协商并通过再培训安置员工。有关如厕监控的指控主要基于工会方面的陈述而非公开证据，同时公司也否认其扫描技术属于 AI。

telegram · zaihuapd · 11月14日 06:15

**背景**: 仓储运营商越来越多地使用计算机视觉摄像头、室内自主无人机和算法化任务追踪来衡量库存准确率与个人产出，而同一批数据也可以被用来评估员工的时间分配。新西兰《2020 年隐私法》对机构（包括雇主）如何收集和使用个人信息作出了规定，这也是该纠纷同时成为隐私议题和劳工议题的原因。由于这类系统通常从第三方供应商采购，员工往往只能通过工会渠道或在遭遇处分之后才得知其存在。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ndtv.com/world-news/new-zealand-workers-defecate-in-shopping-aisles-as-ai-tracks-bathroom-breaks-12324792">Workers Defecate In Shopping Aisles As AI Tracks Bathroom Breaks</a></li>
<li><a href="https://oecd.ai/en/incidents/2026-11-11-dcf0">AI Monitoring Leads to Worker Distress at New Zealand Retailer</a></li>
<li><a href="https://www.verity.net/">Verity | Warehouse Intelligence Platform - Autonomous Inventory ...</a></li>

</ul>
</details>

**标签**: `#AI surveillance`, `#workplace monitoring`, `#privacy`, `#labor rights`, `#New Zealand`

---

<a id="item-14"></a>
## [谷歌 AI Studio 设计师借助 WindowsiOS 在折叠 iPhone 上运行 Windows 11](https://www.windowslatest.com/2026/11/14/windows-11-can-run-on-apples-foldable-iphone-and-googles-ai-boss-proved-it-using-gemini-years-after-microsoft-gave-up-on-windows-phones/) ⭐️ 6.0/10

Google AI Studio 产品设计负责人 Ammaar Reshi 演示了 Windows 11 24H2 在一台名为 iPhone Duo 的折叠设备上本地运行，使用的是开源项目 WindowsiOS；据报道 Gemini 4 Carbon 参与了该过程，并且公开了演示视频。该演示通过基于 JIT 的 ARM64 翻译运行，无需越狱设备。 这是一个引人注目的概念验证，展示了在未越狱的 iOS 硬件上本地运行完整桌面操作系统的可能性，也说明基于 JIT 的翻译层在苹果平台限制下已经发展到相当程度。它可能会激发爱好者对 Windows on ARM 和移动虚拟化的探索，但目前仍只是个人演示，而非可实际使用的产品。 据该项目介绍，WindowsiOS 能以接近原生的 JIT 速度运行 Windows 11 24H2 ARM64，并依赖微软的 Prism 模拟器来运行部分传统 x86 应用。该方案需要约 12 GB 的镜像、一台 Apple Silicon Mac、开发工具以及 LLDB 调试器，而且目前尚无法对该演示进行独立验证。

telegram · zaihuapd · 11月14日 06:52

**背景**: Windows on Arm 通常运行原生 ARM64 软件，并通过微软的 Prism 模拟器翻译 x86 和 x64 应用，这也是 Arm 版 Windows 11 设备能够运行旧软件的原因。在 iOS 上，苹果严格限制即时编译（JIT），因此相关项目往往依赖启用调试器的工作流来允许 JIT 执行，用于开发和研究。WindowsiOS 将这些思路结合起来，在 iOS 之上翻译 ARM64 的 Windows 代码，而不是虚拟化一整台 PC。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ammaarreshi/WindowsiOS">GitHub - ammaarreshi/WindowsiOS: Native Windows 11 ARM64 on ...</a></li>
<li><a href="https://learn.microsoft.com/en-us/windows/arm/apps-on-arm-x86-emulation">How emulation works on Arm | Microsoft Learn</a></li>
<li><a href="https://www.windowscentral.com/software-apps/what-is-microsoft-prism">What is Microsoft 's Prism ? Explaining the... | Windows Central</a></li>

</ul>
</details>

**标签**: `#emulation`, `#Windows on ARM`, `#iOS`, `#JIT translation`, `#AI-assisted development`

---