---
layout: default
title: "Horizon Summary: 2026-11-25 (EN)"
date: 2026-11-25
lang: en
---

> From 30 items, 19 important content pieces were selected

---

1. [Anthropic Says Internal Claude Model Found VP≠VNP Proof with Lean 4 Formalization](#item-1) ⭐️ 9.0/10
2. [Ternary Bonsai 2.5 27B: a 5.9 GB ternary model claiming frontier-level coding](#item-2) ⭐️ 8.0/10
3. [OpenAI says GPT-6 models can design protein minibinders by writing code](#item-3) ⭐️ 8.0/10
4. [GreyNoise: Attackers Forge Check Point Admin Cookies via V8 PRNG](#item-4) ⭐️ 8.0/10
5. [Quad9 withdraws public DNS service from France over legal constraints](#item-5) ⭐️ 8.0/10
6. [Simon Willison Maps Three LLM Inflection Points in Twelve Months](#item-6) ⭐️ 8.0/10
7. [GPT-6.2 Astra Autonomously Identifies Creator of an 1808 Yale Sketchbook](#item-7) ⭐️ 8.0/10
8. [VMware vCenter hit by another 9.8-rated authentication bypass, already exploited as a zero-day](#item-8) ⭐️ 8.0/10
9. [Leaked GTA 6 Xbox Build Boots on Windows via Wine-Style Recompilation](#item-9) ⭐️ 7.0/10
10. [Songe: an open-source engine that trains local LLM agents on idle compute](#item-10) ⭐️ 7.0/10
11. [Flame Graphs and Deterministic VMs Debated for Performance Analysis](#item-11) ⭐️ 7.0/10
12. [Blogger argues closed LLM agents serve their vendors, not their users](#item-12) ⭐️ 7.0/10
13. [GTA 6 'Leonida' PC Recompilation Project Taken Down From GitHub](#item-13) ⭐️ 7.0/10
14. [Developer alleges T3 Code turns on telemetry by default and reads local Codex and Claude credentials](#item-14) ⭐️ 7.0/10
15. [Huawei and Qualcomm Sign Broad Multi-Year Patent Cross-License Covering 5G and AI](#item-15) ⭐️ 7.0/10
16. [SpaceX and Tesla Boards Form Special Committees to Weigh Merger](#item-16) ⭐️ 7.0/10
17. [Anthropic shares fall below $83 IPO price, stirring AI economics debate](#item-17) ⭐️ 6.0/10
18. [Robin Li Says Open-Source LLMs Add Little Value, Baidu Won't Compete With Developers](#item-18) ⭐️ 6.0/10
19. [Anthropic CEO Dario Amodei Predicts AI Could Cure Cancer Within 10 Years](#item-19) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Anthropic Says Internal Claude Model Found VP≠VNP Proof with Lean 4 Formalization](https://t.me/zaihuapd/45345) ⭐️ 9.0/10

On November 24, Anthropic reportedly published a paper titled "VP ≠ VNP over every field" together with a Lean 4 formalization repository, stating that the result was discovered by an internal research Claude model and that both the paper and code were written by AI. The paper claims a super-polynomial arithmetic-circuit lower bound for the Hamiltonian cycle polynomial, implying that VP is a proper subset of VNP and thus resolving Valiant's 1979 algebraic complexity conjecture. If verified, this would be a landmark result in computational complexity and a striking demonstration of AI-driven theorem proving, since a machine-discovered proof of a decades-old open conjecture would reshape how the research community uses AI in mathematics. It would also intensify scrutiny of AI-generated mathematical claims, because the announcement came through a secondary Telegram channel rather than a peer-reviewed venue. The claimed separation applies only to arithmetic circuits, so it does not settle the classical P versus NP question, and the repository reports an audit against three standard axioms plus an independent kernel check. Crucially, the claim is extraordinary and currently rests on a Telegram source, so independent verification by complexity theorists and a successful from-scratch Lean 4 build remain essential.

telegram · zaihuapd · Nov 24, 12:18

**Background**: Arithmetic circuits are the standard model for computing polynomials, where a circuit takes variables or numbers as inputs and combines previously computed expressions by addition and multiplication. In 1979 Valiant introduced the algebraic complexity classes VP and VNP as analogues of P and NP, conjecturing that VP is a proper subset of VNP and showing that the permanent (and the directed Hamiltonian cycle polynomial) is VNP-complete under projections. Lean 4 is a proof assistant based on dependent type theory in which every step of a proof must be mechanically checked by a kernel, so a formalization that compiles leaves no room for a hand-waved argument.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Arithmetic_circuit_complexity">Arithmetic circuit complexity - Wikipedia</a></li>
<li><a href="https://mathworld.wolfram.com/ValiantsConjecture.html">Valiant's Conjecture -- from Wolfram MathWorld</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean ( proof assistant ) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI for science`, `#theorem proving`, `#computational complexity`, `#Lean 4`, `#Anthropic`

---

<a id="item-2"></a>
## [Ternary Bonsai 2.5 27B: a 5.9 GB ternary model claiming frontier-level coding](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 8.0/10

PrismML released Ternary Bonsai 2.5 27B, the largest model in its Bonsai family, a ternary (roughly 1-bit/Q2 GGUF) quantized model derived from Qwen3.8-27B with the architecture left unchanged and shipped in a 5.9 GB footprint. The company claims substantially stronger agentic coding, multi-turn tool use and multi-step task execution at that size, with users reporting results approaching frontier models on SWE-bench Verified. If the claims hold up, a roughly 6 GB model that fits comfortably in 24 GB of unified memory means a consumer Mac Mini or laptop can run a genuinely useful offline coding agent, which would undercut the assumption that agentic coding requires datacenter-scale hardware. It also sharpens the debate over whether small-model gains are real capability progress or benchmark-specific optimization. The model keeps Qwen3.8-27B's hybrid-attention architecture and is distributed as a Q2 GGUF quant, with one community tester measuring about 22–25 tokens/s generation and 222.9 tokens/s prompt processing on a Mac Mini M5 Pro with 24 GB RAM, plus a 2.12 s time-to-first-token and enough headroom for roughly 128k context. Caveats include the fact that SWE-bench Verified covers only a narrow set of Python repository issues, and that the headline comparisons are drawn against much larger frontier models rather than equivalently sized quantized baselines.

hackernews · b0m · Nov 24, 20:08 · [Discussion](https://news.ycombinator.com/item?id=50633922)

**Background**: Ternary quantization is an extreme form of weight compression in which each weight is restricted to just three values (−1, 0, +1), sometimes called 1.58-bit, which shrinks memory use dramatically but is hard to apply well because outliers in weights and activations degrade accuracy. SWE-bench Verified is the most-cited benchmark for AI coding agents: it presents real GitHub issues from Python repositories and requires the model to produce patches that pass the project's test suites. Bonsai is PrismML's family of such aggressively quantized models, with the 27B variant aimed specifically at long-running agent workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.prismml.com/models/bonsai-2-5-27b">Ternary Bonsai 2.5 27B - Bonsai - docs.prismml.com</a></li>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2.5 27B: Powering ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/1.58-bit_large_language_model">1.58-bit large language model - Wikipedia</a></li>
<li><a href="https://www.swebench.com/">SWE-bench Leaderboards</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread is a mix of hands-on enthusiasm and calibrated skepticism: one commenter posted concrete throughput numbers and a working "Pelican" sample from a 1-bit model on an M3 MacBook Air using 7–8 GB of RAM, while another argued the SWE-bench Verified score is roughly comparable to a much larger frontier model and asked how much of that is benchmark-maxxing, benchmark drift, or genuine small-model progress arriving with a delay. Others simply asked for head-to-head comparisons against equivalently small quantized versions of popular models.

**Tags**: `#LLM quantization`, `#ternary models`, `#local inference`, `#small language models`, `#SWE-bench`

---

<a id="item-3"></a>
## [OpenAI says GPT-6 models can design protein minibinders by writing code](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) ⭐️ 8.0/10

OpenAI reported that GPT-6.2, given the three-dimensional structures of five target proteins with the desired attachment sites marked, wrote code to generate 3D designs for potential minibinders without using specialized protein AI models, and lab tests found evidence of binding across all five targets. The company framed the result as an intrinsic protein-design capability emerging from a general-purpose model rather than a purpose-built structural biology system. If a general-purpose LLM can carry out meaningful de novo protein design simply by writing code, it would lower the barrier to AI-assisted biologics and drug-discovery research and blur the boundary between general reasoning models and domain-specific structure-prediction tools. It also raises questions about how much credit for such results belongs to the language model versus the specialized models still used downstream. GPT-6.2 produced only the three-dimensional backbone designs; the amino acid sequences came from the specialized model SolubleMPNN, and other protein models were used to filter candidates predicted to fold as designed and bind at the intended site. The evidence is a single OpenAI publication reporting lab binding signals across five targets, not a peer-reviewed head-to-head benchmark against established design pipelines.

hackernews · acossta · Nov 24, 21:02 · [Discussion](https://news.ycombinator.com/item?id=50634658)

**Background**: Minibinders are small de novo-designed proteins that bind tightly to a specific target protein, and they are a common goal of AI protein design because of their potential as therapeutics and research reagents. Standard pipelines split the problem into two steps: a structure-generating model such as RFdiffusion proposes a 3D backbone, then a sequence-design network such as ProteinMPNN or its soluble variant SolubleMPNN assigns amino acids that should fold into that backbone. Domain-specific models are also used to filter designs by predicted folding stability and binding, which is why the division of labor in OpenAI's report is the crux of the debate.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/">GPT-6 models demonstrate intrinsic protein-design ... - OpenAI</a></li>
<li><a href="https://elifesciences.org/reviewed-preprints/96154">De novo- designed minibinders expand the synthetic biology sensing...</a></li>
<li><a href="https://www.nature.com/articles/s44222-025-00349-8">AI-driven protein design - Nature Reviews Bioengineering</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were divided: a researcher who did a PhD at the Baker lab said it makes total sense and described native fusion of protein and language modeling as the obvious future, while others argued that because the sequence is the structure, GPT-6.2 mainly contributed scaffolding and code while SolubleMPNN did the actual protein design. Others questioned the framing given OpenAI's promotional role and pointed to competing open-weight biology models and reports that Claude was trained on protein sequences at scale.

**Tags**: `#AI for biology`, `#protein design`, `#LLMs`, `#OpenAI`, `#scientific research`

---

<a id="item-4"></a>
## [GreyNoise: Attackers Forge Check Point Admin Cookies via V8 PRNG](https://www.greynoise.io/blog/check-point-security-management-servers-intrusion-campaign) ⭐️ 8.0/10

GreyNoise published research documenting an active intrusion campaign (tracked as GT13) against Check Point Security Management Servers, in which the attacker pivoted to a compromised HFS server and abused its loginSrp1 endpoint, which returns a signed session cookie whose "sid" value is drawn from JavaScript's Math.random(). By performing repeated logins, the actor collected enough consecutive outputs to reconstruct the internal state of the Node.js V8 PRNG, recover the HFS session-cookie signing key, and forge a signed administrator session cookie. The Check Point Security Management Server is the central control point for an organization's firewall policies, gateways and logs, so an attacker holding a forged admin session effectively owns the entire security perimeter. The case is also a textbook demonstration that a non-cryptographic PRNG used for security-sensitive values can be reversed from observed output alone, without any memory leak or key disclosure. GreyNoise states the actor already had access to the victim Check Point Security Management Servers before compromising the HFS server, but could not determine when or how that initial access was obtained; the write-up also notes a possible link to CVE-2026-16232 across multiple affected customers. The attack only works because V8's Math.random() uses a fast, non-cryptographic algorithm whose state can be reconstructed from a handful of consecutive outputs, meaning the flaw lies in using it to generate session identifiers and signing material rather than in the PRNG itself.

hackernews · louiereederson · Nov 24, 16:32 · [Discussion](https://news.ycombinator.com/item?id=50630594)

**Background**: Check Point Security Management Server is the appliance administrators use to define firewall rules and push policy to gateways; compromising it is far more valuable than compromising a single firewall. JavaScript's Math.random() is explicitly specified as returning a pseudo-random number from an implementation-dependent algorithm, and V8 implements it with xorshift128+, a fast generator that is not designed to resist prediction. Web applications often reuse Math.random() for tokens, session IDs or keys because it is convenient, which lets an attacker who can observe enough outputs reconstruct the generator's internal state and predict everything that follows — including secret signing keys.

<details><summary>References</summary>
<ul>
<li><a href="https://www.greynoise.io/blog/check-point-security-management-servers-intrusion-campaign">An Active Intrusion Campaign Against Check Point Security ...</a></li>
<li><a href="https://v8.dev/blog/math-random">There’s Math . random (), and then there’s Math . random () · V 8</a></li>
<li><a href="https://tech.yahoo.com/cybersecurity/articles/control-tower-left-unguarded-check-094326324.html">The Control Tower Left Unguarded: Check Point ’s Management ...</a></li>

</ul>
</details>

**Discussion**: Commenters were impressed by the technical depth of the PRNG state recovery, with several noting it as an old but recurring lesson about non-cryptographic randomness. One widely echoed view was that Math.random() itself should be made at least somewhat secure rather than expecting thousands of applications to use it correctly, while others speculated that LLM-driven automation will soon let far less sophisticated criminals mount such attacks, and at least one reader questioned how the victims' management servers ended up reachable from the internet.

**Tags**: `#security`, `#vulnerability-exploitation`, `#prng`, `#nodejs`, `#check-point`

---

<a id="item-5"></a>
## [Quad9 withdraws public DNS service from France over legal constraints](https://quad9.net/news/blog/quad9-service-deactivation-in-france/) ⭐️ 8.0/10

Quad9 has deactivated its public DNS service for users in France, and queries to its 9.9.9.9 resolver from French networks now return REFUSED responses with an Extended DNS Error stating that service is unavailable due to French legal constraints. This removes a widely used security- and privacy-focused resolver from a major EU country, showing how national legal orders can force global public DNS providers to choose between compliance and withdrawal. French users who rely on Quad9 lose its malware filtering and encrypted DNS options unless they switch to another resolver or use a workaround. Quad9 operates filtered and unfiltered services on separate addresses and hostnames and supports plain DNS, DoT, and DoH; a community member has set up a proxy that forwards French users' queries to Quad9 over those protocols for both IPv4 and IPv6. The refusal is being generated by Quad9's own resolver via REFUSED and EDE code 18 rather than by local network interception, and reports link the dispute to French site-blocking and piracy enforcement.

hackernews · farrokhi · Nov 24, 08:33 · [Discussion](https://news.ycombinator.com/item?id=50625384)

**Background**: DNS is the internet's naming system: resolvers translate domain names such as example.com into IP addresses, and most online activity depends on them. Quad9 is a free public recursive resolver best known for blocking lookups of known malicious domains, and it offers encrypted DNS transports such as DoH and DoT to protect queries from tampering and surveillance. Because public resolvers operate across borders but must answer to local law, countries can compel them to block domains or stop serving users; France has an active site-blocking regime. This case fits a broader debate over DNS privacy, censorship resistance, and who controls public resolution infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Quad9">Quad9 - Wikipedia</a></li>
<li><a href="https://quad9.net/service/service-addresses-and-features/">Service Addresses & Features | Quad9</a></li>
<li><a href="https://www.bleepingcomputer.com/news/technology/google-unveils-dns-over-https-doh-plan-mozillas-faces-criticism/">Google Unveils DNS -over-HTTPS (DoH) Plan, Mozilla's Faces Criticism</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters confirmed the outage with dig output showing REFUSED and an EDE message citing French legal constraints, and one user offered an open proxy as a drop-in replacement for French users. Others questioned why Quad9 complies if it has no French offices or personnel, while links to earlier threads and a TorrentFreak update framed the move as part of a wider piracy-blocking and censorship debate.

**Tags**: `#DNS`, `#privacy`, `#internet censorship`, `#France`, `#Quad9`

---

<a id="item-6"></a>
## [Simon Willison Maps Three LLM Inflection Points in Twelve Months](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 8.0/10

Simon Willison published a follow-up essay to his AI Engineer Code Summit keynote, arguing that LLM and coding-agent capabilities crossed three distinct inflection points between November 2025 and November 2026. He anchors the timeline on November 24, 2026 — the one-year anniversary of Claude Opus 4.5, which he calls a 'consequential model' because it was the first one whose default output in Claude Code was generally correct. Rather than another benchmark table, this gives engineers a periodization of the past year: which model generations actually changed day-to-day coding workflows and when. That framing helps teams reason about how quickly reliability and autonomy have improved, and what to expect from the next generation of coding agents. The first inflection is November 2025, when Claude Opus 4.5 landed alongside OpenAI's GPT-5.1 Instant, GPT-5.1 Thinking, GPT-5.1-Codex and Codex-Max, making both Claude Code and Codex reliably useful. The second is the mid-2026 arrival of what Willison calls 'Fable class models' — Claude Fable 5, a defanged version of the withheld Claude Mythos, which was briefly blocked by US export controls until July 1, and which Willison defines as models that can brute-force a solution once you specify a goal and supply the necessary tools. The excerpt is truncated before the third inflection point is revealed, and the broader search results confirm Opus 4.5 is now deprecated on the Claude API, superseded by Opus 5.5.

rss · Simon Willison · Nov 24, 23:02

**Background**: A coding agent is a large language model given tools — a file system, a shell, test runners, a browser — so that it can take multi-step actions on a codebase rather than just suggesting snippets. Claude Code is Anthropic's agentic command-line tool, launched on February 24, 2025 alongside Claude 3.7 Sonnet, and it was roughly nine months old when Opus 4.5 shipped. Simon Willison is a long-time developer and prolific writer on LLM tooling, and the AI Engineer Code Summit is a San Francisco conference whose 2026 recordings were published on November 10, 2026.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.engineer/code/2026">AI Engineer Code Summit 2026 Recordings: AI Engineering ...</a></li>
<li><a href="https://www.anthropic.com/news/claude-opus-4-5">Introducing Claude Opus 4.5 \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/models/opus-4-5/overview">Claude Opus 4.5 - Claude Platform Docs</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#coding agents`, `#AI engineering`, `#Claude Opus`, `#developer tools`

---

<a id="item-7"></a>
## [GPT-6.2 Astra Autonomously Identifies Creator of an 1808 Yale Sketchbook](https://simonwillison.net/2026/Nov/24/astra-historical-mystery/) ⭐️ 8.0/10

History professor Mark Humphries documented that GPT-6.2 Astra, with minimal prompting, autonomously identified the creator of an anonymous 1808 sketchbook held at Yale's Beinecke Library in just 22 minutes using public primary and secondary sources. In doing so, the system surfaced a little-known paper-archive source that independently constitutes a significant find for Canadian and fur-trade historians. This provides a concrete, professor-documented case of an LLM agent performing genuine novel research and producing a new historical source, rather than merely assisting with search or writing. It is a signal for AI research-tool builders and for historians who may soon face agentic systems that can do archival work humans cannot do as quickly. Astra found a diary reference to a visit by the vicomte de Chabot five days before a date mentioned in the sketchbook at a nearby river, then predicted that Chabot's travel journal—available only by order from Cleveland State University—would confirm the sketchbook was his. The account is a single case study posted on Humphries's Substack rather than a peer-reviewed paper, and Humphries argues historians may face only a mild "Deep Blue" crisis because history is reinterpretive and humanistic rather than a single-truth game like mathematics.

rss · Simon Willison · Nov 24, 16:53

**Background**: GPT-6.2 Astra is an OpenAI frontier model released on November 17, 2026 alongside the more efficient GPT-6.2 Sol; OpenAI positions Astra for the hardest projects, including browsing and computer use. Autonomous agents are systems that pursue goals by sensing an environment and taking actions with minimal human input, which is the mode Humphries describes. The 1808 sketchbook is held at Yale's Beinecke Library and has been digitized, and "Deep Blue" refers to IBM's chess computer that beat Garry Kasparov in 1997, a shorthand for machines surpassing humans in a domain.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-2-astra-sol/">Introducing GPT-6.2 Astra and Sol | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Autonomous_agent">Autonomous agent - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI research agents`, `#LLM applications`, `#autonomous agents`, `#historical research`, `#GPT-6.2`

---

<a id="item-8"></a>
## [VMware vCenter hit by another 9.8-rated authentication bypass, already exploited as a zero-day](https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html) ⭐️ 8.0/10

Broadcom released patches for 23 VMware vulnerabilities, headlined by CVE-2026-123903, a 9.8-rated authentication bypass in vCenter's VMware Directory Service (vmdir) that lets anyone with network access to vCenter skip authentication and gain unauthorized access. The flaw had already been exploited in the wild as a zero-day in the days before the fix was published. vCenter is the central control plane for VMware virtualized estates, so an unauthenticated bypass there can expose every managed ESXi host, virtual machine and stored credential in a datacenter. Because exploitation has already been observed and no credentials are required, defenders running vCenter — including many enterprise and government environments — need to patch immediately rather than wait for a routine maintenance window. The vulnerability resides in vmdir and, per Broadcom's advisory, is exploitable by a malicious actor with network access to vCenter; the fix shipped as part of a batch of 23 VMware patches rather than a standalone release. It is also the latest in a string of vCenter authentication bypasses disclosed in 2026 — including CVE-2026-123890 and the earlier CVE-2026-59309 — which suggests attackers are actively mining the same attack surface.

telegram · zaihuapd · Nov 24, 14:50

**Background**: vCenter Server is VMware's management platform for virtual infrastructure: administrators use it to configure ESXi hosts, provision virtual machines, manage clusters and handle single sign-on, so compromising it is roughly equivalent to compromising the whole virtualization estate. The VMware Directory Service (vmdir) is the LDAP-based directory behind vCenter's embedded identity system (for example the vsphere.local domain) and underpins authentication and SSO, which makes it a high-value place to look for authentication bypasses. An authentication bypass is a flaw that lets an attacker skip the login check entirely rather than steal a password, and a zero-day is a vulnerability exploited before the vendor had a patch available — hence the urgency of this disclosure. CVSS 9.8 is in the 'critical' band and indicates a remotely reachable, low-complexity, unauthenticated issue.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html">VMware vCenter Hit by Another Critical 9.8-Rated Auth Bypass ...</a></li>
<li><a href="https://www.rapid7.com/blog/post/etr-cve-2026-123890-critical-authentication-bypass-vmware-vcenter/">CVE-2026-123890: Critical Authentication Bypass in VMware vCenter</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zero-day_exploit">Zero-day exploit</a></li>
<li><a href="https://knowledge.broadcom.com/external/article/326305/how-to-export-vmdir-information-from-vce.html">How to export VMDir information from vCenter Server Appliance</a></li>

</ul>
</details>

**Tags**: `#security`, `#vmware`, `#vcenter`, `#vulnerability`, `#zero-day`

---

<a id="item-9"></a>
## [Leaked GTA 6 Xbox Build Boots on Windows via Wine-Style Recompilation](https://twitter.com/raul_bs3/status/2125213756238291075) ⭐️ 7.0/10

Community reverse-engineering projects, notably xcl and Victory, have reportedly gotten the leaked Xbox build of GTA 6 running on Windows PCs using Wine-like recompilation and compatibility techniques. The work was surfaced in a post that drew roughly 290 points and 367 comments, with commenters describing it as a real, if rough, compatibility effort rather than a hoax. The feat demonstrates how thin the boundary between modern Xbox consoles and Windows PCs has become, lowering the technical barrier to unofficial native ports of console exclusives. It also sharpens the legal and business questions facing publishers, since a leaked, unprotected binary can be made playable on PC long before any official port ships. According to commenters, the leaked Xbox binary carries no special DRM or obfuscation, so the hard problems are compatibility shims and graphics translation rather than code protection. The projects take a Wine-like approach, and analogous research such as Xbox2Windows translates selected x64 machine code into C++ and gfx1013 shaders into desktop DXIL.

hackernews · andrem · Nov 24, 13:19 · [Discussion](https://news.ycombinator.com/item?id=50627783)

**Background**: Static recompilation is a reverse-engineering technique that translates a game's original machine code into C or C++ source, which is then compiled into a native executable for another platform; it differs from emulation because no interpreter runs at play time. Wine, by contrast, is a compatibility layer that reimplements Windows APIs so Windows binaries can run on other operating systems. Modern Xbox Series X|S consoles use x64 AMD CPUs and AMD RDNA 2 graphics that closely resemble PC hardware, which is why an Xbox game binary is far easier to bring to Windows than, say, a PlayStation or older console title.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/R0Y00/Xbox2Windows">GitHub - R0Y00/Xbox2Windows: Static recompilation research for...</a></li>
<li><a href="https://www.denis-iakimenko.com/blog/reverse-engineering-decompilation-ports">Reverse Engineering Games — Decompilation and Static ...</a></li>
<li><a href="https://recompendium.com/en/consola/xbox/">Xbox games on PC: recompilations, native ports, and ...</a></li>

</ul>
</details>

**Discussion**: Commenters dug into the technical route: because modern Xbox hardware is close to a PC and the leaked binary has no DRM or obfuscation, the remaining work is mostly compatibility and graphics, as pursued by xcl and Victory. Others debated the fallout — one camp argues this will not seriously harm game production given GTA 6's enormous profitability and inevitable official PC port, while another worries about a future where games keep critical components in the cloud specifically to prevent decompilation.

**Tags**: `#game-reverse-engineering`, `#compatibility-layers`, `#wine`, `#recompilation`, `#gta-6`

---

<a id="item-10"></a>
## [Songe: an open-source engine that trains local LLM agents on idle compute](https://github.com/sous-labs/songe) ⭐️ 7.0/10

Songe, a GitHub project under the sous-labs organization, is a training engine that aims to continuously improve local LLM agents by putting a machine's otherwise idle compute to work. Rather than being a model or a runtime, it positions itself as the training layer that sits alongside an agent you already run locally. Most local agent setups today are static: you download a model, run it through something like Ollama, and it never learns from its own failures. If a lightweight, background training loop can work on consumer hardware, it would let hobbyists and small teams improve agents without renting cloud GPUs, feeding directly into the broader research push toward self-improving agentic systems. The repository is early-stage and currently offers little public detail: there are no published benchmarks, no stated hardware requirements, and the documentation does not yet spell out how improvement is measured or which training method (fine-tuning, preference optimization, or replay-based correction) is used. The framing of "idle compute" also implies training runs in the background over hours or days rather than in a single burst.

hackernews · bluepeter · Nov 24, 15:03 · [Discussion](https://news.ycombinator.com/item?id=50629231)

**Background**: A local LLM agent is a system that runs an LLM entirely on your own machine — typically through a runtime such as Ollama or llama.cpp — and uses it to call tools, edit files, or control the computer. Because the model weights live on your disk, you can in principle fine-tune or otherwise adapt them yourself, which is what a "training engine" like Songe is for. The general idea behind such self-improvement loops is to capture an agent's mistakes or successes, turn them into training signal, and feed them back so the model handles similar situations correctly next time. Historically this has meant dedicated GPU time and machine-learning expertise, so the pitch of doing it opportunistically on spare cycles is the novel part.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/sous-labs/songe/tree/main/.github">songe/.github at main · sous-labs/songe · GitHub</a></li>
<li><a href="https://githubsignals.io/repo/sous-labs/songe/">sous-labs/songe — GitHub Signals</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2026/06/self-improving-loops/">Self-Improving Loop: How to Build AI Agents That Actually Learn</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were interested but skeptical, drawing 182 points and 59 comments. Several asked for concrete numbers — how much improvement to expect from a weekend of training or per "dream epoch" — while others wanted a transcribed example of how the system judges improvement and whether it learns from self-corrections or user corrections. One commenter asked whether it would work on a modest, GPU-less Windows machine running a small Qwen model via Ollama, and another floated the idea of a SETI@home-style distributed version.

**Tags**: `#local-llm`, `#training-engine`, `#idle-compute`, `#open-source-tools`, `#agent-self-improvement`

---

<a id="item-11"></a>
## [Flame Graphs and Deterministic VMs Debated for Performance Analysis](https://fzakaria.com/2026/11/12/worshipping-at-the-altar-of-brendan-gregg) ⭐️ 7.0/10

A technical blog post published on November 12, 2026, and the ensuing Hacker News discussion re-examined flame graphs and deterministic virtual machines as tools for performance analysis, with commenters challenging their usefulness for multithreaded and asynchronous systems. Flame graphs are a default visualization for CPU profiling, so their blind spots for cross-thread dependencies and asynchronous critical paths can mislead engineers debugging high-throughput services; the discussion points toward record-replay, tracing, and request-context approaches as complements. Commenters noted that the deterministic VM under discussion is single-threaded, which may limit fidelity for highly concurrent pipelines, and they compared it with rr record-and-replay; others asked how such analysis could recover the critical path of C++ coroutines, fibers, or futures without embedding request context in framework code.

hackernews · kqr · Nov 24, 10:50 · [Discussion](https://news.ycombinator.com/item?id=50626413)

**Background**: Flame graphs, invented by Brendan Gregg, visualize sampled stack traces: each rectangle is a stack frame and its width reflects how often that frame appeared in samples, not elapsed time. Deterministic virtual machines and record-replay systems aim to make execution reproducible so that performance problems and bugs can be re-run and inspected reliably; Antithesis and rr are examples cited in the thread.

<details><summary>References</summary>
<ul>
<li><a href="https://www.brendangregg.com/flamegraphs.html">Flame Graphs - Brendan Gregg Analyze Java performance on Arm servers using flame graphs Flamegraph handles multi-thread program abnormality Generate Java flame graphs using async-profiler | Arm ... What Is Flamegraph? Definition & Examples - nhimg.org Java Async Profiler Flame Graph - Stack Overflow</a></li>
<li><a href="https://dl.acm.org/doi/10.1145/2007477.1952686">Performance profiling of virtual machines | ACM SIGPLAN Notices</a></li>

</ul>
</details>

**Discussion**: The thread was broadly interested in deterministic VMs and reproducible analysis, but several commenters were skeptical of flame graphs for multithreaded work and worried that a single-threaded VM would miss cross-thread effects. Others drew parallels to rr and Antithesis, asked about async critical-path analysis, and discussed Nvidia's 'speed of light' performance culture plus sleep/stall profiling trade-offs.

**Tags**: `#performance-analysis`, `#flamegraphs`, `#deterministic-vm`, `#observability`, `#systems-profiling`

---

<a id="item-12"></a>
## [Blogger argues closed LLM agents serve their vendors, not their users](https://michaelharley.net/posts/2026/11/01/llm-agents-work-for-their-parent-companies-not-for-you/) ⭐️ 7.0/10

A blog post on michaelharley.net argues that closed LLM agents ultimately answer to their parent companies' policies rather than to the people paying for them, illustrated by an anecdote in which Claude refuses to work around Bandcamp's bot restrictions but will still download a YouTube song. The post drew 912 points and 386 comments on Hacker News, making it one of the more heated AI-policy debates of the week. The piece touches a core tension in the agent ecosystem: users want an agent that acts as a loyal delegate, while vendors must enforce usage policies, honor site terms of service and manage legal and reputational risk. How this is resolved will shape what commercial agents are permitted to do on the open web, and will influence trust, adoption and the emerging regulatory conversation around agent duties. The concrete example contrasts two refusals/acceptances that critics call inconsistent: respecting Bandcamp's explicit anti-LLM wishes while still fetching a YouTube track that sends no money to the artist. Commenters also note that a model that ignored site rules whenever a user asked would likely face blocking, legal action and reduced usefulness in the long run.

hackernews · surprisetalk · Nov 24, 12:40 · [Discussion](https://news.ycombinator.com/item?id=50627340)

**Background**: LLM agents are systems that wrap a language model with tool access and planning so they can browse the web, call APIs and complete multi-step tasks on a user's behalf. Because these agents act autonomously, the question of whose instructions they follow — the user's, the model vendor's usage policy, or the target website's terms of service — becomes practically important. 'AI alignment' in this context refers to steering such systems toward the goals and constraints their makers and users actually intend, and some commenters propose borrowing the fiduciary-duty standard that lawyers, doctors and financial advisers owe their clients.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_alignment">AI alignment - Wikipedia</a></li>
<li><a href="https://developer.nvidia.com/blog/building-your-first-llm-agent-application/">Building Your First LLM Agent Application | NVIDIA Technical Blog</a></li>
<li><a href="https://terms.law/Trading-Legal/guides/ai-fiduciary-duty.html">AI Fiduciary Duty: SEC Robo-Adviser Compliance | Terms.Law</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread is polarized: several commenters defend the refusals as correct, arguing that scraping Bandcamp against its terms of service is clear-cut and that a 'free-for-all' agent internet would be far spammier and scammier. Others call the author's argument flimsy and self-serving, while one commenter (Lerc) proposes legally requiring AI advisers to act in their client's best interest, subject to the same no-lawbreaking limits as legal, financial and medical advisers, and never to claim they act for a non-client.

**Tags**: `#LLM agents`, `#AI alignment`, `#AI policy`, `#terms of service`, `#web scraping`

---

<a id="item-13"></a>
## [GTA 6 'Leonida' PC Recompilation Project Taken Down From GitHub](https://github.com/ItsNotRexed/Leonida/issues) ⭐️ 7.0/10

The community-driven 'Leonida' project, which was statically recompiling the Xbox Series X build of GTA 6 into a native PC executable, was taken down from GitHub while its lead developer was at school. The removal follows a prior Hacker News discussion of the project and has become a flashpoint over AI-assisted reverse engineering. It shows how quickly LLM-assisted reverse engineering can turn a console-exclusive title into a playable PC build, undercutting the value of timed platform exclusivity. The takedown also tests how far rights holders are willing to go against community recompilation projects that never distribute game assets. Leonida was an open-source static recompilation framework targeting the leaked GTA 6 Xbox Series X build (Build 1.0.2.1), translating RAGE engine console code into native x86-64 PC binaries rather than emulating it. Because no copyrighted assets were hosted, such projects typically only require users to own the original game files, and GitHub removals of this type are usually the result of a DMCA notice from the rights holder.

hackernews · smuhakg · Nov 24, 02:08 · [Discussion](https://news.ycombinator.com/item?id=50622638)

**Background**: Static recompilation is a technique that converts a console game's machine code directly into native code for another platform, producing a port that runs without an emulator. Historically this required years of manual effort and deep familiarity with the target engine, but recent LLM-based tools have dramatically accelerated decompilation and reverse engineering work — one community catalog counts 151 static recompilations among 300 AI-assisted projects, with Claude used in 275 of them. Rockstar's parent company Take-Two is known for aggressively enforcing its intellectual property, making any GTA-related reverse engineering effort legally risky.

<details><summary>References</summary>
<ul>
<li><a href="https://gta6recomp.com/leonida">Leonida — GTA 6 PC Static Recompilation Project Tracker & Source</a></li>
<li><a href="https://www.retroreversing.com/source-code/decompiled-retail-console-games">Decompiled Retail Console Games - Retro Reversing ...</a></li>
<li><a href="https://reversedwithai.com/ai-game-decompilation">AI reverse engineered games : decompiled and ported with AI</a></li>

</ul>
</details>

**Discussion**: Commenters were split but largely sympathetic to the project: several said they would gladly pay for the game yet refuse to buy a €500+ console just to play it, and one predicted the port will be pirated by people who would otherwise have bought it on Steam. Others expressed astonishment at how fast LLMs made this feasible, with one developer admitting they had dismissed the idea as a massive multi-year undertaking, and several argued that holding back PC releases now looks anachronistic.

**Tags**: `#reverse-engineering`, `#game-preservation`, `#AI-assisted-development`, `#platform-exclusivity`, `#github-takedown`

---

<a id="item-14"></a>
## [Developer alleges T3 Code turns on telemetry by default and reads local Codex and Claude credentials](https://x.com/realchendahuang/status/2125153472450527440) ⭐️ 7.0/10

On November 24, X user @realchendahuang alleged that Theo's T3 Code has shipped with PostHog telemetry enabled by default since PR #174 was merged in March, and that PR #21506 (merged in October) reads ~/.codex/auth.json and ~/.claude.json and uploads unsalted SHA-256 hashes of the Codex user_id and Claude accountUuid together with a device ID. The thread includes code references, but neither Theo nor the project has responded. If accurate, a widely discussed AI coding tool is quietly collecting identifiers derived from other vendors' developer tools, which would raise serious consent and supply-chain concerns for anyone running Codex or Claude Code locally. It also fuels the broader debate over how AI developer tools should handle telemetry and cross-tool credential access by default. The claim is that only unsalted SHA-256 hashes of the identifiers are uploaded, but unsalted hashing is pseudonymization rather than anonymization: stable per-user hashes stay linkable across events and can be matched back if the original ID space is enumerable. The poster also says four pull requests attempting to turn telemetry off were rejected, and that official documentation admits relay diagnostic tracking on browser and mobile cannot be disabled; the allegation remains a single unverified social-media claim.

telegram · zaihuapd · Nov 24, 10:58

**Background**: PostHog is an open-source product-analytics platform that many developer tools embed to collect usage events such as feature adoption and crash reports. Codex stores its login session in ~/.codex/auth.json and Claude Code uses ~/.claude.json, so these files hold authentication material and account identifiers rather than plain passwords, making any library that reads them security-sensitive. Hashing identifiers before upload is a common privacy practice, but its strength depends heavily on whether a salt is used. T3 Code is an AI coding tool released by developer and content creator Theo, and its source is developed publicly through pull requests.

<details><summary>References</summary>
<ul>
<li><a href="https://posthog.com/docs/product-analytics/privacy">Privacy controls - Docs - PostHog</a></li>
<li><a href="https://aicodewith.ai/zh/blog/codex-auth-json">Codex auth . json 是什么：位置、风险与安全排错 | AI Code With</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#telemetry`, `#AI developer tools`, `#security`, `#open source governance`

---

<a id="item-15"></a>
## [Huawei and Qualcomm Sign Broad Multi-Year Patent Cross-License Covering 5G and AI](https://t.me/zaihuapd/45344) ⭐️ 7.0/10

Huawei officially announced a multi-year, broad patent cross-licensing agreement with Qualcomm covering both companies' patent portfolios in 5G, computing, artificial intelligence and networking, under which Qualcomm will also purchase some of Huawei's US patents. According to Bloomberg, citing a Huawei spokesperson, Qualcomm additionally agreed to take a license to Huawei's patents related to "logic folding" chip manufacturing technology, and the deal will close after required regulatory approvals. The deal formalizes IP relations between two of the largest holders of wireless standard-essential patents, lowering litigation risk and giving Qualcomm access to Huawei's chip manufacturing-related IP. It also strengthens Huawei's fast-growing licensing business, which the company says has been revenue-positive since 2021, and signals that Huawei remains a central player in global 5G and AI patent licensing despite US restrictions. Huawei said that once the transaction closes, the cumulative expected contract value of its patent licensing agreements will exceed US$6.9 billion (about 46.302 billion yuan), and the agreement still requires regulatory approval before taking effect. The specific royalty rates, payment schedule, and which US patents Qualcomm is buying were not disclosed.

telegram · zaihuapd · Nov 24, 11:38

**Background**: Patent cross-licensing lets two companies use each other's patented technology without separate royalty negotiations, and is common among major 5G players who each hold standard-essential patents (SEPs) that anyone implementing 5G must license on fair, reasonable and non-discriminatory (FRAND) terms. Huawei has run a formal IP licensing program since 2021, collecting royalties from handset makers, while Qualcomm's licensing arm is a major profit center. "Logic folding" (逻辑折叠) is a term Huawei has used in marketing for its recent Kirin chip designs, generally associated with advanced packaging and stacked chip architectures that boost performance without relying solely on smaller process nodes.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ithome.com/1/031/517.htm">华为 Mate X8 大 折 旗舰机发布：麒麟 9050 Pro...</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#Qualcomm`, `#patent-licensing`, `#5G`, `#AI`

---

<a id="item-16"></a>
## [SpaceX and Tesla Boards Form Special Committees to Weigh Merger](https://t.me/zaihuapd/45351) ⭐️ 7.0/10

The boards of SpaceX and Tesla have each set up special committees made up of independent directors to evaluate a possible merger between the two companies. Elon Musk said the committees were formed at shareholders' request and that he will not take part in the discussions because of his conflict of interest, and he stressed that no deal terms have been agreed. A tie-up would combine the world's most valuable private rocket company with the largest US electric-vehicle maker, concentrating Musk's business empire and reshaping the space, EV and AI-robotics landscape. Because Tesla is publicly traded, any deal would require approval from a majority of all Tesla shareholders, making it a landmark case for corporate governance and conflicted-controller transactions. Musk backs the merger concept but says it is far from certain and will ultimately need shareholder support. Approval is expected to be relatively easy on the SpaceX side, whereas Tesla requires a 50% affirmative vote of all shareholders, a notably higher bar than a simple majority of votes cast.

telegram · zaihuapd · Nov 25, 00:41

**Background**: A special committee of independent directors is a standard governance mechanism used when a company considers a transaction involving insiders, such as a controlling shareholder or CEO, so that conflicted parties are excluded from negotiations. Musk is both CEO and a major shareholder of Tesla, a publicly listed company, and CEO and a major holder of SpaceX, which remains privately held, so the same person sits on both sides of any potential deal. Tesla's charter and Delaware-style corporate norms typically require independent review and, in some deals, supermajority or majority-of-all-shares approval to protect minority investors.

**Tags**: `#SpaceX`, `#Tesla`, `#merger`, `#Elon Musk`, `#corporate governance`

---

<a id="item-17"></a>
## [Anthropic shares fall below $83 IPO price, stirring AI economics debate](https://www.bloomberg.com/news/articles/2026-11-24/anthropic-breaks-below-83-ipo-price-in-premarket-trading) ⭐️ 6.0/10

Anthropic's stock dropped below its $83 IPO price in premarket trading, according to Bloomberg, putting the AI lab's shares underwater relative to where they were priced at listing. The decline became a flashpoint on Hacker News, where a 692-comment thread dissected AI business economics rather than the company's technology. When a leading frontier AI lab trades below its offer price, it tests the widely held assumption that being at the technological frontier automatically translates into strong equity returns, and it can ripple into how employees, late-stage investors and competitors value AI companies. It also matters because AI capital spending is increasingly justified by expected returns, so public-market skepticism about one lab can color the whole sector's fundraising and valuation story. The Bloomberg article itself is thin on technical or financial substance, so most of the value comes from the discussion: one commenter reports running a model-agnostic continuous development pipeline on roughly $10k/week, with about 65% of model spend going to Anthropic, and notes the breakdown shifts as new models ship. Others point out that trading below the IPO price is common post-listing behavior, citing Amazon, Netflix, Tesla and Meta as precedents.

hackernews · Betelbuddy · Nov 24, 13:23 · [Discussion](https://news.ycombinator.com/item?id=50627836)

**Background**: An IPO price is the price at which a company first sells shares to public investors; once trading begins, the stock can move freely and frequently dips below that offer price, which is often seen as a symbolic rather than fundamental verdict. Anthropic is a major AI lab competing at the frontier of large language models, a field where training and inference costs are enormous and where customers can switch between vendors' models. Terms like "open weight" refer to models whose trained parameters are publicly downloadable, letting teams self-host instead of paying per-token API fees, which is central to the cost debates in the thread.

<details><summary>References</summary>
<ul>
<li><a href="https://applied-llms.org/">What We’ve Learned From A Year of Building with LLMs – Applied LLMs</a></li>

</ul>
</details>

**Discussion**: Sentiment is mixed. One commenter supplies concrete unit-economics data from a ~$10k/week model-agnostic pipeline that spends roughly 65% on Anthropic, while another argues it is entirely possible for AI to be transformative and hugely profitable yet for Anthropic's stock to still be a bad investment. A bearish voice claims growth is exhausted and the stock should be priced like a legacy automaker (around $10), countered by others who call a post-IPO dip textbook behavior, citing Amazon, Netflix, Tesla and Meta.

**Tags**: `#anthropic`, `#ai-industry`, `#ipo`, `#llm-economics`, `#market-analysis`

---

<a id="item-18"></a>
## [Robin Li Says Open-Source LLMs Add Little Value, Baidu Won't Compete With Developers](https://t.me/zaihuapd/45334) ⭐️ 6.0/10

An internal speech by Baidu CEO Robin Li was leaked, in which he argued that open-sourcing large models has limited value and that closed-source models will maintain a lasting lead in capability, cost, and inference speed. He also said Baidu will not compete with AI developers for their business, positioning the company as a model provider rather than an application maker. The remarks come from the CEO of one of China's largest AI companies and stake out a strongly contrarian position in the ongoing open-versus-closed LLM debate, potentially influencing how Chinese enterprises and developers choose their model stack. They also signal Baidu's intent to build an ecosystem around its proprietary ERNIE models rather than commoditizing them through open weights. Li argued that open-source models are fundamentally different from traditional open-source software such as Linux and Android, claiming that community contributions do not compound into a faster-improving model. He contended that only a profitable closed-source business can fund the compute and talent needed to stay ahead, and that at equal capability a closed model will always have lower inference cost and faster response.

telegram · zaihuapd · Nov 24, 07:32

**Background**: Large language models can be released as open weights, where anyone can download, modify, and self-host them (as with Meta's Llama series), or kept closed behind an API (as with OpenAI's GPT-4 and Baidu's ERNIE Bot). Open models lower entry barriers and let companies control data and deployment, while closed models are argued to offer stronger performance, easier maintenance, and a clearer revenue model for the developer. In China, both camps are active: Alibaba's Qwen and DeepSeek have released open weights, while Baidu has kept its flagship ERNIE models proprietary.

**Tags**: `#LLM`, `#open-source`, `#closed-source`, `#Baidu`, `#AI industry`

---

<a id="item-19"></a>
## [Anthropic CEO Dario Amodei Predicts AI Could Cure Cancer Within 10 Years](https://t.me/zaihuapd/45336) ⭐️ 6.0/10

Anthropic CEO Dario Amodei predicted that advances in AI could turn cancer, Alzheimer's disease, heart disease and mental illness into "relics of the past" within roughly 10 years. The claim arrives alongside concrete activity: Anthropic has recently acquired several biotech startups, disclosed last month that it has launched an internal new-drug-discovery effort, and set up a San Francisco laboratory studying how AI can support fundamental biology research. A leading frontier-AI lab publicly framing drug discovery and disease elimination as its next frontier signals a deepening convergence between AI companies and the pharmaceutical industry, which could reshape R&D timelines and attract new capital and scientific talent into AI-native biotech. It also raises the reputational stakes for Anthropic: such claims invite scrutiny of whether AI-generated biological insight can actually translate into validated medicines. The statement is a forward-looking prediction rather than a peer-reviewed result — no specific pipeline, timelines, or clinical data were disclosed, and the supporting evidence so far consists of acquisitions, an internal drug-discovery program, and a San Francisco research lab. Amodei previously said on X in August that the best way to persuade AI skeptics would be to actually cure cancer, framing the claim as an accountability pledge.

telegram · zaihuapd · Nov 24, 08:54

**Background**: AI drug discovery uses machine-learning models to analyze biological and chemical data — for example predicting protein structures, screening candidate compounds, and prioritizing targets — so that researchers can explore far more hypotheses than lab experiments alone would allow. Well-known efforts include Isomorphic Labs, a drug-discovery company spun out of Google DeepMind under Demis Hassabis, and Recursion, which builds AI-driven drug discovery pipelines. Progress is constrained by the sparsity and noise of biological data, which is why labs such as Biohub argue that better data and models are prerequisites for AI to meaningfully accelerate basic biology.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Isomorphic_Labs">Isomorphic Labs - Wikipedia</a></li>
<li><a href="https://www.recursion.com/">Pioneering AI Drug Discovery | Recursion</a></li>
<li><a href="https://biohub.org/">Biohub - Leading the new era of AI -powered biology</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Anthropic`, `#biotech`, `#drug discovery`, `#healthcare`

---