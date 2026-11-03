---
layout: default
title: "Horizon Summary: 2026-11-03 (EN)"
date: 2026-11-03
lang: en
---

> From 39 items, 23 important content pieces were selected

---

1. [GPT-6 Astra Reads and Edits Qwen Weights, Boosting Math Scores Nearly Sixfold](#item-1) ⭐️ 9.0/10
2. [vLLM v0.33.0rc3 upgrades to PyTorch 2.14, drops CUDA 12.9 builds](#item-2) ⭐️ 8.0/10
3. [Subvocal's RF smart glasses turn silent mouthing into text](#item-3) ⭐️ 8.0/10
4. [Ubuntu LTS kernels still unpatched for critical Linux 0day RCE after three weeks](#item-4) ⭐️ 8.0/10
5. [Blog claims frontier LLMs can read and write raw neural network weights](#item-5) ⭐️ 8.0/10
6. [Raspberry Pi 5 Launches With 2.4GHz Cortex-A76 and Dual 4K60 HDMI](#item-6) ⭐️ 8.0/10
7. [Blog Post Urges Readers to Back Up Beloved Websites](#item-7) ⭐️ 7.0/10
8. [Show HN: Interactive voxel 3D map of central Warsaw built from open data](#item-8) ⭐️ 7.0/10
9. [GDPx Launches Frontier Benchmark Across High-Value Domains](#item-9) ⭐️ 7.0/10
10. [Laptop-scale replication backs 'good views beat next-token prediction' for vision-language alignment](#item-10) ⭐️ 7.0/10
11. [LightMIS: 131K-Parameter Medical Segmentation Model Runs 10.5× Faster on Edge GPU](#item-11) ⭐️ 7.0/10
12. [LongCat-2.5 released: a 1.6-trillion-parameter native multimodal model](#item-12) ⭐️ 7.0/10
13. [Baidu Netdisk shake-to-jump ads switch to magnetometer-based CLHeading to dodge iOS motion blocks](#item-13) ⭐️ 7.0/10
14. [ChatGPT share-link flaw let attackers hijack sessions and leak private chats](#item-14) ⭐️ 7.0/10
15. [WIRED Finds 400+ AI Apps Hiding Sexual Deepfake Tools Behind Mundane Features](#item-15) ⭐️ 7.0/10
16. [Cyberattack Sets ICA Store Freezers to 50°C Remote in Sweden](#item-16) ⭐️ 7.0/10
17. [Abu Dhabi Signs Four OpenAI Deals, Including 'Machine-Readable Government'](#item-17) ⭐️ 7.0/10
18. [SGLang v0.5.23 ships 1,007 PRs, new models and TPU7x support](#item-18) ⭐️ 6.0/10
19. [LLM 0.37 adds OpenAI-compatible endpoint command and multimodal embeddings](#item-19) ⭐️ 6.0/10
20. [Census AI Adoption Chart Rerun Highlights 'Super Intelligence' Order Clash](#item-20) ⭐️ 6.0/10
21. [Researcher asks how to report a failed reproduction of a published ML baseline](#item-21) ⭐️ 6.0/10
22. [Anthropic Updates Usage Policy to Ban Reselling Claude Access](#item-22) ⭐️ 6.0/10
23. [DeepSeek Harness team proposes Super-agent architecture with a persistent Router and isolated Workers](#item-23) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [GPT-6 Astra Reads and Edits Qwen Weights, Boosting Math Scores Nearly Sixfold](https://rikiyat.github.io/blog/weight-space-programming/) ⭐️ 9.0/10

Researchers at MIT CSAIL published a November 2, 2026 blog post describing 'weight-space programming': asking GPT-6 Astra to make Qwen3.5-0.8B better at math, the model natively inspected and directly rewrote the network's weights — with no gradient descent or training loop — lifting MATH-500 accuracy from 7.9% to 48.1% after changing only 131,072 weight entries, about 0.016% of its nominal 800 million parameters. In a separate demonstration, Astra traced the small model's looping failure (85 of its first 96 practice answers ran to the 32,768-token limit) to a single direction written by the MLPs of layers 15 and 19, and subtracted that direction from 64 output columns in each layer. This sits at the intersection of mechanistic interpretability and model editing, and suggests a possible alternative to fine-tuning: fixing a specific failure mode or capability by surgically editing a handful of weights rather than retraining. If frontier models genuinely have usable native understanding of weight space, it also feeds directly into debates about recursive self-improvement and how cheaply model defects could be patched in the future. The edit is remarkably sparse — roughly 131,072 tensor entries out of ~800 million parameters — but the patch itself required substantial investigation: the researchers gave Astra practice questions, Python access to the weights, and only a limited budget of model executions, with the agent computing replacement values in Python and submitting edited tensors for testing. Caveats worth noting: this is one small model on one benchmark, described in a research blog post rather than a peer-reviewed paper, so generalization to larger models and other capabilities remains unproven.

hackernews · dbreunig · Nov 2, 18:21 · [Discussion](https://news.ycombinator.com/item?id=50341174)

**Background**: A neural network's 'weights' are the numerical parameters learned during training; normally the only way to change a model's behavior is to run more training (gradient descent) on new data, which is expensive and affects the whole network. Mechanistic interpretability is the research field that tries to reverse-engineer what individual weights, neurons and 'directions' inside a network mean — for example, identifying a direction in activation space that corresponds to a behavior like repetition. Weight-space programming goes a step further: instead of a human analyzing the network, an LLM is given read/write access to the raw weight tensors and asked to reason about them and produce edits itself. Qwen is Alibaba's open-weight model family, and MATH-500 is a standard benchmark of competition-style math problems.

<details><summary>References</summary>
<ul>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight - Space Programming: LLMs can natively read & write...</a></li>
<li><a href="https://venturebeat.com/technology/like-gene-editing-for-neural-networks-mit-researchers-used-gpt-6-astra-to-edit-qwens-open-weights-directly-boosting-math-performance">VentureBeat‘Like gene editing for neural networks’: MIT ...</a></li>
<li><a href="https://explainx.ai/blog/weight-space-programming-gpt-6-astra-edits-qwen3-5-0-8b-weights-math-7-9-to-48-1-mit-csail-2026">GPT-6 Astra Edits Qwen Weights: MATH-500 7.9% to 48.1% ...</a></li>

</ul>
</details>

**Discussion**: The discussion (1,828 points, 577 comments) was largely stunned enthusiasm: vessenes said they were 'shook' and admitted they would previously have guessed LLMs' native understanding of their own weights was 'same to less' than human understanding of neurons. xg15 argued the result is insane but not out of the blue, since current LLMs repeatedly show the ability to rapidly grasp complex systems — like a coding agent explaining a sprawling legacy codebase in seconds. vanyle pushed back on the 'emergent capability' framing, speculating that Astra was deliberately trained on neural-weight data as an attempt at recursive self-improvement, so whether that attempt worked remains to be seen.

**Tags**: `#mechanistic-interpretability`, `#model-editing`, `#LLM`, `#weight-space`, `#research`

---

<a id="item-2"></a>
## [vLLM v0.33.0rc3 upgrades to PyTorch 2.14, drops CUDA 12.9 builds](https://github.com/vllm-project/vllm/releases/tag/v0.33.0rc3) ⭐️ 8.0/10

vLLM released v0.33.0rc3, a release candidate bundling 927 commits from 389 contributors (122 of them new), which upgrades the framework to PyTorch 2.14.0 with torchvision 0.29.0 and Triton 3.8.0. The release adds a long list of new models — including Reflection Beam-1.0 (501B MoE, 23B active), Yandex AliceAI-Foundation-80B-A3B, Recursive Flint (40B MoE, 2.5B active), Step-5 Preview and MiniCPM-OCR 1.0 — and drops all CUDA 12.9 wheels and images in favor of CUDA 13.0-only artifacts. vLLM is one of the most widely deployed open-source LLM inference and serving engines, so its packaging and framework jumps directly affect anyone running self-hosted inference at scale. Dropping CUDA 12.9 and moving to PyTorch 2.14 forces operators to validate driver and toolkit compatibility before upgrading, while the new speculative-decoding and ROCm throughput gains translate into concrete serving-cost reductions. Speculative decoding gets several notable additions: the XPress refiner for block-diffusion drafters like DFlash/DSpark, an opt-in lossy verification policy called FLy delivering 1.04-1.31x decode throughput on MI355X and B300, and quantized draft lm_head (+18% decode at concurrency 1). The CUDA wheel is now ABI-stable with libtorch, a new vllm/vllm-openai:v0.33.0-efa image bundles AWS EFA libraries for multi-node KV transfer, and breaking changes remove Medusa, the MLP speculator, and the legacy Ray compiled-graph executor.

github · khluu · Nov 2, 10:10

**Background**: vLLM is a high-throughput, memory-efficient inference and serving engine for large language models, originally developed in the Sky Computing Lab at UC Berkeley and now maintained by a community of over 2000 contributors. Its core innovation is PagedAttention-style KV-cache management, which lets servers batch many concurrent requests efficiently. Speculative decoding is a related technique where a small 'drafter' model proposes tokens that the large target model then verifies, accelerating generation without changing output quality. AWS Elastic Fabric Adapter (EFA) is a network interface for EC2 instances that provides low-latency, high-throughput inter-node communication for AI/ML and HPC workloads, which is why a dedicated image matters for multi-node serving.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/vllm-project/vllm">GitHub - vllm-project/vllm: A high-throughput and memory ...</a></li>
<li><a href="https://github.com/z-lab/dflash">z-lab/dflash: DFlash: Block Diffusion for Flash Speculative Decoding ...</a></li>
<li><a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/efa.html">Elastic Fabric Adapter for AI/ML and HPC workloads on Amazon ...</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#software release`, `#PyTorch`, `#CUDA`

---

<a id="item-3"></a>
## [Subvocal's RF smart glasses turn silent mouthing into text](https://news.ycombinator.com/item?id=50340088) ⭐️ 8.0/10

The Subvocal Company, a YC F26 startup founded by two Georgia Tech CS students, publicly demoed smart glasses that use low-noise RF sensing to decode silently mouthed — or even closed-mouth "internal" — speech into text at roughly the speed of speech. The team started with EMG electrodes at Stanford's TreeHacks in February before abandoning that approach for radio waves that pass through the face and are modulated by the tongue, lips and soft palate. If it works reliably, silent speech input would let people dictate to computers in libraries, offices and public spaces without disturbing anyone, and could be transformative for accessibility users and hands-free computing. It also positions RF sensing as a competitor to camera- and microphone-based input alongside tools like Wispr Flow. The founders say EMG was ruled out because of sweat-induced signal drift, electrical interference, placement variability and the simple fact that nobody wants electrodes stuck to their face, while the remaining hard problems are cross-user generalization (facial anatomy varies wildly) and antenna placement that maximizes field overlap with articulators. The glasses use no camera and no microphone, and the company frames the current hardware as an early product rather than a validated, shipping device.

hackernews · aarushyadav · Nov 2, 17:16

**Background**: Subvocalization is the internal speech we produce when reading or silently thinking through words, accompanied by tiny, usually imperceptible movements of the larynx and articulatory muscles. A silent speech interface tries to capture those non-acoustic signals — via EMG, EEG, cameras or, in this case, RF — and convert them into text or synthesized audio; MIT Media Lab's AlterEgo system is the best-known prior academic attempt. RF sensing works like radar: a transmitter sends weak radio waves into the mouth region and a receiver measures how the returning signal is perturbed by moving tissue, then a trained model maps those perturbations to phonemes and words.

<details><summary>References</summary>
<ul>
<li><a href="https://runany.dev/blog/subvocal/">Subvocal: glasses that type what you mouth silently</a></li>
<li><a href="https://en.wikipedia.org/wiki/Subvocalization">Subvocalization</a></li>
<li><a href="https://en.wikipedia.org/wiki/Silent_speech_interface">Silent speech interface</a></li>

</ul>
</details>

**Discussion**: Commenters were largely enthusiastic, calling the concept sci-fi-grade and predicting it could become as ordinary as buying a mouse or keyboard, with particular excitement about accessibility and faster-than-speaking input. Practical concerns dominated the pushback: fit for non-standard head and nose shapes (requests for adjustable nose pads and a clip-on version for existing prescription frames), whether signal processing runs on-glasses or in an app, battery life, and long-term health effects of an RF emitter sitting next to the eyes and brain.

**Tags**: `#subvocalization`, `#smart-glasses`, `#human-computer-interaction`, `#accessibility`, `#RF-sensing`

---

<a id="item-4"></a>
## [Ubuntu LTS kernels still unpatched for critical Linux 0day RCE after three weeks](https://freenode.net/article/ubuntu-lts-kernels-still-unfixed-for-critical-cve-2026-98432) ⭐️ 8.0/10

Nearly three weeks after the disclosure of CVE-2026-98432 — a critical Linux kernel remote code execution 0day — Ubuntu LTS kernels still have no fix, and Ubuntu's security tracker rates the issue merely "High" priority rather than "Critical," the level that would normally trigger an out-of-schedule emergency kernel update. Ubuntu has also published no official explanation for the delay and no mitigation guidance for affected users. Anyone running Ubuntu servers is exposed to a remotely exploitable kernel flaw with no vendor fix and no official workaround, which is a direct operational risk for production fleets. The silence is also damaging Ubuntu's reputation as a default choice for servers, especially when competitors like RHEL at least published (albeit vague) mitigation advice. Ubuntu has offered no explanation for the delay and no mitigation instructions, while Red Hat's advisory describes a workaround that "reduces exposure to this vulnerability but cannot fully prevent it" without elaborating on what that means. Commenters note no exploit has yet been observed in the wild, and Ubuntu's Livepatch rebootless patching service can only help once a patch actually exists.

hackernews · majorchord · Nov 2, 18:39 · [Discussion](https://news.ycombinator.com/item?id=50341462)

**Background**: A zero-day vulnerability is a security flaw for which no patch exists at the time it becomes publicly known, leaving defenders with only workarounds. Remote code execution (RCE) is a class of bug that lets an attacker run arbitrary code on a target machine over the network — in the kernel, that typically means full system compromise. Ubuntu LTS (Long Term Support) releases are widely used for servers precisely because they promise years of stable, promptly patched kernels; Ubuntu Livepatch is Canonical's mechanism for applying critical kernel fixes without rebooting, but it distributes vendor patches rather than creating them. Kernel patching is especially thorny for embedded devices such as consumer routers, which run Linux but frequently never receive kernel security updates.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zero-day_vulnerability">Zero-day vulnerability - Wikipedia</a></li>
<li><a href="https://www.tenable.com/cybersecurity-guide/principles/zero-day-vulnerability">What is a zero-day vulnerability? | Tenable®</a></li>
<li><a href="https://ubuntu.com/tutorials/enable-the-livepatch-service">Apply kernel patches without rebooting - Ubuntu</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread is largely critical: several users say the missing patch has shaken their trust in Ubuntu and that they will avoid it for new servers, and others demand an official explanation for why a seemingly straightforward kernel fix has taken weeks. Commenters contrast Ubuntu's silence with RHEL's published mitigation guidance and broaden the discussion to consumer routers running permanently unpatched Linux kernels, though at least one participant argues the risk is being blown out of proportion given no observed in-the-wild exploitation and the availability of mitigation options.

**Tags**: `#linux`, `#security`, `#ubuntu`, `#vulnerability`, `#kernel`

---

<a id="item-5"></a>
## [Blog claims frontier LLMs can read and write raw neural network weights](https://www.reddit.com/r/MachineLearning/comments/1xm89ef/sparks_of_weightspace_programming_llms_can/) ⭐️ 8.0/10

A blog post titled "Sparks of Weight-Space Programming" claims that frontier LLMs can natively read and write neural network weights, well beyond what humans or conventional algorithms can do. The author reports that "GPT-6 Astra," given only the raw weights, can identify what a network was trained to do, and can write from scratch small game-playing networks that outplay networks trained with PPO for 100 million steps — without any environment feedback. If it holds up, this would be a qualitatively new capability for LLMs — one that was never explicitly optimized for — with direct implications for both mechanistic interpretability (reading weights to understand behavior) and optimization (generating or editing weights directly instead of relying on gradient-based training like PPO). It also hints at a possible new interface between language models and other neural networks, which could change how small models are produced and debugged. The evidence comes from a single blog post rather than a peer-reviewed paper or released benchmark, and the cited model name "GPT-6 Astra" does not correspond to any publicly documented model, so the claims should be treated as unverified. The reported demonstrations involve small game-playing networks, and the author does not detail evaluation protocols, weight-encoding format, or how much of the raw weight tensor the model actually consumes.

reddit · r/MachineLearning · /u/RobbinDeBank · Nov 2, 20:18

**Background**: Neural network "weights" are the millions or billions of numerical parameters produced by training; normally nobody inspects them directly, because they look like meaningless arrays of floats and the network's function is understood through its behavior. PPO (Proximal Policy Optimization), introduced by Schulman et al. in 2017, is a popular policy-gradient reinforcement learning algorithm used to train agents in deep RL by repeatedly collecting experience in an environment and updating the policy network. "Weight-space programming" refers to the idea of having a language model inspect and edit another network's weights directly, in contrast to the established practice of using LLMs to optimize text artifacts such as prompts and the code around them.

<details><summary>References</summary>
<ul>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight - Space Programming : LLMs can natively read...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proximal_policy_optimization">Proximal policy optimization</a></li>
<li><a href="https://huggingface.co/spaces/akhaliq/weight-space-programming-demo">Weight - Space - Programmed Qwen3.5-0.8B - a Hugging Face Space...</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#interpretability`, `#optimization`, `#neural-network weights`, `#machine-learning research`

---

<a id="item-6"></a>
## [Raspberry Pi 5 Launches With 2.4GHz Cortex-A76 and Dual 4K60 HDMI](https://t.me/zaihuapd/44854) ⭐️ 8.0/10

The Raspberry Pi 5 has officially launched with a 2.4GHz quad-core 64-bit Arm Cortex-A76 CPU and a VideoCore VII GPU supporting OpenGL ES 3.1 and Vulkan 1.2, priced at $60 for the 4GB model and $80 for the 8GB model (plus local taxes). It also adds dual 4K60p HDMI outputs, a 4K60p HEVC decoder, dual-band 802.11ac Wi-Fi, Bluetooth 5.0/BLE, a high-speed microSD interface supporting SDR104 mode, and two USB 3.0 ports capable of 5Gbps simultaneously. This is a major generational leap for the most widely used single-board computer, bringing laptop-class CPU cores and a much stronger GPU to the same low price band, which will benefit hobbyists, educators, and embedded-system developers alike. The addition of dual 4K60 HDMI and genuinely fast USB 3.0 and storage interfaces makes the Pi 5 far more viable as a desktop replacement or media center than earlier models. The CPU is built on Arm's Cortex-A76, which Arm says delivers up to 25% better integer and 35% better floating-point performance than the previous Cortex-A75, while the VideoCore VII integrated GPU offers 12 cores at up to 800MHz in the Broadcom BCM2712 SoC. Note that the quoted $60/$80 prices exclude local taxes, and SDR104 microSD support only helps if paired with a sufficiently fast card.

telegram · zaihuapd · Nov 2, 12:00

**Background**: Raspberry Pi is a line of credit-card-sized single-board computers that run Linux and are widely used in education, hobby projects, and industrial/embedded products. The Cortex-A76 is a 64-bit CPU core implementing the Armv8.2-A architecture, designed by Arm and positioned for laptop-class performance with mobile efficiency. VideoCore is Broadcom's family of low-power multimedia processors used as integrated GPUs in Raspberry Pi boards, and SDR104 is a high-speed UHS-I microSD bus mode that significantly raises card throughput compared with older default modes.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ARM_Cortex-A76">ARM Cortex-A76</a></li>
<li><a href="https://www.notebookcheck.net/Broadcom-VideoCore-VII-Benchmarks-and-Specs.873281.0.html">Broadcom VideoCore VII - Benchmarks and Specs - Notebookcheck</a></li>
<li><a href="https://media.digikey.com/pdf/Data+Sheets/Viking+PDFs/PSFUSDzzzzCzzzz_W_F_DS.pdf">Datasheet for: SDHC/SDXC UHS104 microSD Cards - Digi-Key</a></li>

</ul>
</details>

**Tags**: `#Raspberry Pi`, `#single-board computer`, `#hardware release`, `#Arm Cortex-A76`, `#embedded systems`

---

<a id="item-7"></a>
## [Blog Post Urges Readers to Back Up Beloved Websites](https://blog.mistys-internet.website/post/2026/10/29/if-you-love-a-website-back-it-up/) ⭐️ 7.0/10

A blog post titled "If you love a website, back it up" argues that individuals should personally archive the sites they value rather than assuming the Internet Archive or other services will preserve them. The post sparked a 94-comment Hacker News discussion in which readers shared concrete tooling — the ArchiveWeb.page browser extension for selective captures and SingleFile for saving a page as a self-contained HTML file — along with firsthand stories of forums disappearing without ever being crawled. The discussion highlights how fragile the open web has become: link rot erodes bookmarks within just a few years, and many smaller forums and personal blogs are never captured by large-scale crawlers at all. With commenters warning that centralized LLMs could increasingly replace the open web as the primary information source, deliberate personal archiving is emerging as a practical defense against collective memory loss. Commenters point out that the Wayback Machine's coverage is far from complete — one reader discovered it had never crawled most of a forum they cared about — and that even AI-assisted reconstruction can only salvage what some archive already holds, not recover data that is truly gone. Recommended tools range from SingleFile for quick one-off snapshots to ArchiveWeb.page for hand-picking which pages and page elements to capture, while self-hosted options such as ArchiveBox store captures as WARC files that the user controls.

hackernews · ingve · Nov 2, 13:25 · [Discussion](https://news.ycombinator.com/item?id=50336518)

**Background**: Link rot refers to the tendency of hyperlinks to stop working as pages move, change, or vanish, and it is a long-standing problem for anyone who cites or bookmarks web content. The Internet Archive's Wayback Machine is the best-known public remedy, crawling and storing snapshots of pages over time and serving them back through its site. For durable preservation, archives typically store captures in the WARC (Web ARChive) format, a standardized container that bundles resources together with metadata such as headers and timestamps. Tools like ArchiveBox bring this capability to individuals by letting them run their own archive server that ingests URLs, browser history, or bookmarks and saves HTML, PDFs, media, and more.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WARC_(file_format)">WARC ( file format ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Memento_Project">Memento Project - Wikipedia</a></li>
<li><a href="https://iipc.github.io/warc-specifications/specifications/warc-format/warc-1.1/">The WARC Format</a></li>

</ul>
</details>

**Discussion**: Sentiment was broadly supportive and practical rather than contentious. Readers shared personal losses — dead bookmarks, an Angelfire site with hand-scanned photos that finally went dark after 20 years, and a beloved forum that vanished largely uncrawled — while recommending ArchiveWeb.page and SingleFile for captures. A notable thread of concern was that centralized cloud LLMs may soon replace the open web as an information source and could rewrite the past, prompting calls to buy physical books and archive important sites while they still exist.

**Tags**: `#digital-preservation`, `#link-rot`, `#web-archiving`, `#open-web`, `#tooling`

---

<a id="item-8"></a>
## [Show HN: Interactive voxel 3D map of central Warsaw built from open data](https://p.migdal.pl/warsaw-vibe-voxel/) ⭐️ 7.0/10

Developer stared published a Show HN project that renders central Warsaw as an explorable Minecraft-style voxel city, complete with adjustable date, time of day, and weather, plus clickable pedestrians you can take control of (inspired by Dungeon Keeper). The map is assembled from OpenStreetMap geometry, GUGiK/Geoportal LiDAR for building heights and trees, aerial imagery for colours, and Warsaw's official tree database for seasonal foliage, and the source is released on GitHub. It demonstrates how far open geospatial data — OSM, national LiDAR, municipal tree inventories — can be pushed into a polished, playful browser experience without any proprietary assets. For the open-data and creative-coding communities it is a reusable template for turning public datasets into approachable 3D visualisations, though the performance complaints show the WebGL rendering pipeline still needs work before this scales to larger areas or weaker hardware. The project is designed primarily for desktop, with a mobile version that is admittedly heavy (one commenter reports Safari reloading the page), and the initial load can take a while because geometry and voxel data must be fetched and generated client-side. It is open source under the author's GitHub repository, so others can reuse the pipeline for different cities.

hackernews · stared · Nov 2, 16:25 · [Discussion](https://news.ycombinator.com/item?id=50339221)

**Background**: Voxels are essentially 3D pixels — a three-dimensional grid in which each cube-shaped cell is either filled or empty — giving the blocky, retro look popularised by Minecraft and by voxel art tools such as MagicaVoxel. Building a real city in this style requires accurate footprints and heights: OpenStreetMap supplies building outlines, streets and tram tracks, while airborne LiDAR scanning from Poland's Geoportal provides point clouds whose XYZ coordinates reveal roof heights and tree canopies. Aerial imagery then supplies the colours, and the whole scene is rendered in the browser with WebGL.

<details><summary>References</summary>
<ul>
<li><a href="https://www.geoportal.gov.pl/en/data/lidar-measurements-lidar/">LIDAR measurements (LIDAR) – Geoportal.gov.pl</a></li>
<li><a href="https://ephtracy.github.io/">GitHub Pages - MagicaVoxel</a></li>
<li><a href="https://blog.danielschroeder.me/2024/05/voxel-displacement-modernizing-retro-3d/">Voxel Displacement Renderer — Modernizing the Retro 3 D Aesthetic</a></li>

</ul>
</details>

**Discussion**: Commenters praised the concept but focused heavily on performance: one reported under 1 FPS in Firefox on Linux, and another on a 3080 Ti laptop measured roughly 120 ms frame times with big gaps between updates despite the update loop itself running near 30 FPS. Others offered softer feedback — preferring a sunny default over rain, noting mobile Safari struggles — and the author pointed to similar efforts such as Streets of Prague as prior art.

**Tags**: `#voxel-rendering`, `#3D-visualization`, `#OpenStreetMap`, `#creative-coding`, `#WebGL-performance`

---

<a id="item-9"></a>
## [GDPx Launches Frontier Benchmark Across High-Value Domains](https://newsletter.semianalysis.com/p/gdpx-measuring-frontier-model-capabilities) ⭐️ 7.0/10

SemiAnalysis introduced GDPx, a frontier benchmark that evaluates models across 11 economically valuable domains, including chip design, software engineering, finance, legal, cyber, bio, materials science, quant trading, alignment, hardware design, and recursive self-improvement. It publishes a live leaderboard with per-domain results and cost-per-task data. GDPx shifts evaluation toward economically valuable, agentic work rather than generic academic tasks, which could help enterprises and labs compare frontier models on the domains most likely to generate early AI revenue. It also adds alignment and RSI to the same scorecard, framing capability and safety as part of one measurement problem. The benchmark is built with domain-specialist partners and reports per-domain scores plus cost per task, but the available excerpt does not disclose task counts, grading methodology, or initial model results. Its 11-domain scope mixes engineering, finance, legal, cyber, bio, materials science, alignment, and recursive self-improvement.

rss · Semianalysis · Nov 2, 01:51

**Background**: Frontier models are the most capable general-purpose AI systems from leading labs, and benchmarks are standardized tests used to compare them. Agentic benchmarks evaluate whether a model can complete multi-step tasks with tools and minimal human help, which is closer to real professional work than single-turn question answering. RSI refers to an AI system iteratively designing more capable successors, while alignment research studies how to keep AI systems pursuing intended goals. GDPx groups these areas because it argues the first trillion dollars of AI revenue will concentrate in sectors that can deploy frontier intelligence at high ROI.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/gdpx-measuring-frontier-model-capabilities">GDPx: Measuring Frontier Model Capabilities Across the Most ...</a></li>
<li><a href="https://gdpx.semianalysis.com/domains">GDPx is the best benchmark for measuring general agentic ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Recursive_self-improvement">Recursive self-improvement</a></li>

</ul>
</details>

**Tags**: `#AI benchmarks`, `#frontier models`, `#model evaluation`, `#AI capabilities`, `#ML research`

---

<a id="item-10"></a>
## [Laptop-scale replication backs 'good views beat next-token prediction' for vision-language alignment](https://www.reddit.com/r/MachineLearning/comments/1xlzoze/smallscale_check_of_good_views_beat_nexttoken/) ⭐️ 7.0/10

A Reddit r/MachineLearning author ran a controlled, laptop-scale replication of Balestriero & LeCun's 2026 claim that text encoders align with image encoders faster when trained on 'good views' (two different captions of the same photo) than on 'bad views' or next-token prediction. Using 10,000 COCO photos with 5 human captions each, a frozen DINOv2-base image encoder and an identical 11M-parameter text encoder across all three conditions, good views reached a mutual 10-NN alignment score of 0.320 versus 0.192 for masked bad views and 0.148 for next-token prediction (chance 0.010). The original paper's largest run relied on machine-generated captions, leaving open the possibility that image information leaked into the text and inflated the advantage of good views; this replication removes that confound using only human-written captions and still reproduces the ordering. If the effect holds at larger scale, it would support the JEPA-flavored argument that next-token prediction is a weak, 'bad-view' objective for aligning modalities, with implications for how multimodal models are trained. The setup trained for 3,000 steps at batch size 256 with a VICReg-style variance/covariance anti-collapse loss (rather than the paper's SIGReg), and the author notes major caveats: 11M parameters and 8,000 training photos versus the original's 109M and 72B scales, a single dataset and single image model, and the fact that good views require knowing which captions describe the same photo. Retrieval R@1 with one fitted rotation shows a markedly smaller gap (0.084 vs 0.063 vs 0.057), and the next-token-prediction baseline hit the top of the author's learning-rate range, so the margins are sensitive to measurement choice.

reddit · r/MachineLearning · /u/Traditional_Frame763 · Nov 2, 15:08

**Background**: The Platonic Representation Hypothesis proposes that models trained on different modalities and objectives converge toward a shared representation of reality, which is why vision and language embeddings can be compared at all. Balestriero and LeCun's follow-up frames next-token prediction as a JEPA-style objective fed with 'bad views' — a single caption with spans masked — and argues that training on genuinely different views of the same input aligns modalities faster. DINOv2 is a self-supervised vision transformer whose frozen features serve as a strong, stable image representation, while VICReg is a regularization method that prevents embedding collapse by enforcing variance and decorrelation across dimensions.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/papers/2610.39302">Paper page - Proving and Improving the Platonic Representation...</a></li>
<li><a href="https://dinov2.metademolab.com/">A self - supervised vision transformer model by FAIR</a></li>
<li><a href="https://arxiv.org/abs/2105.04906">[2105.04906] VICReg: Variance-Invariance-Covariance ...</a></li>

</ul>
</details>

**Tags**: `#multimodal learning`, `#representation learning`, `#replication study`, `#self-supervised learning`, `#vision-language alignment`

---

<a id="item-11"></a>
## [LightMIS: 131K-Parameter Medical Segmentation Model Runs 10.5× Faster on Edge GPU](https://www.reddit.com/r/MachineLearning/comments/1xm8dbo/lightmis_ultralightweight_medical_image/) ⭐️ 7.0/10

The LightMIS authors released an ultra-lightweight 2D binary medical image segmentation model with only 131K parameters that aggregates multi-scale encoder features directly instead of using a learned stage-wise decoder. Trained and evaluated under the same nnU-Net protocol across six datasets and five imaging modalities, it reportedly matches nnWNet's modality-macro Dice and IoU averages while using 98.14% fewer parameters and 94.58% fewer GFLOPs, and it ran about 10.5× faster than nnWNet on an Arm Mali-G52 MC2 edge GPU with 100% GPU operator coverage and no CPU fallback. Deploying segmentation models on low-power clinical and embedded hardware is limited by memory, compute and operator-support constraints, so a model that keeps nnU-Net-level accuracy at a fraction of the cost could make on-device medical imaging feasible. Full GPU operator coverage matters practically because any CPU fallback on such devices tends to destroy latency and memory budgets. The comparison is against nnWNet, a CVPR 2025 model that rethinks transformer use in biomedical segmentation, and both models were retrained from scratch in the same controlled environment with nnU-Net v2.3.1 to keep the comparison fair. The scope is deliberately narrow: 2D binary segmentation only, with results reported as averages over modalities rather than as a single-dataset state-of-the-art claim, and the paper, code, and checkpoints are publicly released for reproduction.

reddit · r/MachineLearning · /u/OkLion2068 · Nov 2, 20:22

**Background**: nnU-Net is a self-configuring segmentation framework that automatically adapts preprocessing, network architecture, training and postprocessing to a given dataset, and it has become the de facto baseline in medical image segmentation. nnWNet builds on this pipeline by adding transformer components and reports statistically significant gains over the nnU-Net baseline. Dice and IoU are the standard overlap metrics for segmentation quality, while parameters and GFLOPs approximate model size and computational cost. The Arm Mali-G52 MC2 is a two-core mainstream mobile GPU found in entry-level smartphone and embedded SoCs, representing the kind of constrained target hardware this work aims at.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/MIC-DKFZ/nnUNet">GitHub - MIC-DKFZ/nnUNet · GitHub</a></li>
<li><a href="https://openaccess.thecvf.com/content/CVPR2025/papers/Zhou_nnWNet_Rethinking_the_Use_of_Transformers_in_Biomedical_Image_Segmentation_CVPR_2025_paper.pdf">nnWNet : Rethinking the Use of Transformers in Biomedical Image...</a></li>
<li><a href="https://www.arm.com/products/silicon-ip-multimedia/gpu/mali-g52">Mali-G52 | Boosting mobile visuals and AI – Arm®</a></li>

</ul>
</details>

**Tags**: `#medical-image-segmentation`, `#edge-ai`, `#lightweight-models`, `#nnU-Net`, `#model-efficiency`

---

<a id="item-12"></a>
## [LongCat-2.5 released: a 1.6-trillion-parameter native multimodal model](https://longcat.ai/blog/longcat-2.5/) ⭐️ 7.0/10

The LongCat team released LongCat-2.5, a native multimodal model built for long-horizon agent tasks, with 1.6 trillion total parameters and roughly 48 billion activated per token. It strengthens visual understanding and agentic coding over LongCat-2.0 by encoding visual signals as multi-level discrete tokens handled in the same way as text, enabling tasks such as visual programming. At 1.6T total parameters with sparse activation, LongCat-2.5 joins the small group of frontier-scale multimodal models, and its choice to unify vision and language as discrete tokens points toward a single next-token-prediction objective for both modalities. Developers building agents that must read screenshots, diagrams, or code and act over many steps stand to benefit if the claimed capabilities hold up. The model is already usable through the official site and an API, but GitHub and HuggingFace releases are not yet open, so self-hosting and weight-level inspection are not possible for now. The announcement itself provides no benchmark numbers or architecture details, and third-party listings describe the model as offering multimodal input with a context window on the order of 1M tokens.

telegram · zaihuapd · Nov 2, 03:08

**Background**: LongCat is the model line from Meituan, and its 2.x generation is positioned around agentic work rather than pure chat. A mixture-of-experts (MoE) architecture keeps total parameters large while activating only a fraction per token, which lowers inference cost — here about 48B of 1.6T. "Native multimodal" means the model is trained on interleaved vision and text from the start rather than having a vision encoder bolted on; a common way to do this is to convert images into discrete tokens via a visual tokenizer (as in VQ-VAE-style or newer semantic tokenizers) so that images and words share one vocabulary and one prediction objective. "Long-horizon" agent tasks are multi-step workflows where an agent must plan, call tools, and recover from errors across many turns without human intervention.

<details><summary>References</summary>
<ul>
<li><a href="https://llm-stats.com/models/longcat-2.5">LongCat - 2 . 5 Benchmarks, Pricing & Context Window</a></li>
<li><a href="https://innovation-cat.github.io/posts/2025/12/tokenization/">Discrete Visual Tokenizers for Multimodal LLMs: Bridging ...</a></li>
<li><a href="https://www.emergentmind.com/topics/long-horizon-agentic-tasks">Long - Horizon Agentic Tasks Overview</a></li>

</ul>
</details>

**Tags**: `#multimodal`, `#LLM`, `#model release`, `#agents`, `#MoE`

---

<a id="item-13"></a>
## [Baidu Netdisk shake-to-jump ads switch to magnetometer-based CLHeading to dodge iOS motion blocks](https://t.me/zaihuapd/44850) ⭐️ 7.0/10

A developer used AI to reverse-engineer the ad-redirect logic in Baidu Netdisk for iOS and discovered a framework variant named "NoShake" that abandons CoreMotion and instead reads magnetometer data through Core Location's CLHeading to detect when the phone is being shaken. As a result, disabling gyroscope and accelerometer permissions no longer stops the shake-triggered ad redirects, and the analysis also found that certain parameter sets cause an ad click to fire automatically after about one second. This shows that app-level dark patterns can sidestep the system-level motion protections Apple has been tightening, so users who thought they had blocked shake-to-jump ads may still be tracked and redirected. It raises uncomfortable questions for iOS privacy controls, since a sensor normally associated with compass and navigation features becomes an advertising trigger, and it is likely to intensify scrutiny of Baidu Netdisk and of how Apple enforces motion-data restrictions. The analyzed sample was Baidu Netdisk 13.36.0 for iOS, released on October 22, and the key trick is that CLHeading heading updates via CLLocationManager fall under location services rather than the Motion & Fitness permission that governs CoreMotion. Reports circulating alongside the finding suggest later builds such as 13.36.5 behave differently against iOS 27.2's shake-redirect restrictions, so the cat-and-mouse behavior may already be shifting.

telegram · zaihuapd · Nov 2, 09:27

**Background**: Many Chinese apps monetize through "shake-to-jump" ads, where a slight jolt of the phone launches a full-screen ad or opens a third-party app, and this behavior is traditionally implemented with Apple's CoreMotion framework, which supplies accelerometer and gyroscope data and requires the Motion & Fitness permission. Apple has been adding system-level restrictions on motion-driven redirects, with recent iOS releases such as iOS 27.2 targeting exactly this pattern. Core Location's CLHeading is a separate API normally used by compass, map, and navigation features: calling startUpdatingHeading() on a CLLocationManager returns the device's magnetic heading derived from the magnetometer, and it is governed by location permissions instead of the motion permission — which is why it can serve as a loophole. Reverse engineering like this typically involves decompiling or instrumenting the app binary and inspecting how its ad SDK reacts to sensor callbacks.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@robdeans/measuring-differences-of-degrees-using-cllocations-clheading-5f13f93756d7">Measuring Differences of Degrees Using CLLocation’s CLHeading</a></li>
<li><a href="https://x.com/afteroffline/status/2116187345670250765">After Offline离线后 on X: "IOS 27.2依旧治不了百度网盘摇一摇广告 ...</a></li>
<li><a href="https://www.bilibili.com/en/video/BV1XKxj6YEnE/">Baidu Netdisk's shake-to-open ads can bypass Apple's system ...</a></li>

</ul>
</details>

**Tags**: `#mobile privacy`, `#iOS`, `#reverse engineering`, `#dark patterns`, `#Baidu Netdisk`

---

<a id="item-14"></a>
## [ChatGPT share-link flaw let attackers hijack sessions and leak private chats](https://www.parameter.ai/labs/we-found-a-gap-at-openai) ⭐️ 7.0/10

Parameter's security research team disclosed a ChatGPT share-link vulnerability that let a malicious shared conversation execute code inside a logged-in victim's session, read private chats, and exfiltrate the data to an external server — the victim only had to open the link, with no app install required. OpenAI reproduced both the code-execution and private-chat proofs-of-concept, escalated the severity from P2 to P1, and closed the issue on October 26 with a $5,000 bounty paid to the researchers. ChatGPT is used by hundreds of millions of people who routinely click shared conversation links, so a flaw that turns a benign-looking share link into session-level code execution is a direct account-takeover and privacy risk for ordinary users. The P1 rating and bounty size confirm the severity, and the case highlights how the growing number of rich components inside AI chat frontends (previews, charts, renderers) expands the attack surface. The bug stemmed from a message-handling flaw between ChatGPT's preview feature and its chart component, which allowed injected content to run in the context of the logged-in session. The fix was applied entirely server-side across two versions of ChatGPT's web frontend, so users did not need to update or take any action, and the disclosure was published only after the patch shipped.

telegram · zaihuapd · Nov 2, 10:24

**Background**: A ChatGPT share link is a public URL that renders a saved conversation for anyone who opens it, which makes it a convenient vehicle for delivering malicious content. This class of bug resembles cross-site scripting (XSS): untrusted data from a shared conversation is interpreted as executable code by the chat frontend, running with the victim's privileges. OpenAI's P1 designation is its highest severity tier for security reports, reserved for issues with serious real-world impact such as account takeover or mass data exposure.

<details><summary>References</summary>
<ul>
<li><a href="https://www.parameter.ai/labs">Parameter Labs - Security research and engineering notes ...</a></li>
<li><a href="https://cyberpress.org/openai-fixes-high-severity-chatgpt-flaw/">OpenAI Fixes High-Severity ChatGPT Flaw That Exposed Private ...</a></li>
<li><a href="https://aiweekly.co/alerts/openai-patches-chatgpt-share-link-flaw-that-hijacked-sessions">OpenAI Patches ChatGPT Share-Link Flaw That Hijacked Sessions</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#ChatGPT`, `#OpenAI`, `#XSS`

---

<a id="item-15"></a>
## [WIRED Finds 400+ AI Apps Hiding Sexual Deepfake Tools Behind Mundane Features](https://www.wired.com/story/hundreds-of-mundane-ai-apps-are-hiding-abusive-deepfake-features/) ⭐️ 7.0/10

A WIRED investigation published on November 2 identified a network of more than 400 linked apps and websites that present themselves as ordinary AI tools — pet portraits, language learning and similar utilities — but load a sexual deepfake interface under certain conditions, letting users upload someone else's photo to generate explicit images or video. Researchers tied the sites together through shared code, domains and ad-tracking data; 27 of the apps were still live on Google Play in September with more than 350,000 combined downloads, many rated suitable for all ages. After WIRED shared its findings, Apple removed 19 apps, Google had already taken down most of those it was asked about, and Meta said it blocked 209 related apps from advertising. The case shows how easily app-store review can be gamed: a harmless-looking app can pass inspection and only later swap in abusive content, leaving platform moderation as the last line of defense for people whose photos are used without consent. It also puts pressure on the ad ecosystems that fund such operations, since advertising is often the only visible thread linking a sprawling, deliberately fragmented network of apps and sites. Apple said the developers replaced remote web content after the apps had already passed review, a technique that lets a single approved listing change behavior without a new submission. WIRED's reporting links the network to Chinese-language code, hosting details and domain records pointing to Chinese developers and a Hong Kong-registered company; that attribution is an investigative judgment by the outlet and the operator did not respond to requests for comment.

telegram · zaihuapd · Nov 2, 12:45

**Background**: Deepfakes are images, video or audio generated or manipulated by AI to depict people doing or saying things that never happened, and sexual deepfakes — often made from a single ordinary photo of a real person — have become one of the most widespread and harmful uses of generative models. App stores rely heavily on pre-publication review, but many apps now render their interfaces from remote web pages, meaning the version reviewers see may differ from what users later get. Because such operations often run hundreds of near-identical listings to survive takedowns, investigators and platforms increasingly trace them through shared code signatures, hosting providers and advertising identifiers rather than app names.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Deepfake">Deepfake - Wikipedia</a></li>
<li><a href="https://unric.org/en/artificial-intelligence-what-are-deepfakes/">Artificial intelligence: What are deepfakes?</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#deepfakes`, `#content moderation`, `#app store policy`, `#privacy abuse`

---

<a id="item-16"></a>
## [Cyberattack Sets ICA Store Freezers to 50°C Remote in Sweden](https://x.com/InsiderGeo/status/2117164877701595165) ⭐️ 7.0/10

Swedish supermarket chain ICA reported that multiple stores were hit by an overnight cyberattack in which refrigerated and freezer units were remotely set to 50°C, threatening large amounts of food with spoilage in locations including Sjöbo and Tomelilla. The affected stores paused operations in the morning and were expected to reopen around 9 a.m. local time, with ICA apologizing to customers. This is a concrete cyber-physical attack in which digital access translated directly into physical damage risk, showing that retail refrigeration — often treated as low-priority operational technology — can be weaponized for disruption. It also fits a widening pattern of similar incidents in France and the United States, underscoring that grocery chains and their third-party cooling vendors are now part of the critical-infrastructure threat surface. The report gives no technical detail on the attack vector, so it is unclear whether exposed remote-access interfaces, weak credentials, or a compromised third-party vendor were involved; earlier European incidents were traced to internet-reachable Danfoss refrigeration controllers. ICA has not disclosed how many stores or how much inventory was affected, and food safety consequences depend on how long units sat at 50°C before staff intervened.

telegram · zaihuapd · Nov 2, 13:52

**Background**: Modern supermarket refrigeration is part of operational technology (OT): networked controllers and remote-monitoring platforms let chains and their contractors adjust setpoints and diagnose faults from afar. Because these systems often sit outside the core corporate IT network and are managed by outside vendors, they can be overlooked by traditional security programs even though they carry direct safety and financial consequences. Since October 2026 a wave of similar incidents has struck supermarkets in France and later Belgium, Luxembourg, the Netherlands, Estonia, Ireland and Portugal, with investigators pointing to remotely reachable Danfoss refrigerator regulators such as the AK-SM800 and AK-SC355 as the attack surface.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/2026_French_supermarket_refrigerator_hack">2026 French supermarket refrigerator hack - Wikipedia</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-disrupt-refrigeration-systems-at-european-supermarkets/">Hackers disrupt refrigeration systems at European supermarkets</a></li>
<li><a href="https://secomea.com/blog/ot-security-trends/ot-security-weekly-010-refrigeration-remote-access-risk/">OT Security Weekly #010: Refrigeration attack and SCADA risk</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#IoT security`, `#cyber-physical attacks`, `#critical infrastructure`, `#retail operations`

---

<a id="item-17"></a>
## [Abu Dhabi Signs Four OpenAI Deals, Including 'Machine-Readable Government'](https://thenextweb.com/news/openai-abu-dhabi-deals-machine-readable-government-mubadala) ⭐️ 7.0/10

Abu Dhabi signed four agreements with OpenAI on Monday, one of which — the Machine-Readable Government (MRG) initiative — converts a defined set of policies and regulations into AI-readable rules so that AI can assist officials in reviewing permit and licence applications. The initiative has already been piloted on food imports, and the other deals cover investment analysis with Mubadala, a five-year model-provision agreement via G42's Inception42, and ADNOC becoming the first energy company to deploy the OpenAI Frontier platform. This is one of the clearest real-world templates for sovereign AI adoption, where a national government turns regulation itself into machine-consumable data rather than merely buying chatbots for staff. If the 'rules as code' approach scales beyond pilot programmes, it could reshape how permits, compliance checks and licensing work in governments worldwide — and give OpenAI a deep institutional foothold in the Gulf. Officials retain final decision-making authority, and the pilot reportedly uses UAE-based inference, meaning the model runs locally rather than sending regulatory data abroad. The announcements are light on technical specifics — the scope of the rules encoded, error rates, and audit mechanisms have not been disclosed — and the Inception42 deal is framed as combining OpenAI models with local engineering and implementation services.

telegram · zaihuapd · Nov 2, 15:55

**Background**: Governments have long published regulations as PDFs and prose that only humans can interpret, which makes compliance slow and inconsistent. 'Rules as code' or machine-readable regulation aims to restate laws in structured formats that software — increasingly LLM-based agents — can parse, so routine checks can be automated while humans still sign off on edge cases. OpenAI Frontier, meanwhile, is a platform for building and coordinating AI agents across large organisations, which is what ADNOC intends to use across its energy operations.

<details><summary>References</summary>
<ul>
<li><a href="https://www.utilities-me.com/news/openai-launches-policy-system">OpenAI launches policy system - Utilities Middle East</a></li>
<li><a href="https://www.khaleejtimes.com/uae/abu-dhabi-crown-prince-openai-altman-4-deals-key-sectors">Abu Dhabi Crown Prince meets OpenAI 's Sam Altman... | Khaleej Times</a></li>

</ul>
</details>

**Tags**: `#openai`, `#government-ai`, `#ai-policy`, `#regulation`, `#sovereign-ai`

---

<a id="item-18"></a>
## [SGLang v0.5.23 ships 1,007 PRs, new models and TPU7x support](https://github.com/sgl-project/sglang/releases/tag/v0.5.23) ⭐️ 6.0/10

SGLang released v0.5.23 on GitHub, a version that aggregates 1,007 pull requests from 257 contributors and adds support for a batch of new LLM/VLM and diffusion models — including Muse Spark Open, Beam-1.0, MiniMax-M3.1-Flash, MiniCPM-V 4.7, Cosmos3-Nano-Sim, FLUX.3 Image Klein and MOSS-Image — each shipping with a cookbook entry. The release also introduces an opt-in low-latency mode built on NVIDIA 'megakernel' and AMD 'monokernel' plugins, an opt-in Paged Experts mechanism, and a PyTorch-native plugin that lets SGLang run on Google TPU7x. SGLang is one of the most widely used high-throughput LLM serving frameworks, so each release directly affects teams running inference at scale, and this one brings concrete performance gains: DeepSeek-V4.1 on GB300 gets up to 1.5x more prefill throughput under load and roughly 28% lower first-token latency on 32K–64K prompts. The opt-in Paged Experts feature is arguably the biggest practical change, since it allows MoE models larger than GPU memory to run on a single consumer GPU at up to 30x the speed of CPU offload, and the new TPU7x and Intel backends broaden where SGLang can be deployed. Most of the headline features are opt-in: the megakernel/monokernel low-latency plugins deliver up to 44% faster single-user decode on GB300 and 75% on MI350X for DeepSeek-V4.1-Flash, Paged Experts must be explicitly enabled, and LoRA adapters on quantized MoE models (FP8 and NVFP4) require a new opt-in LoRA engine. Other additions include 30%–58% earlier first tokens for MoE models such as DeepSeek-V4.1-Flash, GLM-5.3-Flash and gpt-oss on 8K prompts on H200, plus HiCache file-based L3 prefix caching for DeepSeek-style MLA models running decode context parallelism; installation requires the --prerelease=allow flag.

github · Fridge003 · Nov 2, 22:14

**Background**: SGLang is an open-source framework for high-throughput serving of large language models, hosted by a non-profit open-source organization and used in production at massive scale — its documentation states it generates trillions of tokens per day across more than 400,000 GPUs. Serving frameworks like this split inference into two phases: prefill, which processes the whole input prompt at once, and decode, which generates tokens one at a time; first-token latency (TTFT) measures how long a user waits before output starts. Mixture-of-Experts (MoE) models activate only a subset of their parameters per token, which makes them fast but memory-hungry, so techniques like Paged Experts that move idle expert weights out of GPU memory matter a lot for running large models on limited hardware. Vision-language models (VLMs) extend text-only LLMs with a vision encoder so they can jointly interpret images and text, while diffusion models generate images rather than text — both categories appear among the newly supported models.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.sglang.io/">Welcome to SGLang - SGLang Documentation</a></li>
<li><a href="https://grokipedia.com/page/SGLang">SGLang</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vision-language_model">Vision-language model - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#LLM inference`, `#SGLang`, `#model serving`, `#release notes`, `#diffusion models`

---

<a id="item-19"></a>
## [LLM 0.37 adds OpenAI-compatible endpoint command and multimodal embeddings](https://simonwillison.net/2026/Nov/2/llm/) ⭐️ 6.0/10

Simon Willison released LLM 0.37, a version bump accumulating roughly two months of features and fixes, which adds a new `llm openai endpoint add` command for configuring models that expose OpenAI-compatible endpoints along with support for the new `gpt-6.1-sol` and `gpt-6.1-terra` models. The release also switches the default model to `gpt-6-luna` at half the price of the previous `gpt-5.6-luna` default, and teaches LLM's embeddings support to track differing content types for binary inputs, which is required for models like Gemini Embedding 2 that embed text, audio, images and video. The endpoint command lowers the friction of pointing LLM at the growing ecosystem of self-hosted and third-party OpenAI-compatible inference servers, so users are no longer limited to a fixed set of providers or forced to hand-edit config files. The cheaper default and multimodal embedding support also keep the tool aligned with how developers actually use models in 2026 — routing across many providers and embedding mixed media rather than plain text. Embedding records now store a content type per item, which matters because multimodal embedding models such as Gemini Embedding 2 map text, images, audio, video and documents into a single vector space. The release credits fixes from 12 contributors, almost all AI-assisted, and Willison notes that AI-assisted triage tools made reviewing that volume of pull requests far less burdensome than he expected, treating them as bug reports with attached examples.

rss · Simon Willison · Nov 2, 23:49

**Background**: LLM is Simon Willison's command-line tool and Python library for running prompts against large language models; it stores prompts and responses in SQLite and supports embeddings for semantic search. Embeddings are vector representations of content that let you compare items by meaning, and LLM historically assumed embedded content was text — an assumption that breaks down as models become natively multimodal. An "OpenAI-compatible endpoint" means a server that implements OpenAI's API shape, a common convention that lets tools like LLM talk to local or third-party model servers without bespoke integrations.

<details><summary>References</summary>
<ul>
<li><a href="https://llm.datasette.io/en/stable/embeddings/index.html">Embeddings - LLM</a></li>
<li><a href="https://deepmind.google/models/gemini/embedding/">Gemini Embedding 2 — Google DeepMind</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-embedding-2/">Gemini Embedding 2: Our first natively multimodal embedding model</a></li>

</ul>
</details>

**Tags**: `#llm-cli`, `#release-notes`, `#openai-compatible-apis`, `#embeddings`, `#developer-tools`

---

<a id="item-20"></a>
## [Census AI Adoption Chart Rerun Highlights 'Super Intelligence' Order Clash](https://simonwillison.net/2026/Nov/2/census-bureau-super-intelligence/) ⭐️ 6.0/10

Simon Willison has rebuilt the U.S. Census Bureau's AI adoption chart using the October 22, 2026 Business Trends and Outlook Survey release, showing 40.7% adoption among firms with 250+ employees. He also noted that the Bureau has run into Executive Order 14434, the September 29, 2026 'Super Intelligence' order. The episode shows how a wording change in an official survey can break a widely used time series, forcing analysts to treat pre- and post-change numbers separately. It also illustrates how an executive order that renames 'AI' as 'Super Intelligence' can reach into mundane federal data collection and public statistics. The BTOS surveys 200,000 of 1.2 million businesses every two weeks, with each panel business responding only every twelve weeks; in November 2025 the question broadened from AI used 'in producing goods or services' to AI used in 'any business function,' so the two series are not comparable. Willison uses a six-survey trailing average and does not bridge the break, and Executive Order 14434 directs federal agencies to replace 'Artificial Intelligence' and 'AI' with 'Super Intelligence' and 'SI.'

rss · Simon Willison · Nov 2, 13:31

**Background**: The Business Trends and Outlook Survey is a biweekly Census Bureau survey that has become a closely watched source for measuring AI adoption across U.S. employer businesses. Executive Order 14434, 'Inaugurating the Era of Super Intelligence,' was signed on September 29, 2026 and directs federal agencies to change their terminology from AI to SI. Simon Willison is a developer and writer known for hands-on experiments using LLM tools to analyze public data.

<details><summary>References</summary>
<ul>
<li><a href="https://www.federalregister.gov/documents/2026/10/02/2026-20321/inaugurating-the-era-of-super-intelligence">Federal Register :: Inaugurating the Era of Super Intelligence</a></li>
<li><a href="https://cofabrix.com/blog/super-intelligence-si-explained">Is AI Now Called Super Intelligence ? The SI Order ... | CoFabrix</a></li>
<li><a href="https://www.federalreserve.gov/econres/notes/feds-notes/monitoring-ai-adoption-in-the-u-s-economy-20260403.html">The Fed - Monitoring AI Adoption in the US Economy</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#AI adoption`, `#data analysis`, `#government statistics`, `#LLM tooling`

---

<a id="item-21"></a>
## [Researcher asks how to report a failed reproduction of a published ML baseline](https://www.reddit.com/r/MachineLearning/comments/1xm64of/couldnt_reproduce_a_published_papers_numbers_with/) ⭐️ 6.0/10

A researcher on r/MachineLearning reports being unable to reproduce a published baseline method on two benchmarks, despite using the authors' released code unmodified, the exact hyperparameters from the paper, and three random seeds, with the reproduction repeated four times over several months. On the remaining benchmarks the numbers match within noise, and the researcher asks how to present both the published and reproduced numbers without appearing incompetent or hostile. Reproducibility is a persistent weak point in machine learning research, and how authors report mismatched baselines directly affects how reviewers and readers interpret claimed improvements. Practical norms for documenting a failed reproduction — in the main table versus an appendix, and whether to notify the original authors first — shape whether these discrepancies surface at all. The researcher's evidence so far includes unchanged authors' code, the paper's own hyperparameters, a multi-seed protocol with three seeds, and a sanity check that the other benchmarks match, plus four independent reproduction attempts spaced months apart. The open question is procedural and rhetorical: whether to contact the authors or file a GitHub issue before submission and whether to mention that contact in the paper.

reddit · r/MachineLearning · /u/InsectActive95 · Nov 2, 19:00

**Background**: In machine learning papers, a baseline is an existing published method that a new approach is compared against, and results are typically reported on standardized benchmark datasets. Reproduction means re-running that baseline using the original authors' released code and hyperparameters, which may still yield different numbers due to hardware differences, library versions, data preprocessing, or random seeds. Reviewers often treat published numbers as authoritative, so a submission that reports lower reproduced values risks being read as an implementation error rather than a genuine discrepancy.

**Tags**: `#reproducibility`, `#machine-learning`, `#peer-review`, `#benchmarking`, `#research-practice`

---

<a id="item-22"></a>
## [Anthropic Updates Usage Policy to Ban Reselling Claude Access](https://www.anthropic.com/legal/aup) ⭐️ 6.0/10

Anthropic updated its Usage Policy — effective November 12, 2026, and the second revision since September 15, 2025 — adding two new prohibitions to the "Do Not Abuse Our Platform" section. The new clauses forbid reselling or proxying Claude access through unauthorized means, including forwarding requests from consumer-grade subscriptions or misrepresenting the product or client being used, and forbid using stolen, fraudulent, or unauthorized payment methods to evade paying. The change directly targets the gray market of Claude access resellers, proxy services, and shared-subscription accounts that arbitrage cheap consumer plans into API-like capacity. It gives Anthropic clearer grounds to suspend accounts and shut down middlemen, affecting developers and small teams who buy Claude access through third parties rather than directly from Anthropic. The policy does not ban legitimate API use or enterprise agreements; it targets unauthorized resale, request forwarding from consumer subscriptions, misrepresentation of the client or product in use, and payment fraud. Enforcement is at Anthropic's discretion through account suspension, and the November 12, 2026 effective date gives existing users a window to migrate to official channels.

telegram · zaihuapd · Nov 2, 05:43

**Background**: Anthropic offers Claude through several channels: consumer subscriptions such as Claude Pro, a paid developer API billed per token, and enterprise agreements. Because subscription pricing and availability differ by region, a gray market has grown up around reselling seats, sharing accounts, and routing traffic through proxies — third-party services that relay requests to Anthropic's servers to mask the user's location or bypass regional blocks. These arrangements violate the spirit of per-seat licensing and expose Anthropic to abuse, chargeback fraud, and loss of control over who uses its models, which is why usage policies increasingly spell out resale and payment-fraud prohibitions explicitly.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kindproxy.com/use-cases/claude/">Claude Proxy — Anthropic API & Developer Access | KindProxy</a></li>
<li><a href="https://www.quarkip.com/blog/guides/3856">Claude Proxy | Unblock IP Bans & Use Claude Stably with QuarkIP</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#Claude`, `#usage policy`, `#AI regulation`, `#API resale`

---

<a id="item-23"></a>
## [DeepSeek Harness team proposes Super-agent architecture with a persistent Router and isolated Workers](https://t.me/zaihuapd/44861) ⭐️ 6.0/10

The DeepSeek Harness team has outlined a "Super-agent" architecture in which a persistent Router layer handles all external interaction and task dispatch, while multiple context-isolated Workers execute tasks concurrently, avoiding single-session blocking and cross-task context confusion. In the team's internal prototype, task completion took a median (p50) of 12.4 minutes and a p95 of 15.7 minutes. The design targets a core pain point of today's coding and general-purpose agents: one conversation can only work on one thing at a time, so long tasks block everything else and parallel work pollutes the shared context. Splitting dispatch from execution is the same direction being explored by Claude Code-style agent products and managed agent services, so this proposal signals DeepSeek pushing from base models into agent orchestration infrastructure. The performance numbers are self-reported from an internal prototype and are end-to-end task completion times rather than per-token or per-call latency, with the small gap between p50 and p95 suggesting relatively stable runs. The team stresses the scheme is still at the architecture-discussion stage, so no full implementation, benchmark methodology, or cost comparison has been published with this item.

telegram · zaihuapd · Nov 2, 17:17

**Background**: DeepSeek Harness is an agent-focused team inside DeepSeek, the Chinese company behind the DeepSeek model family; it works on the "harness" layer — the orchestration and control engineering wrapped around a model, captured in the team's formula "Model + Harness = Agent". In LLM agent systems, a Router is the component that receives user requests and decides which sub-task goes where, while Workers are the executors that actually call tools and the model; "context isolation" means each Worker keeps its own conversation history so parallel tasks do not interfere. p50 and p95 are percentile latency metrics: p50 is the median task, and p95 means 95% of tasks finished faster than that value, which is how engineers measure tail latency rather than just the average.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/DeepSeek_Harness">DeepSeek Harness - 维基百科，自由的百科全书</a></li>
<li><a href="https://baike.baidu.com/item/Harness/67826060">Harness（DeepSeek内部团队）_百度百科</a></li>
<li><a href="https://redreamality.com/cn/blog/deepseek-super-agent-router-worker-architecture/">DeepSeek Super-agent 架构：Router、Worker 与事件驱动 | Redreamali...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#multi-agent systems`, `#DeepSeek`, `#task orchestration`, `#LLM infrastructure`

---