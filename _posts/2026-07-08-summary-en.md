---
layout: default
title: "Horizon Summary: 2026-07-08 (EN)"
date: 2026-07-08
lang: en
---

> From 42 items, 16 important content pieces were selected

---

1. [EU Parliament Passes Chat Control in First Round](#item-1) ⭐️ 9.0/10
2. [MIRA: 5B Parameter Multiplayer World Model for Rocket League](#item-2) ⭐️ 9.0/10
3. [Anthropic Releases Claude Sonnet 5 with Stronger Agentic Abilities](#item-3) ⭐️ 9.0/10
4. [Januscape: 16-Year-Old KVM VM Escape Flaw Disclosed](#item-4) ⭐️ 9.0/10
5. [Kokoro: Local, CPU-Friendly, High-Quality TTS Model](#item-5) ⭐️ 8.0/10
6. [EU Mandates Driver Monitoring Cameras in All New Cars](#item-6) ⭐️ 8.0/10
7. [Why Skilled Workers Leave Germany Despite High Salaries](#item-7) ⭐️ 8.0/10
8. [Microsoft Lays Off id Software's Engine Team](#item-8) ⭐️ 8.0/10
9. [sqlite-utils 4.0 Introduces Schema Migrations](#item-9) ⭐️ 8.0/10
10. [Ph.D. Thesis on Differentiable Ray Tracing for Radio Propagation](#item-10) ⭐️ 8.0/10
11. [Mozilla CTO AMA on Open Source AI Report](#item-11) ⭐️ 8.0/10
12. [Defending fine-tuning poisoning via trusted LoRA subspace](#item-12) ⭐️ 8.0/10
13. [Elon Musk Dissolves xAI, Rebrands as SpaceXAI](#item-13) ⭐️ 8.0/10
14. [China Plans $295B National Compute Network with Domestic AI Chips](#item-14) ⭐️ 8.0/10
15. [DeepSeek Develops Own AI Inference Chip to Reduce Reliance on Nvidia and Huawei](#item-15) ⭐️ 8.0/10
16. [China Considers Restricting Export of Top AI Models](#item-16) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [EU Parliament Passes Chat Control in First Round](https://www.heise.de/en/news/Showdown-in-Strasbourg-The-unexpected-return-of-Chat-Control-1-0-11356680.html) ⭐️ 9.0/10

The EU Parliament passed the controversial Chat Control legislation in its first round using procedural tactics, with a final vote scheduled for Thursday requiring only a simple majority of present MEPs. This legislation would mandate mass surveillance of private communications, potentially breaking end-to-end encryption and threatening digital privacy rights across the EU and beyond, as other countries may copy such regulations. The procedural maneuver gives proponents a tactical advantage: amendments or rejection require an absolute majority of 361 votes, while passage needs only a simple majority of present MEPs, many of whom may have left before the summer break.

hackernews · miroljub · Jul 7, 15:16 · [Discussion](https://news.ycombinator.com/item?id=48819008)

**Background**: Chat Control, formally the Regulation to Prevent and Combat Child Sexual Abuse (CSAR), was proposed in May 2022 to combat online child sexual abuse. Critics argue it enables mass surveillance and undermines encryption. The legislation had previously been rejected but is now being revived through procedural channels.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>
<li><a href="https://reclaimthenet.org/eu-parliament-revives-chat-surveillance-for-thursday-vote">EU Parliament Revives Chat Surveillance for Thursday Vote</a></li>
<li><a href="https://www.heise.de/en/news/Partial-victory-with-a-catch-EU-Parliament-temporarily-defies-chat-control-11349760.html">Partial victory with a catch: EU Parliament temporarily defies chat control | heise online</a></li>

</ul>
</details>

**Discussion**: Commenters expressed frustration over the EU repeatedly pushing unpopular laws through procedural tactics, with one quoting Jean-Claude Juncker's remark about step-by-step erosion of democracy. Others noted that even non-EU countries may adopt similar surveillance measures.

**Tags**: `#EU legislation`, `#surveillance`, `#privacy`, `#encryption`, `#digital rights`

---

<a id="item-2"></a>
## [MIRA: 5B Parameter Multiplayer World Model for Rocket League](https://www.reddit.com/r/MachineLearning/comments/1upofuw/mira_multiplayer_interactive_world_models_trained/) ⭐️ 9.0/10

General Intuition, Kyutai, and Epic Games released MIRA, a 5 billion parameter interactive world model for multiplayer Rocket League, trained on 10,000 hours of synthetic data and capable of running a full 2v2 match at 20 FPS on a single B200 GPU. MIRA is the first multiplayer world model for highly dynamic environments with complex physics, enabling real-time interactive simulation without real-world data collection, which could accelerate reinforcement learning and game AI research. The model uses a latent diffusion architecture to generate video frames conditioned on all four players' actions, and the team released a playable demo, a technical paper, and a 1,000-hour dataset of 4-player gameplay.

reddit · r/MachineLearning · /u/MasterScrat · Jul 7, 07:59

**Background**: World models are AI systems that simulate environment dynamics, allowing agents to plan and learn without real-world interaction. Previous world models were limited to single-player scenarios, treating other agents as part of the environment. MIRA extends this to multiplayer settings by conditioning on multiple action streams, learning to attribute changes to the correct player.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/mira-wm/mira">MIRA: Multiplayer Interactive World Models with ... - GitHub</a></li>
<li><a href="https://arxiv.org/abs/2607.05352">[2607.05352] Multiplayer Interactive World Models with ...</a></li>
<li><a href="https://www.linkedin.com/posts/generalintuition_introducing-mira-a-playable-multiplayer-activity-7479870314252922880-y9CV">Introducing MIRA. A playable, multiplayer world model. A ...</a></li>

</ul>
</details>

**Tags**: `#world models`, `#reinforcement learning`, `#multiplayer`, `#Rocket League`, `#open source`

---

<a id="item-3"></a>
## [Anthropic Releases Claude Sonnet 5 with Stronger Agentic Abilities](https://t.me/zaihuapd/42404) ⭐️ 9.0/10

Anthropic has released Claude Sonnet 5, which it describes as the most agentic Sonnet model yet, capable of planning, using tools like browsers and terminals, and running autonomously. The model is available immediately across all plans, including Free and Pro, with a limited-time pricing of $2 per million input tokens and $10 per million output tokens until August 31, 2026. Claude Sonnet 5 brings agentic capabilities that previously required larger, more expensive models, making advanced AI agents more accessible and cost-effective. Its competitive pricing and strong performance in coding, tool use, and reasoning could accelerate adoption of AI agents in software engineering and other professional workflows. Claude Sonnet 5 outperforms Sonnet 4.6 in reasoning, tool use, coding, and knowledge work, and its performance is close to Opus 4.8 but at a lower price. It becomes the default model for Free and Pro plans on Claude.ai, and is also available via the Anthropic API and Amazon Bedrock.

telegram · zaihuapd · Jul 7, 09:02

**Background**: Anthropic's Claude model family includes Sonnet (mid-range, balanced for speed and capability) and Opus (top-tier, highest performance). Opus 4.8, released in May 2026, set a high bar for agentic tasks, but Sonnet 5 now brings similar capabilities at a lower cost. Agentic abilities refer to a model's capacity to autonomously plan, use external tools, and execute multi-step tasks without constant human guidance.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-sonnet-5">Introducing Claude Sonnet 5 \ Anthropic</a></li>
<li><a href="https://techcrunch.com/2026/06/30/anthropic-launches-claude-sonnet-5-as-a-cheaper-way-to-run-agents/">Anthropic launches Claude Sonnet 5 as a cheaper way to run ...</a></li>
<li><a href="https://www.anthropic.com/news/claude-opus-4-8">Introducing Claude Opus 4.8 \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Anthropic`, `#Claude`, `#LLM`, `#agent`

---

<a id="item-4"></a>
## [Januscape: 16-Year-Old KVM VM Escape Flaw Disclosed](https://github.com/V4bel/Januscape) ⭐️ 9.0/10

Security researchers publicly disclosed Januscape (CVE-2026-53359), a use-after-free vulnerability in KVM's shadow MMU that allows a guest VM to escape to the host on both Intel and AMD x86 platforms. The flaw has existed in the Linux kernel for approximately 16 years, and proof-of-concept code has been released. This is the first KVM/x86 VM escape vulnerability that affects both Intel and AMD platforms, directly threatening the isolation boundary of multi-tenant KVM hosts in public clouds. Additionally, on distributions like RHEL, a local unprivileged user can exploit the flaw to escalate privileges to root. The vulnerability is a use-after-free in the shadow MMU code shared across Intel and AMD, triggered by guest-side actions alone. It was used as a 0-day in Google's kvmCTF and affects Linux kernels from 2010 to June 2026.

telegram · zaihuapd · Jul 7, 10:14

**Background**: KVM (Kernel-based Virtual Machine) is a Linux kernel module that turns the host into a hypervisor, allowing multiple virtual machines (guests) to run. The shadow MMU is used to manage guest memory mappings; a use-after-free bug occurs when a freed memory region is still referenced, leading to memory corruption. VM escape vulnerabilities break the isolation between guest and host, potentially allowing an attacker to control the host system.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/07/16-year-old-linux-kvm-flaw-lets-guest.html">16-Year-Old Linux KVM Flaw Lets Guest VMs Escape to Host on ...</a></li>
<li><a href="https://github.com/V4bel/Januscape">GitHub - V4bel/Januscape</a></li>
<li><a href="https://cybersecuritynews.com/16-year-old-linux-kvm-vulnerability/">16-Year-Old Linux KVM Vulnerability Allows Malicious Guest ...</a></li>

</ul>
</details>

**Tags**: `#KVM`, `#VM escape`, `#security vulnerability`, `#CVE-2026-53359`, `#Linux kernel`

---

<a id="item-5"></a>
## [Kokoro: Local, CPU-Friendly, High-Quality TTS Model](https://ariya.io/2026/03/local-cpu-friendly-high-quality-tts-text-to-speech-with-kokoro/) ⭐️ 8.0/10

Kokoro, an open-weight TTS model with 82 million parameters, has been released, delivering high-quality speech synthesis that runs efficiently on CPUs without requiring a GPU. This makes high-quality TTS accessible to users without dedicated GPUs, enabling local, privacy-preserving automation and accessibility tools for a wider audience. Kokoro is Apache-licensed and can be deployed via a Docker container that serves both a web UI and an OpenAI-compatible API, making integration easy.

hackernews · speckx · Jul 7, 18:24 · [Discussion](https://news.ycombinator.com/item?id=48821576)

**Background**: Text-to-speech (TTS) models traditionally require powerful GPUs for real-time synthesis, limiting their use to cloud services or high-end hardware. Kokoro's lightweight architecture (82M parameters) achieves comparable quality to larger models while being significantly faster and more cost-efficient on CPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/hexgrad/Kokoro-82M">hexgrad/Kokoro-82M · Hugging Face</a></li>
<li><a href="https://github.com/hexgrad/kokoro">GitHub - hexgrad/kokoro: https://hf.co/hexgrad/Kokoro-82M</a></li>
<li><a href="https://ariya.io/2026/03/local-cpu-friendly-high-quality-tts-text-to-speech-with-kokoro/">Local, CPU-Friendly, High-Quality TTS (Text-to-Speech) with Kokoro · ariya.io</a></li>

</ul>
</details>

**Discussion**: Community members praised Kokoro for its ease of use and CPU efficiency, with one user building a pipeline to convert articles to podcasts and another using it for an accessibility product. Some noted limitations with single-word utterances and homograph pronunciation, but overall sentiment was highly positive.

**Tags**: `#TTS`, `#AI`, `#accessibility`, `#open-source`, `#local-models`

---

<a id="item-6"></a>
## [EU Mandates Driver Monitoring Cameras in All New Cars](https://allaboutcookies.org/eu-mandatory-distracted-driver-system) ⭐️ 8.0/10

Starting July 2024, the European Union's General Safety Regulation (EU) 2019/2144 requires all new cars sold in the EU to include a driver monitoring system (DMS) that uses cameras to detect driver distraction and fatigue. This regulation aims to reduce road accidents caused by driver inattention, potentially saving thousands of lives annually, but it also raises concerns about privacy, user experience, and the reliability of automated alerts. The DMS uses an infrared camera on the steering column to track the driver's face and eyes at 60 frames per second, and it works with other safety systems like pre-collision assist. The regulation applies to all new type-approved passenger cars from July 2024.

hackernews · nickslaughter02 · Jul 7, 20:50 · [Discussion](https://news.ycombinator.com/item?id=48823557)

**Background**: Driver monitoring systems use cameras and sensors to detect signs of drowsiness or distraction, such as head nodding or prolonged gaze away from the road. The EU's General Safety Regulation, introduced in 2019, mandates a suite of advanced safety features to reduce fatalities and pave the way for autonomous driving.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Driver_monitoring_system">Driver monitoring system - Wikipedia</a></li>
<li><a href="https://autovista24.autovistagroup.com/news/what-is-the-general-safety-regulation/">What is the General Safety Regulation?</a></li>
<li><a href="https://grokipedia.com/page/2026_German_vehicle_regulations">2026 German vehicle regulations</a></li>

</ul>
</details>

**Discussion**: Comments reveal a split: some users praise the system's accuracy in catching distractions, while others criticize the overall UX of modern cars, citing annoying alerts and intrusive lane assist. There are also privacy concerns and comparisons to Boeing's alarm fatigue.

**Tags**: `#regulation`, `#automotive`, `#privacy`, `#safety`, `#UX`

---

<a id="item-7"></a>
## [Why Skilled Workers Leave Germany Despite High Salaries](https://www.dw.com/en/germany-migrants-skilled-workers-integration-labor-market-bureaucracy-language-housing/a-77853162) ⭐️ 8.0/10

A DW article and community discussion highlight that skilled workers in Germany face bureaucracy, cultural barriers, and limited upward mobility, leading many to leave despite high salaries. This matters for Germany's tech workforce and immigration policy, as retaining skilled talent is critical for economic competitiveness. The discussion reveals systemic issues that could deter future immigrants. Community comments cite slow bureaucracy, deteriorating infrastructure, and a reserved culture that limits trust and leadership opportunities for outsiders. One commenter noted that even high earners (€200k+) consider leaving.

hackernews · theanonymousone · Jul 7, 10:42 · [Discussion](https://news.ycombinator.com/item?id=48815982)

**Background**: Germany has long attracted skilled workers due to its strong economy and high salaries, but integration challenges persist. The country faces a housing crisis, aging infrastructure, and bureaucratic hurdles that affect both locals and immigrants.

**Discussion**: Commenters share personal anecdotes: one naturalized citizen felt unwelcome, another noted limited upward mobility unless in international companies, and a long-term resident lamented worsening infrastructure and bureaucracy. Overall sentiment is critical of Germany's integration and retention policies.

**Tags**: `#immigration`, `#talent retention`, `#Germany`, `#tech workforce`, `#cultural integration`

---

<a id="item-8"></a>
## [Microsoft Lays Off id Software's Engine Team](https://gamefromscratch.com/microsoft-fire-idtech-team-at-id-software/) ⭐️ 8.0/10

Microsoft has laid off the engine team at id Software, the developer behind the idTech engine series, as part of broader cuts at the studio. This move signals a potential shift away from proprietary engine development at Microsoft's studios, raising concerns about industry homogenization and the loss of unique technical expertise that defined id Software's legacy. The layoffs affect the team responsible for idTech, the engine powering titles like Doom and Quake. No official confirmation has been provided by Microsoft or id Software regarding the exact number of employees let go.

hackernews · bauc · Jul 7, 15:33 · [Discussion](https://news.ycombinator.com/item?id=48819244)

**Background**: id Software is a legendary game developer known for pioneering first-person shooters with engines like idTech. The idTech engine has been a cornerstone of in-house technical culture, with John Carmack famously open-sourcing earlier versions. In contrast, Unreal Engine by Epic Games is a widely adopted third-party engine that many studios now use to reduce development costs.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Id_Tech">id Tech - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Unreal_Engine">Unreal Engine</a></li>
<li><a href="https://en.wikipedia.org/wiki/Id_Software">id Software - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters expressed concern that Microsoft is homogenizing its studios by switching to Unreal Engine, sacrificing unique technical culture for cost savings. Some argued that open-sourcing the idTech engine, as Carmack did with Quake 3, would be a better strategy, while others noted a lack of concrete evidence that the engine team was specifically targeted.

**Tags**: `#gaming`, `#layoffs`, `#game engines`, `#Microsoft`, `#id Software`

---

<a id="item-9"></a>
## [sqlite-utils 4.0 Introduces Schema Migrations](https://simonwillison.net/2026/Jul/7/sqlite-utils-4/#atom-everything) ⭐️ 8.0/10

sqlite-utils 4.0 has been released, adding built-in database schema migrations, nested transactions via a new db.atomic() method, and support for compound foreign keys. This major version bump (first since 3.0 in 2020) significantly enhances sqlite-utils as a tool for managing SQLite databases, making schema changes safer and more reproducible for Python developers and data analysts. Migrations are defined as Python functions using a Migrations class, leveraging the existing table.transform() method for complex schema changes that SQLite's ALTER TABLE cannot handle. The release also includes breaking changes documented in an upgrade guide.

rss · Simon Willison · Jul 7, 19:32

**Background**: sqlite-utils is a Python library and CLI tool for manipulating SQLite databases, commonly used in the Datasette ecosystem. Schema migrations allow developers to version-control database schema changes and apply them incrementally, which was previously a manual or third-party task.

<details><summary>References</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jul/7/sqlite-utils-4/">sqlite-utils 4.0, now with database schema migrations</a></li>
<li><a href="https://sqlite-utils.datasette.io/en/latest/migrations.html">Database migrations - sqlite-utils</a></li>
<li><a href="https://github.com/simonw/sqlite-utils">GitHub - simonw/sqlite-utils: Python CLI utility and library ... Managing Database Versions and Migrations in SQLite sqlite-utils 4.0, now with database schema migrations #Shorts SQLite Schema Versioning: Track and Apply Migrations (2026) SQLite Versioning & Migration Strategies for Evolving Apps</a></li>

</ul>
</details>

**Tags**: `#sqlite`, `#python`, `#database`, `#migrations`, `#open source`

---

<a id="item-10"></a>
## [Ph.D. Thesis on Differentiable Ray Tracing for Radio Propagation](https://www.reddit.com/r/MachineLearning/comments/1upvkp5/phd_thesis_on_differentiable_ray_tracing_for/) ⭐️ 8.0/10

A Ph.D. thesis has been published that presents differentiable ray tracing for radio propagation modeling, integrating automatic differentiation via JAX to compute gradients through physical environments for inverse problems and ML training. This work bridges differentiable simulation and wireless communications, enabling gradient-based optimization for channel modeling, localization, and material calibration, which is crucial for next-generation wireless design. The thesis is structured as an accessible textbook with three parts: physics fundamentals, algorithmic core including GPU-accelerated path tracing and discontinuity smoothing, and practical applications. The author developed open-source libraries like DiffeRT using JAX packages (jaxtyping, equinox, optimistix).

reddit · r/MachineLearning · /u/jeertmans · Jul 7, 13:45

**Background**: Differentiable ray tracing extends traditional ray tracing by enabling gradient computation through the rendering pipeline, which is useful for inverse problems and machine learning. Radio propagation modeling predicts how radio waves travel in environments, essential for wireless network planning. JAX is a framework for high-performance numerical computing with automatic differentiation.

<details><summary>References</summary>
<ul>
<li><a href="https://people.csail.mit.edu/tzumao/diffrt/">Differentiable Monte Carlo Ray Tracing through Edge Sampling</a></li>
<li><a href="https://research.nvidia.com/publication/2024-10_learning-radio-environments-differentiable-ray-tracing">Learning Radio Environments by Differentiable Ray Tracing | Research</a></li>
<li><a href="https://docs.jax.dev/en/latest/automatic-differentiation.html">Automatic differentiation — JAX documentation</a></li>

</ul>
</details>

**Discussion**: The Reddit community received the thesis positively, with comments highlighting its value as a textbook-style resource and its integration of JAX for differentiable simulation. The author engaged actively, answering questions about differentiable ray tracing and JAX-based ray tracing engines.

**Tags**: `#differentiable ray tracing`, `#radio propagation`, `#automatic differentiation`, `#JAX`, `#wireless communications`

---

<a id="item-11"></a>
## [Mozilla CTO AMA on Open Source AI Report](https://www.reddit.com/r/MachineLearning/comments/1upxdvc/raffi_krikorian_cto_mozilla_ama_on_the_state_of/) ⭐️ 8.0/10

Mozilla CTO Raffi Krikorian announced an AMA on July 14 to discuss the inaugural State of Open Source AI report, covering real-world production costs, enterprise adoption, the China effect, and developer trust. This AMA provides a rare opportunity for the AI/ML community to directly engage with a major industry leader about the practical realities of open source AI, which is increasingly critical as enterprises and developers navigate cost, trust, and geopolitical factors. The report focuses on the hidden costs of 'free' models, the gap between marketing and real enterprise adoption, the impact of capable Chinese open-source models, and insights from over 950 developers on tool trust. Krikorian also plans to discuss the 'agentic harness'—the infrastructure layer above models that is becoming the key battleground.

reddit · r/MachineLearning · /u/raffikrikorian · Jul 7, 14:51

**Background**: Open source AI refers to AI models and tools released with permissive licenses that allow free use, modification, and distribution. The 'agentic harness' is the software infrastructure that wraps around an LLM or AI agent, handling tasks like memory, tool use, and sandboxing, enabling autonomous behavior. The 'China effect' describes how Chinese AI labs are releasing competitive open-weight models at low or no cost, reshaping global leverage in AI development.

<details><summary>References</summary>
<ul>
<li><a href="https://www.langchain.com/blog/the-anatomy-of-an-agent-harness">The Anatomy of an Agent Harness - langchain.com</a></li>
<li><a href="https://www.technologyreview.com/2026/04/21/1135658/china-open-source-models-ai-artificial-intelligence/">China’s open-source bet: 10 Things That Matter in AI Right ...</a></li>
<li><a href="https://www.mozilla.org/en-US/foundation/annualreport/2024/article/evolving-together-redefining-mozilla-in-the-ai-era/">Evolving Together: Redefining Mozilla in the AI Era</a></li>

</ul>
</details>

**Tags**: `#open source AI`, `#Mozilla`, `#enterprise AI`, `#AI costs`, `#developer trust`

---

<a id="item-12"></a>
## [Defending fine-tuning poisoning via trusted LoRA subspace](https://www.reddit.com/r/MachineLearning/comments/1uq68li/what_if_a_model_could_only_learn_what_trusted/) ⭐️ 8.0/10

A new paper proposes constraining fine-tuning to a subspace learned from trusted LoRA adapters, making malicious updates geometrically unreachable. The approach was tested on 196 public LoRA adapters and shows strong defense against adaptive attacks. This provides a novel defense against fine-tuning poisoning attacks, which are a growing concern for AI safety. By restricting the space of learnable updates, it offers a proactive alternative to detection-based defenses, potentially improving the security of fine-tuned models in production. The defense constrains updates to a subspace spanned by trusted LoRA adapters, ensuring that only behaviors represented in the pool can be learned. The paper reports that attack success drops sharply while useful adaptation is largely preserved on tasks covered by the adapter pool.

reddit · r/MachineLearning · /u/Bright_Warning_8406 · Jul 7, 20:00

**Background**: LoRA (Low-Rank Adaptation) is a parameter-efficient fine-tuning method that learns low-rank updates to pre-trained weights. Fine-tuning poisoning attacks inject malicious data to cause the model to learn hidden backdoors. Existing defenses typically detect or filter poisoned data, but this work takes a different approach by geometrically constraining the update space.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.01938">[2510.01938] StelLA: Subspace Learning in Low-rank Adaptation ... StelLA: Subspace Learning in Low-rank Adaptation using ... SuLoRA: Subspace Low-Rank Adaptation for Parameter-Efficient ... SuLoRA: Subspace Low-Rank Adaptation for Parameter-Efcient ... GitHub - SonyResearch/stella: StelLA: Subspace Learning in ... LaST-LoRA: Adaptive Knowledge Reuse and Latent Subspace ...</a></li>

</ul>
</details>

**Discussion**: Reddit comments discuss the feasibility and limitations of the approach, with some questioning whether the subspace constraint might also limit beneficial adaptation. Others express interest in seeing the method broken and suggest potential improvements.

**Tags**: `#AI Safety`, `#Fine-tuning`, `#LoRA`, `#Adversarial Robustness`, `#Machine Learning`

---

<a id="item-13"></a>
## [Elon Musk Dissolves xAI, Rebrands as SpaceXAI](https://x.com/i/status/2074214064746832060) ⭐️ 8.0/10

Elon Musk announced the dissolution of xAI, which will be rebranded as SpaceXAI and fully integrated into SpaceX. The company has already begun using the SpaceXAI name in a computing partnership announcement with Anthropic. This restructuring consolidates Musk's AI efforts under SpaceX, potentially accelerating AI development for space exploration and other applications. It also marks the end of xAI as an independent entity, reshaping the competitive landscape among AI startups. The acquisition, completed on February 2, 2026, valued SpaceX at $1 trillion and xAI at $250 billion. SpaceXAI's flagship product remains the Grok chatbot, and it also operates the Colossus supercomputer and a data center business.

telegram · zaihuapd · Jul 7, 02:30

**Background**: xAI was founded by Elon Musk in 2023 as an independent AI company to develop the Grok chatbot. In February 2026, SpaceX acquired xAI in an all-stock transaction, making it a wholly owned subsidiary. The rebranding to SpaceXAI reflects deeper integration into SpaceX's operations.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/XAI_(company)">SpaceXAI - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/SpaceXAI">SpaceXAI</a></li>
<li><a href="https://www.businessinsider.com/xai-rebrand-spacexai-new-logo-x-handle-spacex-2026-7">XAI Rebrands to SpaceXAI With New Logo, X Handle, Under ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Elon Musk`, `#xAI`, `#SpaceX`, `#corporate restructuring`

---

<a id="item-14"></a>
## [China Plans $295B National Compute Network with Domestic AI Chips](https://t.me/zaihuapd/42399) ⭐️ 8.0/10

China plans to invest approximately 2 trillion yuan ($295 billion) over the next five years to build a national interconnected data center network, with state-owned telecom operators managing major facilities. The plan prioritizes domestic AI chips from Huawei and other local suppliers, aiming for at least 80% domestic content to reduce reliance on US companies like Nvidia and AMD. This massive investment signals China's strategic push to achieve self-sufficiency in AI infrastructure, potentially reshaping global tech supply chains. The integration of regional compute resources into a unified network could accelerate AI adoption across industries and reduce dependence on foreign technology. The plan is a key part of Beijing's 'Six Networks' infrastructure initiative, which aims to integrate scattered regional compute resources. China Telecom, China Unicom, and other operators have already launched token-based pricing plans, selling compute power like mobile data to pave the way for large-scale AI applications.

telegram · zaihuapd · Jul 7, 04:45

**Background**: China's 'East Data West Computing' project and the national integrated compute network aim to address supply-demand mismatches and high costs by connecting data centers across regions. The 'Six Networks' plan includes water, power, communication, underground pipelines, logistics, and compute networks, with total investment exceeding 7 trillion yuan. Token-based pricing for compute power is a new model where users pay per token, similar to mobile data plans, making AI compute more accessible.

<details><summary>References</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/2023358290831111769">国家数据局最新部署：全国一体化算力网8大枢纽+10大集群最全梳理</a></li>
<li><a href="https://www.gov.cn/zhengce/zhengceku/202401/content_6924596.htm">关于深入实施“东数西算”工程加快构建全国一体化算力网的实施意见_国务...</a></li>
<li><a href="https://news.qq.com/rain/a/20260518A05V3X00">Token套餐全面上线!三大运营商悉数入局，算力进入“按Token收费”时代_...</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#China tech policy`, `#semiconductors`, `#cloud computing`, `#national strategy`

---

<a id="item-15"></a>
## [DeepSeek Develops Own AI Inference Chip to Reduce Reliance on Nvidia and Huawei](https://www.reuters.com/world/china/chinas-deepseek-developing-its-own-ai-chip-sources-say-2026-07-07/) ⭐️ 8.0/10

DeepSeek, a Chinese AI company, is developing its own AI chip focused on inference to reduce reliance on Nvidia and Huawei, according to three sources. The effort began about a year ago and is still in early stages, with DeepSeek recruiting chip design engineers and engaging with foundries and memory companies. This strategic move could reshape the AI hardware landscape by reducing DeepSeek's dependency on sanctioned chip suppliers amid US export controls. It also highlights the growing trend of Chinese AI companies developing in-house chips to navigate geopolitical tensions and secure supply chains. The chip is designed for inference, the fastest-growing segment of AI computing demand, rather than training. DeepSeek previously relied on Nvidia H800 and Huawei Ascend chips, and founder Liang Wenfeng acknowledged chip restrictions as a challenge in a rare 2024 interview.

telegram · zaihuapd · Jul 7, 11:08

**Background**: US export controls restrict the export of advanced GPUs and semiconductor manufacturing equipment to China, aiming to limit China's AI capabilities. DeepSeek, known for its cost-efficient AI models, is now joining other Chinese firms in developing domestic alternatives to navigate these restrictions and reduce reliance on foreign suppliers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.reuters.com/world/china/chinas-deepseek-developing-its-own-ai-chip-sources-say-2026-07-07/">EXCLUSIVE: China's DeepSeek developing its own AI chip ...</a></li>
<li><a href="https://www.cryptopolitan.com/deepseek-plans-its-own-inference-chip/">DeepSeek plans its own inference chip, a threat to Nvidia and ...</a></li>
<li><a href="https://tech-ish.com/2026/07/07/deepseek-own-ai-inference-chip-nvidia-huawei/">DeepSeek is building its own AI chip to cut reliance on ...</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#DeepSeek`, `#US-China tech`, `#semiconductors`, `#inference`

---

<a id="item-16"></a>
## [China Considers Restricting Export of Top AI Models](https://www.reuters.com/world/beijing-is-looking-curbing-overseas-access-chinas-top-ai-models-sources-say-2026-07-07/) ⭐️ 8.0/10

China's Ministry of Commerce has held meetings with Alibaba, ByteDance, and Zhipu AI to discuss restricting overseas access to the country's most advanced AI models, including future releases. This move could reshape the global AI landscape by limiting the availability of competitive Chinese AI models, potentially increasing costs for foreign developers and accelerating the decoupling of US and Chinese AI ecosystems. The restrictions may apply to both closed-source and open-source models, including downloadable weights, and could also limit foreign investment in Chinese AI startups. The final scope is still under discussion.

telegram · zaihuapd · Jul 7, 11:42

**Background**: Chinese AI models, such as DeepSeek's R1, have gained global attention for their low cost and high performance. The proposed export controls aim to prevent the leakage of core AI technologies, which could be considered a threat to national security.

<details><summary>References</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/2058096089899721357">中国也要限制AI模型出口了，中美AI正式脱钩 - 知乎</a></li>
<li><a href="https://www.yzaobao.com/news/china/202607/0775872.html">路透：北京研究限制海外获取中国最先进AI模型_联合早报网</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#China`, `#export control`, `#national security`, `#geopolitics`

---