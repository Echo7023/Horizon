---
layout: default
title: "Horizon Summary: 2026-10-26 (EN)"
date: 2026-10-26
lang: en
---

> From 28 items, 15 important content pieces were selected

---

1. [PHP rushes out emergency patches for two critical unauth RCE flaws](#item-1) ⭐️ 9.0/10
2. [10-Year-Old Inception CNN Beats Frontier LLMs at Skin Cancer Diagnosis](#item-2) ⭐️ 8.0/10
3. [Dan Luu Argues Developers Should Build More Ambitious Software](#item-3) ⭐️ 8.0/10
4. [Cerebras Serves Trillion-Parameter Models on Wafer-Scale Hardware](#item-4) ⭐️ 8.0/10
5. [memt-1.0 internalizes agent memory with gated DeltaNet-2, cutting storage 66x](#item-5) ⭐️ 7.0/10
6. [Sogou Input Method OPPO edition flagged as risky by Google Play Protect](#item-6) ⭐️ 7.0/10
7. [Apple to Unveil First Touchscreen MacBook Pro With OLED on Wednesday](#item-7) ⭐️ 7.0/10
8. [Speaker Urges Resistance to Internet Censorship Ahead of FOSDEM Talk](#item-8) ⭐️ 6.0/10
9. [Show HN Chart Places Employees Inside S&P 500 Market-Cap Bubbles](#item-9) ⭐️ 6.0/10
10. [fheroes2, an open-source Heroes of Might and Magic II engine, draws Hacker News nostalgia](#item-10) ⭐️ 6.0/10
11. [Nanbeige Releases Nanbeige4.3-33B, an Apache 2.0 Teacher Model for Smaller Agents](#item-11) ⭐️ 6.0/10
12. [China's MIIT Drafts Mandatory Standard for Blue-Green ADS Marker Lights](#item-12) ⭐️ 6.0/10
13. [GPU Rental Prices Surge Across the Board, Even the Aging A100](#item-13) ⭐️ 6.0/10
14. [Tesla to launch in-house AI maps with FSD v15](#item-14) ⭐️ 6.0/10
15. [GEEKCON Shanghai drone-hacking challenge halted after vendor police report](#item-15) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [PHP rushes out emergency patches for two critical unauth RCE flaws](https://t.me/zaihuapd/44678) ⭐️ 9.0/10

The PHP team released emergency security updates — PHP 8.5.12, 8.4.27, 8.3.36 and 8.2.35 — fixing two vulnerabilities that allow unauthenticated attackers to execute arbitrary code remotely, both rated CVSS 4.0 9.2. Every PHP deployment that handles web requests is affected, including PHP-FPM, Apache's mod_php, php-cgi, FrankenPHP and LiteSpeed. PHP underpins a huge share of the web — WordPress, Drupal, Laravel and countless bespoke apps — so an unauthenticated RCE in the runtime itself is a paradigm-level security event: patching is needed even if the application code is flawless. With mod_php confirmed exploitable before application code even runs, hosting providers, sysadmins and anyone running PHP behind a web server must upgrade immediately. mod_php carries the highest risk, with verification showing exploitation can occur before any site application code executes, meaning a vulnerable module alone is enough for compromise. The fixes span four supported branches, so admins must confirm their exact minor version rather than assume a recent install is safe.

telegram · zaihuapd · Oct 25, 02:42

**Background**: PHP is a server-side scripting language that most commonly runs behind a web server through an SAPI (Server API) layer. PHP-FPM is a FastCGI process manager that keeps a pool of worker processes and hands requests off from the web server; mod_php instead embeds the PHP interpreter directly into Apache; php-cgi is the older CGI-based approach; FrankenPHP is a newer app server built on Caddy that embeds PHP in a Go process and needs no PHP-FPM. Because these layers sit in front of application code, a flaw in the runtime or SAPI can be triggered by crafted requests without any valid credentials.

<details><summary>References</summary>
<ul>
<li><a href="https://www.php.net/manual/en/install.fpm.php">PHP: FastCGI Process Manager (FPM) - Manual</a></li>
<li><a href="https://www.zend.com/blog/apache-phpfpm-modphp">Configuring Apache HTTPD With PHP - FPM and mod _ php | Zend</a></li>
<li><a href="https://frankenphp.dev/">FrankenPHP : the modern PHP app server</a></li>

</ul>
</details>

**Tags**: `#security`, `#php`, `#vulnerability`, `#remote-code-execution`, `#patching`

---

<a id="item-2"></a>
## [10-Year-Old Inception CNN Beats Frontier LLMs at Skin Cancer Diagnosis](https://lynchlab.net/llm-skin-cancer) ⭐️ 8.0/10

Dermatologist Dr Magnus Lynch tested GPT-6 Astra and Claude Fable 5.1 against a fine-tuned Inception v3 on 200 biopsy-proven skin lesions, and the decade-old CNN named the correct diagnosis for 125 lesions (62%) versus roughly 42% for the frontier LLMs. The CNN was trained on 68,011 dermoscopic and clinical images from the ISIC Archive on a single H100 GPU, with all test lesions and any images of the same lesion or patient removed beforehand. The result challenges the assumption that ever-larger general-purpose models will subsume specialized systems, and it suggests that for narrow, high-stakes tasks like medical imaging a small purpose-built classifier can still be far more accurate and far cheaper to run. It also raises pointed questions about how multimodal LLM benchmarks are constructed and what claims of clinical competence actually mean. The headline comparison is a top-1 diagnostic accuracy on a 200-lesion test set, a small sample that leaves wide confidence intervals, and commenters note the model was carefully isolated from test data and threshold selection — fair practice, but also arguably a benchmark-shaped setup. Critics also point out the architecture is ten years old but the training is recent, so the title slightly overstates the 'old model wins' framing.

hackernews · sungam · Oct 25, 17:15 · [Discussion](https://news.ycombinator.com/item?id=50233779)

**Background**: Inception, originally introduced by Google researchers in 2014 as GoogLeNet, is a family of convolutional neural networks for computer vision whose Inception modules run filters of several sizes in parallel to extract features efficiently at relatively low compute cost. Fine-tuning means taking such a network pretrained on ordinary photographs and continuing to train all its layers on a domain-specific dataset, here dermoscopic images from the ISIC Archive, a large public collection of skin lesion images used widely in dermatology AI research. Frontier LLMs are general-purpose multimodal models trained on broad internet-scale data, so the comparison is between a narrow specialist and a generalist rather than between two versions of the same thing.

<details><summary>References</summary>
<ul>
<li><a href="https://lynchlab.net/llm-skin-cancer">A 10-year-old CNN outperforms frontier LLMs for skin cancer ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Inception_(deep_learning_architecture)">Inception (deep learning architecture) - Wikipedia</a></li>
<li><a href="https://explainx.ai/blog/cnn-beats-gpt-6-astra-claude-fable-5-1-skin-cancer-diagnosis-lynch-2026">CNN vs GPT-6 Astra vs Fable 5.1: Skin Cancer, 62% vs 42% ...</a></li>

</ul>
</details>

**Discussion**: Commenters on Hacker News were largely unsurprised that a dedicated classifier beats a general model, with several arguing the real lesson is to use LLMs to cheaply build narrow, highly accurate models rather than deploy LLMs directly for scaled applications. Others pushed back on the framing, calling the setup 'benchmaxxing' and noting the architecture is old but the training recent, while a further group argued the comparison misses the LLM's real potential — incorporating clinical notes, asking follow-up questions, and handling messy out-of-distribution images.

**Tags**: `#medical-ai`, `#LLMs`, `#CNNs`, `#benchmarking`, `#model-specialization`

---

<a id="item-3"></a>
## [Dan Luu Argues Developers Should Build More Ambitious Software](https://danluu.com/ambitious/) ⭐️ 8.0/10

Dan Luu published an essay titled "We should be more ambitious with the software we build," arguing that developers should aim at genuinely ambitious work instead of settling for incremental or locally optimized improvements. The post reached the front page of Hacker News, where it accumulated roughly 707 points and 645 comments. The essay and the discussion around it reflect a widening debate about whether AI-assisted coding is producing shallow, locally optimized work rather than substantive engineering, a question that affects how teams evaluate productivity gains from LLMs. It also pushes back on a common industry pattern of treating narrow performance wins — a faster database or regex engine — as the primary measure of progress. The piece is opinion and commentary rather than a technical release or benchmark, so its claims are argumentative by nature, and much of its value came from the community responses it provoked. Commenters split between those who see AI code generation as a way to finally build long-deferred side projects and those who report LLM-written code that is overfit to the tested use case, hard to generalize performance-wise, and difficult to maintain.

hackernews · ltratt · Oct 24, 21:47 · [Discussion](https://news.ycombinator.com/item?id=50225695)

**Background**: Dan Luu is a software engineer and long-time blogger known for empirically grounded essays on software performance, engineering productivity research, and the gap between how the industry talks about quality and how it actually builds systems. Hacker News is a technology link-sharing forum run by Y Combinator, where submissions are ranked by upvotes and points, and comment threads frequently become the substantive debate around a post. The community's "faster horse" reference alludes to the apocryphal Henry Ford line that if he had asked customers what they wanted, they would have said faster horses, used here to argue that optimizing an existing tool is a substitute for rethinking the problem.

**Discussion**: Sentiment was broadly engaged but divided. Several commenters argued that AI-assisted coding tends to produce messy, overfit code that neither generalizes in performance nor survives future changes, while others countered that the real gain is ambition — one developer described using AI to build an e-ink SDK and app ecosystem for the Kobo reader that they had long lacked time for. Another thread contended that "a faster Postgres/regex" is precisely the faster-horse fallacy, and one commenter noted that outside the tech bubble real-world software quality — such as the firmware on a consumer heat pump — remains poor.

**Tags**: `#software-engineering`, `#essay`, `#developer-culture`, `#AI-code-generation`, `#hackernews-discussion`

---

<a id="item-4"></a>
## [Cerebras Serves Trillion-Parameter Models on Wafer-Scale Hardware](https://www.cerebras.ai/blog/how-we-deploy-trillion-parameter-frontier-models-on-cerebras) ⭐️ 8.0/10

Cerebras published a technical blog post detailing how it deploys and serves trillion-parameter frontier models on its wafer-scale hardware, and the post drew a 337-point, 119-comment Hacker News discussion. The company frames the achievement as a demonstration that its CS-3-class systems can handle the largest current model class for inference rather than only smaller open models. Serving trillion-parameter models is a systems-level challenge that normally requires large multi-GPU clusters with complex tensor and pipeline parallelism, so doing it on a single wafer-scale engine is a meaningful infrastructure milestone. It also matters commercially: if Cerebras can deliver frontier-class quality at much higher token throughput, it becomes a credible alternative to GPU-based inference providers for latency-sensitive workloads. Cerebras's advantage comes from the WSE-3 generation chip, which packs roughly 4 trillion transistors and 900,000 AI-optimized cores on a single wafer with on-chip memory and high internal bandwidth, avoiding the interconnect bottlenecks of clustered GPUs. The main caveat raised by commenters is model freshness and quality: the models most users can actually access are smaller open ones, and at least one tester reported very high tokens-per-second but frequent wrong answers.

hackernews · gmays · Oct 25, 01:33 · [Discussion](https://news.ycombinator.com/item?id=50227356)

**Background**: Wafer-scale integration (WSI) means building one giant chip from an entire silicon wafer instead of dicing it into many small chips, trading manufacturing difficulty for enormous on-chip bandwidth and memory. Cerebras is the best-known commercial practitioner, selling its WSE chips inside CS-3 systems as a replacement for racks of GPUs. Trillion-parameter models are the largest class of large language models, with parameter counts around or above 1e12, and serving them requires holding enormous weights in fast memory while keeping compute units busy.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Wafer-scale_integration">Wafer-scale integration</a></li>
<li><a href="https://www.cerebras.ai/chip">Cerebras WSE-3 Turbo | Wafer-Scale AI Chip</a></li>

</ul>
</details>

**Discussion**: Sentiment on Hacker News was mixed and notably critical: some argued Cerebras lags frontier labs by roughly 6-9 months but will still offer near-frontier models at far lower cost and much higher speed, while others countered that limited wafer supply means it cannot meet demand and that accessible models like GPT-OSS-120B are fast yet error-prone. One commenter with professional experience praised the technology as remarkable but called the team inadequate, and another raised technical questions about how data flows across the chip's 2D mesh of processing elements.

**Tags**: `#cerebras`, `#wafer-scale`, `#llm-inference`, `#ai-infrastructure`, `#model-serving`

---

<a id="item-5"></a>
## [memt-1.0 internalizes agent memory with gated DeltaNet-2, cutting storage 66x](https://www.reddit.com/r/MachineLearning/comments/1xeu0ht/memt10_architecture_breakdown_gated_deltanet2/) ⭐️ 7.0/10

A technical breakdown posted on r/MachineLearning details memt-1.0's memory-native architecture, which uses gated DeltaNet-2 and a mixture-of-storage (MoS) layer to internalize agent memory into model computation instead of relying on append-only prompts or external RAG pipelines. At a 128k-token history length, memt-1.0-nano reportedly delivers about 1.86x end-to-end inference speedup and a 66x reduction in persistent storage compared with a full-context KV-cache setup. Long-horizon agents increasingly suffer from context bloat and KV-cache memory bottlenecks, so architecture-level memory internalization could offer a more scalable alternative to prompt stacking and external retrieval. If the reported gains generalize, it would affect teams building agent frameworks, long-context inference systems, and memory layers. The post says memt-1.0 uses gated DeltaNet-2 with a stable token-level memory update within each turn, plus a mixture-of-storage layer to scale capacity; its two-stage pipeline of continued pre-training and post-training over 34B tokens reportedly keeps general reasoning competitive with parametric-memory baselines. These figures come from a single technical breakdown and apply to the memt-1.0-nano variant at 128k context, so independent verification is still needed.

reddit · r/MachineLearning · /u/Mrs-Grumpy23 · Oct 25, 05:31

**Background**: Agent memory systems typically either keep past interactions in the prompt/context window, which grows the KV cache, or retrieve external documents through RAG, which adds latency and pipeline complexity. Parametric memory instead encodes information into model weights or recurrent states; linear-attention architectures such as DeltaNet maintain a compact recurrent state rather than a full attention cache. Gated DeltaNet-2 extends this line with separate erase and write gates for finer control over what the memory retains, while mixture-of-storage is memt-1.0's approach to scaling that native memory capacity.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2610.26825">MemT-1.0: Towards Memory -Native Evolution</a></li>
<li><a href="https://www.emergentmind.com/topics/gated-deltanet-2-architecture">Gated DeltaNet - 2 : Advanced Memory Architecture</a></li>
<li><a href="https://arxiv.org/abs/2605.22791">Gated DeltaNet - 2 : Decoupling Erase and Write in Linear Attention</a></li>

</ul>
</details>

**Tags**: `#agent-memory`, `#efficient-inference`, `#DeltaNet`, `#KV-cache`, `#model-architecture`

---

<a id="item-6"></a>
## [Sogou Input Method OPPO edition flagged as risky by Google Play Protect](https://t.me/zaihuapd/44689) ⭐️ 7.0/10

Users of ColorOS devices reported that the OPPO-customized build of Sogou Input Method was flagged by Google Play Protect as a harmful app; the security component automatically revoked its sensitive permissions, disabled the app, and displayed a warning that it may snoop on SMS messages, photos, recordings, and call logs. OPPO customer support reportedly responded that the issue is being worked on and suggested users could temporarily turn off Play Protect in the meantime. The incident puts a spotlight on the trust chain between preinstalled vendor apps and Google's security services, since a widely used input method shipped through a carrier/OEM channel was classified as harmful on users' own devices. Telling users to disable Play Protect is a contentious remedy, because it weakens protection against genuinely malicious apps across the whole system, and the case affects every ColorOS user relying on the bundled keyboard. Play Protect did not merely show a warning: it stripped the app's sensitive permissions and deactivated it, so users may find the keyboard disabled until the build is updated. The specific trigger is unclear, but the listed permissions (SMS, photos, microphone, call logs) go far beyond what a keyboard needs to function, and the dispute is between a third-party app modified by OPPO and Google's automated scanning rather than a Play Store listing.

telegram · zaihuapd · Oct 25, 09:59

**Background**: Google Play Protect is Android's built-in malware scanning service, which checks apps on the device — including sideloaded and preinstalled ones — and can warn users, revoke permissions, or disable an app it deems harmful. Input methods are especially privacy-sensitive because they see everything typed on a phone and, on Android, often request broad permissions; security researchers have repeatedly criticized Chinese input methods over data collection. OEM-customized builds of popular apps are common in China, and because they are distributed outside the Play Store, they do not go through Google's normal review process but can still be flagged by on-device scanning.

<details><summary>References</summary>
<ul>
<li><a href="https://support.google.com/android/answer/2812853?hl=zh-Hans">利 用 Google Play 保 护 机 制 保 障 应 用 的安全性和数据的私密性 - Android...</a></li>
<li><a href="https://www.getdeng.net/blog/input-method-risk.html">getdeng.net/blog/input-method-risk.html</a></li>
<li><a href="http://www.jiguo.com/article/article/99975.html">大意了！ “窃取”聊天记 录 真凶竟是手机 输 入 法 ，会这四招防 隐 私 泄露-极果</a></li>

</ul>
</details>

**Tags**: `#Android`, `#privacy`, `#security`, `#Google Play Protect`, `#Sogou`

---

<a id="item-7"></a>
## [Apple to Unveil First Touchscreen MacBook Pro With OLED on Wednesday](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 7.0/10

Apple is reportedly set to unveil its first touchscreen MacBook Pro on Wednesday, bringing touch input and OLED displays to the Mac for the first time, along with a Dynamic Island, in both 14-inch and 16-inch versions. Pricing is expected to be higher than the current $2,499 starting price. This reverses a long-held Apple position — executives repeatedly rejected touchscreen laptops on ergonomic grounds — making it one of the most significant changes to the Mac's input model in years. It signals a more pragmatic Apple willing to revise its own doctrine rather than insisting the industry follow it, and could pressure rival Windows laptop makers who already ship touch and OLED panels. According to the report, touch will be positioned as a supplement to the keyboard and trackpad rather than a replacement, and the pivot is framed as being driven more by revenue and marketing considerations than by a technical breakthrough. The claim originates from a Bloomberg report and has not been confirmed by Apple, so specifications and pricing remain unverified.

telegram · zaihuapd · Oct 25, 14:25

**Background**: The Dynamic Island is a software-driven UI element Apple introduced with the iPhone 14 Pro in 2022; it expands and changes shape around the camera cutout to show notifications, media playback and live activities, blurring the line between hardware and software. OLED panels emit light per pixel, delivering true blacks and high contrast, whereas current MacBook Pro models use mini-LED backlit LCD displays that get very bright but cannot switch individual pixels off. Apple had for years argued that reaching up to touch a vertical laptop screen is ergonomically poor, which is why the Mac has remained keyboard-and-trackpad only.

<details><summary>References</summary>
<ul>
<li><a href="https://baike.baidu.com/item/灵动岛/61968459">灵动岛（苹果公司应用于手机上的交互UI）_百度百科</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/563292350">灵动岛是什么？灵动岛功能详细解析 - 知乎</a></li>
<li><a href="https://post.smzdm.com/p/aomon7z9/">笔 记 本 屏 幕 选 OLED 还是 LCD ...</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#MacBook Pro`, `#touchscreen`, `#OLED`, `#hardware`

---

<a id="item-8"></a>
## [Speaker Urges Resistance to Internet Censorship Ahead of FOSDEM Talk](https://talkweb.eu/openweb/4558/) ⭐️ 6.0/10

A speaker published a rallying post titled "I refuse to accept a censored Internet. Join Me at FOSDEM 27," calling on readers to push back against internet censorship and promoting an upcoming talk at FOSDEM. The post is largely a pitch for the session rather than a technical release, but it drew a substantial Hacker News thread (255 points, 122 comments) debating whether an uncensored internet is even achievable. The piece lands amid growing concern that control over the internet is shifting from open protocols to a handful of corporations and infrastructure providers, which makes the open-web debate concrete rather than abstract. It also highlights a widening disagreement inside the free-software community over where content moderation ends and censorship begins, and which countries get named when censorship is discussed. The article itself contains little technical substance, consisting mainly of the talk pitch, so most of the value lies in the linked discussion. Commenters note that any "uncensored" network still runs over infrastructure controlled by corporations and states, meaning encrypted overlays can be switched off at the routing or provider level.

hackernews · Tomte · Oct 25, 17:30 · [Discussion](https://news.ycombinator.com/item?id=50233929)

**Background**: FOSDEM (Free and Open source Software Developers' European Meeting) is an annual, non-commercial, volunteer-run conference held in Brussels each late winter, and it is widely regarded as Europe's largest gathering of open-source developers. The "open web" refers to the part of the internet built on shared, permissionless standards such as HTTP, HTML and RSS, in contrast to closed platforms that gatekeep content. Distinguishing content moderation (platform or community enforcement of rules) from censorship (typically state-driven suppression of speech) is a long-running debate in online-community governance.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/FOSDEM">FOSDEM - Wikipedia</a></li>
<li><a href="https://www.drupal.org/association/open-web-manifesto">Open Web Manifesto | Drupal.org</a></li>
<li><a href="https://www.conectys.com/blog/posts/content-moderation-vs-censorship-how-to-tell-the-difference/page/11/">Content Moderation vs Censorship | Blog | Conectys | BPO</a></li>

</ul>
</details>

**Discussion**: Sentiment was thoughtful but skeptical: several commenters argued no truly uncensored internet exists, since it would still be routed through censored infrastructure and corporations can simply pay providers to comply. Others drew a distinction between moderation and censorship while conceding that any online discussion requires some form of moderation, and one commenter contended that most users now accept censorship when it aligns with their politics. A separate thread of criticism accused FOSDEM-style venues of only naming Russia, China and Iran while ignoring censorship closer to home, and one commenter simply praised FOSDEM as a worthwhile, low-sales-pitch conference.

**Tags**: `#internet-censorship`, `#fosdem`, `#content-moderation`, `#privacy`, `#open-web`

---

<a id="item-9"></a>
## [Show HN Chart Places Employees Inside S&P 500 Market-Cap Bubbles](https://bigwhalehunting.com/workforce/) ⭐️ 6.0/10

A Show HN project on bigwhalehunting.com visualizes every S&P 500 company as a bubble sized by market capitalization, with one stick figure drawn inside for each 10,000 employees. The author highlights the contrast between Nvidia, worth about $5.2 trillion with only 42,000 employees (roughly $124 million of market cap per employee), and Accenture, which employs 814,000 people for a $146 billion valuation. The chart turns an abstract valuation metric into an intuitive picture of how differently modern companies convert people into market value, contrasting asset-light AI and software businesses with labor-intensive services firms. It also exposes how shaky the underlying headcount data is, which matters for anyone using per-employee metrics to judge productivity or efficiency. Each stick figure represents 10,000 employees and the visualization is zoomable so users can inspect individual companies. Headcount figures come from company disclosures, which typically count only direct employees and therefore understate workforces at firms relying on contractors, seasonal staff, or franchisees.

hackernews · vfxGer · Oct 25, 15:05 · [Discussion](https://news.ycombinator.com/item?id=50232312)

**Background**: Market capitalization is a company's share price multiplied by its shares outstanding, and the S&P 500 weights constituents by that value, so the largest companies dominate the index. Dividing market cap by headcount yields a rough measure of how much the market values each employee, a metric often used to illustrate the economics of intangible-heavy businesses. Companies report their employee counts in annual 10-K filings, and since 2020 the SEC has also required disclosure of human capital resources, but the definitions used vary widely across firms.

<details><summary>References</summary>
<ul>
<li><a href="https://pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/Employee.html">Employee Metrics by Sector (US) - New York University</a></li>
<li><a href="https://www.sec.gov/files/spotlight/iac/20230921-recommendation-regarding-hcm.pdf">Human Capital Management Disclosure - SEC.gov</a></li>
<li><a href="https://note.com/manndoru/n/n04aabd88adcd?hl=en">How to use 'Market Capitalization per Employee' in corporate ...</a></li>

</ul>
</details>

**Discussion**: Commenters largely questioned the data rather than the visualization: pointing out that part-time, seasonal, and contract workers (as at Amazon and Walmart) distort headcounts, that franchise models make comparisons inconsistent (Marriott's 414,000 listed employees versus McDonald's corporate-only count), and that sector classifications look wrong, such as Alphabet and Meta under information technology, Tesla under industrials, and NetApp included while similarly sized peers are not. One commenter said the tiny stick figures made them feel sympathy for companies whose bubbles were mostly people.

**Tags**: `#data-visualization`, `#finance`, `#S&P 500`, `#Show HN`, `#workforce-analytics`

---

<a id="item-10"></a>
## [fheroes2, an open-source Heroes of Might and Magic II engine, draws Hacker News nostalgia](https://github.com/ihhub/fheroes2) ⭐️ 6.0/10

The fheroes2 project, an open-source reimplementation of the Heroes of Might and Magic II game engine hosted on GitHub under the ihhub organization, reached the Hacker News front page with roughly 184 points and 65 comments. The thread contained no announcement of a new release; instead it became a conversation about the project itself, sibling efforts like VCMI, and whether the original game still holds up today. Engine reimplementations like fheroes2 keep decades-old commercial games playable on modern operating systems and hardware long after the original binaries and publishers have moved on. It also shows that the retro strategy audience is still active and technically engaged, even though the discussion stayed conversational rather than diving into engine architecture. fheroes2 is a from-scratch engine that still requires the original game's data files to play, and its development guide notes that a downloadable demo of the original game is the minimum required for development builds. The project targets multiple platforms including Windows (Visual Studio 2019 project files are provided) as well as macOS and Linux, and it is a separate effort from VCMI, which does the same job for Heroes of Might and Magic III.

hackernews · tosh · Oct 25, 11:09 · [Discussion](https://news.ycombinator.com/item?id=50230384)

**Background**: Heroes of Might and Magic II is a 1996 turn-based strategy game from New World Computing in which players build towns, recruit fantasy creatures, and fight tactical hex-grid battles; the series is now owned by Ubisoft. An 'engine recreation' means developers rewrite the game's code from scratch so the original assets can run natively on modern machines, fixing compatibility, resolution, and bug problems that the shipped executable cannot handle. Such projects typically require players to own the original game, so they function as preservation and modernization efforts rather than free redistributions.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ihhub/fheroes2">GitHub - ihhub/fheroes2: fheroes2 is a recreation of Heroes ...</a></li>
<li><a href="https://ihhub.github.io/fheroes2/DEVELOPMENT.html">fheroes2 build and contribution guide | fheroes2</a></li>
<li><a href="https://github.com/vcmi/vcmi">vcmi / vcmi : Open-source engine for Heroes of Might and Magic III ...</a></li>

</ul>
</details>

**Discussion**: Commenters were mostly nostalgic: one shared an experiment wiring Claude Code to play Heroes of Might and Magic III and reported the model plays badly and very slowly, another pointed to VCMI as the Linux-friendly Heroes III engine, and a third recommended the newer Heroes of Might and Magic: Olden Era. A more skeptical voice argued that childhood favorites like HoMM often feel unbearable to replay as an adult, while one fan wished for a new entry blending HoMM2's art style with HoMM3's mechanics.

**Tags**: `#game-engine`, `#open-source`, `#reverse-engineering`, `#game-preservation`, `#retro-gaming`

---

<a id="item-11"></a>
## [Nanbeige Releases Nanbeige4.3-33B, an Apache 2.0 Teacher Model for Smaller Agents](https://www.reddit.com/r/MachineLearning/comments/1xf6x35/nanbeige_releases_nanbeige4333b_an_apache_20/) ⭐️ 6.0/10

Nanbeige released Nanbeige4.3-33B under the Apache 2.0 license with a 512K-token context window, positioning it as the teacher model for its planned smaller agents, including an upcoming 3B model. The team self-reports 80.9 on Terminal-Bench 2.1 versus 73.0 for Qwen3.8-27B, evaluated with the same harness and inference settings within each benchmark. A permissively licensed 33B teacher model aimed at agentic tool use gives teams a potential distillation source for small, cheap-to-serve agents, a direction much of the open-weights community is pursuing as inference cost dominates deployment budgets. The 512K context window and Apache 2.0 terms also make it usable in commercial products without the restrictions common to some open-weight licenses. The model does not win everywhere: on SWE-Bench Pro it reports 60.3 against 61.7 for the Qwen comparison, and all figures come from the releasing team rather than independent replication. The agent evaluations were run with preserve_thinking=true, a setting the model card recommends for multi-turn tool use but not for general chat, so comparing task success alongside total generated tokens under that fixed setting would be more informative than reading headline scores as a deployment ranking.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 25, 16:32

**Background**: Teacher-student distillation is a common way to build small, fast models: a large model generates high-quality reasoning traces that a smaller model is trained to imitate, so a strong 33B model can bootstrap a 3B agent. Terminal-Bench 2.1 measures whether an agent can complete real command-line tasks in a terminal environment, while SWE-Bench Pro evaluates longer-horizon software engineering work such as resolving issues in real repositories. The preserve_thinking flag controls whether a model's prior reasoning traces are carried forward into later turns of a multi-turn conversation, which matters for agents that call tools repeatedly and need to remember why they took earlier steps.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aiiq.org/benchmarks/terminal-bench-2-1/">Terminal - Bench 2 . 1 Benchmark — AI IQ</a></li>
<li><a href="https://labs.scale.com/leaderboard/swe_bench_pro_public_v2">SWE-Bench Pro V2 - labs.scale.com</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp/issues/22615">Documentation: `preserve_thinking=true` preserves reasoning ...</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#open-weights`, `#AI-agents`, `#benchmarking`, `#model-release`

---

<a id="item-12"></a>
## [China's MIIT Drafts Mandatory Standard for Blue-Green ADS Marker Lights](https://t.me/zaihuapd/44677) ⭐️ 6.0/10

China's Ministry of Industry and Information Technology (MIIT) opened public comment on a draft mandatory national standard for automotive lighting that creates a dedicated blue-green color requirement for the ADS (automated driving system) marker lamp and forbids any lamp function from displaying text. The draft also bans turning lights off by voice command and controlling lamps with hand gestures, and requires that turn signals not be combined with brake lights or rear fog lamps. Until now each automaker has implemented the so-called "little blue light" for driver-assistance systems freely, so a single national color and rule set gives other road users, traffic police and regulators a consistent external signal of whether an automated driving system is active. Because the lamp is tied to L3-and-above automation, the standard is effectively part of the emerging regulatory framework that assigns responsibility when a car drives itself. The standard is proposed to take effect in January 2028, with a four-year grace period for vehicle models already approved, so existing cars will not need immediate retrofit. The ban on text displays and on voice- or gesture-based lamp control targets features that some manufacturers have marketed as light-show or interaction gimmicks.

telegram · zaihuapd · Oct 25, 01:35

**Background**: An ADS marker lamp is an exterior indicator light that tells people outside the car whether an automated driving system is engaged; it has been widely nicknamed the "little blue light" in China because early implementations used blue. Under China's auto-driving classification, L3 marks the point where the system, not the driver, is responsible for monitoring the road in defined conditions, which is why regulators want an unambiguous visual cue. Several Chinese cities and pilot rules had already begun requiring such lamps on L3-capable models before MIIT moved to write the requirement into a mandatory national standard.

<details><summary>References</summary>
<ul>
<li><a href="https://www.toutiao.com/article/7698628794709590566/">不再乱蓝！智驾ADS标志灯敲定蓝绿色，L3时代灯光规则落地</a></li>
<li><a href="https://finance.sina.com.cn/roll/2026-10-20/doc-inivwitm5795852.shtml">L3自动驾驶放开前夕：拟启用“蓝绿色”标志灯，灯亮则责变！</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/1920572045470705569">七月开始，注意车上蓝色小灯！自动驾驶新纪元来了！ - 知乎</a></li>

</ul>
</details>

**Tags**: `#automotive`, `#regulation`, `#ADAS`, `#autonomous-driving`, `#safety`

---

<a id="item-13"></a>
## [GPU Rental Prices Surge Across the Board, Even the Aging A100](https://x.com/a16z/status/2113741008550990191) ⭐️ 6.0/10

An a16z-sourced GPU rental price index, normalized to 100 on January 1, 2026, shows that as of October 19 the seven-day moving average had climbed to roughly 265 for the H200, 225 for the B200, 165 for the RTX PRO 6000 workstation edition, 137 for the H100 SXM, and 102 for the A100 SXM4. That translates into cumulative gains of about 160% for the H200, 120% for the B200, 65% for the RTX PRO 6000, and 35% for the H100, with even the A100 — launched back in 2020 — sitting slightly above its level at the start of the year. Broad-based increases across every generation — including previous-gen H100 and the four-year-old A100 — suggest that supply is tight enough that buyers are being pushed down the stack rather than simply absorbing the newest chips, a classic signal of compute scarcity. Since GPU rental rates feed directly into the unit economics of model training and inference, sustained increases would raise costs for AI startups and could shift the balance of power toward whoever holds contracted capacity. The figures are a seven-day moving average of rental rates indexed to January 1, 2026, so they smooth out daily volatility but reveal nothing about absolute dollar-per-GPU-hour prices, provider mix, contract length, or which regions and instance types were sampled. The newest Blackwell-generation parts show the steepest appreciation — the H200 at roughly 2.65x and the B200 at about 2.25x — while the A100's mere 2% gain over ten months indicates the increase is concentrated at the high end rather than uniform.

telegram · zaihuapd · Oct 25, 06:39

**Background**: A GPU rental price index tracks what cloud providers and neoclouds charge per GPU-hour, similar in spirit to the Ornn Compute Price Index, which is built from executed trades rather than list prices; such indices are watched as a real-time gauge of AI compute supply and demand. The chips involved span several NVIDIA generations: the A100 (2020, Ampere) and H100 (Hopper) are previous-generation workhorses, the H200 is a Hopper refresh with more high-bandwidth memory, and the B200 is a Blackwell-generation part that NVIDIA positions as delivering dramatically higher performance and total cost of ownership than HGX H100 systems. The RTX PRO 6000 Blackwell Workstation Edition is NVIDIA's flagship desktop professional GPU with 96GB of memory, often rented out for AI work that does not require datacenter-class interconnect.

<details><summary>References</summary>
<ul>
<li><a href="https://vast.ai/article/nvidia-h200-vs-b200-comparing-datacenter-grade-accelerators">NVIDIA H200 vs. B200: Comparing Datacenter-Grade Accelerators</a></li>
<li><a href="https://www.nvidia.com/en-us/products/workstations/professional-desktop-gpus/rtx-pro-6000/">NVIDIA RTX PRO 6000 Blackwell Workstation Edition</a></li>
<li><a href="https://data.ornn.com/markets">GPU Market Prices : Compute Price Index (OCPI) | Ornn Data</a></li>

</ul>
</details>

**Tags**: `#GPU pricing`, `#AI infrastructure`, `#compute scarcity`, `#cloud economics`, `#hardware market`

---

<a id="item-14"></a>
## [Tesla to launch in-house AI maps with FSD v15](https://www.digitaltoday.co.kr/en/view/118497/tesla-to-build-in-house-maps-and-navigation-to-address-fsd-limits) ⭐️ 6.0/10

Tesla is building an AI-based in-house mapping and navigation system that will first ship as part of FSD v15, initially handling the start and end segments of a trip before expanding over the following months to full navigation and parking. The system will draw on road data crowdsourced from Tesla's fleet to improve speed-limit recognition, parking and route selection, and will support voice commands and personalized route preferences. This marks a reversal of Tesla's long-standing position that autonomy should not depend on maps, which had been a defining claim of its camera-only, mapless FSD strategy. If Tesla ships a fleet-driven map stack, it will blur the line between the two dominant autonomous-driving camps and could give its vision-only approach a data-driven prior that competitors typically get from HD maps. The rollout is staged rather than a full navigation replacement: v15 covers only trip start and end routing at first, with navigation and parking following months later. Tesla has not published technical specifics such as map format, update cadence or how the fleet-derived layer is fused with the on-car vision network, and the motivation cited in reporting is shareholder criticism of FSD's speed-limit recognition, parking and route selection.

telegram · zaihuapd · Oct 25, 10:57

**Background**: Tesla's FSD has been built as a vision-only system that infers lanes, signs and geometry from cameras in real time, in contrast to rivals such as Waymo and Chinese automakers that rely on HD maps — highly detailed, pre-surveyed 3D maps of the road. The industry has lately shifted toward 'mapless' driving, which is seen as key to scaling autonomous features to new cities without re-surveying every road, and was even the subject of a dedicated CVPR 2024 autonomous-driving challenge. Tesla's twist is a middle path: instead of buying maps from a supplier, it would synthesize a map layer from the sensor data its own customer fleet already collects. Notably, Tesla AI engineer Phil Duan has publicly said navigation and pothole-detection improvements are coming.

<details><summary>References</summary>
<ul>
<li><a href="https://www.notateslaapp.com/news/4761/tesla-fsd-to-get-navigation-improvements-and-pothole-detection">Tesla FSD to Get Navigation Improvements and... - Not a Tesla App</a></li>
<li><a href="https://www.themoonlight.io/zh/review/mapvision-cvpr-2024-autonomous-grand-challenge-mapless-driving-tech-report">[论文评述] MapVision: CVPR 2024 Autonomous Grand Challenge...</a></li>
<li><a href="https://www.cnbeta.com.tw/articles/tech/1435590.htm">AI顶会 自 动 驾 驶 挑战赛：“ 无 图 ”小米全球第二 - 科技与交通 - cnBeta.COM</a></li>

</ul>
</details>

**Tags**: `#tesla`, `#fsd`, `#autonomous-driving`, `#ai-mapping`, `#navigation`

---

<a id="item-15"></a>
## [GEEKCON Shanghai drone-hacking challenge halted after vendor police report](https://tech.ifeng.com/c/8xSZe56UAz6) ⭐️ 6.0/10

At the GEEKCON security event in Shanghai, which closed on the evening of October 24, a drone attack-and-defense challenge reportedly prompted a leading drone manufacturer to call the police, leading to participants being taken away for questioning and the contest being temporarily suspended. The challenge required contestants to bypass GPS-based no-fly restrictions and seize full control of a drone. The incident highlights how fragile the line between authorized white-hat contests and real-world risk is in China, where a challenge run inside a hacking event can still trigger a police response from a vendor. It could have a chilling effect on vulnerability research and coordinated disclosure practices for drones and other connected hardware, and it raises questions about how contest organizers pre-clear sensitive attack scenarios with manufacturers. The reported challenge combined two sensitive capabilities: defeating geofencing that relies on GPS positioning to keep drones out of restricted airspace, and achieving full control takeover of the aircraft. The item is a short media digest with no primary source, no technical write-up, and no confirmation of the specific vendor involved or the legal status of those detained, so details remain unverified.

telegram · zaihuapd · Oct 25, 13:29

**Background**: Consumer drones from major vendors ship with a geofencing system that uses GPS to detect whether the aircraft is inside a no-fly zone and blocks takeoff when it is. Circumventing these limits — often sold as so-called "unlocking" services — is a grey-to-illegal market in China, which is why demonstrating such attacks live is legally sensitive. GEEKCON is an annual security-geek conference held every October 24 and long sponsored by firms such as Huawei, Tencent Security and Ant Group; its 2025 edition added a track on low-altitude economy and robot security, which is where drone topics were featured. Coordinated vulnerability disclosure (CVD) is the norm under which researchers report flaws to vendors before going public, and off-script live demos can break that protocol.

<details><summary>References</summary>
<ul>
<li><a href="https://www.4hou.com/posts/Bv4n">记 GEEKCON 2025...</a></li>
<li><a href="https://www.hnyundian.com/xingyexinwen/174.html">无 人 机 “破 限 ”黑产揭秘：你的“自由 飞 行”可能已触犯刑法</a></li>
<li><a href="https://www.geekpark.net/news/326450">GEEKCON ...</a></li>

</ul>
</details>

**Tags**: `#security-research`, `#drone-security`, `#coordinated-disclosure`, `#china-tech-policy`, `#hacking-contests`

---