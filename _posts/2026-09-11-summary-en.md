---
layout: default
title: "Horizon Summary: 2026-09-11 (EN)"
date: 2026-09-11
lang: en
---

> From 35 items, 21 important content pieces were selected

---

1. [Microsoft Elevates Rust to Tier-1 Language Status](#item-1) ⭐️ 9.0/10
2. [DeepSeek Releases V4.1 Flash With Detailed Tech Report and Ultra-Low Cache Pricing](#item-2) ⭐️ 9.0/10
3. [Calif Research demos WeWorm, first zero-click worm spreading via WeChat calls](#item-3) ⭐️ 9.0/10
4. [Researchers question whether OpenAI can be trusted with unpublished math](#item-4) ⭐️ 8.0/10
5. [Shopify moves its mobile app back from React Native to fully native development](#item-5) ⭐️ 8.0/10
6. [Sony PlayStation digital game ownership lawsuit under scrutiny](#item-6) ⭐️ 8.0/10
7. [DeepSeek ships MIT-licensed Harness framework and opens V4-Pro-0813 weights](#item-7) ⭐️ 8.0/10
8. [Essay Theorizes Software Development Drives People Insane](#item-8) ⭐️ 7.0/10
9. [Cognition launches SWE-2 coding model, claiming parity with Fable 5.1 and GPT-Astra](#item-9) ⭐️ 7.0/10
10. [NASA's Mars False-Color Trick Now Reveals Hidden Earth Rock Art](#item-10) ⭐️ 7.0/10
11. [Raymond Chen reveals Windows XP's algorithm for picking your first user picture](#item-11) ⭐️ 7.0/10
12. [SemiAnalysis Examines Behind-the-Meter Power Hurdles for Datacenters](#item-12) ⭐️ 7.0/10
13. [Fly connectome fails to learn Pong; audit exposes pipeline bugs](#item-13) ⭐️ 7.0/10
14. [Ant International, Visa, Mastercard Team Up on AI Agent Payment Standard](#item-14) ⭐️ 7.0/10
15. [Moonshot AI (Kimi) Confidentially Files for Hong Kong IPO at $50B Valuation](#item-15) ⭐️ 7.0/10
16. [Tencent Hunyuan Open-Sources AuK, a Unified Audio Editing Model](#item-16) ⭐️ 7.0/10
17. [PlanetScale launches Neki, a closed-source Postgres sharding product](#item-17) ⭐️ 6.0/10
18. [.blend URL Viewer: Preview Blender Files in the Browser](#item-18) ⭐️ 6.0/10
19. [348M model trained on 22.7B tokens solves 14-digit arithmetic by showing work](#item-19) ⭐️ 6.0/10
20. [ChatGPT voice mode adds GPT-5.6 Sol and GPT-6 Astra selection](#item-20) ⭐️ 6.0/10
21. [HBM Shortage Drives 20-50% Price Hikes on Chinese AI Chips](#item-21) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Microsoft Elevates Rust to Tier-1 Language Status](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 9.0/10

In a guest post published by the Rust Foundation, Microsoft confirmed that it now treats Rust as a tier-1 language, placing it alongside long-established options such as C, C++, and C# for internal systems work. The designation means Rust receives first-class tooling, engineering investment, and support across Microsoft's platforms rather than being an experimental or hobbyist choice. Microsoft is one of the largest vendors of operating systems and developer tooling, so its formal endorsement gives Rust a strong signal of legitimacy in systems programming and could push other large OS and platform vendors to broaden their language choices for greenfield development. It also matters for security: memory-safety bugs have historically accounted for roughly 70% of Microsoft's CVEs, and Rust's ownership model is designed to eliminate many of those classes of defects. Some specifics behind the headline come from the surrounding discussion rather than the announcement itself: commenters cite a Microsoft goal to convert 1 billion lines of code to Rust by 2030 using automated tooling at a rate of "1 engineer, 1 month, 1 million lines of code," plus DARPA-funded work splitting C-to-Rust automated conversion across six teams. Open questions remain about how far tier-1 status extends, particularly whether Visual Studio will get first-class Rust debugging support and what the MSVC integration rumors will amount to.

hackernews · mmastrac · Sep 10, 13:39 · [Discussion](https://news.ycombinator.com/item?id=49643546)

**Background**: Systems programming means writing the low-level software that makes a computer work — operating systems, device drivers, memory management and networking layers — where performance and direct hardware control matter, and C and C++ have dominated for decades. Rust is a comparatively new language that aims to match C/C++ performance while using compile-time "ownership" rules to prevent memory-safety errors like buffer overflows and use-after-free bugs. Many companies assign internal "tiers" to languages, where tier-1 means fully supported, recommended, and backed by official tooling for production use, as opposed to experimental tiers. Greenfield development refers to building new software from scratch with no legacy code constraints, which is often where a language like Rust can be adopted without a costly rewrite.

<details><summary>References</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=49643546">Rust Is Tier - 1 Language at Microsoft | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Systems_programming">Systems programming - Wikipedia</a></li>
<li><a href="https://qarea.com/blog/difference-between-brownfield-and-greenfield-software-development">Difference between Brownfield and Greenfield Software Development</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (509 points, 279 comments) is largely positive, with commenters calling it big news that all major OS vendors with a role in C/C++ tooling are now diversifying their systems-language options for greenfield work. Several argue the announcement shows Rust is no longer a fledgling, fast-moving language but a mature competitor to C++ and C#, with fewer rough edges than newer "better C/C++" alternatives like Zig and Odin; others welcome long-awaited public news about MSVC integration. Scepticism also appears: one commenter jokes that adopting Rust should mean Microsoft's Weather app stops consuming over 1GB of RAM, and others press on whether tier-1 debugging support in Visual Studio will actually arrive.

**Tags**: `#Rust`, `#Microsoft`, `#programming languages`, `#systems programming`, `#software engineering`

---

<a id="item-2"></a>
## [DeepSeek Releases V4.1 Flash With Detailed Tech Report and Ultra-Low Cache Pricing](https://twitter.com/deepseek_ai/status/2097930608790167907) ⭐️ 9.0/10

DeepSeek released DeepSeek-V4.1-Flash, publishing the model weights on Hugging Face alongside a detailed technical report. The new model scales up to 552B parameters, nearly double the 284B of the original V4 Flash, and advertises a cache-hit input price of just $0.003 per million tokens. The release drew 886 points and 495 comments on Hacker News within a short period. DeepSeek continues to push frontier-scale training while disclosing unusually detailed research, contrasting with the safety-heavy system cards common among US labs. The extreme cache-hit pricing raises a broader question about whether inference economics could restructure how agents and chat APIs are built, since reusing cached context may soon cost less than transmitting it over the network. Commenters note the model is now 552B parameters, which is only nominally a 'Flash' tier and much harder to run locally than the previous 284B version, and they caution that benchmark gains may partly reflect 'benchmaxxing' rather than real-world capability. The headline cache-hit rate of $0.003 per million tokens applies only to repeated input tokens billed at the cached rate instead of the full cache-miss rate, so cost depends heavily on workload patterns and cache hit ratio.

hackernews · Liwink · Sep 10, 06:11 · [Discussion](https://news.ycombinator.com/item?id=49639090)

**Background**: Cache-hit pricing is a common LLM API mechanism in which repeated prompt tokens — typically a long stable prefix such as a system prompt or codebase context — are billed at a lower cached rate instead of the full input rate; competitors such as OpenAI typically discount cached input by roughly 50%, making DeepSeek's rate unusually aggressive. LLM inference prices overall have fallen dramatically, by some estimates a factor of about 1,000 in three years, so pricing structure is increasingly a competitive differentiator rather than a footnote. Parameter count matters because larger models require proportionally more GPU memory to serve locally, which is why the jump from 284B to 552B changes the deployment story for self-hosting users.

<details><summary>References</summary>
<ul>
<li><a href="https://rephrase-it.com/blog/deepseek-v4-cache-pricing-changes-agents">DeepSeek V4 Cache Pricing Changes Agents | Rephrase</a></li>
<li><a href="https://epoch.ai/data-insights/llm-inference-price-trends">LLM inference prices have fallen rapidly but unequally... | Epoch AI</a></li>
<li><a href="https://tkmxai.it.com/openai-vs-anthropic-vs-google">OpenAI vs Anthropic vs Google - ai inference - LLM Gateway Daily</a></li>

</ul>
</details>

**Discussion**: Sentiment is broadly positive and analytically minded: commenters praise DeepSeek's technical report for being full of engineering detail, in contrast to system cards they see as heavily weighted toward safety content, and admire the team's willingness to commit bold research bets at near-frontier scale. Several commenters focus on economics, wondering whether $0.003/M cache-hit tokens could make the chat completion API obsolete if transferring context over the network costs more than the cached tokens themselves, while others point out that the 552B size undermines the 'Flash' branding and makes local deployment far harder.

**Tags**: `#LLM`, `#DeepSeek`, `#model release`, `#AI research`, `#inference pricing`

---

<a id="item-3"></a>
## [Calif Research demos WeWorm, first zero-click worm spreading via WeChat calls](https://simonwillison.net/2026/Sep/10/calif-research/) ⭐️ 9.0/10

Calif Research published a demo of WeWorm on September 8, 2026, describing it as the first zero-click worm that spreads through WeChat calls across both iOS and Android, with the exploit demonstrated spreading among three test phones. The team says that working with AI, it found the bug and wrote the first remote code execution (RCE) exploit in about two days, then spent one more week building the worm. WeChat has well over a billion users, so a worm that propagates through ordinary incoming calls without any victim interaction represents a potentially enormous attack surface. More broadly, the claim that AI compressed months of offensive security work by a larger team into roughly nine days signals a significant shift in how quickly vulnerabilities can be discovered and weaponized. According to Calif Research, the victim does not need to answer the call or interact with the phone at all, and even if they do answer they hear nothing while the exploit still succeeds. The published item is a demo rather than a full technical disclosure, and the demonstration involved three test phones; it is listed as part of the company's Android-tagged research.

rss · Simon Willison · Sep 10, 00:56

**Background**: A "zero-click" exploit is one that runs without any action from the victim, which makes it far harder to defend against than an attack that requires opening a file or tapping a link. A worm is malware that copies itself automatically from machine to machine, and remote code execution (RCE) means an attacker can run arbitrary code on a target device over the network. WeChat calls are handled by a large, complex client on both iOS and Android, and Calif Research's broader point is that AI-assisted vulnerability discovery is already accelerating the pace at which such bugs are found and turned into working exploits.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/09/wechat-zero-click-worm-took-over.html">WeChat Zero-Click Worm Took Over Accounts on iPhone and Android via Incoming Calls</a></li>
<li><a href="https://www.helpnetsecurity.com/2026/09/08/wechat-weworm-vulnerability-exploit-account-hijacking/">"Zero-click" WeChat worm could hijack accounts and spread via a single call - Help Net Security</a></li>
<li><a href="https://www.vulncheck.com/blog/ai-assisted-vulnerability-discovery">The First CVE Wave: Signs That AI-Assisted Vulnerability Discovery Is Reshaping Disclosure Volumes | Blog | VulnCheck</a></li>

</ul>
</details>

**Tags**: `#security`, `#AI`, `#WeChat`, `#zero-click`, `#RCE`

---

<a id="item-4"></a>
## [Researchers question whether OpenAI can be trusted with unpublished math](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

A Hacker News thread (roughly 373 points and 466 comments) debated whether researchers can trust OpenAI after reports circulated that the company used insights gained from private collaborations with mathematicians to publish results without giving the collaborating researchers attribution. The discussion was sparked by posts on Mathstodon, X and Bluesky, including claims that OpenAI's internal models were solving open problems quickly while the researchers who had interacted with its models received no credit. Attribution and trust are the foundation of academic collaboration, so if researchers believe a frontier lab can mine their unpublished ideas without credit, many may stop sharing work-in-progress with AI models or with the labs behind them. This could reshape how AI companies collaborate with the scientific community and intensify calls for clearer data-use and disclosure policies. A central point of contention is OpenAI's reported claim that the model producing the result was not trained on the collaborative chats, with commenters arguing that both claims can hold at once: large models may memorize and internalize chat-derived intuition during pretraining, while reinforcement learning on verifiable math could independently discover genuinely novel techniques. Others note the asymmetry of information, since OpenAI has reportedly given large numbers of researchers free model access while keeping its internal models and training details private.

hackernews · pred_ · Sep 10, 06:49 · [Discussion](https://news.ycombinator.com/item?id=49639408)

**Background**: Large language models are typically pretrained on massive amounts of text, which can include conversations users have with chatbots, and are then refined with techniques such as reinforcement learning on problems whose answers can be automatically verified, like mathematics. In academia, using someone's unpublished ideas without credit is considered serious misconduct, so the debate hinges on whether an AI system counts as a collaborator and whether improvements come from memorized user data or from reasoning the model discovers on its own.

**Discussion**: The prevailing sentiment is skepticism toward OpenAI, with commenters like nezi framing it as analogous to a human collaborator who takes ideas from a colleague, publishes along those lines, and omits attribution, which they call highly unethical. Others such as sashank_1509 argue both explanations can coexist—pretraining may internalize chat-derived intuition while RL on verifiable math discovers superhuman techniques unrelated to any specific chat—and bertonvv openly wonders whether AI is genuinely accelerating on open problems or merely appearing to, given how much fresh data researchers feed it.

**Tags**: `#AI ethics`, `#OpenAI`, `#research attribution`, `#LLM training data`, `#AI policy`

---

<a id="item-5"></a>
## [Shopify moves its mobile app back from React Native to fully native development](https://shopify.engineering/back-to-native) ⭐️ 8.0/10

Shopify's engineering team published an article announcing that it is moving its mobile app away from React Native and back to fully native development for iOS and Android. The decision, detailed at shopify.engineering/back-to-native, quickly became one of the most discussed engineering stories of the day on Hacker News. Shopify is a high-profile company reversing the industry's widespread adoption of cross-platform frameworks, making this a closely watched case study on the real tradeoffs between React Native and native development. It also feeds a broader debate about whether AI-generated native code now reduces the cost advantage that cross-platform frameworks were supposed to provide. Shopify's own content emphasizes engineering reasoning rather than a single technical defect, and the surrounding discussion highlights that AI-assisted code generation tools are increasingly used to rewrite mobile apps from one platform to another. Community members report migrating mid-sized apps (roughly 15-20 screens) quickly with tools like Codex and Maestro, though they note the last mile of polish still takes manual effort.

hackernews · fnthawar2 · Sep 10, 14:09 · [Discussion](https://news.ycombinator.com/item?id=49643982)

**Background**: React Native is an open-source UI framework originally developed by Meta (then Facebook) that lets developers build apps for both iOS and Android using JavaScript and React, sharing most of the codebase across platforms. Native development instead means writing separate code for each platform, typically Swift or Objective-C for iOS and Kotlin or Java for Android, which can offer better performance and platform-specific polish at the cost of maintaining two codebases. AI-assisted code migration uses large language models and coding agents to translate or rewrite code between languages and frameworks, promising to cut the manual effort of such rewrites.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/React_Native">React Native - Wikipedia</a></li>
<li><a href="https://reactnative.dev/">React Native · Learn once, write anywhere</a></li>
<li><a href="https://www.patternfly.org/ai/ai-assisted-development/ai-assisted-code-migration/">PatternFly • AI - assisted code migration</a></li>

</ul>
</details>

**Discussion**: With 573 points and 395 comments, the discussion is broadly receptive to Shopify's reasoning: many argue the cross-platform-versus-native choice is simply a resource-dependent engineering decision rather than an ideological one. Several commenters say AI code generation has weakened React Native's main selling point of letting web developers build mobile apps, while others share first-hand AI-assisted migration experiences and one veteran notes the debate has cycled for nearly two decades without a universal answer.

**Tags**: `#React Native`, `#mobile development`, `#native apps`, `#Shopify`, `#engineering decisions`

---

<a id="item-6"></a>
## [Sony PlayStation digital game ownership lawsuit under scrutiny](https://consumerrights.wiki/w/Sony_PlayStation_digital_game_ownership_lawsuit) ⭐️ 8.0/10

A consumerrights.wiki reference page documenting the Sony PlayStation digital game ownership lawsuit has drawn heavy attention on Hacker News (302 points, 99 comments). The filings described on the page quote PlayStation's Terms of Service, whose Section 14 imposes a binding arbitration agreement and class action waiver, and requires any user who does not wish to be bound to notify Sony in writing within 30 days of accepting the agreement. The dispute goes to the heart of what consumers actually receive when they click "buy" on a digital storefront, and whether arbitration clauses can effectively block collective legal remedies in the games industry. A ruling against Sony could push console platforms toward clearer ownership language or refund obligations across the wider digital media market. The 30-day opt-out window requires written notice to Sony, meaning most players are bound by default without ever realizing it, and arbitration removes both the right to a jury trial and the ability to join a class action. The filings also highlight a striking argument built on the fact that two plaintiffs each bought the same title, Resident Evil Requiem, from the PlayStation Store on different dates at $69.99, which cuts against the idea that a purchase transfers an exclusive copy.

hackernews · haunter · Sep 10, 12:18 · [Discussion](https://news.ycombinator.com/item?id=49642531)

**Background**: Digital storefronts generally sell licenses rather than physical copies, so the buyer's rights are defined by an end-user license agreement and terms of service rather than by traditional property law. Since the 2011 US Supreme Court decision in AT&T Mobility v. Concepcion, arbitration clauses with class action waivers have become standard in tech and gaming terms of service, making it very difficult for consumers to sue collectively. This lawsuit tests whether labeling a purchase as a sale while legally treating it as a revocable license is deceptive.

**Discussion**: Commenters were broadly critical of forced arbitration, with one calling it something that should be outright illegal since its only use is stripping consumers and workers of their rights. Others argued by analogy to books, noting that two people each own their own copy without owning the same copy, and one commenter observed that Sony's defense could open a legal door Sony would rather keep shut. A further commenter expressed ambivalence toward Sony, citing its 2005 rootkit incident as evidence of a large, clumsy company capable of bad decisions.

**Tags**: `#digital ownership`, `#consumer rights`, `#Sony PlayStation`, `#class action lawsuit`, `#arbitration clauses`

---

<a id="item-7"></a>
## [DeepSeek ships MIT-licensed Harness framework and opens V4-Pro-0813 weights](https://t.me/zaihuapd/43738) ⭐️ 8.0/10

DeepSeek released DeepSeek Harness (dsh), an MIT-licensed open-source agent harness whose models, tools, skills, sessions, sandboxes, storage, scheduling and UI are all implemented as swappable plugins, and it also opened the weights of DeepSeek-V4-Pro-0813 on Hugging Face. Harness offers four runtime modes — Standard, PTC, Minimal and Creative — and is distributed via npm and GitHub. The release gives developers a vendor-neutral, fully modular stack for building agents, positioning DeepSeek directly against established coding-agent harnesses such as Claude Code while letting teams swap in their own model, sandbox or UI layer. Opening the flagship V4-Pro weights on top of that lowers the barrier to self-hosted, production-grade agent deployments and strengthens the open-weight ecosystem around large mixture-of-experts models. In PTC mode Harness keeps the Standard-mode toolset but exposes tools through a generated SDK and the reserved run_code transport, where nested calls re-enter the full guarded tool pipeline — safe calls may overlap, exclusive calls act as ordering barriers, and side effects are not rolled back, so token savings remain workload-dependent. According to OpenRouter listings, DeepSeek-V4-Pro-0813 is a large mixture-of-experts model with a 1,048,576-token context window, a maximum output of 393,216 tokens and pricing around $0.99 per million input tokens and $2.97 per million output tokens.

telegram · zaihuapd · Sep 10, 07:28

**Background**: An "agent harness" is the orchestration layer around a language model that decides how the model calls tools, runs code, manages sessions and sandboxes its execution — the difference between a raw model API and a usable coding assistant. DeepSeek Harness follows a "everything is a plugin" design, so each of those capabilities can be swapped or recomposed instead of being baked in. "Open weights" means the trained parameters are published on Hugging Face so anyone can download, fine-tune or self-host the model, as opposed to accessing it only through an API. DeepSeek-V4-Pro-0813 is the official release of the V4-Pro line, superseding the earlier preview version and emphasizing stronger agentic capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">GitHub - deepseek-ai/deepseek-harness: DeepSeek Harness: Everything is a Plugin. · GitHub</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro-0813">deepseek-ai/DeepSeek-V4-Pro-0813 · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#open-source`, `#LLM`, `#model-release`, `#AI-agents`

---

<a id="item-8"></a>
## [Essay Theorizes Software Development Drives People Insane](https://graybeard.ing/software-drives-people-insane/) ⭐️ 7.0/10

An essay published on the blog graybeard.ing argues that the practice of software development itself drives people insane, framing everyday engineering pain as a psychological hazard rather than a mere workflow problem. The piece reached the Hacker News front page, collecting roughly 350 points and 131 comments. The post and its reception tap into a broader industry conversation about developer burnout, mental health, and the erosion of engineering culture as teams grow and become further removed from users. It matters because it names a frustration many engineers feel but rarely articulate, and because the comment thread surfaces competing explanations for why the job feels destabilizing. The essay is observational and anecdotal rather than empirical, so its "theory" is a rhetorical frame rather than a testable claim, and the discussion adds concrete comparisons such as mission-critical real-time trading systems built 20 years ago by teams of a couple dozen developers, with the core trading kernel handled by just four people. Commenters also introduce factors the essay underplays, including ego, management structures, and the intermediary role of project managers.

hackernews · rglover · Sep 10, 16:13 · [Discussion](https://news.ycombinator.com/item?id=49646181)

**Background**: Hacker News is a widely read technology forum where essays about engineering culture regularly become discussion hubs, and "the job makes you crazy" pieces are a recurring genre known for prompting debate about developer life. Software development involves long feedback loops, invisible progress, and frequent requirement changes, conditions that are commonly linked in industry writing to burnout and stress. The thread also reflects an ongoing argument about team size, since many engineers feel that modern organizations employ far more developers than comparable projects once required.

**Discussion**: Commenters largely accepted the premise but disagreed on the root cause: bob1029 argued the real driver is development untethered from customers, since regular user contact massively dampens the madness, especially when teams are siloed off behind a project manager. tcdent suggested the underlying mechanism is human ego expressed through software, proposing a reductionist Zen Buddhist attitude toward professional creativity, while hliyan noted team sizes have ballooned compared with 20 years ago, when a couple dozen developers built mission-critical real-time trading systems. anigbrowl countered that the problem is not software but that most managers are not developers, leaving them in the same position as customers demanding features without understanding the work.

**Tags**: `#software-engineering`, `#developer-culture`, `#mental-health`, `#burnout`, `#industry-commentary`

---

<a id="item-9"></a>
## [Cognition launches SWE-2 coding model, claiming parity with Fable 5.1 and GPT-Astra](https://cognition.com/blog/swe-2) ⭐️ 7.0/10

Cognition released SWE-2, a coding-focused model that it says rivals Anthropic's Fable 5.1 and OpenAI's GPT-Astra, and which the company describes as post-trained from the Kimi K3 base model. The launch drew heavy Hacker News attention (228 points, 109 comments), with much of the debate centering on whether the reported benchmark scores reflect real capability or benchmark overfitting. The release adds another closed-weight entrant to an already crowded coding-model market, and the fact that a vendor can reach frontier-level coding claims by post-training an existing open-weight base like Kimi K3 suggests the capability gap between open and closed models is narrowing fast. That dynamic puts pressure on pricing, access terms, and the credibility of vendor-published benchmarks across the whole ecosystem. The most-cited caveat is a large score gap between benchmarks: SWE-2 reportedly scores 92.8% on Terminal Bench 2.1 but only 27.3% on Terminal Bench 4, which was released just a couple of weeks earlier, suggesting limited generalization to novel tasks. The model is closed-weight with no public parameter or training details beyond the Kimi K3 post-training disclosure.

hackernews · seelos · Sep 10, 15:29 · [Discussion](https://news.ycombinator.com/item?id=49645443)

**Background**: Coding benchmarks such as the SWE-bench-style and Terminal Bench suites measure how well a model completes realistic software engineering tasks in a sandboxed environment; because these suites are public, models can be tuned specifically for them, a practice commenters call "benchmaxxing." Fable 5.1 is Anthropic's flagship model for large coding projects, while GPT-Astra is OpenAI's newest generation model, so both are the reference points that a coding-model launch is now measured against. The open-versus-closed-weight distinction matters here: open-weight models such as Kimi K3 publish downloadable parameters, whereas closed-weight models are only reachable through a vendor's hosted API, and Cognition's choice of the former as a base while shipping the latter is what fuels the debate.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT -6 Astra - Wikipedia</a></li>
<li><a href="https://openk3.org/blog/open-weight-vs-closed-weight-models">Open Weight vs Closed-Weight Models: Key Differences | OpenK3</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread is broadly skeptical: the top objections are the 92.8% versus 27.3% split between Terminal Bench 2.1 and Terminal Bench 4 as evidence of benchmark overfitting, and the lack of any indication that SWE-2 is open-weight, with one commenter asking why anyone would choose it over DeepSeek Flash 4.1. Others note Cognition's past demo of an autonomous Upwork-completing coding bot that did not hold up under scrutiny, while conceding that post-training from the already capable Kimi K3 means the model "can't be that bad." A separate strand of criticism targets Cognition's Devin product, described as the most consistently disappointing tool the commenter has used.

**Tags**: `#AI coding models`, `#LLM benchmarks`, `#closed-weight models`, `#Cognition`, `#HN discussion`

---

<a id="item-10"></a>
## [NASA's Mars False-Color Trick Now Reveals Hidden Earth Rock Art](https://gizmodo.com/this-nasa-color-trick-was-meant-for-mars-now-its-unveiling-rock-art-on-earth-2000809844) ⭐️ 7.0/10

A false-color image enhancement technique originally developed for NASA's Mars missions is being repurposed to reveal faint, weathered rock art on Earth, as detailed in a NASA Spinoff article linked by commenters. The method, a decorrelation stretch, amplifies subtle color differences that are invisible to the naked eye, turning barely perceptible petroglyphs into clearly visible markings. The crossover shows how planetary-science imaging pipelines can be recycled for terrestrial archaeology and cultural-heritage preservation, letting researchers document fragile or remote sites without touching them. It also lowers the barrier to entry, since the same effect can be approximated in free tools like GIMP, encouraging wider experimentation in remote sensing and image analysis. The core algorithm is a decorrelation stretch based on principal component analysis, which removes inter-channel correlation and rescales variance so color differences stand out. Commenters note that a comparable result can be produced in GIMP by decomposing an image into LAB components, maximizing contrast on the A and B chroma channels with auto input levels, then recomposing.

hackernews · gumby · Sep 10, 15:29 · [Discussion](https://news.ycombinator.com/item?id=49645437)

**Background**: False color is a family of rendering methods that assign visible colors to data recorded outside the human-visible spectrum, or that recombine visible bands, so features that differ in reflectance become obvious. NASA has long used it on Mars images, where subtle surface variations are hard to spot in a single band. Decorrelation stretch is the specific enhancement that makes these differences pop, and the same principle underlies multispectral satellite archaeology.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/False_color">False color - Wikipedia</a></li>
<li><a href="https://www.mdpi.com/2227-7390/13/20/3297">Numerical Methods for Decorrelation Stretch - MDPI</a></li>
<li><a href="https://www.dstretch.com/DecorrelationStretch.pdf">Algorithm Theoretical Basis Document for Decorrelation ...</a></li>

</ul>
</details>

**Discussion**: Commenters were enthusiastic, with one recalling false-color composites as a Eureka moment in understanding signals and sensors, and noting that vegetation appears red rather than green in such imagery. Several shared practical tips, including a step-by-step GIMP workflow, a request for an ImageMagick implementation suitable for a pipeline, and one account of unsuccessfully hunting for hidden rock art at Angkor Wat with bandpass filters.

**Tags**: `#remote sensing`, `#image processing`, `#archaeology`, `#false color`, `#NASA`

---

<a id="item-11"></a>
## [Raymond Chen reveals Windows XP's algorithm for picking your first user picture](https://devblogs.microsoft.com/oldnewthing/20260909-00/?p=112683) ⭐️ 7.0/10

In a September 2026 post on his Old New Thing blog, Microsoft engineer Raymond Chen explained that Windows XP did not simply grab the first file in the Default Pictures folder, but instead ran a one-pass random selection routine over the directory listing. The code uses the RtlRandomEx random number generator seeded with the current value of GetTickCount(), and caps the scan at 100 images as a safety check. The post is a rare documented look at an undocumented corner of Windows internals, and it illustrates how a trivial-sounding feature still required deliberate engineering choices about randomness and filesystem behavior. It matters less for what it changes today than as a case study in how small decisions inside a shipped operating system were made and later forgotten. Chen notes that the routine is a one-pass random selection algorithm, so it does not need to enumerate and store the whole directory before choosing. It also stops after sampling 100 pictures, which avoids pathological behavior if somebody drops a million files into the Default Pictures directory; community members additionally linked what appears to be the corresponding leaked Windows source code on GitHub.

hackernews · soheilpro · Sep 10, 09:04 · [Discussion](https://news.ycombinator.com/item?id=49640646)

**Background**: Windows XP introduced a welcome screen where each user account was shown with a picture, and a fresh account was automatically assigned one of the images shipped in the Default Pictures folder. The Old New Thing is Raymond Chen's long-running Microsoft blog about the history and design rationale behind Windows, and posts like this are aimed at developers curious about why shipped software behaves the way it does. RtlRandomEx is a Windows runtime library pseudo-random number generator, and GetTickCount() returns milliseconds elapsed since system start, which makes it a convenient but low-entropy seed.

<details><summary>References</summary>
<ul>
<li><a href="https://devblogs.microsoft.com/oldnewthing/20260909-00/?p=112683">What algorithm did Windows XP use to choose your initial user picture ?</a></li>
<li><a href="https://aicrier.com/post/ttwhpyi9i21yl5cdxocy">Raymond Chen reveals Windows XP avatar algorithm — AICrier</a></li>

</ul>
</details>

**Discussion**: Commenters largely treated the post as a small treat: one praised Raymond Chen's Windows internals writing as "a little Xmas," while another shared a GitHub link to the actual code. A recurring theme was the mental shift programming requires, since picking something at random is trivial for a human but requires deliberate algorithm design on a computer, and one reader lamented that daily task pressure erodes the awareness needed to notice such subtle problems at all.

**Tags**: `#Windows internals`, `#algorithms`, `#randomness`, `#software history`, `#Hacker News`

---

<a id="item-12"></a>
## [SemiAnalysis Examines Behind-the-Meter Power Hurdles for Datacenters](https://newsletter.semianalysis.com/p/what-is-so-hard-about-behind-the) ⭐️ 7.0/10

SemiAnalysis published Part 1 of a series titled 'What is So Hard About Behind-The-Meter Power For Datacenters?', examining the technical and economic challenges of on-site power for datacenters. The teaser notes that in 2026 year-to-date Microsoft has signed over 5GW of behind-the-meter nameplate capacity, including 2.7GW with Chevron and well over 2GW through turnkey datacenter leases with companies such as Crusoe. AI datacenters are consuming unprecedented amounts of power, and grid interconnection delays are pushing operators toward behind-the-meter generation to secure capacity quickly. This shift could reshape energy procurement, utility relationships, and datacenter operations, affecting hyperscalers like Microsoft, power equipment vendors, and local grids. The article notes that on-site generation requires new skills, operating models, and risk frameworks, and that behind-the-meter microgrids often begin as 'bridge power' until a permanent grid interconnect is available. The full breakdown of Microsoft's 5GW portfolio is available only to SemiAnalysis Energy Model subscribers, and the Part 1 teaser does not include the complete analysis.

rss · Semianalysis · Sep 10, 14:28

**Background**: Behind-the-meter power refers to electricity generated and consumed on the customer's side of the utility meter, bypassing the public transmission and distribution grid. Datacenters traditionally rely on grid power plus backup generators, but AI workloads need massive, continuous capacity that strained grids cannot always provide on schedule. As a result, operators are increasingly signing deals for on-site natural gas, fuel cells, microgrids, and turnkey power arrangements with energy and infrastructure companies.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/what-is-so-hard-about-behind-the">What is So Hard About Behind-The-Meter Power For Datacenters ...</a></li>
<li><a href="https://www.datacenterknowledge.com/energy-power-supply/why-data-centers-produce-their-own-power">Why Data Centers Are Turning to Behind-the-Meter Power</a></li>
<li><a href="https://www.williams.com/2026/03/17/powering-data-centers-behind-the-meter-power-explained/">Powering data centers: behind-the-meter power, explained</a></li>

</ul>
</details>

**Tags**: `#datacenters`, `#energy`, `#power infrastructure`, `#AI infrastructure`, `#behind-the-meter`

---

<a id="item-13"></a>
## [Fly connectome fails to learn Pong; audit exposes pipeline bugs](https://www.reddit.com/r/MachineLearning/comments/1wc67ci/i_tried_to_make_a_real_fly_connectome_learn_to/) ⭐️ 7.0/10

An ML practitioner attempted to train a small subgraph of the real MaleCNS v1.0 fly connectome (166k EM-reconstructed neurons) to track a Pong ball using dopamine-style plasticity, and it did not learn — learning-on and learning-off runs produced bit-for-bit identical results across multiple seeds. Auditing why uncovered a neuPrint regex bug (full-match vs substring semantics) that silently zeroed out two entire neuron populations, an original neuron selection with no path from photoreceptors to anything else, and four motor neurons of which half had zero synapses from any sensory pathway. Carefully audited negative results are rare and valuable, and this case study is a concrete counterweight to the viral "fly brain plays Doom / Minecraft / Beat Saber" demos, whose own repositories reportedly admit failed validation gates, a silent motion-detection pathway, hand-injected behaviors, and overfitting to a single track. It underscores that connectome-driven agents need reproducibility checks, not just plausible-looking motion in a permissive game engine. The falsified circuit hypothesis was a courtship-pursuit visual tracking pathway, and after rebuilding around a descending neuron that connected end to end, learning-on vs learning-off finally diverged — but the effect looked like the learning rule globally quieting the system because misses outnumber hits, so punishment dominates and shrinks the motor response rather than producing skill. The author also notes the scope is a small subgraph rather than a generalizable result and invites others to probe the central complex and steering circuits.

reddit · r/MachineLearning · /u/oPeraza2007 · Sep 10, 02:28

**Background**: A connectome is a neuron-by-neuron wiring diagram reconstructed from electron microscopy images; MaleCNS v1.0 is Janelia FlyEM's release of the full adult male Drosophila central nervous system, comprising roughly 166,000 neurons, and it is distributed through the natverse 'malecns' R package and queried via neuPrint, Janelia's web/API tool for connectomics. Dopamine-style plasticity refers to synaptic weight updates gated by a reward or punishment signal, analogous to reinforcement learning. The Pong test bed was chosen precisely because its hit-or-miss signal provides essentially nowhere to hide a null result.

<details><summary>References</summary>
<ul>
<li><a href="https://male-cns.janelia.org/">Male CNS Connectome - MaleCNS connectome</a></li>
<li><a href="https://github.com/natverse/malecns">GitHub - natverse/malecns: Access to the latest 'Janelia ...</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC9350508/">neuPrint: An open access tool for EM connectomics - PMC</a></li>

</ul>
</details>

**Tags**: `#connectome`, `#computational-neuroscience`, `#reinforcement-learning`, `#reproducibility`, `#negative-results`

---

<a id="item-14"></a>
## [Ant International, Visa, Mastercard Team Up on AI Agent Payment Standard](https://www.cnbc.com/2026/09/10/ant-international-visa-mastercard-ai-agent-payment-standard.html) ⭐️ 7.0/10

Ant International announced a collaboration with Visa and Mastercard to build a universal standard for AI agent payments, including a "Know Your Agent" (KYA) mechanism that links each agent to a valid legal entity, evaluates its behavior, and monitors risk. The three parties cited a McKinsey projection that AI agents could handle $3 trillion to $5 trillion of global consumer commerce transactions by 2030. If three of the world's largest payment players converge on one rulebook, AI agents registered with one provider could transact across others without repeated onboarding, which would remove a major friction point for autonomous commerce. It also signals that incumbent card networks intend to shape agentic payments rather than cede the space to crypto-native or platform-specific protocols. The announcement is a standards and partnership initiative rather than a shipped product, and no technical specification, timeline, or governance structure has been published yet. Interoperability is framed as letting an agent registered with one payment provider avoid repeated registration with others, and KYA is positioned alongside existing human-facing compliance regimes such as KYC and AML.

telegram · zaihuapd · Sep 10, 03:00

**Background**: AI agents are software programs that can browse, negotiate, and pay on a user's behalf, but unlike people they have no passports, birth certificates, or addresses, so merchants and networks lack an obvious way to confirm that an agent is legitimate and authorized. "Know Your Agent" is an emerging identity standard that verifies an agent's identity, the delegation chain back to the controlling human or organization, and the spending limits it was given before a payment is authorized. Several competing efforts already exist, including Google's Agent Payments Protocol (AP2), announced in September 2025, and Chainlink's interoperability work for cross-network agent transactions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.cryptonomist.ch/2026/09/10/ai-agent-payment-standards/">AI Agent Payment Standards Set by Visa, Mastercard, Ant</a></li>
<li><a href="https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol">Announcing Agent Payments Protocol (AP2) | Google Cloud Blog</a></li>
<li><a href="https://skyfire.xyz/know-your-agent-kya/">Know Your Agent ( KYA ) - Skyfire</a></li>

</ul>
</details>

**Tags**: `#AI Agents`, `#Payments`, `#Fintech`, `#Standards`, `#Industry News`

---

<a id="item-15"></a>
## [Moonshot AI (Kimi) Confidentially Files for Hong Kong IPO at $50B Valuation](https://t.me/zaihuapd/43743) ⭐️ 7.0/10

Moonshot AI, the Chinese company behind the Kimi chatbot, has confidentially submitted an A1 filing to the Hong Kong Stock Exchange to formally start a Hong Kong IPO, while the company said it has no information to disclose. At the same time it is reportedly advancing a new funding round at a $50 billion pre-money valuation, which may be its last round before listing. If it lists, Moonshot would become one of the first Chinese large-model unicorns to reach the public market, giving investors a rare public benchmark for valuing Chinese LLM startups. Its roughly 8x valuation jump in half a year also raises the stakes for peers, with another leading model company, DeepSeek, expected by outsiders to list in the first half of next year. The A1 form is the initial application document for a Hong Kong listing, and the filing was made confidentially, so detailed financials have not been publicly released; Moonshot declined to comment. According to the report, its valuation rose from about $4.3 billion at the end of 2025 to $35 billion post-money in July, while it shipped K2.5, K2.6 and K3 between January and July on a roughly three-month release cadence.

telegram · zaihuapd · Sep 10, 10:58

**Background**: Moonshot AI is the Chinese company that develops the Kimi assistant and the Kimi series of open-weight large language models, which support multimodal image and video input and offer agentic features such as the Swarm multi-sub-agent mode. In Hong Kong, a company files an A1 form with the Hong Kong Stock Exchange to formally begin an IPO application, and a confidential filing lets it test the market before details become public; 'pre-money valuation' means the company's value before the new money is added. DeepSeek is another Chinese developer of open-weight frontier models, based in Hangzhou and backed by the High-Flyer hedge fund, and is widely seen as the next major Chinese model company that could list.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_(AI)">Kimi (AI) - Wikipedia</a></li>
<li><a href="https://www.kimi.com/">Kimi AI 官网- K3 上线，专为智能体编程与知识工作打造</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek</a></li>

</ul>
</details>

**Tags**: `#AI Industry`, `#IPO`, `#Moonshot AI/Kimi`, `#LLM`, `#China Tech`

---

<a id="item-16"></a>
## [Tencent Hunyuan Open-Sources AuK, a Unified Audio Editing Model](https://x.com/TencentHunyuan/status/2097996926876795197) ⭐️ 7.0/10

Tencent Hunyuan released AuK, an open-source foundational speech model that handles zero-shot text-to-speech, voice/timbre, style and emotion editing, accent removal, and multi-speaker separation through a single natural-language interface. Alongside the base model it shipped AuK-Flash, a distilled variant using 4-step inference that Tencent says runs roughly 4.5x faster under matched conditions, with code, model weights, and a demo all published. AuK collapses a stack of previously separate speech tools — TTS, voice conversion, enhancement, and source separation — into one open-weight model, which lowers the barrier for developers who would otherwise stitch together many proprietary APIs. A permissively licensed, self-hostable model of this scope from a major lab also intensifies competition with closed speech vendors and other open releases in the fast-moving speech-generation space. AuK is a compact ~1.5B-parameter model released under the MIT license, and the distilled AuK-Flash operates without classifier-free guidance to achieve its 4-step generation. The checkpoint bundles the diffusion transformer and layer-fusion weights, while the MLLM encoder and VAE are loaded from separate files at runtime, so missing text_encoder.* keys during checkpoint loading are expected rather than an error.

telegram · zaihuapd · Sep 10, 11:56

**Background**: Zero-shot TTS means the model can clone or synthesize a voice from a short reference audio clip without any fine-tuning on that speaker. Diffusion-based speech models typically need dozens of denoising steps to produce audio, which makes them slow; distillation compresses that process into a handful of steps, trading some quality for latency. Historically these capabilities — generation, editing, enhancement, separation — lived in separate specialized models, each with its own interface and weights.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Tencent-Hunyuan/AuK">Tencent-Hunyuan/AuK: AuK: An Open-Source Foundational Model for...</a></li>
<li><a href="https://auk-project.github.io/">AuK — An Open-Source Foundational Model for Speech Generation...</a></li>
<li><a href="https://www.orcarouter.ai/blog/auk-flash-open-source-release">AuK-Flash & AuK: Tencent's Quiet Open-Source Speech Model</a></li>

</ul>
</details>

**Tags**: `#audio-editing`, `#text-to-speech`, `#open-source-models`, `#Tencent-Hunyuan`, `#speech-generation`

---

<a id="item-17"></a>
## [PlanetScale launches Neki, a closed-source Postgres sharding product](https://planetscale.com/blog/introducing-neki) ⭐️ 6.0/10

PlanetScale introduced Neki, a database sharding solution for Postgres, in a blog post on planetscale.com. The announcement drew mixed community reaction, largely because the post never clearly explained what Neki actually is or what it is for, and because the product ships as closed source. PlanetScale is one of the best-known managed database vendors, so its entry into Postgres sharding signals growing competition in the tooling that lets Postgres scale past a single node. The choice to keep Neki closed source puts it in direct contrast with Supabase's open-source multigres, making the launch a flashpoint in the ongoing debate over open versus proprietary database infrastructure. According to PlanetScale's documentation, Neki provides horizontal sharding for Postgres along with zero-downtime operations, online DDL, replication workflows and cluster management, all running on real Postgres rather than a fork. The critical caveat is availability and licensing: Neki is closed source, and commenters note that its release posture appears to have shifted from earlier hints that it would be open sourced.

hackernews · simon_weber · Sep 10, 15:43 · [Discussion](https://news.ycombinator.com/item?id=49645686)

**Background**: PlanetScale is a relational database platform known for its serverless MySQL offering built on the Vitess sharding system, and it has more recently expanded into Postgres. Sharding is a database architecture pattern in which a large dataset is split into smaller pieces called shards that are distributed across multiple machines, allowing a system to scale beyond what a single database node can handle. Doing this manually is notoriously difficult, which is why managed sharding products are valuable to teams running large Postgres deployments.

<details><summary>References</summary>
<ul>
<li><a href="https://planetscale.com/docs/neki">Neki - PlanetScale</a></li>
<li><a href="https://planetscale.com/docs/postgres/sharding">Horizontal sharding for Postgres - PlanetScale</a></li>
<li><a href="https://aws.amazon.com/what-is/database-sharding/">What is Sharding? - Database Sharding Explained - AWS</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (155 points, 62 comments) was largely meta-critical rather than technical. Commenters complained that the launch post never says what Neki is, accused the CEO of criticizing Supabase's open-source multigres while shipping a closed-source rival, and repeatedly asked whether Neki will be open sourced; some also criticized the CEO's tone.

**Tags**: `#databases`, `#sharding`, `#PlanetScale`, `#open-source`, `#distributed-systems`

---

<a id="item-18"></a>
## [.blend URL Viewer: Preview Blender Files in the Browser](https://simonwillison.net/2026/Sep/9/blender-viewer/) ⭐️ 6.0/10

Simon Willison released a ".blend URL Viewer" web tool that renders Blender .blend files directly in the browser from a pasted CORS-accessible URL or GitHub link, and paired the release with an experiment in which ChatGPT Images 2.5 generated a Pluribus-themed Fabergé egg image and GPT-6 Astra in Codex turned it into a Blender model in 17 minutes 51 seconds. The tool lowers the barrier for sharing 3D assets by turning a .blend file into something anyone can open with a URL, with no Blender installation required, while the accompanying experiment shows how far agentic LLM workflows have come in producing usable 3D content from a single text prompt and an image. Blender 5.x files are the best-supported target, and the viewer renders mesh geometry with approximate materials, lighting and saved camera positions plus orbit controls, wireframe mode and a fit button, but it omits unapplied modifiers and approximates text; GitHub URLs are resolved through jsDelivr, and the demo Pluribus egg model weighs 7.2 MB with 387 meshes, 783,764 vertices, 1,446,560 triangles and 17 materials.

rss · Simon Willison · Sep 9, 23:58

**Background**: .blend is Blender's native project file format, which normally requires the desktop application to open, so browser-based viewers rely on WebGL-style rendering to display geometry without the software. GPT-6 Astra is OpenAI's large language model released on 3 September 2026, and ChatGPT Images 2.5 is the image-generation upgrade OpenAI shipped on 8 September 2026. Willison's workflow also relies on an agent "skill" file, a reusable instruction document that tells the coding agent how to drive Blender locally.

<details><summary>References</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Sep/9/blender-viewer/">Tool: .blend URL Viewer</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra - Wikipedia</a></li>
<li><a href="https://9to5mac.com/2026/09/08/openai-releases-chatgpt-images-2-5-with-sharper-details-and-more-precise-editing/">OpenAI releases ChatGPT Images 2.5 with ‘sharper ... - 9to5Mac</a></li>

</ul>
</details>

**Tags**: `#Blender`, `#3D modeling`, `#AI image generation`, `#web tools`, `#Simon Willison`

---

<a id="item-19"></a>
## [348M model trained on 22.7B tokens solves 14-digit arithmetic by showing work](https://www.reddit.com/r/MachineLearning/comments/1wc7hmu/i_trained_a_348m_model_trained_from_scratch_on/) ⭐️ 6.0/10

A hobbyist released their fifth from-scratch small language model: 348M parameters trained on 22.7B tokens, then fine-tuned into a math model that solves arithmetic by explicitly emitting column-by-column worked steps (carries, borrow chains, partial products). It reports a 99.4% average across the nine GPT-3 arithmetic sub-tasks, hitting 100% on 5-digit addition and 2-digit multiplication where GPT-3 175B few-shot direct answering scores 9.3% and 29.2% respectively. It is a striking data point that a 348M-parameter model with roughly 1/500th the parameters of GPT-3 175B can dominate it on raw arithmetic — not through scale, but by having worked steps trained into it rather than relying on few-shot prompting at inference time. This strengthens the case that reasoning traces (chain-of-thought) are load-bearing behavior for small models, and that arithmetic skill is separable from broader word-problem reasoning. The reported ceiling on clean addition rose from 8 to 14 digits simply by expanding the place-value name list from 6 entries (`ones` … `hundred-thousands`) to 19; the model had already generalized to `millions` and `ten-millions`, which appear in zero training examples, and at 9 digits it silently dropped a column rather than making an arithmetic error. Caveats: greedy decoding is required (sampling corrupts the column routine mid-chain), there is no division at all, 4×4 multiplication is a hard wall, word problems are weak (GSM8K 4%, ASDiv 16.5%) because the failure mode is operation selection rather than computation, and the author flags that the arithmetic harness orders subtraction operands.

reddit · r/MachineLearning · /u/nkthebass · Sep 10, 03:28

**Background**: The GPT-3 arithmetic benchmark suite consists of nine sub-tasks (addition, subtraction and multiplication at various digit widths) in which a model is given a few examples and must output the answer directly, without a calculator or intermediate steps; large models notoriously fall off a cliff past 3–4 digits in this setting. Chain-of-thought prompting, popularized in 2022, instead encourages a model to generate intermediate reasoning steps before answering, which markedly improves multi-step reasoning. This project takes that idea one step further by training the step-by-step column arithmetic directly into a small model rather than eliciting it with a prompt.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chain-of-thought_prompting">Chain-of-thought prompting</a></li>
<li><a href="https://www.promptingguide.ai/techniques/cot">Chain-of-Thought Prompting | Prompt Engineering Guide</a></li>
<li><a href="https://llm-stats.com/benchmarks">AI & LLM Benchmarks 2026: Rankings, Scores & Results</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#arithmetic reasoning`, `#small language models`, `#chain-of-thought`, `#benchmarks`

---

<a id="item-20"></a>
## [ChatGPT voice mode adds GPT-5.6 Sol and GPT-6 Astra selection](https://x.com/athyuttamre/status/2097761052939125132) ⭐️ 6.0/10

A Telegram post relaying a message from OpenAI's Atty Eleti reports that ChatGPT's voice mode now lets users manually choose between the GPT-5.6 Sol and GPT-6 Astra models, along with a configurable effort level. According to the relay, Pro users get access to both options, and voice will invoke the selected model whenever it needs to search or reason. Voice mode was previously an opaque, single-model experience, so exposing model choice and effort control brings the same knobs users already have in text chat into the hands-free interface. It also signals that OpenAI is willing to route Pro-tier voice traffic to its newest and most expensive frontier models, which shapes expectations for how quickly new models reach every surface. The announcement is a brief second-hand relay with no benchmarks, latency figures, availability dates, or rollout regions, so the practical difference between the two models in voice is not quantified. It describes tiered access to existing models rather than a new model release, and in OpenAI's API the underlying reasoning effort parameter takes model-dependent values spanning none, minimal, low, medium, high, xhigh, and max.

telegram · zaihuapd · Sep 10, 00:20

**Background**: GPT-5.6 Sol is the most capable variant of OpenAI's GPT-5.6 family, which also includes Luna and Terra, and was publicly released on July 9, 2026 after a limited preview for trusted partners. GPT-6 Astra, released on September 3, 2026, is OpenAI's next-generation flagship and is described as state-of-the-art in computer use, browsing, software engineering, cybersecurity, science, and professional work. Reasoning effort is a setting that tells a model how much internal deliberation to spend on a task, trading latency and cost against answer quality; capability tiers like Sol versus Astra determine which model performs the work at all.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6_Sol">GPT-5.6 Sol</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra - Wikipedia</a></li>
<li><a href="https://developers.openai.com/api/docs/guides/reasoning">Reasoning models | OpenAI API</a></li>

</ul>
</details>

**Tags**: `#ChatGPT`, `#OpenAI`, `#语音模式`, `#模型选择`, `#AI产品更新`

---

<a id="item-21"></a>
## [HBM Shortage Drives 20-50% Price Hikes on Chinese AI Chips](https://www.reuters.com/world/asia-pacific/chinas-ai-chipmakers-raise-prices-high-bandwidth-memory-shortage-bites-2026-09-10/) ⭐️ 6.0/10

Chinese AI chipmakers including Huawei and Cambricon have begun raising prices because of a global shortage of high-bandwidth memory (HBM). Huawei's Ascend 950DT is reportedly quoted 20%-50% higher than two months ago, with some older chips up about 30%, while Cambricon's next-generation Siyuan 690 is expected to rise roughly 20%-30%. The price increases show that memory, not compute logic, has become the binding constraint on China's domestic AI expansion, raising the cost of building training and inference clusters. It also highlights how US export restrictions amplify the squeeze, since Chinese firms cannot freely buy HBM from SK Hynix, Samsung or Micron and must fall back on less mature domestic alternatives. HBM is 3D-stacked DRAM that supplies the bandwidth AI accelerators need to keep their compute units fed. Notably, Huawei's Ascend 950DT is reported to rely on 144 GB of Huawei's own in-house HBM design delivering roughly 4 TB/s of bandwidth, a specification that depends heavily on domestic memory yield and capacity.

telegram · zaihuapd · Sep 10, 09:29

**Background**: High Bandwidth Memory (HBM) is an advanced memory interface built by stacking multiple DRAM dies vertically and connecting them through silicon vias, originally developed by Samsung, AMD and SK Hynix. It exists because conventional memory bandwidth cannot keep up with the data appetite of AI accelerators such as GPUs and NPUs. HBM is supplied by only three firms — SK Hynix, Samsung and Micron — making it one of the most concentrated links in the AI supply chain. China's AI chip designers, including Huawei with its Ascend line and Cambricon with its Siyuan accelerators, are therefore exposed to both global HBM demand from Nvidia and the US export controls that limit their access to leading-edge memory.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://www.techpowerup.com/forums/threads/huawei-prepares-160-000-ascend-950dt-accelerators-for-deepseek-data-center.352416/">Huawei Prepares 160,000 Ascend 950 DT ... | TechPowerUp Forums</a></li>
<li><a href="https://www.techradar.com/pro/could-cambricon-create-a-deepseek-moment-in-ai-hardware-the-rise-of-chinas-answer-to-nvidia-has-been-nothing-short-of-meteoric-but-is-it-too-good-to-be-true">Cambricon’s Siyuan 690 is designed to rival Nvidia’s H100 but ...</a></li>

</ul>
</details>

**Tags**: `#HBM`, `#AI chips`, `#semiconductor supply chain`, `#China tech`, `#Huawei Ascend`

---