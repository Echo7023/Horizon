---
layout: default
title: "Horizon Summary: 2026-11-05 (EN)"
date: 2026-11-05
lang: en
---

> From 42 items, 26 important content pieces were selected

---

1. [Tencent to Lease 100,000 Advanced AI Chips from Oracle in $7B Deal](#item-1) ⭐️ 9.0/10
2. [AI-Driven Vulnerability Discovery Forces Teams to Confront Decades of Technical Debt](#item-2) ⭐️ 8.0/10
3. [Go's standard library gains a redesigned encoding/json/v2 API](#item-3) ⭐️ 8.0/10
4. [Anthropic Shares FlashProve, a zkSNARK Prototype for Provable LLM Inference](#item-4) ⭐️ 8.0/10
5. [Tencent Releases Hy4, a 770B Open-Weight Model With Game-Dev Focus](#item-5) ⭐️ 8.0/10
6. [North Korean fake job interview linked to $6.3B Binance heist](#item-6) ⭐️ 8.0/10
7. [Gemini Trains on Saved Chats Even for Paying Subscribers, PSA Warns](#item-7) ⭐️ 8.0/10
8. [Moonshot AI releases Kimi K3.1 Pro open weights](#item-8) ⭐️ 8.0/10
9. [RunAnywhere open-sources NKI megakernel inference engine for GLM-5.3-Flash on AWS Trainium2](#item-9) ⭐️ 8.0/10
10. [NIKKE PC launcher alleged to be trojanized in supply chain attack](#item-10) ⭐️ 8.0/10
11. [Residential Proxy Exits Detected on White House-Attributed IP Space](#item-11) ⭐️ 7.0/10
12. [Ripple-65B Preview Claims U.S. Open-Weight SOTA on Agentic Coding](#item-12) ⭐️ 7.0/10
13. [Nvidia RTX Spark Laptops Hit 35% AI Inference Speed on Linux Due to Encrypted Firmware](#item-13) ⭐️ 7.0/10
14. [OpenAI to acquire Pierre Computer, maker of Codex's diff and tree libraries](#item-14) ⭐️ 7.0/10
15. [Verification Is Not Knowledge: Essay Asks What AI Can Add to Science](#item-15) ⭐️ 7.0/10
16. [Hydrogen-1.0: open-weight science model beats GPT-6 Astra on FrontierScience](#item-16) ⭐️ 7.0/10
17. [Looped Transformers Like Huginn Save Weight Storage, Not HBM Traffic, B200 Profiling Finds](#item-17) ⭐️ 7.0/10
18. [Tencent Releases Hunyuan Hy3: 295B MoE Model Halves Hallucinations](#item-18) ⭐️ 7.0/10
19. [Alipay and Partners Launch ACT Protocol, China's First AI Agent Commerce Trust Framework](#item-19) ⭐️ 7.0/10
20. [Huawei Tells Ascend 960DT Customers to Source Samsung, SK Hynix HBM Themselves](#item-20) ⭐️ 7.0/10
21. [Cloudflare adds analytics and tiered controls for personal AI agents](#item-21) ⭐️ 7.0/10
22. [AMD Expects to Outsell Intel in Q4 for the First Time in History](#item-22) ⭐️ 6.0/10
23. [Researcher Urges Top AI Conferences to Desk-Reject AI-Generated Papers](#item-23) ⭐️ 6.0/10
24. [Reddit post asks why CVPR allows 25 submissions per author](#item-24) ⭐️ 6.0/10
25. [Anthropic Says Anti-Distillation Defenses Cut Extracted Data by 90-99%](#item-25) ⭐️ 6.0/10
26. [Microsoft Offers Voluntary Severance to Roughly 60,000 Employees](#item-26) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Tencent to Lease 100,000 Advanced AI Chips from Oracle in $7B Deal](https://t.me/zaihuapd/44912) ⭐️ 9.0/10

Tencent has reportedly signed a roughly $7 billion, five-year lease with Oracle for about 100,000 advanced AI chips, sourced through data centers in Southeast Asia. The deal is described as Tencent's largest overseas leasing arrangement to date and requires about 30% of the payment to be made upfront. The arrangement gives Tencent access to cutting-edge compute it cannot legally buy, showing how Chinese AI firms are restructuring around U.S. export controls by renting capacity abroad instead of purchasing hardware. If the model proves replicable, it could reshape cross-border cloud economics and become a template for other Chinese labs facing the same restrictions. U.S. rules bar Chinese companies from directly buying advanced chips such as Nvidia's H100-class accelerators, but leasing compute hosted overseas falls outside that prohibition. The chips will be spread across multiple Southeast Asian data centers, and Tencent reportedly intends to use the capacity to accelerate development of its AI models and agent tooling.

telegram · zaihuapd · Nov 4, 11:01

**Background**: Since 2022 the U.S. Bureau of Industry and Security has progressively tightened Export Administration Regulations on advanced computing items, blocking sales of top-tier AI accelerators to China and later restricting Nvidia's China-specific H800 and H20 variants. Chinese firms have responded by stockpiling chips, designing domestic alternatives, and increasingly renting compute from overseas cloud providers. Oracle has been expanding its AI cloud infrastructure business, leasing large clusters of Nvidia GPUs to customers who cannot or prefer not to build their own data centers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sidley.com/en/insights/newsupdates/2025/01/new-us-export-controls-on-advanced-computing-items-and-artificial-intelligence-model-weights">New U.S. Export Controls on Advanced Computing Items and ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Hopper_(microarchitecture)">Hopper (microarchitecture) - Wikipedia</a></li>
<li><a href="https://computelaw.blog/deals/export-control-compliance-advanced-ai-chips/">Export control compliance for running advanced AI chips</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#export controls`, `#Tencent`, `#Oracle`, `#cloud computing`

---

<a id="item-2"></a>
## [AI-Driven Vulnerability Discovery Forces Teams to Confront Decades of Technical Debt](https://spectrum.ieee.org/ai-in-cybersecurity-php2shell-vulnerability) ⭐️ 8.0/10

IEEE Spectrum published an analysis arguing that AI-driven vulnerability discovery — framed around the 'php2shell' vulnerability — is exposing decades of accumulated security and technical debt faster than software teams can absorb it. The piece sparked a large Hacker News discussion (1004 points, 607 comments) debating whether AI is finally helping repay that debt or merely putting engineering teams on a compulsory treadmill of fix-work. If AI can find latent flaws at machine speed, every software organization — especially those maintaining long-lived codebases and open-source dependencies — faces a sudden, unbudgeted surge of security remediation work. The debate matters because it reframes technical debt from a slow-burning maintainability concern into an immediate security exposure that cannot be deferred. Commenters pointed out that not all of this debt is composed of narrow, surgically patchable bugs like off-by-one errors; many findings require genuine restructuring or redesign, which is far costlier and slower than applying a quick fix. Others invoked Gödel, Escher, Bach's record-player parable to note that no system can be made perfectly secure even in theory, so AI-driven discovery has no natural endpoint.

hackernews · pseudolus · Nov 4, 11:52 · [Discussion](https://news.ycombinator.com/item?id=50364336)

**Background**: Technical debt is the accumulated cost of shortcuts, outdated designs, and deferred maintenance in a codebase; in security terms it appears as latent vulnerabilities, unpatched dependencies, and fragile legacy code. AI-driven vulnerability discovery uses machine learning and large language models to scan and reason about code at scale, surfacing bugs and exploitable flaws far faster than manual audits or traditional fuzzing. The resulting flood of findings — each mapped to a CVE and a required patch — is what the IEEE Spectrum piece and the Hacker News thread are arguing about.

<details><summary>References</summary>
<ul>
<li><a href="https://clearwatersecurity.com/blog/advisory-for-ai-driven-vulnerability-discovery/">Advisory for Resiliency against AI - Driven Vulnerability Discovery</a></li>
<li><a href="https://www.infotech.com/research/reassess-cybersecurity-exposure-in-the-age-of-ai-driven-vulnerability-discovery">Reassess Cybersecurity Exposure in the Age of AI - Driven ...</a></li>

</ul>
</details>

**Discussion**: Sentiment is split between optimism and skepticism. Optimists like glennfiedler concede the next few months will 'suck a bit' but argue software will end up more secure than ever, while swatcoder warns it may be an 'endless treadmill of feature-neutral fix-work' rather than genuine debt repayment. Arbortheus adds a hope that state-held and commercial zero-days (such as Pegasus-style tooling) will be found incidentally through this wave of AI scanning.

**Tags**: `#AI`, `#cybersecurity`, `#technical debt`, `#vulnerability discovery`, `#software engineering`

---

<a id="item-3"></a>
## [Go's standard library gains a redesigned encoding/json/v2 API](https://go.dev/blog/jsonv2) ⭐️ 8.0/10

The Go team published an official blog post introducing encoding/json/v2, a ground-up redesign of the standard library's JSON encoder and decoder that ships as part of Go 1.27 behind the GOEXPERIMENT=jsonv2 toolchain flag. The new API splits JSON handling into a low-level token package (jsontext) and a higher-level semantic package (json), and the team has also published a dedicated migration guide for moving from v1. encoding/json is one of the most widely imported packages in the Go ecosystem, so any change to it touches virtually every Go service that speaks JSON over HTTP, gRPC gateways, or config files. The redesign addresses long-standing complaints about performance, correctness edge cases, and ergonomics that the community has raised for years, while a migration guide and the experimental flag are intended to keep the transition from breaking existing code. Per the migration guide, v1 is not going away: encoding/json keeps its historical default behavior, and v2 is opt-in via GOEXPERIMENT=jsonv2 until the ecosystem catches up. The redesign changes several defaults and drops convenience helpers such as MarshalIndent, whose equivalent in v2 requires more verbose, non-obvious option configuration, and the jsontext layer exposes token-level streaming that is useful for building custom parsers without reflection overhead.

hackernews · olexsmir · Nov 4, 17:52 · [Discussion](https://news.ycombinator.com/item?id=50369106)

**Background**: Go's encoding/json package has been in the standard library since the language's early days and works by reflecting over Go structs to map them to and from JSON. Over the years users documented a number of quirks: field names are matched case-insensitively, duplicate object keys are silently accepted, invalid UTF-8 is not strictly rejected, and reflection-based encoding is slower than hand-written parsers. A v2 redesign was proposed and debated in the Go issue tracker for several years before landing as an experiment, and it also introduces jsontext, a separate package that handles raw JSON tokens so that applications can build streaming or schema-aware parsers on top of it.

<details><summary>References</summary>
<ul>
<li><a href="https://go.dev/doc/jsonv2-migration">encoding/json/v2 Migration Guide - The Go Programming Language</a></li>
<li><a href="https://pkg.go.dev/encoding/json/v2">json package - encoding/json/v2 - Go Packages</a></li>
<li><a href="https://go.dev/src/internal/goexperiment/flags.go">The Go Programming Language</a></li>

</ul>
</details>

**Discussion**: Commenters broadly welcome the redesign but raise concrete API critiques, most notably that dropping MarshalIndent makes both one-off debugging output and migration noticeably more painful, since the v2 equivalent is complicated and non-obvious. Others note that jsontext already works well in production for building high-performance parsers with precise error reporting, one commenter sketches simdjson-style schema-specialized parsers as a future direction, and several reflect on Go increasingly being a target language for AI-generated code rather than something they write by hand.

**Tags**: `#Go`, `#JSON`, `#standard library`, `#API design`, `#parsing`

---

<a id="item-4"></a>
## [Anthropic Shares FlashProve, a zkSNARK Prototype for Provable LLM Inference](https://www.anthropic.com/research/provable-inference) ⭐️ 8.0/10

Anthropic published a research post on November 2, 2026 describing a research prototype called FlashProve, which uses zkSNARKs to cryptographically prove that a specific language model (reported to be a 400B-parameter Llama 4 Maverick) actually produced a given response. The system commits to model weights once with a roughly 6.5 MB commitment good for about 16 million requests, then emits one proof per request. Provable inference addresses a core trust gap in commercial AI: customers currently have no way to verify that the model they pay for is the model actually running on the provider's servers. Progress here matters for AI safety auditing, compliance, and any agentic or financial workflow where a signed, attributable output is required — though the large compute overhead keeps it a research prototype rather than a deployable product. The cost is steep: proofs impose roughly 90–100x compute overhead (some coverage cites an optimized 72x figure), and verifying a single proof takes about 17 seconds on 24 threads or 21 seconds on a single thread, including the offline phase check. Notably, the scheme still assumes deterministic inference, a requirement that simpler verification approaches also depend on.

hackernews · ltononro · Nov 4, 17:17 · [Discussion](https://news.ycombinator.com/item?id=50368626)

**Background**: A zkSNARK is a cryptographic proof that lets a prover convince a verifier a computation was executed correctly, without the verifier re-running it or learning the private inputs. Applied to LLMs, this would let a provider prove 'model X produced this reply' without revealing its weights, which closed-weight vendors care about. Prior academic work such as zkLLM showed proofs for 13B-parameter models in under 15 minutes, so Anthropic's contribution is largely about scaling to far larger models and reducing overhead.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/provable-inference">Progress on provable inference for large language models</a></li>
<li><a href="https://blockchain.news/news/anthropic-provable-inference-flashprove-llama-4-maverick">Anthropic reports progress on provable inference for large ...</a></li>
<li><a href="https://arxiv.org/abs/2404.16109">zkLLM: Zero Knowledge Proofs for Large Language Models zkLLM: Zero Knowledge Proofs for Large Language Models OpenLLM: Modular and Scalable zkSNARKs for Verifiable LLM ... zkLLM: Zero-Knowledge Proofs for LLMs Zero-Knowledge Proofs for Verifiable AI Inference: The 2026 ... zkGPT: An Efficient Non-interactive Zero-knowledge Proof ...</a></li>

</ul>
</details>

**Discussion**: Commenters pushed back on several fronts: one researcher claimed the work builds heavily on his prior VerInf project, including the choice of 400B Maverick, with little attribution. Others argued that for open-weight models verification is trivial (just re-run the computation), and that a probabilistic proof from four independent inference providers running the same non-batched prompt is far cheaper than a 90–100x compute hit, leaving signed responses and trusted hardware as competing options for closed models.

**Tags**: `#verifiable inference`, `#LLM`, `#cryptography`, `#zero-knowledge proofs`, `#AI safety`

---

<a id="item-5"></a>
## [Tencent Releases Hy4, a 770B Open-Weight Model With Game-Dev Focus](https://hy.tencent.ai/research/hy4) ⭐️ 8.0/10

Tencent released and open-sourced Hy4 (Hy4 preview), a Mixture-of-Experts foundation model with 770B total parameters, 49B active per token and a context window exceeding 1M tokens, published as open weights on Hugging Face under Apache 2.0. Alongside it, Tencent open-sourced two scientific foundation models co-developed with Hyra 2.0 — HyCell for single-cell representation and HyPDE for physical field modeling — and openly stated that a notable gap remains between Hy4 and top proprietary models. A major Chinese lab shipping a frontier-scale open-weight model puts pressure on the open vs. closed gap and gives developers a self-hostable alternative to proprietary APIs at a moment when open-weight releases from big players are increasingly rare. The unusual specialization in game development — spanning Unreal, Unity and Godot integration, gameplay logic, state tracking and multiplayer — targets a large but underserved vertical that general-purpose models handle poorly. Tencent says Hy4 ranks first among open-weight models on TenureTrail, its internal benchmark of 123 research tasks across seven disciplines, but concedes weaknesses on research-level mathematics, long-horizon coding, model self-improvement and advanced visual question answering. The game-development work involved curated training data and evaluations built with Tencent Interactive Entertainment Group (IEG) developers, and the model's scale means most users will end up renting it rather than running it locally.

hackernews · Philpax · Nov 4, 14:11 · [Discussion](https://news.ycombinator.com/item?id=50365780)

**Background**: Tencent Hy, formerly known as Tencent Hunyuan, is Tencent's family of large language models, and like many recent releases it uses a Mixture-of-Experts architecture: only a fraction of the total parameters are activated for each token, which cuts inference cost dramatically compared with a dense model of the same size. "Open-weight" means the trained parameters are downloadable, so researchers and companies can run, fine-tune or inspect the model themselves, even though full training data and code are typically not released. Hy4 also folds in Hyra 2.0, Tencent's earlier model, with which the HyCell and HyPDE scientific models were co-developed.

<details><summary>References</summary>
<ul>
<li><a href="https://hy.tencent.ai/research/hy4">Tencent Hy</a></li>
<li><a href="https://huggingface.co/tencent/Hy4-preview">tencent / Hy 4-preview · Hugging Face</a></li>
<li><a href="https://www.tencent.com/tencent-launches-hy4-joining-the-ranks-of-the-worlds-leading-open-source-ai-models/">Tencent Launches Hy4, Joining the Ranks of the World's Leading Open ...</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were broadly positive: one praised the open-sourcing of HyCell and HyPDE as "a refreshing contrast" to closed commercial AI that restricts research, and another applauded Tencent for candidly acknowledging the gap to top proprietary models. Others focused on the game-development specialization as a genuinely differentiated capability, while Plotly's Chris Parmer reported that Hy4 landed between competing GPT models on a data-analytics cost/accuracy frontier but was "verrrry slow," issuing roughly 26 queries per question and up to 64 in some cases.

**Tags**: `#open-weight models`, `#LLM release`, `#Tencent`, `#game development AI`, `#open source AI`

---

<a id="item-6"></a>
## [North Korean fake job interview linked to $6.3B Binance heist](https://www.theregister.com/security/2026/11/03/north-korean-fake-job-interview-led-to-63b-binance-heist/5307398) ⭐️ 8.0/10

According to The Register, a North Korean fake job-interview campaign allegedly led to a $6.3 billion Binance cryptocurrency heist, with the attack chain reportedly involving a compromised developer work machine. The case shows how social engineering aimed at developers can escalate into supply-chain and CI/CD credential compromise at financial scale, affecting crypto exchanges and any organization with software release pipelines. Commenters pinpoint a container deployment token that was reportedly usable outside CI as a major architectural weakness, and one describes a similar fake-interview attempt that pushed malicious npm dependencies and a trojaned Claude Code installer.

hackernews · smalltech · Nov 4, 14:09 · [Discussion](https://news.ycombinator.com/item?id=50365755)

**Background**: Fake job-interview attacks are a social-engineering technique in which attackers pose as recruiters and ask candidates to run code, clone repositories, or install tools during a supposed technical assessment. CI/CD pipelines automate building, testing, and deploying software, and a deployment token is a credential that should be tightly scoped to those pipelines. A supply-chain attack compromises a trusted software component or vendor to reach a downstream target, which is why developer machines and package dependencies are high-value entry points.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Supply_chain_attack">Supply chain attack</a></li>
<li><a href="https://learn.microsoft.com/en-us/devops/operate/safe-deployment-practices">Safe deployment practices - Azure DevOps | Microsoft Learn</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agree the engineer should not have used a work laptop for an outside interview, but many argue the larger failure is an architecture that let a container deployment token work outside CI. Others criticize dehumanizing, automated hiring funnels for creating the conditions for these scams, and one commenter recounts a fake interview that attempted malicious npm dependencies and a trojaned Claude Code installer; another says LinkedIn is not doing enough to stop fake recruiters.

**Tags**: `#security`, `#social-engineering`, `#supply-chain-attack`, `#ci-cd`, `#cryptocurrency`

---

<a id="item-7"></a>
## [Gemini Trains on Saved Chats Even for Paying Subscribers, PSA Warns](https://news.ycombinator.com/item?id=50363461) ⭐️ 8.0/10

A Hacker News PSA pointed out that for personal Google AI subscriptions, all saved Gemini chat history is used to train generative AI models, and the only ways to opt out are turning off the "Keep Activity" setting (which deletes chats after 72 hours) or using Temporary Chats. The post also cited Google's own help pages stating that a subset of chats is reviewed by human reviewers and that reviewed chats are retained for up to three years even if you delete your activity. Many users assume a paid subscription means their data is not used for training, so this is a concrete, actionable privacy disclosure for anyone using a mainstream consumer AI assistant. It also highlights how consent is bundled into a single activity-tracking toggle, and how human review plus multi-year retention can apply even to conversations users believe they have deleted. According to the cited help pages, turning off Keep Activity means you lose access to chat sessions after 72 hours, and reviewed transcripts are not deleted when you delete your activity but are retained for up to three years. Google explicitly warns users not to enter confidential information they wouldn't want a reviewer to see, and the setting was renamed from "Gemini Apps Activity" to "Keep Activity" around August 2025, with some help pages and menus still using the old name.

hackernews · jameslk · Nov 4, 10:10

**Background**: Gemini is Google's consumer AI assistant, offered free and through paid personal subscriptions. Like most consumer AI services, it has an activity setting that controls whether conversations are saved to your account and whether they may be used to improve Google's services, including training generative AI models. "Temporary Chats" are one-off sessions that are not saved to Gemini Apps Activity and do not influence future responses, while human review is a standard quality-and-safety practice in which a small sample of conversations is read by people.

<details><summary>References</summary>
<ul>
<li><a href="https://explainx.ai/blog/gemini-keep-activity-trains-on-chats-paid-subscribers-human-review-three-years-hacker-news-2026">Gemini Trains on Chats Even for Paid Users: Turn It Off ...</a></li>
<li><a href="https://redact.dev/blog/turn-off-gemini-apps-activity">Gemini Apps Activity Is Now Keep Activity: How to Turn It Off</a></li>
<li><a href="https://blog.google/products-and-platforms/products/gemini/temporary-chats-privacy-controls/">Gemini app personalizes responses based on past chats , plus new...</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed the practice is industry-wide, with one noting that all frontier model providers monitor and human-review interactions even when activity tracking is off, citing journalism on the topic. Pixel owners complained that Gemini refuses to perform basic tasks like setting reminders unless chat history is enabled, calling the UX coercive, while others said the disclosure is unsurprising and one user wondered whether correcting the model would feed useful training data; a further question was raised about whether human review extends to other app data Gemini can access, such as mail or gallery.

**Tags**: `#privacy`, `#Google Gemini`, `#AI training data`, `#terms of service`, `#consumer AI`

---

<a id="item-8"></a>
## [Moonshot AI releases Kimi K3.1 Pro open weights](https://huggingface.co/moonshotai/Kimi-K3.1-Pro) ⭐️ 8.0/10

Moonshot AI has released the weights for Kimi K3.1 Pro, the first model in its K3.1 series and a 3-trillion-parameter-class open-weight model with a 1-million-token context window. According to the release, it was post-trained from Kimi K3 with large-scale joint reinforcement learning across hundreds of downstream domains, improving coding, 3D creation, financial research, factual accuracy, and agentic tasks. A 3T-class model with publicly downloadable weights pushes the open-weight ecosystem closer to proprietary frontier systems, giving companies and researchers an option to self-host or fine-tune rather than rely solely on closed APIs. It also intensifies competition among inference providers, which can lower costs and improve throughput for developers. The model has a 1M-token context window and a Highspeed variant that Moonshot says is 2–3× faster than the standard version; official figures put Terminal-Bench 4.0 at 65.7%, above GPT-6 Astra's 58.2%. Community reports note that self-hosting demands serious hardware—one commenter cites an 8× B300 node—while third-party providers such as OpenRouter, Together, and Modal are already hosting it with differing throughput at similar price points.

hackernews · abrarthought · Nov 4, 15:30 · [Discussion](https://news.ycombinator.com/item?id=50366999)

**Background**: Moonshot AI is a Beijing-based artificial intelligence company and one of China's so-called 'AI tigers'; it develops the Kimi series of open-weight large language models. Its Kimi K3, released in July 2026, was described as the largest open-weight model family at 2.8 trillion parameters, and K3.1 Pro is positioned as a 3T-class successor. 'Open weights' means the trained parameters are publicly released so others can download, run, study, or modify the model, though this typically does not include training data or full training code.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3.1-Pro">moonshotai/Kimi-K3.1-Pro - Hugging Face</a></li>
<li><a href="https://www.kimi.ai/blog/kimi-k3-1-pro">Kimi K3.1 Pro Tech Blog: Advancing Open Intelligence</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were split: some praised it as a very strong open release that is close to the frontier and useful for most use cases, while others suspected it is 'benchmaxxed' because it does not clearly outperform DeepSeekV4.1-Flash and scores lower on Hy4's internal benchmarks than Opus5.5. Hardware cost was a major concern, and several noted that third-party inference providers are already competing on throughput and price, with Together and Modal reportedly offering higher throughput than Moonshot's own endpoint.

**Tags**: `#AI/ML`, `#open-weight models`, `#LLM`, `#inference`, `#Kimi K3.1`

---

<a id="item-9"></a>
## [RunAnywhere open-sources NKI megakernel inference engine for GLM-5.3-Flash on AWS Trainium2](https://www.reddit.com/r/MachineLearning/comments/1xo0yuq/p_nki_layer_megakernels_for_glm53flash_on_aws/) ⭐️ 8.0/10

RunAnywhere open-sourced trnrt, an inference engine that serves GLM-5.3-Flash (a 320B mixture-of-experts model with 1M-token context) on a single trn2.48xlarge instance. By rewriting each layer half as a single NKI megakernel that keeps the working set in SBUF, they cut a batch-8 decode step from 32.2 ms on their 17 October build to 24.2 ms on the 1 November build, against a 6.1 ms memory-bandwidth floor. The profiling shows that on Trainium2 the bulk of decode time was framework and kernel-launch overhead rather than model math — in an early build the actual linear-attention recurrence was only 2% of the attention half. That is a concrete, reproducible case study for anyone optimizing LLM serving on non-NVIDIA accelerators, and the open-sourced code plus rerun commands make the numbers verifiable, which matters given there is no stock AWS baseline: the latest vLLM Neuron plugin registers no GLM model and NxD Inference is in maintenance mode. Each physical NeuronCore has 28 MiB of SBUF, enough to hold a layer half's activations, recurrent state and in-flight weights, and the two physical cores of a logical core must split the weight stream to reach 672–708 GB/s versus 340–400 GB/s for one. Of the remaining 24.2 ms, 6.1 ms is the memory floor, 10.0 ms is engines busy beyond it, 4.6 ms is in-kernel waits, 2.8 ms is exposed collectives and 0.7 ms is idle; the authors also note that seam-fusing compiler-overlapped work and isolated microbenchmarks both backfired, and that three kernels passed the NKI simulator but produced wrong answers on device.

reddit · r/MachineLearning · /u/WildCard727 · Nov 4, 21:47

**Background**: AWS Trainium2 is Amazon's custom AI accelerator; a trn2.48xlarge instance bundles many NeuronCores, each with fast on-chip SRAM called SBUF (28 MiB per physical core) backed by larger but slower HBM. NKI (Neuron Kernel Interface) is a low-level programming interface that gives direct access to NeuronCore hardware primitives and instructions, letting developers hand-write kernels instead of relying on the XLA-based compiler to fuse operations. A megakernel approach merges many small operations into one long-running kernel so that the working set stays on chip and costly kernel-launch boundaries and HBM write-backs are avoided — the same idea popularized on GPUs by Mirage and Hazy Research, and by AMD's per-layer decode kernels in vLLM. Mixture-of-experts (MoE) models activate only a subset of parameters per token, so decode is often memory-bandwidth-bound, which is why the 6.1 ms memory floor matters here.

<details><summary>References</summary>
<ul>
<li><a href="https://awsdocs-neuron.readthedocs-hosted.com/en/latest/nki/index.html?trk=article-ssr-frontend-pulse_little-text-block">Neuron Kernel Interface ( NKI ) — AWS Neuron Documentation</a></li>
<li><a href="https://awsdocs-neuron.readthedocs-hosted.com/en/latest/nki/get-started/about/memory-hierarchy-overview.html">The Trainium Memory Hierarchy — AWS Neuron Documentation</a></li>
<li><a href="https://www.spheron.network/blog/compile-your-llm-into-a-megakernel-a-reproducible-mirage-set/">LLM Inference Latency Optimization Technique... | Spheron Blog</a></li>

</ul>
</details>

**Tags**: `#ML systems`, `#inference optimization`, `#AWS Trainium`, `#mixture-of-experts`, `#kernels`, `#LLM serving`

---

<a id="item-10"></a>
## [NIKKE PC launcher alleged to be trojanized in supply chain attack](https://github.com/WormW/nikke_malware_analysis) ⭐️ 8.0/10

Players and independent researchers allege that the official CDN files loaded by the PC launcher for Goddess of Victory: NIKKE were replaced with a loader that downloads and executes a remote-access trojan. The reported payload contains 19 commands, allowing arbitrary command execution, screen capture, and theft of developer and AI-tool credentials plus data from 28 crypto wallet browser extensions. This is a concrete real-world supply chain compromise reaching users through a publisher's own official distribution channel, so simply installing and launching a legitimate game was enough to be exposed. Because the payload targets developer credentials, AI-tool tokens, and crypto wallets, the blast radius extends well beyond gamers to anyone who runs the launcher on a work machine. Level Infinite reportedly replaced the two modified files on November 3 but has not issued a public statement, and players can check their own machines by searching debug.log for the string "k2f_chan". Researchers recommend not launching the PC version until the vendor responds, and the full technical write-up is published in a public GitHub analysis repository.

telegram · zaihuapd · Nov 4, 07:00

**Background**: A supply chain attack compromises a trusted vendor's code, build process, or update channel so that victims install malware believing it comes from a legitimate source. A remote-access trojan (RAT) is malware that gives an attacker remote control over the victim's machine, often including file access, command execution, and data exfiltration. Here the compromised link in the chain is the game launcher's CDN-hosted update files, which are trusted by both the launcher and the user.

<details><summary>References</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/defender-endpoint/malware/supply-chain-malware">Supply chain attacks - Microsoft Defender for Endpoint</a></li>
<li><a href="https://www.crowdstrike.com/en-us/cybersecurity-101/cyberattacks/supply-chain-attack/">What Is a Supply Chain Attack? Types, Examples, and Prevention</a></li>
<li><a href="https://www.kaspersky.com/resource-center/definitions/what-is-a-rat-remote-access-trojan">What is a Remote Access Trojan ( RAT )? A Cybersecurity Guide</a></li>

</ul>
</details>

**Tags**: `#supply-chain-attack`, `#malware`, `#security-incident`, `#credential-theft`, `#gaming`

---

<a id="item-11"></a>
## [Residential Proxy Exits Detected on White House-Attributed IP Space](https://layer3intel.com/blog/residential-proxies-white-house-network) ⭐️ 7.0/10

Layer3Intel, a security firm, published a report claiming it detected residential proxy exit nodes on IP address space attributed to the White House network, with most activity occurring late in the evening Eastern time. If the attribution holds, the finding suggests a device on a high-value government network may be infected with proxy SDK software and enrolled in a residential proxy botnet, which would raise serious operational-security concerns. It also illustrates how IP-ownership data can fuel strong claims without proving which physical device or person is responsible. The report says about half of the activity falls between 5 p.m. and midnight Eastern and almost none in the early morning, which it interprets as one person rather than a public guest Wi-Fi network. However, the data only shows proxy exits, not the underlying device, and ASN ownership is a routing attribution signal rather than proof of physical location.

hackernews · Rasbora · Nov 4, 20:45 · [Discussion](https://news.ycombinator.com/item?id=50371246)

**Background**: A residential proxy routes traffic through an ordinary ISP-assigned household IP address, often by bundling proxy SDKs into apps or compromised devices, so requests appear to come from real users rather than data centers. The exit node is the final hop whose IP address the destination website records, while ASN ownership identifies the organization operating an IP range but not the individual device or person using it.

<details><summary>References</summary>
<ul>
<li><a href="https://geekflare.com/guides/what-is-residential-proxy/">What Is a Residential Proxy? - Geekflare</a></li>
<li><a href="https://proxy.wiki/glossary/exit-node/">What is an exit node? - proxy.wiki</a></li>
<li><a href="https://nhimg.org/glossary/asn-ownership/">What Is ASN Ownership? Definition & Examples - nhimg.org</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely skeptical of the attribution, noting that the report only identifies who owns the IP space and cannot physically tie the traffic to the White House; it could be a security lab, a media guest network, or another device on that range. Some also warned that compromised devices could later be tasked with less benign command-and-control activity, while one commenter reported their T-Mobile 5G IP being falsely listed as a residential proxy.

**Tags**: `#security`, `#privacy`, `#residential-proxies`, `#networking`, `#attribution`

---

<a id="item-12"></a>
## [Ripple-65B Preview Claims U.S. Open-Weight SOTA on Agentic Coding](https://www.ricursive.com/ripple) ⭐️ 7.0/10

Ricursive released a preview of Ripple-65B, a U.S.-made open-weight 65B dense language model that the company claims achieves state-of-the-art results on agentic coding benchmarks. The release drew a 186-point Hacker News discussion with 62 comments that scrutinized the narrow scope of the "SOTA" claim. A competitive open-weight model from a U.S. company adds another option to a field increasingly dominated by Chinese open-weight releases such as Qwen, and matters specifically for teams legally barred from using models outside U.S. jurisdiction. However, the narrow benchmark scope and the absence of comparisons to other open-weight models limit how much the claim tells us about real-world competitiveness. Commenters noted Ripple-65B scores 80.5 on Terminal Bench 2.1, versus 84.3 for the larger but cheaper-to-run MoE-based Qwen 3.8 Flash Next and 73.0 for Qwen 3.8-27B. Because it is a 65B dense model, inference on consumer-grade hardware will be prohibitively slow, and the company's stated mission of automating chip design suggests the model is aimed at internal workloads rather than local hobbyist use.

hackernews · Philpax · Nov 4, 18:53 · [Discussion](https://news.ycombinator.com/item?id=50369925)

**Background**: "Open-weight" means the downloadable model parameters are published, but training code, data and license terms may not meet the Open Source Initiative's definition of open source, which affects whether you can legally redistribute or build products on the model. "Dense" refers to a standard transformer where every parameter is activated for each token, in contrast to Mixture-of-Experts (MoE) models that route each token through only a subset of expert networks, making MoE models cheaper and faster to run at a given total parameter count. Agentic coding benchmarks such as Terminal Bench measure whether a model can complete multi-step tasks using tools, terminals and software interfaces rather than just answering chat prompts.

<details><summary>References</summary>
<ul>
<li><a href="https://www.promptquorum.com/local-llms/open-weight-vs-open-source-ai-models">Open Weight vs Open Source AI Models 2026: Key Differences</a></li>
<li><a href="https://www.vincirufus.com/en/posts/dense-models-vs-mixture-of-experts/">Dense vs MoE - Choosing Between Dense Models and Mixture of ...</a></li>
<li><a href="https://benchlm.ai/agentic">Best LLMs for Agentic — November 2026 Leaderboard</a></li>

</ul>
</details>

**Discussion**: The Hacker News reaction was congratulatory but sharply skeptical: one commenter mocked how far the term "SOTA" has been diluted by narrowing its category to U.S.-made open models of a certain size, and another called it a bad look that the release did not even mention competing open-weight models. Several commenters focused on practicality, arguing a 65B dense model will be too slow for consumer hardware and thus hard to gain traction with local-model enthusiasts, while others noted the U.S.-jurisdiction angle is a genuine and non-trivial differentiator.

**Tags**: `#open-weight-models`, `#agentic-coding`, `#LLM-benchmarks`, `#model-releases`, `#hackernews-discussion`

---

<a id="item-13"></a>
## [Nvidia RTX Spark Laptops Hit 35% AI Inference Speed on Linux Due to Encrypted Firmware](https://www.mindstudio.ai/blog/linux-nvidia-rtx-spark-laptop) ⭐️ 7.0/10

A hands-on test by Alex Ziskind on an MSI Prestige laptop built on Nvidia's RTX Spark platform found that under Linux the GPU is pinned at roughly 780 MHz, versus over 2 GHz on Windows, so local LLM inference runs at only about 35% of Windows speed. The throttle traces to encrypted power-management firmware on the machine that the current Linux driver has no way to negotiate with. For developers who buy these "AI PC" laptops specifically for local inference, Linux — the default environment for most AI tooling — is effectively a second-class citizen, which undercuts the core pitch of on-device AI. It also feeds the long-running debate over Nvidia's proprietary driver stack and vendor lock-in now that its hardware is the de facto standard for AI workloads. The slowdown shows up when the laptop is plugged in, since the firmware governs the power and thermal budget that decides clock behavior, and there is reportedly no workaround until Nvidia ships the necessary logic in its Linux driver. Caveats worth noting: the test covers a single MSI model, and community members stress this looks like missing Linux driver support for Windows-targeted firmware rather than deliberate encryption to block Linux.

hackernews · novaRom · Nov 4, 08:46 · [Discussion](https://news.ycombinator.com/item?id=50362905)

**Background**: RTX Spark is Nvidia's new laptop platform marketed for running local AI models, and these machines currently ship with Windows only. On modern laptops, dynamic clock boosts and power limits are managed by embedded controller firmware that the operating system's GPU driver must negotiate with; Windows drivers know how to do this for RTX Spark, while the Linux side does not yet, which is why the GPU stays at a safe low clock. For users who need Linux tooling on this hardware, WSL (Windows Subsystem for Linux) is currently the practical fallback.

<details><summary>References</summary>
<ul>
<li><a href="https://www.mindstudio.ai/blog/linux-nvidia-rtx-spark-laptop">Linux on the Nvidia RTX Spark Laptop: What Actually Works</a></li>
<li><a href="https://emergent.sh/news/rtx-spark-linux-ai-performance-capped-35">RTX Spark Linux AI Performance Capped at 35% of Windows</a></li>
<li><a href="https://github.com/Th0rgal/awesome-rtx-spark">GitHub - Th0rgal/awesome-rtx-spark: Independent community ...</a></li>

</ul>
</details>

**Discussion**: The discussion (576 points, 266 comments) pushes back hard on the framing: the top reply argues the article's own details show this is missing Linux driver support for Windows-targeted firmware, not intentional encryption, and notes RTX Spark is brand new and ships Windows-only. Others blame Nvidia's proprietary closed drivers and its monopoly position, warn that cloud-dependent, centralized AI makes the case for "sovereign AI" more urgent, and one commenter questions why the first test used the brand-new Omarchy distro rather than a long-established one.

**Tags**: `#Nvidia`, `#Linux`, `#firmware`, `#proprietary drivers`, `#AI hardware`

---

<a id="item-14"></a>
## [OpenAI to acquire Pierre Computer, maker of Codex's diff and tree libraries](https://openai.com/index/openai-to-acquire-pierre/) ⭐️ 7.0/10

OpenAI announced that it will acquire Pierre Computer Company, Inc., the startup behind Code Storage and a family of open-source developer tools, including the Trees and Diffs libraries that already power file browsing and change review inside OpenAI's Codex app. Pierre was founded by original Bootstrap creators Jacob Thornton and Mark Otto, and OpenAI did not disclose the purchase price or terms. The deal signals that OpenAI is buying up the plumbing of code review and repository-scale tooling rather than only building models, which matters for any developer whose workflow runs through Codex or competing AI coding agents. It also continues a pattern of large AI labs absorbing small, respected developer-tool teams, tightening their grip on the interfaces where code gets written and reviewed. Pierre's Diffs library is an open-source diff and code rendering library built on Shiki for syntax highlighting and theming, and it handles the performance-heavy problem of rendering very large code diffs. OpenAI framed the acquisition around Pierre's low-level, composable infrastructure for "machine work," but it has not said whether the open-source libraries will remain public or how the team will be structured, and financial terms were not disclosed.

hackernews · itunpredictable · Nov 4, 15:21 · [Discussion](https://news.ycombinator.com/item?id=50366863)

**Background**: Pierre Computer Company describes itself as producing low-level, composable product infrastructure for machine work, and its Diffs library is widely used by other developers building code review interfaces. Its founders, Jacob Thornton and Mark Otto, created Bootstrap, the enormously popular front-end CSS framework that shaped how a generation of web UIs were built. OpenAI's Codex is its AI coding product, which needs robust primitives for displaying file trees and diffs accurately at scale. Acquiring the team behind those primitives lets OpenAI own a layer of the coding experience that it previously licensed or integrated from outside.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/openai-to-acquire-pierre/">OpenAI to acquire Pierre Computer Company, Inc.</a></li>
<li><a href="https://diffs.com/">Diffs, from Pierre</a></li>
<li><a href="https://news.ycombinator.com/item?id=50366863">OpenAI to acquire Pierre Computer Company | Hacker News</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters linked the deal to OpenAI's earlier "Scaling Git at OpenAI" engineering work and noted that HashiCorp founder Mitchell Hashimoto is a vocal fan and reportedly an investor in Pierre. Others joked about needing a term for buying a whole company because it is cheaper than the subscription, speculated that the real motive is acqui-hiring talent or harvesting training data on how developer tools are built, and observed that even strong teams in dev tooling struggle to turn a profit in that market.

**Tags**: `#openai`, `#acquisitions`, `#developer-tools`, `#bootstrap`, `#industry-news`

---

<a id="item-15"></a>
## [Verification Is Not Knowledge: Essay Asks What AI Can Add to Science](https://blog.cosmos-institute.org/p/verification-is-not-knowledge) ⭐️ 7.0/10

A Cosmos Institute blog essay titled "Verification Is Not Knowledge" argues that checking whether an answer is correct is fundamentally different from actually gaining scientific knowledge, drawing on examples from both science and mathematics to probe what AI can and cannot contribute to human understanding. The piece drew a substantial Hacker News discussion that broadened into debates about proof, epistemology, and AI-driven research output. As AI systems become capable of producing correct answers and even machine-checkable proofs at scale, the essay asks whether science's real goal is answers or understanding — a question that directly affects how research is evaluated, funded, and taught. It lands amid growing concern that AI-accelerated paper production could reward volume over genuine insight. The piece is a philosophical commentary rather than a technical breakthrough or new empirical result, and it leans heavily on historical cases such as Kepler's laws, which were adopted by astronomers for their computational convenience long before Newton supplied the underlying physical explanation. Its central distinction is between verification (confirming an answer) and understanding (knowing why it is true and how it fits into a broader framework).

hackernews · ersinesen · Nov 4, 09:01 · [Discussion](https://news.ycombinator.com/item?id=50363019)

**Background**: Epistemology is the branch of philosophy concerned with what knowledge is, how it is justified, and how it differs from mere true belief — so a verified answer can be true without anyone understanding it. Kepler's laws of planetary motion describe how planets orbit the Sun with simple mathematical relationships, but Kepler himself could not explain the force behind them; that came with Newton's law of gravitation. The debate matters now because large language models and automated theorem provers can generate or check results faster than humans can interpret them, raising the question of whether science accumulates knowledge or only verified statements.

**Discussion**: Commenters largely agreed with the essay's thrust while extending it in different directions. One noted that Kepler's models were adopted before anyone understood why they worked, simply because the math was easier; another contrasted AI with mathematicians like Peter Scholze, who generate understanding rather than mere proofs; a third compared AI to a calculator that can leapfrog to answers, echoing a schoolroom demand to show your work. A more skeptical commenter doubted academia still cares, describing professors churning out one to three AI-assisted papers a month to capture grant money.

**Tags**: `#science`, `#epistemology`, `#AI`, `#mathematics`, `#philosophy`

---

<a id="item-16"></a>
## [Hydrogen-1.0: open-weight science model beats GPT-6 Astra on FrontierScience](https://www.reddit.com/r/MachineLearning/comments/1xnjhdd/hydrogen10_openweight_scientific_model_beats_gpt6/) ⭐️ 7.0/10

Deep Principle released Hydrogen-1.0, an open-weight model post-trained from GLM-5.3 for chemistry, materials science, and life sciences, reporting a 38.3% pass rate on FrontierScience Research versus 33.3% for GPT-6 Astra at max thinking — a 5 percentage point lead. The team also reports 92.9% on GPQA Diamond (just under Kimi K3's 93.5%) and an estimated output-side cost of $0.25 per FSR problem versus $0.88 for Astra, about 72% lower under their evaluation setup. If the numbers hold up, a relatively small open-weight model post-trained on scientific workflows can match or beat a frontier closed model on research-level science tasks at roughly a quarter of the inference cost, which matters for academic labs and smaller biotech or materials companies with tight compute budgets. It also signals a broader shift toward domain-specialized post-training on top of open base models rather than competing on general-purpose scale alone. All figures are self-reported from the vendor's own evaluation setup and have not been independently validated, and Hydrogen actually trailed Astra on NMR structure elucidation by 3.33 points. The five showcased workflows are selected model-plus-tool walkthroughs rather than an autonomous-research success rate — GROMACS performs the molecular dynamics calculations and the 12-vial Suzuki coupling protocol validation is virtual, meaning no physical experiment was run.

reddit · r/MachineLearning · /u/AKAMA199 · Nov 4, 09:00

**Background**: Hydrogen-1.0 is post-trained from GLM-5.3, the open-weight flagship model from Z.ai released under an MIT license with a 1M-token context window, using supervised fine-tuning and reinforcement learning on lab records, scientist feedback, and recorded discovery trajectories. FrontierScience is a benchmark from OpenAI split into an Olympiad set of 100 olympiad-level questions and a harder Research split that tests research-grade scientific reasoning. GPQA Diamond is the 198-question hardest subset of GPQA, on which PhD-level experts score about 65% while skilled non-experts with web access reach only about 34%.

<details><summary>References</summary>
<ul>
<li><a href="https://openlm.ai/glm-5.3/">GLM-5.3 - openlm.ai</a></li>
<li><a href="https://openai.com/index/frontierscience/">Evaluating AI’s ability to perform scientific research tasks | OpenAI</a></li>
<li><a href="https://epoch.ai/benchmarks/gpqa-diamond">GPQA Diamond - epoch.ai</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#open-weight models`, `#scientific ML`, `#benchmarks`, `#chemistry`

---

<a id="item-17"></a>
## [Looped Transformers Like Huginn Save Weight Storage, Not HBM Traffic, B200 Profiling Finds](https://www.reddit.com/r/MachineLearning/comments/1xnskvt/do_looped_transformers_save_hbm_traffic_profiling/) ⭐️ 7.0/10

A new profiler-backed blog post and open-source repository (dinara-dl/looped-transformer) measured the looped Huginn architecture on an NVIDIA B200 using Nsight Compute and found that reusing the same weights each iteration does not by itself cut HBM traffic. In a controlled chain of eight matmuls, sharing one 72 MiB weight instead of eight identical copies ran 24% faster and read almost nothing from HBM, but once the weight grew to 288 MiB — beyond L2 capacity — the difference disappeared, and a full eight-iteration Huginn Core (a teaching implementation with random weights) took roughly eight times as long and read roughly eight times as much HBM data as a single iteration. Looped or recurrent-depth transformers are usually pitched as parameter-efficient and therefore cheaper to serve, but this experiment shows that parameter savings do not automatically translate into bandwidth savings on memory-bound inference. That distinction matters for anyone designing or deploying recurrent architectures, since HBM bandwidth rather than storage is often the real bottleneck during decoding. The result hinges on L2 cache capacity: a 72 MiB shared weight can stay resident on chip between iterations, while a 288 MiB weight exceeds L2 and is streamed from HBM again every loop. The author cautions that this is a single-GPU case study on a teaching implementation with random weights rather than a trained model, and explicitly asks whether persistent kernels or similar techniques could keep recurrent weights on chip across iterations.

reddit · r/MachineLearning · /u/2dayyy6 · Nov 4, 16:26

**Background**: Looped transformers such as Huginn (from Geiping et al.) reuse the same block of weights across multiple iterations of computation, trading depth of unique parameters for repeated latent computation; Huginn has been trained with up to 32 loops and scaled to 64 loops at test time. GPUs have two relevant tiers of memory: large but relatively slow high-bandwidth memory (HBM) measured in tens or hundreds of gigabytes, and a small, very fast on-chip cache (L2/SRAM). Whether weight sharing actually saves time therefore depends on whether the shared weights fit in cache, and Nsight Compute is NVIDIA's tool for measuring exactly how many bytes a kernel moves from HBM.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gmicloud.ai/en/blog/flashattention-inference-speedup">FlashAttention: Fixing the Memory Wall | GMI Cloud</a></li>
<li><a href="https://www.lesswrong.com/posts/PLisnSFir8y5AHkmP/how-concerned-should-we-be-about-astra-s-recurrent">How concerned should we be about Astra's recurrent architecture ?</a></li>
<li><a href="https://docs.nvidia.com/nsight-compute/ProfilingGuide/index.html">2. Profiling Guide — NsightCompute</a></li>

</ul>
</details>

**Tags**: `#looped-transformers`, `#HBM-bandwidth`, `#GPU-memory`, `#profiling`, `#efficient-inference`

---

<a id="item-18"></a>
## [Tencent Releases Hunyuan Hy3: 295B MoE Model Halves Hallucinations](https://t.me/zaihuapd/44906) ⭐️ 7.0/10

Tencent officially launched the Hunyuan Hy3 model, less than three months after the Hy3 preview version arrived in late April. Hy3 is a Mixture-of-Experts model with 295B total parameters but only 21B active parameters, a 256K-token context window, and vendor claims of a halved hallucination rate and a task resolution rate of 90%. The release adds a strong sparse-architecture entrant to China's frontier model race, with Tencent claiming Hy3 leads among same-size models and can match larger flagship models. In a blind test by 270 internal experts on real work scenarios, Hy3 scored 2.67/4 versus 2.51/4 for Zhipu's GLM5.1, with especially large gaps in front-end development, data storage, and CI/CD. The efficiency story is the headline number: 21B active parameters out of 295B total means inference touches only about 7% of the model's weights per token, keeping serving costs far below a dense model of comparable total size. All performance figures — including the 90% task resolution rate and the blind-test comparison against GLM5.1 — are vendor-reported and internal, with no independent benchmark or public leaderboard verification described.

telegram · zaihuapd · Nov 4, 07:33

**Background**: A Mixture-of-Experts (MoE) model splits the transformer's feed-forward layers into many parallel "expert" subnetworks plus a router, and each token is only sent to a few experts while the rest of the parameters stay dormant. This decouples total parameter count from per-token compute, so a model can hold a very large knowledge capacity while costing roughly as much to run as a much smaller dense model — which is why Chinese labs have collectively shifted toward sparse architectures. The 256K context window refers to how many tokens the model can hold in a single conversation, a scale now common among frontier models and important for long-document and agentic coding work. GLM5.1, the comparison baseline here, is Zhipu (Z.ai)'s open-weight model line aimed at complex code and long-horizon tasks, and its published Hugging Face release lists 754B parameters — more than double Hy3's 295B, which is what makes the head-to-head framing notable.

<details><summary>References</summary>
<ul>
<li><a href="https://baike.baidu.com/item/混合专家模型/65370159">混合专家模型 - 百度百科</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-5.1">zai-org/GLM-5.1 · Hugging Face</a></li>
<li><a href="https://docs.bigmodel.cn/cn/guide/models/text/glm-5.1">GLM-5.1 - 智谱AI开放文档</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#Tencent Hunyuan`, `#MoE`, `#model release`, `#benchmarks`

---

<a id="item-19"></a>
## [Alipay and Partners Launch ACT Protocol, China's First AI Agent Commerce Trust Framework](https://t.me/zaihuapd/44909) ⭐️ 7.0/10

On January 16, Alipay, together with Qwen App (千问 App), Taobao Flash Sale (淘宝闪购) and other partners, released the ACT Protocol (Agent Collaboration & Trust Protocol), billed as China's first open technical framework designed specifically for AI-agent commerce. The protocol lets users complete price comparison, coupon collection and payment through natural conversation in apps such as Qwen App, enabling cross-platform automated shopping. If it gains adoption, ACT could become a shared "common language" between AI assistants and e-commerce or life-service platforms, defining how autonomous agents transact on a user's behalf across systems and organizations. That makes it a potential building block for the emerging agentic-commerce ecosystem, affecting merchants, platforms and payment providers that need a common trust and authorization layer. Alipay says it has built four core infrastructure standards under the protocol so that AI execution flows are traceable and verifiable and that payment always stays user-initiated or user-authorized, while also lowering the cost for merchants to integrate. The announcement itself is light on technical specifics — no public spec details, SDK availability or a full list of launch partners beyond Qwen App and Taobao Flash Sale were disclosed.

telegram · zaihuapd · Nov 4, 08:45

**Background**: Agentic commerce describes a new form of e-commerce in which semi-autonomous or fully autonomous AI agents search for products, compare options and complete purchases on a user's behalf, rather than a human clicking through each step. For that to work with real money, agents need a trust layer that proves who authorized a transaction, what the agent actually did, and how it can be audited afterwards. Qwen App is Alibaba's AI assistant front end, Alipay is Ant Group's dominant Chinese payment platform, and Taobao Flash Sale is an e-commerce channel — so the ACT Protocol is essentially an attempt to wire those pieces together with standardized authorization and traceability rules.

<details><summary>References</summary>
<ul>
<li><a href="https://www.act-protocol.com/">智能体商业信任协议 | ACT Protocol 面向智能体商业的开放协议框架</a></li>
<li><a href="https://www.aibase.com/news/24679">Alipay Launches ACT Protocol, Establishing China's First AI ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agentic_commerce">Agentic commerce</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#agentic commerce`, `#payment protocols`, `#Alipay`, `#e-commerce`

---

<a id="item-20"></a>
## [Huawei Tells Ascend 960DT Customers to Source Samsung, SK Hynix HBM Themselves](https://thenextweb.com/news/huawei-hbm-smuggling-samsung-sk-hynix-ascend-960dt) ⭐️ 7.0/10

The Information reported that Huawei has told some customers its next-generation flagship AI chip, the Ascend 960DT, will rely mainly on Samsung and SK Hynix HBM, and that customers must secure the memory themselves because Chinese HBM capacity is insufficient. This arrangement underscores how U.S. export controls on HBM are constraining Huawei's AI chip ambitions even as it accelerates the 960DT toward a Q1 2027 launch, and it shifts supply-chain risk onto customers. It also signals that domestic Chinese HBM suppliers cannot yet meet demand for high-end accelerators, which is a bottleneck for China's effort to close the AI compute gap with the U.S. Reports describe HBM being soldered onto low-performance processors, declared under processor tariff codes and shipped to Hong Kong, then carried into the mainland and removed by heating; a Shenzhen chip broker said a single HBM3E module has risen from a few hundred dollars a year ago to about $4,000. Huawei has said the 960DT targets Q1 2027 and roughly doubles the compute of its predecessor.

telegram · zaihuapd · Nov 4, 14:52

**Background**: HBM (High Bandwidth Memory) is a type of 3D-stacked DRAM developed by Samsung, AMD and SK Hynix that delivers far higher bandwidth than conventional memory and is a key component of AI accelerators. Since 2024, U.S. export controls have restricted sales of advanced HBM to China, prompting Beijing to pour subsidies into domestic memory development. Huawei's Ascend chips are its answer to Nvidia's GPUs in China, and the 960DT is its next flagship aimed at closing the computing gap.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/09/17/huawei-plans-q1-2027-launch-of-new-ai-chip-as-it-takes-on-nvidia/">Huawei plans Q1 2027 launch of new AI chip as it takes on ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#AI chips`, `#HBM`, `#export controls`, `#supply chain`

---

<a id="item-21"></a>
## [Cloudflare adds analytics and tiered controls for personal AI agents](https://blog.cloudflare.com/personal-agents-visibility-control/) ⭐️ 7.0/10

Cloudflare launched analytics for personal AI agent traffic, adding a new "Personal Assistants" category to its bot analytics chart and a new Top statistics component that breaks down request counts, paths, and status codes per agent. On the control side, the former "Configure AI bot policies" setting is now called "AI Crawler and Agent access policies" and lets site owners set per-agent actions for the top personal agents: allow, block only on ad-bearing pages, or block. Personal agents browse and fetch content on a real person's behalf, so they sit ambiguously between a human visitor and an automated bot, and until now site operators had little visibility into that traffic. Giving publishers and site owners per-agent analytics plus tiered blocking options lets them distinguish monetizable human-driven visits from unwanted automation, which matters for ad-supported sites whose inventory can be consumed by agent traffic. The granular actions apply to individually selectable top personal agents, while existing Search and Training policies remain unchanged, and sites that have enabled Account Abuse Protection can additionally see which end user an agent is acting for. According to Cloudflare's documentation, free-plan detection of AI crawlers relies on self-identifying user-agent strings, while more thorough detection via Cloudflare's Bot Management detection ID requires an upgraded plan.

telegram · zaihuapd · Nov 4, 15:42

**Background**: Cloudflare is a major content delivery network and web security provider that sits in front of a large share of the web, so its bot management settings shape how much automated traffic sites receive. Historically bot controls focused on search engine crawlers and scrapers, but AI has split automated traffic into distinct categories — search, training, and agents that act in real time on a person's behalf, such as chat-fetch bots and browser-use agents. Cloudflare's July 1, 2026 AI traffic policies separated these Search, Agent, and Training behaviors; this release extends that framework with visibility and per-agent controls for the personal-agent category.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.cloudflare.com/bots/additional-configurations/block-ai-bots/">AI Crawler and Agent access policies · Cloudflare bot ...</a></li>
<li><a href="https://community.cloudflare.com/t/bots-granular-access-controls-for-the-top-personal-agents/976315">Bots - Granular access controls for the top Personal Agents</a></li>
<li><a href="https://www.unite.ai/cloudflare-adds-personal-agent-analytics-and-per-agent-access-controls/">Cloudflare Adds Personal Agent Analytics and Per-Agent Access ...</a></li>

</ul>
</details>

**Tags**: `#Cloudflare`, `#AI agents`, `#bot management`, `#web analytics`, `#access control`

---

<a id="item-22"></a>
## [AMD Expects to Outsell Intel in Q4 for the First Time in History](https://www.tomshardware.com/pc-components/cpus/amd-expects-to-outsell-intel-in-q4-for-the-first-time-in-history-usd17b-guidance-would-exceed-intels-projections) ⭐️ 6.0/10

AMD has issued Q4 guidance of roughly $17 billion, a figure that would exceed Intel's own quarterly projections and mark the first time in history that AMD out-sells Intel in a quarter. The growth is driven largely by datacenter demand, particularly sales of AMD's Instinct accelerators alongside its Epyc server CPUs. This is a symbolic milestone for a company that spent most of the 2010s as the perennial underdog in x86 CPUs, and it reflects how AI-driven datacenter spending has reshuffled the semiconductor landscape. It signals real pressure on Intel's core server business, which has historically been its most profitable franchise. The comparison is based on company guidance and revenue, not unit shipments or retail market share — commenters note Intel still undercuts AMD on desktop processor pricing. AMD's Instinct accelerator sales are still small relative to Nvidia's datacenter GPUs, so the datacenter CPU business and Intel's own weakness are the bigger factors.

hackernews · rbanffy · Nov 4, 15:38 · [Discussion](https://news.ycombinator.com/item?id=50367125)

**Background**: AMD and Intel have competed for decades in the x86 processor market, with Intel holding a dominant share of both consumer PCs and servers. AMD's Zen architecture, launched in 2017, let it regain competitiveness in servers via the Epyc line, while its Ryzen chips chipped away at Intel's desktop lead. In parallel, the AI boom has shifted the balance of datacenter spending toward accelerators, an area where Nvidia leads but where AMD is trying to establish a foothold with Instinct.

**Discussion**: Hacker News commenters were skeptical of reading too much into the milestone, arguing it says more about Intel's missteps — such as abandoning Optane, which one commenter says could have helped with MoE offloading and KV-cache storage — than about AMD's execution. Others raised privacy and security concerns about Intel's DCI and AMD's PSP management engines, noted that Intel still undercuts AMD on retail desktop pricing, and pointed out that AMD's Instinct sales remain tiny next to Nvidia's.

**Tags**: `#AMD`, `#Intel`, `#CPU market`, `#semiconductors`, `#datacenter`

---

<a id="item-23"></a>
## [Researcher Urges Top AI Conferences to Desk-Reject AI-Generated Papers](https://www.reddit.com/r/MachineLearning/comments/1xnkbeu/a_message_to_top_tier_conferences_d/) ⭐️ 6.0/10

A researcher posting on r/MachineLearning described attending two CORE A/A* AI conferences where presenters could not explain their own work — one reportedly paused five minutes before answering that a knowledge graph was represented "with a vector," and another openly typed questions into ChatGPT and read the replies on stage. The same post alleged that one author published identical papers at two AI conferences simultaneously with fabricated data, and left the LLM chat prompts visible in a public GitHub repository, prompting the author to demand stricter desk-rejection rules for AI-written submissions. Although the post is anecdotal and names no venues, it taps into a fast-growing worry that LLM-assisted writing and fabricated results are slipping past peer review at the field's most prestigious ML conferences, which would both displace legitimate work and erode trust in published AI research. The concern matters to authors whose papers are rejected, to reviewers and program chairs who must police submissions, and to anyone who relies on conference proceedings as a record of scientific progress. The post offers no concrete evidence, no venue names, no dates, and no specific policy proposal beyond asking conferences to "be hard" on desk rejections; it also conflates several distinct problems — LLM-written prose, fabricated data, dual submission, and presenter incompetence. For context, desk rejection is already a standard filtering step (journals commonly reject 30%–70% of submissions at this stage), and conferences are beginning to experiment with AI-content detectors such as Pangram and Copyleaks, though such tools remain unreliable and contested.

reddit · r/MachineLearning · /u/Vegetable-Formal-753 · Nov 4, 09:55

**Background**: In computer science, conference rankings such as CORE's A*/A/B/C tiers are widely used to judge venue prestige, and "A*" denotes the top tier; in ML, conferences like NeurIPS, ICML, and CVPR are the primary publication venues, so acceptance there carries heavy career weight. Desk rejection is a pre-review screening step in which editors or chairs return a submission without sending it to reviewers, typically for scope violations, formatting problems, or ethical issues like dual submission. Knowledge graphs are graph-structured representations of entities and relations, so describing one as stored "with a vector" is a notable red flag to anyone familiar with the area.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aischolar.com/news/article/is-desk-rejection-common">Is Desk Rejection Common?</a></li>
<li><a href="https://hub.paper-checker.com/blog/ai-detection-academic-conferences-paper-presentation-verification-2026/">AI Detection for Academic Conferences : Paper and Presentation...</a></li>
<li><a href="https://www.core.edu.au/conference-portal">CORE Rankings Portal - core.edu.au Core Conference Ranking/Rating | Top Conferences, Workshops ... Top AI Conferences 2026: Best ML, Robotics & GenAI Events ... 2026 Conference Rankings | CORE, Qualis & ERA Search Tool Top Computer Science & AI Conferences (2026–2027): CORE A* ...</a></li>

</ul>
</details>

**Tags**: `#academic-integrity`, `#peer-review`, `#machine-learning`, `#conferences`, `#llm-abuse`

---

<a id="item-24"></a>
## [Reddit post asks why CVPR allows 25 submissions per author](https://www.reddit.com/r/MachineLearning/comments/1xnscvr/why_cant_conferences_just_reasonably_reduce_the/) ⭐️ 6.0/10

A Reddit r/MachineLearning post by user /u/mofoss questions why CVPR's 2027 author guidelines allow each author to submit up to 25 papers — a limit carried over from CVPR 2026 — arguing that such a generous cap invites AI-generated "slop" papers and gaming of careless reviewers. The poster proposes limiting first-author submissions to 2-3 papers instead, so that authors invest more care in each submission and reviewer load drops. The thread taps into a growing anxiety that the submission pipeline at top ML venues is being flooded faster than volunteer reviewers can handle, eroding review quality and, by extension, the signal value of an A* publication. If conferences tighten submission caps, the change would directly affect how labs, PhD students and career-driven authors plan their publishing strategies. Under the quoted CVPR policy, submissions beyond the 25-paper limit are desk-rejected by the Program Chairs rather than reviewed, so the cap functions as a hard cutoff rather than a soft guideline. Notably, the limit is per author rather than per first author, and the post is an opinion argument without supporting submission or acceptance data.

reddit · r/MachineLearning · /u/mofoss · Nov 4, 16:17

**Background**: CVPR (Conference on Computer Vision and Pattern Recognition), first held in 1983 and sponsored by IEEE and the CVF, is widely regarded as the premier annual computer vision venue, and acceptance there is a heavily weighted credential in academic hiring and promotion. The term "AI slop" refers to low-quality, largely machine-generated content; researchers have begun formalizing ways to measure it, and outlets such as Nature and The Atlantic have reported that preprint servers and conference organizers are struggling to counter a tide of AI slop submissions. Because some institutions and countries tie bonuses and career advancement to A* venue stamps, incentives to maximize submission count can outweigh concerns about research ethics.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Conference_on_Computer_Vision_and_Pattern_Recognition">Conference on Computer Vision and Pattern Recognition - Wikipedia</a></li>
<li><a href="https://cvpr.thecvf.com/">2027 Conference</a></li>
<li><a href="https://www.theatlantic.com/science/2026/01/ai-slop-science-publishing/685704/">Science Is Drowning in AI Slop - The Atlantic</a></li>

</ul>
</details>

**Tags**: `#peer review`, `#ML conferences`, `#paper submissions`, `#AI slop`, `#research culture`

---

<a id="item-25"></a>
## [Anthropic Says Anti-Distillation Defenses Cut Extracted Data by 90-99%](https://t.me/zaihuapd/44911) ⭐️ 6.0/10

On October 12, Anthropic said preliminary evidence shows that its new safeguards against model-distillation attacks on Claude have reduced the amount of extracted data by roughly 90% to 99%, and that it has banned tens of thousands of related accounts — some within two hours of their first attack. Distillation attacks let third parties clone a frontier model's capabilities through the public API without ever touching its weights, so measurable defenses directly protect a lab's core IP and its pricing power. Concrete numbers like these give the industry a first public benchmark for how well API-level abuse detection can actually work, and they will shape how other labs and API-dependent developers design their own safeguards. The measures include restricting how reasoning content can flow across sessions, models and accounts, deploying dual-stage classifiers, and continuously patching bypass techniques; Anthropic reports a false-positive rate below 0.1%, though some developers will need to update their integrations and blocked requests may still be billed.

telegram · zaihuapd · Nov 4, 10:16

**Background**: A model distillation attack does not steal a model's weights or architecture: the attacker sends large volumes of carefully crafted prompts through the API, harvests the outputs, and trains a smaller 'student' model to imitate them. Because this traffic looks superficially like normal heavy usage, detection relies on signals such as extreme volume concentrated in narrow domains, highly repetitive structures, and content that maps onto the most training-valuable outputs. Attackers can also spread a single extraction effort across many sessions and accounts so that no individual request looks suspicious, which is why defenses now track behavior across sessions rather than judging each message in isolation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks">Detecting and preventing distillation attacks \ Anthropic</a></li>
<li><a href="https://repello.ai/blog/model-distillation-attack">Model Distillation Attacks , Explained: How Anthropic... | Repello AI</a></li>
<li><a href="https://arxiv.org/pdf/2604.21131">Cross-Session Threats in AI Agents: Benchmark, Evaluation ...</a></li>

</ul>
</details>

**Tags**: `#model-distillation`, `#AI-security`, `#Anthropic`, `#Claude`, `#API-abuse`

---

<a id="item-26"></a>
## [Microsoft Offers Voluntary Severance to Roughly 60,000 Employees](https://t.me/zaihuapd/44913) ⭐️ 6.0/10

Microsoft is offering voluntary severance packages to roughly 60,000 employees — vice presidents and below in the US, Canada, India and the UK — with Xbox, Windows, Copilot and Finance fully participating, while data center, sales and marketing roles are excluded. A Microsoft spokesperson said the terms are close to the company's standard severance package. The move covers roughly 27% of Microsoft's 223,000-strong workforce as of the end of June, making it one of the largest voluntary buyout programs at a major tech company in recent years. It signals that big tech is continuing to reallocate headcount and spending toward AI infrastructure while trimming mature product organizations like Xbox and Windows. The offer is voluntary rather than a formal layoff, and Microsoft notes the terms are near its standard severance, though the company has not disclosed exact amounts or how many employees it expects to accept. The exclusion of data center roles is notable, since those teams support the cloud and AI infrastructure that Microsoft is currently prioritizing; the company also offered a similar package to retirement-eligible employees in July.

telegram · zaihuapd · Nov 4, 11:46

**Background**: Large tech companies often use voluntary severance — sometimes called a buyout — as a softer alternative to layoffs: employees who leave voluntarily receive a package, and the company reduces headcount without formal redundancies, which can help morale and avoid some legal notification requirements. Microsoft's fiscal year ends on June 30, so headcount and organizational adjustments are frequently announced around mid-year. In recent years Microsoft and its peers have been redirecting capital toward AI data centers and model development while mature consumer businesses such as gaming and Windows face slower growth.

**Tags**: `#Microsoft`, `#tech-layoffs`, `#workforce-restructuring`, `#big-tech`, `#industry-news`

---