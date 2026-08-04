---
layout: default
title: "Horizon Summary: 2026-08-05 (EN)"
date: 2026-08-05
lang: en
---

> From 38 items, 10 important content pieces were selected

---

1. [A Simple Color Space for Generating Diverse Skin Tones](#item-1) ⭐️ 8.0/10
2. [DeepSeek V4 Flash Runs on Single AMD MI300X at 150+ tok/s](#item-2) ⭐️ 8.0/10
3. [Keyv and related npm packages hit in active Shai-Hulud supply chain attack](#item-3) ⭐️ 8.0/10
4. [Xbox Outage Blocks Disc-Based Games, Reigniting DRM Debate](#item-4) ⭐️ 8.0/10
5. [Engineering AI Agent Harnesses for Self-Improvement](#item-5) ⭐️ 8.0/10
6. [MiniMax-H3 Omni-Modal Model Runs on Apple Silicon via MLX Port](#item-6) ⭐️ 8.0/10
7. [Kimi K3 Unveils Novel Architecture with Compressed Memory and Latent Routing](#item-7) ⭐️ 8.0/10
8. [Russia requires Apple to support RuStore on iPhones from Sept 2025](#item-8) ⭐️ 8.0/10
9. [Huawei Proposes Tao's Law, Replacing Geometric Scaling with Time Scaling](#item-9) ⭐️ 8.0/10
10. [Google builds $200B Wall Street financing machine for Anthropic](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [A Simple Color Space for Generating Diverse Skin Tones](https://toneyalexander.github.io/inclusive-color-space/) ⭐️ 8.0/10

A developer has released a new color space and algorithm for generating diverse, believable skin tones. The project includes interactive JavaScript demos, detailed explanations, and a procedural generation implementation in Python. This gives digital artists and game developers a fast, accessible way to generate realistic skin tones for any character, reducing a common pain point in creative workflows. It also aligns with broader industry moves toward inclusive color tools, such as Google's Monk Skin Tone Scale. The color space was constructed from real skin tone data, using a hand-fitted mathematical function rather than a data-driven method like PCA. The author openly discusses methodological limitations and a Future Work section, and provides the equations used in the space.

hackernews · automatoney · Aug 4, 15:16 · [Discussion](https://news.ycombinator.com/item?id=49170165)

**Background**: Skin color is a complex mix of physical and perceptual factors, such as lighting, so it cannot be captured accurately by simple RGB coordinates. Perceptually uniform spaces such as Oklab arrange colors to match human perception and are used to analyze skin tone data. Existing initiatives like Google's Monk Skin Tone Scale focus on AI fairness, while this tool targets creative workflows like digital art and game development.

<details><summary>References</summary>
<ul>
<li><a href="https://toneyalexander.github.io/inclusive-color-space/">What Colors Are We? Constructing A Color Space For Skin Tones</a></li>
<li><a href="https://skintone.google/">Skin Tone Research @ Google</a></li>
<li><a href="https://buzzverified.com/diverse-skin-tones-algorithm/">Diverse Skin Tones Algorithm - buzzverified.com</a></li>

</ul>
</details>

**Discussion**: Commenters were largely positive, praising the presentation and the 'slick' hand-fitted function approach. Some noted that skin tones depend heavily on lighting, so blue skin can be valid in moonlight, and suggested referencing existing standards like Pantone Skin Tones. Another commenter found that real foundation shades form a crescent in Oklab, matching the article's shape.

**Tags**: `#color space`, `#skin tones`, `#procedural generation`, `#digital art`, `#color science`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash Runs on Single AMD MI300X at 150+ tok/s](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

A GitHub project demonstrates DeepSeek V4 Flash running on a single AMD MI300X GPU with full weights at over 150 tokens per second, albeit with a reduced 256K context window instead of the original 1M. This shows that a large 284B-parameter MoE model can be served on a single commodity accelerator with high throughput, which could lower the hardware barrier for running frontier-class LLMs. It also highlights the practical tradeoffs between context length, quantization, and inference speed in real-world deployments. DeepSeek V4 Flash is a Mixture-of-Experts model with 284B total and 13B activated parameters, natively supporting a 1M-token context. The single-MI300X setup uses full weights without aggressive quantization but sacrifices 75% of the context window to fit in the GPU's 192GB HBM.

hackernews · zhoutong · Aug 4, 10:00 · [Discussion](https://news.ycombinator.com/item?id=49166386)

**Background**: DeepSeek V4 Flash is an efficiency-optimized Mixture-of-Experts model from DeepSeek, with 284B total parameters and 13B activated per token, designed for a 1M-token context. The AMD Instinct MI300X is a data-center GPU with 192GB of HBM3 memory, larger than NVIDIA's H100 (80GB), making it attractive for running large language models without multi-GPU sharding. MoE models activate only a subset of parameters per token, reducing compute cost while keeping high capacity.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash">DeepSeek V 4 Flash - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://moreh.io/technical-report/moreh-vllm-performance-evaluation-deepseek-v3-r1-671b-on-amd-instinct-mi300x-gpus-250829/">Moreh vLLM Performance Evaluation: DeepSeek V3/R1 671B on AMD ...</a></li>

</ul>
</details>

**Discussion**: Commenters noted that the MI300X is not sold as a single unit but rather in an 8-GPU chassis costing roughly €250K, and suggested the upcoming MI350P (a PCIe card with 144GB) as a more accessible alternative. Others compared the work to the prior art DwarfStar and discussed whether MXFP4-quantized versions would fit in smaller memory, while one user praised the practical 256K context tradeoff, noting it matches the range used by Codex.

**Tags**: `#deepseek`, `#AMD MI300X`, `#inference optimization`, `#MoE`, `#LLM deployment`

---

<a id="item-3"></a>
## [Keyv and related npm packages hit in active Shai-Hulud supply chain attack](https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack) ⭐️ 8.0/10

The npm package Keyv and related 'friends' packages have been compromised in an active Shai-Hulud supply chain attack. The self-replicating worm is spreading through the npm ecosystem and GitHub repositories, putting downstream users at risk. Keyv is a widely used key-value storage library, so its compromise can affect many JavaScript projects that depend on it. This incident exposes systemic risks in the npm dependency ecosystem and underscores the need for stronger supply chain defenses. The Shai-Hulud worm is active and uses compromised npm packages and GitHub repositories to propagate, with Shai-Hulud 2.0 reportedly exposing secrets in over 25,000 repositories. Developers are advised to disable install scripts, scrutinize packages that add pre-install hooks, and use isolation practices.

hackernews · cimi_ · Aug 4, 11:01 · [Discussion](https://news.ycombinator.com/item?id=49166874)

**Background**: Keyv is a simple key-value storage npm package that supports multiple storage backends and is commonly used in Node.js projects. The Shai-Hulud attack is a supply chain attack that injects malicious code into widely used packages, often via install hooks, so that anyone running npm install can be compromised. Because the npm ecosystem relies heavily on transitive dependencies, a single popular package being compromised can cascade into many downstream applications.

<details><summary>References</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/security/blog/2025/12/09/shai-hulud-2-0-guidance-for-detecting-investigating-and-defending-against-the-supply-chain-attack/">Shai-Hulud 2.0: Guidance for detecting, investigating, and ...</a></li>
<li><a href="https://unit42.paloaltonetworks.com/npm-supply-chain-attack/">" Shai-Hulud " Worm Compromises npm Ecosystem in Supply Chain ...</a></li>
<li><a href="https://www.wiz.io/blog/shai-hulud-2-0-ongoing-supply-chain-attack">Shai-Hulud 2.0 Supply Chain Attack : 25K+ Repos Exposing Secrets</a></li>

</ul>
</details>

**Discussion**: Community commenters expressed frustration with the fragile npm dependency system, saying supply chain attacks like this are hard to clean up and often cause knock-on compromises. Several called for killing or restricting pre-install and post-install hooks, while others recommended practical mitigations such as setting a minimum package release age and using isolated development environments.

**Tags**: `#security`, `#supply-chain`, `#npm`, `#open-source`, `#malware`

---

<a id="item-4"></a>
## [Xbox Outage Blocks Disc-Based Games, Reigniting DRM Debate](https://birchtree.me/blog/xbox-goes-down-you-cant-play-games-you-own-on-disc/) ⭐️ 8.0/10

A recent Xbox service outage made even disc-based games unplayable, as the console required server authentication to launch them. The incident exposed how games that appear to be physical copies still depend on online servers. This matters because it undermines the assumption that owning a physical disc guarantees access to the game. It fuels the ongoing debate about digital ownership, DRM, and whether consumers truly own the games they buy. Almost all modern Xbox consoles require an online connection and server authentication even for disc-based titles, effectively making every game an always-online product. This creates a single point of failure: when servers go down, even previously playable disc games become inaccessible.

hackernews · surprisetalk · Aug 4, 12:01 · [Discussion](https://news.ycombinator.com/item?id=49167448)

**Background**: Always-online DRM is a form of digital rights management that requires a persistent internet connection and server authentication to use a product. While intended to prevent piracy, it has been criticized for punishing legitimate users when servers fail, and for eroding the concept of ownership — consumers often buy a license, not the game itself.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Always-online_DRM">Always-online DRM</a></li>
<li><a href="https://www.pcgamingwiki.com/wiki/List_of_games_using_Always_Online_DRM">List of games using Always Online DRM - PCGamingWiki</a></li>

</ul>
</details>

**Discussion**: HN commenters were largely critical of the gaming industry's move toward server-dependent ownership. One user noted that older consoles like the PS3 still host multiplayer on user consoles, while another argued the real issue is ownership, not physical vs digital: buyers should be able to keep, resell, and archive what they buy.

**Tags**: `#digital ownership`, `#DRM`, `#gaming`, `#Xbox`, `#cloud services`

---

<a id="item-5"></a>
## [Engineering AI Agent Harnesses for Self-Improvement](https://lilianweng.github.io/posts/2026-07-04-harness/) ⭐️ 8.0/10

Lilian Weng published a technical deep-dive on harness engineering, arguing that the surrounding layer around AI agents — prompts, tools, context, and evaluation — is a key lever for improving performance, quality, and cost-efficiency. The post frames this as a new frontier for agent self-improvement beyond merely upgrading model weights. As model training improvements slow, engineering the harness offers a practical path to squeeze more capability out of existing LLM agents. This matters for developers and teams building agentic systems, because small changes to the harness can yield large gains in reliability and cost. The discussion points to practical details like optimizing AGENTS.md, skills, and tools, and to the need for a generic, reliable fitness function for codebases. Some commenters are already applying hillclimbing-style experiments to improve their harnesses in production systems.

hackernews · tosh · Aug 4, 06:17 · [Discussion](https://news.ycombinator.com/item?id=49164896)

**Background**: An LLM agent typically combines a language model with external scaffolding: system prompts, tool definitions, context management, and feedback loops. This scaffolding is often called the 'harness' — it determines how the model perceives its task and what actions it can take. Self-improving agents aim to use loops of planning, acting, and evaluating to get better over time. Harness engineering treats that surrounding layer as a design surface for optimization.

<details><summary>References</summary>
<ul>
<li><a href="https://www.andela.com/publication/inside-the-architecture-of-self-improving-llm-agents">Inside the architecture of self - improving LLM agents</a></li>
<li><a href="https://www.linkedin.com/pulse/what-happens-when-llm-agents-evolve-themselves-andela-ysehe">How to Build Self - Improving AI Agents That Think in Loops</a></li>
<li><a href="https://github.com/wronai/ellma">GitHub - wronai/ellma: Evolutionary Local LLM Agent - Self - improving ...</a></li>

</ul>
</details>

**Discussion**: Commenters were largely positive and practical, sharing real experiments and tools rather than just theory. One user stressed that defining 'quality' and building a generic fitness function is the first step, while another argued that the next big paradigm is training prompts and code rather than model weights. Others shared personal harness-building projects and noted the blog helped improve their own harness-engineering skills.

**Tags**: `#AI`, `#LLM agents`, `#harness engineering`, `#software engineering`, `#self-improvement`

---

<a id="item-6"></a>
## [MiniMax-H3 Omni-Modal Model Runs on Apple Silicon via MLX Port](https://simonwillison.net/2026/Aug/4/minimax-h3-mlx/#atom-everything) ⭐️ 8.0/10

MiniMax released MiniMax-H3, a general-purpose omni-modal generative system, and a community MLX port (PipeNetwork/minimax-h3-mlx) now lets it run on Apple Silicon. Simon Willison successfully generated a 15-second video clip with audio on an M5 Max MacBook Pro using the port. This makes a state-of-the-art omni-modal model accessible to Apple users without cloud dependencies, lowering the barrier for local AI video generation. It also demonstrates MLX's growing ecosystem as a practical framework for running large generative models on consumer hardware. The model requires downloading about 115 GB of model files, and generating the video took just under 45 minutes. The example output had 'weird speech-like garbage' audio because no prompt guidance was given for the audio track; the official prompting guide explains how to improve results.

rss · Simon Willison · Aug 4, 19:10

**Background**: MiniMax-H3 is an omni-modal generative model that accepts text, images, audio, and video as input and can generate up to 15-second video clips with audio. MLX is an open-source array framework developed by Apple for machine learning on Apple Silicon, providing a NumPy-like API. This port adapts MiniMax-H3 to MLX, enabling local execution on Macs with Apple Silicon.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/MiniMaxAI/MiniMax-H3">MiniMaxAI/MiniMax-H3 · Hugging Face</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks and Modalities - MiniMax Research | MiniMax</a></li>
<li><a href="https://opensource.apple.com/projects/mlx/">MLX</a></li>

</ul>
</details>

**Tags**: `#omni-modal`, `#MLX`, `#video generation`, `#MiniMax-H3`, `#Apple Silicon`

---

<a id="item-7"></a>
## [Kimi K3 Unveils Novel Architecture with Compressed Memory and Latent Routing](https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the) ⭐️ 8.0/10

SemiAnalysis published a technical deep-dive into Kimi K3, describing an LLM architecture that combines compressed memory, attention across depth, latent expert routing, and inference performance improvements. The piece highlights K3 as a distinctive design in the frontier LLM landscape. Kimi K3's architectural innovations could improve inference efficiency and long-context handling, key bottlenecks for deploying large models. If the design proves effective, it may influence how other labs optimize memory, routing, and attention in next-generation LLMs. The architecture reportedly uses compressed memory to reduce KV-cache overhead, attention across depth to strengthen information flow between layers, and latent expert routing to dynamically select computations. SemiAnalysis focuses on the inference performance implications rather than benchmark scores.

rss · Semianalysis · Aug 3, 19:42

**Background**: Compressed memory techniques shrink the memory footprint of KV caches or model weights, lowering inference cost. Attention across depth extends the standard Transformer attention mechanism to operate between layers, and latent expert routing uses learned latent representations to route inputs to specialized experts. These concepts build on established Transformer and mixture-of-experts research while applying them in novel combinations.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2502.15443">[2502.15443] When Compression Meets Model Compression: Memory-Efficient Double Compression for Large Language Models</a></li>
<li><a href="https://d2l.ai/chapter_attention-mechanisms-and-transformers/transformer.html">11.7. The Transformer Architecture — Dive into Deep Learning 1.0.3 documentation</a></li>
<li><a href="https://github.com/MilkThink-Lab/Awesome-Routing-LLMs">GitHub - MilkThink-Lab/Awesome-Routing-LLMs: A curated list of awesome works in Routing LLMs paradigm (👉 Welcome to submit your contributions to this code repository)</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLM`, `#architecture`, `#inference`, `#memory`

---

<a id="item-8"></a>
## [Russia requires Apple to support RuStore on iPhones from Sept 2025](https://t.me/zaihuapd/42963) ⭐️ 8.0/10

Russia's State Duma passed a law on June 26, 2025, in its third and final reading, requiring Apple to allow users to install RuStore on iPhones and iPads starting September 1, 2025. The law forbids Apple and Google from imposing installation restrictions, blocking alternative features, forcing developer pricing, or restricting payment methods. This breaks the App Store's monopoly in Russia and forces Apple to open its iOS ecosystem to a state-backed third-party marketplace. It could set a precedent for other governments seeking to regulate app store dominance. The legislation applies to Apple devices sold or used in Russia and covers third-party software installation and updates, while also banning restrictions on alternative payment methods and forced developer pricing. RuStore previously targeted Android and HarmonyOS devices; the new law expands this requirement to Apple's iOS ecosystem.

telegram · zaihuapd · Aug 4, 05:25

**Background**: RuStore is a Russian government-backed app store launched in May 2022 by VK, with support from Russia's Ministry of Digital Development. It was created after Western sanctions led many foreign platforms to restrict services in Russia, and Russian authorities have increasingly required local apps to be preinstalled on devices sold in the country. The new law extends these requirements from Android to Apple's iOS, directly challenging the App Store's exclusive control over app distribution.

<details><summary>References</summary>
<ul>
<li><a href="https://meduza.io/en/feature/2025/06/27/an-app-store-ultimatum">An App Store ultimatum New legislation will require Apple to open iPhones and iPads to Russia’s state-backed marketplace — Meduza</a></li>
<li><a href="https://iphonewired.com/news/984725/">Effective in September: New Russian regulations require iPhone/iPad and other Apple devices to support the installation of third-party app stores RuStore - iPhone Wired</a></li>
<li><a href="https://asoworld.com/en/aso-glossary/rustore/">RuStore -ASOWorld UK</a></li>

</ul>
</details>

**Tags**: `#Regulation`, `#App Store`, `#Apple`, `#Russia`, `#RuStore`

---

<a id="item-9"></a>
## [Huawei Proposes Tao's Law, Replacing Geometric Scaling with Time Scaling](https://t.me/zaihuapd/42966) ⭐️ 8.0/10

At the 2026 IEEE International Symposium on Circuits and Systems in Shanghai, Huawei unveiled 'Tao's Law,' a new semiconductor scaling principle that replaces geometric scaling with temporal scaling. Huawei claims it has designed and mass-produced 381 chips using this approach over the past six years, and a new Kirin smartphone chip using 'logic folding' technology is expected this fall. Tao's Law challenges the long-dominant Moore's Law paradigm, offering a potential path forward as geometric scaling approaches physical limits. If validated, it could reshape the global semiconductor race by giving Huawei and China an alternative route beyond Western-controlled process technology. Tao's Law focuses on systematically reducing the characteristic time constant across every layer of the electronic system, from transistor switching to system-level response. Huawei predicts that by 2031, high-end chips developed under this law could achieve a transistor density equivalent to that of a 1.4nm process, though the company has not disclosed full technical specifics of 'logic folding.'

telegram · zaihuapd · Aug 4, 08:04

**Background**: Moore's Law traditionally predicts that the number of transistors on a chip doubles roughly every two years, driven by geometric scaling that shrinks feature sizes. However, as transistors approach atomic limits, this scaling has slowed, and RC delay—caused by resistance and capacitance in interconnects—has become a major bottleneck. Tao's Law proposes a different optimization target: instead of shrinking physical dimensions, it compresses the time constant for signal transmission, achieving performance gains through multi-level temporal optimization across devices, circuits, chips, and systems.

<details><summary>References</summary>
<ul>
<li><a href="https://xtechpioneer.com/huawei-proposes-new-semiconductor-law-tao-scaling-replaces-geometry-to-fold-time/">Huawei Proposes New Semiconductor Law : ‘ Tao Scaling ’ Replaces...</a></li>
<li><a href="https://chinarxiv.org/items/chinaxiv-202605.00224">A Time Scaling Theory for Multi-Layer Electronic Systems</a></li>
<li><a href="https://en.wikipedia.org/wiki/RC_time_constant">RC time constant - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#Huawei`, `#Moore's law`, `#chip design`, `#technology`

---

<a id="item-10"></a>
## [Google builds $200B Wall Street financing machine for Anthropic](https://www.ft.com/content/549f2e23-5aa2-49c7-9ea6-a9784ab7087c) ⭐️ 8.0/10

A Financial Times investigation published on August 4 found that Google has quietly assembled one of the largest infrastructure-financing structures in history, worth roughly $200 billion, to deliver AI chips to Anthropic. In June, a special purpose vehicle called Compute SPV completed its first transactions, buying about $35 billion of hardware. This is a landmark in AI infrastructure finance: it lets Anthropic, which has no credit rating, access massive computing power while keeping $200 billion in hardware off the balance sheets of the companies involved. It may become a template for how AI companies fund compute and for vendor financing in the broader industry. Risk is shared because Anthropic lacks a credit rating: Google backs data centers, Broadcom buys and helps finance chips, while Apollo and Blackstone buy hardware and lease it back to Anthropic. The first Compute SPV deals in June covered roughly 1 gigawatt of compute and 1 million TPUs.

telegram · zaihuapd · Aug 4, 10:52

**Background**: A special purpose vehicle (SPV) is a separate legal entity created to hold assets, manage risk, or raise money for a specific project, isolating financial risk from parent companies. The deal resembles vendor financing, a model popularized by manufacturers like Boeing and GE to help customers buy expensive equipment such as aircraft and engines. Here, Google, Broadcom, and investors use SPVs to fund huge AI hardware purchases without any single party taking the full burden onto its own balance sheet.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Special-purpose_entity">Special-purpose entity - Wikipedia</a></li>
<li><a href="https://www.investopedia.com/terms/s/spv.asp">Special Purpose Vehicle (SPV): Definition and Reasons Companies Use Them</a></li>
<li><a href="https://www.cscglobal.com/service/entity-solutions/spv-management/guide-to-special-purpose-vehicles-spvs/">Special Purpose Vehicles (SPVs) Guide | CSC</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Google`, `#Anthropic`, `#Finance`, `#Infrastructure`

---