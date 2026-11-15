---
layout: default
title: "Horizon Summary: 2026-11-16 (EN)"
date: 2026-11-16
lang: en
---

> From 31 items, 18 important content pieces were selected

---

1. [Meta FAIR and NYU: Vision Encoder Pretraining Optional, Vision-Only Parameters Essential](#item-1) ⭐️ 8.0/10
2. [Open-source tool makes pageable cudaMemcpy ~5x faster on B300 GPU](#item-2) ⭐️ 8.0/10
3. [Multiplayer CS:GO-style game renders each player's view with a local world model](#item-3) ⭐️ 8.0/10
4. [MacBook Pro OLED PWM flicker raises usability concerns](#item-4) ⭐️ 7.0/10
5. [Microsoft 365 outage blamed for chlorine gas poisoning of 15 hotel guests](#item-5) ⭐️ 7.0/10
6. [Sebastian Raschka Explains How Modern LLMs Encode Position, Sparking Group-Theory Debate](#item-6) ⭐️ 7.0/10
7. [Blogger Argues All AI-Generated Code Should Be Open Source](#item-7) ⭐️ 7.0/10
8. [Report: Lutnick Pushed to Weaken Chip Rules Tied to Family Business](#item-8) ⭐️ 7.0/10
9. [Training-free early exit by editing one output-layer row](#item-9) ⭐️ 7.0/10
10. [FAA Ground Stop Traced to Router Failure After Copper-to-Fiber Upgrade](#item-10) ⭐️ 7.0/10
11. [Telegram Widgets Reportedly Vulnerable to Sandbox Escape and RCE](#item-11) ⭐️ 7.0/10
12. [Study Claims Six Chinese AI Models Carry Blackwell Chip Fingerprints in Their Weights](#item-12) ⭐️ 7.0/10
13. [Huawei Cloud Launches Open-Source openPangu-2.1-Pro Model on MaaS Platform](#item-13) ⭐️ 7.0/10
14. [Retrospective: Turbo Pascal's Tiny Footprint vs. Modern Software Bloat](#item-14) ⭐️ 6.0/10
15. [Blogger Swaps His Conventional Browser for Emacs' eww, Sparking HN Debate](#item-15) ⭐️ 6.0/10
16. [Marimba: an open-weight 'System One' speech model built on frozen Qwen3-ASR](#item-16) ⭐️ 6.0/10
17. [Tesla to Start Selling Two-Seat Cybercab by Year-End, Fleet First](#item-17) ⭐️ 6.0/10
18. [US Judge Denies Micron, Samsung, SK Hynix Bid to Dismiss DRAM Price-Fixing Suit](#item-18) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Meta FAIR and NYU: Vision Encoder Pretraining Optional, Vision-Only Parameters Essential](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR and NYU researchers trained more than 200 multimodal LLMs entirely from scratch — including the language backbone — on identical data with encoder pretraining charged against the same lifetime compute budget, in order to separate three design choices that standard vision encoders normally bundle together: separate pretraining, vision-only parameters, and placement before the LLM. They report that separate encoder pretraining is optional (pretrained encoders at best tie a scratch-trained one at matched compute), that vision-only parameters are required at every scale from 0.6B to 6.4B, and that pre-fusion placement before the LLM is optional because an "in-fusion" variant that injects zero-initialized vision-only weights into the LLM's first 8 layers performs on par while cutting time to first token by about 13%. This is a large-scale, tightly controlled ablation that directly challenges a widely held assumption — that a multimodal LLM needs a separately pretrained vision encoder such as CLIP or SigLIP — and it arrives while shipped models disagree sharply, with Gemma 4 12B dropping the encoder, Kimi K3 training its encoder from scratch, and Inkling 2 Small restoring one. Because published models differ in data, architecture, and compute, comparing them cannot isolate any single choice, so this decomposition gives MLLM designers a concrete answer about where to spend compute: keep dedicated vision capacity, but you can save the encoder pretraining budget and still fuse inside the backbone. The main comparisons use Qwen3-1.7B and 4B configurations with 0.4B parameters of vision capacity, plus a scaling ladder from 0.6B to 6.4B backbones, evaluated on 16 Cambrian VQA benchmarks at 448 px and 12 language benchmarks. Encoder-free models trail at every size and need roughly 3x the compute to catch up, whereas giving the LLM the encoder's parameters improves text but not VQA; notably, pretraining MetaCLIP 6.5x longer lifted ImageNet linear-probe accuracy from 80.4% to 84.4% without helping VQA, and at 1.7B the in-fusion vision-only branches in layers 1–8 reached 45.0 VQA versus 44.4 for the encoder, 42.3 when text shares those parameters, and 35.1 when placed in the last 8 layers.

reddit · r/MachineLearning · /u/trungh98 · Nov 15, 17:38

**Background**: Most multimodal LLMs (MLLMs) follow a recipe in which a vision encoder — typically a CLIP- or SigLIP-style model pretrained on hundreds of millions of image-text pairs — converts an image into tokens that a language model then reads alongside text. Because nearly every strong MLLM uses such an encoder, it is commonly assumed that this upstream visual pretraining is what gives the model its visual competence, and the encoder's parameters are usually trained separately, occupy their own module, and sit before the LLM. The problem is that these three properties are always bundled, so no comparison of released models can tell you whether the pretraining, the dedicated parameters, or the placement is actually doing the work. This paper "unbundles" them by charging encoder pretraining against the same lifetime compute budget as multimodal training, so a pretrained encoder has to justify the extra compute it consumed.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.17334">[2611.17334] Unbundling Multimodal Vision Encoding - arXiv.org</a></li>
<li><a href="https://huggingface.co/papers/2611.17334">Paper page - Unbundling Multimodal Vision Encoding</a></li>
<li><a href="https://magazine.sebastianraschka.com/p/understanding-multimodal-llms">Understanding Multimodal LLMs - by Sebastian Raschka, PhD</a></li>

</ul>
</details>

**Tags**: `#multimodal-llm`, `#vision-encoder`, `#pretraining`, `#model-architecture`, `#scaling-experiments`

---

<a id="item-2"></a>
## [Open-source tool makes pageable cudaMemcpy ~5x faster on B300 GPU](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 8.0/10

A developer released cudamemcpy-tuner, a tool whose `cmt tune` wrapper raises pageable CPU→GPU copy bandwidth on an NVIDIA B300 from 10.2 GB/s to 51.5 GB/s — roughly a 5x speedup — when copying a 1 GB uint8 PyTorch tensor. The project ships with benchmark scripts, a technical blog post explaining the approach, and open-source code on GitHub. Host-to-device transfers are often the slowest link in GPU workflows, so a drop-in tuner that multiplies pageable copy bandwidth can speed up data loading and preprocessing for anyone using default (non-pinned) tensors, without rewriting their model code. If the gains hold across other GPUs and workloads, it could change the long-standing advice that developers must manually manage pinned memory to get good transfer throughput. The reported numbers come from a simple micro-benchmark that copies a 1 GB tensor to the GPU and back and averages five iterations, so real-world gains will depend on transfer size, host memory layout, and PCIe generation. The tool is invoked as a wrapper (`cmt tune -- python bench.py`), meaning it tunes the copy path transparently rather than requiring code changes, but the published results cover only the B300 (Blackwell Ultra) platform.

reddit · r/MachineLearning · /u/makneeee · Nov 15, 18:20

**Background**: By default, host memory allocated by programs like NumPy or PyTorch is "pageable," meaning the operating system can swap or relocate it, so the GPU cannot DMA directly from it. When you call cudaMemcpy on pageable memory, the CUDA driver must first copy the data into a temporary page-locked ("pinned") staging buffer and then transfer it to the device, adding an extra host-to-host copy that cuts effective bandwidth. Pinned memory avoids that staging step and is normally the recommended fix, but it is expensive to allocate and reduces memory available to the OS — which is why a tool that closes the gap for ordinary pageable buffers is notable. The B300 is NVIDIA's Blackwell Ultra data-center GPU, announced at GTC in March 2025 with 288 GB of HBM3e, and it is paired with very fast host interconnects where copy overhead becomes more visible.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/how-optimize-data-transfers-cuda-cc/">How to Optimize Data Transfers in CUDA C/C++ | NVIDIA ... What is the difference between pinned memory and pageable ... Pinned vs. Pageable Memory | drkennetz/cuda_examples | DeepWiki Pinned and Pageable memory - CUDA Programming and Performance ... cuda_examples/MemoryAndStructureExamples/pinned_vs_pageable ... CUDA Pinned vs Pageable Memory: Faster Host-to-Device Transfers</a></li>
<li><a href="https://stackoverflow.com/questions/50184146/cuda-pinned-memory-vs-pageable-memory-tradeoffs">optimization - CUDA - Pinned Memory vs. Pageable Memory ... Code sample</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/dgx-b300/">An AI Factory for AI Reasoning NVIDIA DGX B 300</a></li>

</ul>
</details>

**Tags**: `#CUDA`, `#GPU memory transfer`, `#performance optimization`, `#PyTorch`, `#systems`

---

<a id="item-3"></a>
## [Multiplayer CS:GO-style game renders each player's view with a local world model](https://www.reddit.com/r/MachineLearning/comments/1xx4ta3/we_made_a_multiplayer_game_where_each_players/) ⭐️ 8.0/10

A team trained a diffusion-transformer world model on roughly 3,958 hours of 10-player CS:GO bot matches, with all POVs and inputs aligned at 16 Hz, and launched a free open beta multiplayer game where a lightweight server keeps state synchronized while each player's GPU generates their own view in real time. The beta requires an RTX 3080 or better, with an experimental Mac build also available. This moves neural world models beyond single-user demos into a network-synchronized multiplayer prototype, suggesting a path where each player's frames are generated locally rather than streamed as pixels. The accompanying roughly 4,000-hour aligned dataset also adds direct research value for game AI, action-conditioned video generation, and world-model work. The prototype is still limited to one small map, pistols only, and imperfect fine detail. Server state, player actions, and the previous frame are fed into diffusion transformers to draw the next frame, and the training dataset is released on Hugging Face.

reddit · r/MachineLearning · /u/bengal7ion · Nov 15, 19:46

**Background**: A world model is a learned model that predicts future observations — here, the next rendered frame — conditioned on the current game state and player actions, rather than replaying a conventional 3D engine. Diffusion transformers (DiTs) are a class of generative models that replace the U-Net backbone of diffusion models with a transformer operating on latent patches, which scales well and has become a common backbone for high-quality image and video generation. Running such a model in real time is challenging because diffusion typically requires multiple denoising steps per frame, so doing it on a consumer GPU while keeping multiplayer state in sync is the core technical achievement here.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2212.09748">[2212.09748] Scalable Diffusion Models with Transformers Diffusion Transformer Explained | Towards Data Science What Are Diffusion Transformers (DiTs)? The Architecture ... Diffusion Transformer (DiT) Architecture - emergentmind.com Diffusion Transformer Architectures (DiT) - emergentmind.com Diffusion Transformers (DiT) Architecture - apxml.com</a></li>
<li><a href="https://towardsdatascience.com/diffusion-transformer-explained-e603c4770f7e/">Diffusion Transformer Explained | Towards Data Science</a></li>

</ul>
</details>

**Tags**: `#world-models`, `#diffusion-transformers`, `#game-ai`, `#real-time-rendering`, `#multiplayer-systems`

---

<a id="item-4"></a>
## [MacBook Pro OLED PWM flicker raises usability concerns](https://macanorak.com/the-macbook-pros-oled-pwm-problem-when-a-better-display-becomes-worse-to-use/) ⭐️ 7.0/10

A technical article argues that the MacBook Pro's OLED display can cause PWM-flicker-related discomfort for sensitive users even though it is technically superior, while a Hacker News discussion questions the reported 240 Hz PWM rate. This matters because display quality is not just about contrast and color; flicker can affect eye comfort, concentration and usability for people with light sensitivity, migraines or concussion history, and may shape buying decisions and expectations for future Apple displays. PWM dimming works by rapidly switching the display's light output on and off, and frequencies below roughly 1000 Hz are commonly flagged as problematic for sensitive users; commenters argue that a tandem OLED could run two layers 180 degrees out of phase at 480 Hz each, producing an effective 960 Hz and making the 240 Hz figure a possible measurement or harmonic artifact.

hackernews · MacAnorak · Nov 15, 13:15 · [Discussion](https://news.ycombinator.com/item?id=50506719)

**Background**: PWM (pulse-width modulation) is a common way to control display brightness by pulsing light on and off very quickly; the longer the on-time relative to the off-time, the brighter the perceived output. OLED panels have no separate backlight, so many OLED screens dim by modulating the pixels themselves, which can produce visible flicker in some conditions. Some users are sensitive to this flicker and report eye strain, headaches or dizziness, even when the display's color, contrast and motion performance are otherwise excellent.

<details><summary>References</summary>
<ul>
<li><a href="https://daylightcomputer.com/blog/screen-flicker-101">Daylight | Light Flicker — Why your screen turning on & off 500 times...</a></li>
<li><a href="https://discussions.apple.com/thread/254749941">Severe Eye Strain due to OLED PWM Dimming - Apple Community</a></li>
<li><a href="https://circadianshield.com/guides/oled-pwm-flicker-eye-strain/">OLED PWM Dimming and Eye Strain : Why OLED ... | Circadian Shield</a></li>

</ul>
</details>

**Discussion**: Commenters welcome the focus on flicker sensitivity but push back on the 240 Hz claim, suggesting the tandem OLED may operate at 480 Hz per layer and about 960 Hz effective when out of phase; others add that CRI, motion blur, concussion-related screen sensitivity and flicker perception above the display refresh rate are also important factors.

**Tags**: `#OLED`, `#PWM flicker`, `#display technology`, `#eye strain`, `#Apple`

---

<a id="item-5"></a>
## [Microsoft 365 outage blamed for chlorine gas poisoning of 15 hotel guests](https://www1.wdr.de/nrw/rheinland/rhein-erft-kreis/technischer-defekt-chlor-phantasialand-100.html) ⭐️ 7.0/10

A Microsoft 365 outage meant that a hotel at the Phantasialand resort in Germany's Rhein-Erft-Kreis never received an automated email alert from the maintenance safety system of its sauna/pool area, so no one noticed that the automatic chlorine dosing system had injected too much chlorine into the pool. As a result, 15 guests suffered chlorine gas poisoning, a link the operator confirmed to German broadcaster WDR. The incident is a vivid, real-world demonstration of what happens when a safety-critical alarm path depends on a general-purpose cloud service with no fallback: a routine outage of a productivity suite escalated into physical injury. It is likely to sharpen scrutiny of how hotels, water parks and other public facilities architect their monitoring and alerting, and it feeds the broader debate about resilience gaps created by cloud and third-party dependency. According to the reporting, the pool's automatic dosing system over-chlorinated the water and the maintenance safety system raised an alert only via email, with no SMS, phone call, siren or on-site alarm providing a second channel. The failure mode was therefore not the dosing hardware itself but a single, non-redundant notification path that silently swallowed the warning during a third-party outage.

hackernews · DeepLogin · Nov 15, 18:36 · [Discussion](https://news.ycombinator.com/item?id=50509411)

**Background**: Microsoft 365 is Microsoft's cloud subscription suite that includes Exchange Online, the hosted email service many organizations use instead of on-premises mail servers; when it has an outage, mail delivery can be delayed or lost for hours. Commercial pools and saunas commonly use automatic chlorine dosing systems, where sensors measure disinfectant or redox levels and pumps inject chlorine, and modern controllers can emit alarms when dosing goes out of range. In safety engineering, such alarms are treated as safety-critical: they are expected to use redundant, independently powered channels and to trigger local, audible warnings rather than relying on a single messaging system.

<details><summary>References</summary>
<ul>
<li><a href="https://www.atlanticcouncil.org/in-depth-research-reports/report/critical-infrastructure-and-the-cloud-policy-for-emerging-risk/">Critical infrastructure and the cloud: Policy for emerging risk</a></li>
<li><a href="https://www.bdo.com.au/en-au/insights/cyber-security/managing-third-party-and-cloud-dependency-risks-strategies-for-stronger-resilience">Managing third-party and cloud dependency risks - BDO</a></li>
<li><a href="https://chloroklean.com/auto-dosing">Auto- Dosing ClO2 for Holiday Parks | ChloroKlean</a></li>

</ul>
</details>

**Discussion**: Commenters on Hacker News were nearly unanimous that the fault lies with the hotel's design rather than with Microsoft, with one calling it unacceptable that warnings about something so dangerous rely solely on email without backup or double-checking. Others stressed that anything capable of causing this kind of harm needs a more resilient, redundant architecture, and one commenter who identified as an Azure employee explicitly said the post was not a defense of the outage. A separate thread underscored how serious chlorine gas exposure can be, with an anecdote about a relative who needed emergency care after inhaling chlorine produced at home.

**Tags**: `#cloud-dependency`, `#safety-critical-systems`, `#reliability`, `#incident-analysis`, `#Microsoft 365`

---

<a id="item-6"></a>
## [Sebastian Raschka Explains How Modern LLMs Encode Position, Sparking Group-Theory Debate](https://magazine.sebastianraschka.com/p/understanding-positional-embeddings) ⭐️ 7.0/10

Sebastian Raschka published a technical explainer in his magazine covering how modern large language models encode and process token position information, walking through classic absolute/sinusoidal schemes as well as contemporary methods such as RoPE and what recent open models actually use. The piece drew substantial Hacker News attention (183 points, 23 comments), where commenter programjames argued that the article stays at the implementation level and omits the deeper theory that positional embeddings are group representations. Positional encoding is a core architectural choice in transformers, and it directly constrains how far a model can generalize beyond its training context length, so a clear cross-model comparison is practically useful for anyone building or fine-tuning LLMs. The accompanying debate highlights a recurring tension in the field between engineering recipes that work and the mathematical foundations that explain why they work. The article contrasts additive absolute position embeddings with rotation-based relative schemes like RoPE, which encodes absolute position via a rotation matrix while injecting explicit relative-position dependency into the self-attention formulation. The critique from commenters is that a purely implementation-level treatment misses why particular parameterizations are differentiable and learnable, a question usually answered through one-parameter groups and their irreducible representations.

hackernews · vismit2000 · Nov 15, 12:14 · [Discussion](https://news.ycombinator.com/item?id=50506376)

**Background**: Transformers process all tokens in parallel, so unlike recurrent networks they have no built-in notion of order and must be given position information explicitly. Early models added fixed sinusoidal vectors to token embeddings; later approaches, notably Rotary Position Embedding (RoPE) introduced with RoFormer in 2021, instead rotate the query and key vectors by an angle proportional to token position, so that attention scores depend naturally on relative distance. Group theory enters because a consistent positional encoding under translation can be described as a one-parameter group, and known results about such groups sharply constrain which encodings are even possible.

<details><summary>References</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/understanding-positional-embeddings">Understanding Positional Embeddings in Modern LLMs</a></li>
<li><a href="https://arxiv.org/abs/2104.09864">RoFormer: Enhanced Transformer with Rotary Position Embedding</a></li>
<li><a href="https://blog.janestreet.com/using-group-theory-to-explore-positional-encodings-attention/">Using group theory to explore the space of positional ...</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread was largely appreciative of the explainer but pushed back on its scope: programjames argued that positional embeddings are group representations and that this framework is precisely how one discovers and parameterizes them to be differentiable and learnable, citing rotary embeddings as representations of the abelian translation group ℝⁿ. The overall sentiment was that implementation walkthroughs are useful but incomplete without the theoretical lens.

**Tags**: `#LLMs`, `#positional-embeddings`, `#transformers`, `#group-theory`, `#machine-learning`

---

<a id="item-7"></a>
## [Blogger Argues All AI-Generated Code Should Be Open Source](https://jakub.jankiewicz.org/blog/ai-code-open-source/) ⭐️ 7.0/10

Jakub Jankiewicz published a blog post arguing that any code generated with the help of AI should be released under an open source license or Creative Commons Zero (CC0), on the grounds that the models themselves were trained on a massive corpus of open source code written since the GNU Project began. The post reached the front page of Hacker News, collecting over 1,000 upvotes and roughly 550 comments. The proposal strikes at the core commercial assumption behind AI coding assistants: that companies can keep AI-assisted output proprietary. If widely adopted, the norm would reshape how enterprises license software built with tools like Copilot or Cursor, and it feeds into the broader, still-unsettled debate over training data, copyright and open source reciprocity. The core argument is a reciprocity claim about training data rather than a strictly legal one, and commenters noted that US Copyright Office guidance holds that using AI to assist rather than stand in for human creativity does not by itself bar copyright protection for the output. Others pointed out that even if purely AI-generated code were uncopyrightable, that alone would not grant third parties any right to have it conveyed to them.

hackernews · jcubic · Nov 15, 14:46 · [Discussion](https://news.ycombinator.com/item?id=50507303)

**Background**: Modern AI coding assistants are trained on large volumes of publicly available source code, much of it under permissive or copyleft open source licenses, which has raised questions about whether their output inherits any licensing obligations. Separately, the U.S. Copyright Office has been publishing a multi-part report on AI: its January 2025 Part 2 addresses the copyrightability of generative AI outputs, and its March 2023 registration guidance requires applicants to disclose AI-generated content and exclude material beyond de minimis amounts. The post's author, Jakub Jankiewicz, frames the issue as a matter of fairness to the open source ecosystem that supplied the training data.

<details><summary>References</summary>
<ul>
<li><a href="https://www.copyright.gov/ai/">Copyright and Artificial Intelligence | U.S. Copyright Office</a></li>
<li><a href="https://jakub.jankiewicz.org/blog/ai-code-open-source/">All AI - generated code should be Open Source</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly split rather than hostile: one side cited US Copyright Office guidance that existing law already resolves AI copyrightability questions and that AI-assisted output remains protectable, while others argued AI is simply a tool like a compiler and that the direction, refinement and engineering effort over months constitutes substantial human authorship. A recurring counterargument was that by the post's logic, code using open source frameworks or learned from Stack Overflow should also be forced open, and that conflating writing code with software engineering ignores ownership and business risk; a further practical point was that what actually keeps proprietary code proprietary is the difficulty of extracting it from a company, not copyright alone.

**Tags**: `#ai`, `#open-source`, `#copyright`, `#licensing`, `#software-engineering`

---

<a id="item-8"></a>
## [Report: Lutnick Pushed to Weaken Chip Rules Tied to Family Business](https://www.nytimes.com/2026/11/15/us/politics/lutnick-pushed-to-weaken-chip-rules-that-overlap-with-his-family-business.html) ⭐️ 7.0/10

A New York Times report published on November 15, 2026 alleges that Commerce Secretary Howard Lutnick pushed to weaken U.S. chip export rules in areas that overlap with the business interests of his family's firm. The story frames the alleged push as raising both conflict-of-interest and national-security questions in how AI hardware policy is set. Export controls are the primary lever Washington uses to control access to advanced AI accelerators, so any perceived weakening of those rules can directly shape which countries and customers can obtain cutting-edge chips. Allegations that a sitting Commerce Secretary acted where his own family's financial interests were at stake could erode the credibility of the export-control regime and invite congressional scrutiny. The report centers on overlap between Lutnick's official decisions and the holdings of his family's firm, Cantor Fitzgerald, which he led before joining the government; the summary available here does not specify exactly which rules were targeted. The underlying claims are journalistic allegations, and community discussion references a Malaysian data center investment and Nvidia's Blackwell GPUs, details that are not independently confirmed by the material provided.

hackernews · JumpCrisscross · Nov 15, 11:40 · [Discussion](https://news.ycombinator.com/item?id=50506180)

**Background**: U.S. export controls on advanced semiconductors are administered by the Commerce Department's Bureau of Industry and Security, which maintains lists of restricted technologies and entities that determine what American-designed chips can be sold abroad, particularly to China. Because AI training clusters depend on a small number of high-end GPUs, these rules are the main chokepoint in the global AI hardware supply chain. Howard Lutnick, formerly CEO of the financial services firm Cantor Fitzgerald, became Commerce Secretary in 2025, putting him in charge of the agency that oversees those controls.

**Discussion**: Hacker News discussion (roughly 435 points and 188 comments) was overwhelmingly critical, with commenters describing Lutnick as ethically compromised from his Wall Street career and some accusing him of prioritizing his firm's interests over national security. A few replies widened the frame to broader cynicism about corruption in AI hardware policy, with one commenter noting that open-weight models were trained on Chinese-owned Nvidia GPUs and wondering what the counterfactual would look like.

**Tags**: `#AI chips`, `#export controls`, `#technology policy`, `#national security`, `#conflicts of interest`

---

<a id="item-9"></a>
## [Training-free early exit by editing one output-layer row](https://www.reddit.com/r/MachineLearning/comments/1xx1xdm/trainingfree_early_exit_for_reasoning_models_a/) ⭐️ 7.0/10

A Reddit project proposes a training-free early-exit method for reasoning models that adds a probe direction, scaled by 14, to the </think> token's weight row in the output layer, making the model stop thinking earlier. The author reports Qwen3.5-4B matching accuracy on 8 unseen MATH-500 problems with 54% fewer tokens and DeepSeek V4.1 Flash solving 7/7 vs 6/7 maths problems with 40% fewer tokens. If it generalizes, this could cut the costly overthinking phase of reasoning models at inference time without retraining, extra runtime code, or a custom inference stack, since the result is an ordinary weights file. That matters for anyone serving long chain-of-thought models where latency and token cost are dominated by redundant re-checking. The probe is fitted with linear discriminant analysis on hidden states from 24 maths problems, using paragraph ends after the correct answer appears as done labels; because only the </think> row changes, the author can simulate the edited model offline from recorded hidden states. The author acknowledges prior work on probe-based early stopping (Zhang et al. 2025, arXiv 2504.05419) and lists limitations: small samples, one run per setting, a maths-only probe, and an AIME 2025 comparison using a 32k-token budget below Qwen's recommended 81,920.

reddit · r/MachineLearning · /u/Good-Presentation-23 · Nov 15, 17:52

**Background**: Early exit is a general inference-efficiency idea: instead of always running a model to its full depth or full generation length, let it stop when an intermediate signal says the answer is good enough. A linear probe is a simple linear classifier fitted on a model's internal hidden states to detect a property, such as whether the model is still working or merely re-checking. Reasoning models such as DeepSeek and Qwen write a scratchpad before answering and end it with a special </think> token; their output layer scores each vocabulary token by multiplying its weight row with the current hidden state. The post combines these ideas by editing the single output-layer row for </think>, a lightweight form of model editing that changes behavior without retraining.

<details><summary>References</summary>
<ul>
<li><a href="https://intellabs.github.io/distiller/algo_earlyexit.html">Early Exit - Neural Network Distiller</a></li>
<li><a href="https://deepwiki.com/guijiejie/Attention-driven-Masking-and-Throwing/5.3-linear-probing">Linear Probing | DeepWiki</a></li>
<li><a href="https://www.researchgate.net/publication/386121431_A_Survey_on_Knowledge_Editing_of_Neural_Networks">(PDF) A Survey on Knowledge Editing of Neural Networks</a></li>

</ul>
</details>

**Tags**: `#LLM reasoning`, `#early exit`, `#model editing`, `#inference efficiency`, `#machine learning`

---

<a id="item-10"></a>
## [FAA Ground Stop Traced to Router Failure After Copper-to-Fiber Upgrade](https://www.theverge.com/transportation/1033898/faa-ground-stop-sean-duffy-faa-copper-wire) ⭐️ 7.0/10

US Transportation Secretary Sean Duffy said on November 14 that the FAA's nationwide ground stop ordered on Friday was triggered by routine maintenance at a remote facility that replaced aging copper wire with fiber, after which a newly installed router began flooding other routers with more than 1,000 connection requests every 4 to 5 seconds. The failure disrupted radar signals and aircraft communications and grounded thousands of flights; Duffy said the root cause remains unconfirmed and could be a hardware fault, a configuration error, or a mistake by contractor L3Harris. The incident shows how a single misbehaving device introduced during routine legacy modernization can cascade into a nationwide outage of a safety-critical system, grounding thousands of flights and even prompting European authorities to suspend US-bound departures. It strengthens the case for the FAA's multi-billion-dollar air traffic control overhaul and gives reliability engineers a concrete case study in the risks of swapping copper for fiber in critical networks. The trigger was a router that inundated its peers with connection requests at a rate of over a thousand every four to five seconds, overwhelming the network that carries radar data and air-ground communications. Duffy said investigators have not pinned down whether the fault lies in hardware, configuration, or contractor execution, and he used the press conference to call on Congress to approve additional funding for air traffic control modernization.

telegram · zaihuapd · Nov 15, 02:10

**Background**: The FAA has been replacing decades-old copper wiring across its facilities — from major air route traffic control centers to remote radar sites and weather stations — with high-speed fiber as part of its FAA Telecommunications Infrastructure (FTI) program, work carried out by contractor L3Harris. This modernization feeds into the broader Brand New Air Traffic Control System (BNATCS) effort, which aims to replace aging radar, software, hardware, and telecom networks by the end of 2028. Because many of these sites are unmanned and geographically isolated, a single faulty device there can still sit on the critical path for nationwide traffic management.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/2026_FAA_nationwide_ground_stop">2026 FAA nationwide ground stop - Wikipedia</a></li>
<li><a href="https://www.republicworld.com/world-news/us-air-travel-should-normalise-sunday-after-ground-stop-triggers-mass-cancellations-faa-2026-11-15-141088">US Air Travel Should Normalise Sunday After Ground... | Republic World</a></li>
<li><a href="https://www.l3harris.com/all-capabilities/faa-telecommunications-infrastructure-fti">FAA Telecommunications Infrastructure (FTI) - L3Harris</a></li>

</ul>
</details>

**Tags**: `#aviation`, `#network-outage`, `#infrastructure`, `#systems-reliability`, `#legacy-modernization`

---

<a id="item-11"></a>
## [Telegram Widgets Reportedly Vulnerable to Sandbox Escape and RCE](https://t.me/zaihuapd/45139) ⭐️ 7.0/10

A Telegram channel post warns that Telegram Widgets, introduced in Bot API 10.4 on November 9, 2026, contain a sandbox escape that could lead to remote code execution, and urges users to avoid unknown bots. If confirmed, the flaw would let a malicious bot run code on a user's device simply by displaying a widget in a chat, putting Telegram's large user base and bot ecosystem at risk. Widgets are self-contained HTML documents with inline CSS and JavaScript capped at 32 KB (4 KB compressed) and are supposed to run in a no-network sandbox; the post gives no CVE, affected client versions, or proof-of-concept, so the claim remains unverified.

telegram · zaihuapd · Nov 15, 10:51

**Background**: Telegram's Bot API lets third-party bots send messages, buttons, and other interactive content into chats. Bot API 10.4 added Widgets, which are small interactive HTML blocks rendered inside a message bubble on the user's device. Because widgets include JavaScript, Telegram apps must isolate them in a sandbox; a sandbox escape means malicious widget code breaks out of that isolation. Such vulnerabilities are serious because the widget is delivered through ordinary chat messages and may not require a separate app install.

<details><summary>References</summary>
<ul>
<li><a href="https://core.telegram.org/bots/widgets">Telegram Widgets</a></li>
<li><a href="https://core.telegram.org/bots/api-changelog">Bot API changelog - Telegram APIs Telegram Bot API 10.4 Explained: HTML Widgets and TON Wallet Telegram Bot API 10.4 introduces Interactive Message Widgets ... Telegram's Bot API 10.4 adds interactive mini-apps in chats Telegram обновил Bot API до версии 10.4: что нового Telegram widgets (Bot API 10.4): interactive cards inside ...</a></li>

</ul>
</details>

**Tags**: `#Telegram`, `#security vulnerability`, `#RCE`, `#Bot API`, `#JavaScript sandbox`

---

<a id="item-12"></a>
## [Study Claims Six Chinese AI Models Carry Blackwell Chip Fingerprints in Their Weights](https://t.me/zaihuapd/45140) ⭐️ 7.0/10

Unemployment Labs published an analysis claiming that six publicly released model weights from DeepSeek, Moonshot (月之暗面), MiniMax and Ant Group show initial parameter layouts consistent with initialization on Nvidia Blackwell GPUs. The researchers say the DeepSeek-V4-Flash result was reproduced on a physical B300 machine, and that Kimi K3 showed a highly correlated match on GB200 hardware. If hardware can be attributed from public model weights, it would give outside researchers a way to infer which GPUs were used to build frontier models — a capability with direct implications for export-control enforcement and AI supply-chain transparency. It would also undercut assumptions that chip usage inside Chinese labs is opaque to outsiders. The claim rests entirely on post hoc analysis of public model weights rather than any disclosure from the labs, and the replication so far amounts to correlated matches on B300 and GB200 machines rather than a peer-reviewed proof. The authors infer that the models were initialized on Blackwell hardware and speculate that the same chips also took part in training, a step beyond what a pure initialization fingerprint would establish.

telegram · zaihuapd · Nov 15, 11:08

**Background**: Model fingerprinting is a family of techniques for attributing a model to its origin by matching intrinsic evidence — parameter statistics, internal representations, or elicited behaviors — against known references, and it has mostly been studied for ownership and provenance verification rather than hardware attribution. Blackwell is Nvidia's GPU microarchitecture succeeding Hopper, shipping as parts such as the B200 and B300 as well as the GB200/GB300 Grace-Blackwell modules, and it is the class of hardware restricted under US export controls. The models named, including DeepSeek-V4-Flash and Kimi K3, are recent Chinese releases with open weights, which is what makes weight-level inspection possible at all.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2605.29245">Implicit Identity Technologies for LLMs: Fingerprinting and ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Blackwell_(microarchitecture)">Blackwell (microarchitecture) - Wikipedia</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#AI models`, `#hardware fingerprinting`, `#Nvidia Blackwell`, `#export controls`, `#model weights`

---

<a id="item-13"></a>
## [Huawei Cloud Launches Open-Source openPangu-2.1-Pro Model on MaaS Platform](https://mp.weixin.qq.com/s/8JfFmscBTDl_mPQMycD8Nw) ⭐️ 7.0/10

On November 15, Huawei Cloud officially launched the open-source Pangu model openPangu-2.1-Pro on its Model-as-a-Service (MaaS) platform, upgrading capabilities in three directions: Agent development, AI coding, and inference optimization. The model was tuned on over 100,000 specialized data samples to improve Skills triggering and tool calling, with particular focus on HarmonyOS ArkTS development and Ascend operator generation. This gives HarmonyOS and Ascend developers a first-party model that is tuned for their own toolchains rather than generic coding tasks, which could meaningfully speed up native HarmonyOS app development and Ascend kernel work. Low cache-hit input pricing at 0.016 yuan per million tokens also makes high-volume Agent workloads more economically viable on Huawei Cloud. Pricing is set at 0.8 yuan per million input tokens and 3.2 yuan per million output tokens, with cached input billed at just 0.016 yuan per million tokens. The model is being wired into internal products including AgentArts (智果), CodeArts (码道), and OfficeAce (果办), but Huawei has not published independent benchmark comparisons or model size details in this announcement.

telegram · zaihuapd · Nov 15, 16:03

**Background**: Huawei Cloud's MaaS (Model-as-a-Service) platform offers one-click access to pre-trained models for text generation, code generation, Q&A, and translation, so developers can call models via API instead of deploying their own infrastructure. ArkTS is Huawei's dedicated programming language for the HarmonyOS ecosystem, built on TypeScript syntax with stronger static checks, while Ascend is Huawei's own AI accelerator line whose operators often need hand-written optimization. The Pangu family is Huawei's in-house LLM series, and the "open" openPangu variants are positioned as publicly downloadable weights that can also be served on Huawei Cloud.

<details><summary>References</summary>
<ul>
<li><a href="https://1y.hk/en/post/11-15-openpangu-2-1-2jsl">Huawei Cloud to Launch openPangu - 2 . 1 - Pro on November 15 · AI Brief</a></li>
<li><a href="https://www.huaweicloud.com/intl/en-us/product/maas.html">Huawei Cloud MaaS - HUAWEI CLOUD</a></li>
<li><a href="https://developer.huawei.com/consumer/en/arkts/">ArkTS - HUAWEI Developers</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#Pangu`, `#LLM`, `#open-source AI`, `#Huawei Cloud`

---

<a id="item-14"></a>
## [Retrospective: Turbo Pascal's Tiny Footprint vs. Modern Software Bloat](https://prog21.dadgum.com/116.html) ⭐️ 6.0/10

A 2011 blog post from prog21.dadgum.com resurfaced, using Turbo Pascal—Borland's compact Pascal compiler and IDE—as a benchmark to show that many modern binaries, even trivial ones like the Unix `touch` command, are far larger than an entire 1980s development environment. The piece resurfaced on Hacker News, where commenters debated whether such byte-for-byte comparisons are meaningful. The discussion taps into a long-running debate about software bloat: as hardware has grown vastly more capable, developers increasingly trade binary size and runtime efficiency for productivity, abstraction layers, and features. For engineers working on embedded systems, minimal container images, or security-sensitive code, the question of how much complexity is truly necessary remains practically relevant. Turbo Pascal was famous for extremely fast single-pass compilation and shipped as a compact IDE plus compiler; Borland later released versions 1.0, 3.02, and 5.5 for DOS free of charge due to their historical interest. Critics in the thread noted that raw byte comparisons ignore differing functionality, platform conventions, and the real costs of creation, storage, and transfer that have changed dramatically since the 1980s.

hackernews · ksec · Nov 15, 13:44 · [Discussion](https://news.ycombinator.com/item?id=50506894)

**Background**: Turbo Pascal was a compiler and integrated development environment for the Pascal language on CP/M and MS-DOS, originally written by Anders Hejlsberg at Borland and first released in 1983; its speed and small size made Borland a leading PC development-tool vendor. Software bloat describes the tendency of successive program versions to consume more disk space, memory, and CPU while quality stagnates, often caused by feature creep, added abstraction layers, or de-prioritizing optimization.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Turbo_Pascal">Turbo Pascal - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Software_bloat">Software bloat</a></li>

</ul>
</details>

**Discussion**: Commenters praised Anders Hejlsberg as one of the greatest language designers, citing Turbo Pascal, Delphi, C#, and TypeScript, while others questioned why Pascal faded despite its influence. Several argued that even trivial utilities like `touch` should not exceed Turbo Pascal in size and blamed repeated boilerplate and developer laziness, whereas skeptics called the comparisons senseless because bytes have different historical context, utility, and cost.

**Tags**: `#software-bloat`, `#turbo-pascal`, `#programming-languages`, `#software-history`, `#hacker-news-discussion`

---

<a id="item-15"></a>
## [Blogger Swaps His Conventional Browser for Emacs' eww, Sparking HN Debate](https://joshblais.com/blog/emacs-as-my-browser/) ⭐️ 6.0/10

Josh Blais published a blog post on joshblais.com titled "Emacs Is My Browser," describing how he uses eww — the text-based web browser built into Emacs — as his everyday way of reading the web instead of a conventional browser. The post drew roughly 80 substantive comments on Hacker News, where readers swapped tricks and argued about the approach's limits. The write-up is a concrete case study in minimal, keyboard-driven computing, and the discussion around it lays out plainly where that philosophy collides with today's JavaScript-heavy commercial web. It matters most to Emacs users and to developers weighing how much of the modern web they actually need a full browser to read. eww renders HTML into plain Emacs buffers without running JavaScript, so static HTML and blogs work well while Reddit and most commercial sites break or degrade badly. Commenters pointed to partial workarounds such as embedding WebKit through Emacs' xwidget support, or falling back to lightweight browsers like Dillo and w3m-mode.

hackernews · nyc111 · Nov 15, 15:21 · [Discussion](https://news.ycombinator.com/item?id=50507553)

**Background**: Emacs is a highly extensible, scriptable text editor that many programmers use as a full working environment for editing, email, terminal sessions and more. eww (the "Emacs Web Wowser") is a browser built into Emacs that fetches a page and renders its HTML as formatted text inside an Emacs buffer, rather than in a graphical browser window. Because it lives inside the editor, it appeals to people who want to stay in one keyboard-centric environment without a separate application — the same minimalist ethos associated with Richard Stallman's free-software advocacy, though Stallman's own reason for avoiding browsers is ideological rather than about focus.

<details><summary>References</summary>
<ul>
<li><a href="https://planet.emacslife.com/">Planet Emacslife</a></li>
<li><a href="https://en.wikipedia.org/wiki/Richard_Stallman">Richard Stallman - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly sympathetic but realistic: Arubis stressed that the modern commercial web "does not play nice" with this setup, so it is fine for static HTML and blogs but not for Reddit or commercial sites. Others shared practical hacks — kmstout plugged a follow-mode-based columnar display for fitting more text on screen, krylon described reviving an old laptop with w3m-mode for reading Wikipedia, and jll29 noted that Stallman browses by having pages emailed to him out of ideology; leoc argued the real need is a content-addressable replacement for HTTP(S).

**Tags**: `#emacs`, `#web-browsing`, `#eww`, `#developer-tooling`, `#hackernews-discussion`

---

<a id="item-16"></a>
## [Marimba: an open-weight 'System One' speech model built on frozen Qwen3-ASR](https://www.reddit.com/r/MachineLearning/comments/1xwzsm4/marimba_a_system_one_model_for_speech_r/) ⭐️ 6.0/10

A developer released Marimba, an open-weight (Apache-2.0), pip-installable model ('marimba-audio') that sits on top of a frozen Qwen3-ASR-0.6B and returns typed decisions — yes/no, a chosen option, or a score — instead of transcripts. Word- and language-level questions are answered via zero-shot scores derived from the ASR decoder's hypotheses plus calibration, while small readouts on the frozen encoder handle voice activity detection, turn endings, speaker changes and speaker count; a paper is promised on arXiv the same week. It shows a practical way to squeeze many lightweight speech decisions out of an existing small ASR checkpoint without retraining the backbone, which lowers the cost and barrier for building always-on voice interfaces such as VAD, turn-taking and language routing. Open weights plus a pip package make it easy for others to reproduce and extend, even though validation is still limited at this stage. The backbone is frozen, so all adaptation happens in calibration or small readout heads rather than in the ASR model itself, which keeps the system lightweight but likely caps accuracy on tasks far from transcription. Details such as benchmark numbers, latency and robustness across noise conditions are not yet fully documented since the paper is still pending, and the project is a single-developer effort.

reddit · r/MachineLearning · /u/solanotodesch · Nov 15, 16:30

**Background**: Qwen3-ASR-0.6B is a compact open ASR model from the Qwen3-ASR family, which also includes a 1.7B variant; it supports multilingual transcription and language identification and is built on the audio understanding capability of Qwen3-Omni. The term 'System One' comes from TypeSafe AI's Jev, describing a class of models designed to make fast, structured judgments software can consume directly, as opposed to slower deliberate reasoning. Marimba adapts this idea to audio, also drawing on the common technique of linear probing — training a simple classifier on frozen activations to test whether a concept is linearly decodable.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3-ASR-0.6B">Qwen/Qwen3-ASR-0.6B · Hugging Face</a></li>
<li><a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">Introducing System One Models & Jev - TypeSafe AI Blog</a></li>
<li><a href="https://ai-math-map.vercel.app/methods/linear-probing">Linear probing — Math in LLMs Research Map</a></li>

</ul>
</details>

**Tags**: `#speech-recognition`, `#asr`, `#small-models`, `#open-weights`, `#audio-classification`

---

<a id="item-17"></a>
## [Tesla to Start Selling Two-Seat Cybercab by Year-End, Fleet First](https://t.me/zaihuapd/45131) ⭐️ 6.0/10

On its third-quarter earnings call on Wednesday, Tesla said it will begin selling the Cybercab to customers before the end of this year. Vehicle engineering vice president Lars Moravy said all current production is going to Tesla's own robotaxi fleet, after which the company will deliver fully autonomous vehicles to customers at small scale. This is the first time Tesla has put a timeline on selling its purpose-built robotaxi, signaling that a vehicle designed with no steering wheel is moving from concept toward a commercial product. It also puts Tesla's sales model on a collision course with federal safety regulators at a moment when its ride-hailing service is still small and its unsupervised self-driving software remains unfinished. The two-seat Cybercab has no steering wheel or pedals and relies on a camera-only autonomous driving system, and it is currently the subject of an NHTSA inquiry into whether it complies with federal safety standards. Musk has said the Cybercab is intended mainly as a ride-hailing service rather than a personal purchase, and unsupervised FSD is now pushed back to the second quarter of next year.

telegram · zaihuapd · Nov 15, 01:10

**Background**: Under US law, automakers self-certify that their vehicles meet the Federal Motor Vehicle Safety Standards, and NHTSA can later audit the basis for that certification — which is what Tesla now faces over a vehicle built without driver controls. Tesla unveiled the Cybercab in October 2024 as a purpose-built robotaxi, distinct from its consumer cars that run the driver-monitored 'Full Self-Driving (Supervised)' software. Until now, Tesla's paid robotaxi rides have been operated by the company itself rather than through vehicles sold to individuals.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tesla_Cybercab">Tesla Cybercab</a></li>
<li><a href="https://www.nhtsa.gov/vehicle-safety/automated-vehicle-safety">Automated Vehicle Safety - NHTSA</a></li>
<li><a href="https://electrek.co/2026/04/22/tesla-elon-musk-unsupervised-fsd-consumer-cars-q4-delay-again/">Elon Musk pushes unsupervised FSD for consumer Teslas — again</a></li>

</ul>
</details>

**Tags**: `#Tesla`, `#Cybercab`, `#autonomous driving`, `#robotaxi`, `#regulation`

---

<a id="item-18"></a>
## [US Judge Denies Micron, Samsung, SK Hynix Bid to Dismiss DRAM Price-Fixing Suit](https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge) ⭐️ 6.0/10

US District Judge Noël Wise denied a motion by Micron, Samsung, and SK Hynix to dismiss a DRAM price-fixing class action, ruling that the plaintiffs presented plausible new evidence of collusion. The plaintiffs — 17 individuals and small businesses — allege the three chipmakers took four parallel actions within a single year to restrict DRAM supply, driving prices up by as much as 500%. The ruling pushes the case past its earliest hurdle and into discovery, where internal pricing and supply-planning communications from the three firms that control roughly all global DRAM output could be exposed. Because DRAM feeds into nearly every PC, phone, and server, any finding of collusion could reshape memory pricing, procurement contracts, and antitrust scrutiny across the tech industry. Judge Wise characterized the three firms' synchronized behavior as resembling "hawks flying in formation" rather than independent decisions, which is significant because parallel conduct alone normally does not prove an antitrust agreement under US law. The defendants must respond by December 7, with a case management conference scheduled for January 2027, and the denial of a motion to dismiss is a procedural step that does not establish liability.

telegram · zaihuapd · Nov 15, 16:39

**Background**: DRAM (dynamic random-access memory) is the mainstream semiconductor memory used as the main working memory in computers, phones, and servers, and the market has consolidated into essentially three suppliers: Samsung, SK Hynix, and Micron. US antitrust law requires evidence of an actual agreement rather than mere conscious parallelism, so plaintiffs typically must show additional "plus factors" such as simultaneous capacity cuts or suspicious communications. A motion to dismiss is an early procedural request asking a court to throw out a case before discovery; denying it means the plaintiffs' allegations are plausibly supported, not that wrongdoing has been proven.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/动态随机存储器">动态随机存储器 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.fapingedu.com/sys-nd/11907.html">法律英语知识之 Motion （ 动 议 ） - 法平教育</a></li>

</ul>
</details>

**Tags**: `#DRAM`, `#semiconductors`, `#antitrust`, `#hardware-supply-chain`, `#legal`

---