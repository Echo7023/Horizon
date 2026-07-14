---
layout: default
title: "Horizon Summary: 2026-07-15 (EN)"
date: 2026-07-15
lang: en
---

> From 36 items, 10 important content pieces were selected

---

1. [AI Coding Over-reliance Erodes Problem-Solving](#item-1) ⭐️ 8.0/10
2. [EU Age Verification App Requires Android/iOS, Sparks Debate](#item-2) ⭐️ 8.0/10
3. [New Benchmark Reveals LLM Coordination Struggles](#item-3) ⭐️ 8.0/10
4. [RL agent trained to RL-train other models autonomously](#item-4) ⭐️ 8.0/10
5. [Leaked ICM Code Suggests 2026 Fields Medalists](#item-5) ⭐️ 8.0/10
6. [DeepSeek Raises $7.4B in First Round at $50B Valuation](#item-6) ⭐️ 8.0/10
7. [AutoNavi Launches World Model Workshop with Spacetime Portal](#item-7) ⭐️ 8.0/10
8. [DeepMind CEO Calls for US-Led Global AI Watchdog](#item-8) ⭐️ 8.0/10
9. [DeepSeek seeks $71B valuation one month after first round](#item-9) ⭐️ 8.0/10
10. [White House to Enlist Power Firms, Data Centers to Shield Consumers from AI Energy Costs](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [AI Coding Over-reliance Erodes Problem-Solving](https://adi.bio/reality) ⭐️ 8.0/10

A developer shares a cautionary reflection on relying heavily on AI for coding, warning that it can result in messy, unmanageable code and strip away the satisfaction of solving problems. This article addresses a critical issue in AI-assisted development, emphasizing the risk of deteriorating code quality and loss of meaningful problem-solving, which is vital for the software engineering community. The developer describes how AI-produced code looked functional but was overly convoluted, with redundant commands and poor internal consistency. Meaningful progress resumed only after engaging directly with documentation and understanding the underlying systems.

hackernews · AdityaAnand1 · Jul 14, 11:33 · [Discussion](https://news.ycombinator.com/item?id=48905118)

**Background**: The article is part of a larger discussion on AI's role in software development. Large language models (LLMs) are increasingly used to generate code, but critics warn that without deep understanding, developers may introduce bugs and accumulate technical debt. The author emphasizes that the essence of programming lies in creatively solving real-world problems, which AI cannot replace.

**Discussion**: Commenters recount personal struggles with AI-assisted coding, describing outcomes like 'frankenstein' codebases. Some find AI useful for grunt work but caution against eroding the meaning of genuine problem-solving. A quote from Philip K Dick is used to underline the persistence of reality.

**Tags**: `#AI`, `#software engineering`, `#productivity`, `#code quality`, `#LLM`

---

<a id="item-2"></a>
## [EU Age Verification App Requires Android/iOS, Sparks Debate](https://github.com/eu-digital-identity-wallet/av-doc-technical-specification/discussions/19) ⭐️ 8.0/10

A GitHub discussion criticizes the EU digital identity wallet's age verification app for requiring Android or iOS, with no support for desktop or alternative mobile operating systems. This technical requirement raises concerns about digital sovereignty, privacy, and consent, potentially excluding users of alternative platforms and undermining trust in EU digital identity initiatives. The app is part of the EU Digital Identity Wallet framework under eIDAS 2, which aims to provide secure, private digital identification for all EU citizens by 2026.

hackernews · roundabout-host · Jul 14, 08:34 · [Discussion](https://news.ycombinator.com/item?id=48903777)

**Background**: The EU Digital Identity Wallet (EUDI Wallet) is a legislative initiative under eIDAS 2 that requires each member state to provide a digital wallet for citizens to prove identity and store documents. The age verification app is a specific use case designed to allow users to prove their age without revealing other personal data, but critics argue that mandating Android or iOS creates technical coercion and exclusion.

<details><summary>References</summary>
<ul>
<li><a href="https://ec.europa.eu/digital-building-blocks/sites/spaces/EUDIGITALIDENTITYWALLET/pages/694487738/EU+Digital+Identity+Wallet+Home">EU Digital Identity Wallet Home - EU Digital Identity Wallet -</a></li>
<li><a href="https://eidas.ec.europa.eu/efda/wallet">European Digital Identity Wallet</a></li>

</ul>
</details>

**Discussion**: Commenters express concerns about consent and digital sovereignty, with some noting that the status quo (e.g., Roblox age verification) is worse, while others argue the question should not be how to technically enforce age verification but why it is being pushed. Links to related discussions highlight that the app also bans Android systems not licensed by Google and lacks desktop support.

**Tags**: `#privacy`, `#age verification`, `#digital identity`, `#EU regulation`, `#Android/iOS`

---

<a id="item-3"></a>
## [New Benchmark Reveals LLM Coordination Struggles](https://www.reddit.com/r/MachineLearning/comments/1uwc6ni/new_llm_coordination_benchmark_benchmarking/) ⭐️ 8.0/10

A new benchmark called ALEN evaluates 13 modern LLMs on open-ended multi-agent coordination in a Minecraft-like environment, finding most achieve only ~6% normalized return, but Gemini 3.1 Pro zero-shot performs comparably to a MARL agent trained for 1 billion steps. This benchmark identifies coordination as a distinct bottleneck for LLMs beyond long-horizon task competence, with communication being the most impactful factor. The surprising zero-shot performance of Gemini 3.1 Pro suggests that some LLMs may have emergent coordination abilities that are not yet well understood. The benchmark uses a normalized return metric to account for variable episode lengths, and harness ablations show that communication has the largest effect on performance. The project provides a full paper, code, leaderboard, and interactive traces for reproducibility.

reddit · r/MachineLearning · /u/ktessera · Jul 14, 15:37

**Background**: Multi-Agent Reinforcement Learning (MARL) studies how multiple agents learn to coordinate in shared environments. Normalized return is a metric that normalizes cumulative rewards to allow fair comparison across episodes of different lengths. Harness ablations isolate the contribution of specific engineered components like communication modules to understand their impact on agent performance.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Multi-agent_reinforcement_learning">Multi-agent reinforcement learning - Wikipedia</a></li>
<li><a href="https://stackoverflow.com/questions/49801638/normalizing-rewards-to-generate-returns-in-reinforcement-learning">Normalizing Rewards to Generate Returns in reinforcement learning Usage example</a></li>
<li><a href="https://www.emergentmind.com/topics/harness-module-ablation">Harness Module Ablation in AI Agents - emergentmind.com</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#multi-agent`, `#benchmark`, `#coordination`, `#language agents`

---

<a id="item-4"></a>
## [RL agent trained to RL-train other models autonomously](https://www.reddit.com/r/MachineLearning/comments/1uwfmfa/p_rltraining_qwen36_to_rltrain_tool_using_ai/) ⭐️ 8.0/10

A developer, Dan Austin, built and trained a reinforcement learning agent (based on Qwen3.6-35B-A3B) that autonomously writes and submits complete training jobs for smaller language models (0.6B or 1.7B) using real GPUs, and uses the performance improvement of those models as reward to improve its own policy via GRPO and LoRA. This demonstrates a recursive meta-RL system where an AI agent can improve its ability to train other AI models, potentially accelerating automated machine learning and self-improving AI pipelines. If scaled, such approaches could significantly reduce the human effort required for model development. The outer-loop training cost about $1,300 total ($810 for Runpod GPUs, $465 for Tinker), with each inner training job costing only $0.13–$0.30. The agent learned to prefer the stronger 1.7B base model over 0.6B (1.7B job share rose from 42% to 95%) and began using hyperparameter configurations more frequently (from 21% to 78% of episodes).

reddit · r/MachineLearning · /u/DanAiTuning · Jul 14, 17:39

**Background**: Reinforcement learning (RL) trains an agent to make decisions by rewarding desirable outcomes. GRPO (Group Relative Policy Optimization) is an RL algorithm used for fine-tuning large language models, comparing groups of completions to update the policy efficiently. Prime Intellect's prime-rl framework enables large-scale asynchronous RL training of LLMs, while verifiers provides RL environments and evaluation tools. Tinker is a training framework that supports LoRA (Low-Rank Adaptation) and GRPO for efficient fine-tuning.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/PrimeIntellect-ai/prime-rl">GitHub - PrimeIntellect-ai/prime-rl: Agentic RL Training at Scale · GitHub</a></li>
<li><a href="https://docs.primeintellect.ai/prime-rl/overview">Overview - Prime Intellect Docs</a></li>
<li><a href="https://github.com/PrimeIntellect-ai/verifiers">GitHub - PrimeIntellect-ai/verifiers: Our library for RL environments + evals · GitHub</a></li>

</ul>
</details>

**Tags**: `#reinforcement-learning`, `#meta-learning`, `#LLM training`, `#autoML`, `#AI agent`

---

<a id="item-5"></a>
## [Leaked ICM Code Suggests 2026 Fields Medalists](https://www.reddit.com/r/math/comments/1urv4id/fields_medal_26_predictionsdiscussion/) ⭐️ 8.0/10

A user discovered a hidden schedule of Fields Medal lectures for 2026 in the ICM website's front-end code, naming Yu Deng, John Pardon, Jacob Tsimerman, and Hong Wang as the alleged winners. If confirmed, this would reveal the most prestigious award in mathematics two years early, shocking the community and potentially undermining the official announcement process. The leak comes from the ICM 2026 schedule page where four lectures were hidden but accessible via code inspection; Polymarket odds for the leak's accuracy stand at 95%.

telegram · zaihuapd · Jul 14, 05:51

**Background**: The Fields Medal is awarded every four years to mathematicians under 40 for outstanding achievements. Hong Wang recently proved the 3D Kakeya conjecture, a major breakthrough, making her a top candidate. The ICM (International Congress of Mathematicians) typically announces winners in advance, but a leak of this nature is unprecedented.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kakeya_conjecture">Kakeya conjecture</a></li>
<li><a href="https://www.quantamagazine.org/once-in-a-century-proof-settles-maths-kakeya-conjecture-20250314/">‘Once in a Century’ Proof Settles Math’s Kakeya Conjecture | Quanta Magazine</a></li>
<li><a href="https://en.wikipedia.org/wiki/Polymarket">Polymarket</a></li>

</ul>
</details>

**Discussion**: On Reddit, users had previously listed Wang and Tsimerman as strong contenders, and the leak adds weight to those predictions. Some express skepticism about the leak's validity, noting that hidden code does not guarantee official selection.

**Tags**: `#Fields Medal`, `#mathematics`, `#leak`, `#ICM`, `#awards`

---

<a id="item-6"></a>
## [DeepSeek Raises $7.4B in First Round at $50B Valuation](https://t.me/zaihuapd/42557) ⭐️ 8.0/10

DeepSeek has completed its first funding round, raising over 50 billion yuan (approximately $7.4 billion) at a valuation exceeding 50 billion yuan. The round uses a special limited partnership structure where investors put money into a fund managed by CEO Liang Wenfeng, accepting a five-year lockup and no voting rights. This massive funding round signals strong investor confidence in DeepSeek as a leading AI startup, while the unusual governance structure allows founder Liang Wenfeng to retain control despite raising substantial capital. It could set a precedent for how deep-tech startups balance large funding with founder control. Liang Wenfeng personally invested 20 billion yuan in this round. Tencent is considering investing 10 billion yuan, and CATL plans to invest 5 billion yuan, potentially becoming the largest external investors. DeepSeek has not commented on the report.

telegram · zaihuapd · Jul 14, 11:06

**Background**: Startup funding rounds typically involve investors buying equity directly in the company, often with voting rights. However, some founders use structures like limited partnerships or dual-class shares to retain control. In this case, investors contribute to a limited partnership managed by the founder, accepting a lockup and no voting rights, which is unusual for such a large round.

<details><summary>References</summary>
<ul>
<li><a href="https://lomitpatel.com/articles/founder-control-startup-funding/">Navigating Founder Control Startup Funding Dynamics</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#AI`, `#funding`, `#startup`, `#governance`

---

<a id="item-7"></a>
## [AutoNavi Launches World Model Workshop with Spacetime Portal](https://www.ithome.com/0/976/538.htm) ⭐️ 8.0/10

AutoNavi (Alibaba) released ABot-WorldStudio, a general world model workshop that generates interactive 3D worlds from text or images, featuring a 'spacetime portal' that teleports users between complete 3D environments. This marks a significant advancement in world model AI, enabling long-duration continuous reasoning (over 1 hour) and local deployment on a single RTX 5090, far exceeding the typical 1-minute limit of competitors, with open-source models that can accelerate research in embodied AI, gaming, and education. ABot-WorldStudio unifies interactive video generation and 3D Gaussian Splatting (3DGS) scene generation in one product, outputting 3DGS assets with real geometric structure and photorealistic fidelity; the underlying ABot-World model series is fully open-sourced.

telegram · zaihuapd · Jul 14, 12:22

**Background**: World models are AI systems that build internal representations of environments to simulate dynamics such as physics and object interactions, enabling planning and reasoning without real-world trial and error. 3D Gaussian Splatting (3DGS) is a volume rendering technique that achieves real-time radiance field rendering from multiple images, popularized in 2023. AutoNavi, the Chinese mapping and navigation service under Alibaba, has expanded into AI world modeling with this release.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/3D_Gaussian_splatting">3D Gaussian splatting</a></li>
<li><a href="https://en.wikipedia.org/wiki/World_model_(artificial_intelligence)">World model (artificial intelligence)</a></li>

</ul>
</details>

**Tags**: `#世界模型`, `#3D生成`, `#AI`, `#开源`, `#阿里巴巴`

---

<a id="item-8"></a>
## [DeepMind CEO Calls for US-Led Global AI Watchdog](https://www.theverge.com/tech/965270/google-deepmind-demis-hassabis-global-ai-watchdog) ⭐️ 8.0/10

DeepMind CEO Demis Hassabis has proposed creating a US-led global AI watchdog that would assess frontier models before deployment and coordinate industry-wide deployment pauses if risks are deemed too high, with the aim of starting operations by the end of 2025. This proposal from a leading AI figure could shape the future of international AI governance, addressing the urgent need for coordinated oversight as advanced AI systems become more powerful and potentially dangerous. The proposed watchdog would be composed of independent experts and representatives from the open-source community, and would have authority to evaluate frontier AI models prior to release. Hassabis has been in discussions with the Trump administration, other AI labs, and European officials, reporting positive feedback.

telegram · zaihuapd · Jul 14, 14:29

**Background**: Frontier AI models are the most advanced general-purpose AI systems, trained with massive computational resources (on the order of 10^26 FLOPS) and capable of exceeding state-of-the-art performance across multiple domains. As these models become more capable, concerns about potential risks — including misuse, accidents, and societal harm — have intensified. Currently, AI regulation remains fragmented across countries, with no global body dedicated to assessing frontier model risks before deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>
<li><a href="https://www.datacamp.com/blog/frontier-models">Frontier Models Explained: What Defines the Cutting Edge of AI | DataCamp</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#DeepMind`, `#governance`, `#policy`

---

<a id="item-9"></a>
## [DeepSeek seeks $71B valuation one month after first round](https://t.me/zaihuapd/42564) ⭐️ 8.0/10

DeepSeek, a Chinese AI startup, is in preliminary talks for a new funding round at a pre-money valuation of $71 billion, just one month after its first round at $52 billion. The company is also developing its own AI chips to reduce reliance on Nvidia and Huawei. The rapid valuation increase from $52B to $71B within a month signals strong investor confidence and the strategic importance of AI in China. Developing proprietary chips could reshape the AI hardware supply chain and reduce geopolitical risks. The first round, completed in late May, raised approximately $7 billion at a $52 billion valuation. DeepSeek's chip development effort aims to lessen dependence on Nvidia and Huawei, according to a Reuters report.

telegram · zaihuapd · Jul 14, 15:15

**Background**: DeepSeek is a Chinese AI startup focused on large language models and AI applications. The company gained attention for its competitive models similar to GPT-4. Developing its own chips is a strategic move to ensure supply chain security and cost efficiency, as US export controls restrict access to advanced Nvidia chips.

**Tags**: `#DeepSeek`, `#AI startup`, `#funding`, `#valuation`, `#AI chips`

---

<a id="item-10"></a>
## [White House to Enlist Power Firms, Data Centers to Shield Consumers from AI Energy Costs](https://t.me/zaihuapd/42566) ⭐️ 8.0/10

The White House plans to convene power companies and data center developers in the coming weeks to push for a voluntary commitment that the surge in electricity demand from artificial intelligence will not be passed on to residential and business customers. This policy could set a precedent for how the costs of AI infrastructure are distributed, preventing increased electricity bills for consumers while enabling continued AI expansion. It signals government intervention in the energy and AI sectors to balance growth with affordability. Earlier this year, companies like Google, Meta, and OpenAI signed similar commitments to bear the costs of power generation and grid upgrades for AI projects. The new round aims to expand the commitment to include electric utilities, data center operators, and governors of states at the forefront of energy grid expansion.

telegram · zaihuapd · Jul 14, 16:00

**Background**: Artificial intelligence requires massive computing power, leading to a rapid increase in electricity demand from data centers. This has raised concerns that utility costs could be shifted onto households and small businesses. The White House is seeking voluntary industry commitments to prevent that, building on earlier pledges by major tech firms.

**Tags**: `#AI`, `#energy policy`, `#data centers`, `#regulation`

---