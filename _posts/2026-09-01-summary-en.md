---
layout: default
title: "Horizon Summary: 2026-09-01 (EN)"
date: 2026-09-01
lang: en
---

> From 39 items, 25 important content pieces were selected

---

1. [File Shadowing Attack Breaks Claude Code Auto Mode](#item-1) ⭐️ 9.0/10
2. [Google Removes Manifest V2 Extensions Like uBlock Origin from Chrome Web Store](#item-2) ⭐️ 8.0/10
3. [ChatGPT Work Tool Reference Showcases Self-Documenting Playwright Browser Skill](#item-3) ⭐️ 8.0/10
4. [NAT Blamed for Internet Centralization in Provocative Essay](#item-4) ⭐️ 8.0/10
5. [OpenShot 4.0 Launches with AI Object Masking and UI Overhaul](#item-5) ⭐️ 8.0/10
6. [ChatGPT Work Explained: Two Products in One](#item-6) ⭐️ 8.0/10
7. [GNNs on Dynamic Graphs Leak Future Edges; SynthFin-AML Enforces Causal Splits](#item-7) ⭐️ 8.0/10
8. [Claude Shared Links Indexed by Search Engines Leak User Data](#item-8) ⭐️ 8.0/10
9. [Apple caught off guard by AI-driven demand for Mac Mini and Mac Studio](#item-9) ⭐️ 7.0/10
10. [Sliding-window attention beats linear attention on long-context reasoning](#item-10) ⭐️ 7.0/10
11. [OpenClaw Releases Landmark 2.0 Update with 16,000+ Pull Requests](#item-11) ⭐️ 7.0/10
12. [Apple Announces Tim Cook to Step Down as CEO; John Ternus to Succeed in 2026](#item-12) ⭐️ 7.0/10
13. [DeepSeek Releases v4-flash-vision-exp Multimodal Model on API](#item-13) ⭐️ 7.0/10
14. [Chinese AI firms MiniMax, Zhipu post surging revenue yet remain loss-making](#item-14) ⭐️ 7.0/10
15. [EU Designates ChatGPT, Reddit, Roblox as Very Large Services Under DSA](#item-15) ⭐️ 7.0/10
16. [Xiaomi Unveils Xuanjie O3, O100 and D100 Chips for AI and Auto](#item-16) ⭐️ 7.0/10
17. [Walkable ASCII Cyberpunk City Fits in a Single HTML File](#item-17) ⭐️ 6.0/10
18. [Professor's Tips on Cold Emailing about PhD Positions](#item-18) ⭐️ 6.0/10
19. [Entropic Scree: Mutual Information-Based Diagnostic for Messy Tabular Data](#item-19) ⭐️ 6.0/10
20. [OpenAI Codex Tests New Context Window Strategy: Switching Instead of Summarizing](#item-20) ⭐️ 6.0/10
21. [Jensen Huang: AI Drives U.S. Reindustrialization, $400B in Startup Funding](#item-21) ⭐️ 6.0/10
22. [Court Upholds Ruling: iQIYI Must Restore HD Screen Casting for Existing Members](#item-22) ⭐️ 6.0/10
23. [Thailand Launches Free AI Platform with 33 Models, Aiming for 5 Million Users](#item-23) ⭐️ 6.0/10
24. [Wingtech Sues Nexperia Netherlands Under China's Anti-Foreign Sanctions Law](#item-24) ⭐️ 6.0/10
25. [Hanxu Technology Unveils MRAM Inference Roadmap with uHBM and uLPU](#item-25) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [File Shadowing Attack Breaks Claude Code Auto Mode](https://embracethered.com/blog/posts/2026/breaking-claude-code-opus-5-and-automode/) ⭐️ 9.0/10

A security researcher demonstrated a trojan-style attack against Claude Code Opus 5's Auto Mode, using file shadowing to replace a standard Python module in an attacker-controlled directory. The attack exploits the agent's predictable tool usage, such as invoking `python -c`, to silently execute malicious code. This research highlights a significant security flaw in AI agent execution, where trusted tools can be hijacked by files in the working directory. It underscores the need for sandboxing and stronger safeguards in AI coding assistants, affecting developers who rely on autonomous agent modes. The attack relies on file shadowing, where a malicious `struct.py` (or similar) shadows Python's standard library module when code runs inside an attacker-controlled directory. It specifically targets Claude's known behavioral patterns, such as its tendency to use the same tools and phrases, rather than general prompt injection.

hackernews · Recursing · Aug 31, 07:49 · [Discussion](https://news.ycombinator.com/item?id=49506819)

**Background**: Claude Code is Anthropic's agentic coding tool that can understand codebases, edit files, and run commands to help developers ship faster. Auto Mode is a feature that enables more autonomous execution of tasks. File shadowing is a technique where a file in a directory overrides a similarly named module or executable, which the agent may then unknowingly import or execute.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**Discussion**: Commenters observed that the attack exploits Claude's specific tool-use tics, making it a trojan aimed at tricking Claude rather than a classic prompt injection. Some emphasized sandboxing as a key mitigation, sharing anecdotal evidence of unexpected agent behavior. One commenter praised the attack's design but questioned its direct connection to Auto Mode.

**Tags**: `#AI safety`, `#LLM agents`, `#prompt injection`, `#security`, `#Claude Code`

---

<a id="item-2"></a>
## [Google Removes Manifest V2 Extensions Like uBlock Origin from Chrome Web Store](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

Google has removed all remaining Manifest V2 extensions from the Chrome Web Store, including the widely used ad blocker uBlock Origin. As a result, these extensions can no longer be newly installed, and existing installations will not receive updates. This move affects millions of users who rely on Manifest V2-based ad blockers, which are more effective under the older framework. With Google pushing Manifest V3, many users are expected to migrate to browsers like Firefox to preserve ad-blocking capability. Manifest V3 (MV3) prohibits remotely hosted code and introduces restrictions that weaken ad and tracker blocking compared to MV2. The Chrome Web Store removal marks the final stage of Google's MV2 deprecation, which began years earlier with a phased roll-out.

hackernews · twapi · Aug 31, 21:10 · [Discussion](https://news.ycombinator.com/item?id=49514878)

**Background**: A Chrome extension's manifest is a JSON file that defines its name, permissions, and capabilities. Manifest V2 was the long-standing specification, while Manifest V3 is Google's architectural overhaul focused on security, but it cuts off certain APIs and remote code execution that ad blockers used. Google has been depreciating MV2, and the removal from the Web Store is the culmination of that transition.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline">Manifest V2 support timeline | Chrome for Developers</a></li>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3">Extensions / Manifest V3 | Chrome for Developers</a></li>
<li><a href="https://www.theverge.com/2024/5/30/24168057/google-chrome-extension-change-manifest-v3-ad-blockers">Google will roll out Chrome’s new extension spec on June 3rd | The Verge</a></li>

</ul>
</details>

**Discussion**: Commenters overwhelmingly support moving to Firefox, praising uBlock Origin's performance there and criticizing Google's control over the web. Several users say they switched long ago and have experienced few issues, while others express frustration with Chrome's direction and Google's unilateral decisions.

**Tags**: `#Chrome`, `#Manifest V3`, `#uBlock Origin`, `#Firefox`, `#Ad Blocking`

---

<a id="item-3"></a>
## [ChatGPT Work Tool Reference Showcases Self-Documenting Playwright Browser Skill](https://codex-tool-reference.simonw.chatgpt.site/) ⭐️ 8.0/10

A new reference site catalogues ChatGPT Work tools and skills, and its most notable control-browser skill tells the agent to launch Playwright via a Node.js REPL and call nodeRepl.write(await browser.documentation()) at runtime for instructions. This gives ChatGPT Work teams a practical catalog of reusable agent skills, and the self-documenting browser pattern offers a template for reducing hallucinated steps in AI browser automation. It is especially relevant as OpenAI pushes agentic ChatGPT Work features. The control-browser skill is designed as a driver that executes deterministic Playwright code in the user's visible browser rather than an autonomous agent, and browser.documentation() returns complete usage instructions on demand. The reference site is hosted at codex-tool-reference.simonw.chatgpt.site.

hackernews · ijidak · Aug 31, 14:07 · [Discussion](https://news.ycombinator.com/item?id=49510000)

**Background**: ChatGPT Work is OpenAI's agentic offering, powered by GPT-5.6, that helps teams turn goals into finished deliverables by connecting tools and automating tasks. Playwright is Microsoft's browser automation library for testing and scripting browsers, and browser-control skills in this ecosystem typically act as deterministic drivers rather than autonomous agents.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/chatgpt-work/">ChatGPT Work for every team | OpenAI</a></li>
<li><a href="https://learn.chatgpt.com/docs/get-started-with-work">Get started with ChatGPT Work | ChatGPT Learn</a></li>
<li><a href="https://www.skills.sh/anomalyco/browser-control/browser-control">browser - control — anomalyco/ browser - control</a></li>

</ul>
</details>

**Discussion**: In the comments, simonw highlights the control-browser skill as the most interesting, especially its runtime self-documentation; satvikpendem questions how it differs from Codex, while montroser complains the site's sidebar is hard to scroll on regular-sized screens. enraged_camel adds a meta observation that AI-generated websites tend to share a common visual style, reminiscent of the Bootstrap era.

**Tags**: `#chatgpt`, `#ai-tools`, `#browser-automation`, `#playwright`, `#llm-agents`

---

<a id="item-4"></a>
## [NAT Blamed for Internet Centralization in Provocative Essay](https://dreamstation.systems/personal/ntppost.html) ⭐️ 8.0/10

A new essay on dreamstation.systems argues that NAT was one of the earliest drivers of Internet centralization, because it normalized client-server architecture and trained people to see it as natural. The post sparked a lively Hacker News debate, including a comment from Rusty Russell, the Linux NAT implementer. The essay challenges the conventional narrative that centralization is caused mainly by corporate platforms, pointing instead at a foundational networking technology. If correct, it reframes how engineers think about IPv6 adoption, peer-to-peer protocols, and the enduring value of a publicly reachable endpoint. The author suggests that NAT not only made servers harder to run but also mentally trained users to accept a world where devices talk to 'the cloud' rather than to each other. Commenters counter that regular NAT is manageable and arguably protected millions of insecure devices, while Carrier-Grade NAT (CGNAT) is the truly harmful variant.

hackernews · robinpie · Aug 31, 02:23 · [Discussion](https://news.ycombinator.com/item?id=49504905)

**Background**: Network Address Translation (NAT) maps multiple private IP addresses to a single public IP address, allowing many devices to share one public address. It became pervasive because the original IPv4 protocol only provides roughly 4 billion addresses, which is insufficient for the modern Internet. NAT breaks the end-to-end principle of the original Internet design, making it difficult for external peers to initiate connections to devices behind it.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Network_address_translation">Network address translation - Wikipedia</a></li>
<li><a href="https://www.cisco.com/site/us/en/learn/topics/networking/what-is-network-address-translation-nat.html">What Is Network Address Translation (NAT)? - Cisco</a></li>
<li><a href="https://www.geeksforgeeks.org/computer-networks/network-address-translation-nat/">Network Address Translation (NAT) - GeeksforGeeks</a></li>

</ul>
</details>

**Discussion**: Commenters were split: some agreed NAT was an early killer of the open Internet and a UX disaster for self-hosting, while others argued normal NAT is acceptable and CGNAT is the real problem. Rusty Russell admitted that his Linux NAT implementation prioritized squeezing more connections into one IP, unintentionally eroding public endpoints. Another commenter blamed the internet's original design for applying real-world security assumptions to cyberspace.

**Tags**: `#NAT`, `#Internet architecture`, `#centralization`, `#networking`, `#IPv4`

---

<a id="item-5"></a>
## [OpenShot 4.0 Launches with AI Object Masking and UI Overhaul](https://www.openshot.org/blog/2026/08/30/openshot-40-record-edit-color-like-never-before/) ⭐️ 8.0/10

OpenShot 4.0, the latest major release of the open-source video editor, introduces AI-powered object masking using ONNX models and a refreshed user interface. The release underscores the project's continued active development. This release brings advanced AI-assisted editing capabilities to a free, open-source tool, making features like object masking accessible to users who cannot afford premium editors. It also signals that open-source video editors are keeping pace with industry trends toward AI-driven workflows. The AI object masking feature relies on ONNX models and is available via the OpenShot/openshot-onnx repository. The UI update modernizes the editing experience, and the project remains actively maintained with a strong community following.

hackernews · metrofun · Aug 31, 09:59 · [Discussion](https://news.ycombinator.com/item?id=49507822)

**Background**: ONNX (Open Neural Network Exchange) is an open format for representing machine learning models, allowing models trained in different frameworks to run across various hardware. AI-based object masking automatically identifies and isolates objects or people in video frames, a feature increasingly found in commercial editors like Adobe Premiere and VEGAS Pro. OpenShot is a popular free, open-source video editor that has been developed for many years.

<details><summary>References</summary>
<ul>
<li><a href="https://onnx.ai/">ONNX | Home</a></li>
<li><a href="https://helpx.adobe.com/premiere/desktop/add-video-effects/work-with-masks/object-masking.html">Object Masking in Premiere (beta) | Premiere</a></li>
<li><a href="https://www.vegascreativesoftware.com/blog/smart-mask/">Smart Mask in VEGAS Pro│AI Masking and Video Editing Tool</a></li>

</ul>
</details>

**Discussion**: Commenters generally welcomed the release, with praise for the UI improvements and the integration of ONNX-based AI masking. Some users mentioned alternative tools like LosslessCut, Shortcut, Blick, and Shotstack Studio SDK, while one commenter expressed a preference for lossless editing as a default behavior.

**Tags**: `#video editing`, `#open source`, `#release`, `#AI`, `#ONNX`

---

<a id="item-6"></a>
## [ChatGPT Work Explained: Two Products in One](https://simonwillison.net/2026/Aug/30/understanding-chatgpt-work/) ⭐️ 8.0/10

Simon Willison published an expert breakdown of OpenAI's ChatGPT Work, clarifying that it is actually two distinct products: Work Cloud (via chatgpt.com and mobile apps) and Work Local (via the desktop app formerly called Codex). The analysis details exclusive features available only in Work, such as model selection, code execution with internet access, and a persistent filesystem. This matters because ChatGPT Work is widely described as powerful yet confusing, and this breakdown gives developers and power users a concrete map of what it does and when to use it. It helps the AI/software engineering community navigate an important new product from OpenAI and understand its relationship to the existing ChatGPT and Codex ecosystems. Work is available only to paid subscribers at $20/month and above, and its exclusive features include GPT-5.6 Luna/Terra/Sol model selection, a code execution environment with internet access, a headless Chrome browser, a persistent shared filesystem, ChatGPT Sites publishing, and sub-agent sessions. The desktop 'Work Local' variant feels like a less intimidating, re-skinned Codex for non-developers.

rss · Simon Willison · Aug 30, 23:59

**Background**: In July 2026, OpenAI launched ChatGPT Work as an AI agent that can create presentations, spreadsheets, and other documents based on information from connected apps and files. Codex is OpenAI's coding agent available as a CLI, IDE extension, macOS desktop app, and cloud runner; the desktop app has now been folded into the ChatGPT Work offering. The article mentions future model names such as GPT-5.6 Sol, Luna, and Terra, which appear to be the same models available through the OpenAI API.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ChatGPT">ChatGPT - Wikipedia</a></li>
<li><a href="https://goodtransformer.ai/insights/what-is-chatgpt-work/">What is ChatGPT Work, and why did the launch confuse everyone? | Good Transformer</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai / codex : Lightweight coding agent that runs in your...</a></li>

</ul>
</details>

**Tags**: `#ChatGPT`, `#OpenAI`, `#AI tools`, `#Product analysis`, `#Software engineering`

---

<a id="item-7"></a>
## [GNNs on Dynamic Graphs Leak Future Edges; SynthFin-AML Enforces Causal Splits](https://www.reddit.com/r/MachineLearning/comments/1w3imxy/your_gnn_is_probably_just_an_overcomplicated_mlp/) ⭐️ 8.0/10

The authors released SynthFin-AML v10.0, a synthetic graph dataset with 100k nodes and 1.2M edges, engineered with strict 3-snapshot causal splits so models cannot see future edges. In their benchmark, inductive GraphSAGE reached 0.881 PR-AUC versus 0.848 for a tuned LightGBM, on a strict temporal split. This exposes a critical evaluation flaw: many GNN results on dynamic graphs are inflated by temporal leakage, where models 'see' future edges during training. The dataset and benchmark provide a way to enforce causal boundaries, which is essential for fraud detection, financial networks, and reproducible graph research. The 3-snapshot split uses train edges up to Day 7, validation up to Day 8, and test edges up to Day 10, physically bounding the GNN receptive field. To remove tabular leakage, fraud and normal transaction amounts share the same lognormal distribution (μ=8.517, σ=0.8); the benchmark was submitted upstream as PyTorch Geometric PR #10774.

reddit · r/MachineLearning · /u/Glabmayt2075 · Aug 31, 16:21

**Background**: Graph neural networks (GNNs) update node embeddings by aggregating messages from neighbors; if a dynamic graph is converted into a static snapshot, a message-passing step can incorporate edges that occur after the prediction time, leaking future information into training. This temporal leakage is especially problematic in financial transaction networks, where the direction and timing of fund flows define causality. Causal or point-in-time splits prevent the model from using future edges and are promoted by frameworks such as PyTorch Geometric for temporal graphs.

<details><summary>References</summary>
<ul>
<li><a href="https://kumo.ai/pyg/production/temporal-graphs/">Handling Time in Graph Neural Networks | PyG Guide | Kumo.ai</a></li>
<li><a href="https://arxiv.org/pdf/2510.25348">Beyond Leakage and Complexity: Towards Realistic and Efficient...</a></li>
<li><a href="https://github.com/valiyevoktay-cmd/synthfin-aml-">GitHub - valiyevoktay-cmd/ synthfin - aml -: A graph-native Anti-Money...</a></li>

</ul>
</details>

**Tags**: `#GNN`, `#temporal leakage`, `#anti-money laundering`, `#dataset`, `#evaluation`

---

<a id="item-8"></a>
## [Claude Shared Links Indexed by Search Engines Leak User Data](https://t.me/zaihuapd/43511) ⭐️ 8.0/10

Claude's shared conversation feature has a serious privacy flaw: public links lack a noindex tag, so Google and other search engines have indexed them, exposing sensitive user data. Anthropic has not yet fixed the issue, and users are advised to manually delete private shared conversations. This is a major privacy breach affecting Claude users, exposing API keys, crypto wallets, personal records, and confidential materials to anyone via search. It underscores the need for AI platforms to enforce noindex policies on user-shared content by default. The leaked data includes API keys, cryptocurrency wallets, resumes, lawyer consultation records, internal company project materials, and social security numbers. A similar issue affected ChatGPT about a year ago and was quickly fixed, but Anthropic has not yet addressed it.

telegram · zaihuapd · Aug 31, 03:22

**Background**: Claude is a series of large language models and an AI chatbot developed by Anthropic, released in March 2023. In web publishing, the noindex meta tag or X-Robots-Tag header tells search engines not to index a page; without it, public URLs can be crawled and listed in search results if linked or discovered.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI)</a></li>
<li><a href="https://www.techmagnate.com/blog/meta-robots-tag-x-robots-tag-explained/">Meta Robots Tag vs X- Robots -Tag, Key SEO Use Cases & Impact</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#security`, `#Claude`, `#data-leak`, `#AI`

---

<a id="item-9"></a>
## [Apple caught off guard by AI-driven demand for Mac Mini and Mac Studio](https://www.macrumors.com/2026/08/30/apple-unexpected-mac-mini-and-studio-demand/) ⭐️ 7.0/10

According to a new report, Apple was caught off guard by unexpectedly strong demand for its Mac Mini and Mac Studio computers, driven largely by AI workloads. The company underestimated how many developers and researchers would buy these machines for local AI inference and training. This signals that local AI inference is becoming a major driver in the PC market, as users prioritize privacy, speed, and cost control over cloud convenience. It also demonstrates that even large tech companies can misjudge emerging product-market fit, potentially affecting Apple's supply chain and future product direction. The article notes that Apple reportedly lacked an engineering team dedicated to business customers, had no developer relations staff, and had no enterprise AI strategy. The demand spike is attributed to developers and researchers using the machines for local training and inference workloads, including reinforcement learning projects.

hackernews · thm · Aug 31, 12:41 · [Discussion](https://news.ycombinator.com/item?id=49508982)

**Background**: Local AI inference involves running AI models on a user's own device rather than sending data to cloud services, offering advantages in privacy, latency, and ongoing costs. Macs with Apple silicon and large unified memory are particularly suited to this because they can run models like LLMs efficiently without expensive GPUs. However, the most powerful models still require tens of gigabytes of storage and significant compute, meaning not all use cases can be handled locally.

<details><summary>References</summary>
<ul>
<li><a href="https://www.merciaai.com/post/what-is-local-ai-inference-and-why-it-might-change-how-you-use-ai">What Is Local AI Inference ? (Privacy, Speed, Cost) - Mercia AI</a></li>
<li><a href="https://www.fourfoldai.com/post/on-device-ai-explained-how-ai-runs-locally-on-devices-2026-guide">On - Device AI Explained: How AI Runs Locally on Devices (2026 Guide)</a></li>
<li><a href="https://www.linkedin.com/pulse/rise-local-ai-inference-why-2026-year-move-beyond-alexander-chamandy-pdu5e">The Rise of Local AI Inference : Why 2026 Is the Year to Move Beyond...</a></li>

</ul>
</details>

**Discussion**: Commenters were divided: some highlighted that local hardware is invaluable for iterative work like reinforcement learning, avoiding cloud provisioning delays, while others doubted that current consumer hardware can match cheap cloud subscriptions for general use. Critics noted that the AI-driven demand has displaced other uses like home theater PCs and warned that some buyers may be disappointed by model quality issues.

**Tags**: `#Apple`, `#AI hardware`, `#local inference`, `#Mac Studio`, `#developer trends`

---

<a id="item-10"></a>
## [Sliding-window attention beats linear attention on long-context reasoning](https://www.reddit.com/r/MachineLearning/comments/1w3j1vw/slidingwindow_attention_beats_linear_on/) ⭐️ 7.0/10

A new arXiv preprint (2608.28444) by Alexia Jolicoeur-Martineau et al. shows that sliding-window attention with sinks matches or outperforms post-trained linear attention models on long-context reasoning. The authors report 2–10 times higher performance on Needle-in-a-Haystack and BABILong benchmarks. This result challenges the prevailing research direction of post-training linear attention for long-context efficiency, arguing that a simple baseline has been overlooked. It could save substantial compute and prompt a re-evaluation of benchmarks and model designs. The authors emphasize that SWA with sinks needs no post-training, runs fast, and keeps memory usage low. They strongly recommend switching to SWA instead of post-training linear models, noting linear attention may require training from scratch or extensive post-training to match SWA.

reddit · r/MachineLearning · /u/Justgototheeffinmoon · Aug 31, 16:35

**Background**: Sliding-window attention (SWA) reduces Transformer cost from quadratic to linear by letting each token attend only to a fixed-size window of nearby tokens; adding attention sinks preserves early tokens to stabilize generation. Linear attention methods also aim for O(N) complexity but often need post-training or special kernels. BABILong is a long-context reasoning benchmark that tests whether models can reason over facts distributed across very long distractor text.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.28444v1">Sliding - window beats linear attention</a></li>
<li><a href="https://www.abhik.ai/concepts/transformers/sliding-window-attention">Sliding Window Attention | Abhik Sarkar</a></li>
<li><a href="https://arxiv.org/abs/2406.10149">[2406.10149] BABILong : Testing the Limits of LLMs with Long ...</a></li>

</ul>
</details>

**Tags**: `#attention mechanisms`, `#long-context`, `#LLM efficiency`, `#machine learning research`

---

<a id="item-11"></a>
## [OpenClaw Releases Landmark 2.0 Update with 16,000+ Pull Requests](https://openclaw.ai/blog/openclaw-2-accidentally) ⭐️ 7.0/10

OpenClaw released version 2.0 on August 30, its largest update ever, incorporating over 16,000 pull requests from 933 contributors, including 569 first-time participants. The update spans installation, messaging, memory, skills, models, browser, plugins, and security. This major community-driven release demonstrates the rapid growth and strong engagement around OpenClaw's open-source AI agent ecosystem. The simplified installation, rebuilt browser experience, and new shared cloud sessions for multiplayer collaboration make autonomous AI assistants more accessible and practical for broader adoption. The team spent nearly seven weeks without a new release to consolidate the changes, and the 16,000+ pull requests account for about half of all pull requests in the project's history. Specific technical breakdowns of individual features were not provided in the announcement.

telegram · zaihuapd · Aug 31, 04:38

**Background**: OpenClaw is a free and open-source autonomous AI agent that executes tasks via large language models (LLMs), using messaging platforms such as WhatsApp, Telegram, and Discord as its primary user interface. A pull request is a collaboration mechanism on GitHub where proposed code changes are reviewed and discussed before being merged; 16,000 pull requests reflects an exceptionally large community contribution.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenClaw">OpenClaw - Wikipedia</a></li>
<li><a href="https://openclaw.ai/">OpenClaw — Open -Source AI Assistant</a></li>
<li><a href="https://www.hostinger.com/tutorials/what-is-github/">What Is GitHub, and How to Use It?</a></li>

</ul>
</details>

**Tags**: `#OpenClaw`, `#major-release`, `#open-source`, `#community`, `#software-update`

---

<a id="item-12"></a>
## [Apple Announces Tim Cook to Step Down as CEO; John Ternus to Succeed in 2026](https://t.me/zaihuapd/43516) ⭐️ 7.0/10

Apple has announced a leadership transition: Tim Cook will step down as CEO in September 2026 and become executive chairman, while hardware engineering senior vice president John Ternus will take over as CEO. This marks Apple's first CEO transition since Tim Cook succeeded Steve Jobs in 2011, and it will shape the company's product and strategic direction for the next decade. The choice of a hardware executive signals Apple's continued focus on hardware innovation. The board unanimously approved the plan. Current chairman Arthur Levinson will become lead independent director on September 1, 2026, and Ternus will join the board on the same day; Cook will remain CEO through the summer to complete the transition.

telegram · zaihuapd · Aug 31, 10:21

**Background**: Apple is one of the world's most valuable technology companies, known for products such as the iPhone, Mac, and iPad. Tim Cook has served as CEO since 2011, succeeding company co-founder Steve Jobs, and has overseen Apple's growth into a services-heavy business. John Ternus joined Apple in 2001, became vice president of hardware engineering in 2013, and joined the executive team in 2021, overseeing development of iPhone, Mac, iPad, and AirPods.

**Tags**: `#Apple`, `#CEO transition`, `#Tim Cook`, `#John Ternus`, `#tech industry`

---

<a id="item-13"></a>
## [DeepSeek Releases v4-flash-vision-exp Multimodal Model on API](https://t.me/zaihuapd/43518) ⭐️ 7.0/10

DeepSeek has launched deepseek-v4-flash-vision-exp, its first experimental multimodal vision model in the V4 family, now available on the DeepSeek API. The official documentation and pricing have also been updated to reflect the release. This release closes the gap for developers who need image input through the same API endpoints they already use for text, making DeepSeek more competitive in the multimodal AI space. It is particularly significant for AI/ML practitioners who rely on DeepSeek for vision-language tasks. The model is experimental and can be accessed by setting model='deepseek-v4-flash-vision-exp'. Compared with DeepSeek-V4-Flash-0731, it achieves substantial improvements in multimodal agent capabilities while maintaining comparable performance on text-only agent tasks.

telegram · zaihuapd · Aug 31, 11:41

**Background**: DeepSeek-V4-Flash-Vision-Exp builds on the DeepSeek-V4-Flash architecture by incorporating visual modules and undergoing continued training to unlock visual understanding capabilities. It is the first experimental multimodal model in the DeepSeek V4 family, allowing developers to send images directly through the existing API endpoints. The model is positioned as an early experimental release, with pricing and documentation already updated on the official DeepSeek API platform.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp">deepseek -ai/ DeepSeek - V 4 - Flash - Vision - Exp · Hugging Face</a></li>
<li><a href="https://api-docs.deepseek.com/updates/">DeepSeek API Docs</a></li>
<li><a href="https://zenn.dev/neotechpark/articles/ded1c59067e6ed">DeepSeek V 4 - Flash - Vision - Exp : Image Input Finally Hits the API</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#API`, `#AI`, `#Model Release`, `#Vision`

---

<a id="item-14"></a>
## [Chinese AI firms MiniMax, Zhipu post surging revenue yet remain loss-making](https://ir-upload.realxen.net/iis/0100/uploads/iis/2026/12300095-0.PDF) ⭐️ 7.0/10

MiniMax and Zhipu (Z.AI) published their H1 2026 results, showing revenue of RMB 117 million (+283.1% year-over-year) for MiniMax and RMB 954 million (+399.7%) for Zhipu. Both companies remain loss-making, though their net losses narrowed compared with a year earlier. These results highlight how China's leading AI startups are rapidly commercializing via MaaS and API offerings while still investing heavily. The surge in revenue and API business signals growing enterprise adoption of Chinese large language models and intensifying competition in the global AI market. Zhipu's cloud-deployment revenue share rose to 86.5%, while its open-platform and API business revenue grew more than 27 times year-over-year. Its MaaS platform surpassed 7.4 million users (up 144% since early 2026), with paying daily active users up 603%; MiniMax narrowed its net loss by 11% to RMB 358 million.

telegram · zaihuapd · Aug 31, 13:11

**Background**: Model-as-a-Service (MaaS) delivers AI models through cloud-based, serverless APIs with pay-as-you-go pricing, allowing enterprises to integrate AI without managing underlying infrastructure. Chinese AI startups such as MiniMax and Zhipu are increasingly relying on MaaS and API revenue to monetize large language models, but heavy spending on training and deployment keeps them unprofitable. These H1 2026 results illustrate the commercialization trend across China's AI industry.

<details><summary>References</summary>
<ul>
<li><a href="https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-models-as-a-service-maas">What is Model as a Service (MaaS)? - Microsoft Azure</a></li>
<li><a href="https://www.redhat.com/en/topics/ai/what-is-models-as-a-service">What is Model-as-a-Service? - Red Hat</a></li>

</ul>
</details>

**Tags**: `#AI industry`, `#financial results`, `#MiniMax`, `#Zhipu`, `#MaaS`

---

<a id="item-15"></a>
## [EU Designates ChatGPT, Reddit, Roblox as Very Large Services Under DSA](https://www.euronews.com/next/2026/08/31/eu-places-chatgpt-reddit-and-roblox-under-strictest-digital-safety-rules) ⭐️ 7.0/10

On August 31, 2026, the European Commission designated ChatGPT as a Very Large Online Search Engine and Reddit and Roblox as Very Large Online Platforms under the Digital Services Act, because each has over 45 million monthly active users in the EU. All three now face stricter safety and transparency obligations, with a four-month transition period to comply. This expands EU digital regulation to AI-driven services and major community platforms, setting a precedent that AI chatbots with web-search capability can be treated as search engines. It also forces ChatGPT, Reddit, and Roblox to proactively tackle illegal content, child safety, and user well-being, affecting their product design and operations in Europe. The three services have four months to carry out annual systemic risk assessments, undergo independent audits, and share data with regulators and vetted researchers, focusing on illegal content, minor protection, and user mental health. The European Commission will also monitor their compliance, and these DSA obligations come on top of other EU rules such as GDPR and the AI Act where applicable.

telegram · zaihuapd · Aug 31, 14:39

**Background**: The Digital Services Act (DSA) is an EU regulation that sets harmonized rules for online platforms, with additional obligations for Very Large Online Platforms (VLOPs) and Very Large Online Search Engines (VLOSEs) exceeding 45 million monthly users in the EU. Those obligations include systemic risk assessments, transparency reporting, and measures to mitigate risks such as disinformation and harm to minors. ChatGPT was classified as a search engine because its real-time web-access feature lets users retrieve information similarly to traditional search engines. The EU has already designated other major services like Google, Meta, and Amazon under the DSA.

<details><summary>References</summary>
<ul>
<li><a href="https://digital-strategy.ec.europa.eu/en/faqs/digital-services-act-questions-and-answers">Digital Services Act: Questions and Answers | Shaping Europe’s digital...</a></li>
<li><a href="https://www.theverge.com/23845672/eu-digital-services-act-explained">The EU’s Digital Services Act is now in effect... | The Verge</a></li>
<li><a href="https://arxiv.org/pdf/2601.17064">Between search and platform: ChatGPT under the DSA</a></li>

</ul>
</details>

**Tags**: `#DSA`, `#EU regulation`, `#ChatGPT`, `#Reddit`, `#Roblox`

---

<a id="item-16"></a>
## [Xiaomi Unveils Xuanjie O3, O100 and D100 Chips for AI and Auto](https://t.me/zaihuapd/43524) ⭐️ 7.0/10

Xiaomi announced three new Xuanjie chips: the AI flagship SoC Xuanjie O3, the 1.22 TB/s high-bandwidth AI accelerator Xuanjie O100, and the Xuanjie D100, China's first 3nm autonomous-driving AI chip. All three have passed tape-out verification and cover on-device AI compute across Xiaomi's human-vehicle-home ecosystem. This marks Xiaomi's expansion from smartphones into custom silicon for AI acceleration and autonomous driving, strengthening its vertical integration and competitiveness against other mobile and auto chipmakers. The Xuanjie O3's world-first LPDDR6 support and the 3nm D100 also highlight China's rapid progress in advanced semiconductor design despite export controls. The Xuanjie O3 uses a ten-core all-big-core CPU with multi-core benchmark scores exceeding 15,000, and debuts the G2-Ultra NX GPU, claiming 85% higher performance and 64% lower power draw. It is also the world's first mobile processor to support LPDDR6 memory; the O100 accelerator uses a 6nm wafer-level architecture designed for edge-side large models.

telegram · zaihuapd · Aug 31, 15:15

**Background**: Xuanjie is Xiaomi's in-house chip line aimed at powering mobile, automotive, and AI edge devices. The O3's GPU, G2-Ultra NX, is described as a 16-core Arm Mali-G2 Ultra NX with AI upscaling and frame generation capabilities, and its LPDDR6 support aligns with JEDEC's new memory standard that boosts mobile and AI memory performance. The D100 is notable for being China's first 3nm autonomous-driving AI chip, reflecting a broader push in domestic chip design.

<details><summary>References</summary>
<ul>
<li><a href="https://www.jedec.org/news/pressreleases/jedec®-releases-new-lpddr6-standard-enhance-mobile-and-ai-memory-performance">JEDEC® Releases New LPDDR6 Standard to Enhance Mobile and AI Memory Performance | JEDEC</a></li>
<li><a href="https://gadgets.beebom.com/guides/xiaomi-xring-o3-benchmark-specs">Xiaomi Xring O3: Benchmarks and Specs | Beebom Gadgets</a></li>
<li><a href="https://www.aibase.com/news/30572">Xiaomi Releases Xuanjie O100 Chip , With the Highest Edge-side...</a></li>

</ul>
</details>

**Tags**: `#Xiaomi`, `#SoC`, `#AI chip`, `#semiconductor`, `#autonomous driving`

---

<a id="item-17"></a>
## [Walkable ASCII Cyberpunk City Fits in a Single HTML File](https://www.youtube.com/watch?v=3YtygAx_C6A) ⭐️ 6.0/10

A new video showcases a walkable first-person ASCII cyberpunk city contained entirely in one HTML file. The project uses a seeded 2.5D textured DDA raycaster, with characters serving as the texels in a neon-on-black rendering. This highlights the creative potential of browser-based fixed-width character art and raycasting techniques. It could inspire other developers to build retro-styled 3D experiences that run anywhere with just an HTML file. The city is seeded, so the layout is reproducible, and the raycasting engine renders in 2.5D using a DDA algorithm. The video itself demonstrates recent updates including traffic, interiors, elevation, and skyscrapers, though some viewers reported the live version looks different from the video.

hackernews · keithcarolus · Aug 31, 18:21 · [Discussion](https://news.ycombinator.com/item?id=49512975)

**Background**: ASCII art uses characters from the ASCII standard to create images, and when animated or rendered in real time, it can simulate 3D environments. Raycasting is a rendering technique that traces rays from the viewer through a grid to project 3D scenes onto a 2D screen, enabling efficient pseudo-3D effects like those seen in early games such as Wolfenstein 3D. Doing this in a browser lets creators control fonts and layout precisely, and the result can run without any installation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=3YtygAx_C6A">A Walkable ASCII Cyberpunk City in One HTML File - YouTube</a></li>
<li><a href="https://github.com/ludthor/ascii-city">GitHub - ludthor/ ascii - city : Seeded walkable first-person ASCII ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ray_casting">Ray casting - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were generally positive, with one praising the browser as a superior platform for fixed-width character art and another feeling nostalgic for Sonic's Starlight Zone. However, one user reported that the live version did not match the video's visuals, and another questioned whether the GitHub project synced with the videos; one comment flagged the post as a duplicate.

**Tags**: `#ASCII art`, `#creative coding`, `#browser graphics`, `#cyberpunk`, `#HTML`

---

<a id="item-18"></a>
## [Professor's Tips on Cold Emailing about PhD Positions](https://www.reddit.com/r/MachineLearning/comments/1w3bwci/cold_emailing_profs_about_phd_positions_read_this/) ⭐️ 6.0/10

A machine learning professor posted advice on Reddit about common mistakes students make when cold emailing professors about PhD positions, including sending mass emails, listing generic research interests, misrepresenting workshop papers as conference papers, and overusing LLMs for research thinking. This advice is significant for both prospective PhD students and professors, as it reflects growing concerns about AI-generated applications and the importance of targeted, honest communication. Students can improve their chances by following these guidelines, while professors may spend less time filtering unsuitable emails. The professor specifically warns against passing off workshop papers as conference papers, using LLMs to generate research directions, and ignoring instructions on supervisors' websites. Instead, they recommend showing how you could build on the professor's work rather than summarizing it.

reddit · r/MachineLearning · /u/tariban · Aug 31, 12:09

**Tags**: `#PhD applications`, `#cold emailing`, `#machine learning`, `#academic career`, `#advice`

---

<a id="item-19"></a>
## [Entropic Scree: Mutual Information-Based Diagnostic for Messy Tabular Data](https://www.reddit.com/r/MachineLearning/comments/1w3br9c/how_to_assess_if_there_is_a_strong_signal_in_your/) ⭐️ 6.0/10

The Reddit post introduces Entropic Scree, a new diagnostic tool that uses a transformed mutual information metric to estimate signal strength, signal-to-noise ratio, intrinsic rank, and linearity in high-dimensional, real-world tabular data. An R function is already available, with Python and R packages to follow. Standard PCA and variance-based diagnostics often fail on dirty, high-dimensional data because they rely on linear assumptions and distance metrics. By offering a more assumption-light way to measure signal quality, Entropic Scree could help practitioners decide when uncurated data is still usable for predictive modeling, complementing the 'From Garbage to Gold' framework. The method evaluates a transformed mutual information metric instead of linear variance, rank order, or Euclidean distance, and it can produce an exploratory map that identifies decoupled sub-networks of variables. The full technical details are in a preprint (DOI 10.5281/zenodo.22028087), and the R function is currently available on GitHub.

reddit · r/MachineLearning · /u/Chocolate_Milk_Son · Aug 31, 12:02

**Background**: Mutual information measures how much knowing one variable reduces uncertainty about another, capturing nonlinear relationships that correlation cannot. Principal component analysis (PCA), by contrast, assumes the important structure is linear variance, which makes it fragile when data contains errors, outliers, or mixed scales. Entropic Scree builds on the 'From Garbage to Gold' framework, which studies when noisy, uncurated data can still be used to build accurate prediction models. The tool is designed for exploratory data analysis before modeling, giving a quick read on whether a dataset has enough signal to proceed.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/tjleestjohn/Entropic-Scree">GitHub - tjleestjohn/ Entropic - Scree : Overcome the limits of standard...</a></li>
<li><a href="https://arxiv.org/html/2603.12288">From Garbage to Gold : A Data-Architectural Theory of Predictive...</a></li>

</ul>
</details>

**Tags**: `#data diagnostics`, `#mutual information`, `#tabular data`, `#signal-to-noise`, `#PCA`

---

<a id="item-20"></a>
## [OpenAI Codex Tests New Context Window Strategy: Switching Instead of Summarizing](https://github.com/openai/codex/pull/27488) ⭐️ 6.0/10

OpenAI is testing a new context window management approach in Codex that replaces summarization-based compression with switching to a fresh window, using history and notes for continuity. The change appears in PRs #27488, #29743, and #39827, and is still in development. This could reduce token consumption and detail loss in long coding sessions, addressing a key bottleneck for LLM-based agents. If successful, it may influence how other coding assistants handle context limits. Under the new approach, the model can proactively request a new window, and both manual and automatic cleanup follow the new-window flow; no summaries are generated anymore. The accompanying history and notes features let the model retrieve prior content after switching windows, avoiding task interruptions.

telegram · zaihuapd · Aug 31, 00:02

**Background**: An LLM's context window is the maximum amount of text, measured in tokens, the model can process in a single input. Traditional summarization compression condenses the conversation history into a summary, but this consumes tokens and can lose important details. Codex, OpenAI's coding agent, is experimenting with a different strategy: ending the current window and starting a new one, with external history and notes preserving continuity. This approach is part of broader efforts to improve long-context handling in LLM-based tools.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@tahirbalarabe2/what-is-llms-context-window-understanding-and-working-with-the-context-window-641b6d4f811f">What is LLM ’s Context Window ?:Understanding and... | Medium</a></li>
<li><a href="https://www.emergentmind.com/topics/context-compression-techniques">Context Compression Techniques</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Codex`, `#context window`, `#LLM`, `#coding agent`

---

<a id="item-21"></a>
## [Jensen Huang: AI Drives U.S. Reindustrialization, $400B in Startup Funding](https://x.com/JensenHuang/status/2094173025881272408) ⭐️ 6.0/10

Jensen Huang posted on X that AI is bringing manufacturing back to the U.S., driving reindustrialization after decades of outsourcing. He also cited $400 billion in funding for AI startups over the past six months. This statement reflects how a leading AI executive frames AI as an industrial policy driver, linking it to investments in energy grids, chip plants, and data centers. It matters for policymakers, builders, and local communities because it ties AI growth to domestic jobs and infrastructure development. The post says AI-driven demand is spurring investment in aging power grids and sustainable energy, as well as construction and manufacturing jobs in energy, chips, and data centers. No detailed source or methodology for the $400 billion figure was provided in the post.

telegram · zaihuapd · Aug 31, 01:00

**Background**: For decades, the U.S. offshored much of its manufacturing. The rapid growth of AI requires enormous computing infrastructure, including chip factories and data centers, which demand significant electricity. This has spurred calls for new energy generation and grid upgrades. Jensen Huang is CEO of NVIDIA, a leading AI chip maker, so his remarks reflect industry expectations about AI-driven physical infrastructure investment.

**Tags**: `#AI`, `#制造业`, `#投资`, `#NVIDIA`, `#再工业化`

---

<a id="item-22"></a>
## [Court Upholds Ruling: iQIYI Must Restore HD Screen Casting for Existing Members](https://t.me/zaihuapd/43510) ⭐️ 6.0/10

On November 6, the court of second instance upheld the original ruling in the iQIYI screen-casting restriction case. iQIYI must continue providing HD screen casting to existing members during their membership validity and compensate them with 41 days of gold member service. This ruling sets a legal precedent for streaming platform user rights in China, affirming that platforms cannot unilaterally degrade services for existing paying members. It may encourage other affected users to seek similar compensation and push platforms to honor original service promises. The plaintiff, Zhu Yuan, noted that while the judgment applies to his individual case, iQIYI faces all members in similar situations at the same time. He hopes iQIYI will publicly announce equal compensation for all affected members after the judgment takes effect.

telegram · zaihuapd · Aug 31, 02:41

**Background**: Screen casting (投屏) lets users mirror their phone or computer screen onto a larger display, such as a TV, often through dedicated apps (e.g., LetsView, DouWan) or built-in protocols. Streaming platforms like iQIYI had restricted HD casting for some members, prompting a consumer lawsuit. The case highlights tensions between platform cost-cutting and consumer rights in China's digital market.

<details><summary>References</summary>
<ul>
<li><a href="https://letsview.com/screen-mirroring">LetsView | Free Screen Mirroring App</a></li>
<li><a href="https://douwan.tv/">DouWan - Plug and Play Screen Mirroring for Your Phone</a></li>

</ul>
</details>

**Tags**: `#iQIYI`, `#legal ruling`, `#consumer rights`, `#streaming platform`, `#China`

---

<a id="item-23"></a>
## [Thailand Launches Free AI Platform with 33 Models, Aiming for 5 Million Users](https://thethaiger.com/hot-news/technology/thailand-ai-passport-launches-today) ⭐️ 6.0/10

Thailand's Ministry of Digital Economy and Society launched the TH-AI Passport platform on August 31 at 9 a.m., offering free access to 33 AI models from 14 service providers. The government aims to reach 5 million users. This marks a major push by a national government to democratize AI access, potentially accelerating AI literacy and adoption across Thailand. It also sets an example for other emerging economies looking to leverage AI for public benefit. The platform is restricted to Thai citizens aged 15 and older. The 33 models cover image generation, video creation, music production, coding, and website building scenarios.

telegram · zaihuapd · Aug 31, 07:55

**Background**: The Thai government has been promoting the adoption of artificial intelligence as part of its digital economy strategy. Thailand's first Artificial Intelligence Act is currently in draft and open for public consultation. Industry estimates put the country's AI market at around 50 billion baht, with more than 40 billion baht of that relying on foreign technology.

**Tags**: `#AI`, `#Thailand`, `#Government Platform`, `#AI Adoption`, `#Policy`

---

<a id="item-24"></a>
## [Wingtech Sues Nexperia Netherlands Under China's Anti-Foreign Sanctions Law](https://t.me/zaihuapd/43519) ⭐️ 6.0/10

Wingtech Technology has filed a lawsuit against Nexperia Netherlands at the Dongguan Intermediate People's Court in Guangdong Province, and the court has formally accepted the case. Wingtech invokes China's Anti-Foreign Sanctions Law, demanding a ruling that Nexperia's interference is unlawful, restoration of control over core assets, and damages. This is a notable test of whether China's Anti-Foreign Sanctions Law can be used in private civil litigation between a Chinese parent and its foreign subsidiary, potentially setting a precedent for cross-border tech governance. It also highlights rising geopolitical pressure on semiconductor supply chains, as Nexperia's components are critical to the global automotive industry. The lawsuit was filed in Guangdong Province and centers on what Wingtech calls 'improper interference' by Nexperia Netherlands; specific actions are not disclosed. Wingtech's core demands include a judicial declaration of illegality, restoration of control over core assets, and compensation for damages.

telegram · zaihuapd · Aug 31, 12:26

**Background**: Nexperia is a semiconductor manufacturer headquartered in Nijmegen, the Netherlands, producing essential components such as transistors, diodes, and MOSFETs used widely in automotive electronics. China's Anti-Foreign Sanctions Law, passed in June 2021, establishes a legal framework for countermeasures against foreign sanctions and discriminatory measures, though it is primarily designed to be implemented by state authorities. Wingtech Technology is a Chinese listed company with ownership links to Nexperia, making this civil suit an unusual application of the law.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anti-Foreign_Sanctions_Law">Anti-Foreign Sanctions Law</a></li>
<li><a href="https://www.nexperia.com/">Nexperia : Global semiconductor company</a></li>
<li><a href="https://boardor.com/blog/discussing-chips-through-the-nexperia-incident">Discussing Chips through the " Nexperia Incident" - Boardor</a></li>

</ul>
</details>

**Tags**: `#legal dispute`, `#semiconductor`, `#anti-sanctions law`, `#business conflict`, `#tech company`

---

<a id="item-25"></a>
## [Hanxu Technology Unveils MRAM Inference Roadmap with uHBM and uLPU](https://mp.weixin.qq.com/s/adyFanNueXUHKnxr9m64kg) ⭐️ 6.0/10

Hanxu Technology, claiming to be China's first MRAM magnetic-computing company, unveiled its uHBM and uLPU inference architectures. The first-gen uHBM targets 24 TB/s on-chip read bandwidth, and the uLPU aims for over 2,000 tokens/s decode throughput on 4B multimodal models. The roadmap suggests a memory-centric alternative to GPU-based inference, keeping model weights resident in persistent MRAM to avoid repeated weight movement. If realized, it could reduce power and latency for AI inference, especially at the edge and in data centers, and strengthen a domestic Chinese MRAM supply chain. Model weights reside in Persistent MRAM arrays, and matrix-vector operations are completed on the same chip to reduce repeated weight movement. The SpinPU-ED01 validation chip has passed third-party testing and 24-hour stable operation verification, with the roadmap covering chip, 2U tray, and rack products.

telegram · zaihuapd · Aug 31, 13:41

**Background**: MRAM stores data via magnetic states rather than electric charge, offering non-volatility and, when integrated on-chip, the potential for high bandwidth and low latency compared to DRAM. Existing research has explored on-chip MRAM as a replacement for DRAM physical memories to ease bandwidth bottlenecks. Persistent MRAM is also being positioned for CXL memory pools and edge-AI hardware, where model weights and intermediate states can be stored in MRAM.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Magnetoresistive_RAM">Magnetoresistive RAM - Wikipedia</a></li>
<li><a href="https://user.it.uu.se/~erikhage/courses/tic/Papers/Lecture2/Extra:Desikan02.pdf">mram _techrep.dvi</a></li>
<li><a href="https://www.prodigitalweb.com/beginner-guide-to-magnetoresistive-ram-mram/">Beginner Guide To Magnetoresistive RAM ( MRAM )... | ProDigitalWeb</a></li>

</ul>
</details>

**Tags**: `#MRAM`, `#AI Inference`, `#Hardware`, `#uHBM`, `#uLPU`

---