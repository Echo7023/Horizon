---
layout: default
title: "Horizon Summary: 2026-11-15 (EN)"
date: 2026-11-15
lang: en
---

> From 29 items, 14 important content pieces were selected

---

1. [Lovable-built apps leak passports and 200K+ messages via Supabase defaults](#item-1) ⭐️ 8.0/10
2. [SpaceX Catches Super Heavy Booster to Close Out Starship Flight 15](#item-2) ⭐️ 8.0/10
3. [PyPI rolls out redesigned project pages with clearer security and provenance signals](#item-3) ⭐️ 7.0/10
4. [All 13 versions of The Secret of Monkey Island compared side by side](#item-4) ⭐️ 7.0/10
5. [EFF Warns Tech Companies Are Redefining Privacy Again](#item-5) ⭐️ 7.0/10
6. [SpaceX to attempt first full recovery of Starship and Super Heavy next month](#item-6) ⭐️ 7.0/10
7. [Cloudflare open-sources Kitesurf, a stateless browser for AI agents](#item-7) ⭐️ 7.0/10
8. [Italy's privacy regulator fines Meta €805 million over photo album access](#item-8) ⭐️ 7.0/10
9. [Documentary Traces KDE's Three-Decade Run as a Volunteer Desktop Project](#item-9) ⭐️ 6.0/10
10. [Reddit User Ranks ICLR 2027 Initial Review Scores by University](#item-10) ⭐️ 6.0/10
11. [Reddit ML thread: short-horizon price forecasting papers should benchmark against market-implied forecasts](#item-11) ⭐️ 6.0/10
12. [China's W5000, billed as the world's largest unmanned cargo aircraft, completes first validation flight](#item-12) ⭐️ 6.0/10
13. [New Zealand Warehouse Workers Protest AI Monitoring of Bathroom Breaks](#item-13) ⭐️ 6.0/10
14. [Google AI Studio designer runs Windows 11 on foldable iPhone via WindowsiOS](#item-14) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Lovable-built apps leak passports and 200K+ messages via Supabase defaults](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

Security research published by a researcher known as neathack (crissyfield.de) shows that apps built with the AI app builder Lovable, which provision Supabase backends with row-level security left off by default, have publicly exposed sensitive data including passport details and more than 200,000 private messages. The data was reachable simply by inspecting network calls in the browser and reusing the public anon key shipped in the client bundle, with no sophisticated hacking required. The disclosure shifts the discussion from a single vendor's bug to an industry-wide default-configuration problem: as AI tools let non-developers ship full-stack apps in minutes, permissive database defaults become a systemic privacy risk affecting large numbers of ordinary users. It also puts pressure on both Supabase and platforms like Lovable to adopt deny-by-default security postures. Supabase tables created via SQL have row-level security turned off by default, so the anon key embedded in the browser bundle can read every row; Supabase says it addressed the default on October 30, but commenters report existing projects may still keep the old permissive behavior. The exploits here required no tooling beyond browser dev tools, and the population of such apps keeps growing daily as more people generate apps from prompts.

hackernews · armcat · Nov 14, 17:43 · [Discussion](https://news.ycombinator.com/item?id=50499017)

**Background**: Lovable is an AI app builder that generates interfaces, databases and logic from plain-language prompts — part of the "vibe coding" trend where users describe what they want instead of writing code. Supabase is a popular open-source Firebase alternative providing a Postgres database and auto-generated APIs; its row-level security (RLS) feature is what restricts which rows a given user's key can access. When RLS is not enabled and policies are not written, the public anon key that Supabase requires in client-side code effectively grants read access to the whole table.

<details><summary>References</summary>
<ul>
<li><a href="https://amabrik.com/blog/supabase-row-level-security/">Supabase Row Level Security (RLS) Explained | Amabrik</a></li>
<li><a href="https://supabase.com/docs/guides/api/securing-your-api">Securing your API | Supabase Docs</a></li>
<li><a href="https://lovable.dev/">App & Website Builder | Build Software in Minutes | Lovable</a></li>

</ul>
</details>

**Discussion**: Commenters largely blamed Supabase, pointing to a GitHub discussion (#4547) where the permissive default was supposedly fixed on October 30 but may still apply to existing projects, and arguing it was a deliberate onboarding tradeoff made years ago. Others framed AI-generated apps as easy, high-volume targets whose users don't understand the risk, and called for deny-by-default databases, least-privilege APIs and automated auth tests so that insecure deployments become hard rather than easy. The author joined the thread, noting the post originally flopped on Hacker News two weeks earlier.

**Tags**: `#security`, `#supabase`, `#AI-generated-code`, `#data-privacy`, `#vibe-coding`

---

<a id="item-2"></a>
## [SpaceX Catches Super Heavy Booster to Close Out Starship Flight 15](https://x.com/i/broadcasts/2brajgZlOKRMka) ⭐️ 8.0/10

SpaceX's live broadcast of Starship Flight 15 ended with the Super Heavy booster being caught in mid-air by the launch tower's robotic arms rather than splashing down in the ocean. The catch capped the test flight and was presented as another step in the company's push toward fully reusable launch hardware. Routinely catching the booster is the key enabler for rapid reuse: it keeps the stage intact, on land, and close to its launch site so it can be inspected and flown again quickly. Each successful catch therefore matters not just for SpaceX's Mars ambitions but for the economics of super heavy-lift launch more broadly. The catch is performed by the launch tower's so-called "chopstick" arms, which must arrest a descending booster carrying on the order of 100 megajoules of kinetic energy within seconds, relying on precise timing and the booster's remaining engines and grid fins. Success depends on the booster being healthy enough at landing, which is why earlier flights had to divert to a water landing instead.

hackernews · ls612 · Nov 14, 21:22 · [Discussion](https://news.ycombinator.com/item?id=50500963)

**Background**: Super Heavy is the reusable first stage of SpaceX's Starship, a super heavy-lift vehicle consisting of the booster plus the Starship upper stage, developed over more than a decade as part of SpaceX's Mars plans. The robotic catch system on the launch tower is nicknamed "Mechazilla"; it first successfully caught a booster on Flight 5 in October 2024, a milestone that made the tower-catch approach a practical alternative to landing legs. Since then SpaceX has been refining the maneuver across subsequent test flights.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SpaceX_Super_Heavy">SpaceX Super Heavy - Wikipedia</a></li>
<li><a href="https://www.universetoday.com/articles/spacexs-mechazilla-catches-starship-booster">SpaceX's Mechazilla Catches a Starship Booster on First Try</a></li>
<li><a href="https://www.linkedin.com/posts/waseem-rehmancpengcmrppmp_spacexs-launch-tower-catching-super-heavy-activity-7436278279784812544-qO2E">SpaceX's Super Heavy Booster Catch Mechanism ... | LinkedIn</a></li>

</ul>
</details>

**Discussion**: Commenters were overwhelmingly enthusiastic, calling the catch "insane" and the dawn of a new era more than a decade in the making, with several saying the engineering feat could inspire millions of young people to study engineering. Others noted lighter touches, such as the "don't panic" message written on the fuselage above an S42 badge, and one joked that the catch was "so precise it was almost boring" — a compliment to how routine the maneuver is starting to look.

**Tags**: `#SpaceX`, `#Starship`, `#aerospace engineering`, `#reusable rockets`, `#engineering milestone`

---

<a id="item-3"></a>
## [PyPI rolls out redesigned project pages with clearer security and provenance signals](https://blog.pypi.org/posts/2026-11-06-ui-updates-complete/) ⭐️ 7.0/10

On November 6, 2026, PyPI completed a redesign of its project pages that adds a dedicated Security tab, per-file provenance attestations, and more prominent warnings about missing, incomplete, or conflicting release metadata. Alongside the interface changes, PyPI expanded its user documentation with a package security guide covering source assessment, provenance checking, integrity verification, and attack reporting. The change puts supply-chain evidence directly in front of users at the moment they decide whether to install a package, making it harder for a compromised or hijacked release to slip through unnoticed. Because PyPI is the default distribution channel for the Python ecosystem, even modest visibility improvements can shift publishing norms toward attestation and Trusted Publishing across thousands of projects. The provenance warnings are designed to flag releases whose metadata is absent or inconsistent with a project's history, which helps catch previously benign projects whose PyPI credentials were stolen — but it does not detect packages that were malicious from the start. Trusted Publishing also still does not support GitHub reusable workflows, a limitation tracked in warehouse issue #11096.

hackernews · rbanffy · Nov 14, 15:40 · [Discussion](https://news.ycombinator.com/item?id=50497892)

**Background**: Provenance attestations are machine-readable, signed records describing where a software artifact came from and how it was built; on PyPI they are typically generated automatically when a package is published through Trusted Publishing from a CI/CD system. Sigstore is the open-source project behind much of this, providing "keyless" signing where a short-lived certificate is tied to an OIDC identity such as a GitHub Actions workflow rather than a long-lived private key. This matters because traditional signing keys are easy to leak or lose, whereas a keyless signature ties a release to the specific pipeline and commit that produced it.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.pypi.org/using-pypi/package-security/provenance/">Checking Provenance (package origin) - PyPI Docs</a></li>
<li><a href="https://www.sigstore.dev/">Home · Sigstore</a></li>
<li><a href="https://daysec.org/pypi-security-tab-provenance-warnings-guide/">Read PyPI’s New Security Signals Before Installing a Release</a></li>

</ul>
</details>

**Discussion**: Commenters broadly welcomed PyPI surfacing provenance, with one user citing Datasette (with provenance) versus dlt (without) as a concrete before-and-after example, and others calling for Sigstore-style keyless signing to spread so that more CI/CD providers support the required OIDC handling. Concerns centered on centralization — one commenter argued the trust model effectively depends on "big cloud" providers and promotes lock-in, which they found un-Pythonic — while another noted the signals catch hijacked but previously benign projects rather than malicious ones from the outset.

**Tags**: `#PyPI`, `#software supply chain security`, `#provenance`, `#Sigstore`, `#Python packaging`

---

<a id="item-4"></a>
## [All 13 versions of The Secret of Monkey Island compared side by side](https://monkeyisland.pages.dev/) ⭐️ 7.0/10

A website at monkeyisland.pages.dev presents a side-by-side visual comparison of all 13 versions of Lucasfilm Games' 1990 adventure classic The Secret of Monkey Island, letting visitors see how the same scenes were rendered across different platforms and graphics modes. The project reached the front page of Hacker News, drawing roughly 440 points and 141 comments. The comparison makes tangible how one game had to be re-authored for a dozen different display and hardware standards, which is exactly the sort of work that software preservation and retro-computing studies aim to document. It also resonates because many players' first encounter with adventure games was through one specific, heavily constrained version of this title. The comparison spans the 4-color CGA, 16-color EGA and 256-color VGA DOS releases as well as the Amiga version, so palette and resolution differences between ports are directly visible rather than described. The site's own interface deliberately imitates Borland Turbo Vision, the text-mode windowing look that many DOS applications of the period shared.

hackernews · maximilianburke · Nov 14, 04:23 · [Discussion](https://news.ycombinator.com/item?id=50493904)

**Background**: The Secret of Monkey Island was built on the SCUMM engine, which Lucasfilm Games created for Maniac Mansion (1987) so that locations, items and dialogue could be defined without writing engine-level code. Because SCUMM kept game scripts and data files cross-platform, the same game could be re-used across many systems, which is why so many distinct versions exist. In that era, PCs shipped with incompatible graphics standards — CGA could show only four colors at 320x200, EGA sixteen, and VGA 256 — so artists had to redraw or re-dither the same scenes for each target machine.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SCUMM_engine">SCUMM engine</a></li>
<li><a href="https://en.wikipedia.org/wiki/ScummVM">ScummVM - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The discussion is dominated by nostalgia but splits on CGA: some commenters say its cyan, magenta, black and white palette felt cold and they could never get used to it, while others express deep respect for artists who produced recognisable scenes from four colors or fewer. Others recall the Amiga release of Monkey Island 2 shipping on around 13 floppy disks with copy protection that only tripped up players partway through the game, and several praise the site's Turbo Vision-style interface and lament that the era's adventure-game magic has never been reproduced.

**Tags**: `#retro-computing`, `#game-development`, `#graphics`, `#software-preservation`, `#adventure-games`

---

<a id="item-5"></a>
## [EFF Warns Tech Companies Are Redefining Privacy Again](https://www.eff.org/deeplinks/2026/11/tech-companies-are-trying-shift-entire-concept-privacy-again) ⭐️ 7.0/10

The Electronic Frontier Foundation published a new analysis arguing that tech companies are once again trying to shift the entire concept of privacy to suit their business models. The piece lands amid growing workplace deployment of AI meeting recorders and other monitoring tools, and it pairs the critique with advice on how individuals can protect themselves. How privacy is defined determines what data collection is considered normal, so a reframing pushed by industry quietly reshapes the default rules for hundreds of millions of ordinary users and employees. The debate is especially urgent in the workplace, where workers report that opting out of AI notetakers is effectively impossible without risking their jobs. The item is policy commentary rather than a technical disclosure, so it offers no new product or vulnerability specifics; its value lies in framing and in the practical, individual-level mitigation advice it points to. The accompanying Hacker News thread (about 395 points and 151 comments) focused heavily on AI meeting transcription as the most concrete everyday manifestation of the trend.

hackernews · gslin · Nov 14, 12:45 · [Discussion](https://news.ycombinator.com/item?id=50496602)

**Background**: The Electronic Frontier Foundation is a San Francisco-based nonprofit digital rights group founded in 1990 to promote internet civil liberties, and it is best known for defending digital privacy, free speech and innovation through litigation, activism and tools such as Privacy Badger. Its warning about companies "shifting the concept of privacy" refers to a long-running pattern in which industry actors redefine privacy as, for example, user control over settings or notice-and-consent, rather than as a limit on collection itself. This matters because the definition used in policy debates typically becomes the definition regulators enforce. The current flashpoint is workplace AI surveillance: always-on notetakers, screen and activity tracking, and even facial emotion analysis are increasingly marketed to employers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Electronic_Frontier_Foundation">Electronic Frontier Foundation - Wikipedia</a></li>
<li><a href="https://www.eff.org/">Electronic Frontier Foundation | Defending your rights in the digital...</a></li>
<li><a href="https://www.inc.com/chloe-rosenberg/is-your-boss-watching-your-face-the-next-frontier-of-workplace-surveillance/91393352">Is Your Boss Watching Your Face? The Next Frontier of Workplace ...</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly hostile to the new surveillance normal: one asked whether it is possible to make "turn off the AI notetaker" an accepted norm for meetings that don't need transcription, since opting out currently looks career-limiting. Others invoked Article 12 of the Universal Declaration of Human Rights on arbitrary interference with privacy, argued for compartmentalized real and throwaway identities plus air gaps, and urged support for EFF and similar litigators; one drew a pointed comparison to the backlash against the original Google Glass.

**Tags**: `#privacy`, `#surveillance`, `#AI`, `#tech-policy`, `#EFF`

---

<a id="item-6"></a>
## [SpaceX to attempt first full recovery of Starship and Super Heavy next month](https://t.me/zaihuapd/45117) ⭐️ 7.0/10

During an earnings call, Elon Musk announced that SpaceX will next month attempt to recover both the Starship spacecraft and its Super Heavy booster on the same flight for the first time. Musk acknowledged the attempt is not guaranteed to succeed but said the odds are higher than on the previous flight. If it works, it would be the first complete recovery of an orbital launch system, a key step toward Musk's goal of rapid, low-cost reuse that underpins Starship's role in NASA's lunar landing plans and SpaceX's Starlink expansion. Full reuse of both stages is what would let SpaceX refurbish and relaunch vehicles quickly rather than building new ones each time. The previous flight was cut short at roughly three hours after one engine shut down early, leaving both the booster and the ship unrecovered; Super Heavy is normally caught by the launch tower's arms, while the ship would return to the launch site for a catch. Musk did not give a specific flight date or vehicle configuration, and the plan remains an announced intention rather than a completed milestone.

telegram · zaihuapd · Nov 14, 03:03

**Background**: Starship is SpaceX's fully reusable, two-stage launch system: Super Heavy is the first stage, powered by 33 Raptor engines burning sub-cooled liquid methane and liquid oxygen, and Starship is the upper stage and spacecraft. SpaceX recovers Super Heavy by catching it with the large "chopstick" arms of the launch tower, and intends to do the same with the ship. Achieving both in one flight is what SpaceX describes as the first full recovery of an orbital launch system; until now, each vehicle has been recovered separately or not at all.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Super_Heavy_Booster_10">Super Heavy Booster 10</a></li>
<li><a href="https://www.zerohedge.com/technology/watch-live-spacex-targets-historic-starship-booster-double-chopsticks-catch">SpaceX Aborts Starship /Booster 'Double Chopsticks' Recovery <!-- --&...</a></li>

</ul>
</details>

**Tags**: `#SpaceX`, `#Starship`, `#spaceflight`, `#reusable rockets`, `#technology news`

---

<a id="item-7"></a>
## [Cloudflare open-sources Kitesurf, a stateless browser for AI agents](https://www.phoronix.com/news/Cloudflare-Kitesurf-Open-Source) ⭐️ 7.0/10

Cloudflare has open-sourced Kitesurf under the Apache 2.0 license, a stateless browser designed specifically for AI agents that runs entirely on top of Cloudflare Workers. It parses HTML, handles CSS, and executes JavaScript without needing a full Chromium container, with the code published on GitHub. Agent workloads are typically bursty and short-lived, so spinning up full browser containers for every task wastes CPU and memory; a Workers-native browser makes such tasks far cheaper and lets agents scale globally on demand. If it gains adoption, it could become a standard lightweight execution layer for web-facing AI agents. Cloudflare claims Kitesurf uses substantially less CPU and memory than Chromium for common agentic tasks such as screenshots and HTML extraction, allowing more concurrent sessions. Because it is stateless and fully isolated, it is aimed at ephemeral sessions rather than long-running interactive browsing, and it only runs inside the Cloudflare Workers ecosystem.

telegram · zaihuapd · Nov 14, 09:33

**Background**: Headless browsers like Chromium run a full rendering engine plus a separate driver (such as the Chrome DevTools Protocol) inside a container, which is powerful but heavy and slow to start. Cloudflare Workers is a serverless runtime that executes JavaScript at the edge in hundreds of cities without managing servers, making it well suited to short, high-concurrency requests. Kitesurf combines these ideas: a browser-like engine that parses pages and runs scripts directly on Workers, avoiding the container overhead entirely.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.cloudflare.com/browser-run/kitesurf/">Kitesurf · Cloudflare Browser Run docs</a></li>
<li><a href="https://kitesurf.cloudflare.app/">Kitesurf - stateless browser running entirely on Workers</a></li>
<li><a href="https://developers.cloudflare.com/workers/">Overview · Cloudflare Workers docs</a></li>

</ul>
</details>

**Tags**: `#Cloudflare`, `#AI agents`, `#browser`, `#serverless`, `#open source`

---

<a id="item-8"></a>
## [Italy's privacy regulator fines Meta €805 million over photo album access](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10321080) ⭐️ 7.0/10

Italy's data protection authority, Garante Privacy, fined Meta €805 million for a Facebook Android photo album recommendation feature launched in 2023, which was enabled by default and accessed the photos, videos and metadata of roughly 20 million Italian users without specific consent. Meta must switch the feature to opt-in and obtain separate, explicit consent within 60 days, or it cannot be offered to users without valid authorization. This is one of the largest GDPR-related penalties ever levied against a major platform, and it reinforces that pre-ticked or default-on settings requiring access to device media are unlikely to satisfy Europe's consent standard. It signals continued aggressive enforcement by national regulators that could shape how Meta and other big tech companies design permission flows across the EU. The regulator's core objection was that the consent prompt was too generic to count as specific consent for accessing a device's photo library, and the fine targets the Android app's media and metadata access rather than Facebook's core service. Meta faces a 60-day remediation deadline, and the order requires an opt-in mechanism with separate consent rather than a single bundled authorization.

telegram · zaihuapd · Nov 14, 14:37

**Background**: The GDPR is the EU's data protection framework, under which companies must have a lawful basis — often explicit, specific user consent — for processing personal data; Italy's Garante Privacy is one of the bloc's most active enforcement authorities. Photos and their embedded metadata (such as timestamps, device details and location data) count as personal data, so scanning a user's gallery requires a clear legal basis. National regulators can fine companies up to 4% of global annual turnover, which is why penalties against platforms like Meta reach hundreds of millions of euros.

**Tags**: `#privacy`, `#Meta`, `#GDPR`, `#regulation`, `#Italy`

---

<a id="item-9"></a>
## [Documentary Traces KDE's Three-Decade Run as a Volunteer Desktop Project](https://tube.kockatoo.org/w/fFinNHfanLT7aBEb2B8y4c) ⭐️ 6.0/10

A documentary about the history and impact of KDE has been published on the PeerTube instance tube.kockatoo.org, prompting a Hacker News thread that reached 322 points and 70 comments. The film chronicles how a volunteer community built a free desktop environment in C++ on top of the Qt toolkit and kept it alive across multiple major rewrites. KDE is one of the longest-running free software desktop projects and its code now ships on devices ranging from school computers in Brazil to the Steam Deck, so the documentary doubles as a case study in sustaining a large volunteer codebase for decades. For developers, the discussion surfaces hard lessons about C++ maintenance burden, community governance, and the cost of disruptive redesigns like the KDE 4 transition. The film is distributed via PeerTube rather than YouTube, and the surrounding thread is driven less by the video itself than by long-time users recounting their personal timelines with KDE 3.x tools such as Amarok 1.4, k3b and Konqueror's KIO slaves. Commenters note that even people who migrated to tiling window managers like AwesomeWM often keep using Dolphin and Konsole, a sign of how sticky individual KDE applications can be even when the full desktop is abandoned.

hackernews · mrkn1 · Nov 14, 13:43 · [Discussion](https://news.ycombinator.com/item?id=50496976)

**Background**: KDE is an international free software community that produces Plasma, a graphical shell for Linux and BSD that manages windows, panels, widgets and system settings, along with a large family of applications such as the Kdenlive video editor and the Krita digital painting tool. Most KDE software is written in C++ using the Qt framework, a cross-platform toolkit for building graphical user interfaces from a single codebase. KDE software is used by millions of people and has been deployed in schools, governments and commercial products, with Brazil alone reporting tens of millions of schoolchildren using KDE-based software.

<details><summary>References</summary>
<ul>
<li><a href="https://kde.org/">Home - KDE Community</a></li>
<li><a href="https://en.wikipedia.org/wiki/KDE_Plasma">KDE Plasma - Wikipedia</a></li>
<li><a href="https://www.qt.io/development/qt-framework">Qt Framework – Build Fast, Scalable Cross-Platform Software | Qt</a></li>

</ul>
</details>

**Discussion**: The mood is affectionate but clear-eyed: commenters describe KDE as a fascinating study in how hard it is to build software in C++ that works for most people, praising the community for absorbing mistakes and holding together contributors with differing cultures and needs. Several long-time users trace their history back to the original Usenet call for volunteers to build a "Kool Desktop Environment" and to the KDE 3.x era, while others say the instability of KDE 4 pushed them away even though they still rely on individual apps like Dolphin and Konsole.

**Tags**: `#KDE`, `#open source`, `#Linux desktop`, `#documentary`, `#community`

---

<a id="item-10"></a>
## [Reddit User Ranks ICLR 2027 Initial Review Scores by University](https://www.reddit.com/r/MachineLearning/comments/1xwcjuq/iclr_2027_initial_review_scores_ranked_by/) ⭐️ 6.0/10

A Reddit user (/u/No-Lab4175) posted a ranking of ICLR 2027 initial review scores aggregated by the authors' university affiliations, building the dataset by crawling OpenReview, matching paper titles to arXiv, and resolving institutional affiliations through OpenAlex. Because ICLR uses open peer review, review scores are publicly visible, which makes it possible to benchmark institutions by how their submissions are received rather than only by acceptance counts; such rankings are increasingly used by prospective students and hiring committees as a rough signal of research strength, even though they are methodologically fragile. The pipeline relies on title matching between OpenReview submissions and arXiv preprints plus OpenAlex affiliation records, so it is exposed to mismatched titles, papers without arXiv versions, and ambiguous or multi-institution author affiliations; the Reddit post itself gives only a one-line description of the methodology and offers no error analysis or normalization for submission volume.

reddit · r/MachineLearning · /u/No-Lab4175 · Nov 14, 20:33

**Background**: ICLR (International Conference on Learning Representations) is one of the premier deep learning conferences and publishes all submissions, reviews, and scores on OpenReview, a free open-source platform built to make peer review transparent. OpenAlex is a free, open bibliographic catalogue of hundreds of millions of scholarly works, authors, and institutions, started in 2022 by OurResearch as a successor to Microsoft Academic Graph. Combining these sources lets anyone reconstruct which institutions submitted which papers and how reviewers scored them.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open_reviewing">Open reviewing</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAlex">OpenAlex</a></li>
<li><a href="https://openreview.net/about">About | OpenReview</a></li>

</ul>
</details>

**Tags**: `#ICLR`, `#peer-review`, `#bibliometrics`, `#machine-learning-research`, `#academic-rankings`

---

<a id="item-11"></a>
## [Reddit ML thread: short-horizon price forecasting papers should benchmark against market-implied forecasts](https://www.reddit.com/r/MachineLearning/comments/1xw6fk9/should_shorthorizon_price_forecasting_papers/) ⭐️ 6.0/10

A Reddit r/MachineLearning post by /u/happypeanut-t argues that most short-horizon crypto and commodity forecasting papers (transformers, LSTMs) only compare against ARIMA, a random walk, or a simple LSTM and report lower RMSE, while rarely benchmarking against what the market already expects, such as options-implied volatility or paid crowd forecasts like prediction markets. The post also complains that papers usually score only the point forecast, and asks whether data access explains why interval coverage of, for example, an 80% interval is not standard evaluation for assets like BTC. The critique matters because beating a random walk is a weak claim once market-implied forecasts, which already aggregate a lot of public information, are on the table; a model that cannot beat the market's own expectation adds little practical value. Emphasizing interval coverage over RMSE also shifts evaluation toward the risk and uncertainty quantification that traders and risk managers actually care about, affecting how ML and quant researchers design and report forecasting results. The post is a discussion prompt rather than a developed empirical analysis, and it offers data access as one possible explanation for the gap while asking whether relevant papers already exist. It specifically distinguishes options-implied volatility, which describes the market's expected range rather than a single point forecast, from prediction markets where participants put money on outcomes.

reddit · r/MachineLearning · /u/happypeanut-t · Nov 14, 16:23

**Background**: In time-series forecasting papers, a random walk (predicting the last value) and ARIMA are standard naive baselines, so reporting a lower RMSE than them is a common but weak benchmark. Options-implied volatility is derived from option prices and reflects the market's estimate of future price swings, effectively a market-implied forecast of the future range. Prediction markets are exchange-traded markets where contract prices indicate the crowd's probability of an event. Interval coverage measures how often the actual outcome falls inside a forecast's nominal interval, so an 80% interval that contains the outcome only 50% of the time is badly calibrated even if its RMSE looks good.

<details><summary>References</summary>
<ul>
<li><a href="https://www.fidelity.com/viewpoints/active-investor/implied-volatility">Implied volatility | Fidelity</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prediction_market">Prediction market</a></li>
<li><a href="https://r-statistics.co/Checking-Prediction-Interval-Coverage.html">The Expert Edge in Forecasting Like a Pro Lesson 7: Checking ...</a></li>

</ul>
</details>

**Tags**: `#financial-forecasting`, `#evaluation-methodology`, `#machine-learning`, `#quantitative-finance`, `#prediction-markets`

---

<a id="item-12"></a>
## [China's W5000, billed as the world's largest unmanned cargo aircraft, completes first validation flight](https://www.ithome.com/1/027/068.htm) ⭐️ 6.0/10

White Whale (白鲸航线) announced on November 14 that its W5000 large unmanned cargo aircraft completed a technical validation test flight in Otog Front Banner, Inner Mongolia, with climb, level flight, turning, descent and approach-and-landing all flown as planned. The company expects to obtain airworthiness certification in the first half of 2027. With a 5-tonne payload and a 2,600 km design range, the W5000 points toward a cargo model where no pilot is on board at all, potentially cutting crew costs and enabling routes too thin or too remote for conventional freighters. A successful certification in 2027 would make it one of the first large unmanned freighters to enter commercial logistics service, a milestone for China's low-altitude economy push. The aircraft has a maximum takeoff weight of 10.8 tonnes, a 5-tonne payload and a 2,600 km design range — roughly a medium truckload delivered 2,600 km away in one sortie. It uses turboprop propulsion with an autonomous-flight, ground-monitoring operating model, and by design a single crew can supervise six to seven aircraft at once.

telegram · zaihuapd · Nov 14, 05:00

**Background**: The W5000 is developed by White Whale (白鲸航线), a Chinese startup whose project began in 2021 and whose first aircraft rolled off the assembly line at its Changzhou production base in October. Large cargo drones like this sit in a regulatory category distinct from consumer drones: in China, unmanned aircraft above 25 kg fall under CCAR-92 airworthiness rules, so the 2027 target means completing design, flight-test and production certification with the civil aviation authority. Turboprop engines — jet turbines driving propellers — are favoured for freighters because they are efficient at the moderate speeds and altitudes such aircraft fly.

<details><summary>References</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260321A0615B00">全球最大 无 人 货 运飞 机 ， 白 鲸 航 线 W 5000 ...</a></li>
<li><a href="https://www.163.com/dy/article/K886ASET05149OCK.html">平安产险护 航 白 鲸 启 航 ： W 5000 无 人 货 运 机 首飞开启 航 空新篇</a></li>
<li><a href="https://www.cnblogs.com/sweetheart-sole/p/21043927">2026...</a></li>

</ul>
</details>

**Tags**: `#unmanned aviation`, `#autonomous cargo`, `#logistics`, `#China tech`, `#test flight`

---

<a id="item-13"></a>
## [New Zealand Warehouse Workers Protest AI Monitoring of Bathroom Breaks](https://www.independent.co.uk/news/world/australasia/new-zealand-workers-ai-bathroom-breaks-b3084317.html) ⭐️ 6.0/10

More than 300 workers at The Warehouse Group's distribution centers in Auckland and Christchurch protested this week, with the Worker First alliance alleging that staff had been reprimanded over bathroom breaks tracked by monitoring systems and that some employees suffered accidents after holding it in. The company's chief people officer denied the most serious claims, saying the scanning technology used is not AI and is unrelated to bathroom breaks, and that no roles were cut because of inventory drones. The dispute is a concrete, high-profile example of how AI-enabled workplace surveillance is moving from theory into daily labor conflict, and it shows that productivity-tracking tools can quickly become privacy and dignity issues that trigger organized backlash. It is likely to feed into broader debates about what employers must disclose to workers and unions before deploying automation and monitoring systems. The union also claims the company introduced large robotic picking machines and AI drones that replaced part of the inventory team, while the company says the drones did not eliminate any positions but declined to guarantee future roles, promising only consultation and retraining where possible. The allegations about bathroom breaks rest on union testimony rather than published evidence, and the company disputes the characterization of its scanning technology as AI.

telegram · zaihuapd · Nov 14, 06:15

**Background**: Warehouse operators increasingly use computer vision cameras, autonomous indoor drones and algorithmic task-tracking to measure inventory accuracy and individual productivity, and the same data streams can be used to score how workers spend their time. New Zealand's Privacy Act 2020 sets rules on how organizations may collect and use personal information, including in the workplace, which is why the dispute has become a privacy question as much as a labor one. Because these systems are often procured from third-party vendors, workers frequently learn about them only through union channels or after discipline begins.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ndtv.com/world-news/new-zealand-workers-defecate-in-shopping-aisles-as-ai-tracks-bathroom-breaks-12324792">Workers Defecate In Shopping Aisles As AI Tracks Bathroom Breaks</a></li>
<li><a href="https://oecd.ai/en/incidents/2026-11-11-dcf0">AI Monitoring Leads to Worker Distress at New Zealand Retailer</a></li>
<li><a href="https://www.verity.net/">Verity | Warehouse Intelligence Platform - Autonomous Inventory ...</a></li>

</ul>
</details>

**Tags**: `#AI surveillance`, `#workplace monitoring`, `#privacy`, `#labor rights`, `#New Zealand`

---

<a id="item-14"></a>
## [Google AI Studio designer runs Windows 11 on foldable iPhone via WindowsiOS](https://www.windowslatest.com/2026/11/14/windows-11-can-run-on-apples-foldable-iphone-and-googles-ai-boss-proved-it-using-gemini-years-after-microsoft-gave-up-on-windows-phones/) ⭐️ 6.0/10

Ammaar Reshi, a product design lead at Google AI Studio, demonstrated Windows 11 24H2 running locally on a foldable device called the iPhone Duo using the open-source WindowsiOS project, with Gemini 4 Carbon reportedly involved in the process and a video of the demo published. The demo uses JIT-based ARM64 translation without jailbreaking the device. This is a striking proof of concept for running a full desktop operating system locally on non-jailbroken iOS hardware, showing how far JIT-based translation layers have come despite Apple's platform restrictions. It is likely to energize enthusiasts exploring Windows-on-ARM and mobile virtualization, though it remains a single-person showcase rather than a practical product. WindowsiOS runs Windows 11 24H2 ARM64 at near-native JIT speed and relies on Microsoft's Prism emulator to run some traditional x86 applications, according to the project. The setup requires an approximately 12 GB image, an Apple Silicon Mac, development tools and an LLDB debugger, and independent verification of the demo is not yet available.

telegram · zaihuapd · Nov 14, 06:52

**Background**: Windows on Arm normally runs native ARM64 software and uses Microsoft's Prism emulator to translate x86 and x64 applications, which is how Windows 11 on Arm devices can run older software. On iOS, Apple tightly restricts just-in-time compilation, so projects often rely on debugger-enabled workflows to allow JIT execution for development and research. WindowsiOS combines these ideas by translating ARM64 Windows code on top of iOS rather than virtualizing a full PC.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ammaarreshi/WindowsiOS">GitHub - ammaarreshi/WindowsiOS: Native Windows 11 ARM64 on ...</a></li>
<li><a href="https://learn.microsoft.com/en-us/windows/arm/apps-on-arm-x86-emulation">How emulation works on Arm | Microsoft Learn</a></li>
<li><a href="https://www.windowscentral.com/software-apps/what-is-microsoft-prism">What is Microsoft 's Prism ? Explaining the... | Windows Central</a></li>

</ul>
</details>

**Tags**: `#emulation`, `#Windows on ARM`, `#iOS`, `#JIT translation`, `#AI-assisted development`

---