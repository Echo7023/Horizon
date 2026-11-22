---
layout: default
title: "Horizon Summary: 2026-11-23 (EN)"
date: 2026-11-23
lang: en
---

> From 23 items, 7 important content pieces were selected

---

1. [OpenAI Argues Perplexity Tracks Model Intelligence, Sparking Debate](#item-1) ⭐️ 8.0/10
2. [Tesla begins rolling out FSD v15 overseas with Reality View](#item-2) ⭐️ 8.0/10
3. [US Commerce to Finalize Rule Closing China's Remote AI Chip Access](#item-3) ⭐️ 8.0/10
4. [Tim O'Reilly asks why Silicon Valley stopped building for human flourishing](#item-4) ⭐️ 7.0/10
5. [Show HN: Worker755 Game Casts You as an LLM's Subagent](#item-5) ⭐️ 7.0/10
6. [Muru: Graham Dumpleton's AI-Assisted Rust Server for ASGI and WSGI](#item-6) ⭐️ 7.0/10
7. [Google Gemini splits activity controls so users can keep chat history but opt out of model training](#item-7) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [OpenAI Argues Perplexity Tracks Model Intelligence, Sparking Debate](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI published a post titled "Perplexity and Intelligence" arguing that perplexity — equivalently cross-entropy loss on next-token prediction — should be established as a shared metric for comparing model developers and informing safety standards, and it released more transparency into its pretraining progress as a first step. The piece drew a large Hacker News thread (434 points, 297 comments) debating whether the metric still tracks capability in the reinforcement-learning era. If a single, cheap-to-compute number like perplexity reliably tracks model capability, it offers a far simpler benchmark than the increasingly convoluted evaluation suites being spun up, and could give labs and regulators a common yardstick for comparing models and setting safety thresholds. Because it also touches on whether pretraining progress is still the main driver of intelligence, the claim has implications for how the whole field measures and reports model quality. Commenters were struck by how clearly cross-entropy loss still tracks capability despite the shift toward RL-based post-training, and the post's framing suggests perplexity could serve as a cross-lab comparison and safety metric rather than a task-specific benchmark. The main caveat raised is that perplexity is a general next-token metric — small models heavily specialized on domains like math may show strong task performance while having poor general perplexity, so the correlation is only meaningful given matched training data.

hackernews · acossta · Nov 22, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50601525)

**Background**: Perplexity measures how "surprised" a language model is when predicting each next token in a sequence; formally it is the exponentiated cross-entropy loss, ranging from 1 (perfect prediction) up to the vocabulary size (random guessing). It is grounded in information theory, where predicting the next symbol well is equivalent to compressing the data — the classic "prediction is compression" argument. Large language models are trained by minimizing exactly this next-token cross-entropy, so perplexity is the most direct readout of pretraining progress, even though it only partially reflects downstream performance.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li><a href="https://dev.to/trismegistus/compression-is-prediction-and-it-explains-why-llms-actually-work-209e">Compression Is Prediction — and It Explains Why... - DEV Community</a></li>
<li><a href="https://www.comet.com/site/blog/perplexity-for-llm-evaluation/">Perplexity for LLM Evaluation</a></li>

</ul>
</details>

**Discussion**: One commenter supplied a precise definition of perplexity since the article itself omits it, while another expressed surprise that cross-entropy still tracks capability now that RL training dominates, calling it a welcome simple benchmark. A third cited a 2008 paper making the same prediction-equals-compression argument, and a skeptic questioned claims that specific abilities "emerge" at given perplexity levels, pointing to domain-specialized small models as a counterexample; one commenter also asked what happened with GPT-4.5.

**Tags**: `#llm-evaluation`, `#perplexity`, `#compression`, `#openai`, `#machine-learning`

---

<a id="item-2"></a>
## [Tesla begins rolling out FSD v15 overseas with Reality View](https://x.com/Tesla/status/2124222447855743019) ⭐️ 8.0/10

Tesla has started rolling out FSD v15 to overseas markets, claiming up to a 25x improvement in handling safety-critical scenarios. The update also introduces a new "Tesla Reality View" visualization that overlays camera footage and FSD's driving plan on the in-car screen, alongside navigation overlays, gentler turn-signal chimes, and refined speed control near schools and in bad weather. FSD v15 is a major version release for Tesla's flagship driver-assistance software, and the claimed safety-critical gains go to the core of whether supervised autonomy can be trusted in edge cases. The GTA-style Reality View also signals a shift in how Tesla communicates what the neural network is planning, which could shape how drivers and regulators interpret the system's intent. Reality View is described as a real-time generative visualization that streams a view from a virtual camera positioned above the vehicle, replacing multiple separate model signals with a single unified rendering, and it supports fullscreen, map, split-screen, and quiet modes. The 25x safety figure comes from Tesla's own promotional materials and has not been independently verified or backed by published disengagement or collision data.

telegram · zaihuapd · Nov 22, 00:03

**Background**: FSD (Full Self-Driving) is Tesla's advanced driver-assistance package, which despite its name still requires an attentive driver ready to take over. Version numbers like v15 denote successive rewrites or major upgrades of the underlying end-to-end neural network that maps camera input directly to driving behavior. Tesla has increasingly used the in-car display to show what the network perceives and plans, and Reality View is the most ambitious version of that idea so far.

<details><summary>References</summary>
<ul>
<li><a href="https://www.autoinsightreview.com/2026/11/22/tesla-fsd-v15-rollout-reality-view/">Tesla FSD v15 Begins Rolling Out With GTA-Style Reality View</a></li>
<li><a href="https://gizmodo.com/its-like-gta-musk-touts-video-game-like-update-to-tesla-fsd-2000843584">Tesla Adds GTA-Like Update to FSD</a></li>
<li><a href="https://www.zerohedge.com/technology/tesla-rolls-out-gta-style-reality-view-full-self-driving">Tesla Rolls Out "GTA-Style" Reality View For Full... | ZeroHedge</a></li>

</ul>
</details>

**Tags**: `#Tesla`, `#FSD`, `#autonomous driving`, `#vehicle software`, `#UI`

---

<a id="item-3"></a>
## [US Commerce to Finalize Rule Closing China's Remote AI Chip Access](https://t.me/zaihuapd/45289) ⭐️ 8.0/10

The US Commerce Department is finalizing a rule that would stop Chinese AI companies from remotely accessing advanced AI chips hosted in overseas data centers, with publication possible as early as this month. The rule would also extend existing semiconductor export restrictions to seven countries, including Malaysia, Singapore and Thailand, in an effort to shut down both remote-access loopholes and chip smuggling routes. This closes one of the biggest remaining workarounds in the US-China tech rivalry: Chinese labs could previously rent compute abroad instead of importing restricted chips. Extending controls to Southeast Asia could reshape where global AI data-center capacity is built and complicate business for Nvidia, cloud providers and the region's semiconductor supply chains. The rule is being finalized after consultations with other government agencies and covers seven countries beyond the current restrictions, targeting both remote access and physical diversion of chips. Nvidia has reportedly lobbied against closing the remote-access gap, arguing that US AI infrastructure needs to win globally, and the White House has separately asked Congress to legislate on the matter.

telegram · zaihuapd · Nov 22, 04:34

**Background**: Since October 2022, the US Bureau of Industry and Security (BIS) has restricted exports of advanced AI chips and semiconductor manufacturing equipment to China, tightening the rules further in later rounds. Because the controls regulate the physical shipment of hardware, Chinese firms could still rent time on Nvidia GPUs sitting in data centers in Singapore, Malaysia, the Middle East or Europe — a loophole US officials now want to close by treating remote access as a deemed export. Southeast Asia has meanwhile become a key transit and hosting hub, with authorities in the region reporting attempted smuggling of millions of dollars' worth of AI chips.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gibsondunn.com/bis-expands-advanced-computing-controls-to-address-data-center-remote-access-and-third-country-diversion/">BIS Expands Advanced Computing Controls to Address Data Center ...</a></li>
<li><a href="https://hushread.com/stories/us-tightens-ai-chip-export-rules-targeting-chinas-overseas-data-center-access-111746">US Tightens AI Chip Export Rules, Targeting China's Overseas Data ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/05/moonshot-ai-nvidia-chips-europe-china.html">China's Moonshot AI sought Nvidia chip access in Europe amid...</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#export controls`, `#US-China tech`, `#semiconductors`, `#AI policy`

---

<a id="item-4"></a>
## [Tim O'Reilly asks why Silicon Valley stopped building for human flourishing](https://www.oreilly.com/radar/what-happened-to-silicon-valley/) ⭐️ 7.0/10

Tim O'Reilly published an essay on O'Reilly Radar arguing that Silicon Valley has drifted from building products that serve human flourishing toward optimizing for shareholder value, and calling for "mechanism design as reverse game theory" — asking not how to win the current game but what game we ought to be playing. The piece drew a large Hacker News discussion (roughly 323 points and 170 comments) that extended the argument to ZIRP-era incentives and AI-driven cannibalization of core businesses. The essay gives a big-picture frame for a widespread unease in the tech industry: that venture funding, growth metrics and public-market pressure have reshaped what companies build and for whom. Because O'Reilly is a long-time industry chronicler, his framing resonates with engineers and founders who feel the incentive structure — not just individual company culture — is the root problem. The core proposal is mechanism design, the economics subfield that designs rules and institutions to produce a desired outcome and is often described as reverse game theory; O'Reilly uses it to argue that we should first decide what to optimize for and then engineer the rules accordingly. Commenters added a proximate-cause argument that zero interest rate policy (ZIRP) let companies grow to outsized scale and pushed startups toward greenfield gambles rather than competing in known markets.

hackernews · greenyouse · Nov 22, 19:20 · [Discussion](https://news.ycombinator.com/item?id=50602947)

**Background**: Mechanism design is a branch of economics and game theory that starts from a desired outcome and works backwards to construct rules that make self-interested participants produce that outcome, even when the designer doesn't know their private information; Leonid Hurwicz, Eric Maskin and Roger Myerson won the 2007 Nobel Prize for laying its foundations, and it underpins internet systems such as ad auctions and inter-domain routing. ZIRP (zero interest rate policy) describes a central-bank stance of holding nominal short-term rates near 0% to encourage borrowing and investment, a regime that prevailed across much of the 2010s and is widely credited with inflating growth-at-all-costs business models.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanism_design">Mechanism design</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zero_interest-rate_policy">Zero interest - rate policy - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed with O'Reilly but pushed on causes: one argued that governance is futile until we treat the market as an engineered machine whose mechanism designers should be held accountable, and another said the essay's most important idea is buried near the end and deserves far more emphasis. Others blamed ZIRP for letting companies grow to grotesque proportions, warned that AI is now cannibalizing core competencies, and lamented that the finance-minded culture of the 1980s gave way to self-serving "VC influencers".

**Tags**: `#silicon-valley`, `#tech-industry`, `#mechanism-design`, `#venture-capital`, `#economics`

---

<a id="item-5"></a>
## [Show HN: Worker755 Game Casts You as an LLM's Subagent](https://github.com/gulivan/worker755) ⭐️ 7.0/10

A developer released worker755 on GitHub, a command-line game in which the player takes the role of a subagent working under an LLM "director" that hands out tasks and watches what you do. The Show HN post drew 254 points and 59 comments, with players trading stories about typing destructive commands such as `rm -rf` and getting the terse response "The director saw that." The game turns a familiar but abstract concept — a manager agent delegating work to specialized subagents — into something players can directly experience, making agentic orchestration patterns tangible for developers who build or debug such systems. Because the tension comes from being watched and judged by the director, it doubles as a lighthearted probe of how much autonomy and trust we actually want to give AI workers. The project is a text/terminal-based interactive experience rather than a full graphical game, and the player's shell commands are the actual interface for advancing. The submission's score sits at 7.0/10, and at least one commenter noted the lack of support for local LLM backends, which would block offline or homelab use.

hackernews · ivantgam · Nov 22, 13:56 · [Discussion](https://news.ycombinator.com/item?id=50599762)

**Background**: In modern agentic AI systems, a common architecture has a manager or orchestrator LLM break a user request into subtasks and delegate them to narrower subagents, each with its own tools and context, then combine the results. This delegation pattern keeps context windows small and lets parallel subagents return predictable structured output, which is why frameworks such as Spring AI and various orchestration libraries formalize it. worker755 inverts the perspective: instead of playing the orchestrator, you are the subagent receiving instructions and dealing with the consequences of your commands.

<details><summary>References</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/subagent-architecture">Subagent Architecture in AI Agent Harnesses</a></li>
<li><a href="https://spring.io/blog/2026/01/27/spring-ai-agentic-patterns-4-task-subagents">Spring AI Agentic Patterns (Part 4): Subagent Orchestration</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2024/10/agentic-design-patterns/">Top 4 Agentic AI Design Patterns</a></li>

</ul>
</details>

**Discussion**: Commenters generally found the game fun and funny, with several voluntarily testing how far they could push it by deleting files and seeing the director react. A recurring criticism was that the manager spoon-fed exact commands instead of leaving the challenge to the player, and one commenter said they skipped it entirely because it doesn't support local LLMs; another replied with a half-joking "Butlerian Jihad Now."

**Tags**: `#LLM agents`, `#Show HN`, `#AI game`, `#interactive fiction`, `#developer tools`

---

<a id="item-6"></a>
## [Muru: Graham Dumpleton's AI-Assisted Rust Server for ASGI and WSGI](https://simonwillison.net/2026/Nov/21/muru/) ⭐️ 7.0/10

Graham Dumpleton, who created the mod_wsgi Apache module 20 years ago, has launched Muru, a new Rust-based server for running both ASGI and WSGI Python applications in development and production. He is building it with heavy AI assistance and has published roughly 19 detailed posts about the project between November 4 and November 22, 2026. Muru brings two decades of hard-won production experience with Python request serving into a modern Rust implementation, potentially offering a unified replacement for today's split between WSGI servers like Gunicorn/uWSGI and ASGI servers like Uvicorn. Its emphasis on Kubernetes integration, zero-scale, canary releases and tracing suggests it targets containerised production deployments rather than only local development. The published posts cover worker internals, an "import once, fork many" model, HTTPS in development, running WSGI and ASGI side by side, releases without restarts, canaries without a service mesh, Kubernetes-native operation, scaling from worker-reported metrics, scaling to zero, scheduled overlays, and a per-page toolbar with tracing. Dumpleton is explicit that AI does much of the surface work, while judging what is not yet good enough still rests with him.

rss · Simon Willison · Nov 21, 23:56

**Background**: WSGI is the long-standing Python specification that lets synchronous web frameworks such as Flask and older Django deployments talk to a web server, one request at a time per process or thread. ASGI is its asynchronous successor, allowing frameworks like Starlette and FastAPI to handle concurrent connections and protocols such as WebSockets. mod_wsgi was one of the earliest and most widely deployed ways to run Python applications inside Apache, which is why its author's view on how serving Python in production should work carries weight.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Asynchronous_Server_Gateway_Interface">Asynchronous Server Gateway Interface - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/python/difference-between-asgi-and-wsgi-in-django/">Difference Between ASGI and WSGI in Django - GeeksforGeeks</a></li>
<li><a href="https://simonwillison.net/2026/Sep/11/wrapture/">Don't sleep on wrapture | Simon Willison’s Weblog</a></li>

</ul>
</details>

**Tags**: `#python`, `#rust`, `#asgi`, `#wsgi`, `#web-servers`

---

<a id="item-7"></a>
## [Google Gemini splits activity controls so users can keep chat history but opt out of model training](https://blog.google/innovation-and-ai/products/gemini-app/updated-controls/) ⭐️ 6.0/10

Google's Gemini team announced that in the coming weeks it will replace the Gemini app's single "Keep Activity" toggle with two separate settings: one controlling how long chat history is retained, and another that independently decides whether conversations — including text and attachments — may be used to train generative AI models. Users can therefore keep their history saved while refusing training consent, and when the change takes effect both settings will mirror the state of the original toggle. This separates two privacy permissions that were previously bundled together, giving users and privacy-conscious developers a way to keep Gemini's context and history features without contributing their conversations to model improvement. It is a meaningful policy shift for a mainstream AI assistant, though it is an incremental control change rather than a technical breakthrough. If users turn off history, new Gemini conversations are kept for roughly two months and may still be reviewed by human reviewers to respond to users, handle feedback, and protect Google, its users, and the public. Audio and Gemini Live recordings remain, by default, not used to improve Google services and are unaffected by this change.

telegram · zaihuapd · Nov 22, 01:24

**Background**: Google accounts bundle many privacy toggles under activity controls, and Gemini's "Apps Activity" setting previously did double duty: it governed whether chats were stored in your Google Account and whether they could be used for model training. Similar debates have played out across the industry, where vendors including Google Cloud have publicly stated that API prompts and responses are not used to train models, while consumer-facing assistants often opt users in by default. Splitting retention from training consent aligns Gemini with a growing expectation that users control these two decisions separately.

<details><summary>References</summary>
<ul>
<li><a href="https://support.google.com/gemini/answer/13278892?hl=en&co=GENIE.Platform=Android">Manage & delete your activity in Gemini Apps - Android phone...</a></li>
<li><a href="https://ip.net.coffee/ai/news/20261122b.html">Gemini 把「 留 记 录 」和「拿去 训 练 」拆成两个开关 - Net.Coffee</a></li>
<li><a href="https://t.me/AI_News_CN/46069">ChatGPT / AI新闻聚合 – Telegram</a></li>

</ul>
</details>

**Tags**: `#Google Gemini`, `#AI privacy`, `#model training`, `#data retention`, `#product update`

---