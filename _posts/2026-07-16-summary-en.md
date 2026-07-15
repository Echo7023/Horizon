---
layout: default
title: "Horizon Summary: 2026-07-16 (EN)"
date: 2026-07-16
lang: en
---

> From 33 items, 7 important content pieces were selected

---

1. [DeepSeek Raises Over 50 Billion RMB in First Funding Round](#item-1) ⭐️ 9.0/10
2. [Musk: X to open-source all code unconditionally](#item-2) ⭐️ 9.0/10
3. [Mental health and communication in software development](#item-3) ⭐️ 8.0/10
4. [Claude web_fetch bypass enables memory exfiltration](#item-4) ⭐️ 8.0/10
5. [DeepSeek Plans IPO by 2025/2026, Seeks New Funding](#item-5) ⭐️ 8.0/10
6. [Retail 'Vertical Era' Ends: Sam's, Snack Stores, Pinduoduo Compete for Same Wallet](#item-6) ⭐️ 8.0/10
7. [Telegram Launches Serverless Platform for Bots](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek Raises Over 50 Billion RMB in First Funding Round](https://t.me/zaihuapd/42589) ⭐️ 9.0/10

DeepSeek has completed its first external funding round, raising over 50 billion RMB (approximately 7.4 billion USD) at a valuation exceeding 50 billion USD. The round uses a special limited partnership structure that allows founder Liang Wenfeng to maintain control, with no voting rights for investors and a five-year lock-up period. This massive funding round validates DeepSeek as a major player in the global AI race, especially given its cost-efficient model development. The unique control structure could influence how other startups negotiate funding while preserving founder autonomy. Founder Liang Wenfeng personally invested 20 billion RMB in this round. Tencent is considering an investment of 10 billion RMB, and CATL plans to invest 5 billion RMB, making them the largest external investors.

telegram · zaihuapd · Jul 15, 12:56

**Background**: DeepSeek is a Chinese AI company founded in 2023 by Liang Wenfeng, previously backed by hedge fund High-Flyer. It gained prominence in early 2025 with its R1 model, which rivals OpenAI's GPT-4 at a fraction of the training cost. The company uses a limited partnership structure — investors contribute to a fund managed by Liang, not directly to DeepSeek — to preserve founder control, a common tactic in venture capital to balance investor influence with founder vision.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_(Company)">DeepSeek (Company)</a></li>
<li><a href="https://lomitpatel.com/articles/founder-control-startup-funding/">Navigating Founder Control Startup Funding Dynamics</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Funding`, `#DeepSeek`, `#Startup`, `#Venture Capital`

---

<a id="item-2"></a>
## [Musk: X to open-source all code unconditionally](https://x.com/elonmusk/status/2077361679034118271) ⭐️ 9.0/10

Elon Musk announced that X will open-source its entire codebase unconditionally after a security vulnerability review, and will invite third-party reviewers to verify the running system matches the open-source code. This represents a major shift towards transparency for a widely-used social media platform, potentially increasing trust and accountability among users and regulators. It sets a precedent for other platforms to follow in open-sourcing their core infrastructure. The open-sourcing will occur after a security vulnerability review, and third-party reviewers will be used to confirm that the running system matches the released code. The announcement did not specify a timeline or which parts of X's stack would be included.

telegram · zaihuapd · Jul 15, 13:32

**Background**: Open-sourcing a platform's code allows anyone to inspect, audit, and contribute to it, promoting transparency and community trust. Third-party review of running systems adds an extra layer of verification to ensure no hidden modifications exist. This move follows Musk's earlier pledges to make X more transparent, though many details remain to be seen.

**Tags**: `#open source`, `#social media`, `#transparency`, `#Elon Musk`, `#code audit`

---

<a id="item-3"></a>
## [Mental health and communication in software development](https://ramones.dev/posts/mental-health/) ⭐️ 8.0/10

A blog post advocating for prioritizing mental health and effective communication in software development has sparked extensive community discussion with 141 comments, focusing on neurodiversity and self-management strategies. Mental health is often overlooked in the high-pressure software industry; this post and discussion highlight systemic issues and offer practical self-management advice, especially for neurodivergent developers. The post shares personal goals for 2027, including eliminating stupid mistakes via structured planning, but commenters argue that neurodivergent conditions like ADD cannot be fixed by willpower alone and require proper diagnosis and accommodation.

hackernews · ramon156 · Jul 15, 11:27 · [Discussion](https://news.ycombinator.com/item?id=48919198)

**Background**: Neurodiversity in software development refers to the natural variation in human brain functions, including conditions like ADHD, autism, and dyslexia. Increasingly, companies recognize that neurodivergent individuals bring unique strengths but also require tailored work environments and communication styles.

<details><summary>References</summary>
<ul>
<li><a href="https://dl.acm.org/doi/10.1145/3613372.3613384">Understanding and Supporting Neurodiverse Software Developers ...</a></li>
<li><a href="https://blog.auticon.com/neurodiversity-in-software-engineering/">Neurodiversity in Software Engineering: Unlocking the ...</a></li>

</ul>
</details>

**Discussion**: Commenters strongly debate the root cause of productivity struggles: some attribute them to neurodivergent conditions like ADD, urging proper diagnosis over self-help tips, while others emphasize self-awareness and adapting work strategies. One comment compares managing oneself to managing a valuable employee, focusing on strengths rather than perceived shortcomings.

**Tags**: `#mental health`, `#software development`, `#neurodiversity`, `#self-management`, `#communication`

---

<a id="item-4"></a>
## [Claude web_fetch bypass enables memory exfiltration](https://simonwillison.net/2026/Jul/15/claude-web-fetch-exfiltration/#atom-everything) ⭐️ 8.0/10

Security researcher Ayush Paul discovered a loophole in Anthropic's Claude web_fetch tool that allowed attackers to exfiltrate private user memory data by tricking the AI into following malicious links embedded in fetched pages. This vulnerability undermines the core privacy protections of conversational AI agents that store user memories, demonstrating that even carefully designed exfiltration barriers can be bypassed through creative prompt injection. It highlights the ongoing challenge of securing AI systems against the lethal trifecta of private data, untrusted content, and external communication. The attack exploited web_fetch's ability to navigate to URLs embedded in previously fetched pages, using a honeypot site that instructed Claude to concatenate private data into URLs for exfiltration. The attack was only triggered for clients with a 'Claude-User' user-agent to avoid detection, and successfully extracted the user's name, city, and employer.

rss · Simon Willison · Jul 15, 14:21

**Background**: The 'lethal trifecta' refers to a dangerous combination where an AI agent has access to private data, processes untrusted content (e.g., from the web), and can communicate externally, enabling prompt injection attacks. Claude's web_fetch tool is designed to only fetch exact URLs provided by the user or returned from web_search, but Ayush Paul found it could also follow links from fetched pages, creating an exfiltration vector.

<details><summary>References</summary>
<ul>
<li><a href="https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/">The lethal trifecta for AI agents: private data, untrusted content, and external communication</a></li>
<li><a href="https://mikhail.io/2025/10/claude-code-web-tools/">Inside Claude Code's Web Tools: WebFetch vs WebSearch</a></li>

</ul>
</details>

**Tags**: `#security`, `#AI`, `#Claude`, `#data exfiltration`, `#vulnerability`

---

<a id="item-5"></a>
## [DeepSeek Plans IPO by 2025/2026, Seeks New Funding](https://t.me/zaihuapd/42577) ⭐️ 8.0/10

DeepSeek has initiated IPO preparations, aiming to file by late 2025 or early 2026 and list in 2027, while concurrently seeking a new funding round at a pre-money valuation of approximately $71 billion. This news signals significant investor confidence in DeepSeek's AI capabilities and growth trajectory, potentially marking one of the largest AI IPOs in Chinese history and providing substantial capital for further development. The new funding round targets at least 10 billion yuan (about $1.4 billion), with the final amount potentially multiplying based on investor demand; the valuation of $71 billion represents a sharp increase from the $50 billion valuation during its first external funding round in early June 2025.

telegram · zaihuapd · Jul 15, 07:04

**Background**: DeepSeek is a Chinese AI startup based in Hangzhou, founded by Liang Wenfeng. In early June 2025, it completed its first external funding round of $700 million from investors including Tencent and CATL. The company focuses on developing advanced AI models and has rapidly gained market attention.

**Tags**: `#DeepSeek`, `#IPO`, `#AI`, `#funding`, `#startup`

---

<a id="item-6"></a>
## [Retail 'Vertical Era' Ends: Sam's, Snack Stores, Pinduoduo Compete for Same Wallet](https://mp.weixin.qq.com/s/dAHAVxglD-F1RovjcvqCRw) ⭐️ 8.0/10

Based on a large-scale survey of 257 interviews and 5,224 questionnaires, Chinese retail's vertical era has ended; different retail formats like Sam's Club, snack discount stores, instant retail, and Pinduoduo now compete for the same household spending. This shift signals a fundamental change in consumer behavior and market structure, forcing retailers to compete on trust and convenience rather than just price or category specialization. The survey found that 48% of respondents plan to control consumption; for offline purchases, distance is more important than price; and overly low prices for food items trigger safety concerns, making trust the primary competitive factor.

telegram · zaihuapd · Jul 15, 09:01

**Background**: The 'vertical era' in Chinese retail refers to a period when retailers specialized in narrow product categories to gain a competitive edge. However, this era is now ending as consumers increasingly treat all retail formats as interchangeable options for fulfilling daily needs, blurring traditional category boundaries. Instant retail, which delivers groceries and goods within minutes like food delivery, is also blurring the lines between online and offline channels.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sohu.com/a/761203003_100198219">在日本“失去的三十年”中，零售业态如何保持自身的竞争力？</a></li>
<li><a href="https://m.pedaily.cn/news/494407">商品像外卖一样送到家，品牌们盯上了 即 时 零 售 |投资界</a></li>

</ul>
</details>

**Tags**: `#零售业`, `#消费趋势`, `#行业分析`, `#调研`

---

<a id="item-7"></a>
## [Telegram Launches Serverless Platform for Bots](https://core.telegram.org/bots/serverless) ⭐️ 8.0/10

Telegram has officially launched a serverless platform that allows developers to run bot and Mini App backend code directly on Telegram's infrastructure, deployable with a single command via npx tgcloud push. This dramatically simplifies bot development and deployment, eliminating the need for developers to manage servers or handle scaling. It may accelerate the Telegram bot ecosystem by lowering barriers for new developers. The platform uses JavaScript modules running in an isolated V8 sandbox near the Bot API, and includes a built-in SQLite database for persistent storage. Deployment is done via the command npx tgcloud push.

telegram · zaihuapd · Jul 15, 16:00

**Background**: Telegram bots are automated programs that interact with users, but previously required developers to host their own backend servers. Serverless computing abstracts server management, allowing code to run on cloud infrastructure without provisioning. The V8 sandbox ensures security isolation for each bot's code.

<details><summary>References</summary>
<ul>
<li><a href="https://core.telegram.org/bots/webapps">Telegram Mini Apps</a></li>
<li><a href="https://v8.dev/blog/sandbox">The V8 Sandbox</a></li>

</ul>
</details>

**Tags**: `#Telegram`, `#serverless`, `#bots`, `#developer tools`, `#JavaScript`

---