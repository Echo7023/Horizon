---
layout: default
title: "Horizon Summary: 2026-10-24 (EN)"
date: 2026-10-24
lang: en
---

> From 34 items, 13 important content pieces were selected

---

1. [Moonshot AI launches Kimi K3.1 Pro and Highspeed, weights due Nov 4](#item-1) ⭐️ 8.0/10
2. [Security researchers demonstrate a working iPhone exploit](#item-2) ⭐️ 8.0/10
3. [SemiAnalysis: AWS Trainium Shifts From Inference Chip to Credible Training Platform](#item-3) ⭐️ 8.0/10
4. [PHP Ships Emergency Patches for Two CVSS 9.2 RCE Flaws](#item-4) ⭐️ 8.0/10
5. [Local Wikipedia: Wikipedia, but only for things a half hour walk from you](#item-5) ⭐️ 7.0/10
6. [EFF Warns Canadians' Time to Oppose Bill C-22 Is Running Out](#item-6) ⭐️ 7.0/10
7. [Swarm Imitation Proven Equivalent to a Single Bandit-Learning Agent](#item-7) ⭐️ 7.0/10
8. [ByteDance launches Seedance 2.5 video model with 30-second generation](#item-8) ⭐️ 7.0/10
9. [Claimed Untethered iPhone 18 Pro Jailbreak Survives Reboot](#item-9) ⭐️ 7.0/10
10. [China's State Council Issues Guidance to Curb AI-Driven Job Displacement](#item-10) ⭐️ 7.0/10
11. [Job Loss and Cortisone Mania: A Personal Essay That Resonated on HN](#item-11) ⭐️ 6.0/10
12. [LLM Memory May Need Forgetting, Not Just More Recall](#item-12) ⭐️ 6.0/10
13. [Microsoft quietly tests Project Pantheon, a Recall alternative with user-selected AI memories](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Moonshot AI launches Kimi K3.1 Pro and Highspeed, weights due Nov 4](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

Moonshot AI released Kimi K3.1 Pro on October 24, 2026 as the first model in its new K3.1 series, alongside a faster companion variant called Kimi K3.1 Pro Highspeed. Both are available immediately on Kimi.ai, Kimi Work, Kimi Code, and the Kimi API, with full model weights promised by November 4. Kimi K3.1 Pro scores 55 on the Artificial Analysis Intelligence Index, placing 4th overall and ahead of both GPT-6 Astra and Fable 5.1 while running faster, which makes a Chinese open-weight model a genuine frontier contender. The planned weight release also puts pressure on the open-versus-closed debate, since a near-frontier model becoming downloadable reshapes what developers can self-host and what safety frameworks must handle. K3.1 Pro is a post-trained version of Kimi K3 trained with substantially larger post-training compute, and Moonshot states its offensive cyber capability is deliberately kept below what its pipeline could produce and behind frontier proprietary models, with plans to progressively raise the cyber capability released in open weights. On the Intelligence Index evaluation it generated 150M tokens versus a median of 87M, indicating a notably more verbose reasoning style.

hackernews · Jowsey · Oct 23, 16:59 · [Discussion](https://news.ycombinator.com/item?id=50212065)

**Background**: Kimi is the model family from Moonshot AI (月之暗面), a Chinese AI lab that has positioned itself around long-context models and, more recently, coding and agentic workloads. Post-training refers to the fine-tuning and reinforcement-learning stages after base pretraining, where most recent gains in reasoning and tool use are made. Open-weight models are ones whose parameters can be downloaded and run locally, which makes guardrails harder to enforce once released. Model distillation, a recurring topic in the discussion, is the practice of training a smaller student model on the outputs or signals of a larger teacher model to imitate its behavior more cheaply.

<details><summary>References</summary>
<ul>
<li><a href="https://www.unite.ai/moonshot-ai-releases-kimi-k3-1-pro-first-model-in-new-k3-1-series/">Moonshot AI Releases Kimi K3.1 Pro, First Model in New K3.1 ...</a></li>
<li><a href="https://www.kimi.ai/blog/kimi-k3-1-pro">Kimi K3.1 Pro Tech Blog: Advancing Open Intelligence</a></li>
<li><a href="https://snorkel.ai/blog/llm-distillation-demystified-a-complete-guide/">LLM distillation demystified: a complete guide | Snorkel AI</a></li>

</ul>
</details>

**Discussion**: Commenters were split between enthusiasm and skepticism: one user questioned how anyone could realistically distill a 1–2TB closed frontier model, while another reported hitting the 5-hour quota of a $99/month plan within 47 minutes of a single session. Others focused on the safety framing, noting that Moonshot admits it could build stronger cyber capabilities but chooses not to release them, and praising the gradual, "slow warming" approach to raising open-weight cyber ability.

**Tags**: `#AI models`, `#Kimi`, `#open weights`, `#AI safety`, `#LLM`

---

<a id="item-2"></a>
## [Security researchers demonstrate a working iPhone exploit](https://blog.calif.io/p/iphone) ⭐️ 8.0/10

A security research team published a write-up titled "Today, we hacked what we'd set out to hack: the iPhone," demonstrating what appears to be a full exploit chain against Apple's iOS. The post, which drew roughly 587 points and nearly 400 comments on Hacker News, reads as a proof-of-concept demonstration rather than the release of a weaponized tool. iOS is one of the most heavily audited and hardened consumer platforms, so a demonstrated exploit chain is a notable data point about the state of mobile security. The discussion around it also touches on whether AI-assisted vulnerability discovery is becoming a decisive advantage for whichever labs and vendors can afford frontier models. The published material is a demo rather than a shipped product or a disclosed CVE, and the summary notes that at least part of the work likely relied on AI-assisted exploit discovery. Commenters specifically asked whether Apple's Lockdown Mode — which restricts message attachments, web technologies, and wired connections — would actually block the demonstrated techniques, a question the post does not appear to settle.

hackernews · pavel_lishin · Oct 23, 16:21 · [Discussion](https://news.ycombinator.com/item?id=50211474)

**Background**: Lockdown Mode is an optional, opt-in iOS setting that severely limits attack surface — for example by blocking most message attachment types, disabling just-in-time JavaScript compilation in Safari, and refusing wired connections to accessories — in order to defeat highly targeted spyware such as Pegasus. Past iOS exploit chains, notably Project Zero's ForcedEntry, have chained a malicious PDF or image parser bug with a sandbox escape, which is why commenters flagged PDFs as a recurring weak point. Meanwhile, frontier AI labs increasingly gate access to their most capable models through "trusted cyber access" or red-team programs, which shapes who can do this kind of research.

<details><summary>References</summary>
<ul>
<li><a href="https://support.apple.com/en-us/105120">About Lockdown Mode - Apple Support</a></li>
<li><a href="https://www.bitdefender.com/en-us/blog/hotforsecurity/what-is-lockdown-mode-iphone-mac-spyware-when-use-it">Apple’s Lockdown Mode Explained: What It Does, Who Needs It ...</a></li>
<li><a href="https://cloud.google.com/blog/topics/threat-intelligence/vulnerability-discovery-and-exploitation-trends-in-the-ai-era">Vulnerability Discovery and Exploitation Trends in the AI Era</a></li>

</ul>
</details>

**Discussion**: Sentiment was a mix of admiration for the demos and frustration with the surrounding ecosystem. Several commenters mourned the loss of tinkering culture, noting that jailbreaking now risks being locked out of iCloud and iMessage, while others argued that restricting frontier-model access to an "inner circle" makes those programs "a moat rather than a safeguard." A recurring practical question was whether Lockdown Mode meaningfully mitigates these exploits, and one commenter noted that the videos were less fun without the dancing anime girl and EDM.

**Tags**: `#security`, `#iOS`, `#exploit-research`, `#AI-red-teaming`, `#mobile-security`

---

<a id="item-3"></a>
## [SemiAnalysis: AWS Trainium Shifts From Inference Chip to Credible Training Platform](https://newsletter.semianalysis.com/p/amazons-trainium-takes-a-strike-at) ⭐️ 8.0/10

SemiAnalysis published a deep dive arguing that Amazon's Trainium has evolved from an inference-focused accelerator into a credible AI training platform. The analysis highlights native PyTorch support on Trainium, high-quality continuous integration (CI), integration with TorchTitan, and profiling tooling the authors describe as "GPU impossible." Training is the most demanding and lucrative segment of the AI accelerator market, and Nvidia's dominance there rests as much on software (CUDA, PyTorch tooling) as on silicon. If Trainium can genuinely run mainstream PyTorch training workloads with good tooling, AWS gains a stronger cost argument against Nvidia GPUs and offers large cloud customers a real second source for training capacity. The key claim is that Trainium now supports PyTorch natively rather than requiring heavy graph rewrites, backed by solid CI so that frameworks and kernels do not silently break, plus TorchTitan-based recipes for large-scale distributed training. The item is based on a short excerpt, so specific benchmark numbers, supported model sizes, and remaining limitations versus Nvidia hardware are not detailed in the available content.

rss · Semianalysis · Oct 23, 19:06

**Background**: Trainium is Amazon's in-house AI chip family, built to deliver better price-performance than GPU instances for training and inference inside AWS data centers; Amazon has advertised up to roughly 50% cost-to-train savings versus comparable EC2 instances and uses the chips in its partnership with Anthropic. Historically, custom accelerators have struggled less on raw compute than on software: developers expect their PyTorch code to run unchanged, and any missing operator or weak profiler can sink adoption. TorchTitan is a PyTorch-native reference platform for large-scale generative model training, bundling 3D parallelism, training optimizations, and scalable distributed checkpointing, which makes it a useful yardstick for whether a new accelerator's software stack is production-ready.

<details><summary>References</summary>
<ul>
<li><a href="https://aws.amazon.com/ai/machine-learning/trainium/">AI Accelerator - AWS Trainium - AWS | Amazon Web Services, Inc.</a></li>
<li><a href="https://www.aboutamazon.com/news/aws/what-you-need-to-know-about-the-aws-ai-chips-powering-amazons-partnership-with-anthropic">AWS AI chips powering Amazon 's partnership with Anthropic</a></li>
<li><a href="https://github.com/pytorch/torchtitan">GitHub - pytorch/ torchtitan : A PyTorch native platform for training...</a></li>

</ul>
</details>

**Tags**: `#AWS Trainium`, `#AI hardware`, `#ML training`, `#PyTorch`, `#SemiAnalysis`

---

<a id="item-4"></a>
## [PHP Ships Emergency Patches for Two CVSS 9.2 RCE Flaws](https://t.me/zaihuapd/44647) ⭐️ 8.0/10

The PHP team released out-of-band security updates — PHP 8.5.12, 8.4.27, 8.3.36 and 8.2.35 — fixing two critical vulnerabilities, each rated 9.2 under CVSS 4.0, that let an attacker execute arbitrary code remotely without authenticating, and it is urging all users to upgrade immediately. PHP underpins a very large share of the public web, and these flaws affect essentially every deployment that handles HTTP requests — PHP-FPM, Apache's mod_php, php-cgi, FrankenPHP and LiteSpeed — so any unpatched internet-facing server is potentially exploitable by an anonymous attacker, making this an urgent patch-now event for operators and hosting providers. mod_php carries the highest risk: validation has shown the attack can be triggered before the site's own application code runs, so application-layer defenses and input filtering inside your PHP code will not stop it. Upgrading to one of the four fixed releases is the only reliable remedy, and because the fix is an emergency patch rather than a documented technical deep-dive, administrators should verify their actual web server SAPI (FPM, mod_php, CGI, FrankenPHP or LiteSpeed) is running the patched binary rather than trusting a package version string alone.

telegram · zaihuapd · Oct 23, 13:46

**Background**: PHP is a scripting language executed by a server-side component (the SAPI) on behalf of the web server. The most common setup is PHP-FPM, a FastCGI process manager that runs PHP worker processes separately from the web server and is typically used on heavily loaded sites; the older alternative is mod_php, which embeds the PHP interpreter directly inside the Apache process, and newer options such as FrankenPHP embed PHP inside a Go/Caddy-based application server. The CVSS 4.0 scoring system published by FIRST rates vulnerabilities from 0 to 10, where 9.0–10.0 is classified as Critical — so a 9.2 score with no authentication required signals a flaw that should be treated as actively dangerous rather than a theoretical risk.

<details><summary>References</summary>
<ul>
<li><a href="https://www.php.net/manual/en/install.fpm.php">PHP: FastCGI Process Manager (FPM) - Manual</a></li>
<li><a href="https://frankenphp.dev/">FrankenPHP : the modern PHP app server</a></li>
<li><a href="https://php2shell.io/">PHP2Shell: Fix CVE-2026-109618 & CVE-2026-109619</a></li>

</ul>
</details>

**Tags**: `#security`, `#php`, `#vulnerability`, `#remote-code-execution`, `#patching`

---

<a id="item-5"></a>
## [Local Wikipedia: Wikipedia, but only for things a half hour walk from you](https://edjefferson.com/localwiki/) ⭐️ 7.0/10

Local Wikipedia is a hyperlocal Wikipedia browser that shows only articles about places within walking distance, sparking discussion about knowledge curation and proximity-based relevance.

hackernews · sohkamyung · Oct 22, 23:01 · [Discussion](https://news.ycombinator.com/item?id=50202285)

**Tags**: `#Wikipedia`, `#hyperlocal`, `#geolocation`, `#knowledge curation`, `#web tools`

---

<a id="item-6"></a>
## [EFF Warns Canadians' Time to Oppose Bill C-22 Is Running Out](https://www.eff.org/deeplinks/2026/10/canadians-are-running-out-time-oppose-dangerous-c-22-surveillance-bill) ⭐️ 7.0/10

The EFF has published a warning that Canadians have limited time to oppose Bill C-22, a surveillance bill that would expand data sharing with foreign law enforcement and threaten messaging privacy. If enacted, Bill C-22 could expose Canadian users' data to foreign law enforcement, weaken end-to-end encryption, and push major messaging services to block or withdraw from Canada. The bill would require telecoms, messaging apps, and potentially other digital services to build police and CSIS surveillance capabilities and retain user metadata for up to a year, and it has already passed the House of Commons and moved to the Senate.

hackernews · hn_acker · Oct 22, 22:43 · [Discussion](https://news.ycombinator.com/item?id=50202114)

**Background**: Bill C-22, also called the Lawful Access Act, is a Canadian surveillance bill that would amend the Criminal Code, the CSIS Act, and related laws to give police and intelligence agencies new investigative powers. Its critics say the metadata-retention and system-rebuilding mandates amount to surveillance backdoors that would undermine encryption. The bill also expands cross-border data sharing, a sensitive issue because Canada and the United States have been negotiating reciprocal access agreements under cloud-data laws.

<details><summary>References</summary>
<ul>
<li><a href="https://www.le-vpn.com/canada-bill-c-22-lawful-access-vpn/">Canada Bill C - 22 Explained: Lawful Access and VPNs | Le VPN</a></li>
<li><a href="https://reclaimthenet.org/even-google-warns-canada-bill-c-22-creates-surveillance-backdoors">Even Google Warns Canada Bill C - 22 Creates Surveillance Backdoors</a></li>
<li><a href="https://www.accessnow.org/press-release/encryption-and-privacy-threats-in-canadas-bill-c-22/">Open letter from European civil society organisations on encryption ...</a></li>

</ul>
</details>

**Discussion**: Commenters were divided but largely skeptical: some argued that petitions and public engagement are the only real counterweight and urged Canadians to act, while others said the Senate rarely kills bills and that the fight may already be lost. Several warned that major messaging services would block Canada if the bill stands, and some criticized Canada-U.S. data-sharing arrangements that could give American police access without Canadian court oversight.

**Tags**: `#privacy`, `#surveillance`, `#Canada`, `#encryption`, `#tech policy`

---

<a id="item-7"></a>
## [Swarm Imitation Proven Equivalent to a Single Bandit-Learning Agent](https://www.reddit.com/r/MachineLearning/comments/1xdhf7r/r_the_hive_mind_is_a_single_reinforcement/) ⭐️ 7.0/10

A Reddit r/MachineLearning post (submitted by /u/mistlab) presents a proof that decentralized local imitation in a large population — including the honey bee waggle-dance "weighted voter" model — is mathematically equivalent to a single-agent reinforcement learning update in a multi-armed bandit. The authors derive a new macro-level algorithm called Maynard-Cross Learning (MCL), in which each of the N non-learning individuals acts as a parallel environment rollout, giving an effective per-sample step size of alpha = 1/N. If the equivalence holds, it gives a formal mechanism for how "hive mind" collective intelligence can emerge from individuals that merely copy neighbors without any learning or payoff comparison, linking swarm intelligence and evolutionary game theory to standard RL theory. That has implications for biologists modeling collective cognition and for engineers designing scalable, decentralized swarm-robotics algorithms where coordination arises from simple local rules. The proof first shows that the classic "imitation of success" protocol — copying neighbors with probability proportional to their payoffs — evolves identically to the expected update of the Cross Learning bandit algorithm, and then extends this to the payoff-blind waggle-dance imitation rule to obtain MCL. The claim is an unverified preprint-level result posted on Reddit rather than a peer-reviewed publication, and the key limitation is that the equivalence is stated for the macroscopic population distribution under mean-field-style replicator dynamics, not for finite, structured, or spatially heterogeneous populations.

reddit · r/MachineLearning · /u/mistlab · Oct 23, 15:37

**Background**: The multi-armed bandit is a canonical reinforcement learning problem: an agent repeatedly picks one of several arms, each returning a random reward from an unknown distribution, and must balance exploiting the best-known arm against exploring others. Cross Learning is an early, simple bandit algorithm that updates action probabilities directly from observed rewards. Evolutionary game theory describes how strategy frequencies in a population change over time via replicator dynamics, and honey bee nest-site selection is the textbook biological example — scouts advertise sites with a waggle dance whose duration scales with site quality, and followers copy advertised sites without evaluating them. The paper's claim is that these two descriptions — population-level imitation and single-agent learning — are the same mathematical object.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Multi-armed_bandit">Multi-armed bandit - Wikipedia</a></li>
<li><a href="https://content.ces.ncsu.edu/honey-bee-dance-language">The Honey Bee Dance Language - NC State Extension Publications What Is the Waggle Dance? How Honey Bees Communicate Distance ... The evolution of honey bee dance communication: a mechanistic ... Frontiers | Why, when and where did honey bee dance ... Foraging distance distributions reveal how honeybee waggle ...</a></li>

</ul>
</details>

**Tags**: `#reinforcement-learning`, `#swarm-intelligence`, `#multi-armed-bandits`, `#evolutionary-game-theory`, `#collective-decision-making`

---

<a id="item-8"></a>
## [ByteDance launches Seedance 2.5 video model with 30-second generation](https://t.me/zaihuapd/44639) ⭐️ 7.0/10

ByteDance officially released Seedance 2.5 on July 31, a next-generation audio-video joint generation model that doubles the single-pass output of the previous version from 15 seconds to 30 seconds. It adds multi-round extension for producing multi-minute continuous videos, accepts up to 30 images, 10 videos and 10 audio clips as references in one request, and supports timestamp-level control over shots and pacing. Longer single-pass clips plus extension and dense reference inputs move AI video generation from short demo shots toward usable narrative sequences, which matters for advertisers, short-drama producers and other content teams in China. Rolling it out through Jimeng AI and Doubao Pro before the Volcano Ark API means ByteDance is pushing the capability to both consumers and enterprise developers almost simultaneously. The release emphasizes long-form storytelling, multimodal reference and editing, with timestamp-based control letting creators steer individual segments rather than regenerating a whole clip. The news brief gives no benchmarks, resolution details or pricing, and availability, duration and cost are expected to vary by entry point such as Seedance.tv, Jimeng AI and the Volcano Ark API.

telegram · zaihuapd · Oct 23, 08:27

**Background**: Seedance is ByteDance's family of video generation models; the earlier 2.0 version established the original multimodal generation system, while 2.5 is positioned around longer narratives, larger reference sets and more advanced editing. Jimeng AI (known overseas as Dreamina) is ByteDance's one-stop AI creation platform where users turn text or images into short videos and pictures, and Doubao is its consumer AI assistant brand. Volcano Ark is the model service platform from ByteDance's cloud arm Volcano Engine, offering inference, fine-tuning and deployment, with APIs compatible with the OpenAI protocol so developers can migrate existing SDK-based code.

<details><summary>References</summary>
<ul>
<li><a href="https://seed.bytedance.com/en/seedance2_5">Seedance 2.5 - seed.bytedance.com</a></li>
<li><a href="https://moge.ai/zh/product/jimeng-ai">Jimeng AI : 字 节 跳 动 推出的 AI ... - MOGE</a></li>
<li><a href="https://www.huasheng.ai/insights/volcengine-ark-api-guide/">火山引擎方舟 API 平台深度调研 | 花叔 火山方舟 - 首页 - ark.volcengine.com SDK中心 - api.volcengine.com 安装及升级 SDK - 火山方舟 - 火山引擎</a></li>

</ul>
</details>

**Tags**: `#AI video generation`, `#ByteDance`, `#Seedance`, `#multimodal`, `#generative AI`

---

<a id="item-9"></a>
## [Claimed Untethered iPhone 18 Pro Jailbreak Survives Reboot](https://t.me/zaihuapd/44644) ⭐️ 7.0/10

A Telegram channel report claims that researcher @calif_io demonstrated an untethered jailbreak on an iPhone 18 Pro that persists across reboots without needing a computer, which would make it the first publicly shown full untethered jailbreak since iOS 9. The claimed attack chain spans three layers: abuse of the cryptex subsystem, spoofing of TSS ticket signing, and a bypass of PAC (Pointer Authentication Code). If confirmed, a reboot-persistent jailbreak on current hardware would be a major milestone for iOS security research, showing that Apple's layered defenses — signed system volumes, server-side signing checks, and hardware pointer authentication — can still be chained together and defeated. It would also matter for the broader ecosystem, since jailbreak techniques often foreshadow the kinds of exploit chains used by commercial spyware and influence iOS hardening priorities. The claim rests on a single short Telegram post with no published write-up, proof-of-concept code, or independent corroboration, and the timing is notable because Apple reportedly patched 273 vulnerabilities on September 14, suggesting the chain relies on flaws that were not covered by that update. Details such as the affected iOS version, the device's A-series chip, and whether userland persistence is truly achieved after a full reboot remain unverified.

telegram · zaihuapd · Oct 23, 11:43

**Background**: A jailbreak removes Apple's software restrictions to allow code and apps outside the App Store; a 'tethered' jailbreak breaks after every reboot and must be reapplied from a computer, while an 'untethered' one survives restarts on its own, which is far harder to achieve. The cryptex subsystem is Apple's mechanism for delivering cryptographically signed auxiliary software in personalized disk images, and because it controls where those images are published and mounted, it is a tempting target for bypassing signature checks. TSS (Ticket Signing System) is the Apple server that issues signed 'tickets' authorizing a specific firmware to be installed, so spoofing those tickets means fooling the device into accepting code Apple never approved. PAC (Pointer Authentication Code) attaches a cryptographic signature to pointers on A12 (iPhone XS) and later chips, so a corrupted pointer fails its signature check and crashes instead of yielding code execution — making a PAC bypass the crucial final step for kernel-level control on modern iPhones.

<details><summary>References</summary>
<ul>
<li><a href="https://keith.github.io/xcode-man-pages/cryptex.5.html">cryptex (5)</a></li>
<li><a href="https://tin-z.github.io/ios-exploit-starterpack/en/pac/">PAC -- Pointer Authentication Code | iOS Exploit Starterpack</a></li>
<li><a href="https://eclecticlight.co/2022/11/16/cryptex-how-a-custom-iphone-is-changing-macos-updates/">Cryptex : how a custom iPhone is changing macOS updates</a></li>

</ul>
</details>

**Tags**: `#iOS jailbreak`, `#mobile security`, `#exploit chain`, `#PAC bypass`, `#Apple`

---

<a id="item-10"></a>
## [China's State Council Issues Guidance to Curb AI-Driven Job Displacement](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 7.0/10

On October 23, China's State Council General Office published the "Opinions on Adapting to the Development of Artificial Intelligence Technology and Helping Build an Employment-Friendly Development Model" (Guobanfa [2026] No. 29), which calls for mitigating the job-replacement effects of AI applications. The document directs that AI be prioritized in roles facing labor shortages or high environmental risk, that its deployment in labor-intensive industries be advanced with steady and prudent control over scope, intensity and pace, and that enterprises be encouraged to explore an "unemployment buffer period" system with advance notice to affected workers plus retraining and job-transfer support. This is one of the first formal State Council-level policy documents to treat AI-driven job displacement as a governance problem rather than only an efficiency opportunity, signaling that Chinese AI adoption will increasingly be weighed against employment stability. It could shape how companies in labor-intensive sectors such as manufacturing, logistics, customer service and content operations sequence their automation rollouts, and it gives local governments a mandate to build retraining and transition support infrastructure. The guidance is framed as an "opinion" (意见) rather than binding legislation, so its force comes through local implementation and follow-on measures; it emphasizes amplifying AI's positive effects on job creation, upgrading traditional roles and raising job quality while curbing substitution effects. The "unemployment buffer period" is described as something enterprises are encouraged to explore, meaning participation is voluntary rather than a mandated severance or notice requirement.

telegram · zaihuapd · Oct 23, 12:54

**Background**: China's State Council General Office is the administrative office of the central government, and documents it issues with a "Guobanfa" numbering (here No. 29 of 2026) set the policy direction that ministries and provincial governments then implement. "Employment-friendly development model" (就业友好型发展方式) is a policy concept that frames economic and technological development in terms of whether it expands or preserves decent jobs. As generative AI spreads into white-collar and service work, Chinese policymakers have increasingly paired promotion of AI with measures to stabilize employment, following earlier commentary from bodies such as the National Development and Reform Commission on AI empowering rather than displacing workers.

<details><summary>References</summary>
<ul>
<li><a href="https://www1.xinhuanet.com/politics/20261023/f21a5777774749daa0eed451c81f4002/c.html">国务院办公厅印发《关于适应人工智能技术发展助力构建就业友好型发展...</a></li>
<li><a href="https://www.stdaily.com/web/2026-10/23/content_601752.html">国务院办公厅关于适应人工智能技术发展助力构建就业友好型发展方式的...</a></li>
<li><a href="https://finance.eastmoney.com/a/202610243906815770.html">国务院办公厅公布《关于适应人工智能技术发展助力构建就业友好型发展...</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#employment`, `#China`, `#AI governance`, `#labor market`

---

<a id="item-11"></a>
## [Job Loss and Cortisone Mania: A Personal Essay That Resonated on HN](https://tilschuenemann.de/job-loss-cortisone-mania) ⭐️ 6.0/10

The author of the blog tilschuenemann.de published a first-person account of how losing his job and then undergoing cortisone (corticosteroid) treatment tipped him into a manic episode. The post reached the Hacker News front page, drawing roughly 156 points and 89 comments, with the author himself showing up in the thread to thank readers and note that he is currently tapering off the drug after about six weeks of treatment. Corticosteroid-induced psychiatric effects are well documented in the medical literature but rarely discussed among general tech audiences, so a candid first-person account can help patients and their families recognize mania, hypomania, and psychosis as possible drug side effects rather than purely psychological events. The discussion also broadened into a wider conversation about how much identity and meaning people attach to their jobs. The author notes he has access to Germany's public health insurance and good doctors, and is tapering off the cortisone after a roughly six-week course. Anecdotes from commenters suggest the psychiatric and physical fallout can appear even in patients taking the drugs for non-psychiatric reasons, such as cancer treatment or immunotherapy.

hackernews · speckx · Oct 23, 10:31 · [Discussion](https://news.ycombinator.com/item?id=50206840)

**Background**: Cortisone belongs to the corticosteroid class of drugs (alongside prednisone and prednisolone), which are widely prescribed as potent anti-inflammatory and immunosuppressive agents for conditions ranging from allergies and autoimmune disease to cancer treatment support. Their psychiatric side effects are recognized but often underappreciated: reviews describe mood disturbance, anxiety, insomnia, and in some cases frank mania or psychosis, with euphoria and hypomania being the most common short-term effects. Proposed mechanisms center on dysregulation of the hypothalamic–pituitary–adrenal (HPA) axis, and case reports indicate manic symptoms can occur even at low doses.

<details><summary>References</summary>
<ul>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11675195/">Corticosteroid-Induced Psychiatric Disorders: Mechanisms ...</a></li>
<li><a href="https://www.mayoclinicproceedings.org/article/S0025-6196(11)61160-9/fulltext">Psychiatric Adverse Effects of Corticosteroids - Mayo Clinic ...</a></li>
<li><a href="https://www.frontiersin.org/journals/pharmacology/articles/10.3389/fphar.2025.1628765/full">Frontiers | Corticosteroid - induced manic and /or psychotic symptoms...</a></li>

</ul>
</details>

**Discussion**: The thread was overwhelmingly supportive, with the author expressing surprise and gratitude at the response. Commenters shared serious firsthand experiences — one described immunotherapy causing extreme muscle weakness and inflammation after treatment for thymus carcinoma, echoing the essay's theme — while others reflected philosophically that modern life leaves little fulfillment outside of work and that job loss can paradoxically feel liberating.

**Tags**: `#mental-health`, `#corticosteroids`, `#job-loss`, `#work-life-balance`, `#personal-essay`

---

<a id="item-12"></a>
## [LLM Memory May Need Forgetting, Not Just More Recall](https://www.reddit.com/r/MachineLearning/comments/1xdpek9/are_we_solving_llm_memory_by_remembering_more/) ⭐️ 6.0/10

A Reddit r/MachineLearning post argues that LLM memory research focuses too heavily on recall capacity and neglects the harder problem of updating or forgetting outdated knowledge. It compares how Transformers, RAG, linear attention, DeltaNet, and BDH handle conflicts between old and new information, using an example where a coding agent keeps applying a 30-second API timeout after documentation changes it to 5 seconds. As long-context models reach hundreds of thousands or millions of tokens, simply retaining more information does not guarantee that agents use the current version of a fact. This matters for coding agents, RAG systems, and any application where stale knowledge can cause incorrect actions. The post distinguishes storing information from updating it and asks whether the core difficulty lies in memory storage/update mechanisms or in reasoning over contradictions. It notes that DeltaNet uses prediction-error-based updates and BDH uses Hebbian-style synaptic plasticity, but questions when to update, when to retain, and how to avoid corrupting unrelated memories; it proposes contradiction-based evaluations but presents no experiments or benchmark results.

reddit · r/MachineLearning · /u/Prestigious-Tip6030 · Oct 23, 20:39

**Background**: Long-context LLMs are designed to keep large amounts of text available during inference, but most evaluations test whether a model can retrieve a fact rather than whether it revises that fact when newer evidence appears. In a standard Transformer or RAG pipeline, old and new passages can coexist in the context, leaving the model to resolve the conflict at read time. Linear attention compresses history into a fixed-size state, and DeltaNet-style updates use the difference between predicted and observed values to erase and rewrite associations. BDH (Dragon Hatchling) instead explores Hebbian synaptic plasticity, where memory is tied to changing connection weights rather than an explicit token buffer.

<details><summary>References</summary>
<ul>
<li><a href="https://sustcsonglin.github.io/blog/2024/deltanet-3/">DeltaNet Explained (Part III) | Songlin Yang</a></li>
<li><a href="https://www.crvscience.com/post/the-dragon-hatchling-a-bio-physical-paradigm-for-post-transformer-artificial-intelligence">The Dragon Hatchling : A Bio-Physical Paradigm for Post-Transformer...</a></li>
<li><a href="https://arxiv.org/pdf/2507.19595">Efficient Attention Mechanisms for Large Language Models: A ...</a></li>

</ul>
</details>

**Tags**: `#LLM memory`, `#long-context`, `#DeltaNet`, `#RAG`, `#machine-learning`

---

<a id="item-13"></a>
## [Microsoft quietly tests Project Pantheon, a Recall alternative with user-selected AI memories](https://www.windowslatest.com/2026/10/23/microsoft-is-quietly-testing-another-recall-for-windows-11-but-this-one-doesnt-record-your-screen/) ⭐️ 6.0/10

Microsoft is reportedly quietly testing a Windows 11 AI memory app called Project Pantheon, with a version named Context Vault that saves only content users explicitly select—web pages, files, screenshots, text, and audio/video—as memories. It lets users query those memories and exposes them to AI tools such as Claude and Cursor through an MCP server, unlike Recall's automatic screen recording. If shipped, this would give Windows a more consent-driven memory layer than Recall and could make the PC a shared context source for third-party AI agents via MCP. It also signals Microsoft is still experimenting with Recall-style features despite the privacy backlash that followed Recall's announcement. The app is a separate download and reportedly relies on cloud models rather than on-device processing; Microsoft has not announced or committed to a release and is reportedly considering encryption, Windows Hello authentication, and IT management controls. Because it is unofficial and unconfirmed, availability, pricing, and privacy guarantees remain unknown.

telegram · zaihuapd · Oct 23, 07:42

**Background**: Windows Recall, announced in 2024, periodically captures screenshots of user activity so they can search past work, but it drew criticism because it records the screen automatically and initially required a Copilot+ PC with a dedicated NPU. MCP (Model Context Protocol) is an open standard introduced by Anthropic that lets AI applications connect to external data sources and tools through a common interface, so clients like Claude or Cursor can call into local or remote services.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/gadgets/2025/04/in-depth-with-windows-11-recall-and-what-microsoft-has-and-hasnt-fixed/">In depth with Windows 11 Recall —and what Microsoft... - Ars Technica</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#Microsoft`, `#Windows 11`, `#AI memory`, `#MCP`, `#Privacy`

---