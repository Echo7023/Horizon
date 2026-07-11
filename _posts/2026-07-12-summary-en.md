---
layout: default
title: "Horizon Summary: 2026-07-12 (EN)"
date: 2026-07-12
lang: en
---

> From 28 items, 7 important content pieces were selected

---

1. [Humanoid robot performs world's first live pig gallbladder surgery](#item-1) ⭐️ 9.0/10
2. [OpenAI Launches GPT-5.6 Series with Sol, Terra, Luna Variants](#item-2) ⭐️ 9.0/10
3. [SGLang v0.5.15 Boosts LLM Serving with Major Optimizations](#item-3) ⭐️ 8.0/10
4. [Apple Sues OpenAI for Trade Secret Theft](#item-4) ⭐️ 8.0/10
5. [Residential proxies and the scraper arms race](#item-5) ⭐️ 8.0/10
6. [VultronRetriever tops MTEB with huge efficiency gains](#item-6) ⭐️ 8.0/10
7. [Six U-Boot flaws allow firmware bypass and code execution](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Humanoid robot performs world's first live pig gallbladder surgery](https://arstechnica.com/ai/2026/07/humanoid-robots-controlled-by-surgeons-did-world-first-operation-on-live-pigs/) ⭐️ 9.0/10

Surgeons at UC San Diego successfully teleoperated two Unitree G1 humanoid robots to perform the world's first live pig gallbladder removal surgeries, as reported in Nature on July 8, 2026. This breakthrough demonstrates that affordable, general-purpose humanoid robots can be adapted for precision surgery, potentially lowering costs and expanding access to surgical care in remote or resource-limited settings. The Unitree G1 has a base price of $13,500 and costs around $67,000 with dexterous hands, far less than specialized surgical robots like the da Vinci system, which cost $500,000 to millions.

telegram · zaihuapd · Jul 11, 02:29

**Background**: Teleoperated robotic surgery allows a surgeon to control robot arms remotely with high precision. The Unitree G1 is a commercially available, general-purpose humanoid robot standing about 1.5 meters tall and weighing 27 kg. This study marks the first time a non-specialized humanoid robot has been used for live surgery, opening new possibilities for versatile medical robots.

<details><summary>References</summary>
<ul>
<li><a href="https://today.ucsd.edu/story/surgeons-use-teleoperated-humanoid-robots-to-perform-live-surgery-a-world-first">Surgeons Use Teleoperated Humanoid Robots to Perform Live...</a></li>
<li><a href="https://www.unitree.com/g1/">Humanoid robot G 1 _ Humanoid Robot ... | Unitree Robotics</a></li>

</ul>
</details>

**Tags**: `#humanoid robots`, `#telemedicine`, `#surgical robotics`, `#medical robotics`, `#Unitree G1`

---

<a id="item-2"></a>
## [OpenAI Launches GPT-5.6 Series with Sol, Terra, Luna Variants](https://t.me/zaihuapd/42497) ⭐️ 9.0/10

OpenAI has officially launched the GPT-5.6 series, featuring three variants: Sol (flagship), Terra (balanced performance and cost), and Luna (high-concurrency, low-cost). The release emphasizes enhanced capabilities in code, knowledge work, design, research, and cybersecurity, along with new features such as max/ultra inference, multi-agent collaboration, and Programmatic Tool Calling. This release represents a major leap in LLM capabilities with a focus on cost-performance optimization, potentially making advanced AI more accessible for complex tasks. The introduction of multi-agent collaboration and programmatic tool calling could redefine how AI systems handle multi-step workflows and enterprise automation. The flagship Sol variant will be the default model for GPT-5.6, offering the highest capability with max/ultra inference for deeply reasoning chains. Terra balances performance and cost for general use, while Luna is optimized for high-concurrency, low-cost scenarios. The model also supports Programmatic Tool Calling, which allows agents to write and execute code for tool invocation, as described by Anthropic and Letta.

telegram · zaihuapd · Jul 11, 13:34

**Background**: GPT-5.6 is the latest generation of OpenAI's large language model, succeeding GPT-4. The series offers three variants to cater to different use cases: Sol for maximum capability, Terra for balanced performance-cost, and Luna for high throughput. Key innovations include max/ultra inference scaling (using more computation at inference time for deeper reasoning) and multi-agent collaboration, where multiple AI agents coordinate to solve complex tasks collectively. Programmatic Tool Calling is a technique where an LLM writes and executes code to invoke external tools, improving efficiency and accuracy for tool-using agents.

<details><summary>References</summary>
<ul>
<li><a href="https://www.letta.com/blog/programmatic-tool-calling-with-any-llm">Programmatic Tool Calling with any LLM | Letta</a></li>
<li><a href="https://www.ibm.com/think/topics/multiagent-system">What is a Multi - Agent System? | IBM</a></li>
<li><a href="https://learn-more.supermicro.com/data-center-stories/ai-inference-time-scaling-laws-explained">AI Inference Time Scaling Laws Explained</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-5.6`, `#AI`, `#LLM`, `#Language Model`

---

<a id="item-3"></a>
## [SGLang v0.5.15 Boosts LLM Serving with Major Optimizations](https://github.com/sgl-project/sglang/releases/tag/v0.5.15) ⭐️ 8.0/10

SGLang v0.5.15 introduces significant performance improvements, including tuned GLM-5.2 NVFP4 on Blackwell GPUs (500+ tok/s/user on 8x B300), Spec V2 enabled by default for 11% TPS gain, and IndexShare MTP for up to 1.9x lower draft-step cost. These optimizations directly improve throughput and reduce latency for production LLM serving, making SGLang more competitive for high-performance AI workloads. The advancements in speculative decoding and GPU kernel fusion benefit a wide range of models. The release also includes TopK V2 with runtime k up to 2048, indexer prologue fusion reducing kernels from 12 to 4, shape-specialized JIT router GEMM, and breakable CUDA Graph enabled by default. New model support includes Hunyuan 3, HRM-Text, and Qwen3.6 NVFP4.

github · Fridge003 · Jul 10, 22:58

**Background**: SGLang is an open-source framework for efficient LLM serving, featuring speculative decoding and advanced GPU optimizations. Speculative decoding uses a lightweight draft model to predict tokens in parallel, then verifies with the main model. NVFP4 is NVIDIA's 4-bit floating-point format supporting low-precision inference on Blackwell GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/zai-org/glm-52-blog">GLM-5.2: Built for Long-Horizon Tasks</a></li>
<li><a href="https://arxiv.org/html/2604.03950v1">Diagonal-Tiled Mixed- Precision Attention for Efficient Low-Bit MXFP...</a></li>
<li><a href="https://undef.dev/writing/learn/speculative-decoding/">Speculative decoding : when LLMs predict their own... — undef.dev</a></li>

</ul>
</details>

**Tags**: `#LLM inference`, `#GPU optimization`, `#speculative decoding`, `#performance`, `#sglang`

---

<a id="item-4"></a>
## [Apple Sues OpenAI for Trade Secret Theft](https://9to5mac.com/2026/07/10/apple-sues-openai-trade-secret-theft/) ⭐️ 8.0/10

Apple has filed a lawsuit against OpenAI, accusing the company of orchestrating a scheme where former employees stole confidential trade secrets and used them for OpenAI's benefit. This lawsuit could set legal precedents on intellectual property protection in AI and heighten tensions between tech giants competing for AI talent. Apple alleges that OpenAI instructed new hires to avoid detection by not disclosing their new employer, and that OpenAI used Apple's confidential hardware information to approach Apple suppliers.

hackernews · stock_toaster · Jul 10, 20:47 · [Discussion](https://news.ycombinator.com/item?id=48865019)

**Background**: Trade secret theft involves unauthorized acquisition or use of confidential business information. Apple has substantial resources for litigation, while OpenAI has faced criticism over its intellectual property practices, including training data issues.

**Discussion**: Community comments strongly condemn OpenAI, warning users about potential IP theft and predicting that Apple's deep pockets will lead to a damaging discovery process for OpenAI.

**Tags**: `#Apple`, `#OpenAI`, `#trade secrets`, `#lawsuit`, `#AI ethics`

---

<a id="item-5"></a>
## [Residential proxies and the scraper arms race](https://lwn.net/SubscriberLink/1080822/990a8a5e2d379085/) ⭐️ 8.0/10

LWN reports on the escalating battle between scrapers using residential proxies and site owners implementing countermeasures, highlighting the difficulty of distinguishing bots from legitimate users. This ongoing arms race threatens the open web, as anti-scraping measures can harm legitimate users and centralize control with entities like Cloudflare. Residential proxies route traffic through real ISP-assigned home IPs, making them hard to block. Some sites use proof-of-work challenges, but scrapers can leverage millions of compromised devices to bypass them.

hackernews · chmaynard · Jul 10, 19:38 · [Discussion](https://news.ycombinator.com/item?id=48864252)

**Background**: Residential proxies are intermediaries that use IP addresses assigned by internet service providers to real homes, making bot traffic appear as regular users. Tools like Cloudflare Bot Management attempt to distinguish bots from humans using behavioral analysis and challenges. However, the proliferation of malicious apps that install proxy software on phones has expanded the pool of residential IPs available to scrapers.

<details><summary>References</summary>
<ul>
<li><a href="https://techreviewadvisor.com/what-is-a-residential-proxy/">What Is a Residential Proxy? How It Works - Tech Review Advisor</a></li>
<li><a href="https://developers.cloudflare.com/bots/get-started/bot-management/">Bot Management · Cloudflare bot solutions docs</a></li>

</ul>
</details>

**Discussion**: Commenters debate solutions like improved common crawl and proof-of-work limitations. Some worry that anti-scraping rhetoric will harm the open web and empower Cloudflare. Others note that intensity and volume of bots are the real issue, and that low-volume scraping should be tolerated.

**Tags**: `#web scraping`, `#residential proxies`, `#anti-bot`, `#open web`, `#cloudflare`

---

<a id="item-6"></a>
## [VultronRetriever tops MTEB with huge efficiency gains](https://www.reddit.com/r/MachineLearning/comments/1utmxq8/vultronretriever_family_of_models_released_on/) ⭐️ 8.0/10

Vultr released the VultronRetriever family of models (Prime 8B, Core 4.5B, Flash 0.8B), each ranking #1 in its class on the MTEB leaderboard, with up to 16x smaller index size and 12x higher throughput than previous leaders, and demonstrated offline Q&A and embedding on an iPhone. These models set a new efficiency standard for retrieval, enabling high-precision search on edge devices like smartphones, which could democratize offline retrieval-augmented generation (RAG) and reduce server costs for enterprises. The VultronRetriever family uses the Hydra architecture, which unifies late interaction retrieval and generation in a single model, reducing memory usage by up to half compared to separate models; all models are trained on datasets with 0% cross-dataset duplication and 0% eval contamination.

reddit · r/MachineLearning · /u/madkimchi · Jul 11, 15:22

**Background**: The MTEB leaderboard is a widely used benchmark for evaluating embedding models on retrieval and other language tasks. Late interaction retrieval, used in models like ColBERT, processes queries and documents separately until the final matching stage, balancing efficiency and precision. The Hydra architecture extends this by enabling both retrieval and generation with LoRA adapters, allowing a single model to switch between tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/spaces/mteb/leaderboard">MTEB Leaderboard - a Hugging Face Space by mteb</a></li>
<li><a href="https://jina.ai/news/what-is-colbert-and-late-interaction-and-why-they-matter-in-search/">What is ColBERT and Late Interaction and Why They Matter in Search?</a></li>

</ul>
</details>

**Tags**: `#retrieval`, `#MTEB`, `#edge AI`, `#embeddings`, `#information retrieval`

---

<a id="item-7"></a>
## [Six U-Boot flaws allow firmware bypass and code execution](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 8.0/10

Binarly disclosed six vulnerabilities in U-Boot's FIT signature verification code, two allowing arbitrary code execution and four causing device crashes, affecting versions since 2013.07. These vulnerabilities allow attackers to execute malicious code before the OS boots, potentially disabling firmware security, altering boot flow, or implanting persistent firmware malware across millions of devices. The flaws are in the Flattened Image Tree (FIT) signature verification logic, with two leading to memory corruption and arbitrary code execution. Patches have been accepted by upstream but OEMs must integrate them into firmware updates.

telegram · zaihuapd · Jul 11, 08:32

**Background**: U-Boot (Das U-Boot) is a free, open-source boot loader used in embedded devices across many architectures (ARM, MIPS, x86, etc.). It uses Flattened Image Trees (FIT) for verified boot, signing kernel images and device trees. Baseboard Management Controllers (BMCs) often rely on U-Boot and support remote firmware updates, making them vulnerable to remote exploitation without physical access.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Das_U-Boot">Das U-Boot - Wikipedia</a></li>
<li><a href="https://u-boot.org/">Das U-Boot: The Universal Boot Loader</a></li>
<li><a href="https://docs.u-boot.org/en/latest/usage/fit/signature.html">U-Boot FIT Signature Verification — Das U-Boot unknown version documentation</a></li>

</ul>
</details>

**Tags**: `#security`, `#bootloader`, `#U-Boot`, `#vulnerability`, `#firmware`

---