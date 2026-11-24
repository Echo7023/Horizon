---
layout: default
title: "Horizon Summary: 2026-11-24 (EN)"
date: 2026-11-24
lang: en
---

> From 31 items, 14 important content pieces were selected

---

1. [Anthropic's formal-math repo claims VP ≠ VNP over every field](#item-1) ⭐️ 9.0/10
2. [Nvidia Board Reinstates Jensen Huang as CEO After Two-Week Ouster](#item-2) ⭐️ 8.0/10
3. [Ladybird, the browser engine built from scratch, reaches alpha](#item-3) ⭐️ 8.0/10
4. [Z.ai releases GLM-5.4, its first loop transformer for generalized coding](#item-4) ⭐️ 8.0/10
5. [Meta AI chief Alexandr Wang warns superintelligence is near and control is at risk](#item-5) ⭐️ 8.0/10
6. [Stalwart 1.2.0 becomes a drop-in replacement for Microsoft Exchange](#item-6) ⭐️ 7.0/10
7. [Zed's GPUI Rust UI framework gets its own repository](#item-7) ⭐️ 7.0/10
8. [Arm Forces Shutdown of Popular Third-Party ISA Documentation Mirror](#item-8) ⭐️ 7.0/10
9. [Nospeaker Turns a MacBook Trackpad Into a Speaker Using Its Haptic Motor](#item-9) ⭐️ 7.0/10
10. [Codex2api supply-chain attack ships backdoored releases v3.1.10–v3.1.12](#item-10) ⭐️ 7.0/10
11. [LeCun Accuses Amodei of Hyping AI Risk to Outlaw Open Models](#item-11) ⭐️ 6.0/10
12. [Kagi opens public beta of AI-centric Kagi Mail](#item-12) ⭐️ 6.0/10
13. [ByteDance's Doubao opens invite-only beta of 'Xiaodou' personal AI assistant](#item-13) ⭐️ 6.0/10
14. [45,000 EU businesses urge Brussels to open case against Apple's iPhone browser rules](#item-14) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Anthropic's formal-math repo claims VP ≠ VNP over every field](https://github.com/anthropics/formal-math/tree/main/vp-vnp) ⭐️ 9.0/10

Anthropic's formal-math GitHub repository published a paper, together with a machine-checked formalization, claiming the separation VP ≠ VNP over every field. The algebraic-complexity claim is unrefereed and accompanied by the authors' own admission that they have not analyzed how the argument relates to relativization or algebrization. VP versus VNP is the algebraic analogue of P versus NP, so a claimed separation over every field would be a landmark result in algebraic complexity and would intensify interest in machine-assisted attacks on complexity lower bounds. Because the work comes from Anthropic's formal-math effort, it also signals that frontier AI labs are now aiming automated reasoning at problems long considered holy grails. The paper and formalization live in a specific pinned commit of the anthropics/formal-math repository, and the result remains contested because the authors explicitly state that relativization and algebrization — canonical barriers for separation proofs — have not been analyzed. A commenter independently reran the checks and formalized the statement implications, lending some credibility to the formalization while leaving the mathematical significance open.

hackernews · mikeryan52 · Nov 23, 22:09 · [Discussion](https://news.ycombinator.com/item?id=50620102)

**Background**: In algebraic complexity, VP plays the role of P and VNP the role of NP, but the objects are polynomials and arithmetic circuits rather than Turing machines; VNP is roughly the class of polynomials for which a given monomial's coefficient can be checked efficiently. Complexity theory has identified barriers — relativization, natural proofs, and algebrization — showing that broad families of proof techniques cannot by themselves settle questions like P versus NP, so any claimed separation is expected to explain how it evades them. Formal verification with proof assistants such as Lean turns a proof into a machine-checked object, which raises confidence in correctness but does not by itself establish that the formalized statement is the intended one or that it matters.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Natural_proof">Natural proof - Wikipedia</a></li>
<li><a href="https://math.uchicago.edu/~may/REU2016/REUPapers/Vale.pdf">BARRIERS IN COMPLEXITY THEORY - University of Chicago</a></li>
<li><a href="https://www.anthropic.com/research/formal-verification">LLMs are making formal software verification feasible at a ...</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters treated the result as a possibly partial step in a broader push toward P versus NP, with some joking about an AI-lab arms race and others worried about what such machine-assisted progress means for human mathematicians' careers. The most substantive thread highlighted the paper's own admission that relativization and algebrization are unanalyzed, and one commenter independently reran the checks, yielding a skeptical but verification-oriented discussion rather than hype.

**Tags**: `#complexity-theory`, `#VP vs VNP`, `#P vs NP`, `#formal-verification`, `#AI for mathematics`

---

<a id="item-2"></a>
## [Nvidia Board Reinstates Jensen Huang as CEO After Two-Week Ouster](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 8.0/10

Nvidia's board announced on November 23, 2026 that Jensen Huang has been reinstated as President, CEO, and a member of the board, effective immediately, less than two weeks after he resigned. The board's statement said it received input from senior levels of the United States government and is confident that Huang's reinstatement poses no national security risk. Nvidia is the central supplier of AI accelerators, so a leadership crisis at the company ripples through the entire AI hardware market and the stock's role as a bellwether for the AI trade. The explicit reference to government input also raises uncomfortable questions about how much influence Washington now exerts over the governance of a private chipmaker. The reinstatement came less than two weeks after Huang stepped down following an admission of an extramarital affair with a woman US security agencies reportedly suspected of being a Chinese intelligence asset, and reports say the Department of Justice has indicated it will not prosecute. The board's public justification focused on national security rather than on the substance of the allegations, leaving many governance questions unresolved.

hackernews · jaz · Nov 23, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50611576)

**Background**: Jensen Huang co-founded Nvidia in 1993 and has led it for most of its history, becoming closely identified with the company's rise from graphics cards to the dominant supplier of GPUs used to train AI models. Nvidia's chips are treated as strategically sensitive by both Washington and Beijing, and US export controls on advanced AI chips have made the company a recurring subject of national-security policy debate. In corporate governance terms, a board removing and then rapidly reinstating a founder-CEO within weeks is highly unusual and puts scrutiny on the directors' decision-making process.

<details><summary>References</summary>
<ul>
<li><a href="https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-Board-Reinstates-Jensen-Huang-as-President-CEO-and-Board-Director/default.aspx">NVIDIA Corporation - NVIDIA Board Reinstates Jensen Huang as...</a></li>
<li><a href="https://www.bbc.co.uk/news/live/crd61y5dwqgpt">Jensen Huang reinstated as Nvidia CEO, board says - BBC News</a></li>
<li><a href="https://finance.yahoo.com/markets/stocks/live/nvidia-live-updates-jensen-huang-reinstated-as-ceo-142447561.html">Nvidia live updates: Jensen Huang reinstated as CEO</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters focused on the board's statement that it received US government input, with several calling that the most revealing part of the announcement. Others debated board liability under Delaware's Caremark precedent, expressed surprise at a unanimous 180-degree reversal in under two weeks, and criticized the board's communication and succession planning, while some pushed back on assumptions that Nvidia had committed a crime and argued the media coverage has been confusing.

**Tags**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#national security`, `#AI chips`

---

<a id="item-3"></a>
## [Ladybird, the browser engine built from scratch, reaches alpha](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

The Ladybird project, an independent open-source web browser with its own engine built from the ground up, has officially entered alpha, announced on ladybird.org. The milestone means the browser is now usable enough for broader testing, drawing over 1,500 points and 369 comments on Hacker News. Nearly every mainstream browser today runs on engines descended from a handful of codebases — Blink, WebKit and Gecko — with Blink dominating and closely tied to Google's ad-driven business. A genuinely independent engine backed by a non-profit offers a rare check on that concentration, and alpha status is the first sign it may become viable for real users rather than only developers. Ladybird's engine, LibWeb (rendering) and LibJS (JavaScript), shares no code with Blink, WebKit or Gecko, and the project has replaced several homegrown libraries with production-grade ones such as SQLite and Skia to speed up development. It is a multi-process browser emphasizing process isolation, but the project's own materials still describe it as alpha/pre-alpha software intended primarily for developers and early testers.

hackernews · janvdberg · Nov 23, 16:13 · [Discussion](https://news.ycombinator.com/item?id=50614249)

**Background**: A browser engine is the core component that turns HTML, CSS and JavaScript into the interactive page you see, and it is the single hardest part of a browser to build. Ladybird began as part of Andreas Kling's SerenityOS hobby operating system, growing out of its LibWeb and LibJS components before becoming a standalone project run by the non-profit Ladybird Browser Initiative. Writing an engine from scratch is a multi-year effort because the modern web depends on an enormous surface of standards and quirks that established engines have accumulated over decades.

<details><summary>References</summary>
<ul>
<li><a href="https://ladybird.org/">Ladybird is a truly independent web browser , backed by a non-profit.</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ladybird_(web_browser)">Ladybird (web browser ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Browser_engine">Browser engine - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were largely enthusiastic, with several reporting that tricky sites — overloaded news pages and even Proxmox's NoVNC remote console — rendered correctly, some finding it snappier than Firefox, though one noted slightly jerky scrolling. Others felt nostalgic about the project's earlier SerenityOS hacker spirit after it adopted production-grade libraries, and raised concerns about fingerprinting defenses, granular permissions, and security precautions for early users.

**Tags**: `#Ladybird`, `#web browsers`, `#browser engines`, `#open source`, `#alpha release`

---

<a id="item-4"></a>
## [Z.ai releases GLM-5.4, its first loop transformer for generalized coding](https://z.ai/blog/glm-5.4) ⭐️ 8.0/10

Zhipu AI (Z.ai) released GLM-5.4, described as its first flagship model built on a Loop Transformer architecture, where a single shared block of layers is run for multiple iterations instead of stacking many distinct layers. Z.ai claims this gives reasoning depth comparable to 2T–3T parameter models without adding parameters, and positions the model for "generalized coding" tasks such as generating games, CAD models, GLSL shaders and video through code. It is one of the first major commercial-scale LLM releases to bet on looped/recurrent-depth architectures rather than sheer parameter count, making it a closely watched test of whether weight sharing can keep scaling progress going. Because the model comes from a leading Chinese lab and ships with unusually detailed technical disclosure, it also shifts expectations for transparency among frontier model providers. Z.ai's developer docs state the Model API will only be made available after a security assessment is completed, and early testers report GLM-5.4 was not on OpenRouter or the standard Z.ai API plan, requiring a switch to the Coding Plan whose keys expose the new model. Community reports also flag long "marathon thinking" reasoning traces that sharply increase time-to-completion on even conceptually simple tasks.

hackernews · foohis · Nov 23, 10:06 · [Discussion](https://news.ycombinator.com/item?id=50609685)

**Background**: The Transformer, introduced in the 2017 paper "Attention is All You Need," computes each of its stacked layers exactly once per generated token. A loop transformer instead reuses one shared block of weights across several iterations, which is loosely analogous to a recurrent neural network but loops over architectural depth rather than over input sequence steps. The motivation is partly hardware: inference is heavily memory-bandwidth bound because every layer's weights must be moved from HBM into the chip for each token, so reusing a block that already sits in fast memory can buy extra effective depth at lower cost.

<details><summary>References</summary>
<ul>
<li><a href="https://anyrouter.dev/model/z-ai/glm-5.4">GLM - 5 . 4 · Zhipu AI · pricing & API · AnyRouter</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.4">GLM - 5 . 4 - Overview - Z . AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://magazine.sebastianraschka.com/p/gpt-6-astra-looped-transformers-and">GPT-6 Astra, Looped Transformers , and Hidden Reasoning</a></li>

</ul>
</details>

**Discussion**: Commenters broadly praised Zhipu for publishing concrete technical details, calling the openness a refreshing contrast to the locked-down approach of Western labs, and several agreed looped transformers are an obvious architectural direction. The sharpest criticism was practical rather than architectural: users complained that Chinese models' long "marathon thinking" sessions make them slow and self-doubting on simple tasks, with one suggesting this is how they close the gap on benchmarks, while others detailed access friction through the Coding Plan and shared hands-on SVG generation comparisons against GLM-5.3.

**Tags**: `#llm`, `#transformer-architecture`, `#ai-research`, `#coding-models`, `#zhipu-glm`

---

<a id="item-5"></a>
## [Meta AI chief Alexandr Wang warns superintelligence is near and control is at risk](https://thenextweb.com/news/metas-ai-chief-says-superintelligence-is-arriving-and-control-is-at-risk) ⭐️ 8.0/10

Meta Chief AI Officer and Superintelligence Labs head Alexandr Wang posted a long thread on X arguing that superintelligence is no longer a "someday" issue, pointing to a claimed proof of the Riemann Hypothesis produced by mathematician Levent Alpöge with Anthropic's Claude that was machine-verified by the Lean and Mathlib community on Saturday. Wang said the remaining gap between AI and top human mathematicians is down to concrete knowledge, engineering integration and experimentation, and called for urgent investment in safety, alignment and safeguard research. If the claim holds up, a machine-verified proof of the Riemann Hypothesis — a 166-year-old open problem with major implications for number theory and cryptography — would be one of the strongest public signals yet that AI can do frontier mathematics, not just assist with routine work. Coming from the head of a major lab's superintelligence team, the warning also pushes the AI-safety and control debate from speculative futurism into near-term policy and research prioritization. The result currently has no human-readable version, only a formal proof checked against Lean and Mathlib, so independent mathematicians have not yet reviewed the argument, and the news reaches readers second-hand rather than through a preprint or a public Lean repository. Wang's argument rests on the claim that an AI system capable of unlimited self-improvement, or one a thousand times smarter than humans, would be very hard for humans to keep under control.

telegram · zaihuapd · Nov 23, 12:49

**Background**: Lean is a functional programming language and interactive theorem prover developed at Microsoft Research in 2013, and Mathlib is its large community-maintained library of formalized mathematics; a proof accepted by Lean is checked line by line by a small trusted kernel, which is what "machine-verified" means. The Riemann Hypothesis, formulated by Bernhard Riemann in 1859, states that all non-trivial zeros of the Riemann zeta function lie on the critical line x = 1/2, and its resolution would reshape large parts of number theory. AI alignment is the research field concerned with making AI systems reliably pursue intended goals — split into outer alignment (specifying the goal correctly) and inner alignment (ensuring the system robustly adopts that specification) — while "superalignment" refers specifically to supervising and governing artificial superintelligence.

<details><summary>References</summary>
<ul>
<li><a href="https://hegl.mathi.uni-heidelberg.de/theorem-proving-with-lean/">Theorem Proving with Lean – HEGL</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_alignment">AI alignment - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/superalignment">What is superalignment? - IBM</a></li>

</ul>
</details>

**Tags**: `#超级智能`, `#AI安全`, `#黎曼猜想`, `#Lean/Mathlib`, `#Meta AI`

---

<a id="item-6"></a>
## [Stalwart 1.2.0 becomes a drop-in replacement for Microsoft Exchange](https://stalw.art/blog/microsoft-exchange-replacement/) ⭐️ 7.0/10

Stalwart released version 1.2.0, which the project says makes it a drop-in replacement for Microsoft Exchange — meaning organizations can migrate mailboxes away from Exchange while keeping Outlook clients working rather than ripping out the client side too. The announcement is a milestone for an open-source mail server that previously positioned itself around open protocols like IMAP, JMAP, SMTP, CalDAV, CardDAV and WebDAV. Exchange has been the default enterprise mail and groupware server for over twenty years, and the perceived impossibility of keeping Outlook working without it is one of the strongest forms of vendor lock-in in enterprise IT. Adding Exchange compatibility removes a major practical barrier to de-Microsoftifying mail infrastructure, which matters most for self-hosters, small organizations and public-sector or cost-sensitive deployments. The compatibility claim targets the Exchange/Outlook protocol surface rather than Exchange's full feature set, and Stalwart's core stack remains the open trio of IMAP, JMAP and SMTP plus CalDAV/CardDAV/WebDAV for calendars, contacts and files. Notably, the German GoBD requirement to archive mail immutably for up to ten years is not covered by Stalwart's regular plans or the open-source editions, so regulated businesses still need a separate archival layer.

hackernews · shaunpud · Nov 23, 22:32 · [Discussion](https://news.ycombinator.com/item?id=50620349)

**Background**: Stalwart is an open-source, all-in-one mail and collaboration server that bundles spam and phishing filtering along with mail, calendar, contacts and file sharing in a single service; it is the mail server behind Mozilla's Thundermail offering. Microsoft Exchange is the long-dominant enterprise mail and groupware server, and Outlook clients traditionally talk to it over Microsoft's own MAPI/RPC protocols rather than standard IMAP. That proprietary client-server pairing is why Exchange migrations are notoriously painful: replacing the server usually forces a simultaneous change of clients, calendars and shared mailboxes. A "drop-in replacement" means the server side can be swapped while the existing Outlook-based workflow keeps functioning.

<details><summary>References</summary>
<ul>
<li><a href="https://stalw.art/blog/microsoft-exchange-replacement/">Stalwart is now a drop - in replacement for Microsoft Exchange</a></li>
<li><a href="https://github.com/stalwartlabs/stalwart">GitHub - stalwartlabs/ stalwart : All-in-one Mail & Collaboration server .</a></li>
<li><a href="https://stalw.art/">Stalwart Mail & Collaboration Server</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters raised three main concerns: a German freelancer noted that GoBD-compliant, tamper-proof ten-year mail archiving is missing from Stalwart's plans, another argued that implementing MAPI deepens protocol lock-in and ultimately harms the open email ecosystem rather than undermining Microsoft's, and others worried about long-term sustainability — pointing to past vendor rug-pulls such as CommuniGate's free tier — while acknowledging the tool is a genuine option for low-budget organizations.

**Tags**: `#email`, `#open-source`, `#microsoft-exchange`, `#self-hosting`, `#interoperability`

---

<a id="item-7"></a>
## [Zed's GPUI Rust UI framework gets its own repository](https://github.com/zed-industries/gpui) ⭐️ 7.0/10

Zed's GPUI, the GPU-accelerated Rust UI framework used to build the Zed editor, is being split out of the main Zed codebase into a standalone repository at zed-industries/gpui. The move makes the framework directly accessible and trackable outside the editor repository. Extracting GPUI into its own repo lowers the barrier for Rust developers to adopt it as a general-purpose desktop UI toolkit and could grow an ecosystem of third-party components such as gpui-kit. It also gives the Rust GUI community a more direct alternative to compare with established options like egui and iced. GPUI describes itself as a hybrid immediate and retained mode, GPU-accelerated UI framework for Rust, and it is still pre-1.0 and under active development alongside Zed. The standalone repository does not by itself signal API stability, so early adopters should expect changes.

hackernews · EvilGoose · Nov 23, 20:52 · [Discussion](https://news.ycombinator.com/item?id=50619103)

**Background**: GPUI is Zed Industries' UI engine, originally developed inside the Zed code editor repository, so using it independently previously meant depending on or extracting code from the editor project. Rust's GUI landscape includes egui, an immediate-mode library, and iced, a cross-platform GUI library inspired by Elm, each with different programming models. GPUI's split into a standalone repo is meant to make it a reusable framework rather than an internal Zed component.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/zed-industries/zed/blob/main/crates/gpui/README.md">zed /crates/ gpui /README.md at main · zed -industries/ zed · GitHub</a></li>
<li><a href="https://iced.rs/">iced - A cross-platform GUI library for Rust</a></li>
<li><a href="https://rodneylab.com/trying-egui/">Trying egui : building a Cistercian Clock with Rust GUI | Rodney Lab</a></li>

</ul>
</details>

**Discussion**: HN commenters largely welcomed the standalone repo, with one saying they had wanted to use GPUI but felt awkward that it lived inside the editor repo, and another praising gpui-kit's rich component library while envying it after building an app with iced. Others defended egui against criticism, complained that Rust's hello-world example is verbose and ugly, and debated whether 'GPUI' is a confusing name for a library when the immediate-mode technique predates it.

**Tags**: `#rust`, `#gui`, `#gpui`, `#zed`, `#open-source`

---

<a id="item-8"></a>
## [Arm Forces Shutdown of Popular Third-Party ISA Documentation Mirror](https://arm.jonpalmisc.com/) ⭐️ 7.0/10

Arm has asked the operator of arm.jonpalmisc.com, an independently hosted mirror of Arm's architecture documentation, to discontinue the site by 4 December 2026, citing trademark and IP concerns. The site's maintainer, jonpalmisc, confirmed the request and said he is exploring options such as outside hosting offers, legal counsel, or releasing the site-generator source code without Arm's copyrighted material. The mirror is widely used by systems and embedded developers as a fast, browseable reference for Arm's instruction-set documentation, so its removal makes a routine engineering resource harder to access. The episode also feeds a broader debate over how far hardware vendors can control access to documentation for chips they sell publicly, and it highlights the fragility of community-maintained developer references. The maintainer notes the demand is hard to work around because hosting Arm's documentation at all involves using Arm's trademarks and IP, and community members have suggested alternatives such as mirror hosting elsewhere, legal representation, or publishing the conversion tooling minus Arm content so users can build the site locally. Commenters also observed that similarly converted Arm64 documentation already exists on university-hosted pages, suggesting the site is generated by tooling rather than being a raw copy of Arm's HTML files.

hackernews · tech234a · Nov 23, 19:17 · [Discussion](https://news.ycombinator.com/item?id=50617499)

**Background**: Arm designs the CPU architectures used in most smartphones and a huge share of embedded devices, and its architecture reference manuals describe instruction sets, exception levels, and system registers that low-level developers depend on. Third-party mirrors like this one typically reformat vendor documentation into easily linkable, searchable HTML because official portals can be slow, require registration, or are awkward to navigate. Because such mirrors redistribute vendor text, they sit in a gray zone between fair use, trademark law, and the licensing terms attached to vendor documentation.

**Discussion**: The thread is overwhelmingly critical of Arm: commenters argue the takedown is legal overreach that harms the very developers generating value for Arm, and several question how documenting publicly sold hardware could be restricted at all. Others point to technical counterarguments, noting that Arm's machine-readable architecture specification (MRAS) appears to be distributed under a BSD-style license and that near-identical converted documentation is already hosted elsewhere, while one commenter suggests legal decisions like this should be signed off by someone who understands the business impact.

**Tags**: `#arm`, `#intellectual-property`, `#documentation`, `#legal`, `#open-source`

---

<a id="item-9"></a>
## [Nospeaker Turns a MacBook Trackpad Into a Speaker Using Its Haptic Motor](https://github.com/os6/nospeaker) ⭐️ 7.0/10

Developer Cody Collier has open-sourced nospeaker, a tool that drives the haptic actuator under a MacBook's Force Touch trackpad up to 4,000 times per second, fast enough that the glass vibrates at audible frequencies and can speak text out loud. It feeds text through macOS's built-in speech synthesis, samples two formants plus loudness and pitch every 10 ms, and replays that description on the motor, producing a distinctly robotic voice. The project is a striking demonstration that everyday consumer hardware can be pushed well beyond its designed purpose, turning a silent input surface into a speaker without any additional components. It also highlights how much actuator capability sits behind Apple's private MultitouchSupport framework, since the public haptics API only exposes a handful of fixed taps. Nospeaker bypasses Apple's public haptics API and instead calls the private MultitouchSupport framework, using MTActuationCreateFromDictionary to describe a vibration as a list of sine tones (frequency, strength, length) and MTActuationActuate to play it. Audio is reported audible from roughly 100 Hz to 4 kHz with the clearest output near 1 kHz; it only speaks text (no music or video), requires a Force Touch trackpad, and the author says it has only been verified on an M5 Max MacBook Pro.

hackernews · yakkomajuri · Nov 23, 11:31 · [Discussion](https://news.ycombinator.com/item?id=50610318)

**Background**: Apple's Force Touch trackpad does not physically move when you click; instead a linear actuator inside it taps the surface to simulate the sensation of a button press, a technique Apple markets as Taptic Engine feedback. Apple's public APIs for this, such as Core Haptics on iOS and the basic feedback calls on macOS, only allow a few predefined patterns, so fine-grained control requires undocumented interfaces. Hardware hackers have a long tradition of coaxing sound out of non-audio components — floppy disk drives, piezoelectric PC speakers, and printers — and the sum-of-sines motor driver used here is conceptually similar to driving a tiny speaker voice coil.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/os6/nospeaker">os6/nospeaker: make your macbook's trackpad talk using its haptic ...</a></li>
<li><a href="https://www.macworld.com/article/3294451/trick-turns-macbooks-force-touch-trackpad-into-audio-speaker.html">This insane trick turns the MacBook’s trackpad into a speaker</a></li>
<li><a href="https://www.digitaltrends.com/computing/macbook-trackpads-can-now-talk-in-a-robot-voice-without-the-speakers-thanks-to-a-free-tool/">MacBook trackpads can now talk in a robot voice without the ...</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (292 points, 167 comments) is broadly admiring: one commenter argues that the trackpad's simulated click on an unmoving slab is even more impressive than the sound trick, while others trade nostalgia about Commodore 1541 floppy drives playing music and even video, and about piezo PC speakers playing terrible music. The most technical thread comes from RossBencina, who speculates that Apple's sum-of-sines motor API may exist to avoid burning out the motor, to allow simple feed-forward compensation of actuator dynamics per partial, and to provide a low-bandwidth encoding that travels efficiently over USB/HID — possibly all three at once.

**Tags**: `#hardware-hacking`, `#haptics`, `#macbook`, `#reverse-engineering`, `#apple`

---

<a id="item-10"></a>
## [Codex2api supply-chain attack ships backdoored releases v3.1.10–v3.1.12](https://github.com/WormW/codex2api-incident-2026-11) ⭐️ 7.0/10

The author account of the Codex2api project was compromised, and the attacker bypassed the main branch by pushing tags directly, causing the release pipeline to build backdoored versions v3.1.10 through v3.1.12. Version 3.1.11 stripped out authentication entirely, granting unauthenticated remote command execution, while an injected workflow exfiltrated 16 GitHub Actions secrets and affected at least 21 repositories under the same account. Anyone running Codex2api — a proxy that pools accounts behind a single API base URL — may have exposed their upstream credentials and host to full remote command execution. The incident also shows how a single compromised maintainer account can fan out into dozens of repositories when workflows share secrets across an organization. The attack bypassed normal review by pushing tags rather than commits to main, so the release build produced artifacts that never existed in the reviewed branch. Remediation per the report: immediately stop and roll back to v3.1.9, then rotate the GitHub token, SSH keys, database credentials, and DeepSeek and other related API keys; an independent postmortem dated 2026-11-23 publishes the verified timeline, code analysis, IOCs and detection guidance.

telegram · zaihuapd · Nov 23, 11:21

**Background**: Codex2api is an open-source account-pool proxy that exposes many pooled accounts behind one Codex-compatible API base URL, so its users typically configure it with valuable upstream API keys. In a tag-based release workflow, GitHub Actions builds and publishes artifacts whenever a version tag is pushed, which means write access to tags alone can ship code that never landed on the protected branch. GitHub Actions secrets are encrypted values injected into workflow runs, and once a malicious workflow is present it can read those secrets and send them to an external server in a single run.

<details><summary>References</summary>
<ul>
<li><a href="https://hysenlabs.com/projects/james-6-23-codex2api">codex2api: an account pool behind one API base URL</a></li>
<li><a href="https://docs.github.com/actions/security-guides/using-secrets-in-github-actions">Using secrets in GitHub Actions</a></li>

</ul>
</details>

**Discussion**: Discussion around this item is thin: it is a relay of a warning originally circulated in a chat group, telling users who updated Codex2api that afternoon to check immediately, with the poster explicitly declining responsibility for the risk. No detailed technical debate or counterargument is present in the provided comments.

**Tags**: `#supply-chain-attack`, `#security`, `#github-actions`, `#secrets-exposure`, `#incident-report`

---

<a id="item-11"></a>
## [LeCun Accuses Amodei of Hyping AI Risk to Outlaw Open Models](https://twitter.com/ylecun/status/2124550037912920090) ⭐️ 6.0/10

Yann LeCun tweeted that Dario Amodei has spent his time since GPT-2 "hyping the dangers so that open models would be made illegal and *he* would stay in control," comparing the strategy to the Ottoman Empire's ban on Arabic printing presses. The post drew a large Hacker News thread with 1,319 points and roughly 730 comments debating regulatory capture, open-weight AI, and frontier-lab incentives. The exchange puts a spotlight on a live policy question: whether safety arguments from frontier labs are sincere risk mitigation or a form of regulatory capture that entrenches incumbent players and restricts open-weight competition. How governments treat downloadable models will directly affect researchers, startups, and hobbyists who rely on locally run AI. The seed content is a terse, polemical tweet rather than a technical report, so most of the thread's substance comes from commenters speculating about enforcement mechanisms such as GPU microcode restrictions or registration requirements for private compute. Notably, the accusation is framed as an interpretation of Amodei's motives, and the tweet itself offers no supporting evidence or documentation.

hackernews · MrBuddyCasino · Nov 23, 17:07 · [Discussion](https://news.ycombinator.com/item?id=50615308)

**Background**: Regulatory capture describes a situation in which an agency meant to oversee an industry ends up acting in the interests of the few firms it regulates, often through rules that only large incumbents can afford to comply with. Open-weight models are models whose trained weights are publicly downloadable, letting users run them on their own hardware — unlike closed APIs from frontier labs such as Anthropic and OpenAI, which keep weights private. Frontier labs are the organizations pushing the most advanced, and generally most expensive, model training, and their public safety messaging shapes how regulators draft AI rules.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnet.com/tech/services-and-software/what-are-open-weight-ai-models/">What Are Open - Weight AI Models ? - CNET</a></li>
<li><a href="https://competitivecompliance.co/what-is-regulatory-capture-and-how-bill-gurley-went-all-in-calling-out-brian-armstrong-and-sam-altman/">What is Regulatory Capture and How Bill Gurley Went All-in Calling...</a></li>
<li><a href="https://intelligence.org/2025/06/11/so-you-want-to-work-at-a-frontier-ai-lab/">So You Want to Work at a Frontier AI Lab - Machine Intelligence...</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly skeptical of frontier labs: one quoted the full "new form of..." accusation approvingly, another argued labs are subsidizing usage to build dependence before switching everyone to paid API pricing, which open models would undermine. Others pushed back on the polarization itself, with one commenter noting AI is "not particularly dangerous yet" but likely to become riskier, so neither shutdown nor complacency is warranted; another suggested the compute held by frontier labs, not open models, is what makes AI dangerous.

**Tags**: `#ai-regulation`, `#open-source-models`, `#regulatory-capture`, `#ai-policy`, `#industry-debate`

---

<a id="item-12"></a>
## [Kagi opens public beta of AI-centric Kagi Mail](https://blog.kagi.com/kagi-mail-public-beta) ⭐️ 6.0/10

Kagi Inc., the paid, ad-free search engine, launched a public beta of Kagi Mail, an email service whose headline feature is AI assistance over your inbox. The announcement was accompanied by a Hacker News thread (375 points, 280 comments) that mixed enthusiasm for the Kagi ecosystem with skepticism about the product's direction. Email is the recovery key to nearly every online account, so moving from search into mail is a much deeper bet on user trust than adding another AI feature. For a subscription-only, privacy-positioned company, it tests whether that business model can extend beyond search into a market dominated by Google, Microsoft, and established privacy players like Proton and Fastmail. The launch is a public beta rather than a general release, and the central selling point is letting an AI assistant work over your mail — which, as commenters noted, implies cloud LLM access to message contents. Critics also point out that a niche provider must be dependable for account recovery and long-term retention, a far higher bar than for a search engine.

hackernews · rdmuser · Nov 23, 17:17 · [Discussion](https://news.ycombinator.com/item?id=50615481)

**Background**: Kagi is a subscription-based, ad-free search engine developed by Kagi Inc. of Palo Alto, California; its name comes from the Japanese word 鍵 (kagi), meaning 'key'. It positions itself as an alternative to ad-funded search by charging users directly and promising no tracking, no ad-driven ranking, and no sale of user attention. Kagi Mail extends that same subscription-and-privacy pitch into email, a category where the incumbent providers monetize through advertising or bundled productivity suites.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kagi_(search_engine)">Kagi (search engine)</a></li>
<li><a href="https://kagi.com/html/welcome">Kagi Search - A Premium Search Engine</a></li>

</ul>
</details>

**Discussion**: Commenters were split: several Kagi subscribers said Fastmail is already good enough and that they would never let a cloud LLM read their email, while others worried about feature creep after Kagi Translate's quality declined and became capped as a separate subscription. A recurring concern was brand drift — that Kagi's 'we don't store your data' identity is being quietly revised — plus the view that Kagi and Proton are now expanding into each other's territory instead of improving their core products.

**Tags**: `#email`, `#privacy`, `#kagi`, `#product-launch`, `#ai-features`

---

<a id="item-13"></a>
## [ByteDance's Doubao opens invite-only beta of 'Xiaodou' personal AI assistant](https://mp.weixin.qq.com/s/4JBJszozOuJ5Ve5Ca3lHHA) ⭐️ 6.0/10

Doubao announced that "Xiaodou" (小豆), its standalone AI personal assistant product, has entered public beta. During the beta, access is granted by invitation code and invitees receive a certain amount of free usage quota. This puts ByteDance directly against Meta's Muse in the nascent "personal agent" category, a step beyond chat assistants toward software that actually executes everyday tasks. It also signals ByteDance is willing to ship a separate consumer product rather than folding everything into the main Doubao app. The announcement is a short promotional blurb with no technical detail: no model, platform, pricing, or launch-date information was disclosed, only that the capabilities and experience will gradually roll out in the Doubao App. The invite-only gate limits early scale and suggests the product is still being hardened before general availability.

telegram · zaihuapd · Nov 24, 02:41

**Background**: Doubao is ByteDance's flagship AI assistant app, built on its in-house Seed foundation models. A "personal agent" differs from a plain chatbot in that the user hands over a goal or routine task and the agent carries it out across apps and data — Meta's Muse, for example, organizes files, fills out forms and pulls from Messages, Calendar and Notes on macOS with the user's permission. ByteDance has reportedly been reorganizing its AI teams, with the Flow group overseeing consumer-facing Doubao products, which fits the launch of a dedicated personal-assistant line.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.meta.com/muse/">Muse: Meta's personal AI agent, features & capabilities</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2093268137995256128">Personal Agent 是什么？为什么大厂都抢着做？连 DeepSeek Bot 都来了...</a></li>
<li><a href="https://m.okjike.com/users/14BE6DDB-0744-477B-AD83-CCCEF5EA4302">潘乱的 个 人 主页 - 即刻App</a></li>

</ul>
</details>

**Tags**: `#AI assistants`, `#ByteDance`, `#product launch`, `#AI agents`, `#consumer AI`

---

<a id="item-14"></a>
## [45,000 EU businesses urge Brussels to open case against Apple's iPhone browser rules](https://appleinsider.com/articles/26/11/23/eu-urges-to-challenge-apples-grip-on-iphone-browsers?utm_source=rss) ⭐️ 6.0/10

A coalition of companies and civil-society groups including Mozilla and Shopify has sent a joint letter to the European Commission asking it to open formal proceedings against Apple over its iPhone browser rules, saying the signatories collectively represent roughly 45,000 to 55,000 EU businesses and organizations. The letter is open for additional signatures until December 3, 2026. The letter turns the DMA's browser-engine obligations into a concrete enforcement test: even though Apple now nominally allows rival engines in the EU, the coalition argues that in practice users and developers still cannot escape WebKit. If Brussels acts, it would reshape competition between native apps and the open web on iOS, affecting every browser vendor, web developer and EU business that pays App Store commissions. The coalition estimates that if half of native iOS apps moved to the web, EU businesses would save about €11 billion a year in development costs and €1.3 billion in App Store fees. The document is a lobbying letter rather than a ruling, and Apple has already opened alternative engines in the EU under the DMA, subject to entitlement, security and notarization requirements that critics say remain impractical.

telegram · zaihuapd · Nov 24, 03:02

**Background**: WebKit is the browser engine behind Safari and, historically, behind essentially every browser on iOS and iPadOS: App Store rules required all apps that browse the web to use WebKit and its JavaScript engine, so Firefox ran on Gecko everywhere except iOS. The EU Digital Markets Act designates large platforms such as Apple as "gatekeepers" and requires them to make their markets fairer and more contestable, including by no longer limiting rival browser engines. Apple began allowing alternative engines on iOS in the EU in 2024, but Mozilla has publicly argued that the conditions attached make shipping a Gecko-based Firefox on iOS effectively impossible.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.mozilla.org/en/mozilla/internet-policy/apple-ios-browser-engine-rules/">Why there are still no non-WebKit browsers on iOS</a></li>
<li><a href="https://www.macrumors.com/2026/11/23/coalition-of-eu-businesses-challenges-apple/">Coalition of 55,000 EU Businesses Challenges Apple</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebKit">WebKit - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#antitrust`, `#EU-DMA`, `#Apple`, `#browsers`, `#WebKit`

---