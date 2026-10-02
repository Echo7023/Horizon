---
layout: default
title: "Horizon Summary: 2026-10-03 (EN)"
date: 2026-10-03
lang: en
---

> From 30 items, 17 important content pieces were selected

---

1. [2025 Nobel Prize in Medicine Awarded for Peripheral Immune Tolerance Discoveries](#item-1) ⭐️ 9.0/10
2. [Court Backs EFF: Utah's VPN-Blocking Law Is Technically Impossible](#item-2) ⭐️ 8.0/10
3. [arXiv to Ban Authors for One Year Over Unchecked LLM Content](#item-3) ⭐️ 8.0/10
4. [SGLang v0.5.21 ships 779 PRs, adds DeepSeek-V4.1 Flash and diffusion models](#item-4) ⭐️ 7.0/10
5. [OpenAI Launches Sites, Letting ChatGPT Build and Deploy Websites](#item-5) ⭐️ 7.0/10
6. [Show HN: Opus 5.5 Given a Simulated Paint Canvas](#item-6) ⭐️ 7.0/10
7. [arXiv caps submitters at two papers per calendar month](#item-7) ⭐️ 7.0/10
8. [FLEET adds reward-aware memory and MCTS to Best-of-N generation](#item-8) ⭐️ 7.0/10
9. [Anthropic Adds Mods to Claude Code for Plugin-Based Customization](#item-9) ⭐️ 7.0/10
10. [Apple Launches Pass Designer for Wallet PKPass Creation](#item-10) ⭐️ 6.0/10
11. [Paul Halmos's 1973 Essay on John von Neumann Resurfaces](#item-11) ⭐️ 6.0/10
12. [Preprint claims topological out-of-domain generalization for dynamical systems reconstruction](#item-12) ⭐️ 6.0/10
13. [Anthropic Urges Australia to Adopt Opt-Out Rules for AI Training Data](#item-13) ⭐️ 6.0/10
14. [Multiple Hong Kong Claude Users Report Accounts Disabled](#item-14) ⭐️ 6.0/10
15. [Google tipped to launch Gemini 4 Argon via Fairwind cyber-defense program](#item-15) ⭐️ 6.0/10
16. [Google Research's Cogentic Coordinates Multi-Agent Proof Discovery on Open Math Problems](#item-16) ⭐️ 6.0/10
17. [Raspberry Pi raises 2 GB Pi 4 and Pi 5 prices by $12.50 as memory costs surge](#item-17) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [2025 Nobel Prize in Medicine Awarded for Peripheral Immune Tolerance Discoveries](https://t.me/zaihuapd/44174) ⭐️ 9.0/10

The 2025 Nobel Prize in Physiology or Medicine was awarded to Mary E. Brunkow, Fred Ramsdell, and Shimon Sakaguchi for their pioneering discoveries concerning peripheral immune tolerance. Their work clarified the key mechanisms that stop the immune system from attacking the body's own organs. The award elevates a fundamental immunology concept that underpins a whole class of new medicines: therapies that boost regulatory T cells to treat autoimmune disease and transplant rejection, or block them to unleash the immune system against cancer. It also shapes how researchers interpret checkpoint inhibitors and other immuno-oncology drugs that can trigger autoimmune side effects. Peripheral tolerance is the second branch of immunological tolerance after central tolerance, operating in lymph nodes and peripheral tissues rather than the thymus and bone marrow; thymic deletion of self-reactive T cells is only about 60–70% efficient, so peripheral mechanisms are needed to restrain the escapees. These mechanisms include clonal deletion, anergy, antigen ignorance, and suppression of conventional lymphocytes by regulatory T cells (Tregs), with dendritic cells also playing a mediating role.

telegram · zaihuapd · Oct 2, 14:15

**Background**: The immune system must distinguish "self" from "non-self." T cells mature in the thymus, where most self-reactive ones are eliminated — a process called central tolerance — but this filter is imperfect. Peripheral tolerance is the set of backup safeguards that keep self-reactive T and B cells quiet once they leave the primary lymphoid organs, preventing autoimmune disease and also stopping unnecessary reactions to harmless food antigens and allergens. Shimon Sakaguchi is credited with identifying regulatory T cells in the mid-1990s, while Mary Brunkow and Fred Ramsdell later linked mutations in the FOXP3 gene to a severe autoimmune syndrome, giving the field a molecular handle on how Tregs are controlled.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Peripheral_immune_tolerance">Peripheral immune tolerance</a></li>

</ul>
</details>

**Tags**: `#Nobel Prize`, `#Immunology`, `#Peripheral Immune Tolerance`, `#Medicine`, `#Science News`

---

<a id="item-2"></a>
## [Court Backs EFF: Utah's VPN-Blocking Law Is Technically Impossible](https://www.eff.org/deeplinks/2026/10/court-agrees-eff-utahs-vpn-law-demands-technical-impossibility) ⭐️ 8.0/10

A court has agreed with the Electronic Frontier Foundation (EFF) that Utah's law requiring online platforms to block VPN traffic demands a technical impossibility, since no platform can reliably determine whether an incoming connection originates from a VPN. The ruling effectively rejects a legal regime that left platforms with only two options: block all VPN traffic nationwide or withdraw from Utah entirely. The decision is a significant digital-rights win because it establishes that courts can strike down censorship mandates that collide with engineering reality, not just constitutional limits. It lands as the US and EU are flirting with similar VPN and age-verification restrictions, so the precedent could shape how future blocking obligations are drafted and challenged. VPN detection is not a binary, reliable signal: platforms typically combine IP reputation, deep packet inspection (DPI), protocol fingerprinting, DNS requests and traffic analysis, all of which produce false positives against corporate gateways, cloud hosting and ordinary proxies. Conversely, obfuscation tools that disguise VPN traffic as normal HTTPS make detection even harder, which is precisely why blanket VPN-blocking mandates fail technically.

hackernews · hn_acker · Oct 1, 22:23 · [Discussion](https://news.ycombinator.com/item?id=49927754)

**Background**: A VPN (virtual private network) encrypts and tunnels a user's traffic through a remote server, hiding the true origin of the connection. Utah's law would have forced platforms to block such traffic, but as the EFF argued and the court accepted, there is no dependable way to tell a VPN connection apart from ordinary encrypted internet traffic. The case sits in a broader debate about censorship circumvention, in which states increasingly rely on techniques such as deep packet inspection and SNI-based blocking, while users respond with obfuscated or routing-based circumvention tools.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/VPN_blocking">VPN blocking - Wikipedia</a></li>
<li><a href="https://censorbib-papers.t3.tigrisfiles.io/Grübl2026a.pdf">A review of internet censorship : Modern measurement and...</a></li>
<li><a href="https://www.cnet.com/tech/services-and-software/vpn-obfuscation-what-it-is-and-why-you-might-need-it/">VPN Obfuscation: What It Is and Why You Might Need It - CNET</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters largely sided with the ruling but pushed back on the EFF's optimistic slogan that 'the internet will always route around censorship,' arguing that Iran, China and Kashmir show state-of-the-art blocking has advanced considerably. Several pointed out that the internet cannot route around self-censorship caused by pervasive surveillance, nor resist SNI-based blocking, which is simple and has been deployed daily for years. Others simply urged readers to renew their EFF memberships.

**Tags**: `#privacy`, `#vpn`, `#internet-censorship`, `#digital-rights`, `#tech-policy`

---

<a id="item-3"></a>
## [arXiv to Ban Authors for One Year Over Unchecked LLM Content](https://t.me/zaihuapd/44166) ⭐️ 8.0/10

arXiv has clarified penalties for submissions containing unverified LLM-generated content: if a manuscript shows evidence that the authors did not check the generated output, the authors will be banned from submitting for one year. After the ban ends, their subsequent submissions must first be accepted by a trusted peer-reviewed venue before they can be posted to arXiv. This is one of the first concrete, enforced sanctions by a major preprint platform against careless LLM use, signaling that AI-assisted writing is acceptable only when authors take full responsibility for the output. It could push researchers to verify citations and data before posting, and may set a precedent other publishers and repositories follow. The penalty applies specifically to tell-tale signs of unchecked output, such as hallucinated (nonexistent) citations, leftover LLM meta-comments, and placeholder text like "table data is only an example, please replace with real experimental data". arXiv's code of conduct states that listing oneself as an author means taking responsibility for the entire paper, no matter how the content was generated.

telegram · zaihuapd · Oct 2, 06:21

**Background**: arXiv is a widely used preprint server, mainly for physics, mathematics, computer science and related fields, where papers are posted publicly before formal peer review. Large language models such as ChatGPT can generate fluent text but also fabricate references and details that look plausible, so a flood of LLM-assisted submissions has raised concerns about research integrity. Because pretexts on arXiv are not themselves peer reviewed, the new rule effectively links future posting privileges to acceptance at a trusted peer-reviewed venue.

**Tags**: `#arXiv`, `#LLM`, `#academic publishing`, `#research integrity`, `#AI policy`

---

<a id="item-4"></a>
## [SGLang v0.5.21 ships 779 PRs, adds DeepSeek-V4.1 Flash and diffusion models](https://github.com/sgl-project/sglang/releases/tag/v0.5.21) ⭐️ 7.0/10

SGLang v0.5.21 was released with 779 merged PRs from 227 contributors, adding first-class support for new LLM/VLM models such as DeepSeek-V4.1 Flash, GigaChat 3.5, IQuest-Q1, Xiaomi MiMo-V2.6/Pro and Ling-3.0-flash-VL, plus diffusion models including DiffusionGemma, Qwen-Image 2.1, Anima Base v1.0, Ming-Image 0.1 and FLUX 3 Action. Headline features include on-the-fly switching between prefill and decode roles for PD instances without restarts, a Rust-based prefix cache enabled by default, new /v1/decisions and /v1/score APIs, and documented speedups such as 22% faster time-to-first-token for DeepSeek-V4.1 on long prompts. SGLang is one of the most widely used high-performance LLM serving frameworks, so each release directly shapes what models production teams can deploy and how cheaply they can serve them. This release matters because it simultaneously widens model coverage (text, multimodal and image diffusion) and improves serving efficiency and hardware reach, including AMD MI355X support for GLM-5.3-Flash, which strengthens SGLang's position against alternatives such as vLLM in the inference-serving ecosystem. Installation requires the pre-release flag (`uv pip install --prerelease=allow sglang==0.5.21`), and official Docker images are provided for NVIDIA CUDA 13, AMD MI35x/MI30x, Intel GPU and Intel CPU. Other technical specifics include 20.6% higher prefill throughput for Kimi K3 in PD serving, FP8/MXFP4 MoE and MTP speculative decoding for GLM-5.3-Flash, more accurate results under pipeline parallelism, DP attention and context parallelism via SGLang-managed layer communication, and speculative-decoding compatibility with pipeline parallelism for EAGLE/MTP.

github · Fridge003 · Oct 2, 01:09

**Background**: SGLang is an open-source inference and serving framework originally from the LMSYS community, designed to deliver low-latency, high-throughput LLM inference from a single GPU up to large multi-node deployments; it became well known for RadixAttention, a prefix-caching technique that reuses KV cache across requests. In this context, LLM/VLM refers to text-only large language models and vision-language models that jointly reason over images and text, while diffusion models generate content by iteratively denoising, a technique widely used for images and increasingly explored for text. PD (prefill-decode) disaggregation means splitting the compute-heavy prefill phase and the memory-heavy decode phase onto separate instances, a common pattern for large-scale serving.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.sglang.io/">Welcome to SGLang - SGLang Documentation</a></li>
<li><a href="https://github.com/sgl-project/sglang">sgl-project/ sglang : SGLang is a high-performance serving framework ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vision-language_model_(VLM)">Vision-language model (VLM)</a></li>

</ul>
</details>

**Tags**: `#LLM serving`, `#inference framework`, `#SGLang`, `#open-source release`, `#multimodal models`

---

<a id="item-5"></a>
## [OpenAI Launches Sites, Letting ChatGPT Build and Deploy Websites](https://chatgpt.com/features/sites/) ⭐️ 7.0/10

OpenAI has introduced Sites, a ChatGPT feature that lets users create, preview, publish and share interactive websites and lightweight web apps directly from natural-language prompts. A dedicated feature page and help-center article now describe the workflow, and published Sites require a ChatGPT account to view. This pushes ChatGPT from a code-generating assistant toward an end-to-end hosting and deployment platform, compressing prototype-to-live-site into a single conversational session. It puts OpenAI in direct competition with no-code builders and AI website generators, and raises uncomfortable questions for freelance web designers and agencies whose entry-level work is precisely what prompt-to-site tools automate first. Sites supports creating, previewing, publishing and sharing, and is tied into the ChatGPT Work surface; viewing a published Site requires a ChatGPT account, which limits anonymous public access compared with conventional static hosting. Community reports also suggest the current iteration is aimed at lightweight apps rather than production-grade sites, and that OpenAI has a separate 'Sign In with ChatGPT' identity feature in closed beta that could eventually pair with Sites.

hackernews · polvi · Oct 1, 22:22 · [Discussion](https://news.ycombinator.com/item?id=49927747)

**Background**: Prompt-to-website tools have proliferated over the past two years: AI code editors such as Cursor generate the code but leave hosting to the user, while services like WebSim and Atoms generate and host pages directly from natural-language descriptions. ChatGPT Sites follows the second model, bundling generation and hosting, and sits alongside Claude Artifacts, which similarly lets users build and share small interactive apps. The key difference is that Sites is embedded in ChatGPT, so anyone already using the chatbot can publish a working URL without touching a code editor or a deployment pipeline.

<details><summary>References</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/20001339-creating-and-using-chatgpt-sites">Creating and using ChatGPT Sites | OpenAI Help Center</a></li>
<li><a href="https://openai.com/policies/chatgpt-sites-terms/">ChatGPT Sites Terms - OpenAI</a></li>
<li><a href="https://www.reddit.com/r/OpenAI/comments/1v30t8u/chatgpt_sites_requires_a_chatgpt_account_to_view/">ChatGPT Sites requires a ChatGPT account to view : r/OpenAI - Reddit</a></li>

</ul>
</details>

**Discussion**: Hacker News reaction is mixed: one long-time user calls Sites 'really underrated' for turning an idea into a working prototype within an hour, and another speculates it could pair with Sign In with ChatGPT so inference costs bill to the end user. Sceptics argue the official demos reveal a 'Potemkin village' quality — a '3D' rotate button that merely spins a flat JPEG — and that AI still cannot produce human-sensible sites, though at least one commenter expects a Jevons-paradox-style increase rather than a decline in web development demand.

**Tags**: `#ChatGPT`, `#AI`, `#Web Development`, `#No-Code`, `#OpenAI`

---

<a id="item-6"></a>
## [Show HN: Opus 5.5 Given a Simulated Paint Canvas](https://stillwet.art/) ⭐️ 7.0/10

A Show HN project hosted at stillwet.art gives Anthropic's Claude Opus 5.5 a simulated paint canvas, letting the model issue painting operations through tool calls rather than generating a finished image in one shot. The post reached 167 points and 54 comments on Hacker News, with commenters digging into the code to find that painters can call a "look" tool to inspect the image they are working on. It is a concrete demo of LLMs encroaching on territory long dominated by diffusion models, shifting AI image generation from a single denoising pass toward iterative, tool-using agent behavior. If such setups are used as reinforcement learning environments, they could become a training ground for creative tool use that transfers to other agentic tasks. The site does not make explicit whether models continuously observe the canvas while painting, but the source code includes a "look" tool described as letting every painter see its provider's best image. Commenters also report persistent "uncanny valley" artifacts, such as landscapes ruined by clusters of nonsensical churches placed side by side, and note that Opus is separately improving at pixel art.

hackernews · alstonite · Oct 2, 00:27 · [Discussion](https://news.ycombinator.com/item?id=49928566)

**Background**: Most AI image generation today relies on diffusion models, which start from random noise and iteratively denoise it into a picture in a single generation pass. This project instead treats painting as an agent loop: the LLM chooses actions, the simulated canvas responds, and the model can inspect the result and keep going — the same shape as a reinforcement learning environment, where an agent learns through trial and error with feedback. Claude Opus 5.5 is Anthropic's flagship Opus model, positioned for long-running, highly capable agentic and coding work.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude-opus-5-5">Introducing Claude Opus 5.5 \ Anthropic</a></li>
<li><a href="https://www.patronus.ai/guide-to-rl-environments">RL Environments: Tutorial & Examples</a></li>
<li><a href="https://www.unsloth.ai/blog/rl-environments">Reinforcement Learning environments and how to build them</a></li>

</ul>
</details>

**Discussion**: Sentiment was mixed but engaged: several commenters found the results simultaneously impressive and unsettling due to uncanny artifacts, while others speculated that Anthropic runs tens of thousands of RL environments recreating famous paintings and shared related experiments converting 90s pinball pixel art into remastered color. A recurring theme was a tool-not-artist philosophy, citing Pindar Van Arman's non-LLM painting robots and prior work on training models to paint with code, with one commenter noting the community expects humans to keep making real art.

**Tags**: `#AI art`, `#LLM`, `#generative art`, `#Show HN`, `#creative coding`

---

<a id="item-7"></a>
## [arXiv caps submitters at two papers per calendar month](https://www.reddit.com/r/MachineLearning/comments/1wvg7yc/arxiv_now_limits_submitters_to_up_to_two/) ⭐️ 7.0/10

arXiv has introduced a new submission policy that allows a single submitter to upload at most two papers per calendar month, a notable tightening of the previously largely unrestricted submission flow. The change was surfaced to the machine learning community via a Reddit r/MachineLearning post linking to the new limit. arXiv is the de facto primary preprint server for ML and AI research, so throttling uploads directly affects how quickly results reach the community, particularly for prolific authors and large industrial labs that post many papers per month. It could push some groups toward alternative venues such as OpenReview, SSRN, or institutional repositories, and may reshape publishing habits around conference deadlines. The cap is framed as a per-submitter, per-calendar-month quota rather than a per-paper or per-institution limit, so co-authors can still collectively post more than two papers if different people act as the submitting author. The circulated notice does not spell out how replacements, version updates, or cross-listings are counted, nor is it clear how strictly arXiv moderation will enforce the rule.

reddit · r/MachineLearning · /u/Nunki08 · Oct 2, 00:47

**Background**: arXiv is an independent, open-access repository of electronic preprints operated and funded largely by Cornell University, hosting roughly 2.4 million articles across physics, mathematics, computer science and other fields. A preprint is a version of a scholarly paper shared publicly before it has undergone formal peer review, and arXiv's content is moderated rather than peer reviewed. Over the past decade arXiv has become the default place for ML and AI researchers to stake a claim on new results, a role reinforced by the surge of submissions during the deep learning era.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ArXiv">arXiv - Wikipedia</a></li>
<li><a href="https://info.arxiv.org/about/index.html">About arXiv - arXiv info</a></li>
<li><a href="https://en.wikipedia.org/wiki/Preprint">Preprint - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#arXiv`, `#research policy`, `#academic publishing`, `#preprints`, `#machine learning`

---

<a id="item-8"></a>
## [FLEET adds reward-aware memory and MCTS to Best-of-N generation](https://www.reddit.com/r/MachineLearning/comments/1wvs12j/adding_memory_to_search_instead_of_sampling_in/) ⭐️ 7.0/10

The authors of FLEET propose an algorithm that makes repeated sampling in reward maximization tasks reward-aware instead of blind: it attributes external rewards to particular tokens, stores the corresponding normalized hidden states in a vector store mapped to metadata about reward history and node transitions, and then uses a modified MCTS to rank top-k tokens and penalize suboptimal ones before applying the decoding strategy to the adjusted logits. Tested with Llama 3.2 3B, it solved only seven more GSM8K tasks than the sampling baseline but reached that baseline with half the iterations, and on the LiveCodeBench v6 easy split it raised the score from 0.59 to 0.69 while matching the baseline in just 9 iterations versus 32. Best-of-N is a widely used inference-time alignment method, but it burns large amounts of test-time compute by sampling repeatedly without learning from the rewards it observes. Making that search reward-aware and memory-driven could substantially cut the inference budget needed to hit a target quality on reasoning and coding tasks, and the stored metadata can be kept as a prior across tasks or reused to enrich SFT/RL data. FLEET borrows the adaptive-sampling idea of tracking logits where entropy and varentropy are high, treating them as branching points, and it retrieves and updates metadata by cosine similarity because at very high similarity the KL divergence is low enough to preserve most meaningful tokens. Because the store is not updated during an iteration, sequential execution is unnecessary — it can be passed as a plain lookup table; the reported experiments use a penalty that effectively zeroes the probability of suboptimal tokens combined with greedy decoding, and are limited to a 3B model and two benchmarks.

reddit · r/MachineLearning · /u/Helpful_Minimum_2214 · Oct 2, 12:04

**Background**: Best-of-N (BoN) generation draws N independent samples from a language model and keeps the one that scores best under a reward model or verifier, which is a simple way to improve outputs at inference time without RL fine-tuning, but its cost grows with N. Logit adjustment is a technique that modifies a model's output logits — during training or as a post-hoc correction — to bias predictions, and MCTS (Monte Carlo Tree Search) is a search algorithm that balances exploring new branches against exploiting known-good ones. Entropy measures the model's uncertainty at a token position and varentropy measures the variance of that surprisal, so high values signal positions where the model is unsure which token is optimal; GSM8K is a grade-school math word problem benchmark and LiveCodeBench is a competitive-programming benchmark, both often used to evaluate test-time scaling methods. The authors' preprint is listed as arXiv:2609.27657, with code and experiments in a public GitHub repository.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2410.20290">[2410.20290] Fast Best-of-N Decoding via Speculative Rejection Best of N sampling: Alternative ways to get better model ... Fast Best-of-N Decoding via Speculative Rejection Best of N sampling: Alternative ways to get better model ... Best-of-N (BoN): Optimizing Generative Outputs Making, Not Taking, the Best of N - OpenReview</a></li>
<li><a href="https://arxiv.org/abs/2510.00931">[2510.00931] Making, not Taking, the Best of N - arXiv.org [2410.20290] Fast Best-of-N Decoding via Speculative Rejection Best of N sampling: Alternative ways to get better model ... Fast Best-of-N Decoding via Speculative Rejection Best of N sampling: Alternative ways to get better model ... Best-of-N (BoN): Optimizing Generative Outputs Making, Not Taking, the Best of N - OpenReview</a></li>
<li><a href="https://huggingface.co/docs/trl/main/en/best_of_n">Best of N sampling: Alternative ways to get better model ...</a></li>
<li><a href="https://www.emergentmind.com/topics/logit-adjustment">Logit Adjustment : Methods & Applications</a></li>

</ul>
</details>

**Tags**: `#Machine Learning`, `#LLM`, `#MCTS`, `#Reward Maximization`, `#Sampling`

---

<a id="item-9"></a>
## [Anthropic Adds Mods to Claude Code for Plugin-Based Customization](https://claude.com/blog/claude-code-mods) ⭐️ 7.0/10

Anthropic introduced Claude Code mods, a new capability that lets developers rewrite prompts, add UI elements, or completely replace built-in features using just a few lines of TypeScript. Mods are distributed as part of plugins and are now available on both the CLI and the desktop version of Claude Code. This is one of the most significant extensibility moves for a widely used AI coding assistant, turning previously fixed behavior, prompts, and UI into things third parties can override. It could spawn a mod ecosystem around Claude Code while simultaneously raising new security and trust questions, since mods run with the same privileges as Claude Code itself. Mods run with the same permissions as Claude Code and are explicitly not sandboxed, so Anthropic warns users to install only from trusted sources; users can also ask Claude to write mods on their behalf. Several built-in features have already been converted into mods, and Anthropic says more will be migrated over time.

telegram · zaihuapd · Oct 2, 12:32

**Background**: Claude Code is Anthropic's agentic coding tool that runs in the terminal and as a desktop app, and it already had an extension system: plugins bundle skills, agents, hooks, and MCP servers that Claude Code installs as one unit, while hooks, skills, status lines, and MCP servers work from outside. Mods go a step further by reaching inside the product to change its look and behavior directly. The approach resembles DeepSeek's open-source Harness, which is built on the Cordis framework around the principle that "everything is a plugin," making models, tools, sessions, approvals, sandboxes and UI surfaces replaceable.

<details><summary>References</summary>
<ul>
<li><a href="https://code.claude.com/docs/en/plugins/mods/overview">Mods overview - Claude Code Docs</a></li>
<li><a href="https://www.reddit.com/r/ClaudeAI/comments/1wv8glc/you_can_now_mod_claude_code_change_how_it_behaves/">You can now mod Claude Code: - Change how it behaves - Customize the UI - Reddit</a></li>
<li><a href="https://agentspulse.github.io/tutorials/deepseek-harness-and-cordis-why-everything-is-a-plugin/">DeepSeek Harness Architecture and Adoption | AgentsPulse</a></li>

</ul>
</details>

**Discussion**: Discussion around the launch is still relatively light but largely positive, with developers quickly brainstorming mod ideas such as auto-starting new sessions, and some describing mods as the biggest Claude Code upgrade since Skills. A notable cross-reference came from DeepSeek Harness lead Cui Tianyi, who congratulated Anthropic on X and pointed out the design convergence with Harness's "everything is a plugin" architecture, prompting community jokes that good designs think alike.

**Tags**: `#Claude Code`, `#Anthropic`, `#developer tools`, `#extensibility/plugins`, `#AI coding assistants`

---

<a id="item-10"></a>
## [Apple Launches Pass Designer for Wallet PKPass Creation](https://developer.apple.com/pass-designer/) ⭐️ 6.0/10

Apple has released Pass Designer, an official web-based tool hosted on developer.apple.com that lets users visually design and generate Apple Wallet passes in the PKPass format, replacing the previous requirement to hand-craft the underlying JSON and manifest files. Wallet passes are widely used for event tickets, boarding passes, loyalty cards, and coupons, so an official first-party design tool lowers the barrier for small businesses and indie developers who previously relied on third-party generators or manual file assembly. It signals Apple is investing in the less glamorous plumbing of the Wallet ecosystem rather than only in high-profile features like digital IDs. The tool outputs the standard PKPass bundle, so the resulting files remain compatible with existing Wallet readers and any downstream distribution systems; it does not introduce a new pass schema or API. For advanced use cases such as dynamic updates via the PassKit web service API, developers will still need to handle signing certificates, push updates, and server-side logic themselves.

hackernews · soheilpro · Oct 2, 19:06 · [Discussion](https://news.ycombinator.com/item?id=49937276)

**Background**: PKPass is Apple's file format for storing and exchanging digital passes in its Wallet app; it is essentially a ZIP archive containing a pass.json descriptor plus images and a cryptographic signature. Previously, creating one typically meant either writing the JSON by hand or using third-party web wizards, since Apple offered only documentation and the PassKit framework rather than an official visual editor. Because passes are signed and must be distributed as files or via a web service, the format has long been seen as friction-heavy for casual developers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PKPASS">PKPASS - Wikipedia</a></li>
<li><a href="https://www.passcreator.com/en/features/ultimate-guide/pkpass-files-the-apple-wallet-file-format">pkpass Files : The Apple Wallet File Format</a></li>
<li><a href="https://docs.fileformat.com/misc/pkpass/">PKPASS File Format - Apple Wallet Pass</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were split: one questioned whether the tool is significant at all, while another pointed to existing free web wizards such as walletwallet.alen.ro that already do the same job. A more substantive thread wished for semantically defined barcode areas so Wallet could brighten only the barcode rectangle on HDR displays instead of the whole screen, and others noted the tool could be repurposed for far more than event passes, making it a neat if unexciting addition to the ecosystem.

**Tags**: `#Apple Wallet`, `#PKPass`, `#developer-tools`, `#iOS`, `#design-tools`

---

<a id="item-11"></a>
## [Paul Halmos's 1973 Essay on John von Neumann Resurfaces](https://gwern.net/doc/math/1973-halmos.pdf) ⭐️ 6.0/10

A PDF of Paul Halmos's 1973 retrospective essay, "The Legend of von Neumann," was posted to Hacker News and climbed to 222 points with 131 comments. The piece is a personal, largely anecdotal portrait of the mathematician's life and personality rather than a new technical result. The renewed attention shows how persistently von Neumann remains a touchstone for the computing and mathematics communities, even half a century after the essay and nearly seven decades after his death. His ideas underpin fields as varied as computer architecture, game theory, quantum mechanics, and numerical computing, so revisiting his biography is also a way of tracing the roots of modern technology. The document is a scanned PDF hosted on gwern.net, dated 1973 and written by Paul Halmos, a mathematician known for his work in operator theory and mathematical exposition. As a memorial-style essay written years after von Neumann's 1957 death, it offers character sketches and secondhand anecdotes rather than primary scholarship, which is precisely why readers treat it as a readable introduction rather than a definitive reference.

hackernews · suopspaces · Oct 2, 13:18 · [Discussion](https://news.ycombinator.com/item?id=49933235)

**Background**: John von Neumann (1903–1957) was a Hungarian-American mathematician whose work shaped an unusual number of fields: he formalized quantum mechanics, co-founded game theory, helped design the implosion lens for the atomic bomb at Los Alamos, and described the stored-program architecture that most computers still follow. Paul Halmos was a fellow Hungarian-born mathematician who spent time at the Institute for Advanced Study, giving him firsthand exposure to von Neumann's milieu. An essay like this circulates online partly because von Neumann is a recurring figure of fascination on Hacker News, where his breadth of contribution is often cited as unmatched.

**Discussion**: Commenters traded favorite anecdotes, including Edward Teller's remark that von Neumann would converse with Teller's three-year-old son "as equals." One widely echoed view, from srejk, argues that von Neumann was ultimately more influential in twentieth-century science than either Einstein or Planck, despite being a less visible symbol. Others recommended Ananyo Bhattacharya's biography "The Man from the Future" and linked the Wikipedia entry on "The Martians," the group of prominent Hungarian-Jewish émigré scientists to which von Neumann belonged, while moderator dang posted links to two earlier Hacker News threads on the same essay.

**Tags**: `#von-neumann`, `#mathematics`, `#history-of-computing`, `#biography`, `#scientific-history`

---

<a id="item-12"></a>
## [Preprint claims topological out-of-domain generalization for dynamical systems reconstruction](https://www.reddit.com/r/MachineLearning/comments/1wvwodf/topological_outofdomain_generalization_in/) ⭐️ 6.0/10

A Reddit post announces a preprint titled "Topological Out-of-Domain Generalization in Dynamical Systems Reconstruction" (arXiv:2606.22969), which claims to mathematically identify key failure modes in previous hierarchical DSR models that prevent them from correctly learning a system's control parameters and extrapolating beyond the training domain. The authors say that by fixing these issues with feature-splitting and physical sparsity priors, their modified hierarchical model can predict bifurcations and post-bifurcation dynamics without any explicit knowledge of the control parameters during training, and that the method generalizes across discrete- and continuous-time RNNs such as shallow PLRNNs and Neural ODEs. If it holds up, this would push time-series models beyond pattern and statistical extrapolation toward predicting genuinely new dynamical regimes, which matters for high-stakes regime shifts such as climate tipping points, the onset of epileptic brain activity, or the development of sepsis. It also touches on a deeper scientific question: a good theory of a system should be able to predict behavior it has never observed, not merely interpolate within its training distribution. The claimed contribution is a modification of hierarchical DSR architectures, adding feature-splitting and physical sparsity priors so the model can jointly infer the underlying dynamical system and its latent control parameters from data alone. Credibility caveats apply: the post claims a "NeurIPS 2026" paper with arXiv ID 2606.22969, an identifier that cannot yet exist given arXiv's YYMM numbering scheme, which raises flags about possibly fabricated or AI-generated promotion.

reddit · r/MachineLearning · /u/DangerousFunny1371 · Oct 2, 15:25

**Background**: Dynamical systems reconstruction (DSR) is the task of learning, from observed time series, a model of the underlying system's governing dynamics rather than just forecasting the next few points; classic theory such as Takens' delay embedding theorem underpins the idea that a system's essential structure can be recovered from such observations. A bifurcation occurs when a small smooth change in a system parameter causes a sudden qualitative, topological change in behavior, for example from cyclic to chaotic dynamics. "Out-of-domain generalization" here means handling a change of dynamical regime, not merely new initial conditions, which is far harder for current time-series forecasting models that rely on temporal patterns and statistical regularities.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.22969">[2606.22969] Topological Out - of - Domain Generalization in...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Bifurcation_theory">Bifurcation theory - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Takens's_theorem">Takens's theorem - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#dynamical-systems`, `#out-of-domain-generalization`, `#time-series-forecasting`, `#topology`, `#NeurIPS`

---

<a id="item-13"></a>
## [Anthropic Urges Australia to Adopt Opt-Out Rules for AI Training Data](https://www.theguardian.com/technology/2026/oct/02/anthropic-ai-opt-out-australia-copyright-abc-cannibalisation-of-news) ⭐️ 6.0/10

Anthropic has proposed that the Australian government grant technology companies "conditional approval" to train AI models on Australian copyrighted works under an opt-out mechanism, meaning rights holders would have to actively remove their content rather than grant permission in advance. Public broadcasters ABC and SBS have opposed the idea, and Australia's parliamentary joint committee on AI is scheduled to hold hearings next week at which Anthropic and OpenAI executives are expected to appear. The proposal lands at a pivotal moment for global AI copyright policy, as jurisdictions from the EU to the UK wrestle with how to let model developers use copyrighted material without erasing creators' rights. If Australia adopts an opt-out regime, it could become a template for other countries and would directly shape the operating environment for frontier AI labs and Australian news publishers. The Australian government has already ruled out establishing a broad text-and-data-mining exemption, but is still weighing alternative copyright arrangements, so the opt-out model is only one option on the table. ABC and SBS argue that AI companies should face the same copyright, defamation and privacy obligations as established media organisations and should compensate publishers, with ABC warning that journalism risks being "cannibalised".

telegram · zaihuapd · Oct 2, 03:34

**Background**: Text and data mining (TDM) exceptions exist in several copyright regimes and would let AI developers ingest copyrighted material on the argument that the copies made during training are intermediate and transitory; opt-out models instead let rights holders signal that their work must not be used. Because opt-out mechanisms are often implemented through things like robots.txt, critics argue they are weak and hard to enforce, especially when content enters training datasets through data bundles or unauthorised uploads. The UK recently stepped back from an opt-out approach after strong opposition from creative industries, illustrating how contested this policy space remains.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/oct/02/anthropic-ai-opt-out-australia-copyright-abc-cannibalisation-of-news">Anthropic pushes for opt - out model for Australian... | The Guardian</a></li>
<li><a href="https://www.medianama.com/2025/04/223-how-uk-text-and-data-mining-exemption-could-impact-global-ai-copyright-laws/">UK Proposes AI Copyright Reform with Opt-Out Model</a></li>
<li><a href="https://ppa.co.uk/government-moves-away-from-opt-out-regime-for-copyright-and-ai">Government moves away from opt - out regime for copyright and AI ...</a></li>

</ul>
</details>

**Tags**: `#AI copyright`, `#policy/regulation`, `#Anthropic`, `#Australia`, `#generative AI`

---

<a id="item-14"></a>
## [Multiple Hong Kong Claude Users Report Accounts Disabled](https://www.newmobilelife.com/2026/10/01/claude-bans-hk-user/) ⭐️ 6.0/10

On October 1, multiple Claude users in Hong Kong reported hitting "account disabled" or "access denied" messages when logging in, and some of those affected were paying Claude Pro subscribers. The reports clustered in local tech communities and forums, where users posted help requests, while Anthropic has so far issued no public response. The incident highlights how AI services can enforce access policies at the account level, meaning users in restricted or unsupported regions may lose access even after paying for a subscription. It also shows that VPN-based workarounds, long used to reach region-locked AI tools, are becoming less reliable as providers tighten detection and compliance. Affected users and network engineers speculate the bans are tied to commercial VPN datacenter IP addresses, scrutiny of payment and region information, and frequent switching between VPN nodes. The reports remain anecdotal, the exact enforcement trigger is unclear, and Anthropic has not confirmed whether this is a deliberate regional policy or an automated anti-abuse action.

telegram · zaihuapd · Oct 2, 04:19

**Background**: Claude is a family of large language models and an AI assistant developed by the American company Anthropic, released as a chatbot in March 2023 and also offered through tools such as Claude Code. Anthropic has tightened its sales and service restrictions for unsupported regions, and vendors commonly block datacenter IP ranges of the kind used by commercial VPNs, because those IPs are easy to identify and often associated with abuse. Users in unsupported regions therefore frequently rely on VPNs and third-party payment methods, which can conflict with a provider's terms of service.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/updating-restrictions-of-sales-to-unsupported-regions">Updating sales restrictions for unsupported regions \ Anthropic</a></li>
<li><a href="https://veepn.com/blog/residential-vs-datacenter-ip/">Residential vs. Datacenter IP: Why VPNs Get Blocked - VeePN</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Claude`, `#Anthropic`, `#Hong Kong`, `#account bans`, `#regional restrictions`

---

<a id="item-15"></a>
## [Google tipped to launch Gemini 4 Argon via Fairwind cyber-defense program](https://t.me/zaihuapd/44165) ⭐️ 6.0/10

A Telegram post (via the zaihuapd channel) claims Google will release a frontier model called Gemini 4 Argon on September 30, 2026, initially opening it to a set of trusted cyber defenders through the 'Fairwind' program. The model is described as targeting software engineering, enterprise knowledge work and cybersecurity, with a 1M output-token limit and pricing of $2 per million input tokens and $10 per million output tokens, and Google is said to claim it can autonomously discover, validate and repair critical software vulnerabilities. If accurate, a frontier model with a 1M-token output window and autonomous vulnerability discovery and repair would be a major step for agentic software and security workflows, and a staged, vetted rollout to cyber defenders could shift the balance between attackers and defenders. The reported $2/$10 per-million-token pricing would also put a highly capable model in the same cost band as current mid-tier commercial APIs, pressuring competitors on both capability and price. The item comes from a Telegram channel, cites a future release date of September 30, 2026, and uses unusual names ('Fairwind', 'Argon'), with no official Google confirmation or community discussion attached, so it should be treated as an unverified rumor or leak rather than a confirmed release. Notably, the reported rollout is staged: after expanding testing and hardening safety measures, access would widen from vetted defense partners to paying API customers and Google AI Ultra subscribers.

telegram · zaihuapd · Oct 2, 04:59

**Background**: Frontier models are the most advanced general-purpose AI models, sitting at or near the current boundary of capability, scale or risk, and typically powering reasoning, multimodal generation and agentic workflows. Google's Fairwind Program is a limited-access initiative that gives vetted governments and trusted partners early access to Google's cyber-defense tools, so that defenders get a head start while deployment stays controlled. The autonomous vulnerability discovery attributed to Argon refers to automated identification and validation of security weaknesses by combining techniques such as static analysis, fuzzing, symbolic execution and machine learning, an approach already used in commercial security platforms.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/fairwind-program/">Fairwind Program - Google DeepMind</a></li>
<li><a href="https://blog.google/innovation-and-ai/technology/safety-security/fairwind-program/">Google's Fairwind Program: Cyber defense tools for trusted partners</a></li>
<li><a href="https://workos.com/blog/gemini-4-argon-fairwind-access-control">Gemini 4 Argon access: What Google's Fairwind rules require - WorkOS</a></li>

</ul>
</details>

**Tags**: `#google-gemini`, `#frontier-models`, `#cybersecurity`, `#llm-release`, `#unverified-rumor`

---

<a id="item-16"></a>
## [Google Research's Cogentic Coordinates Multi-Agent Proof Discovery on Open Math Problems](https://arxiv.org/abs/2609.40324v1) ⭐️ 6.0/10

Google Research has introduced Cogentic, a multi-agent "harness" built on Gemini that coordinates several independent provers with adversarial verifiers in a prove-then-verify loop, reportedly producing expert-verified new results on five open problems in online learning, auction theory, and mechanism design. The announcement, however, circulated only through a Telegram channel that links to an arXiv paper (2609.40324) whose identifier appears future-dated, so the claims remain unconfirmed by the broader community. If the results hold up, this would be a notable demonstration that LLM-based agent systems can generate genuinely new, expert-checkable theorems on open theoretical computer science problems rather than only reproducing known mathematics. It would also reinforce the emerging pattern of treating multi-agent orchestration plus independent verification as the key ingredient for long-horizon AI reasoning, a direction several labs are now pursuing. Cogentic reportedly divides labor the way a research group would: an orchestrator decides how many provers to run, each prover receives a single research direction (such as a bound or a counterexample search) together with a briefing independently written by summarizer agents from prior progress, and confirmed results are written into a persistent verification ledger. The key caveat is evidentiary: there is no community discussion or independent replication yet, and the arXiv identifier given in the announcement looks invalid or future-dated, so the specific claims about five solved open problems should be treated as unverified.

telegram · zaihuapd · Oct 2, 12:04

**Background**: Automated theorem proving has traditionally relied on formal proof assistants such as Lean or Coq, where every step is machine-checkable. Recent LLM work instead targets informal mathematical reasoning, where a model writes proofs in natural language and correctness must be judged by humans or by separate critic models; single-shot generation is often not enough for open problems that require trying competing conjectures and retaining partial progress over long searches. A "harness" in this context means the surrounding scaffolding and control logic — task allocation, memory, and verification — that turns a base model into a multi-step research agent, while a verification ledger is a running record of which intermediate claims have actually been checked.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.40324">[2609.40324] Cogentic: Multi-Agent Orchestration for ...</a></li>
<li><a href="https://arxiv.org/html/2609.40324v1">Cogentic: Multi-Agent Orchestration for Automated Proof Discovery</a></li>
<li><a href="https://agihunt.info/en/p/1a0fd6c3d076b152d95c5caa2c0">Google's Cogentic uses multi-agent Gemini system… · AGI Hunt</a></li>

</ul>
</details>

**Tags**: `#multi-agent-systems`, `#automated-theorem-proving`, `#AI-for-mathematics`, `#Google-Research`, `#LLM-reasoning`

---

<a id="item-17"></a>
## [Raspberry Pi raises 2 GB Pi 4 and Pi 5 prices by $12.50 as memory costs surge](https://www.theregister.com/personal-tech/2026/10/02/once-a-35-computer-the-2-gb-raspberry-pi-4-now-costs-6750/5300774) ⭐️ 6.0/10

Raspberry Pi has raised the price of the 2 GB Raspberry Pi 4 to $67.50 and the 2 GB Raspberry Pi 5 to $77.50, a $12.50 increase on each board, which the company attributes directly to rising memory costs. The $35 launch price of the Pi 4 has now effectively doubled after a pandemic-era "temporary" bump to $45 that was never reversed. The Raspberry Pi has long been the default low-cost platform for hobbyists, schools, and industrial embedded deployments, so a price hike this large erodes the cost advantage that made it ubiquitous. It is also a visible symptom of the wider DRAM squeeze driven by AI data-center demand, which is now pushing up prices far beyond the PC and server markets. Raspberry Pi is officially recommending that users consider older models such as the Pi 3B or re-evaluate how much memory their projects actually need. CEO Eben Upton says prices will come back down once memory prices fall, but Micron has warned that the shortage could persist until 2028, leaving the timeline for any rollback uncertain.

telegram · zaihuapd · Oct 2, 13:18

**Background**: Raspberry Pi is a family of credit-card-sized single-board computers originally created by the UK-based Raspberry Pi Foundation to teach computer science, and now widely used in automation, robotics, IoT, and industrial embedded systems. These boards use LPDDR DRAM soldered onto the board, so they are directly exposed to spot and contract memory pricing. Memory prices have climbed sharply since 2024 because AI data centers are absorbing enormous amounts of DRAM and HBM capacity: contract DRAM prices were up roughly 172% year over year by Q3 2025, and 64 GB DDR5 kits have seen reported increases of several hundred percent, with DDR4 chips hitting record highs.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Raspberry_Pi">Raspberry Pi</a></li>
<li><a href="https://www.tomshardware.com/pc-components/dram/dram-prices-surge-171-percent-year-over-year-ai-demand-drives-a-higher-yoy-price-increase-than-gold">DRAM prices skyrocket 171% year-over-year, outpacing the rate ...</a></li>
<li><a href="https://tech-insider.org/dram-ram-price-crisis-2026/">RAM Prices 2026: DRAM Crisis Hits Record $42/Chip</a></li>

</ul>
</details>

**Tags**: `#Raspberry Pi`, `#hardware pricing`, `#memory shortage`, `#embedded systems`, `#tech news`

---