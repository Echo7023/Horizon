---
layout: default
title: "Horizon Summary: 2026-10-04 (EN)"
date: 2026-10-04
lang: en
---

> From 24 items, 8 important content pieces were selected

---

1. [Aleph Alpha Releases Kolibri, a Sovereign Open-Weight German LLM](#item-1) ⭐️ 8.0/10
2. [Report: OpenAI Cancels GPT-6.1 "Astra" Release Over Safety Concerns](#item-2) ⭐️ 8.0/10
3. [Cloudflare Launches OHTTP Gateway for Privacy-Preserving HTTP Requests](#item-3) ⭐️ 7.0/10
4. [Qt 6.12 LTS Released, Adds Official HarmonyOS Support](#item-4) ⭐️ 7.0/10
5. [Google Bans Fake Bylines and AI-Generated Author Headshots in Search Guidelines](#item-5) ⭐️ 7.0/10
6. [Newgrounds Nostalgia: Ruffle Brings Old Flash Games Back to Life](#item-6) ⭐️ 6.0/10
7. [Cambridge paper probes ADHD, autism and complex trauma overlap](#item-7) ⭐️ 6.0/10
8. [ICLR 2027 Compresses Reviewer Scoring to a 1–4 Scale](#item-8) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Aleph Alpha Releases Kolibri, a Sovereign Open-Weight German LLM](https://aleph-alpha.com/en/blog/kolibri-has-landed-a-sovereign-open-weight-model/) ⭐️ 8.0/10

Aleph Alpha released Kolibri, an English-German Mixture-of-Experts language model with 78B total parameters and roughly 3B active parameters per token, published under the Apache 2.0 license with weights available on Hugging Face. The model was trained from scratch on infrastructure in Germany and Finland, supports a context window of up to 1M tokens, and comes with a full technical report, dataset documentation, and abstention training designed to make it say "I don't know" when the answer is not in the provided context. This is a notable European bid for AI sovereignty: a fully open-weight model trained entirely on EU infrastructure gives enterprises and public-sector users an alternative to US and Chinese model providers, with no vendor lock-in and easier alignment with EU AI Act requirements. The exceptional transparency of the accompanying technical report also raises the bar for how open models are documented, and the release triggered a large Hacker News discussion with independent benchmarking. Kolibri's MoE architecture activates only about 3.5-4.4% of its 78B parameters per token, which keeps inference costs far below a dense model of comparable size, and it was trained with abstention data plus Aleph Alpha's Merlin-Arthur protocol to reduce hallucination. Community benchmarks are mixed, however: one commenter reported that Qwen3 27B scored 79.9 versus Kolibri's 70.8 on German tasks in Kolibri's own harness, and questions remain about whether the "sovereign" label holds after Cohere's takeover of Aleph Alpha.

hackernews · bastitx · Oct 3, 09:36 · [Discussion](https://news.ycombinator.com/item?id=49942706)

**Background**: Aleph Alpha is a German AI company that positions its models for "sovereign" and mission-critical use, meaning customers can run them on their own or EU-hosted infrastructure rather than depending on foreign cloud APIs. "Open-weight" means the trained model parameters are downloadable and self-hostable, though not necessarily trained with fully open data or code. Mixture-of-Experts (MoE) is an architecture in which only a small subset of the model's parameters — the "experts" — are used for each token, letting a model have a very large total parameter count while staying cheap to run. Abstention training is a technique that teaches a model to output "I don't know" instead of guessing when the necessary information is missing, which is important for high-stakes enterprise and government deployments.

<details><summary>References</summary>
<ul>
<li><a href="https://aleph-alpha.com/en/blog/kolibri-has-landed-a-sovereign-open-weight-model/">Kolibri Has Landed: A Sovereign Open - Weight Model — Aleph Alpha</a></li>
<li><a href="https://tej.as/blog/aleph-alpha-kolibri">Aleph Alpha Kolibri: How the Sovereign German LLM Works</a></li>
<li><a href="https://elsolitario.org/en/2026/10/03/aleph-alpha-kolibri-german-llm/">Aleph Alpha Kolibri: What It Is and How It Works</a></li>

</ul>
</details>

**Discussion**: Hacker News reaction was warm but critical: many praised the technical report for being so detailed it reads like a tutorial on "how to build your own modern agentic LLM," and one team even offered free hosted access to Kolibri-1 for anyone to try. A member of the training team confirmed it is the first release from a group formed less than a year ago with a strong focus on iteration velocity, while skeptics pointed to Qwen3 beating Kolibri on German benchmarks and questioned whether the "sovereign" claim survives Cohere's acquisition.

**Tags**: `#LLM`, `#open-weight`, `#Aleph Alpha`, `#transparency`, `#benchmarks`

---

<a id="item-2"></a>
## [Report: OpenAI Cancels GPT-6.1 "Astra" Release Over Safety Concerns](https://t.me/zaihuapd/44198) ⭐️ 8.0/10

The Wall Street Journal reported that OpenAI has canceled the release of its next-generation model, referred to as GPT-6.1 "Astra," after researchers found safety problems during internal testing. The model had reportedly been scheduled to arrive in ChatGPT and Codex in October, and the news was relayed by the Telegram aggregator channel 科技圈·茶馆. It is rare for a leading AI lab to shelve an already-developed frontier model over safety concerns, so the decision — if confirmed — could set a precedent for how other labs weigh capability launches against risk. It also lands amid heightened scrutiny of AI governance and comes after a summer of industry reports about AI systems behaving in uncontrolled ways. The report is thin on specifics: it comes from a brief aggregator post citing the WSJ, with no primary confirmation from OpenAI and no technical description of what the safety problem actually was. The naming "GPT-6.1 Astra" is also unusual for OpenAI's model lineup, so the accuracy of the designation remains uncertain.

telegram · zaihuapd · Oct 3, 12:20

**Background**: OpenAI's GPT family powers ChatGPT, its widely used conversational assistant, while Codex is OpenAI's AI coding agent — originally launched in 2021 as a code-focused language model and re-emerged in April 2025 as a Codex CLI agent available via ChatGPT's web app, command line, desktop apps and IDE integrations. Frontier models normally go through internal safety evaluations and staged deployment before reaching users, so a cancellation at that stage would represent a deliberate halt rather than a routine delay. The broader industry has been under pressure to demonstrate that safety review can actually stop a release, not just document it.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(AI_agent)">OpenAI Codex - Wikipedia</a></li>
<li><a href="https://openai.com/codex/">Codex | AI Coding Partner from OpenAI</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI Safety`, `#GPT-6`, `#Model Release`, `#AI Governance`

---

<a id="item-3"></a>
## [Cloudflare Launches OHTTP Gateway for Privacy-Preserving HTTP Requests](https://blog.cloudflare.com/announcing-cloudflare-ohttp-gateway/) ⭐️ 7.0/10

Cloudflare announced an OHTTP (Oblivious HTTP) gateway that lets website owners route visitor requests through Cloudflare's relay infrastructure so that no single party sees both the request content and the visitor's IP address. Instead of every site having to stand up its own relay and gateway pair, Cloudflare is offering the gateway role as an off-the-shelf service that sites can enable. OHTTP is already used by Apple, Google, Meta and Mozilla for telemetry and similar use cases, but it has mostly been reachable only to large engineering organizations; a mainstream CDN offering the gateway lowers the barrier substantially. At the same time, it intensifies the debate over centralization, since a single company operating both a large share of web traffic and a privacy relay reduces the separation of trust that OHTTP depends on. OHTTP splits trust between a relay that sees the client's IP but only encrypted bytes, and a gateway that decrypts the request but is not supposed to learn the client identity; the protocol is specified in RFC 9458, published in January 2024 by authors affiliated with Mozilla and Cloudflare, and the RFC itself notes it is simpler and cheaper than stronger systems like Tor or Prio. A practical caveat raised by observers is whether visitors can know in advance that OHTTP is being used for a given request, and whether site owners can silently toggle it off.

hackernews · est · Oct 3, 03:15 · [Discussion](https://news.ycombinator.com/item?id=49941091)

**Background**: Oblivious HTTP (OHTTP) is an IETF protocol for forwarding encrypted HTTP messages so that an origin server can receive requests without being able to link them to a client or determine that multiple requests came from the same client. It works by having two separate parties handle different parts of each transaction — a relay that knows the IP address but not the content, and a gateway that knows the content but not the IP address. RFC 9458 was published in January 2024, and providers such as Cloudflare and Fastly already run relays that partners including Apple, Google, Meta and Mozilla use for things like software metrics, ad measurement and AI request processing.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Oblivious_HTTP">Oblivious HTTP</a></li>
<li><a href="https://www.rfc-editor.org/info/rfc9458/">RFC 9458: Oblivious HTTP | RFC Editor</a></li>
<li><a href="https://datatracker.ietf.org/wg/ohttp/about/">Oblivious HTTP (ohttp) - Internet Engineering Task Force</a></li>

</ul>
</details>

**Discussion**: Commenters were largely skeptical about centralization: one joked that everything Cloudflare does is exactly what you would expect from a covert intelligence operation, and another said they would rather share their IP with the website they visit than with a handful of big tech companies. Others asked whether visitors can detect or opt out of OHTTP per request, while one developer welcomed the announcement, saying they had wanted this for update checks in their offline desktop transcription software.

**Tags**: `#OHTTP`, `#privacy`, `#Cloudflare`, `#networking`, `#IETF`

---

<a id="item-4"></a>
## [Qt 6.12 LTS Released, Adds Official HarmonyOS Support](https://www.qt.io/blog/qt-6.12-released) ⭐️ 7.0/10

Qt 6.12 LTS was released with a five-year maintenance and support window, and for the first time it officially adds Huawei's HarmonyOS to the Qt LTS supported-platform matrix, giving the platform the same stability commitments, routine maintenance and technical support as other major targets. The release also optimizes WebAssembly start-up and runtime behavior to further reduce Qt Quick's resource footprint. Qt is one of the most widely used cross-platform C++ application frameworks for desktop, mobile and embedded software, so a new long-term-support release sets the baseline that commercial and enterprise projects will standardize on for years. Extending official LTS status to HarmonyOS is a notable ecosystem expansion, opening a supported, maintained path for developers who want to ship Qt-based apps onto Huawei's device ecosystem instead of relying on community ports. The LTS designation matters because Qt's long-term-support releases trade new features for a stable API/ABI and years of maintenance; Qt 5.12 LTS, for comparison, received three years of support, while this release is announced with a five-year window. According to the announcement date given in the item, Qt 6.12 LTS was released on September 30, 2026, and the accompanying note is brief, with little technical depth about the HarmonyOS port itself.

telegram · zaihuapd · Oct 3, 04:52

**Background**: Qt is a cross-platform application development framework, primarily built around C++, that lets developers write one codebase and target Windows, macOS, Linux, Android, iOS and embedded systems; in Qt terminology an LTS (Long Term Support) release is a frozen, enterprise-friendly version that receives bug fixes and security patches for multiple years rather than new features. HarmonyOS is Huawei's in-house operating system for smart devices: its earlier versions were built on OpenHarmony with Linux-kernel compatibility and AOSP-derived code, while HarmonyOS 5 / HarmonyOS NEXT moved to the Hongmeng kernel and removed AOSP code, making native porting work by frameworks such as Qt necessary.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ithome.com/1/009/402.htm">跨平台开发框架 Qt 6.12 LTS 发布，首次将华为 HarmonyOS 加入 LTS ...</a></li>
<li><a href="https://www.qt.io/zh-cn/blog/2018/12/17/qt-5-12-lts-released">Qt 5.12 LTS （ 长 期 支 持 版 本 ）正式发布</a></li>
<li><a href="https://zh.wikipedia.org/wiki/鸿蒙操作系统">鸿蒙 操 作 系 统 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**Tags**: `#Qt`, `#HarmonyOS`, `#Cross-Platform`, `#Framework Release`, `#LTS`

---

<a id="item-5"></a>
## [Google Bans Fake Bylines and AI-Generated Author Headshots in Search Guidelines](https://futurism.com/artificial-intelligence/google-updates-guidelines-fake-bylines-ai-generated-headshots) ⭐️ 7.0/10

Google has added explicit language to its search guidelines banning deceptive author attribution, stating that using AI-generated headshots, fabricated names, or fake credentials to make content appear written by a human expert is a form of deception. Previously the company only encouraged accurate bylines; now it treats fake authorship as a signal of low-quality pages that it will not "prioritize" in search results. This turns an informal best practice into an enforceable quality standard, giving Google a documented basis to demote or remove sites that manufacture fake expert personas, which could reshape SEO tactics for publishers and content platforms that rely on AI-generated output. It also signals that authorship signals such as headshots and bios are now part of Google's spam-fighting arsenal, affecting anyone who publishes under a byline. The guideline states that deceptive authorship undermines trust for both users and automated quality systems, and Google has already acted on it: after Futurism exposed the AI content farm Brown Brothers Media, which bought up struggling news sites and invented reporters, Google suppressed the company in search and news and it stopped publishing. Similar operations were reportedly identified in Canada, Florida, and Rhode Island.

telegram · zaihuapd · Oct 3, 16:31

**Background**: Google's search guidelines and spam policies define what content the company considers high or low quality, and violations can lead to ranking demotion or manual actions against a site. In recent years Google has promoted the idea of E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness), which makes visible, verifiable authorship important for ranking. Meanwhile, cheap generative AI has fueled "content farms" that mass-produce SEO articles under invented bylines, often by reviving dormant news domains to borrow their credibility.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/AI-Generated_Profile_Pictures">AI-Generated Profile Pictures</a></li>
<li><a href="https://kontentferma.com/en/ai-content-farm">AI Content Farm : Content Automation | Kontent Farm</a></li>

</ul>
</details>

**Tags**: `#Google`, `#SEO`, `#AI content`, `#search guidelines`, `#fake bylines`

---

<a id="item-6"></a>
## [Newgrounds Nostalgia: Ruffle Brings Old Flash Games Back to Life](https://www.newgrounds.com/) ⭐️ 6.0/10

A Hacker News thread revisiting Newgrounds.com drew 415 points and 122 comments, with former Flash developers and players sharing memories of the site's early era. Several commenters highlighted that Ruffle, an open-source Flash Player emulator, now makes years-old Newgrounds games and animations playable again in modern browsers. For well over a decade, Newgrounds hosted a huge amount of user-generated games, animations and music that became unplayable when Adobe Flash was discontinued at the end of 2020. Ruffle's progress means a large slice of early web culture is being preserved and revived rather than lost to time, and it gives a new generation of developers and players access to that archive. Ruffle is a Flash Player emulator written in Rust that runs both natively on desktop and in browsers via WebAssembly, including on iOS and Android, and it is also distributed as a Chrome extension. One commenter noted a Flash game they uploaded 15 years ago is now fully playable, while others recalled Newgrounds mechanics like the community voting system that could "blam" a submission off the site.

hackernews · azhenley · Oct 3, 00:55 · [Discussion](https://news.ycombinator.com/item?id=49940394)

**Background**: Newgrounds was founded by Tom Fulp in 1995 and became the first Flash showcase site with an automated, self-serve submission system in 2000, letting community members vote on which games and movies stayed up. It played a central role in 2000s internet culture, spawning memes, musicians and indie game developers. Adobe discontinued Flash Player at the end of 2020, making the vast library of .swf content on sites like Newgrounds unplayable until emulators such as Ruffle emerged.

<details><summary>References</summary>
<ul>
<li><a href="https://ruffle.rs/">Ruffle - Flash Emulator</a></li>
<li><a href="https://en.wikipedia.org/wiki/Newgrounds">Newgrounds - Wikipedia</a></li>
<li><a href="https://www.newgrounds.com/wiki/about-newgrounds/history">Newgrounds Wiki - History</a></li>

</ul>
</details>

**Discussion**: The discussion is warmly nostalgic: former Flash developers recall publishing games and Clock Crew animations on the site, and more than one person notes that Ruffle has finally made their long-lost uploads playable again. A recurring counterpoint is that today's equivalent creative scene on Roblox or Minecraft feels far more commercial than Newgrounds' heyday, though commenters agree it was a uniquely special time to be online.

**Tags**: `#flash`, `#game-development`, `#web-preservation`, `#ruffle`, `#community`

---

<a id="item-7"></a>
## [Cambridge paper probes ADHD, autism and complex trauma overlap](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/30CC4826561366615BFAEC807CDE28A7/S0007125026108046a.pdf/adhd-autism-or-complex-trauma-the-complicated-nature-of-the-question.pdf) ⭐️ 6.0/10

A Cambridge University Press paper titled "ADHD, autism or complex trauma? The complicated nature of the question" examines how these three commonly conflated conditions overlap clinically and how clinicians can tell them apart. The paper was posted to Hacker News, where it drew 170 points and 141 comments, an unusually heavy and personal discussion for an academic PDF. ADHD, autism and complex trauma share symptoms such as executive dysfunction, sensory sensitivity and emotional dysregulation, so misdiagnosis can send people into years of ineffective treatment. Getting the distinction right affects how clinicians choose between trauma-processing therapy and more directive, skills-and-structure-based interventions, which matters to the large number of adults now seeking first diagnoses. A central argument quoted in the discussion is that people most affected by executive dysfunction need therapy that is more directive, specific and accountable, and that processing past trauma and relational approaches alone are not sufficient. The item itself is a paywalled-style Cambridge PDF rather than a summary article, and the Hacker News thread was driven largely by self-identified neurodivergent commenters rather than clinicians.

hackernews · skeptical1884 · Oct 3, 18:08 · [Discussion](https://news.ycombinator.com/item?id=49946403)

**Background**: ADHD (attention-deficit/hyperactivity disorder) is a neurodevelopmental condition marked by inattention, impulsivity and executive dysfunction, while autism is a neurodevelopmental condition affecting social communication, sensory processing and patterns of interest. Complex trauma, sometimes called C-PTSD, arises from prolonged or repeated traumatic experiences, often in childhood, and can produce emotional dysregulation and difficulty with relationships and self-organization. Because all three can look similar from the outside — and frequently co-occur — differential diagnosis is genuinely difficult. "Neurodivergence" is the umbrella term for the idea that these neurological differences are natural variations rather than pure deficits.

**Discussion**: Commenters with lived experience broadly agreed with the paper's point that directive, structure-building therapy helps more than trauma processing alone; one noted years of therapy before finding that structure and mastery over daily tasks produced real progress. Others pushed back on the loose expansion of the word "trauma," while several described the mixture of relief and grief that comes with an adult diagnosis and argued that trauma and neurodivergence are mutually reinforcing, often running together across generations.

**Tags**: `#ADHD`, `#autism`, `#complex-trauma`, `#clinical-psychology`, `#neurodiversity`

---

<a id="item-8"></a>
## [ICLR 2027 Compresses Reviewer Scoring to a 1–4 Scale](https://www.reddit.com/r/MachineLearning/comments/1wwqzxy/iclr_2027_reviewing_scores_d/) ⭐️ 6.0/10

A reviewer posting on r/MachineLearning reported that after receiving three papers to review for ICLR 2027, the recommended-decision scale had been changed to just four options: 1 = Clear rejection, 2 = Weak rejection, 3 = Weak acceptance, 4 = Clear acceptance. The poster noted that the range had apparently been changed "again this year" and called the compression of the scale "very strange" and hard to justify. Review score granularity directly shapes how papers are ranked, how meta-reviewers and area chairs calibrate borderline decisions, and how authors interpret their feedback at one of the three highest-impact machine learning conferences. If the four-point scale is confirmed, it could reduce score clustering in the middle of the distribution, but also strip reviewers of the ability to distinguish between papers that are merely weak versus clearly flawed. The new form asks reviewers to base their recommendation on the submission's overall soundness, significance, clarity, and contribution, without any visible intermediate or confidence-level options in the screenshot quoted by the poster. The change is currently only reported by a single Reddit user, so the official ICLR 2027 review guidelines should be consulted for confirmation, and it remains unclear whether separate technical-quality or confidence fields still exist alongside the four-point recommendation.

reddit · r/MachineLearning · /u/random-tomato · Oct 3, 16:10

**Background**: ICLR (International Conference on Learning Representations) is held annually in late April or early May and, together with NeurIPS and ICML, ranks as one of the three primary conferences of highest impact and reputation in machine learning and AI research. Like other top venues, it relies on volunteer peer reviewers who assign a numeric recommendation to each submission, and the design of that scale matters because scores are used to sort papers, trigger discussion, and inform accept/reject decisions. Conferences periodically revise these scales and category labels — a practice aimed at countering score clustering around middling values and score inflation — which is why the poster's remark that the range changed "again this year" is plausible.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/International_Conference_on_Learning_Representations">International Conference on Learning Representations</a></li>
<li><a href="https://iclr.cc/">ICLR - 2027 Conference</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#peer review`, `#ICLR`, `#academic publishing`, `#conference policy`

---