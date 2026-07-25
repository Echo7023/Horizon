---
layout: default
title: "Horizon Summary: 2026-07-26 (EN)"
date: 2026-07-26
lang: en
---

> From 24 items, 9 important content pieces were selected

---

1. [SGLang v0.5.16: DSpark Speculative Decoding and Inkling MoE Support](#item-1) ⭐️ 9.0/10
2. [vLLM v0.26.0 Adds Inkling Support, Boosts DeepSeek-V4](#item-2) ⭐️ 8.0/10
3. [Open-weight AI parallels Kubernetes rise](#item-3) ⭐️ 8.0/10
4. [Android May Restrict On-Device ADB](#item-4) ⭐️ 8.0/10
5. [Introducing Claude Opus 5](#item-5) ⭐️ 8.0/10
6. [AMD Challenges CUDA Moat with MI455X and Agentic Kernel Generation](#item-6) ⭐️ 8.0/10
7. [China Issues New Offshore Trust Tax Rules](#item-7) ⭐️ 8.0/10
8. [China Fines Trip.com 5.18 Billion Yuan for Monopoly](#item-8) ⭐️ 8.0/10
9. [Microsoft to Block Pirated Windows Activation with TPM Chips](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.16: DSpark Speculative Decoding and Inkling MoE Support](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 9.0/10

SGLang v0.5.16 introduces DSpark, a confidence-driven speculative decoding algorithm achieving 383.7 tok/s, and adds support for the Inkling 975B-parameter multimodal MoE model. This release significantly improves inference throughput, enabling faster generation for large models. DSpark's adaptive verification and Inkling's massive scale demonstrate progress in efficient inference for multimodal and MoE architectures. DSpark uses semi-autoregressive drafting with confidence-based verify window sizing. Inkling combines sliding-window, full attention, and Mamba2 linear attention, supports NVFP4 quantization, and handles a 1M-token context. The release also removes experimental QServe and FBGEMM FP8 paths.

github · Qiaolin-Yu · Jul 25, 00:13

**Background**: Speculative decoding speeds up LLM inference by having a small draft model generate candidate tokens that are verified by the target model. MoE (Mixture of Experts) models activate only a subset of parameters per token, enabling large model capacity with efficient computation. SGLang is an open-source inference engine optimized for large language and vision models.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative ...</a></li>
<li><a href="https://www.marktechpost.com/2026/06/27/deepseek-releases-dspark-a-speculative-decoding-framework-that-accelerates-deepseek-v4-per-user-generation-60-85-over-mtp-1/">DeepSeek Releases DSpark, a Speculative Decoding Framework ...</a></li>

</ul>
</details>

**Tags**: `#speculative decoding`, `#MoE`, `#large language models`, `#inference optimization`, `#SGLang`

---

<a id="item-2"></a>
## [vLLM v0.26.0 Adds Inkling Support, Boosts DeepSeek-V4](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 introduces day-0 support for the TML Inkling multimodal model family, delivers significant performance improvements for DeepSeek-V4 via specialized kernels and routing optimizations, and adds flexible attention backends per KV-cache group, among many other enhancements. This release demonstrates vLLM's continued role as a high-performance inference engine for cutting-edge LLMs, with day-0 support for a major new model family (Inkling) and deep optimizations for the popular DeepSeek-V4 model, benefiting both researchers and production users. The Inkling support includes piecewise CUDA graphs, Hopper FA4 relative attention, MTP=1 speculative decoding, LoRA, and ModelOpt NVFP4 quantization. For DeepSeek-V4, a specialized routing kernel yields 2.94% end-to-end TPOT improvement, and fused_topk_bias achieves 1.5–2x kernel speedup. The new head_dtype option enables fp32 lm_head for improved generation accuracy.

github · khluu · Jul 25, 10:38

**Background**: vLLM is an open-source high-throughput LLM inference engine developed by UC Berkeley and community contributors. The TML Inkling is a 1-trillion-parameter multimodal model by Thinking Machines Lab that accepts text, image, and audio inputs. DeepSeek-V4 is the latest version of DeepSeek's open-weight LLM family, known for its cost-effective training and competitive performance.

<details><summary>References</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-07-15-inkling">TML Inkling on vLLM: Day-0 Support with Optimized Performance</a></li>
<li><a href="https://docs.vllm.ai/en/latest/api/vllm/models/inkling/">inkling - vLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#performance optimization`, `#release notes`

---

<a id="item-3"></a>
## [Open-weight AI parallels Kubernetes rise](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 8.0/10

This article, published on July 25, 2026, draws a direct analogy between the rise of open-weight AI models and the trajectory of Kubernetes, arguing that open-weight AI is becoming the interoperable standard that prevents vendor lock-in and drives down costs. This analogy is significant because it suggests open-weight AI could reshape the AI infrastructure landscape, reducing dependency on closed API providers and fostering a more competitive ecosystem, similar to how Kubernetes standardized cloud-native computing. Open-weight models allow users to download the model's learned parameters for customization and local deployment, but unlike fully open-source AI, training data and code are not always included. The article highlights that this trade-off mirrors Kubernetes's role as a portable abstraction layer without exposing all underlying details.

hackernews · tknaup · Jul 25, 14:49 · [Discussion](https://news.ycombinator.com/item?id=49048034)

**Background**: An open-weight AI model makes its internal parameters (weights) available for download, enabling users to run and fine-tune the model on their own hardware, but it may not meet all criteria for open-source software. Kubernetes, originally developed by Google, became the de facto standard for container orchestration, preventing vendor lock-in in cloud deployments. The cloud-native computing foundation (CNCF) was formed to steward Kubernetes as a neutral open-source project.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/open-weight-ai-what-we-finally-opened-bonnet-nicolas-pistorio-n3ulf">Open - weight AI : what if we finally opened the bonnet ?</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kubernetes">Kubernetes - Wikipedia</a></li>
<li><a href="https://kingy.ai/blog/open-models-vs-closed-models/">Open Models vs Closed Models: The 2026 AI Verdict</a></li>

</ul>
</details>

**Discussion**: Community comments largely agree with the analogy, with users noting that open-weight models provide a sanity-inducing baseline for inference pricing (tokenomics) and could enable collaborative model development similar to Linux. However, some express concerns about hardware costs and the need for truly open training data to fully realize the parallel. A comment also praises the idea of government procurement driving demand for interoperable systems.

**Tags**: `#AI`, `#open-source`, `#industry-trends`, `#analogy`, `#infrastructure`

---

<a id="item-4"></a>
## [Android May Restrict On-Device ADB](https://kitsumed.github.io/blog/posts/android-may-soon-restrict-on-device-adb/) ⭐️ 8.0/10

Google is considering restricting on-device ADB access, which would require additional authentication or limit which IP addresses can connect, based on a feature request in the Android issue tracker. This change could impact Android developers who rely on ADB for debugging and sideloading, potentially reducing attack surface but also limiting developer control and freedom. The proposed restriction specifically targets on-device ADB (Wireless Debugging), not USB-based ADB; some suggestions include allowing connections only from specific IP addresses or requiring a confirmation dialog.

hackernews · shscs911 · Jul 25, 06:57 · [Discussion](https://news.ycombinator.com/item?id=49045159)

**Background**: ADB (Android Debug Bridge) is a command-line tool that allows developers to communicate with an Android device for debugging and app installation. On-device ADB enables wireless debugging without a computer, making it convenient for developers and power users. This feature has been used for side loading apps and accessing advanced settings.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Android_Debug_Bridge">Android Debug Bridge - Wikipedia</a></li>
<li><a href="https://developer.android.com/tools/adb">Android Debug Bridge (adb) | Android Studio | Android Developers</a></li>
<li><a href="https://medium.com/@EazSoftware/a-comprehensive-guide-to-adb-android-debug-bridge-the-unsung-hero-for-android-developers-28b349037436">A Comprehensive Guide to ADB (Android Debug Bridge): The ...</a></li>

</ul>
</details>

**Discussion**: Community reactions are divided: some argue the change is unnecessary because enabling ADB already requires user consent, while others see it as part of a broader trend of Google locking down Android, reducing openness compared to iOS. Several commenters express concerns about future restrictions on sideloading and developer autonomy.

**Tags**: `#Android`, `#ADB`, `#security`, `#developer tools`, `#Google`

---

<a id="item-5"></a>
## [Introducing Claude Opus 5](https://simonwillison.net/2026/Jul/24/introducing-claude-opus-5/#atom-everything) ⭐️ 8.0/10

Anthropic introduces Claude Opus 5, a cost-effective model rivaling frontier intelligence.

rss · Simon Willison · Jul 24, 23:48

**Tags**: `#AI`, `#large language models`, `#Claude`, `#Anthropic`

---

<a id="item-6"></a>
## [AMD Challenges CUDA Moat with MI455X and Agentic Kernel Generation](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

AMD launched the Instinct MI455X GPU and Helios rack-scale system at Advancing AI 2026, while also revealing a new software initiative called Agentic Kernel Generation aimed at automating CUDA kernel optimization using reinforcement learning. AMD's efforts could weaken Nvidia's CUDA monopoly by improving ROCm software stack and delivering competitive hardware, potentially lowering costs and increasing choice for AI infrastructure. The MI455X features 432GB of HBM4 memory on a 2nm process, offering up to 4x performance in MXFP8/MXFP4 versus the MI355X; the Helios rack connects 72 such GPUs via UALink. Agentic Kernel Generation uses large-scale RL to generate high-performance CUDA kernels, a direct attack on Nvidia's software advantage.

rss · Semianalysis · Jul 25, 00:33

**Background**: Nvidia's CUDA ecosystem has long been a major moat, with proprietary libraries and tools that lock developers into Nvidia hardware. AMD's ROCm aims to provide an open alternative but has lagged in performance and developer adoption. The MI455X and Agentic Kernel Generation represent AMD's latest push to overcome these barriers, combining new hardware with automated software optimization.

<details><summary>References</summary>
<ul>
<li><a href="https://www.phoronix.com/news/AMD-Instinct-MI455X-Helios">AMD Launches Instinct MI455X, Helios AI Rack - Phoronix</a></li>
<li><a href="https://arxiv.org/abs/2602.24286">[2602.24286] CUDA Agent: Large-Scale Agentic RL for High-Performance CUDA Kernel Generation</a></li>

</ul>
</details>

**Tags**: `#AMD`, `#CUDA`, `#AI hardware`, `#software ecosystem`, `#GPU`

---

<a id="item-7"></a>
## [China Issues New Offshore Trust Tax Rules](https://liaoning.chinatax.gov.cn/art/2026/7/24/art_5869_7823.html) ⭐️ 8.0/10

On July 24, 2026, the Ministry of Finance and State Taxation Administration jointly issued rules requiring Chinese tax residents to declare and pay tax on property transferred into offshore trusts and on annual trust income, effective immediately. This regulation closes tax avoidance loopholes by applying a look-through (pass-through) taxation principle, treating undistributed trust income as taxable each year, significantly impacting high-net-worth individuals and wealth planning. The fixed tax rate is 20% on appreciation (current value minus original cost and expenses) at all stages—transfer, operation, and liquidation. Retroactive compliance for 2023–2025 requires filing within 90 days without late payment surcharges.

telegram · zaihuapd · Jul 25, 00:31

**Background**: Offshore trusts are legal arrangements established under foreign law to hold assets, often used for estate planning and tax optimization. Previously, income retained within the trust was not taxed until distributed, allowing deferral. China now adopts a pass-through approach, taxing the resident settlor or beneficiary directly on the trust's income each year.

<details><summary>References</summary>
<ul>
<li><a href="https://www.shui5.cn/article/c6/12399.html">shui5.cn/article/c6/12399.html</a></li>
<li><a href="https://www.bjnews.com.cn/detail/1784880489129754.html">bjnews.com.cn/detail/1784880489129754.html</a></li>
<li><a href="https://www.zenind.com/zh-CHS/help/post/pass-through-taxation-for-small-business-owners-how-it-works-and-which-entities-qualify">小企业主的穿透式征税：运作方式及适用实体类型</a></li>

</ul>
</details>

**Tags**: `#tax regulation`, `#offshore trust`, `#China`, `#personal income tax`, `#wealth management`

---

<a id="item-8"></a>
## [China Fines Trip.com 5.18 Billion Yuan for Monopoly](https://t.me/zaihuapd/42767) ⭐️ 8.0/10

On July 25, China's State Administration for Market Regulation fined Trip.com Group 5.179 billion yuan for abusing its market dominance, confiscating illegal gains of 1.658 billion yuan and imposing a fine of 3.521 billion yuan. This is one of the largest antitrust penalties in China's tech sector, signaling intensified regulatory scrutiny on platform companies and reinforcing the government's commitment to fair competition. The regulator also ordered Trip.com to refund 122 million yuan in deposits forcibly deducted from hotel operators and required comprehensive corrective actions, including public disclosure of reforms.

telegram · zaihuapd · Jul 25, 11:56

**Background**: China's Anti-Monopoly Law prohibits businesses with market dominance from abusing their position, such as through unfair pricing or exclusive dealing. Trip.com, as a leading online travel platform in China, faced allegations of forcing hotels into exclusive agreements and charging excessively high commissions.

**Tags**: `#antitrust`, `#regulation`, `#tech industry`, `#China`

---

<a id="item-9"></a>
## [Microsoft to Block Pirated Windows Activation with TPM Chips](https://www.techspot.com/news/113232-microsoft-using-tpm-chips-crack-down-pirated-windows.html) ⭐️ 8.0/10

Microsoft announced a new TPM-based attestation mechanism for its Key Management Service (KMS) that verifies the hardware identity of activation servers before allowing bulk Windows activation, effectively blocking counterfeit KMS servers used by pirates. The feature will become mandatory starting with the next version of Windows Server and will be prompted in Windows Server 2025 from August 2026. This move represents a significant escalation in Microsoft's anti-piracy efforts, targeting the widely exploited KMS activation loophole that pirates have used for years. It could render many current activation tools obsolete, but the cat-and-mouse dynamic continues with new exploits like TSforge emerging. The new feature is called 'KMS Hardware-Secured' and uses TPM attestation to ensure activation servers are running on trusted hardware. Microsoft already disabled the KMS38 loophole in 2025, and the new TPM verification aims to stop Online KMS tools like those from Massgrave that require periodic reconnection to fake servers.

telegram · zaihuapd · Jul 25, 15:55

**Background**: Key Management Service (KMS) is a Microsoft technology for enterprise volume activation of Windows and Office, allowing organizations to activate multiple devices through a local server. Pirates have long abused KMS by running counterfeit activation servers. The Trusted Platform Module (TPM) is a hardware chip that provides secure cryptographic functions, including attestation to verify system integrity. Previous exploits like KMS38 allowed offline activation until 2038, while the newer TSforge method claims to bypass the entire Software Protection Platform.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techspot.com/news/113232-microsoft-using-tpm-chips-crack-down-pirated-windows.html">Microsoft is using TPM chips to crack down on pirated Windows ...</a></li>
<li><a href="https://petri.com/microsoft-secure-windows-kms-tpm-attestation/">Microsoft to Secure Windows KMS With TPM Attestation</a></li>
<li><a href="https://massgrave.dev/blog/tsforge">TSforge | MAS</a></li>

</ul>
</details>

**Tags**: `#Windows`, `#security`, `#DRM`, `#anti-piracy`, `#TPM`

---