---
layout: default
title: "Horizon Summary: 2026-09-12 (EN)"
date: 2026-09-12
lang: en
---

> From 38 items, 22 important content pieces were selected

---

1. [Terry Tao Flags a 'Severe Misalignment' of AI in Mathematics](#item-1) ⭐️ 9.0/10
2. [GitLab Patches CVSS 10.0 Flaw Enabling Unauthenticated File Reads](#item-2) ⭐️ 9.0/10
3. [trynix.dev boots any Nix package in a browser VM](#item-3) ⭐️ 8.0/10
4. [Shopify drops React Native for native Swift and Kotlin, citing AI agents](#item-4) ⭐️ 8.0/10
5. [SemiAnalysis: Nvidia's Backstop Economics and the Limits of Its Balance Sheet](#item-5) ⭐️ 8.0/10
6. [Solo-GPU training of a 210M text-to-image DiT yields three novel measurements](#item-6) ⭐️ 8.0/10
7. [OpenAI Launches GPT-Live-1 Full-Duplex Speech Model in Its API](#item-7) ⭐️ 8.0/10
8. [OpenAI Launches Public Beta Agents API for Cloud Agents](#item-8) ⭐️ 8.0/10
9. [Anthropic Restricts Claude to Users Over 18 With Age Assurance](#item-9) ⭐️ 7.0/10
10. [EPA Proposes Scrapping Mandatory Public Review for Data Center Pollution Permits](#item-10) ⭐️ 7.0/10
11. [Measuring the sloppiness of code](#item-11) ⭐️ 7.0/10
12. [Datasette ships security patches after AI-assisted audit](#item-12) ⭐️ 7.0/10
13. [ACL Announces Sustainable Reviewing Policy with Submission Caps](#item-13) ⭐️ 7.0/10
14. [Anthropic Urges Global Slowdown of Frontier AI Development](#item-14) ⭐️ 7.0/10
15. [DeepSeek Releases V4.1 Flash, a 552B Multimodal Model on a New Architecture](#item-15) ⭐️ 7.0/10
16. [Anthropic Report Accuses Seven Chinese AI Labs of Large-Scale Claude Distillation](#item-16) ⭐️ 7.0/10
17. [Boris Cherny: Claude-Written Production Code Should Be Held to a Higher Bar](#item-17) ⭐️ 6.0/10
18. [Simon Willison urges Python devs not to sleep on wrapture](#item-18) ⭐️ 6.0/10
19. [China Releases First Mandatory National Safety Standard for Power Banks](#item-19) ⭐️ 6.0/10
20. [China cancels original Chang'e-8 plan, merges lunar programs](#item-20) ⭐️ 6.0/10
21. [Japan Digital Agency Breach May Expose Data of 246,000 People](#item-21) ⭐️ 6.0/10
22. [Kimi Code Ships K2.8 Preview With Near-K3 Performance](#item-22) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Terry Tao Flags a 'Severe Misalignment' of AI in Mathematics](https://mathandai.org/) ⭐️ 9.0/10

Terry Tao published a blog post titled 'A severe misalignment of AI in mathematics', arguing that current AI efforts — particularly OpenAI's approach — are misaligned with the values, norms and incentives of the mathematical community. The post was quickly amplified by an Economist article headlined 'Top mathematicians are outraged by OpenAI's methods' and by a 361-comment Hacker News discussion. The debate reframes AI in mathematics from a pure capability question into one about research ethics, credit assignment and how mathematical knowledge is verified and trusted. Because Tao is a Fields Medalist whose blog is read across the field, his framing is likely to shape how universities, journals and AI labs approach machine-generated mathematical results. The discussion centres on verification and on the 'yardstick' used to measure mathematical contribution — traditionally the solving of open problems — as well as on who receives credit when an AI system, rather than a human, produces a result. Commenters drew parallels to Mochizuki's abc conjecture proof, an isolated and famously hard-to-parse contribution that still spurred years of conferences and papers.

hackernews · meredydd · Sep 11, 17:45 · [Discussion](https://news.ycombinator.com/item?id=49662371)

**Background**: Terry Tao is a Fields Medalist and one of the most influential living mathematicians, and his blog is widely followed both inside and outside the field. 'Alignment' normally refers to making AI systems pursue the goals their users actually intend; Tao borrows the term to describe a mismatch between how AI is deployed in mathematics and the discipline's own norms. Mathematics has long relied on peer review, seminars and, more recently, interactive proof assistants and formal verification to check results, so breakthroughs asserted by automated systems raise immediate questions about who gets credit and how the claims can be checked at all.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_alignment">AI alignment - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_assistant">Proof assistant - Wikipedia</a></li>
<li><a href="https://www.mathlumen.com/articles/formal-proofs-lean-mathematics">The Formal Proof Revolution: How Lean Is Rebuilding the ...</a></li>

</ul>
</details>

**Discussion**: Sentiment in the 361-comment thread is split between cautious optimism and concern. One mathematician compares the situation to Mochizuki's abc conjecture, arguing that even an isolated, near-incomprehensible proof generated years of productive scrutiny, while another contends that AI has not destroyed mathematicians' ability to build and share understanding but rather the 'yardstick' of solving open problems used to measure contribution — and that the cat is already out of the bag regarding model capability. Others reach for analogies such as Baudelaire's 19th-century dismissal of photography as a mechanical record of what already exists, and one commenter detours into finitism as a way to escape undecidability.

**Tags**: `#AI`, `#mathematics`, `#research-ethics`, `#OpenAI`, `#academia`

---

<a id="item-2"></a>
## [GitLab Patches CVSS 10.0 Flaw Enabling Unauthenticated File Reads](https://docs.gitlab.com/releases/patches/patch-release-gitlab-19-3-2-released/) ⭐️ 9.0/10

On September 10, GitLab released emergency out-of-band patches in versions 19.3.2, 19.2.6 and 19.1.8 to fix CVE-2026-85706, a vulnerability rated CVSS 10.0. Under specific conditions, an unauthenticated user can exploit a path-constraint and authentication flaw in the code repository commits API to read arbitrary files on the GitLab server. Because self-managed GitLab instances are widely deployed in enterprises and typically store source code, CI/CD secrets and credentials, a maximum-severity, authentication-free file-read flaw means sensitive configuration and token files could be disclosed without any account. GitLab is strongly urging all self-managed administrators to upgrade immediately, making this an urgent operational priority rather than a routine patch. Affected versions are 18.7 through before 19.1.8, 19.2 before 19.2.6, and 19.3 before 19.3.2; GitLab.com has already been patched and GitLab Dedicated customers need take no action. The flaw was reported by researcher s3ntago through HackerOne, GitLab has not publicly disclosed the exact preconditions, and no reproducible public proof-of-concept or evidence of in-the-wild exploitation has appeared so far.

telegram · zaihuapd · Sep 11, 11:05

**Background**: CVSS (Common Vulnerability Scoring System) rates vulnerabilities on a 0–10 scale, where 10.0 is the maximum possible severity. GitLab is an open-source DevSecOps platform covering source control, CI/CD and security scanning, available as self-managed installations and as the hosted GitLab.com service, plus GitLab Dedicated as a single-tenant SaaS fully managed by GitLab. The commits API is a REST endpoint for listing a project's repository commits, which normally requires authentication via a private token; this vulnerability abused that endpoint's path handling to escape the intended directory scope.

<details><summary>References</summary>
<ul>
<li><a href="https://thecybersecguru.com/news/gitlab-cve-2026-85706-cvss-10-path-traversal/">GitLab CVE-2026-85706: Critical CVSS 10 . 0 Path Traversal Flaw</a></li>
<li><a href="https://docs.gitlab.com/api/commits/">Commits API | GitLab Docs</a></li>
<li><a href="https://ben.ii.pw.edu.pl/gitlab/help/administration/dedicated/index.md">Index · Dedicated · Administration · Help · GitLab</a></li>

</ul>
</details>

**Tags**: `#Security`, `#GitLab`, `#CVE`, `#Vulnerability`, `#Self-Hosted`

---

<a id="item-3"></a>
## [trynix.dev boots any Nix package in a browser VM](https://simonwillison.net/2026/Sep/10/trynix/) ⭐️ 8.0/10

Farid Zakaria launched trynix.dev, which uses the qemu-wasm project to run an x86_64 Linux virtual machine entirely inside the browser via WebAssembly, and can boot that VM with any Nix package built over the past 13 years. Packages are URL-addressable, so a link like https://trynix.dev/?pkg=python3%403.6.2 loads an interactive shell running Python 3.6.2 from 2017, and a companion GitHub Action called trynix-preview posts such a link as a comment on pull requests. This turns software archaeology and reproducible debugging into a single click: instead of recreating an old toolchain locally, a developer or reviewer can open a URL and get the exact historical package running. The trynix-preview GitHub Action extends this to code review, letting reviewers boot a PR's build in a serverless browser sandbox, which is a notable usability win for the Nix ecosystem and for reproducibility practices generally. The whole environment depends on qemu-wasm, which compiles QEMU's x86_64 system emulator to WebAssembly, so performance is emulation-bound and not comparable to a native install; users must click "Load" to trigger the boot, and the 13-year window reflects the range of packages available through Nix's binary cache and pinned revisions. The author himself calls the project his "magnum opus" of Nix work.

rss · Simon Willison · Sep 10, 23:44

**Background**: Nix is a cross-platform, purely functional package manager created by Eelco Dolstra in 2003 that installs every package into its own unique, content-addressed store path, which makes builds reproducible and lets many versions of the same software coexist. That property is what makes trynix.dev possible: because Nix can reliably rebuild and fetch exact historical revisions, the site can offer a multi-year catalogue of packages. QEMU is a general-purpose machine emulator and virtualizer, and qemu-wasm is a port of it that runs in the browser through WebAssembly, so the VM executes client-side with no backend server involved.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ktock/qemu-wasm">GitHub - ktock/ qemu - wasm : QEMU on browser · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nix_(package_manager)">Nix (package manager) - Wikipedia</a></li>
<li><a href="https://nixos.org/">Nix & NixOS | Declarative builds and deployments</a></li>

</ul>
</details>

**Tags**: `#nix`, `#webassembly`, `#qemu`, `#virtualization`, `#developer-tools`

---

<a id="item-4"></a>
## [Shopify drops React Native for native Swift and Kotlin, citing AI agents](https://simonwillison.net/2026/Sep/10/shopify-react-native/) ⭐️ 8.0/10

Shopify announced it is moving its mobile apps off React Native and back to separate native Swift (iOS) and Kotlin (Android) codebases, reversing the cross-platform migration it made in 2020. As part of the shift, its open-source libraries react-native-skia and flash-list are being handed to new maintainers, while restyle will be archived at the end of 2026 because of its smaller user base. A major e-commerce company publicly reversing a six-year React Native bet is a strong industry signal that AI coding agents may now be eroding the core economic argument for cross-platform frameworks: avoiding duplicated work. If that holds, other engineering organizations weighing React Native or Flutter adoption may reassess, with knock-on effects for the React Native ecosystem and the mobile engineers who specialize in it. Shopify is explicit that the cost of maintaining software on two platforms has not disappeared; what changed is that agents now handle enough of the implementation, translation, testing, and review work that duplication is no longer the deciding factor it was in 2020. The company also credits React Native as a good platform during its six years of use, and notes that restyle is being retired specifically because it has a smaller user base than its other libraries.

rss · Simon Willison · Sep 10, 21:11

**Background**: React Native is Meta's open-source framework that lets developers write a single JavaScript/TypeScript codebase that runs on both iOS and Android, which is why Shopify adopted it in 2020 to stop building the same features twice. Going "native" instead means writing separate apps in Swift for iOS and Kotlin for Android, which typically yields better performance and platform fidelity at the price of duplicated effort. AI coding agents are LLM-based tools that can write, port, test, and review code across languages, and the argument here is that they reduce the human cost of that duplication. Shopify maintained three widely used React Native libraries, so its exit has direct consequences for other projects that depend on them.

**Tags**: `#react-native`, `#mobile-development`, `#ai-coding-agents`, `#swift`, `#kotlin`

---

<a id="item-5"></a>
## [SemiAnalysis: Nvidia's Backstop Economics and the Limits of Its Balance Sheet](https://newsletter.semianalysis.com/p/nvidias-backstop-universe-heads-i) ⭐️ 8.0/10

SemiAnalysis published a deep-dive analysis titled "Nvidia's Backstop Universe – Heads I Win, Tails Who Loses?", examining Nvidia's backstop economics — the financing arrangements through which the chipmaker helps underwrite GPU purchases by cloud and neocloud operators — against the backdrop of an estimated $11 trillion AI infrastructure buildout. The piece focuses on how far Nvidia's own balance sheet can credibly absorb the risk it is effectively guaranteeing. The analysis matters because Nvidia is simultaneously the main supplier of AI compute and, increasingly, the financier standing behind the debt used to buy its chips, meaning its own financial health is becoming entangled with the sustainability of AI capex itself. If demand or pricing weakens, the same balance sheet that funds the buildout could be the one absorbing the losses, with consequences for neoclouds, lenders, investors, and compute pricing across the ecosystem. Related SemiAnalysis reporting notes that Nvidia takes a usage-linked revenue share — cited at roughly 25% — in the neoclouds it helps finance, and projects AI-related debt could exceed $7 trillion by 2029, a structure that echoes other circular GPU financing arrangements. Those terms raise open questions about vendor lock-in, compute pricing power, and who ultimately bears provider risk if the assets fail to generate expected revenue.

rss · Semianalysis · Sep 11, 17:04

**Background**: A "backstop" in finance is a commitment to provide last-resort capital or demand when the primary source of funding or buyers falls short, commonly used in underwriting and liquidity support. In AI, "neoclouds" are newer GPU-focused cloud providers that rent out accelerated compute but often lack the credit strength of hyperscalers, so they depend on debt and on vendor support to acquire Nvidia hardware. Nvidia's dominant position in AI accelerators, combined with an infrastructure buildout measured in trillions of dollars, has pushed it into a role that resembles that of a lender or guarantor as much as a chip supplier.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/nvidia-gpu-debt-backstop-unleashes">Nvidia GPU Debt Backstop Unleashes the AI Project Trinity ...</a></li>
<li><a href="https://www.spheron.network/blog/nvidia-neocloud-backstop-financing-circular-gpu-2026/">NVIDIA's Neocloud Backstop Financing Explained: What Circular ...</a></li>
<li><a href="https://businessmodelanalyst.com/nvidia-usage-linked-revenue-25-percent-backstop/">Nvidia’s 25% Backstop Bought a Toll Booth on Its Own Chips</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#AI infrastructure`, `#semiconductors`, `#finance`, `#AI buildout`

---

<a id="item-6"></a>
## [Solo-GPU training of a 210M text-to-image DiT yields three novel measurements](https://www.reddit.com/r/MachineLearning/comments/1wdfmvq/training_a_210m_texttoimage_dit_from_scratch_on/) ⭐️ 8.0/10

A developer trained a 210M-parameter text-to-image diffusion transformer (DiT) from scratch on a single RTX PRO 6000 GPU in 3.5 days, using 4.2M images at 256² resolution, and published three measurements rather than samples. The reported findings are that two learned key/value slots appended to cross-attention absorb roughly 90% of the cross-attention mass at mid-noise (while the usual EOS sink drops to ~4%), that flow-matching loss tracks training health rather than sample quality, and that the training-time timestep shift is worth more than doubling the number of sampling steps. It shows that meaningful diffusion-transformer research and reproducible ablations are now feasible on a single consumer-adjacent GPU rather than a cluster, lowering the barrier for independent practitioners. The attention-sink and register-token measurements also give concrete, quantitative evidence for how null slots stabilize cross-attention, which is directly relevant to anyone debugging or compressing text-conditioned diffusion models. The model uses cross-attention DiT (896 width, 16 blocks), 2D RoPE, QK-norm, SwiGLU, adaLN-single, rectified flow with logit-normal timesteps, 16 register tokens in the image stream, and five aspect-ratio buckets; its register vectors grow to 4–13× the norm of image tokens by the middle blocks. The flow-matching loss only moved 0.805 → 0.754 over the whole run while held-out FID went 33.7 → 27.0, FD-DINOv2 570 → 218, and detector-based object accuracy 65% → 90%, and at 20 sampling steps shift 2.8 gave FID 27.0 versus 27.3 with no shift (FD-DINOv2 218 vs 228), with the shift 2.8 derived from the SD3/RAE rule √(32·32·32/4096) for the 32-channel FLUX.2 latent.

reddit · r/MachineLearning · /u/IvanMikhnenkov · Sep 11, 13:00

**Background**: A diffusion transformer (DiT) is a generative model that replaces the convolutional U-Net of classic diffusion models with a transformer backbone, generating images by iteratively denoising latent representations conditioned on text. Attention sinks are tokens that absorb a disproportionate share of attention despite carrying little information; register tokens are extra, input-independent tokens (introduced in the 'Vision Transformers Need Registers' work) that give a model a dedicated place to dump such global bookkeeping, reducing artifacts. Flow matching / rectified flow trains a model to regress a velocity field along a path between noise and data, and the timestep shift is a sampling-time reweighting of noise levels (popularized by SD3) that changes how many steps are needed; FID is a standard distribution-distance metric where lower is better.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2604.10098">[2604.10098] Attention Sink in Transformers: A Survey on ...</a></li>
<li><a href="https://arxiv.org/abs/2309.16588">[2309.16588] Vision Transformers Need Registers</a></li>
<li><a href="https://arxiv.org/abs/2210.02747">[2210.02747] Flow Matching for Generative Modeling</a></li>

</ul>
</details>

**Tags**: `#text-to-image`, `#diffusion transformers`, `#attention sinks`, `#register tokens`, `#single-GPU training`

---

<a id="item-7"></a>
## [OpenAI Launches GPT-Live-1 Full-Duplex Speech Model in Its API](https://openai.com/index/introducing-gpt-live-1-in-the-api/) ⭐️ 8.0/10

On September 10, 2026, OpenAI released GPT-Live-1 in its API, a full-duplex speech model that can listen and speak simultaneously, supporting natural interruptions, background-noise handling, long conversations, and telephony voice agents. OpenAI reports that GPT-Live-1 improves by 30 percentage points over GPT-Realtime-2.1 on Full Duplex Bench, at a voice-frontend price of $0.05 per minute. This is a platform-level release for developers building real-time voice agents: full-duplex interaction removes the rigid turn-taking of cascaded speech pipelines, making assistants feel far more natural on phone lines and in live conversations. The explicit per-minute pricing also makes it easier to estimate the cost of production voice agents, which could accelerate adoption in customer service, telephony, and interactive assistants. A notable design point is that GPT-Live-1 focuses on the speech front end and can hand off complex reasoning and tool calls to a backend model, separating real-time interaction from heavy inference. The 30-point gain and the $0.05-per-minute voice-frontend price come from OpenAI's own announcement, which provides no technical detail or independent benchmark verification.

telegram · zaihuapd · Sep 11, 03:09

**Background**: Traditional voice assistants use a cascaded pipeline: speech recognition transcribes the audio, a language model generates a text reply, and text-to-speech synthesizes the answer, which means the system must wait for the user to finish before responding. Full-duplex speech models instead process incoming and outgoing audio streams at the same time, enabling behaviors like backchanneling ("mm-hmm"), pause handling, and interruption management. Full-Duplex-Bench is an academic benchmark that systematically scores these turn-taking behaviors, and GPT-Realtime-2.1 is OpenAI's previous low-latency streaming speech-to-speech model for conversational AI.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2503.04721">[2503.04721] Full-Duplex-Bench: A Benchmark to Evaluate Full-duplex Spoken Dialogue Models on Turn-taking Capabilities</a></li>
<li><a href="https://developers.openai.com/api/docs/models/gpt-realtime-2.1">GPT-Realtime-2.1 Model | OpenAI API</a></li>
<li><a href="https://getstream.io/blog/realtime-speech-language-models/">Using a Speech Language Model That Can Listen While Speaking</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#speech-model`, `#realtime-voice`, `#API-release`, `#voice-agents`

---

<a id="item-8"></a>
## [OpenAI Launches Public Beta Agents API for Cloud Agents](https://openai.com/index/introducing-the-agents-api/) ⭐️ 8.0/10

On September 10, 2026, OpenAI released the public beta of its Agents API, which lets developers create production-grade cloud agents with a single API call and choose between OpenAI-hosted sandboxes, their own infrastructure, or partner environments. The API is built on the open-source Codex harness and adds long-session context compression, tool search, parallel tool calls and sub-agent collaboration. This shifts agent development away from assembling DIY frameworks toward a first-party managed platform, potentially sparing developers much of the orchestration, sandboxing and context-management plumbing they currently build themselves. It also raises the competitive pressure on other agent platforms and open-source agent frameworks across the LLM infrastructure stack. The service supports hosted sandboxes, self-managed infrastructure or partner environments, so teams can keep code execution inside their own perimeter if they prefer. During the public beta there are no additional platform fees — users only pay for the tokens and tools their agents consume.

telegram · zaihuapd · Sep 11, 11:12

**Background**: An "agent" here means an LLM that carries out multi-step tasks on its own: it calls tools, observes the results and keeps going. Running such agents in production requires a sandbox for safe code execution, plus mechanisms for managing an ever-growing conversation history and for selecting the right tool out of many — which is why context compression, tool search and sub-agents matter. The Codex harness is the open-source agent scaffolding behind OpenAI's Codex coding agent, and this API exposes that same machinery to third-party developers.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.openai.com/blog/codex-as-a-platform">Codex as a platform: build on the open agent harness</a></li>
<li><a href="https://openai.com/index/harness-engineering/">Harness engineering: leveraging Codex in an agent-first world</a></li>
<li><a href="https://arxiv.org/abs/2510.00615">[2510.00615] ACON: Optimizing Context Compression for Long ... Context Compaction: Delete Noise, Keep Signal | Technical Guide Acon: Optimizing Context Compression for Long-horizon LLM Agents GitHub - broalantaps/Awesome-Context-Compression-LLMs: A ... How to Build Context Compression - oneuptime.com ACON: Optimizing Context Compression for Long-horizon LLM ... Context Compression for LLM Agents: A Survey of Methods ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI Agents`, `#API`, `#Developer Tools`, `#LLM Infrastructure`

---

<a id="item-9"></a>
## [Anthropic Restricts Claude to Users Over 18 With Age Assurance](https://support.claude.com/en/articles/15171100-age-assurance-on-claude) ⭐️ 7.0/10

Anthropic has updated its Claude support documentation to state that Claude is only available to people over 18 years of age, and has introduced age assurance measures to enforce that restriction. Community members digging into the change note that the underlying policy dates back to December 2025 and that the terms of service already barred minors as far back as February 2024, even though the support page only began circulating in January 2026. This makes Anthropic one of the first major general-purpose LLM providers to gate mainstream AI access behind age checks, setting a precedent that other vendors may follow and that regulators may cite. It also directly affects how students, schools and hobbyists choose their tools, with some commenters predicting a shift toward open-source and Chinese-hosted models that require no verification. Commenters point out that the policy is older than it appears, with a December 2025 archived copy of the support page and a February 2024 terms-of-service clause already excluding minors. Anthropic reportedly receives only the verification result rather than the underlying identity data, but critics argue that this does not eliminate the risk created by third-party ID verification vendors, which have suffered large-scale data breaches in the past.

hackernews · Muhammad523 · Sep 11, 10:48 · [Discussion](https://news.ycombinator.com/item?id=49656225)

**Background**: “Age assurance” is an umbrella term for any method a platform uses to determine, verify or estimate a user's age online, ranging from document-based ID checks and facial age estimation to simple age gating and segmentation; “age verification” refers specifically to the high-certainty subset of these methods. The shift toward such measures is driven by a growing patchwork of online-safety laws aimed at protecting minors, but privacy researchers warn that mandatory verification can create centralized databases of identity documents and effectively turn ordinary users into tracked “transparent citizens.” Chatbot providers face additional pressure because of ongoing public debate about the effect of AI companions on minors' mental health.

<details><summary>References</summary>
<ul>
<li><a href="https://www.incode.com/blog/age-assurance-explained-verification-estimation-segmentation-and-gating/">Age Assurance Explained: Verification, Estimation ...</a></li>
<li><a href="https://epic.org/issues/platform-accountability-governance/age-assurance/">Age Assurance – EPIC – Electronic Privacy Information Center</a></li>
<li><a href="https://theconversation.com/age-verification-online-can-be-done-safely-and-privately-heres-how-276104">Age verification online can be done safely and privately. Here’s how</a></li>

</ul>
</details>

**Discussion**: Sentiment on Hacker News is overwhelmingly skeptical: top comments mock the appearance of a compliance-driven motive, recall a 2026 breach in which a third-party ID verification service exposed 153 million driver's licenses, and argue that these decisions should be left to parents rather than companies and governments. Others note the policy is old news already codified in the terms of service, suggest Chinese and open-source models as a way to avoid verification entirely, and worry that the next generation of students will be trained on different tools than the industry actually uses.

**Tags**: `#privacy`, `#age-verification`, `#anthropic`, `#claude`, `#policy`

---

<a id="item-10"></a>
## [EPA Proposes Scrapping Mandatory Public Review for Data Center Pollution Permits](https://capitalbnews.org/data-centers-permit-rules-epa/) ⭐️ 7.0/10

The Environmental Protection Agency has proposed eliminating the federal requirement that states publicize and solicit public input before approving air pollution permits for a range of industrial facilities, including the data centers being built across the country and the power plants built to feed them. Under the proposal, state and local agencies would instead be given discretion to determine whether, when, and for how long to offer opportunities for public participation. Public notice and comment is often the main — and sometimes the only — leverage local communities have when fighting data center and power plant construction, so removing it could smooth the path for AI infrastructure expansion while reducing environmental oversight. The change would shift decision-making power toward state agencies and developers and away from residents, environmental groups, and tribes affected by emissions. The proposal targets the public-participation requirement attached to permits, including so-called minor-source permits that cover the diesel backup generators and gas turbines commonly used at data centers, and it comes alongside EPA's launch of a Clean Air Act resource page intended to give data center developers, communities and tribes centralized information. Because it is only a proposed rule, it still has to go through a rulemaking process, and states could choose to keep their own notice-and-comment requirements even if the federal mandate is dropped.

hackernews · doener · Sep 11, 18:05 · [Discussion](https://news.ycombinator.com/item?id=49662672)

**Background**: Under the Clean Air Act, facilities that emit certain pollutants must obtain air pollution permits before operating, and federal rules have long required that the public be notified and allowed to comment on those applications before approval. Data centers matter here because they draw enormous amounts of electricity and typically rely on on-site diesel generators for backup power, while the new gas plants built to serve them are themselves major emissions sources. The proposal fits a broader pattern of deregulatory moves by the current EPA, which critics say has been weakened and has narrowed its own ability to measure and regulate pollution.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/08/25/climate/epa-data-centers-public-comment.html">E.P.A. Moves to Curb Public Input on Air Pollution Permits ...</a></li>
<li><a href="https://www.techtimes.com/articles/325694/20260826/epa-proposes-ending-mandatory-public-comment-minor-source-data-center-permits.htm">EPA Proposes Ending Mandatory Public Comment on Minor-Source ...</a></li>
<li><a href="https://truthout.org/articles/the-epa-is-planning-to-scrap-public-review-rules-for-data-center-pollution/">The EPA Is Planning to Scrap Public Review Rules for Data ...</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were overwhelmingly critical, framing the rollback as part of a national AI arms race in which the government will sacrifice environmental safeguards to win, and arguing that communities which successfully blocked data centers now look vindicated. A notable counterpoint came from one commenter who read the rule as giving local governments more control, saying that local elections are where individual votes and voices count most and disputing the idea that people have lost faith in local government.

**Tags**: `#data centers`, `#EPA`, `#regulation`, `#AI infrastructure`, `#environment`

---

<a id="item-11"></a>
## [Measuring the sloppiness of code](https://earendil.com/posts/measuring-code-sloppiness/) ⭐️ 7.0/10

The blog post "Measuring the sloppiness of code" from earendil.com proposes quantitative metrics for evaluating how sloppy a piece of code is, explicitly framing the question as "if coding is solved, what now?" and arguing that measuring code quality is a prerequisite for giving AI coding agents reliable feedback. As AI agents generate ever more code at low marginal cost, the bottleneck shifts from writing code to judging whether that code is good, so having objective sloppiness metrics could shape how teams review, gate, and pay for AI-generated contributions across the software industry. The author acknowledges that evaluating sloppiness is hard because human intuition and taste remain either implicitly or explicitly baked into the metrics, and points to other promising directions such as coupledness of functions, code churn, and cohesion.

hackernews · doppp · Sep 11, 13:42 · [Discussion](https://news.ycombinator.com/item?id=49658311)

**Background**: Code quality has long been assessed with established metrics such as cyclomatic complexity and LCOM (lack of cohesion of methods), alongside the broader concept of technical debt, which describes the future maintenance cost incurred by choosing expedient solutions today. AI coding agents, which use large language models to generate and edit code autonomously, make these measurements newly urgent because an agent with no sense of quality can flood a codebase with plausible-looking but poorly structured code.

<details><summary>References</summary>
<ul>
<li><a href="https://earendil.com/posts/measuring-code-sloppiness/">If coding is solved, what now?: Measuring the sloppiness of ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Technical_debt">Technical debt - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_coding_agent">AI coding agent</a></li>

</ul>
</details>

**Discussion**: Commenters broadly welcomed quantitative feedback for agents but pushed back on the framing: dherman argued the problems that really matter are global properties of a codebase rather than local ones, since an agent can fix local sloppiness on a by-need basis, while toddwprice warned that unlimited token spend on frontier models stops looking cost-effective once you pay per token, making human effort competitive again. justinmarsan shared that the same reflections led them to build an architecture-review agent, which taught them the metrics (LCOM, cyclomatic complexity) behind practices they had followed for years, and asked for more effort on correctness and self-improving feedback loops involving developers.

**Tags**: `#code quality`, `#technical debt`, `#AI agents`, `#software engineering`, `#metrics`

---

<a id="item-12"></a>
## [Datasette ships security patches after AI-assisted audit](https://simonwillison.net/2026/Sep/11/datasette-security/) ⭐️ 7.0/10

Datasette released two security patch versions, 1.0a39 for the alpha series and 0.65.4 for the stable 0.65.x family, after an extensive audit conducted with Claude Fable 5.1, GPT-5.6, and GPT-6 Astra. The audit followed issues reported by Sevban Dönmez, and Simon Willison and Alex Garcia then spent nearly a week reviewing and implementing the fixes. Anyone running a Datasette instance on the public web, especially one that mixes public and private tables, should upgrade promptly because the bugs were subtle enough to evade normal review. It also signals a broader shift: a widely used open-source project now plans to make frontier-model security audits a routine part of all development work. The advisory specifically warns instances that mix public and private tables, since that configuration is where the subtle bugs could be exploited. Willison described a workflow where the two developers split each issue — one wrote automated tests that reproduced the flaw while the other implemented the fix — so that two humans plus agents running different models reviewed every issue.

rss · Simon Willison · Sep 11, 03:27

**Background**: Datasette is an open-source tool created by Simon Willison for exploring data of any shape and publishing it as an interactive website and API; it maintains parallel stable (0.65.x) and alpha (1.0a) release lines. AI-assisted security audits use large language models to scan code, trace dependencies, and probe boundary conditions far faster than manual review, with humans judging which findings are real. The project's plan to apply such audits routinely reflects a growing practice of pairing model-driven scanning with experienced human review.

<details><summary>References</summary>
<ul>
<li><a href="https://datasette.io/">Datasette: An open source multi-tool for exploring and ...</a></li>
<li><a href="https://medium.com/oak-security/ai-assisted-security-audits-0bd76608e3be">AI - Assisted Security Audits . A Practical Guide with... | Medium</a></li>

</ul>
</details>

**Tags**: `#security`, `#datasette`, `#release`, `#ai-audit`, `#open-source`

---

<a id="item-13"></a>
## [ACL Announces Sustainable Reviewing Policy with Submission Caps](https://www.reddit.com/r/MachineLearning/comments/1wd7b83/acl_sustainable_reviewing_policy_d/) ⭐️ 7.0/10

ACL announced on X a new "Sustainable Reviewing Policy" for ACL Rolling Review (ARR) that ties the number of reviewed submissions to available reviewer capacity, requiring each submission to "pay" for itself via a qualified service contributor (reviewer or chair), with submissions lacking such capacity entering a lottery for leftover slots. The policy also introduces per-author quotas capping authors at 20 total submissions and 5 first-author (including shared first-author) submissions per review cycle, plus penalties or bans for accounts that systematically submit or endorse low-quality work. This is one of the most significant structural changes to peer review in the NLP community in years, since it directly links submission privileges to reviewing labor and could reshape how labs, students, and industry groups plan their publication strategies. It may ease the reviewer overload that has degraded review quality, but also risks disadvantaging authors from smaller institutions or groups with fewer qualified reviewers. Authors who lack a qualified reviewer among themselves can nominate a non-author designated contributor, but that person must vouch for the work in an arXiv-endorsement style, and a mentorship system will be built for contributors who are not yet qualified. The 20-total and 5-first-author caps per cycle are per author (shared first authorship counts), and ACL says abuse-detection measures will be implemented, with more details to follow on the ACL website.

reddit · r/MachineLearning · /u/S4M22 · Sep 11, 05:38

**Background**: ACL Rolling Review (ARR) is a centralized reviewing service run by the Association for Computational Linguistics on top of the OpenReview platform, in which authors submit papers and receive reviews in roughly two-month cycles, then commit accepted papers to top-tier ACL conferences. Submission volumes to ARR and major NLP conferences have grown dramatically in recent years, straining a reviewer pool that is largely volunteer-based, which has led to concerns about review quality, reviewer burnout, and unreliable decisions. This policy is ACL's attempt to make that system sustainable by matching the number of submissions to the number of people actually willing to review.

<details><summary>References</summary>
<ul>
<li><a href="https://aclrollingreview.org/">ACL Rolling Review – A peer review platform for the ...</a></li>
<li><a href="https://www.aclweb.org/portal/content/acl-rolling-review">ACL Rolling Review | ACL Member Portal</a></li>

</ul>
</details>

**Tags**: `#ACL`, `#peer review`, `#NLP`, `#academic publishing`, `#machine learning`

---

<a id="item-14"></a>
## [Anthropic Urges Global Slowdown of Frontier AI Development](https://t.me/zaihuapd/43753) ⭐️ 7.0/10

Anthropic publicly called on major AI labs worldwide to consider coordinating a slowdown in frontier model development, warning in a blog post that AI progress is so fast that systems capable of "recursive self-improvement" without human intervention could soon emerge. The company argued that any unilateral pause would simply let rivals race ahead, and therefore proposed a synchronized, multi-country halt by leading AI firms governed by verifiable rules. It is a rare case of a leading frontier lab publicly proposing a coordinated global pause on the very technology it is building, pushing AI safety and governance questions into the center of policy debate. The idea has met resistance in Washington and Silicon Valley, where critics argue it overstates the risks, serves as a pretext to hobble competitors, and could hand China a strategic advantage if the US slows down alone. The proposal hinges on synchronized participation by multiple national AI champions under verifiable compliance rules, since Anthropic concedes that a lone pause would only benefit faster-moving rivals. No concrete enforcement mechanism, timeline, or set of verification standards has been detailed, and the pushback centers on whether such risk claims justify slowing an industry that is also a geopolitical race.

telegram · zaihuapd · Sep 11, 02:23

**Background**: A "frontier model" is a general-purpose AI system sitting at or near the current leading edge of capability, judged against the best-known results across many benchmarks — a moving target rather than a fixed class of model. "Recursive self-improvement" is a hypothesized process in which an AI rewrites its own code and improves the mechanisms that generate further improvements, potentially triggering an intelligence explosion; no attempt so far has shown such an effect. Anthropic's emphasis on "verifiable" rules echoes ongoing work on verifiable training, which aims to let outside parties confirm the integrity and origin of a model's training process.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Recursive_self-improvement">Recursive self-improvement</a></li>
<li><a href="https://www.levellers.ai/what-is/frontier-model">What is a frontier model ? Clear business guide | Levellers. ai</a></li>
<li><a href="https://futureoflife.org/ai/verifiable-training-of-ai-models/">Verifiable Training of AI Models - Future of Life Institute</a></li>

</ul>
</details>

**Tags**: `#AI Safety`, `#AI Policy`, `#Anthropic`, `#Frontier Models`, `#AI Regulation`

---

<a id="item-15"></a>
## [DeepSeek Releases V4.1 Flash, a 552B Multimodal Model on a New Architecture](https://t.me/zaihuapd/43770) ⭐️ 7.0/10

DeepSeek officially released V4.1 Flash, the smallest model in its brand-new architecture family, built on a 552B-parameter Causal-Encoder-Decoder design with 8B input and 16B output activation and native support for multimodal visual understanding. The model is already live on the DeepSeek API under the name deepseek-flash, with new pricing taking effect at 12:00 on 10 September 2026, after which deepseek-v4-pro requests will be routed elsewhere from 12:00 on 14 September. The release signals DeepSeek's push to make frontier-class capabilities cheaper and faster to serve: by keeping only a small slice of a 552B model active per token, inference and especially agentic workloads can drop dramatically in cost, which pressures rivals' pricing and could make long-running autonomous agents economically viable for far more developers. Retiring or rerouting deepseek-v4-pro also shows DeepSeek is willing to consolidate its lineup around the new architecture rather than maintain older models indefinitely. The headline efficiency claim rests on sparse activation: only 8B parameters are activated for input and 16B for output out of the 552B total, a design comparable to the sparse-activation techniques used to cut compute and memory movement in large models. Two caveats are worth noting: the announced pricing takes effect on a future date (September 2026), which makes it hard to verify now, and the source is a short truncated Telegram post, so details such as benchmark numbers, context length and the exact routing target for deepseek-v4-pro are not yet disclosed.

telegram · zaihuapd · Sep 11, 11:32

**Background**: Most modern LLMs such as GPT and Llama are decoder-only transformers that use causal masking to generate text autoregressively, one token at a time; an encoder-decoder design instead first encodes the input into a representation and then decodes the output, which can help with multimodal inputs such as images. DeepSeek has become known for highly efficient large models that only activate a fraction of their parameters per token, which is why a 552B-parameter model can still be served at relatively low cost. "Native multimodal vision" means the model was trained to handle images from the start rather than having vision bolted on afterwards, while an API model name such as deepseek-flash is simply the identifier developers pass in their requests.

<details><summary>References</summary>
<ul>
<li><a href="https://forkast.news/deepseeks-new-architecture-slashes-agentic-costs-by-80/">DeepSeek’s New Architecture Slashes Agentic Costs by 80%</a></li>
<li><a href="https://www.labellerr.com/blog/exploring-architectures-and-configurations-for-large-language-models-llms/">Large Language Model Architecture Explained [Updated]</a></li>
<li><a href="https://arxiv.org/pdf/2310.04564">Exploiting Activation Sparsity in Large Language Models</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLM`, `#DeepSeek`, `#model-release`, `#multimodal`

---

<a id="item-16"></a>
## [Anthropic Report Accuses Seven Chinese AI Labs of Large-Scale Claude Distillation](https://t.me/zaihuapd/43771) ⭐️ 7.0/10

Anthropic's latest threat intelligence report claims it has detected and blocked large-scale "distillation" activity against Claude by seven Chinese AI labs since February 2025, explicitly naming Alibaba, Zhipu, Xiaomi, SenseTime and MiniMax. Alibaba was described as the largest offender, generating more than 151 million interactions between May and July, peaking at nearly 3 million per day. The accusation escalates the friction between US frontier model providers and Chinese labs over how model outputs may be used, touching on terms-of-service enforcement, export controls and geopolitical tensions around AI. If such distillation claims lead to tighter API restrictions or policy action, it could affect how Chinese labs close the capability gap with leading Western models and how broadly Claude is resold or accessed. Anthropic claims the harvested data was used to train Qwen 3.5, 3.6 and 3.7, as well as for reinforcement-learning environments and model architecture work, but the report is Anthropic's own account and the figures have not been independently verified. Distillation through legitimate API access typically breaches a provider's terms of service rather than any law, which is why the dispute is framed as a threat-intelligence and policy issue rather than a clear-cut legal one.

telegram · zaihuapd · Sep 11, 13:10

**Background**: Knowledge or model distillation is a standard machine-learning technique in which a smaller "student" model is fine-tuned on the outputs of a larger, more capable "teacher" model, allowing it to match the teacher's performance on specific tasks at much lower cost. Because frontier labs sell access to their models through APIs, anyone with an account can in principle collect large volumes of high-quality outputs; most providers' terms of service forbid using those outputs to train competing models. Reinforcement-learning environments, also mentioned in the report, are simulated settings in which an AI agent is trained through trial-and-error rewards, and they are a growing part of post-training for large models.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>
<li><a href="https://openai.com/index/api-model-distillation/">Model Distillation in the API - OpenAI</a></li>

</ul>
</details>

**Tags**: `#AI industry news`, `#model distillation`, `#Anthropic`, `#Chinese AI labs`, `#AI policy/geopolitics`

---

<a id="item-17"></a>
## [Boris Cherny: Claude-Written Production Code Should Be Held to a Higher Bar](https://simonwillison.net/2026/Sep/11/boris-cherny/) ⭐️ 6.0/10

Boris Cherny, an Anthropic engineer closely associated with Claude Code, argued in a post on X that production code written by Claude should be held to a higher standard than code written by a human. He listed the guardrails Anthropic relies on to enforce this: extensive lint rules, extensive tests, Claude-driven end-to-end tests, Claude-powered fuzzers running daily, automated code and security reviews, and automated code refactoring. As coding agents move from autocomplete-style suggestions to autonomously editing and shipping real code, the bottleneck shifts from generation to verification, and Cherny's stance suggests that the leading AI lab treats AI-authored code as something requiring more scrutiny, not less. If this becomes an industry norm, teams adopting agentic coding tools will need to invest heavily in automated testing, static analysis, and review infrastructure rather than simply trusting model output. Notably, several of the guardrails are themselves Claude-driven — the same model family writes the code and helps generate end-to-end tests, fuzzers, and reviews — which raises the question of how independent that self-verification really is. Cherny offers no concrete metrics or failure rates, and his justification is framed around maintainability: without these guardrails, he warns, you end up with a mess that is hard to maintain over time.

rss · Simon Willison · Sep 11, 17:47

**Background**: Claude Code is Anthropic's agentic coding tool that lives in the terminal or IDE, understands a codebase, edits files, runs commands, and handles git workflows via natural language. Fuzzing is an automated testing technique that feeds invalid, unexpected, or random data into a program to surface crashes and security holes; linting, unit tests, and automated code review are more conventional software quality checks. Cherny's argument sits inside a broader debate about how much human review AI-generated code needs before it reaches production.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Fuzzing">Fuzzing - Wikipedia</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>
<li><a href="https://www.anthropic.com/features/making-of-claude-code">The Making of Claude Code \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Claude`, `#coding-agents`, `#software-engineering`, `#code-quality`

---

<a id="item-18"></a>
## [Simon Willison urges Python devs not to sleep on wrapture](https://simonwillison.net/2026/Sep/11/wrapture/) ⭐️ 6.0/10

In a short post published on September 11, 2026, Simon Willison highlighted wrapture, Graham Dumpleton's new Python monkey patching library released on August 31, 2026, which is designed to serve both testing and observability tracing at the same time. Dumpleton has since published roughly ten tutorials on the library — covering unit testing, call recording, phased behaviour, live tracing, zero-code tracing, Flask instrumentation, slow-code detection and OpenTelemetry export — plus a set of interactive JupyterLab workshops. Wrapture unifies two use cases that Python developers normally solve with separate tools — unittest.mock-style patching for tests and New Relic-style runtime tracing for observability — which could let teams consolidate their instrumentation stack into one dependency. A public endorsement from Simon Willison, combined with Dumpleton's strong reputation in the Python community, may help a library with surprisingly little buzz gain wider adoption. Wrapture is still alpha software ahead of a 1.0.0 release, and it builds on the safe monkey-patching machinery from the existing wrapt library; notably, Dumpleton has said the code was written by an AI under his direction rather than designed by it. A companion package, wrapture-instrumentation, ships ready-made instrumentation for Flask, Django, FastAPI, Starlette, aiohttp, gRPC, requests, httpx, urllib3, SQLAlchemy, sqlite3, Jinja2, Uvicorn and others, and traces can be exported to OpenTelemetry or configured entirely through a TOML file without touching Python source code.

rss · Simon Willison · Sep 11, 13:51

**Background**: Monkey patching means dynamically modifying code at runtime — replacing functions, methods or attributes in memory — rather than editing the original source, a technique Python allows freely and that is widely used for testing and instrumentation. wrapt, also by Graham Dumpleton, is the long-established library that makes such patching safe and transparent, and wrapture is its sibling project; Dumpleton is a well-known Python developer, also the author of the mod_wsgi Apache module. Observability tracing, meanwhile, is the practice of recording the flow and timing of calls inside a running application so developers can see where time goes and why things behave as they do; OpenTelemetry is the vendor-neutral standard format for exporting such traces.

<details><summary>References</summary>
<ul>
<li><a href="https://pypi.org/project/wrapture/">wrapture · PyPI</a></li>
<li><a href="https://github.com/GrahamDumpleton/wrapture">GitHub - GrahamDumpleton/wrapture: Monkey patch, test, and ...</a></li>
<li><a href="https://simonwillison.net/2026/Aug/31/introducing-wrapture/">Introducing wrapture</a></li>

</ul>
</details>

**Tags**: `#python`, `#monkey-patching`, `#testing`, `#observability`, `#tooling`

---

<a id="item-19"></a>
## [China Releases First Mandatory National Safety Standard for Power Banks](https://t.me/zaihuapd/43755) ⭐️ 6.0/10

China officially published GB 47372-2026, its first mandatory national safety standard for power banks, drafted by the Ministry of Industry and Information Technology together with more than 30 leading companies and institutions including Huawei, Xiaomi, OPPO, Anker and UGREEN. The standard takes mandatory effect on April 1, 2027. Billed as the strictest power-bank safety rule to date, the standard will reshape the battery and consumer-electronics supply chain by forcing cell makers and assemblers to meet cell-level safety tests and eliminating refurbished cells from the market. With 28 cell suppliers such as ATL and BYD already listed as compliant, non-conforming factories face exclusion from the world's largest power-bank market. The regulation requires cells to pass a nail-penetration test without catching fire or exploding, tightens thermal-abuse and overcharge tests, adds new whole-device mechanical tests such as drop and crush, bans tiered-recycled or second-hand refurbished cells, and mandates labeling of the product's safe service life.

telegram · zaihuapd · Sep 11, 03:34

**Background**: A nail-penetration test drives a steel nail through a cell to simulate an internal short circuit, making it one of the harshest ways to gauge a lithium battery's thermal-runaway resistance; China's GB 38031 applies a comparable requirement to EV batteries. Thermal-abuse and overcharge tests instead evaluate how a cell behaves under extreme heat or excess charging current. Tiered recycling refers to reusing retired EV or consumer cells in less demanding applications, which is cheap but introduces unpredictable aging and safety risk. Power banks have historically been covered mainly by voluntary or general battery standards, leaving a regulatory gap that this GB standard now closes.

<details><summary>References</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/84688001">锂离子电池针刺测试 - 知乎专栏</a></li>
<li><a href="https://www.seantest.com/battery-nail-penetration-test.html">电池针刺测试标准与流程详解_第三方检测机构 - 深圳晟安检测</a></li>
<li><a href="https://www.elecfans.com/d/2372383.html">电池 热 滥 用 测 试 和过充 测 试 的不同之处-电子发烧友网</a></li>
<li><a href="https://eu.36kr.com/zh/p/3348283380095880">震惊！ 电 池坟场宁德时代竟不敌小作坊</a></li>

</ul>
</details>

**Tags**: `#battery-safety`, `#consumer-electronics`, `#regulation`, `#supply-chain`, `#hardware`

---

<a id="item-20"></a>
## [China cancels original Chang'e-8 plan, merges lunar programs](https://spacenews.com/china-alters-change-8-lunar-south-pole-mission-amid-lunar-program-reorganization/) ⭐️ 6.0/10

In May 2026 the China Manned Space Agency (CMSA) announced it would merge the uncrewed lunar exploration program previously run by the China National Space Administration with the crewed lunar landing program into a single "Lunar Exploration Program," integrating missions, resources, and personnel. As a result, the standalone Chang'e-8 mission — originally scheduled to launch around 2029 and land at Moulton crater near the lunar south pole — has been cancelled or substantially restructured, and Pakistan confirmed in September 2026 that it would move its payload to another lunar mission in 2030–2031. This is an institutional power shift in China's space program: overall management of lunar missions moves to the crewed spaceflight agency, which is now reconfiguring the robotic landing roadmap. It could delay or reshape scientific robotic missions, alter the construction schedule of the International Lunar Research Station, and force international partners such as Pakistan to renegotiate their payload opportunities. Chang'e-8 was designed as the first Chinese probe in the construction phase of the International Lunar Research Station and, together with Chang'e-7, was to form the basic configuration of a lunar south-polar research station; it had also opened around 200 kg of international payload capacity. Notably, the reported details come largely from Chinese Wikipedia and SpaceNews reporting rather than a full official mission specification, so the exact scope of the restructured mission remains unclear.

telegram · zaihuapd · Sep 11, 04:00

**Background**: China's lunar effort is organized as the Chang'e program, run for years by the China National Space Administration (CNSA), with successive missions covering orbiting, landing, sample return, and polar prospecting. The crewed spaceflight effort is managed separately by the China Manned Space Agency (CMSA), a body established in 1993 that oversees the Shenzhou, Tiangong, and future crewed lunar landing work. The International Lunar Research Station is China's proposed long-term lunar base, planned to be assembled in stages starting with robotic precursors around the lunar south pole, an area of interest because of permanently shadowed craters that may hold water ice. Moulton, the original Chang'e-8 landing target, is an ancient impact crater on the lunar far side and the northern terminus of Schrödinger valley.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/嫦娥八号">嫦娥八号 - 维基百科，自由的百科全书</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/莫尔顿环形山">莫尔顿环形山 - 维基百科，自由的百科全书</a></li>
<li><a href="https://zh.wikipedia.org/wiki/中國載人航天工程辦公室">中國載人航天工程辦公室 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**Tags**: `#space`, `#china-lunar-program`, `#chang'e-8`, `#aerospace-policy`, `#science-news`

---

<a id="item-21"></a>
## [Japan Digital Agency Breach May Expose Data of 246,000 People](https://www.bloomberg.com/news/articles/2026-09-11/japan-s-digital-agency-hit-by-unauthorized-access-to-servers) ⭐️ 6.0/10

Japan's Digital Agency reported that its servers were accessed without authorization, potentially exposing the personal data of about 246,000 people. An investigation found that attackers exploited a VPN vulnerability in late June to reach a large number of files through a maintenance account, potentially obtaining names, email addresses and phone numbers. This is a government-level breach at the agency responsible for Japan's digital transformation, so it directly affects public trust in e-government services and citizen data handling. It also highlights how exploited VPN flaws and privileged maintenance accounts remain one of the most common entry paths into otherwise hardened public-sector networks. The agency has not confirmed that any of the potentially exposed data has actually been misused, and the exposed fields appear limited to names, email addresses and phone numbers rather than more sensitive identifiers. The key weak point was a maintenance account reachable over VPN, a class of privileged access that is frequently exempt from multi-factor authentication and strict monitoring.

telegram · zaihuapd · Sep 11, 05:10

**Background**: Japan's Digital Agency (デジタル庁) was created in September 2021 to centralize and modernize the country's fragmented government IT systems and digital services. Many public agencies rely on VPNs to let employees and contractors reach internal systems remotely, which makes VPN software and gateways attractive targets for attackers. Maintenance or administrative accounts are privileged logins used for patching and upkeep; when such accounts are poorly protected or accessible from the internet, they can let intruders move through a network without exploiting user-facing systems.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.scalefusion.com/top-vpn-vulnerabilities-every-business-must-know/">Top 10 VPN Vulnerabilities You Need to Know in 2026</a></li>
<li><a href="https://llumin.com/blog/cybersecurity-best-practices-for-maintenance-systems/">Cybersecurity Best Practices for Maintenance Systems</a></li>
<li><a href="https://www.gsa.gov/system/files?file=Maintenance-(MA)-[CIO-IT-Security-10-50-Rev-5]-11-05-2024.pdf">IT Security Procedural Guide: Maintenance (MA) CIO-IT ... - GSA</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#data-breach`, `#government-it`, `#vpn-vulnerability`, `#privacy`

---

<a id="item-22"></a>
## [Kimi Code Ships K2.8 Preview With Near-K3 Performance](https://www.kimi.com/code/docs/kimi-code/whats-new.html) ⭐️ 6.0/10

Moonshot AI's Kimi Code has fully rolled out the K2.8 Preview model, which the company says delivers overall performance close to K3 while markedly improving thinking efficiency. The release adds three adjustable thinking-effort tiers and a 1M-token context window, renames the permission modes to "Ask when necessary" and "Fully automatic," and introduces a new dangerous-command guardrail. Coding assistants are increasingly judged on agentic reliability, latency and cost rather than raw benchmark scores, so a preview model that approaches flagship quality could give developers K3-class results at a lower price or faster response time. The thinking-effort tiers and 1M-token context also matter for long-horizon tasks that span an entire repository. The near-K3 performance claim and the 1M-token context window come from Moonshot's own announcement rather than independent benchmarks, and because the model is explicitly labeled "Preview," behavior, API stability and pricing may still change. The new dangerous-command guardrail is a safety layer that intercepts risky shell commands before they execute, which matters most when the permission mode is set to "Fully automatic."

telegram · zaihuapd · Sep 11, 09:00

**Background**: Kimi Code is Moonshot AI's developer-focused coding agent, usable in the terminal and inside IDEs, that writes, refactors, debugs and explains code in an agent-style workflow with tool support. Its flagship counterpart, Kimi K3, is an open model at roughly the 2.8-trillion-parameter / 3T class with around 1M tokens of context, built for long-horizon coding and knowledge work. "Thinking effort" tiers — also called reasoning budget — let users control how much internal reasoning the model performs before answering, trading quality against latency and token cost.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/code/en">Kimi Code with Kimi K3: Next-Gen AI Code Agent & CLI</a></li>
<li><a href="https://www.moonshot.ai/">Moonshot AI</a></li>
<li><a href="https://lmmarketcap.com/llm-parameters/reasoning-effort">Reasoning Effort (Thinking Budget) - LLM Parameter Guide</a></li>

</ul>
</details>

**Tags**: `#Kimi`, `#LLM`, `#coding-assistant`, `#model-release`, `#AI-tools`

---