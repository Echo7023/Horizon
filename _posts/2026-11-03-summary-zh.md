---
layout: default
title: "Horizon Summary: 2026-11-03 (ZH)"
date: 2026-11-03
lang: zh
---

> 从 39 条内容中筛选出 23 条重要资讯。

---

1. [GPT-6 Astra 直接读写 Qwen 权重，数学成绩提升近六倍](#item-1) ⭐️ 9.0/10
2. [vLLM v0.33.0rc3 升级至 PyTorch 2.14，停止发布 CUDA 12.9 构建](#item-2) ⭐️ 8.0/10
3. [Subvocal 用射频智能眼镜把无声口型转成文字](#item-3) ⭐️ 8.0/10
4. [Ubuntu LTS 内核近三周仍未修复严重 Linux 0day 远程代码执行漏洞](#item-4) ⭐️ 8.0/10
5. [博客称前沿大模型可原生读写神经网络原始权重](#item-5) ⭐️ 8.0/10
6. [树莓派 5 正式发布：搭载 2.4GHz Cortex-A76 与双 4K60 HDMI](#item-6) ⭐️ 8.0/10
7. [博客呼吁：珍爱的网站，请自行备份](#item-7) ⭐️ 7.0/10
8. [Show HN：基于开放数据构建的华沙市中心体素交互式 3D 地图](#item-8) ⭐️ 7.0/10
9. [GDPx 发布覆盖高价值领域的前沿模型基准](#item-9) ⭐️ 7.0/10
10. [笔记本规模复现支持“好视图优于下一词预测”的视觉-语言对齐结论](#item-10) ⭐️ 7.0/10
11. [LightMIS：13.1 万参数医学分割模型在边缘 GPU 上快 10.5 倍](#item-11) ⭐️ 7.0/10
12. [LongCat-2.5 发布：1.6 万亿参数原生多模态模型](#item-12) ⭐️ 7.0/10
13. [百度网盘摇一摇广告改用磁力计 CLHeading 绕过 iOS 运动权限限制](#item-13) ⭐️ 7.0/10
14. [ChatGPT 分享链接漏洞可致会话被劫持、私密对话泄露](#item-14) ⭐️ 7.0/10
15. [WIRED 调查：400 多个 AI 应用以普通工具为掩护暗藏色情深伪功能](#item-15) ⭐️ 7.0/10
16. [瑞典 ICA 多家门店遭网络攻击，冷柜被远程调至 50°C](#item-16) ⭐️ 7.0/10
17. [阿布扎比与 OpenAI 签署四项协议，推出「机器可读政府」计划](#item-17) ⭐️ 7.0/10
18. [SGLang v0.5.23 发布：合并 1007 个 PR，新增多款模型与 TPU7x 支持](#item-18) ⭐️ 6.0/10
19. [LLM 0.37 发布：新增 OpenAI 兼容端点配置命令与多模态嵌入支持](#item-19) ⭐️ 6.0/10
20. [人口普查局 AI 采用图表重制，凸显“超级智能”行政令冲突](#item-20) ⭐️ 6.0/10
21. [研究者求助：无法复现已发表机器学习基线的结果该如何呈现](#item-21) ⭐️ 6.0/10
22. [Anthropic 更新使用政策，禁止转售 Claude 访问权限](#item-22) ⭐️ 6.0/10
23. [DeepSeek Harness 团队提出 Super-agent 架构：常驻 Router 搭配上下文隔离 Worker](#item-23) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [GPT-6 Astra 直接读写 Qwen 权重，数学成绩提升近六倍](https://rikiyat.github.io/blog/weight-space-programming/) ⭐️ 9.0/10

MIT CSAIL 的研究人员于 2026 年 11 月 2 日发布博客，提出“权重空间编程”（weight-space programming）：要求 GPT-6 Astra 提升 Qwen3.5-0.8B 的数学能力时，该模型在没有任何梯度下降或训练循环的情况下，原生地检查并直接改写目标网络的权重，仅修改 131,072 个权重条目（约占其名义 8 亿参数的 0.016%），就把 MATH-500 的准确率从 7.9% 提升到 48.1%。在另一项演示中，Astra 将小模型“循环重复”的失败模式（前 96 次练习回答中有 85 次撞上 32,768 token 上限）定位到第 15 层和第 19 层 MLP 写出的某一个方向，并从这两层各自的 64 个输出列中减去了该方向。 这项成果正处在机制可解释性与模型编辑的交汇点，暗示了一条可能替代微调的新路径：与其重新训练，不如精准地改动极少量权重来修复某种特定失败模式或补上某项能力。如果前沿模型确实对权重空间具备可用的原生理解，这也直接关系到关于“递归自我改进”的讨论，以及未来修复模型缺陷的成本能低到什么程度。 这次改动极为稀疏——在约 8 亿参数中只触及约 131,072 个张量条目——但打这个补丁本身需要大量调查工作：研究者向 Astra 提供了练习题、通过 Python 访问权重的权限以及有限的模型执行预算，由智能体用 Python 计算出替换值，再提交修改后的张量进行测试。需要注意的是：这只是单个小模型在单个基准上的结果，且以研究博客而非同行评审论文的形式发布，因此能否推广到大模型和其他能力上仍未得到验证。

hackernews · dbreunig · 11月2日 18:21 · [社区讨论](https://news.ycombinator.com/item?id=50341174)

**背景**: 神经网络的“权重”是训练过程中学到的数值参数；通常要改变模型行为，只能在新数据上继续训练（梯度下降），成本高昂且会影响整个网络。机制可解释性是一门试图逆向解析网络内部单个权重、神经元和“方向”含义的研究领域，例如找出激活空间中对应“重复”这类行为的某个方向。权重空间编程则更进一步：不是由人类去分析网络，而是让一个 LLM 获得对原始权重张量的读写权限，自行推理并给出修改方案。Qwen 是阿里巴巴的开放权重模型系列，MATH-500 则是竞赛风格数学题的标准基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight - Space Programming: LLMs can natively read & write...</a></li>
<li><a href="https://venturebeat.com/technology/like-gene-editing-for-neural-networks-mit-researchers-used-gpt-6-astra-to-edit-qwens-open-weights-directly-boosting-math-performance">VentureBeat‘Like gene editing for neural networks’: MIT ...</a></li>
<li><a href="https://explainx.ai/blog/weight-space-programming-gpt-6-astra-edits-qwen3-5-0-8b-weights-math-7-9-to-48-1-mit-csail-2026">GPT-6 Astra Edits Qwen Weights: MATH-500 7.9% to 48.1% ...</a></li>

</ul>
</details>

**社区讨论**: 讨论区（1828 分、577 条评论）弥漫着震惊与兴奋：vessenes 表示自己“被震住了”，并坦言如果今早被问到 LLM 对自身权重的原生理解处于什么水平，他会猜是“与人类对神经元的理解相当或更低”。xg15 认为这一结果固然疯狂但并不完全出乎意料，因为当前 LLM 反复展现出快速掌握复杂系统的能力，比如编程智能体能在几秒内解释庞大的遗留代码库。vanyle 则反对“涌现能力”的说法，推测 Astra 是被刻意用神经权重数据训练出来的、属于迈向递归自我改进的一次尝试，至于这次尝试是否奏效还有待观察。

**标签**: `#mechanistic-interpretability`, `#model-editing`, `#LLM`, `#weight-space`, `#research`

---

<a id="item-2"></a>
## [vLLM v0.33.0rc3 升级至 PyTorch 2.14，停止发布 CUDA 12.9 构建](https://github.com/vllm-project/vllm/releases/tag/v0.33.0rc3) ⭐️ 8.0/10

vLLM 发布候选版本 v0.33.0rc3，包含来自 389 位贡献者（其中 122 位是新贡献者）的 927 个提交，并将框架升级至 PyTorch 2.14.0，同时配套 torchvision 0.29.0 与 Triton 3.8.0。该版本新增了大量模型支持，包括 Reflection Beam-1.0（501B MoE、23B 激活参数）、Yandex AliceAI-Foundation-80B-A3B、Recursive Flint（40B MoE、2.5B 激活参数）、Step-5 Preview 与 MiniCPM-OCR 1.0，同时彻底停止发布 CUDA 12.9 的 wheel 与镜像，只提供 CUDA 13.0 构建产物。 vLLM 是部署最广泛的开源大模型推理与服务引擎之一，因此它的打包方式与底层框架跃迁会直接影响所有大规模自建推理服务的团队。停止提供 CUDA 12.9 并升级到 PyTorch 2.14 意味着运维人员必须先验证驱动与工具链的兼容性，而新的投机解码与 ROCm 吞吐优化则能带来实实在在的服务成本下降。 投机解码方面有若干值得注意的新增：面向 DFlash、DSpark 等块扩散草稿模型的 XPress 精炼器，可选的有损校验策略 FLy（在 MI355X 和 B300 上带来 1.04–1.31 倍解码吞吐），以及量化草稿 lm_head（并发度为 1 时解码速度 +18%）。CUDA wheel 现已与 libtorch 实现 ABI 稳定，新增的 vllm/vllm-openai:v0.33.0-efa 镜像内置 AWS EFA 库以支持多节点 KV 传输，同时破坏性变更移除了 Medusa、MLP speculator 以及旧的 Ray compiled-graph 执行器。

github · khluu · 11月2日 10:10

**背景**: vLLM 是一个高吞吐、内存高效的大语言模型推理与服务引擎，最初由加州大学伯克利分校 Sky Computing Lab 开发，如今由超过 2000 名贡献者的社区共同维护。其核心创新是 PagedAttention 式的 KV 缓存管理，使服务器能够高效地对大量并发请求进行批处理。投机解码是一种相关技术：由一个小型“草稿”模型先提出候选 token，再由大目标模型进行校验，从而在不改变输出质量的前提下加速生成。AWS Elastic Fabric Adapter（EFA）是 EC2 实例上的一种网络接口，为 AI/ML 与 HPC 负载提供低延迟、高吞吐的节点间通信，这正是推出专用镜像对多节点服务具有重要意义的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/vllm-project/vllm">GitHub - vllm-project/vllm: A high-throughput and memory ...</a></li>
<li><a href="https://github.com/z-lab/dflash">z-lab/dflash: DFlash: Block Diffusion for Flash Speculative Decoding ...</a></li>
<li><a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/efa.html">Elastic Fabric Adapter for AI/ML and HPC workloads on Amazon ...</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#software release`, `#PyTorch`, `#CUDA`

---

<a id="item-3"></a>
## [Subvocal 用射频智能眼镜把无声口型转成文字](https://news.ycombinator.com/item?id=50340088) ⭐️ 8.0/10

YC F26 创业公司 The Subvocal Company 由两名佐治亚理工学院计算机专业学生创办，公开展示了一款智能眼镜：它通过低噪声射频传感，把用户无声的口型（甚至闭着嘴的“内部默念”）解码成文字，速度大致接近正常语速。团队最早在今年 2 月斯坦福 TreeHacks 黑客松上用肌电电极做原型，后来放弃该方案，改用穿透面部、并被舌头、嘴唇和软腭动作调制的无线电波。 如果该技术能够稳定工作，无声语音输入就能让人在图书馆、办公室和公共场所不打扰他人地向电脑口述内容，对视障或行动不便的无障碍用户以及免手操作场景都可能带来变革。它也让射频传感成为摄像头与麦克风输入方案（如 Wispr Flow）之外的竞争者。 创始人表示放弃肌电方案的原因是汗液导致信号漂移、电气干扰、电极位置难以复现，以及没人愿意把电极贴在脸上；剩下最难的问题是跨用户泛化（每个人的面部解剖结构差异极大）以及让天线布局尽可能覆盖发音器官。眼镜不使用摄像头也不使用麦克风，公司将该硬件定位为早期产品，而非已验证、可量产的设备。

hackernews · aarushyadav · 11月2日 17:16

**背景**: 默读或心中念词时产生的“内部语音”被称为 subvocalization（无声言语），它伴随喉部与发音肌肉极细微、通常无法察觉的运动。无声语音接口就是捕捉这些非声学信号（肌电、脑电、摄像头，或本例中的射频），再转换成文字或合成语音，MIT 媒体实验室的 AlterEgo 是最知名的早期学术尝试。射频传感的原理类似雷达：发射端向口腔区域发出微弱无线电波，接收端测量回波被运动组织扰动的方式，再由训练好的模型把这些扰动映射为音素和词。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://runany.dev/blog/subvocal/">Subvocal: glasses that type what you mouth silently</a></li>
<li><a href="https://en.wikipedia.org/wiki/Subvocalization">Subvocalization</a></li>
<li><a href="https://en.wikipedia.org/wiki/Silent_speech_interface">Silent speech interface</a></li>

</ul>
</details>

**社区讨论**: 评论整体非常热情，认为这个概念堪比科幻，甚至可能像买鼠标或键盘一样普及，尤其看好它在无障碍和比开口说话更快的输入上的价值。质疑主要集中在实用层面：非标准头型和鼻型能否戴稳（有人希望保留可调金属鼻托，也有人想要能夹在自己近视镜上的版本）、信号处理是在眼镜端还是交给手机 App、续航表现，以及射频发射器长期贴近眼睛和大脑是否影响健康。

**标签**: `#subvocalization`, `#smart-glasses`, `#human-computer-interaction`, `#accessibility`, `#RF-sensing`

---

<a id="item-4"></a>
## [Ubuntu LTS 内核近三周仍未修复严重 Linux 0day 远程代码执行漏洞](https://freenode.net/article/ubuntu-lts-kernels-still-unfixed-for-critical-cve-2026-98432) ⭐️ 8.0/10

在严重 Linux 内核远程代码执行 0day 漏洞 CVE-2026-98432 被公开近三周后，Ubuntu LTS 内核依然没有发布修复补丁；Ubuntu 安全跟踪页仅将其标记为“High”（高）优先级，而非通常会触发计划外紧急内核更新的“Critical”（严重）级别。同时，Ubuntu 既未给出延迟修复的官方解释，也没有向受影响用户提供任何缓解措施指引。 所有运行 Ubuntu 服务器的用户都暴露在一个可被远程利用、却既无厂商补丁也无官方临时缓解方案的内核漏洞之下，这对生产环境构成了直接的运维风险。这种沉默同时也在损害 Ubuntu 作为服务器默认选项的信誉，尤其当 RHEL 等竞争对手至少给出了（尽管含糊的）缓解建议时，对比更加明显。 Ubuntu 既未解释延迟原因，也未提供缓解操作说明；而 Red Hat 的安全公告给出了一个变通方案，称其“可降低受此漏洞影响的程度，但无法完全阻止”，却未说明具体含义。有评论者指出目前尚未观察到野外实际利用，而 Ubuntu 的 Livepatch 免重启打补丁服务只有在补丁真正存在之后才能发挥作用。

hackernews · majorchord · 11月2日 18:39 · [社区讨论](https://news.ycombinator.com/item?id=50341462)

**背景**: 零日（0day）漏洞是指在公开时还没有可用补丁的安全缺陷，防御方只能依靠临时变通手段。远程代码执行（RCE）是一类允许攻击者通过网络在目标机器上运行任意代码的漏洞，若发生在内核层，通常意味着整机被完全攻陷。Ubuntu LTS（长期支持）版本之所以被广泛用于服务器，正是因为它承诺多年稳定且及时打补丁的内核；Ubuntu Livepatch 是 Canonical 提供的免重启应用关键内核修复的机制，但它只是分发厂商补丁，而非自己开发补丁。对于家用路由器等嵌入式设备而言，内核打补丁尤其困难——它们运行 Linux，却常常永远收不到内核安全更新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zero-day_vulnerability">Zero-day vulnerability - Wikipedia</a></li>
<li><a href="https://www.tenable.com/cybersecurity-guide/principles/zero-day-vulnerability">What is a zero-day vulnerability? | Tenable®</a></li>
<li><a href="https://ubuntu.com/tutorials/enable-the-livepatch-service">Apply kernel patches without rebooting - Ubuntu</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论整体偏批评：多位用户表示缺补丁已动摇他们对 Ubuntu 的信任，未来新服务器会尽量避开它；也有人要求官方解释为何一个看似并不复杂的内核修复拖了数周。评论者将 Ubuntu 的沉默与 RHEL 公布的缓解指引做对比，并把话题延伸到常年不更新内核的家用路由器上；不过也有参与者认为，鉴于尚无野外利用的观察结果且存在多种缓解手段，当前的风险被夸大了。

**标签**: `#linux`, `#security`, `#ubuntu`, `#vulnerability`, `#kernel`

---

<a id="item-5"></a>
## [博客称前沿大模型可原生读写神经网络原始权重](https://www.reddit.com/r/MachineLearning/comments/1xm89ef/sparks_of_weightspace_programming_llms_can/) ⭐️ 8.0/10

一篇题为《Sparks of Weight-Space Programming》的博客文章声称，前沿大语言模型能够原生地读取和写入神经网络权重，其能力远超人类或传统算法的预期。作者称，名为“GPT-6 Astra”的模型仅凭原始权重就能判断出一个网络被训练用来做什么，并且在没有环境反馈的情况下，从零写出小型游戏网络，其表现超过了用 PPO 训练 1 亿步的网络。 如果这一结论能够成立，那么对大模型而言这将是一种质变级的新能力——而它从未被专门优化过——并且会直接影响两个方向：机制可解释性（通过读取权重来理解模型行为）和优化（直接生成或编辑权重，而非依赖 PPO 之类的梯度训练）。它还暗示了语言模型与其他神经网络之间可能存在一种新的接口，可能改变小型模型的生成与调试方式。 证据来自一篇单独的博客文章，而非经过同行评审的论文或公开的基准测试；文中提到的模型名称“GPT-6 Astra”也不对应任何有公开记录的模型，因此这些说法应被视为尚未验证。文中展示的示例都是小型游戏网络，作者没有详细说明评测协议、权重的编码格式，也没有说明模型实际读取了多少原始权重张量。

reddit · r/MachineLearning · /u/RobbinDeBank · 11月2日 20:18

**背景**: 神经网络“权重”是训练产生出的数百万乃至数十亿个数值参数；通常没有人直接查看它们，因为它们看起来只是无意义的浮点数数组，网络的功能主要靠行为来理解。PPO（近端策略优化）由 Schulman 等人在 2017 年提出，是一种流行的策略梯度强化学习算法，通过反复在环境中收集经验并更新策略网络来训练深度强化学习智能体。所谓“权重空间编程”，指的是让语言模型直接查看并编辑另一个网络的权重，这与目前普遍的做法——用大模型去优化提示词及其周边代码等文本产物——形成鲜明对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight - Space Programming : LLMs can natively read...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proximal_policy_optimization">Proximal policy optimization</a></li>
<li><a href="https://huggingface.co/spaces/akhaliq/weight-space-programming-demo">Weight - Space - Programmed Qwen3.5-0.8B - a Hugging Face Space...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#interpretability`, `#optimization`, `#neural-network weights`, `#machine-learning research`

---

<a id="item-6"></a>
## [树莓派 5 正式发布：搭载 2.4GHz Cortex-A76 与双 4K60 HDMI](https://t.me/zaihuapd/44854) ⭐️ 8.0/10

树莓派 5 正式发布，搭载 2.4GHz 四核 64 位 Arm Cortex-A76 CPU 和 VideoCore VII GPU，支持 OpenGL ES 3.1 与 Vulkan 1.2，4GB 型号售价 60 美元、8GB 版本售价 80 美元（另加当地税费）。它还提供双路 4K60p HDMI 输出、4K60p HEVC 解码器、双频 802.11ac Wi-Fi、蓝牙 5.0/BLE、支持 SDR104 模式的高速 microSD 接口，以及两个可同时运行在 5Gbps 的 USB 3.0 端口。 这是目前使用最广泛的单板计算机的一次重大代际跃升，在相同的低价区间引入了笔记本级 CPU 核心和强得多的 GPU，将同时惠及爱好者、教育用户和嵌入式系统开发者。双路 4K60 HDMI 以及真正高速的 USB 3.0 和存储接口，使树莓派 5 比以往型号更有可能充当桌面替代机或媒体中心。 CPU 基于 Arm 的 Cortex-A76，Arm 称其整数性能比上一代 Cortex-A75 提升最高 25%、浮点性能提升最高 35%；VideoCore VII 集成 GPU 在 Broadcom BCM2712 SoC 中提供 12 个核心、最高 800MHz 频率。需要注意，60 美元/80 美元的报价不含当地税费，而且 SDR104 microSD 支持只有搭配足够高速的存储卡才能发挥作用。

telegram · zaihuapd · 11月2日 12:00

**背景**: 树莓派是一系列信用卡大小的单板计算机，运行 Linux，广泛用于教育、创客项目和工业/嵌入式产品。Cortex-A76 是采用 Armv8.2-A 架构的 64 位 CPU 核心，由 Arm 设计，定位为兼具移动能效与笔记本级性能。VideoCore 是博通的一系列低功耗多媒体处理器，在树莓派主板上用作集成 GPU；SDR104 则是 UHS-I microSD 的高速总线模式，相比旧的默认模式能显著提升存储卡吞吐量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ARM_Cortex-A76">ARM Cortex-A76</a></li>
<li><a href="https://www.notebookcheck.net/Broadcom-VideoCore-VII-Benchmarks-and-Specs.873281.0.html">Broadcom VideoCore VII - Benchmarks and Specs - Notebookcheck</a></li>
<li><a href="https://media.digikey.com/pdf/Data+Sheets/Viking+PDFs/PSFUSDzzzzCzzzz_W_F_DS.pdf">Datasheet for: SDHC/SDXC UHS104 microSD Cards - Digi-Key</a></li>

</ul>
</details>

**标签**: `#Raspberry Pi`, `#single-board computer`, `#hardware release`, `#Arm Cortex-A76`, `#embedded systems`

---

<a id="item-7"></a>
## [博客呼吁：珍爱的网站，请自行备份](https://blog.mistys-internet.website/post/2026/10/29/if-you-love-a-website-back-it-up/) ⭐️ 7.0/10

一篇题为《如果你爱一个网站，就把它备份下来》的博客文章主张，人们应当亲自归档自己珍视的网站，而不是想当然地认为互联网档案馆（Internet Archive）或其他服务会替自己保存。该文在 Hacker News 上引发了 94 条评论的讨论，读者们分享了具体工具——用于选择性抓取的浏览器扩展 ArchiveWeb.page，以及可将页面保存为自包含 HTML 文件的 SingleFile——并讲述了论坛从未被爬取便悄然消失的亲身经历。 这场讨论凸显了开放网络已变得多么脆弱：链接腐烂（link rot）只需几年就会让书签失效，而许多小型论坛和个人博客根本从未被大规模爬虫收录。有评论者警告，集中化的 LLM 可能日益取代开放网络成为主要信息来源，因此有意识的个人归档正成为一种抵御集体记忆流失的务实手段。 评论者指出，Wayback Machine 的覆盖范围远非完整——一位读者发现自己关心的某个论坛的大部分内容从未被它爬取过——而即便是 AI 辅助的重建，也只能抢救某些档案中已存在的内容，无法恢复真正已经消失的数据。推荐的工具从用于快速单次快照的 SingleFile，到可手动挑选抓取哪些页面及页面元素的 ArchiveWeb.page，再到 ArchiveBox 这类自托管方案，可将抓取结果保存为用户自己掌控的 WARC 文件。

hackernews · ingve · 11月2日 13:25 · [社区讨论](https://news.ycombinator.com/item?id=50336518)

**背景**: 链接腐烂（link rot）指的是超链接随着页面迁移、改版或消失而逐渐失效的现象，对任何引用或收藏网络内容的人来说都是长期困扰。互联网档案馆的 Wayback Machine 是最知名的公共补救手段，它会随时间爬取并保存页面快照，再通过其网站回放。为实现长期保存，档案机构通常以 WARC（Web ARChive）格式存储抓取结果，这是一种标准化容器，把多个资源连同标头、时间戳等元数据打包在一起。ArchiveBox 之类的工具则将这一能力带给个人用户，让他们可以运行自己的归档服务器，导入网址、浏览器历史或书签，并保存 HTML、PDF、媒体文件等。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WARC_(file_format)">WARC ( file format ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Memento_Project">Memento Project - Wikipedia</a></li>
<li><a href="https://iipc.github.io/warc-specifications/specifications/warc-format/warc-1.1/">The WARC Format</a></li>

</ul>
</details>

**社区讨论**: 整体情绪是支持与务实，而非争论。读者们分享了各自的损失——失效的书签、一个存放着手工扫描照片的 Angelfire 站点在维持 20 年后终于下线、以及一个大部分内容未被爬取便消失的心爱论坛——同时推荐用 ArchiveWeb.page 和 SingleFile 进行抓取。一个值得注意的忧虑是，集中化的云端 LLM 可能很快取代开放网络成为信息来源，并有可能改写过去，这促使人们呼吁购买纸质书籍，并在重要网站仍然存在时将其归档。

**标签**: `#digital-preservation`, `#link-rot`, `#web-archiving`, `#open-web`, `#tooling`

---

<a id="item-8"></a>
## [Show HN：基于开放数据构建的华沙市中心体素交互式 3D 地图](https://p.migdal.pl/warsaw-vibe-voxel/) ⭐️ 7.0/10

开发者 stared 发布了一个 Show HN 项目，把华沙市中心渲染成可自由探索的《我的世界》风格体素城市，支持调整日期、时刻和天气，还能点击行人进行操控（灵感来自《地下城守护者》）。该地图由 OpenStreetMap 的几何数据、GUGiK/Geoportal 用于建筑高度与树木的 LiDAR、用于配色的航拍影像，以及华沙官方树木数据库（用于季节性树叶变化）共同构建，源代码已在 GitHub 上开源。 它展示了开放地理数据——OpenStreetMap、国家级 LiDAR、市政树木清单——在不依赖任何专有素材的情况下，可以被推进到多么精致、有趣的浏览器体验。对开放数据与创意编程社区而言，这是一个可复用的范本，说明如何把公共数据集转化为平易近人的 3D 可视化；不过性能方面的抱怨也表明，这条 WebGL 渲染管线在扩展到更大范围或更弱硬件之前仍需优化。 该项目主要面向桌面端设计，移动版明显偏重（有评论者反映 Safari 会重新加载页面），且由于几何体与体素数据需要在客户端抓取和生成，首次加载可能耗时较长。项目已在作者的 GitHub 仓库开源，其他人可以复用这套管线来构建别的城市。

hackernews · stared · 11月2日 16:25 · [社区讨论](https://news.ycombinator.com/item?id=50339221)

**背景**: 体素本质上就是“三维像素”——一个三维网格，每个立方体单元要么被填充要么为空——由此形成被《我的世界》以及 MagicaVoxel 这类体素美术工具带火的方块化复古外观。用这种风格还原真实城市需要准确的建筑轮廓与高度：OpenStreetMap 提供建筑轮廓、街道和有轨电车轨道，而波兰 Geoportal 的机载 LiDAR 扫描提供点云，其 XYZ 坐标可以还原屋顶高度和树冠。航拍影像则提供颜色，整个场景最终通过 WebGL 在浏览器中渲染。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geoportal.gov.pl/en/data/lidar-measurements-lidar/">LIDAR measurements (LIDAR) – Geoportal.gov.pl</a></li>
<li><a href="https://ephtracy.github.io/">GitHub Pages - MagicaVoxel</a></li>
<li><a href="https://blog.danielschroeder.me/2024/05/voxel-displacement-modernizing-retro-3d/">Voxel Displacement Renderer — Modernizing the Retro 3 D Aesthetic</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了创意，但讨论重心明显落在性能上：有人报告在 Linux 上的 Firefox 中帧率不足 1 FPS，另一位使用 3080 Ti 笔记本的用户测得单帧约 120 毫秒，且两帧之间存在巨大空档，尽管更新循环本身接近 30 FPS。也有人给出较温和的意见——希望默认天气是晴天而不是下雨，并指出移动端 Safari 难以承受——作者则提到 Streets of Prague 等类似项目作为先行案例。

**标签**: `#voxel-rendering`, `#3D-visualization`, `#OpenStreetMap`, `#creative-coding`, `#WebGL-performance`

---

<a id="item-9"></a>
## [GDPx 发布覆盖高价值领域的前沿模型基准](https://newsletter.semianalysis.com/p/gdpx-measuring-frontier-model-capabilities) ⭐️ 7.0/10

SemiAnalysis 推出了 GDPx 前沿基准，覆盖芯片设计、软件工程、金融、法律、网络安全、生物、材料科学、量化交易、对齐、硬件设计和递归自我改进等 11 个高经济价值领域。该基准提供实时排行榜、分领域结果和每个任务的成本数据。 GDPx 将评测重心转向具有经济价值、需要智能体完成的工作，而非通用学术题，这可能帮助企业和技术实验室在最有希望产生早期 AI 收入的领域比较前沿模型。它还将对齐与 RSI 纳入同一评分体系，把能力与安全视为同一个测量问题。 该基准与领域专家合作伙伴共同构建，报告分领域得分以及每个任务的成本，但目前可见的摘要并未披露任务数量、评分方法或初始模型结果。其 11 个领域范围混合了工程、金融、法律、网络安全、生物、材料科学、对齐和递归自我改进。

rss · Semianalysis · 11月2日 01:51

**背景**: 前沿模型是领先实验室开发的最强通用 AI 系统，而基准是用来比较它们的标准化测试。智能体基准评估模型能否借助工具、在极少人工帮助的情况下完成多步骤任务，这比单轮问答更接近真实专业工作。RSI 指 AI 系统反复设计能力更强的后继系统，而对齐研究则关注如何让 AI 系统追求预期目标。GDPx 将这些领域归在一起，是因为它认为首个万亿美元 AI 收入将集中在能以高投资回报率部署前沿智能的行业。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/gdpx-measuring-frontier-model-capabilities">GDPx: Measuring Frontier Model Capabilities Across the Most ...</a></li>
<li><a href="https://gdpx.semianalysis.com/domains">GDPx is the best benchmark for measuring general agentic ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Recursive_self-improvement">Recursive self-improvement</a></li>

</ul>
</details>

**标签**: `#AI benchmarks`, `#frontier models`, `#model evaluation`, `#AI capabilities`, `#ML research`

---

<a id="item-10"></a>
## [笔记本规模复现支持“好视图优于下一词预测”的视觉-语言对齐结论](https://www.reddit.com/r/MachineLearning/comments/1xlzoze/smallscale_check_of_good_views_beat_nexttoken/) ⭐️ 7.0/10

一位 Reddit r/MachineLearning 用户对 Balestriero 与 LeCun 2026 年的论文结论做了受控的笔记本规模复现：该论文声称，用“好视图”（同一张照片的两条不同描述）训练时，文本编码器与图像编码器的对齐速度快于“坏视图”或下一词预测。实验使用 10,000 张 COCO 图片（每张 5 条人工描述）、冻结的 DINOv2-base 图像编码器，以及三种条件下完全相同的 1100 万参数文本编码器，结果好视图的互 10-NN 对齐分数为 0.320，掩码坏视图为 0.192，下一词预测为 0.148（随机基线 0.010）。 原论文最大规模的实验使用了机器生成的图像描述，因此存在图像信息泄漏进文本、从而夸大“好视图”优势的可能；本次复现仅使用人工描述，排除了这一混淆因素，仍然重现了相同的排序。如果该效应在更大规模下依然成立，将为“下一词预测是一种较弱的‘坏视图’目标、不利于模态对齐”这一带有 JEPA 色彩的论点提供支持，并对多模态模型的训练方式产生影响。 实验训练 3,000 步、批大小 256，采用 VICReg 风格的方差/协方差防坍缩损失（而非论文中的 SIGReg）；作者也指出了重要局限：仅 1100 万参数和 8,000 张训练图片，远小于原论文的 1.09 亿参数与 720 亿规模，且只用了单一数据集和单一图像模型，同时“好视图”需要知道哪些描述对应同一张照片。加入一次拟合旋转后的检索 R@1 差距明显缩小（0.084 对 0.063 对 0.057），且下一词预测基线的最优学习率恰好落在作者搜索范围的上界，说明结论对度量方式和超参数较为敏感。

reddit · r/MachineLearning · /u/Traditional_Frame763 · 11月2日 15:08

**背景**: “柏拉图表示假说”认为，在不同模态和目标上训练的模型会收敛到对现实的共享表示，这也是视觉与语言嵌入可以相互比较的前提。Balestriero 与 LeCun 的后续工作将下一词预测视为一种被喂入“坏视图”（单条描述并掩码部分词）的 JEPA 式目标，并主张用同一输入真正不同的视图来训练能更快实现模态对齐。DINOv2 是一种自监督视觉 Transformer，其冻结特征可作为强大而稳定的图像表示；VICReg 则是一种通过对各维度施加方差约束与去相关约束来防止嵌入坍缩的正则化方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/papers/2610.39302">Paper page - Proving and Improving the Platonic Representation...</a></li>
<li><a href="https://dinov2.metademolab.com/">A self - supervised vision transformer model by FAIR</a></li>
<li><a href="https://arxiv.org/abs/2105.04906">[2105.04906] VICReg: Variance-Invariance-Covariance ...</a></li>

</ul>
</details>

**标签**: `#multimodal learning`, `#representation learning`, `#replication study`, `#self-supervised learning`, `#vision-language alignment`

---

<a id="item-11"></a>
## [LightMIS：13.1 万参数医学分割模型在边缘 GPU 上快 10.5 倍](https://www.reddit.com/r/MachineLearning/comments/1xm8dbo/lightmis_ultralightweight_medical_image/) ⭐️ 7.0/10

LightMIS 作者发布了超轻量级二维二值医学图像分割模型，仅有 13.1 万个参数，通过直接聚合多尺度编码器特征取代了逐阶段学习的解码器。该模型在相同 nnU-Net 协议下、覆盖六个数据集和五种成像模态完成训练与评估，据称其模态宏平均 Dice 与 IoU 与 nnWNet 相当，而参数量减少 98.14%、GFLOPs 减少 94.58%；在 Arm Mali-G52 MC2 边缘 GPU 上，完整模型运行速度约为 nnWNet 的 10.5 倍，且实现 100% GPU 算子覆盖、无 CPU 回退。 在低功耗临床与嵌入式硬件上部署分割模型，往往受限于内存、算力和算子支持，因此一个能以极小代价维持 nnU-Net 级精度的模型，有可能让端侧医学影像分析真正可行。完整的 GPU 算子覆盖在实用层面尤为关键，因为在此类设备上任何 CPU 回退都会严重拖垮时延与内存预算。 对比对象是 CVPR 2025 的 nnWNet，该模型重新审视了 Transformer 在生物医学分割中的使用方式；两个模型均在相同受控环境下使用 nnU-Net v2.3.1 从零训练，以保证比较公平。其适用范围被有意收窄：仅限二维二值分割，结果以跨模态平均值形式报告，而非宣称在单一数据集上达到最优，同时论文、代码与检查点均已公开以便复现。

reddit · r/MachineLearning · /u/OkLion2068 · 11月2日 20:22

**背景**: nnU-Net 是一个自配置分割框架，会根据给定数据集自动调整预处理、网络结构、训练与后处理流程，已成为医学图像分割领域事实上的基准。nnWNet 在这一流程基础上引入 Transformer 组件，并报告了相对 nnU-Net 基线具有统计显著性的提升。Dice 与 IoU 是衡量分割质量的标准重叠度指标，而参数量与 GFLOPs 则近似反映模型规模与计算开销。Arm Mali-G52 MC2 是一款双核主流移动 GPU，常见于入门级手机与嵌入式芯片，正是此类工作所面向的资源受限目标硬件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/MIC-DKFZ/nnUNet">GitHub - MIC-DKFZ/nnUNet · GitHub</a></li>
<li><a href="https://openaccess.thecvf.com/content/CVPR2025/papers/Zhou_nnWNet_Rethinking_the_Use_of_Transformers_in_Biomedical_Image_Segmentation_CVPR_2025_paper.pdf">nnWNet : Rethinking the Use of Transformers in Biomedical Image...</a></li>
<li><a href="https://www.arm.com/products/silicon-ip-multimedia/gpu/mali-g52">Mali-G52 | Boosting mobile visuals and AI – Arm®</a></li>

</ul>
</details>

**标签**: `#medical-image-segmentation`, `#edge-ai`, `#lightweight-models`, `#nnU-Net`, `#model-efficiency`

---

<a id="item-12"></a>
## [LongCat-2.5 发布：1.6 万亿参数原生多模态模型](https://longcat.ai/blog/longcat-2.5/) ⭐️ 7.0/10

LongCat 团队发布 LongCat-2.5，这是一个面向长程 agent 任务的原生多模态模型，总参数达 1.6 万亿，每个 token 约激活 480 亿参数。相比 LongCat-2.0，它强化了视觉理解与 agentic coding 能力，核心做法是把视觉信号编码为多级离散 token，与文本统一处理，从而支持视觉编程等任务。 凭借 1.6 万亿总参数与稀疏激活设计，LongCat-2.5 跻身少数前沿规模多模态模型之列，而它把视觉与语言统一为离散 token 的做法，指向用同一套 next-token prediction 目标处理两种模态。对于需要读取截图、图表或代码并在多步操作中持续执行的 agent 应用开发者来说，如果其宣称的能力得到验证，将直接受益。 该模型已可通过官网试用并接入 API，但 GitHub 与 HuggingFace 版本尚未开放，因此目前还无法自行部署或检视模型权重。此次发布公告本身没有给出基准测试成绩或架构细节；第三方模型信息站显示其支持多模态输入，上下文窗口约为 100 万 token。

telegram · zaihuapd · 11月2日 03:08

**背景**: LongCat 是美团旗下的模型系列，其 2.x 代把重心放在 agent 型任务而非单纯的对话。混合专家（MoE）架构让总参数保持很大，但每个 token 只激活其中一小部分，从而降低推理成本——这里是 1.6 万亿中的约 480 亿。“原生多模态”指模型从训练之初就同时接触交错的视觉与文本数据，而不是事后外挂一个视觉编码器；常见做法是用视觉 tokenizer（如 VQ-VAE 系或更新的语义化 tokenizer）把图像转成离散 token，使图像与文字共享同一词表和同一预测目标。“长程”（long-horizon）agent 任务指的是需要多步执行的工作流，agent 要在多轮交互中自行规划、调用工具并从错误中恢复，尽量不需要人工介入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://llm-stats.com/models/longcat-2.5">LongCat - 2 . 5 Benchmarks, Pricing & Context Window</a></li>
<li><a href="https://innovation-cat.github.io/posts/2025/12/tokenization/">Discrete Visual Tokenizers for Multimodal LLMs: Bridging ...</a></li>
<li><a href="https://www.emergentmind.com/topics/long-horizon-agentic-tasks">Long - Horizon Agentic Tasks Overview</a></li>

</ul>
</details>

**标签**: `#multimodal`, `#LLM`, `#model release`, `#agents`, `#MoE`

---

<a id="item-13"></a>
## [百度网盘摇一摇广告改用磁力计 CLHeading 绕过 iOS 运动权限限制](https://t.me/zaihuapd/44850) ⭐️ 7.0/10

有开发者借助 AI 分析百度网盘 iOS 版的广告跳转逻辑，发现框架中存在一个名为 NoShake（「没有运动」）的变体：它绕开 CoreMotion，改用 Core Location 的 CLHeading 读取磁力计数据来判断手机是否晃动。因此用户即使禁用了陀螺仪和加速度计权限，仍会被「摇一摇」跳转广告，报告还指出在特定参数下等待约 1 秒会自动执行广告点击。 这说明应用层的「暗黑模式」可以绕过苹果不断收紧的系统级运动数据限制，用户自以为已经屏蔽了摇一摇跳转广告，实际上仍可能被识别动作并被强制跳转。这也给 iOS 的隐私管控提出了难题——一个通常与指南针、导航相关的传感器被拿来当作广告触发器，百度网盘以及苹果对运动数据限制的执行力度很可能因此受到更多审视。 此次分析的样本是 10 月 22 日发布的百度网盘 13.36.0 iOS 版，其核心手法在于：通过 CLLocationManager 获取的 CLHeading 航向数据归属于定位服务权限，而不是管控 CoreMotion 的「运动与健身」权限。与这一发现同时流传的信息显示，13.36.5 等后续版本面对 iOS 27.2 的摇一摇跳转限制时表现有所不同，说明这场攻防可能已在变化。

telegram · zaihuapd · 11月2日 09:27

**背景**: 国内不少 App 依靠「摇一摇跳转」广告变现：手机轻微一晃就会弹出全屏广告或直接拉起第三方应用，这种逻辑传统上通过苹果的 CoreMotion 框架实现，该框架提供加速度计和陀螺仪数据，需要「运动与健身」权限。苹果近年来在系统层面不断限制这类由运动数据触发的跳转，近期的 iOS 27.2 等版本正是针对这一模式。而 Core Location 的 CLHeading 是另一套 API，通常用于指南针、地图和导航：调用 CLLocationManager 的 startUpdatingHeading() 会返回由磁力计计算出的磁航向，它受定位权限管辖而非运动权限，因此可以充当绕过的口子。此类逆向分析一般需要反编译或动态调试 App 二进制，观察其广告 SDK 如何响应传感器回调。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@robdeans/measuring-differences-of-degrees-using-cllocations-clheading-5f13f93756d7">Measuring Differences of Degrees Using CLLocation’s CLHeading</a></li>
<li><a href="https://x.com/afteroffline/status/2116187345670250765">After Offline离线后 on X: "IOS 27.2依旧治不了百度网盘摇一摇广告 ...</a></li>
<li><a href="https://www.bilibili.com/en/video/BV1XKxj6YEnE/">Baidu Netdisk's shake-to-open ads can bypass Apple's system ...</a></li>

</ul>
</details>

**标签**: `#mobile privacy`, `#iOS`, `#reverse engineering`, `#dark patterns`, `#Baidu Netdisk`

---

<a id="item-14"></a>
## [ChatGPT 分享链接漏洞可致会话被劫持、私密对话泄露](https://www.parameter.ai/labs/we-found-a-gap-at-openai) ⭐️ 7.0/10

Parameter 安全研究团队披露了一个 ChatGPT 分享链接漏洞：攻击者构造的恶意分享对话可以在已登录受害者的会话中执行代码，读取私密对话并把数据外传到外部服务器，而受害者只需打开链接，无需安装任何应用。OpenAI 复现了代码执行和私密会话窃取两个概念验证，将定级从 P2 提升为 P1，并于 10 月 26 日完成修复，同时向研究团队支付了 5000 美元赏金。 ChatGPT 拥有数以亿计的用户，而分享对话链接是极常见的使用场景，因此一个能把看似无害的分享链接变成会话级代码执行的漏洞，对普通用户构成直接的账号接管与隐私风险。P1 定级和赏金规模印证了问题的严重性，同时也说明 AI 聊天前端中越来越多的富媒体组件（预览、图表、渲染器）正在扩大攻击面。 漏洞根源在于 ChatGPT 预览功能与图表组件之间的消息处理缺陷，使注入的内容能够在已登录会话的上下文中执行。修复完全在服务端完成，并覆盖了 ChatGPT 网页前端的两个版本，用户无需更新或采取任何操作；相关细节也是在补丁上线之后才对外公布。

telegram · zaihuapd · 11月2日 10:24

**背景**: ChatGPT 的分享链接是一个公开 URL，任何人打开都能看到被分享的对话内容，因此很容易被用作投递恶意内容的载体。此类漏洞本质上类似跨站脚本攻击（XSS）：来自分享对话的不可信数据被聊天前端当作可执行代码解析，从而以受害者权限运行。OpenAI 的 P1 是其安全报告定级中的最高严重级别，通常保留给账号接管、大规模数据泄露等具有严重现实影响的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.parameter.ai/labs">Parameter Labs - Security research and engineering notes ...</a></li>
<li><a href="https://cyberpress.org/openai-fixes-high-severity-chatgpt-flaw/">OpenAI Fixes High-Severity ChatGPT Flaw That Exposed Private ...</a></li>
<li><a href="https://aiweekly.co/alerts/openai-patches-chatgpt-share-link-flaw-that-hijacked-sessions">OpenAI Patches ChatGPT Share-Link Flaw That Hijacked Sessions</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#ChatGPT`, `#OpenAI`, `#XSS`

---

<a id="item-15"></a>
## [WIRED 调查：400 多个 AI 应用以普通工具为掩护暗藏色情深伪功能](https://www.wired.com/story/hundreds-of-mundane-ai-apps-are-hiding-abusive-deepfake-features/) ⭐️ 7.0/10

WIRED 于 11 月 2 日发布调查，发现一个由 400 多个相互关联的应用和网站组成的网络，它们对外以宠物画像、语言学习等普通 AI 工具示人，却在特定条件下加载色情深度伪造界面，允许用户上传他人照片生成露骨图像或视频。研究人员通过共享代码、域名和广告追踪数据将这些站点串联起来；其中 27 款应用在 9 月仍上架 Google Play，累计下载量超过 35 万次，不少标注为适合所有年龄段。在 WIRED 提供线索后，苹果下架了 19 款应用，谷歌在被问询前已移除其中大部分，Meta 则表示已阻止 209 款相关应用投放广告。 这一案例说明应用商店审核很容易被绕过：一款看似无害的应用可以先通过审查，之后再替换为滥用性内容，使平台的内容审核成为那些照片被未经同意使用的人的最后一道防线。它同时也给为这类运营提供资金的广告生态带来压力，因为广告往往是串联起这个刻意碎片化、规模庞大的应用与网站网络的唯一可见线索。 苹果表示，开发者在应用通过审核之后替换了远程加载的网页内容，这种手法让同一个已获批的应用无需重新提交即可改变行为。WIRED 的报道依据中文代码、托管信息和域名记录，将该网络与中文开发者及一家在香港注册的公司联系起来；这一归属判断属于媒体与研究人员的调查结论，相关运营方未回应置评请求。

telegram · zaihuapd · 11月2日 12:45

**背景**: 深度伪造（deepfake）指用 AI 生成或篡改的图像、视频或音频，让人呈现出从未做过的事或说过的话；其中色情深度伪造往往只需一张真实人物的普通照片即可制作，已成为生成式模型最普遍且危害最大的滥用形式之一。应用商店主要依赖上架前审核，但如今许多应用通过远程网页渲染界面，审核人员看到的版本可能与用户最终获得的版本并不一致。由于这类运营通常同时维护数百个高度相似的应用以在被下架后继续存活，调查人员和平台越来越依赖共享代码特征、托管服务商和广告标识来追踪它们，而非应用名称。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Deepfake">Deepfake - Wikipedia</a></li>
<li><a href="https://unric.org/en/artificial-intelligence-what-are-deepfakes/">Artificial intelligence: What are deepfakes?</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#deepfakes`, `#content moderation`, `#app store policy`, `#privacy abuse`

---

<a id="item-16"></a>
## [瑞典 ICA 多家门店遭网络攻击，冷柜被远程调至 50°C](https://x.com/InsiderGeo/status/2117164877701595165) ⭐️ 7.0/10

瑞典连锁超市 ICA 表示，多家门店在夜间遭到网络攻击，冷藏柜和冷冻柜被远程设定为 50°C，可能导致斯约博、托梅利拉等多地门店的大量食品变质。受影响门店当天上午暂停营业，预计当地时间 9 点重新开门，ICA 已就此向顾客致歉。 这是一次典型的网络—物理攻击：数字层面的入侵直接转化为物理损失风险，说明常被视为低优先级的零售制冷系统也可能被用来制造运营中断。此事还与法国、美国近期发生的类似事件形成呼应，表明连锁超市及其第三方制冷供应商已被纳入关键基础设施的攻击面。 报道未披露攻击向量等技术细节，因此尚不清楚是暴露的远程访问接口、弱口令，还是被攻陷的第三方供应商所致；此前的欧洲类似事件曾被追溯到可联网访问的 Danfoss 制冷控制器。ICA 也未说明受影响门店数量和库存损失规模，而食品安全后果取决于冷柜在员工介入前于 50°C 状态下持续了多久。

telegram · zaihuapd · 11月2日 13:52

**背景**: 现代超市制冷属于运营技术（OT）范畴：联网的控制器和远程监控平台让连锁企业及其承包商能够远程调整设定温度、诊断故障。由于这类系统往往位于企业核心 IT 网络之外，且由外部供应商代为管理，即便它们直接关系到食品安全和财务损失，也容易被传统安全体系忽视。自 2026 年 10 月起，法国以及随后比利时、卢森堡、荷兰、瑞典、爱沙尼亚、爱尔兰、葡萄牙等国的超市接连遭遇同类事件，调查人员将可远程访问的 Danfoss 制冷调节器（如 AK-SM800 和 AK-SC355）视为主要攻击面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/2026_French_supermarket_refrigerator_hack">2026 French supermarket refrigerator hack - Wikipedia</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-disrupt-refrigeration-systems-at-european-supermarkets/">Hackers disrupt refrigeration systems at European supermarkets</a></li>
<li><a href="https://secomea.com/blog/ot-security-trends/ot-security-weekly-010-refrigeration-remote-access-risk/">OT Security Weekly #010: Refrigeration attack and SCADA risk</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#IoT security`, `#cyber-physical attacks`, `#critical infrastructure`, `#retail operations`

---

<a id="item-17"></a>
## [阿布扎比与 OpenAI 签署四项协议，推出「机器可读政府」计划](https://thenextweb.com/news/openai-abu-dhabi-deals-machine-readable-government-mubadala) ⭐️ 7.0/10

阿布扎比周一与 OpenAI 签署了四项协议，其中「机器可读政府」（MRG）计划把一批既定的政策和法规转换为 AI 可读的规则，让 AI 协助官员审查许可与执照申请。该计划已在食品进口场景完成试点；其余协议分别涉及穆巴达拉的投资分析合作、G42 旗下 Inception42 为期五年的模型供给协议，以及 ADNOC 成为首家部署 OpenAI Frontier 平台的能源公司。 这是主权级 AI 落地最清晰的现实范本之一：一国政府不只是给公务员采购聊天机器人，而是把监管规则本身变成机器可消费的数据。如果这种「规则即代码」的做法能从试点走向规模化，它可能重塑全球各地政府的许可审批、合规检查与执照发放流程，同时也让 OpenAI 在海湾地区获得深厚的机构级立足点。 官员保留最终决定权，且据报道该试点采用阿联酋本地推理，即模型在本地运行，而非将监管数据传往海外。这些公告在技术细节上较为含糊——被编码规则的覆盖范围、错误率以及审计机制均未披露；而 Inception42 的协议被描述为把 OpenAI 的模型与本地工程和实施服务相结合。

telegram · zaihuapd · 11月2日 15:55

**背景**: 长期以来，政府以 PDF 和自然语言文本发布法规，只有人类才能解读，导致合规流程缓慢且标准不一。「规则即代码」或机器可读监管意在用结构化格式重述法律，使软件（如今越来越多是基于大语言模型的智能体）能够解析，从而自动完成常规核查，而边缘案例仍由人类拍板。另一方面，OpenAI Frontier 是一个用于在大型组织内构建和协调 AI 智能体的平台，ADNOC 计划将其用于能源业务的各个环节。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.utilities-me.com/news/openai-launches-policy-system">OpenAI launches policy system - Utilities Middle East</a></li>
<li><a href="https://www.khaleejtimes.com/uae/abu-dhabi-crown-prince-openai-altman-4-deals-key-sectors">Abu Dhabi Crown Prince meets OpenAI 's Sam Altman... | Khaleej Times</a></li>

</ul>
</details>

**标签**: `#openai`, `#government-ai`, `#ai-policy`, `#regulation`, `#sovereign-ai`

---

<a id="item-18"></a>
## [SGLang v0.5.23 发布：合并 1007 个 PR，新增多款模型与 TPU7x 支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.23) ⭐️ 6.0/10

SGLang 在 GitHub 上发布了 v0.5.23 版本，本次发布汇总了来自 257 位贡献者的 1007 个 PR，新增了对一批 LLM/VLM 与扩散模型的支持，包括 Muse Spark Open、Beam-1.0、MiniMax-M3.1-Flash、MiniCPM-V 4.7、Cosmos3-Nano-Sim、FLUX.3 Image Klein 和 MOSS-Image，并为每款模型提供了 cookbook 文档。该版本还引入了基于 NVIDIA megakernel 与 AMD monokernel 插件的可选低延迟模式、可选启用的 Paged Experts 机制，以及让 SGLang 能够运行在 Google TPU7x 上的 PyTorch 原生插件。 SGLang 是目前使用最广泛的高吞吐 LLM 服务框架之一，因此每次发版都会直接影响大规模推理部署团队，而本次更新带来了切实的性能提升：DeepSeek-V4.1 在 GB300 上高负载时预填充吞吐最高提升 1.5 倍，在 32K 至 64K 提示词下首 token 延迟降低约 28%。可选启用的 Paged Experts 可以说是最具实用价值的变化，它让超出显存容量的大规模 MoE 模型能在单张消费级 GPU 上运行，速度最高可达 CPU offload 的 30 倍；新增的 TPU7x 与 Intel 后端也拓宽了 SGLang 的部署范围。 大部分主打特性都需要手动开启：megakernel/monokernel 低延迟插件让 DeepSeek-V4.1-Flash 在 GB300 上的单用户解码最高提速 44%、在 MI350X 上最高提速 75%；Paged Experts 必须显式启用；在量化 MoE 模型（FP8 与 NVFP4）上挂载 LoRA 适配器则需要新的可选 LoRA 引擎。其他改进还包括：在 H200 上处理 8K 提示词时，DeepSeek-V4.1-Flash、GLM-5.3-Flash 和 gpt-oss 等 MoE 模型的首 token 时间提前 30% 至 58%；以及为运行解码上下文并行的 DeepSeek 风格 MLA 模型提供 HiCache 基于文件的 L3 前缀缓存；安装时需要使用 --prerelease=allow 参数。

github · Fridge003 · 11月2日 22:14

**背景**: SGLang 是一个用于大语言模型高吞吐服务的开源框架，由非营利开源组织托管，并在生产环境中大规模使用——其文档称它每天在超过 40 万块 GPU 上生成数万亿个 token。这类服务框架将推理拆分为两个阶段：预填充（prefill）一次性处理整个输入提示词，解码（decode）则逐 token 生成输出；首 token 延迟（TTFT）衡量的是用户等待输出开始的时间。混合专家（MoE）模型每个 token 只激活部分参数，速度快但显存占用高，因此像 Paged Experts 这样把闲置专家权重移出显存的技术，对于在有限硬件上运行大模型至关重要。视觉语言模型（VLM）在纯文本 LLM 基础上增加了视觉编码器，可以同时理解图像与文本；扩散模型则用于生成图像而非文本——这两类模型都出现在本次新增支持的名单中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.sglang.io/">Welcome to SGLang - SGLang Documentation</a></li>
<li><a href="https://grokipedia.com/page/SGLang">SGLang</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vision-language_model">Vision-language model - Wikipedia</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#SGLang`, `#model serving`, `#release notes`, `#diffusion models`

---

<a id="item-19"></a>
## [LLM 0.37 发布：新增 OpenAI 兼容端点配置命令与多模态嵌入支持](https://simonwillison.net/2026/Nov/2/llm/) ⭐️ 6.0/10

Simon Willison 发布了 LLM 0.37，这个版本汇总了约两个月的功能与修复，新增了 `llm openai endpoint add` 命令，用于配置那些提供 OpenAI 兼容端点的模型，同时支持新的 `gpt-6.1-sol` 和 `gpt-6.1-terra` 模型。该版本还把默认模型切换为价格只有此前默认 `gpt-5.6-luna` 一半的 `gpt-6-luna`，并让 LLM 的嵌入功能能够记录二进制内容的不同 content-type，这是支持 Gemini Embedding 2 这类可嵌入文本、音频、图像和视频的模型所必需的。 新的端点配置命令降低了把 LLM 指向日益壮大的自托管与第三方 OpenAI 兼容推理服务生态的门槛，用户不再局限于固定几家服务商，也不必手动编辑配置文件。更便宜的默认模型和多模态嵌入支持也让这一工具贴合开发者在 2026 年的实际用法：在多个服务商之间灵活切换，并对混合媒体内容而非纯文本做嵌入。 嵌入记录现在会为每条内容保存 content-type，这一点很重要，因为像 Gemini Embedding 2 这样的多模态嵌入模型会把文本、图像、音频、视频和文档映射到同一个向量空间。该版本感谢了 12 位贡献者的修复，其中几乎全部由 AI 辅助完成；Willison 表示，借助 AI 辅助的分诊工具，审阅这批 PR 的负担远低于他的预期，他把这些 PR 视为附带示例的缺陷报告。

rss · Simon Willison · 11月2日 23:49

**背景**: LLM 是 Simon Willison 开发的命令行工具兼 Python 库，用于向大语言模型发送提示词；它把提示词和回复存入 SQLite，并支持用嵌入做语义搜索。嵌入是把内容表示为向量，从而按语义比较不同条目，而 LLM 过去默认嵌入的内容都是文本——随着模型原生支持多模态，这一假设已不再成立。“OpenAI 兼容端点”指的是实现了 OpenAI API 形式的服务，这一通用约定让 LLM 这类工具无需专门适配就能连接本地或第三方的模型服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://llm.datasette.io/en/stable/embeddings/index.html">Embeddings - LLM</a></li>
<li><a href="https://deepmind.google/models/gemini/embedding/">Gemini Embedding 2 — Google DeepMind</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-embedding-2/">Gemini Embedding 2: Our first natively multimodal embedding model</a></li>

</ul>
</details>

**标签**: `#llm-cli`, `#release-notes`, `#openai-compatible-apis`, `#embeddings`, `#developer-tools`

---

<a id="item-20"></a>
## [人口普查局 AI 采用图表重制，凸显“超级智能”行政令冲突](https://simonwillison.net/2026/Nov/2/census-bureau-super-intelligence/) ⭐️ 6.0/10

Simon Willison 使用 2026 年 10 月 22 日发布的美国人口普查局《商业趋势与展望调查》数据重制了 AI 采用率图表，显示员工数 250 人以上的企业采用率达到 40.7%。他还指出，人口普查局与 2026 年 9 月 29 日签署的第 14434 号“超级智能”行政令发生了冲突。 这一事件表明，官方调查中一个措辞变化就可能打断被广泛使用的时间序列，迫使分析人员将变化前后的数据分开处理。它也说明，把“人工智能”改称为“超级智能”的行政令可能波及日常的联邦数据收集与公共统计。 BTOS 每两周调查 120 万家企业中的 20 万家，且同一小组企业每十二周才回复一次；2025 年 11 月，调查问题从“用于生产商品或服务”的 AI 扩大为“任何业务职能”中的 AI，因此前后两个序列不可直接比较。Willison 采用六次调查的移动平均，并且没有对断点做衔接；第 14434 号行政令则要求联邦机构把“Artificial Intelligence”和“AI”替换为“Super Intelligence”和“SI”。

rss · Simon Willison · 11月2日 13:31

**背景**: 《商业趋势与展望调查》是美国人口普查局每两周开展一次的调查，已成为衡量美国雇主企业 AI 采用情况的重要数据来源。第 14434 号行政令《开启超级智能时代》于 2026 年 9 月 29 日签署，要求联邦机构将术语从 AI 改为 SI。Simon Willison 是一位开发者和写作者，以使用大语言模型工具分析公共数据的实践实验而知名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.federalregister.gov/documents/2026/10/02/2026-20321/inaugurating-the-era-of-super-intelligence">Federal Register :: Inaugurating the Era of Super Intelligence</a></li>
<li><a href="https://cofabrix.com/blog/super-intelligence-si-explained">Is AI Now Called Super Intelligence ? The SI Order ... | CoFabrix</a></li>
<li><a href="https://www.federalreserve.gov/econres/notes/feds-notes/monitoring-ai-adoption-in-the-u-s-economy-20260403.html">The Fed - Monitoring AI Adoption in the US Economy</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#AI adoption`, `#data analysis`, `#government statistics`, `#LLM tooling`

---

<a id="item-21"></a>
## [研究者求助：无法复现已发表机器学习基线的结果该如何呈现](https://www.reddit.com/r/MachineLearning/comments/1xm64of/couldnt_reproduce_a_published_papers_numbers_with/) ⭐️ 6.0/10

一位研究者在 r/MachineLearning 上发帖称，自己在两个基准上无法复现已发表基线方法的结果，尽管使用了作者原封未动的开源代码、论文中列出的精确超参数以及三个随机种子，并在数月间重复复现了四次。在其余基准上其结果与原文在噪声范围内一致；该研究者询问应如何同时呈现已发表数字与自己的复现数字，既不显得能力不足，也不显得是在攻击原文。 可复现性一直是机器学习研究的薄弱环节，而作者如何报告与自己复现不一致的基线数字，直接影响审稿人和读者对论文所宣称改进幅度的解读。关于如何记录复现失败的实用规范——放在主表还是附录、是否先通知原作者——在很大程度上决定了这些差异能否被公开暴露出来。 该研究者目前掌握的证据包括：未改动的作者代码、论文自带的超参数、使用三个种子的多种子实验协议、其余基准结果吻合这一合理性检验，以及相隔数月进行的四次独立复现尝试。悬而未决的问题属于流程与表达层面：投稿前是否应联系原作者或在 GitHub 上提 issue，以及是否应在论文中说明这一联系。

reddit · r/MachineLearning · /u/InsectActive95 · 11月2日 19:00

**背景**: 在机器学习论文中，基线是指用来与新方法对比的已发表现有方法，结果通常在标准化基准数据集上报告。复现是指使用原作者公开的代码和超参数重新运行该基线，但由于硬件差异、库版本、数据预处理或随机种子等因素，结果仍可能不同。审稿人往往将已发表的数字视为权威，因此报告中复现值更低的投稿容易被理解为实现有误，而非真实存在的差异。

**标签**: `#reproducibility`, `#machine-learning`, `#peer-review`, `#benchmarking`, `#research-practice`

---

<a id="item-22"></a>
## [Anthropic 更新使用政策，禁止转售 Claude 访问权限](https://www.anthropic.com/legal/aup) ⭐️ 6.0/10

Anthropic 更新了其使用政策（Usage Policy），新版本将于 2026 年 11 月 12 日生效，这是继 2025 年 9 月 15 日之后的再次修订，在「Do Not Abuse Our Platform」一节中新增了两条禁令。新增条款禁止通过未经授权的方式转售或代理 Claude 访问，包括经消费级订阅转发请求、虚假陈述所使用的产品或客户端，同时也禁止使用盗用、欺诈或未获授权的付款方式来逃避付费。 这一变动直接针对 Claude 访问权限转售、代理服务以及拼车共享订阅等灰色市场行为——这些模式本质上是把廉价的消费级订阅套餐套利成类似 API 的调用能力。政策更新让 Anthropic 有更明确的依据来封停账号、清理中间商，从而影响那些通过第三方而非直接从 Anthropic 购买 Claude 访问权限的开发者和小型团队。 该政策并不禁止合法的 API 使用或企业协议，其针对的是未经授权的转售、从消费级订阅转发请求、虚假陈述所用客户端或产品，以及支付欺诈行为。执行方式由 Anthropic 自行裁量，包括暂停账号；2026 年 11 月 12 日的生效日期为现有用户留出了迁移到官方渠道的窗口期。

telegram · zaihuapd · 11月2日 05:43

**背景**: Anthropic 通过多种渠道提供 Claude：Claude Pro 等消费级订阅、按 token 计费的付费开发者 API，以及企业协议。由于订阅价格和可用性因地区而异，围绕转售席位、共享账号和通过代理转发流量形成了一个灰色市场——所谓代理，即把请求中转至 Anthropic 服务器以隐藏用户真实位置或绕过地区封锁的第三方服务。这类做法违背了按席位授权的原则，也让 Anthropic 面临滥用、拒付欺诈以及无法掌握模型使用者身份的风险，因此使用政策越来越多地明确写入禁止转售和支付欺诈的条款。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kindproxy.com/use-cases/claude/">Claude Proxy — Anthropic API & Developer Access | KindProxy</a></li>
<li><a href="https://www.quarkip.com/blog/guides/3856">Claude Proxy | Unblock IP Bans & Use Claude Stably with QuarkIP</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#Claude`, `#usage policy`, `#AI regulation`, `#API resale`

---

<a id="item-23"></a>
## [DeepSeek Harness 团队提出 Super-agent 架构：常驻 Router 搭配上下文隔离 Worker](https://t.me/zaihuapd/44861) ⭐️ 6.0/10

DeepSeek Harness 团队提出了一种“Super-agent”架构：由常驻的 Router 层统一负责对外交互与任务分派，多个上下文相互隔离的 Worker 并发执行任务，从而避免单会话阻塞和多任务之间的上下文混乱。在该团队内部原型中，任务完成耗时的中位数（p50）为 12.4 分钟，p95 为 15.7 分钟。 该设计直指当前编程与通用智能体的核心痛点：单个会话一次只能处理一件事，长任务会阻塞其他工作，并行任务又会污染共享上下文。把“派活”与“干活”分离，与 Claude Code 类智能体产品及托管式 Agent 服务探索的方向一致，也表明 DeepSeek 正从基础模型竞争延伸到智能体编排基础设施。 这些数据来自内部原型的自测，统计的是端到端任务完成耗时，而不是单次调用或单 token 的延迟；p50 与 p95 之间差距较小，说明运行相对稳定。团队强调该方案目前仍处于架构思路探讨阶段，因此本次并未随附完整实现、基准测试方法或成本对比。

telegram · zaihuapd · 11月2日 17:17

**背景**: DeepSeek Harness 是 DeepSeek（开发 DeepSeek 系列模型的中国公司）内部专注于智能体的团队，主攻“harness”层，即环绕大模型的编排与控制工程，团队将其概括为“Model + Harness = Agent”。在 LLM 智能体系统中，Router 是接收用户请求并决定子任务分派去向的组件，Worker 则是真正调用工具和模型的执行单元；所谓“上下文隔离”，是指每个 Worker 维护自己的对话历史，使并行任务互不干扰。p50 与 p95 是延迟分位数指标：p50 表示中位数任务耗时，p95 表示 95% 的任务在该时间内完成，工程上用它们衡量尾部延迟，而不仅仅看平均值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/DeepSeek_Harness">DeepSeek Harness - 维基百科，自由的百科全书</a></li>
<li><a href="https://baike.baidu.com/item/Harness/67826060">Harness（DeepSeek内部团队）_百度百科</a></li>
<li><a href="https://redreamality.com/cn/blog/deepseek-super-agent-router-worker-architecture/">DeepSeek Super-agent 架构：Router、Worker 与事件驱动 | Redreamali...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#multi-agent systems`, `#DeepSeek`, `#task orchestration`, `#LLM infrastructure`

---