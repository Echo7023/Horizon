---
layout: default
title: "Horizon Summary: 2026-10-23 (EN)"
date: 2026-10-23
lang: en
---

> From 39 items, 26 important content pieces were selected

---

1. [Quad9 to Exit France After Contempt Fine Over DNS Blocking](#item-1) ⭐️ 8.0/10
2. [eMudhra exits global SSL/TLS certificate business after key compromise](#item-2) ⭐️ 8.0/10
3. [Switch 2 Jailbroken via LLM-Agent-Driven Automated Exploit Research](#item-3) ⭐️ 8.0/10
4. [Faster than Earcut: triangulating 3.7M map polygons in 489 ms](#item-4) ⭐️ 8.0/10
5. [Anthropic Donates Agent Skills Standard to Linux Foundation's Agentic AI Foundation](#item-5) ⭐️ 8.0/10
6. [研究：智能电视关掉内容识别仍在上报](#item-6) ⭐️ 8.0/10
7. [333 Backdoored Tor Exit Relays Pulled Offline After Ebury Infection](#item-7) ⭐️ 8.0/10
8. [Banned Nvidia B300 Servers Reportedly Found in Chinese State-Backed Network](#item-8) ⭐️ 8.0/10
9. [NVIDIA OpenShell: An Open-Source Sandboxed Runtime for AI Agent Fleets](#item-9) ⭐️ 7.0/10
10. [GNU Taler prepares for real-world payment operations in Germany](#item-10) ⭐️ 7.0/10
11. [HackiOS boots iOS 16.5 XNU kernel and user space on Android phones via QEMU](#item-11) ⭐️ 7.0/10
12. [pwn.watch: A Live Tracker for Actively Exploited Security Incidents](#item-12) ⭐️ 7.0/10
13. [WorldTUI: a 360M model trained to hallucinate a working terminal](#item-13) ⭐️ 7.0/10
14. [Carbon-X: an open 14.8B model trained jointly on DNA and text](#item-14) ⭐️ 7.0/10
15. [Frontier audio models struggle to tag ASMR trigger sounds, benchmark finds](#item-15) ⭐️ 7.0/10
16. [Claude API 2026-10-21 Ships, Removing Temperature, Top_p and Top_k](#item-16) ⭐️ 7.0/10
17. [Australian Federal Court Rules Apple and Google Abused Market Power](#item-17) ⭐️ 7.0/10
18. [Tesla begins North American production of the steering-wheel-free Cybercab](#item-18) ⭐️ 7.0/10
19. [miHoYo and Tsinghua Open-Source GameScaling Game Control Models](#item-19) ⭐️ 7.0/10
20. [Oracle Issues Critical Security Alert for CVE-2026-91403 in Java SE JSSE](#item-20) ⭐️ 7.0/10
21. [China Proposes Export Controls on 40 AI, Biotech and Solar Technologies](#item-21) ⭐️ 7.0/10
22. [Woman Faces Six Years in Prison Over Fraudulent Cash App Account](#item-22) ⭐️ 6.0/10
23. [Hacker News user apologizes for unintentionally breaking PHP RCE embargo](#item-23) ⭐️ 6.0/10
24. [Arc browser sunset as Atlassian-owned Browser Company pivots to Dia](#item-24) ⭐️ 6.0/10
25. [WhissleAI shrinks steerable TTS to 11.84 MB with int4 quantization](#item-25) ⭐️ 6.0/10
26. [XPeng IRON runs second-gen VLA on-device, re-reasoning every 0.2 seconds](#item-26) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Quad9 to Exit France After Contempt Fine Over DNS Blocking](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

Quad9, the privacy-focused public DNS resolver, announced it is withdrawing its service from France after a French court held it in contempt and fined it for failing to fully comply with a music-industry blocking order. The case arose because Sony Music Entertainment GmbH used a VPN from Germany to reach content that Quad9 had blocked only for French IP addresses, which the court treated as noncompliance. The withdrawal is a significant precedent for internet governance: it shows that DNS-level copyright blocking orders can be effectively unenforceable when rights holders themselves circumvent geo-blocking, yet intermediaries still bear the legal risk. It also signals that major global resolvers may abandon entire national markets rather than accept selective censorship obligations, leaving users in those countries with fewer neutral DNS options. Quad9 says it will likely apply geoIP filtering to block French users from its resolvers after November 24, and its CTO John Todd acknowledged the awkward tension of using geoIP blocking for country-level exclusion while arguing the same technique is inadequate for selectively blocking individual domain names. The dispute began with a Sony Music blocking order; Quad9 had responded by denying resolution of the blocklisted names only to French users rather than globally.

hackernews · farrokhi · Oct 22, 14:32 · [Discussion](https://news.ycombinator.com/item?id=50195959)

**Background**: DNS resolvers are the internet's lookup service, translating domain names into IP addresses; Quad9 operates a free public resolver known for blocking malware domains and for a charter that prioritizes user privacy. Rights holders in France, notably Canal+ and Sony Music, have obtained court orders requiring ISPs and DNS operators to block piracy- and copyright-related domains. Geo-blocking, which restricts access based on the IP address's apparent country, is a common but brittle control, since VPNs and proxies allow users to appear to be located elsewhere.

<details><summary>References</summary>
<ul>
<li><a href="https://quad9.net/">Quad 9 | A public and free DNS service for a better security and privacy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Geo-blocking">Geo-blocking</a></li>
<li><a href="https://internet.exchangepoint.tech/stifling-speech-through-dns-infrastructure/">Stifling Speech Through DNS Infrastructure</a></li>

</ul>
</details>

**Discussion**: Commenters were largely sympathetic to Quad9 and critical of the ruling, with one comparing DNS resolvers being fined to punishing a phone book for listing a criminal's number, and another noting that the plaintiff itself defeated the protection via VPN yet Quad9 was still held liable. Several drew parallels to Cisco's earlier exit from the French market following Canal+ blocking injunctions against Google, Cloudflare and Cisco, and one suggested resolvers should stop resolving domains belonging to companies that sue them.

**Tags**: `#DNS`, `#internet-privacy`, `#copyright-enforcement`, `#geo-blocking`, `#internet-governance`

---

<a id="item-2"></a>
## [eMudhra exits global SSL/TLS certificate business after key compromise](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 8.0/10

Indian certificate authority eMudhra (which operates under the emSign brand) announced it is withdrawing from the global SSL/TLS certificate authority business after eight of its intermediate CA private keys were found to be fatally weak and were distrusted by browser vendors. The compromised keys were P-384 keys generated in April 2025 whose actual values were smaller than 256, meaning anyone could recover them by testing just 256 possible numbers. This is a full-blown public trust failure in the Web PKI: a CA trusted by all major browsers effectively issued certificates whose private keys could be brute-forced in milliseconds, so anyone could have forged browser-trusted certificates for any domain. Mozilla, Google and Apple all moved to block the affected certificates, and Cloudflare is notifying customers still using them to avoid breakage. The flaw was a cryptographic defect during certificate generation: the keys were nominally P-384 but had such small numeric values that recovery required only a 256-guess search, which security researchers and Mozilla's incident report confirmed publicly. eMudhra's press release notably blames "social media amplification" for scrutiny "out of proportion to SSL/TLS's place in our business" rather than explaining how the keys were generated, and it claims no end-entity certificates were issued from the affected CAs — a claim commenters find dubious since anyone with the private keys could issue certificates.

hackernews · bo0tzz · Oct 22, 13:33 · [Discussion](https://news.ycombinator.com/item?id=50195110)

**Background**: A certificate authority (CA) is the entity that signs the digital certificates browsers rely on to verify that a website is who it claims to be. Trust in the Web PKI is hierarchical: a root certificate is embedded in browsers and operating systems, and it delegates authority to intermediate CAs, which actually issue site certificates. If an intermediate CA's private key leaks or is guessable, attackers can mint valid-looking certificates for any domain, which is why browsers enforce strict incident reporting rules — as they did with the WoSign case — and can remove a CA from their trust stores entirely.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/mozilla-google-apple-block-compromised-emudhra-ca-certificates/">Mozilla , Google, Apple block compromised eMudhra CA certificates</a></li>
<li><a href="https://unit42.paloaltonetworks.com/emudhra-certificate-compromise/">EMudhra Intermediate CA Certificates Compromised</a></li>
<li><a href="https://blog.cloudflare.com/emudhra-certificate-compromise/">8 eMudhra certificates are compromised. | Cloudflare Blog</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters (838 points, 586 comments) were scathing: one noted the scrutiny is "inversely proportional to bit complexity of the private keys they used," while another joked that the RSA private key is literally just the number 4. Others highlighted the brutal question battery the Chrome team publicly filed on Mozilla's Bugzilla, and several ridiculed the press release's claim that no end-entity certificates were issued "given that anyone can issue certificates out of the affected CAs."

**Tags**: `#security`, `#TLS/PKI`, `#certificate-authority`, `#incident-response`, `#hackernews-discussion`

---

<a id="item-3"></a>
## [Switch 2 Jailbroken via LLM-Agent-Driven Automated Exploit Research](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 8.0/10

Developer pepsipu published a technical write-up on ns2jb, a software-only, tethered jailbreak for the Nintendo Switch 2 that reportedly runs arbitrary native code on the latest firmware, including version 23.0.1. The account is notable for using Codex LLM agents with JetKVM hardware and a Bluetooth-controlled power-button presser to automate exploit research. If confirmed, this is the first software-only jailbreak for Nintendo's newest console, opening the door to homebrew, game dumping, and recompilation projects that could bring console exclusives to arbitrary hardware. Its LLM-plus-KVM workflow also signals a broader shift toward agentic automation in hardware security research. The exploit is a userland, software-only, tethered jailbreak, meaning it does not persist across reboots and needs an external host-assisted launch. The automation rig uses JetKVM to send controller inputs over USB and capture HDMI video, Codex to drive experimentation, and a SwitchBot Bot to physically press the power button after crashes.

hackernews · ledoge · Oct 22, 08:01 · [Discussion](https://news.ycombinator.com/item?id=50192536)

**Background**: The Nintendo Switch 2 is Nintendo's latest game console, and like its predecessor it uses a locked-down boot chain and signed code to block unofficial software. A jailbreak is an exploit chain that bypasses those restrictions to run unsigned native code, enabling homebrew and, controversially, game dumping. JetKVM is a hardware KVM-over-IP device that gives software remote keyboard/controller input and HDMI capture, while LLM agents are increasingly being studied as tools for automated vulnerability discovery and exploitation.

<details><summary>References</summary>
<ul>
<li><a href="https://gbatemp.net/news/switch-2-jailbreak-ns2jb-released-software-only-exploit-tethered.685698/">Switch 2 jailbreak "ns2jb" released. Software-only exploit , tethered</a></li>
<li><a href="https://wccftech.com/nintendo-switch-2-hacked-jailbreak/">The Nintendo Switch 2 Has Been Hacked, As First Jailbreak Blows...</a></li>
<li><a href="https://www.emergentmind.com/papers/2404.08144">LLM Agents Exploit One-day Vulnerabilities</a></li>

</ul>
</details>

**Discussion**: Commenters were impressed by the achievement and the LLM-plus-KVM automation, with some predicting Switch 2 game dumps and recompiled exclusives could appear quickly. Others argued that manufacturers should be required to release jailbreak tools after a fixed period, such as ten years, while one commenter questioned why Codex often refuses security-research requests and another identified the Bluetooth power-button device as a SwitchBot Bot.

**Tags**: `#security`, `#hardware-hacking`, `#jailbreak`, `#LLM-agents`, `#reverse-engineering`

---

<a id="item-4"></a>
## [Faster than Earcut: triangulating 3.7M map polygons in 489 ms](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 8.0/10

A new technical write-up presents a triangulation library—referred to in the HN discussion as Earstrip—that processes 3.7 million map polygons in 489 ms, claiming faster performance than Mapbox's Earcut. The post is backed by benchmark data and a published polygon corpus for comparison. Mapping and GIS applications depend on fast polygon triangulation to drive WebGL rendering and spatial analysis, so performance at the million-polygon scale can directly affect the cost of rendering large vector maps. The result also feeds into the broader debate over which triangulation algorithm geometry libraries should choose. The discussion notes that Earcut deliberately rejects some optimizations to keep its bundle at roughly 4.1 KB min+gzip and does not guarantee a correct triangulation on arbitrary input. The author also published the polygon datasets, enabling comparisons with alternatives such as Delaunay32.

hackernews · molind · Oct 22, 09:31 · [Discussion](https://news.ycombinator.com/item?id=50193170)

**Background**: Polygon triangulation is the process of decomposing a polygon into triangles so GPUs and geometry pipelines can render or analyze it. Ear clipping is a simple, widely used method—and the basis of Mapbox's Earcut—that repeatedly removes 'ears' from a polygon; it is easy to implement but can be slow on complex shapes and needs special handling for holes. Alternatives include Seidel's trapezoidal method and constrained Delaunay triangulation, which offer different tradeoffs in asymptotic complexity, triangle quality, and support for holes.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/mapbox/earcut">GitHub - mapbox/ earcut : The fastest and smallest JavaScript polygon ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Polygon_triangulation">Polygon triangulation - Wikipedia</a></li>
<li><a href="https://gwlucastrig.github.io/TinfourDocs/DelaunayIntroCDT/index.html">Constrained Delaunay</a></li>

</ul>
</details>

**Discussion**: The HN thread was substantive: Earcut author mourner thanked the author and said he might borrow tricks, while explaining that Earcut rejects some optimizations to keep its bundle near 4.1 KB min+gzip. Delaunay32 author morishuz asked how the divide-and-conquer constrained Delaunay approach would compare, and another commenter questioned why ear clipping dominates over Seidel's trapezoidal method given its near-linear complexity and natural hole handling. One commenter also pointed to Quake's Triangle as a classic triangulator.

**Tags**: `#triangulation`, `#computational-geometry`, `#gis`, `#performance`, `#algorithms`

---

<a id="item-5"></a>
## [Anthropic Donates Agent Skills Standard to Linux Foundation's Agentic AI Foundation](https://simonwillison.net/2026/Oct/22/donating-agent-skills/) ⭐️ 8.0/10

Anthropic announced it is donating its Agent Skills standard to the Agentic AI Foundation (AAIF), the Linux Foundation-hosted body it co-founded with Block and OpenAI, and to which it had previously donated the Model Context Protocol (MCP). The company framed the move as a commitment to keeping Agent Skills open, community-driven and vendor-neutral, and the format is now documented as an open standard at agentskills.io. Handing a proprietary-origin format to neutral governance makes it far easier for competing agent products to adopt it without ceding control to a single vendor, which is exactly what happened with MCP. If Agent Skills follows the same trajectory, it could become the de facto packaging format for portable agent capabilities across the whole ecosystem. The Agent Skills format was originally developed by Anthropic, released as an open standard, and has since been adopted by a growing number of agent products, with the specification now open to contributions from the broader ecosystem. This is a governance announcement rather than a technical change: the donation itself does not alter the specification's contents, and details such as how much decision-making authority Anthropic retains within AAIF were not spelled out in the announcement.

rss · Simon Willison · Oct 22, 18:09

**Background**: Agent Skills is a format for packaging reusable instructions and resources so that AI agents can load and perform specific tasks, rather than each vendor inventing its own scheme. MCP, which Anthropic open-sourced earlier, is a universal standard for connecting AI applications to external data sources, tools and workflows. The Agentic AI Foundation is an open-source initiative hosted by the Linux Foundation, announced on December 9, 2025, to give agentic AI projects neutral governance; founding contributions reportedly include OpenAI's AGENTS.md specification alongside Anthropic's MCP.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation">Donating Agent Skills to the Agentic AI Foundation \ Anthropic</a></li>
<li><a href="https://agentskills.io/home">Agent Skills Overview - Agent Skills</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agentic_AI_Foundation">Agentic AI Foundation</a></li>

</ul>
</details>

**Tags**: `#Agent Skills`, `#Agentic AI Foundation`, `#Anthropic`, `#MCP`, `#open standards`

---

<a id="item-6"></a>
## [研究：智能电视关掉内容识别仍在上报](https://watchingthewatchers.github.io/watchingthewatchers/index.html) ⭐️ 8.0/10

A study of 12 smart TVs from 10 vendors found that some devices continue reporting content-recognition data even after ACR is disabled, with VIDAA OS and Vizio WatchFree+ exposing viewing information via unencrypted channels.

telegram · zaihuapd · Oct 22, 09:50

**Tags**: `#privacy`, `#smart TV`, `#ACR`, `#IoT security`, `#data leakage`

---

<a id="item-7"></a>
## [333 Backdoored Tor Exit Relays Pulled Offline After Ebury Infection](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

A Tor operator ran a scripted scan of roughly 3,000 exit relays and found 333 of them — about 10% — infected with the Ebury OpenSSH backdoor, which redirected SSH connections on port 22 to one of 12 interception servers to harvest credentials. All 333 were assigned the BadExit flag on October 4 and went offline the following day. Exit relays are the single point where Tor traffic leaves the anonymity network, so a roughly 10% compromise rate means any Tor user could have had SSH logins silently captured without any misconfiguration on their side. The incident also shows how a supply-chain-style compromise of privacy infrastructure can be used for broad credential theft rather than targeted attacks. Compromised relays forwarded ordinary encrypted web traffic normally but diverted port-22 SSH sessions to the 12 interception servers, and some ports were blocked so the attackers could preferentially collect unencrypted mail traffic; the initial intrusion vector is still undetermined. The activity was noticed after an SSH connection triggered a "REMOTE HOST IDENTIFICATION HAS CHANGED" warning, and users who clicked through that changed host key may have exposed their passwords.

telegram · zaihuapd · Oct 22, 14:52

**Background**: Ebury is an OpenSSH backdoor and credential stealer associated with the Windigo group and seen since 2009; it typically works by modifying shared libraries (.so files) loaded by the legitimate OpenSSH binary, so the sshd process looks normal while silently capturing credentials and redirecting connections. Tor exit relays are the volunteer-run servers that carry traffic from the Tor network out to the open internet; when a relay is found malicious, directory authorities assign it the BadExit flag, which effectively turns it into a non-exit so clients stop routing traffic through it.

<details><summary>References</summary>
<ul>
<li><a href="https://attack.mitre.org/software/S0377/">Ebury, Software S0377 | MITRE ATT&CK®</a></li>
<li><a href="https://archive.torproject.org/websites/support.torproject.org/relay-operators/what-is-the-bad-exit-flag/">What is the BadExit flag ? | Tor Project | Support</a></li>
<li><a href="https://cybersecuritynews.com/hackers-hijack-333-tor-exit-nodes/">Hackers Hijack 333 Tor Exit Nodes to Intercept SSH Logins and ...</a></li>
<li><a href="https://thehackernews.com/2026/10/attackers-hijacked-over-300-tor-exit.html">Attackers Hijacked Over 300 Tor Exit Relays to Intercept SSH ...</a></li>

</ul>
</details>

**Tags**: `#Tor`, `#supply chain security`, `#Ebury malware`, `#SSH credential theft`, `#privacy infrastructure`

---

<a id="item-8"></a>
## [Banned Nvidia B300 Servers Reportedly Found in Chinese State-Backed Network](https://theinference.org/article/china-s-state-money-bought-banned-nvidia-b300-servers-then-redacted-the-receipts) ⭐️ 8.0/10

A state-controlled Chinese semiconductor leasing group reportedly financed the purchase of 32 ASUS servers equipped with export-banned Nvidia B300 chips on behalf of AI company Rongyao Shitu Technology, as part of a larger 700-plus-server transaction worth more than RMB 3 billion (30亿元) intended for China Mobile's Ningxia hub. After the filing drew scrutiny, the leasing group resubmitted documents with the hardware descriptions redacted, and both Nvidia and ASUS have said they are investigating. If confirmed, this would be one of the most direct public traces of top-tier Blackwell-class AI hardware reaching Chinese state-controlled telecom infrastructure despite US export controls, undermining Washington's core strategy of preserving a compute lead over China. It also puts compliance pressure on Nvidia and Taiwan OEMs like ASUS, whose systems sit in the supply chain, and could trigger tighter end-user verification and enforcement across the AI server market. The B300 sits in the strictest US export-control tier and is effectively banned for sale to China, so the servers would have required an indirect route or misdeclared end users. A detail that stands out is that the hardware was delivered as ASUS-branded systems, and the subsequent redaction of public filings suggests the parties recognized the sensitivity of disclosing the chip model.

telegram · zaihuapd · Oct 22, 15:22

**Background**: Nvidia's B300 is part of its Blackwell-generation data-center lineup, the class of accelerators the US restricts most heavily because they underpin frontier AI training. Under the Commerce Department's tiered export framework, China falls into the most restricted category, with stringent controls or outright bans on advanced AI chips, which has pushed buyers toward third-country intermediaries — Taiwan recently indicted nine people over an alleged scheme to re-export B300 GPUs to China, and reports have described similar routing of B200 chips through Malaysia. China Mobile's Ningxia facility is one of the country's major state-backed data-center clusters, making it a natural destination for large-scale AI compute buildouts.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/nine-indicted-by-taiwan-over-illegal-export-of-nvidia-b300-gpus-to-china-details-reveal-five-point-strategy-to-exploit-and-avoid-customs-controls">Nine indicted by Taiwan over illegal export of Nvidia B 300 GPUs to...</a></li>
<li><a href="https://www.cnbc.com/2026/08/19/china-ai-nvidia-chips-us-export-controls.html">China AI firms tap Nvidia power overseas as U.S. weighs crackdown</a></li>
<li><a href="https://townhall.com/columnists/john-koufos/2025/03/16/bidens-ai-diffusion-rule-will-undermine-trumps-vision-for-american-dominance-in-ai-markets-n2653834">Biden’s AI Diffusion Rule Will Undermine Trump’s Vision for American...</a></li>

</ul>
</details>

**Tags**: `#export-controls`, `#nvidia`, `#semiconductors`, `#us-china-tech`, `#ai-hardware`

---

<a id="item-9"></a>
## [NVIDIA OpenShell: An Open-Source Sandboxed Runtime for AI Agent Fleets](https://github.com/NVIDIA/OpenShell) ⭐️ 7.0/10

NVIDIA has released OpenShell, an open-source, secure-by-design runtime that executes fleets of autonomous AI agents inside kernel-level sandboxes governed by declarative policy. Announced at GTC San Jose 2026, it governs agent execution, what resources agents can access, and where inference traffic is routed. Autonomous agents are proliferating in enterprises faster than teams can observe or govern them, so runtime-level containment is becoming a missing security layer between the model and production systems. Having a major infrastructure vendor ship a policy-driven agent runtime may standardize how organizations run agents safely rather than each team bolting together ad-hoc containers. OpenShell combines kernel-level sandboxing with declarative policies for filesystem, network, credential and resource access, and it collects anonymous telemetry limited to operational categories and counts by default. Users can opt out by setting OPENSHELL_TELEMETRY_ENABLED=false on the gateway or server.telemetryEnabled=false for Helm-based installs.

hackernews · niemandhier · Oct 22, 17:44 · [Discussion](https://news.ycombinator.com/item?id=50198675)

**Background**: AI agents increasingly write and execute code, call tools and touch external systems on their own, which makes prompt-level guardrails insufficient — a malicious or hallucinated action must be contained at the infrastructure level. Sandboxing approaches such as microVMs (e.g. Firecracker) and user-space kernels (e.g. gVisor) isolate AI-generated code, while policy engines decide which files, network endpoints and secrets an agent may reach. OpenShell packages these ideas into a runtime built specifically for managing many agents at once, a layer some commenters liken to an 'agent harness'.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/ai/openshell/">NVIDIA OpenShell | Open, Secure Runtime for AI Agents</a></li>
<li><a href="https://perspectives.nvidia.com/nvidia-openshell/">OpenShell</a></li>
<li><a href="https://cryptobriefing.com/nvidia-openshell-ai-agent-security/">Nvidia launches OpenShell , an open-source runtime for securing...</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree that containerization is already table stakes for running agents, and see OpenShell as a convenient way to manage those containers. Several criticized that anonymous telemetry is enabled by default, noting the environment variables needed to turn it off, and one wryly observed that it took a GPU maker — not the AI labs — to ship a solid agent sandbox. Others liked the term 'agent runtime' as a clearer name for what is commonly called a coding agent or agent harness.

**Tags**: `#AI agents`, `#sandboxing`, `#security`, `#container runtime`, `#NVIDIA`

---

<a id="item-10"></a>
## [GNU Taler prepares for real-world payment operations in Germany](https://www.taler.net/en/news/2026-13.html) ⭐️ 7.0/10

The GNU Taler project announced that it is getting ready to operate its privacy-preserving electronic payment system in Germany, moving from research and pilot deployments toward production use in a major European market. The announcement was published on taler.net as the project's 2026 news item and drew substantial discussion on Hacker News. A production rollout in Germany would be one of the most concrete tests of whether a free-software, non-blockchain payment system can survive contact with European KYC/AML rules, which matters both for privacy technology and for EU efforts at digital sovereignty in payments. If it succeeds, it offers a cash-like alternative to bank-backed schemes such as Wero and to US-controlled card networks. GNU Taler is designed so that buyers remain anonymous to merchants and to the exchange while merchants are auditable and taxable, and it uses blind signatures and cut-and-choose cryptography rather than a blockchain. Its exchanges are built to support highly configurable, programmable KYC/AML processes, meaning the degree of buyer privacy in Germany will depend heavily on how the local exchange operator configures those rules.

hackernews · dewey · Oct 22, 16:14 · [Discussion](https://news.ycombinator.com/item?id=50197404)

**Background**: GNU Taler is a free-software electronic payment system developed under the GNU project, named as an acronym for "Taxable Anonymous Libre Electronic Resources". Unlike Bitcoin-style systems, it does not use a blockchain: instead, an "exchange" issues digital coins backed by real bank money, and cryptography hides who spent which coin while keeping merchants accountable to tax authorities. Wero is a separate European wallet built by the European Payments Initiative (EPI) and backed by major banks, which launched in Germany, France and Belgium and is the incumbent home-grown competitor Taler would face.

<details><summary>References</summary>
<ul>
<li><a href="https://www.taler.net/en/index.html">GNU Taler: Home</a></li>
<li><a href="https://docs.taler.net/taler-kyc-manual.html">2. Exchange KYC /AML Operator Manual — GNU Taler</a></li>
<li><a href="https://en.wikipedia.org/wiki/European_Payments_Initiative">European Payments Initiative - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were interested but skeptical: several argued that EU KYC/AML requirements will choke off meaningful payment privacy just as they did for crypto, and one dismissed "cash-like tokens" as an illusion since money must ultimately enter via a traceable bank transaction. Others welcomed the project as a needed European alternative to US payment giants and worried whether it can compete with bank-backed Wero, while one widely echoed tl;dr explained that neither buyer nor seller is anonymous, but the bank cannot see when, where, or whether Taler coins are spent.

**Tags**: `#digital-payments`, `#privacy`, `#gnu-taler`, `#cryptography`, `#eu-tech-policy`

---

<a id="item-11"></a>
## [HackiOS boots iOS 16.5 XNU kernel and user space on Android phones via QEMU](https://github.com/oosexgang/hackios-xnu-kernel) ⭐️ 7.0/10

A Show HN project called HackiOS (oosexgang/hackios-xnu-kernel) boots Apple's open-source XNU kernel — specifically xnu-8796.121.2, the kernel shipped in iOS 16.5 — on Android phone hardware and runs the unmodified iOS 16.5 user space on top of it, from launchd through backboardd and SpringBoard up to apps. It works both under QEMU and on real devices such as the POCO X5 Pro 5G and some Xiaomi phones, using a custom EFI loader, a UEFI port, self-written replacements for Apple's closed drivers, and a Linux Wi-Fi driver running on a compatibility layer. Getting a closed, tightly hardware-coupled mobile OS kernel to boot on entirely foreign hardware is a rare reverse-engineering feat that pushes the boundaries of what mobile virtualization and driver reimplementation can achieve, and it drew heavy community attention (246 points, 83 comments). Its practical impact, however, is limited: it is a research bench rather than a usable ROM, and commenters worry it mainly opens the door to iPhone clones and other misuse. According to the project's own description and community comments, it is a research bench rather than a ROM: a session lasts only a set number of seconds before the kernel returns control to the loader and hands over its log. Booting requires substantial scaffolding — a custom EFI loader, a UEFI port, replacement drivers for Apple's closed-source hardware drivers, and a Linux Wi-Fi driver behind a compatibility layer — which means it is far from a daily-driver installation.

hackernews · aghuang · Oct 22, 15:26 · [Discussion](https://news.ycombinator.com/item?id=50196718)

**Background**: XNU ("X is Not Unix") is Apple's hybrid kernel, combining the Mach microkernel with FreeBSD components and the IOKit driver API; it underpins macOS, iOS, iPadOS, watchOS and tvOS, and its source is released as part of Apple's open-source Darwin distribution. QEMU is a generic machine emulator and virtualizer that lets one operating system run inside another by emulating a full machine, including CPU and peripherals. Because iOS ships with closed-source drivers tied to Apple's own silicon, running its user space elsewhere requires reimplementing those drivers and providing a boot path Apple never intended, which is exactly what this project does.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/oosexgang/hackios-xnu-kernel">GitHub - oosexgang/hackios-xnu-kernel</a></li>
<li><a href="https://en.wikipedia.org/wiki/XNU">XNU - Wikipedia</a></li>
<li><a href="https://www.androidauthority.com/ios-on-android-phones-3726001/">Forget custom ROMs, you can now run iOS on Android phones</a></li>

</ul>
</details>

**Discussion**: Reaction was split: many found the technical achievement impressive, especially that it runs not only in QEMU but on real Xiaomi/POCO hardware, while others questioned the point of running iOS on Android at all — one commenter argued the more desirable goal would be running a free Android distribution like GrapheneOS on Apple hardware, or liberating bootloader-locked Android phones. Several raised concerns that it lowers the barrier to iPhone clones and warrants caution, and one noted that modern iOS is clunky enough that the old desire for iOS on other hardware has faded.

**Tags**: `#iOS`, `#Android`, `#virtualization`, `#QEMU`, `#mobile-security`, `#reverse-engineering`

---

<a id="item-12"></a>
## [pwn.watch: A Live Tracker for Actively Exploited Security Incidents](https://pwn.watch/) ⭐️ 7.0/10

pwn.watch, a site that aggregates live security incidents — CVEs, patch status, fixed versions, vendor advisories and the posts that first surfaced them — hit the front page of Hacker News with roughly 300 points and 141 comments. At the time of discussion the dashboard listed around 40 live incidents, 19 of them rated critical, spanning products from Cisco, Microsoft and Ivanti to Signal's RTC stack. Rather than a raw CVE feed, the site frames vulnerabilities as ongoing incidents with patch status, which is closer to how defenders and on-call engineers actually triage risk. Its popularity reflects growing anxiety about the pace of vulnerability discovery, with commenters arguing that LLM-assisted bug hunting is about to push incident volume far higher. The tracker is a curated dashboard rather than a complete vulnerability database, and its editorial judgments are contestable: one commenter noted that a Signal RTC flaw (CVE-2026-113380) is flagged "Live" and "ongoing" even though it was patched over a month before being publicly announced. Others criticised the information-dense layout, arguing that AI-generated pages tend to cram too much into too small a space.

hackernews · mrkd · Oct 22, 14:08 · [Discussion](https://news.ycombinator.com/item?id=50195543)

**Background**: In security jargon, "pwn" (a leetspeak variant of "owned") means to fully compromise or defeat a system, a term popularised by the breach-notification service Have I Been Pwned. Vulnerability tracking traditionally revolves around CVE identifiers assigned by MITRE and scored for severity with CVSS, while lists such as CISA's Known Exploited Vulnerabilities catalogue mark which flaws are actually being attacked in the wild. Sites like pwn.watch sit on top of that data and try to answer a more operational question: what is exploitable right now, and is there a fix yet?

<details><summary>References</summary>
<ul>
<li><a href="https://pwn.watch/">pwn.watch · live security incidents</a></li>
<li><a href="https://vexdynamics.com/news/live-security-incident-tracker-vulnerabilities-and-exploits">Live Security Incident Tracker: Vulnerabilities and Exploits</a></li>
<li><a href="https://haveibeenpwned.com/FAQs">Have I Been Pwned : Frequently Asked Questions</a></li>

</ul>
</details>

**Discussion**: Commenters largely found the resource useful but picked at its presentation: some questioned how incidents are categorised and when an "ongoing" entry should ever be closed, others complained about the cramped UI. The broader thread turned to the accelerating rate of flaw discovery, with one commenter warning that current-generation LLMs "are going to drive the largest wave of security incidents the world has ever seen," and another quipping that the site missed a chance to call itself "pwnhub".

**Tags**: `#security`, `#vulnerabilities`, `#incident-tracking`, `#AI-security`, `#hackernews`

---

<a id="item-13"></a>
## [WorldTUI: a 360M model trained to hallucinate a working terminal](https://simedw.com/2026/10/21/world-model-terminal/) ⭐️ 7.0/10

Developer simedw fine-tuned a small model — starting from Qwen2.5-Coder-0.5B, described as a ~360M model — to emulate a terminal purely as a generative loop, taking keypresses as input and predicting screen updates as output, including full-screen apps like vim and tmux. The write-up and demo hit the front page of Hacker News, drawing 468 points and 153 comments. The demo is a compact, reproducible example of “generative UI,” where an interface is synthesized by a model instead of rendered by fixed application logic — the same direction that AI-native UI frameworks and research on “Neural Computers” are exploring. Because it runs on a sub-billion-parameter model, it suggests that believable interface emulation may not require frontier-scale compute. The author deliberately chose a small coding model to approach real-time responsiveness, reasoning that a code-focused model had already seen plenty of CLI usage during pretraining. Community members noted that fine-tuning appeared to improve the model's memory of terminal state far more than expected, and the author published benchmarks comparing the base and fine-tuned versions.

hackernews · alphax314 · Oct 22, 02:18 · [Discussion](https://news.ycombinator.com/item?id=50190363)

**Background**: Qwen2.5-Coder, also known as CodeQwen, is Alibaba Cloud's family of code-specialized LLMs offered in six sizes from 0.5B to 32B parameters, and it is commonly adapted through supervised fine-tuning (SFT) or direct preference optimization (DPO). A normal terminal emulator parses escape sequences and renders text deterministically, whereas WorldTUI replaces that logic with next-token prediction over keypress-and-screen-update pairs, so the “filesystem” and command output are hallucinated rather than real. Commenters framed this as a micro version of a “Neural Computer,” where the entire UI is a repeating (user input) → (predicted output) loop and a perfect one would be indistinguishable from a real machine.

<details><summary>References</summary>
<ul>
<li><a href="https://simedw.com/2026/10/21/world-model-terminal/">WorldTUI : I trained a 360M model to pretend to be a terminal</a></li>
<li><a href="https://www.alibabacloud.com/help/en/pai/use-cases/training-evaluation-compression-and-deployment-of-qwen2-5-coder-model">Qwen2.5-Coder PAI Model Gallery train fine-tune deploy ...</a></li>
<li><a href="https://aijourn.com/beyond-static-screens-how-ai-driven-generative-user-interfaces-could-transform-human-computer-interaction/">Beyond Static Screens: How AI-Driven Generative ... | The AI Journal</a></li>

</ul>
</details>

**Discussion**: Sentiment was strongly positive: commenters called the project “very very cool” and were impressed it worked with fine-tuning alone, while the author fielded questions directly. The thread surfaced adjacent hobby projects such as a “lossy git” that stores code by training a neural network and regenerates it on checkout, asked methodological questions about memory and benchmarks, and traced the idea back to early ChatGPT “pretend to be a terminal” prompts.

**Tags**: `#llm`, `#fine-tuning`, `#generative-ui`, `#neural-computer`, `#terminal-emulation`

---

<a id="item-14"></a>
## [Carbon-X: an open 14.8B model trained jointly on DNA and text](https://www.reddit.com/r/MachineLearning/comments/1xchayq/carbonx_is_an_open_148b_model_trained_jointly_on/) ⭐️ 7.0/10

Carbon-X is a 14.8B-parameter decoder-only model released under Apache 2.0 on Hugging Face that accepts raw DNA directly inside a normal chat and answers in English, sharing a single token stream between text and DNA via 6-mer tokens. It was mid-trained on 302B tokens and the model card reports a 66.7% average across five DNA benchmarks with thinking disabled, versus 67.5% for GPT-6.1 Sol. The headline value is deployability: the weights fit on a single 80 GB GPU in bfloat16, which means sensitive genomic data can be analyzed locally instead of being uploaded to a closed API. If the reported benchmark parity with a frontier proprietary model holds up, open-weight multimodal DNA-text models become a practical option for labs that cannot send patient or proprietary sequences off-premises. The model card explicitly states that Carbon-X has not been clinically validated and that exact sequence operations should still be handled by code rather than by the model itself. The 66.7% figure is an average over five DNA benchmarks measured with thinking disabled, so per-task variance and performance on non-public variant datasets remain unquantified.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 22, 12:32

**Background**: DNA language models treat nucleotide sequences like text and learn statistical patterns from genomes; because DNA has no explicit word boundaries, most of these models chunk sequences into fixed-length k-mers (here 6-mers) or overlapping k-mers as their tokens. Decoder-only transformers, the architecture behind GPT-style models, generate output autoregressively and are the standard design for chat-style general-purpose models. bfloat16 is a 16-bit floating-point format that keeps the 8-bit exponent range of 32-bit floats while cutting memory use roughly in half, which is why a 14.8B-parameter model can fit on one 80 GB accelerator.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bfloat16_floating-point_format">Bfloat16 floating-point format</a></li>
<li><a href="https://arxiv.org/html/2507.18570">Hybrid Tokenization Strategy for DNA Language Model using Byte...</a></li>
<li><a href="https://www.nature.com/articles/s42256-024-00872-0">DNA language model GROVER learns... | Nature Machine Intelligence</a></li>

</ul>
</details>

**Discussion**: Discussion around the release was thin, but the central question raised was whether the benchmark gains actually hold on private variant datasets rather than only on the public benchmarks cited in the model card. That framing reflects a broader skepticism about generalization claims for genomic models evaluated outside clinical or proprietary data.

**Tags**: `#genomics`, `#LLM`, `#multimodal`, `#open-source`, `#bioinformatics`

---

<a id="item-15"></a>
## [Frontier audio models struggle to tag ASMR trigger sounds, benchmark finds](https://www.reddit.com/r/MachineLearning/comments/1xcbqdm/frontier_models_are_bad_at_hearing_asmr_8_judges/) ⭐️ 7.0/10

A practitioner building a text-to-ASMR generation model benchmarked eight frontier audio and multimodal models as automatic sound labellers on 480 clips, including 320 human-labelled sound-effect clips from FSD50K and ESC-50 plus ASMR clips labelled by crowdsourced annotators. The best performer, Gemini 3.1 Pro, reached only 0.325 trigger-class F1 against human labels, while cheaper options like MiMo v2.6 Pro landed at 0.243 and spectrogram-image-based judges (Claude Opus 5.5, Grok 4.7) scored just 0.121 and 0.110. The results suggest that strong general audio understanding does not transfer to fine-grained foley and trigger-sound tagging, which matters for anyone building audio datasets through LLM-assisted labelling rather than manual annotation. It also quantifies a large cost spread — $0.0088 per clip for Gemini 3.1 Pro versus $0.0008 for MiMo — showing that the most expensive judge is not automatically the best one for niche sound classes. The failure is class-specific: whispering scored a healthy 0.70–0.79 F1, but paper rustling was almost never detected (Gemini 3.1 Pro and 2.5 Pro each named it only 4 times across 40 paper clips), and brushing F1 on real ASMR fell to 0.18 despite 92% accuracy on clean sound-effect clips, showing clean foley is not the same as ASMR. The author also warns that a cheap model was previously reading transcripts rather than audio — a linear probe on frozen CLAP embeddings could not beat the majority class on those labels — and notes that after fusing judges with Dawid-Skene, the resulting CLAP-ASMR student still detects brushing and paper on 0% of external clips because fusion cannot recover labels no judge can hear.

reddit · r/MachineLearning · /u/MissAppleby · Oct 22, 07:10

**Background**: ASMR (autonomous sensory meridian response) content consists of whispering and quiet "trigger" sounds such as tapping, crinkling, brushing and page turning, and text-to-ASMR systems need every training clip tagged with the sounds it contains — here roughly 126,000 recordings. FSD50K and ESC-50 are standard open datasets of human-labelled environmental sound events, used in this test to measure how well models recall known sound classes. Dawid-Skene is a classic method for aggregating noisy labels from multiple annotators by estimating each one's reliability, and CLAP is a contrastive audio-text embedding model commonly fine-tuned as a sound tagger.

<details><summary>References</summary>
<ul>
<li><a href="https://zenodo.org/records/4060432">FSD50K - Zenodo</a></li>
<li><a href="https://huggingface.co/datasets/Fhrozen/FSD50k">Fhrozen/FSD50k · Datasets at Hugging Face</a></li>

</ul>
</details>

**Tags**: `#audio ML`, `#model evaluation`, `#ASMR`, `#multimodal models`, `#benchmarking`

---

<a id="item-16"></a>
## [Claude API 2026-10-21 Ships, Removing Temperature, Top_p and Top_k](https://x.com/ClaudeDevs/status/2113013247209021918) ⭐️ 7.0/10

Anthropic released Claude API version 2026-10-21, the first official version bump since the 2023-06-01 release, and it removes the temperature, top_p, and top_k sampling parameters — requests that still pass them now return an HTTP 400 error. The official SDKs and the `ant` CLI now default to the new version, and authentication headers have moved to `Authorization: Bearer`. This is a breaking change for any developer whose code explicitly sets sampling parameters or pins a version header, so many Claude integrations will need code and configuration updates before they hit 400 errors in production. It also signals a broader shift away from exposing raw sampling knobs, implying that Anthropic wants models to manage their own randomness rather than leaving it to per-request tuning. The legacy 2023-06-01 version is explicitly not deprecated, so teams can keep their current behavior by pinning the old version header and migrating on their own schedule. The switch to Bearer token authentication matters most for hand-rolled HTTP clients that previously relied on a different auth header format, while SDK users are moved over automatically.

telegram · zaihuapd · Oct 22, 03:54

**Background**: Sampling parameters control how a large language model picks its next token: temperature flattens or sharpens the probability distribution, top_p (nucleus sampling) truncates it to the most likely cumulative mass, and top_k applies a hard cutoff on the candidate list. Developers have long used these knobs to trade determinism for creativity, so removing them from an API is a notable design decision. Claude's API is versioned through a request header, which is why a dated version like 2026-10-21 can coexist with the older 2023-06-01 behavior. Authentication is likewise handled by a standard HTTP `Authorization` header, and Bearer tokens are the common modern convention for token-based API access.

<details><summary>References</summary>
<ul>
<li><a href="https://www.explainx.ai/blog/what-is-temperature-top-p-top-k-llm-sampling-2026">Temperature , Top - P , Top - K in LLMs: Complete Sampling Guide 2026</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Authorization">Authorization header - HTTP | MDN - MDN Web Docs</a></li>
<li><a href="https://letsdatascience.com/blog/llm-sampling-temperature-top-k-top-p-and-min-p-explained">LLM Sampling Parameters Explained: Intuition to... | Let's Data Science</a></li>

</ul>
</details>

**Tags**: `#Anthropic Claude`, `#API Design`, `#Breaking Changes`, `#LLM Tooling`, `#Developer Experience`

---

<a id="item-17"></a>
## [Australian Federal Court Rules Apple and Google Abused Market Power](https://t.me/zaihuapd/44612) ⭐️ 7.0/10

On 12 August 2025, Australia's Federal Court issued an oral ruling finding that both Apple and Google abused a substantial degree of market power in app stores and payment systems, substantially lessening competition in breach of Australian competition law. The court specifically held that Apple's requirement that developers use only its in-app payment system, and Google's conduct in Android app store and payment markets, were anti-competitive. This is a rare ruling that finds both major mobile platform owners liable under a single competition-law framework, giving developers, regulators and courts outside the US and EU an additional precedent against mandatory in-app payment rules and 30%-style commissions. Epic Games called the decision a victory for developers and consumers and expects Apple to be forced to let Epic sell products in the App Store. The full judgment has not been published and is currently sealed because of confidentiality disputes, so the exact reasoning and scope of liability remain unclear. Apple and Google have both signalled they will challenge parts of the decision, and remedies — such as forced opening of payment options or third-party storefronts — have yet to be determined.

telegram · zaihuapd · Oct 22, 06:54

**Background**: The case hinges on section 46 of Australia's Competition and Consumer Act 2010, which prohibits a firm with a substantial degree of market power from conduct that has the purpose, effect or likely effect of substantially lessening competition; a 2017 amendment introduced this "effects test". Epic Games has been litigating against Apple and Google since 2020 over the iOS App Store's mandatory in-app payment system and its 30% commission, and similar questions are being pursued by regulators in the EU, UK and elsewhere.

<details><summary>References</summary>
<ul>
<li><a href="https://www.accc.gov.au/business/competition-and-exemptions/misuse-of-market-power">Misuse of market power | ACCC</a></li>
<li><a href="https://www5.austlii.edu.au/au/legis/cth/consol_act/caca2010265/s46.html">COMPETITION AND CONSUMER ACT 2010 - SECT 46 Misuse of market ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Epic_Games_v._Apple">Epic Games v. Apple - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#antitrust`, `#Apple`, `#Google`, `#app-store`, `#regulation`

---

<a id="item-18"></a>
## [Tesla begins North American production of the steering-wheel-free Cybercab](https://t.me/zaihuapd/44614) ⭐️ 7.0/10

Tesla has started volume production of the Cybercab in North America, a purpose-built two-seat robotaxi that ships with no steering wheel, pedals, or side mirrors, with the onboard AI handling all driving control. According to reference material, the vehicle was unveiled in October 2024 and production began in February 2026. This is one of the first mass-production vehicles designed from the ground up with no human controls, making it a concrete step from driver-supervised assisted driving toward commercial driverless ride-hailing. If it scales, it would put Tesla in direct competition with Waymo-style robotaxi operators and could reshape the economics of urban transport. The Cybercab uses a camera-only autonomous-driving stack rather than lidar or radar, and Tesla has targeted an operating cost below US$0.30 per mile; the design also drops the rear window. Because existing US federal motor-vehicle safety standards were written for human-driven cars, Tesla's self-certification has drawn scrutiny, with the NHTSA reportedly opening an investigation and emergency responders raising concerns about the missing steering wheel.

telegram · zaihuapd · Oct 22, 07:54

**Background**: A robotaxi is an autonomous vehicle (SAE Level 4 or 5) operated for a ride-hailing service, meaning it can drive without a human behind the wheel within a defined area. Tesla's Robotaxi service using Full Self-Driving software began limited operation in Austin, Texas, in June 2025, and since then has expanded to several Texas and Florida cities. The Cybercab is intended to become the main vehicle of that fleet, replacing modified consumer cars. Regulatory approval and public trust remain the main obstacles: surveys consistently show a minority of respondents willing to ride in a self-driving car.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tesla_Cybercab">Tesla Cybercab</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tesla_Robotaxi">Tesla Robotaxi - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Robotaxi">Robotaxi</a></li>

</ul>
</details>

**Tags**: `#autonomous-vehicles`, `#tesla`, `#robotaxi`, `#self-driving`, `#industry-news`

---

<a id="item-19"></a>
## [miHoYo and Tsinghua Open-Source GameScaling Game Control Models](https://arxiv.org/abs/2610.28698v1) ⭐️ 7.0/10

miHoYo's Honkai AI team, together with Tsinghua University's Spatial Intelligence Lab and collaborators, released GameScaling, a family of Qwen3.5-based vision-language models (0.8B to 27B parameters) that were continued-pre-trained to play games with keyboard and mouse and that output the next 200ms of actions on each call. Eight checkpoints and an inference client are published under Apache-2.0 on Hugging Face and GitHub alongside an arXiv preprint. It is an unusually large-scale public release of a game-playing vision-language agent from a major studio, giving game-AI and VLA-agent researchers ready-to-use Apache-2.0 checkpoints spanning a 30x parameter range. Its systematic 120-configuration scaling study also offers concrete empirical guidance on when more data, more diversity, or bigger models actually help in virtual worlds. Each prediction covers 200ms of control as 6 discrete steps of 33ms plus one mouse movement and scroll for the whole chunk, conditioned on the current frame and a short history of past frames and actions. Training code is not released, and the scaling results show that more data improves in-domain performance and greater diversity transfers to visually similar games but yields limited gains on very different ones.

telegram · zaihuapd · Oct 22, 11:32

**Background**: Vision-language-action (VLA) models extend vision-language models — networks that jointly process screenshots and text, such as the natively multimodal Qwen3.5 — by attaching an action decoder so the model outputs control signals instead of words. GameScaling is built by continued pre-training such a model on large amounts of recorded gameplay, the same recipe used for embodied agents in robotics, but applied across many virtual worlds that each have their own visuals, physics, and control schemes. That fragmentation is precisely why the paper frames its question as whether scaling laws carry over from one physical world to many virtual ones.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/THUSI-Lab/GameScaling">GitHub - THUSI-Lab/GameScaling: Scaling in Games: Continued ...</a></li>
<li><a href="https://huggingface.co/THUSI-Lab/GameScaling">THUSI-Lab/GameScaling · Hugging Face</a></li>
<li><a href="https://gamescaling.github.io/">Scaling in Games: Continued Pre-Training for Embodied Agents ...</a></li>

</ul>
</details>

**Tags**: `#game-ai`, `#vision-language-models`, `#agents`, `#open-source`, `#scaling-laws`

---

<a id="item-20"></a>
## [Oracle Issues Critical Security Alert for CVE-2026-91403 in Java SE JSSE](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 7.0/10

Oracle published a security alert for CVE-2026-91403, a CVSS 9.1-rated vulnerability in the Java SE JSSE component that can be exploited remotely over the network without any authentication. Patches have been released covering Java SE 8u511, 11.0.33, 17.0.21, 21.0.13, 25.0.5 and 27.0.1, as well as multiple affected GraalVM versions. Because JSSE is the component that implements SSL/TLS in the JDK, virtually any JVM-based server, client, API gateway or middleware that negotiates encrypted connections may be exposed. A remotely exploitable, unauthenticated flaw in a runtime embedded across enterprise backends and third-party applications makes prompt patching a fairly urgent operational task. Oracle's advisory states the flaw can seriously compromise data confidentiality and integrity but gives little technical detail — no exploit prerequisites, attack complexity breakdown or proof-of-concept information is published. Administrators should also check container images, application-bundled JREs and build toolchains, since many deployments ship their own runtime rather than relying on the system-wide JDK.

telegram · zaihuapd · Oct 22, 12:30

**Background**: JSSE (Java Secure Socket Extension) is the standard JDK/JRE component that provides SSL and TLS support and has shipped as part of the JRE since version 1.4, which means encrypted traffic handling in most Java applications runs through it. CVSS is the Common Vulnerability Scoring System, where scores of 9.0 and above are classified as critical. GraalVM is a high-performance polyglot virtual machine that also offers a Native Image tool for ahead-of-time compiling Java applications into standalone executables, so its affected releases need patching too.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.csdn.net/a82514921/article/details/104590197/">Java SSL实现使用详解-CSDN博客</a></li>
<li><a href="https://www.first.org/cvss/calculator/3-1">Common Vulnerability Scoring System Version 3.1 Calculator</a></li>
<li><a href="https://juejin.cn/post/7291937010405916681">GraalVM 入门教程 GraalVM 是 什 么 GraalVM ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#java`, `#vulnerability`, `#CVE`, `#patching`

---

<a id="item-21"></a>
## [China Proposes Export Controls on 40 AI, Biotech and Solar Technologies](https://t.me/zaihuapd/44626) ⭐️ 7.0/10

China's Ministry of Commerce (MOFCOM) has opened a public comment period on a draft revision to the Catalog of Technologies Prohibited or Restricted from Export, covering 40 technologies across three sectors. The proposal places temporary registration requirements on 23 AI technologies (including large models, AI agents, computing power clusters and information processing), 5 biotech technologies (cell and gene therapy, small nucleic acid drugs, pathogenic microorganisms) and 12 photovoltaic technologies (polysilicon, wafer and solar cell manufacturing). The catalog is one of the main legal levers Beijing uses to control technology outflows, so adding AI models, agents and compute-cluster know-how would directly affect cross-border research collaboration, model licensing deals and how Chinese labs publish or open-source their work. Because China dominates global polysilicon and solar cell production and is a fast-growing biotech licensing partner, the revision could ripple through clean-energy and pharmaceutical supply chains well beyond China. The draft explicitly carves out technologies that have already entered the public domain through open-sourcing or academic publication, and it offers facilitative measures such as automatic licensing for biotech out-licensing arrangements that do not involve a transfer of ownership. The proposed mechanism is framed as "temporary registration" rather than an outright ban, and the measure is still a draft open for public comment rather than a finalized rule.

telegram · zaihuapd · Oct 22, 16:10

**Background**: China's export-control catalog lists technologies whose transfer abroad requires government permission, and it is administered by MOFCOM together with the Ministry of Science and Technology; the list was first issued in 2001 and is revised periodically as technology evolves. This round targets relatively new categories: AI agents are systems driven by large language models that plan and execute multi-step tasks using tools, while computing power clusters are the networked GPU/accelerator farms used to train frontier models. Small nucleic acid drugs are a newer drug class — including antisense oligonucleotides and siRNA — that target RNA directly rather than proteins, and photovoltaic manufacturing spans the polysilicon, wafer and cell stages of the solar supply chain.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-agents">What are AI agents? - IBM</a></li>
<li><a href="https://www.nature.com/articles/s41392-024-02112-8">Landscape of small nucleic acid therapeutics: moving from the ... Nucleic acid drugs: recent progress and future perspectives Small nucleic acid therapeutics: delivery breakthroughs ... Current status and trends in small nucleic acid drug ... - PubMed Landscape of small nucleic acid therapeutics: moving from the ... Small Nucleic Acid Drugs: siRNA vs ASO – BOC Sciences</a></li>

</ul>
</details>

**Tags**: `#export-controls`, `#ai-policy`, `#china-regulation`, `#open-source-ai`, `#tech-geopolitics`

---

<a id="item-22"></a>
## [Woman Faces Six Years in Prison Over Fraudulent Cash App Account](https://www.techspot.com/news/114296-woman-spends-three-nights-jail-faces-six-years.html) ⭐️ 6.0/10

Amanda Smith, who spent three nights in jail, faces up to six years in prison after a fraudulent Cash App account was opened in her name, and she has refused a plea deal offering a $1,000 fine, $1,000 in restitution, and three years' probation because she says she is innocent. The case, first reported by 404 Media, has drawn widespread attention as an example of both fintech identity-verification failures and aggressive prosecution of a likely victim. The case shows how lightly verified fintech onboarding can turn an identity-theft victim into a criminal defendant, shifting the consequences of platform design flaws onto individuals. It also fuels a broader debate about prosecutorial incentives, since a plea bargain lets authorities close a weak case while the accused absorbs a criminal record. Smith was jailed for three nights and, under the offer, would have avoided prison by pleading to a misdemeanor-level penalty despite maintaining her innocence; the amount of money involved in the fraudulent account has not been publicly detailed, and the original reporting comes from 404 Media. The case hinges on whether prosecutors can show she — rather than an unknown third party — controlled the account.

hackernews · oidar · Oct 22, 13:11 · [Discussion](https://news.ycombinator.com/item?id=50194833)

**Background**: Fintech apps like Cash App are required to run Know Your Customer (KYC) checks — identity verification and due-diligence controls meant to confirm who a customer is and to satisfy anti-money-laundering law — but remote, app-based onboarding is often lighter-touch than opening a bank branch account. Fraudsters exploit this with identity fraud, using another person's personal information such as name, address, or Social Security number without authorization, and with synthetic identity fraud, where fabricated or mixed identities are used; the Boston Fed notes synthetic identity losses exceeded $35 billion in 2023. Cash App, operated by Block (formerly Square) and issued with partner banks such as Sutton Bank, has been the subject of litigation alleging inadequate fraud controls.

<details><summary>References</summary>
<ul>
<li><a href="https://financialjusticenow.com/blog/thorne-v-square-inc-and-sutton-bank-allegations-of-cash-app-fraud/">Thorne v. Square, Inc. and Sutton Bank: Allegations of Cash App Fraud</a></li>
<li><a href="https://www.kychub.com/blog/kyc-for-fintech">KYC for Fintech: Compliance and Onboarding Guide | KYC Hub</a></li>
<li><a href="https://www.bostonfed.org/news-and-events/news/2025/04/synthetic-identity-fraud-financial-fraud-expanding-because-of-generative-artificial-intelligence.aspx?ref=blog.scoreplex.io">Gen AI is ramping up the threat of synthetic identity fraud</a></li>

</ul>
</details>

**Discussion**: Commenters were overwhelmingly critical of the prosecution, arguing that plea deals are used to paper over official mistakes and pressure innocent people into accepting punishment to avoid risk. Several called for prosecutors and police to face personal liability for gross negligence, and others argued that Cash App's founders and executives should be held accountable for building a fraud-prone system with too few checks.

**Tags**: `#fintech`, `#identity-theft`, `#criminal-justice`, `#security`, `#cash-app`

---

<a id="item-23"></a>
## [Hacker News user apologizes for unintentionally breaking PHP RCE embargo](https://news.ycombinator.com/item?id=50193416) ⭐️ 6.0/10

A Hacker News user publicly apologized for posting about the then-unreleased PHP remote code execution vulnerabilities tracked as CVE-2026-109618 and CVE-2026-109619 ahead of their coordinated disclosure date, saying the early post disrupted the release schedule and created extra workload for responders. He explained that neither he nor his contact had been told an embargo existed, and that his intent was simply to warn fellow users who compile PHP from source on its four-weekly release cycle. The episode is a case study in how fragile multiparty coordinated disclosure is: a single well-intentioned post from someone outside the coordination circle can apparently shift a vendor's release timeline and force defenders to scramble. It also raises the question of who is actually accountable when embargo information fails to travel down the disclosure chain. The apology's central claim is that the embargo was never communicated to him — his contact said there was no embargo, and her own contact said the same — so he argues he had no obligation to keep the information private. Commenters also pointed to an Amazon threat intelligence post indicating the flaws had already leaked and were being exploited before his post.

hackernews · petecooper · Oct 22, 10:11

**Background**: Coordinated vulnerability disclosure (CVD) is the practice of reporting a flaw privately to a vendor and agreeing to stay quiet until a patch is ready, so users have a fix available the moment details go public. That quiet period is called an embargo, and it typically involves multiple parties — reporters, vendors, coordinators, downstream distributors — which is exactly why embargo failures grow more likely as more people join the coordination. CVE identifiers such as CVE-2026-109618 are the standard dictionary names used to track a specific publicly known vulnerability across advisories and scanners, while remote code execution (RCE) is the most severe class of bug, since an attacker can run their own code on a server, in this case in PHP itself regardless of the application built on top of it.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tenable.com/blog/php2shell-cve-2026-109618-cve-2026-109619-frequently-asked-questions-about-critical-php-remote">php 2shell (CVE-2026-109618, CVE-2026-109619): Critical PHP RCE ...</a></li>
<li><a href="https://certcc.github.io/CERT-Guide-to-CVD/howto/coordination/cvd_recipes/">Troubleshooting CVD - CERT® Guide to Coordinated Vulnerability ...</a></li>
<li><a href="https://markesler.com/notes/coordinated-vulnerability-disclosure/">Coordinated Vulnerability Disclosure | Mark Esler</a></li>

</ul>
</details>

**Discussion**: Commenters largely rejected the premise of the apology, arguing that you cannot break an embargo you were never subject to or informed about, and that responsibility lies with whoever passed the information along without its conditions. Others noted the vulnerabilities had already leaked and were being exploited before his post, and one commenter mocked the phrase "I take full responsibility" as empty rhetoric rather than a concrete commitment.

**Tags**: `#security`, `#coordinated-disclosure`, `#php`, `#vulnerability`, `#open-source`

---

<a id="item-24"></a>
## [Arc browser sunset as Atlassian-owned Browser Company pivots to Dia](https://arc.net/) ⭐️ 6.0/10

The Browser Company is officially sunsetting Arc, its design-forward browser, on December 22, 2026, and directing users toward Dia, its AI-first browser. The company announced the decision on Thursday, roughly a year after Arc's development was halted and its team was absorbed through Atlassian's $610 million acquisition. Arc was one of the most influential browser UX experiments of the decade, popularizing sidebar tabs, spaces, and split-view navigation that are now being copied across the browser market. Its end marks the close of a VC-funded attempt to reinvent the browser as a product, and it pushes displaced users toward alternatives such as Zen and Orion, which inherited different parts of its philosophy. Arc was originally a Chromium-based browser built by The Browser Company, a startup founded by Josh Miller and Harsh Agrawal, and it is now owned by Atlassian following the 2025 acquisition. The most-cited successors differ architecturally: Zen is an open-source Firefox fork licensed under MPL 2.0, while Orion is a closed-source WebKit browser from Kagi aimed at macOS and iOS.

hackernews · suhdonghwi · Oct 22, 16:27 · [Discussion](https://news.ycombinator.com/item?id=50197601)

**Background**: Arc launched in 2022 as an attempt to rethink browser chrome entirely, moving tabs into a collapsible sidebar and organizing work into separate "Spaces" with custom themes and AI-assisted page tweaks. In 2024 The Browser Company told users Arc would no longer receive major new features as it built Dia, an AI-native browser that treats browsing and chatbot interaction as one workflow. Atlassian acquired the company in 2025 for a reported $610 million. Because many of Arc's ideas proved popular, community forks and rivals now compete to carry them forward.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/10/22/arc-browser-sunsets-december-22-as-the-browser-company-doubles-down-on-dia/">Arc browser sunsets December 22 as The Browser Company ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Arc_(web_browser)">Arc (web browser) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zen_Browser">Zen Browser</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely resigned rather than surprised, with several saying the writing was on the wall once the company pivoted to Dia. Kagi's Orion drew praise for its sustainable, subscription-funded business model and WebKit base, though its closed-source nature was called a major blow, while others reported happily switching to Zen or to Safari augmented with tools like SupaSidebar and OpenIn. A dissenting commenter questioned what Arc actually offered that native OS window-management shortcuts could not, arguing vertical tabs waste screen space when windows are tiled side by side.

**Tags**: `#browsers`, `#Arc`, `#Hacker News`, `#UX`, `#software products`

---

<a id="item-25"></a>
## [WhissleAI shrinks steerable TTS to 11.84 MB with int4 quantization](https://www.reddit.com/r/MachineLearning/comments/1xcum4s/we_shrank_our_steerable_small_tts_to_1184_mb_wer/) ⭐️ 6.0/10

WhissleAI released steer-tts-edge, an edge variant of its SteerTTS v1 steerable English TTS whose total shipping footprint — weights, voices, text front end and Python runtime — is just 11.84 MB. The 9.25M-parameter acoustic model (attention plus bidirectional Mamba-3) was quantization-aware trained to int4, and the vocoder is a 6.2M-parameter Vocos-style model distilled from charactr/vocos-mel-24khz, also int4 QAT. Packing a full TTS stack into under 12 MB makes on-device speech synthesis realistic for mobile apps, browsers and embedded hardware where multi-hundred-megabyte models are impractical. It also shows that aggressive int4 quantization can preserve intelligibility, a useful data point as the ecosystem pushes speech models toward the edge. On the Open TTS Leaderboard protocol run locally, Seed-TTS WER stayed at 0.96% and CV3-Eval WER went from 2.62% to 2.67%, while UTMOS fell about 0.1 (4.20→4.11 and 4.17→4.08), almost entirely due to the small int4 vocoder. On CPU with 4 threads it reaches RTF 0.053 (~19x realtime) and ~120 ms to first audio, but weights are dequantized to fp32 at load, so the gain is size rather than speed; it is English-only with 200 voices and no voice cloning, free-text prompts or flow refiner.

reddit · r/MachineLearning · /u/Working_Hat5120 · Oct 22, 20:57

**Background**: A TTS pipeline typically pairs an acoustic model, which turns text into intermediate audio features, with a vocoder that renders those features into a waveform; Vocos is a fast GAN-trained vocoder that predicts spectral coefficients and reconstructs audio in a single forward pass via inverse Fourier transform. Quantization-aware training simulates low-precision arithmetic during training so a model can be stored in 4-bit integers with minimal quality loss, which is how the footprint drops by roughly an order of magnitude. Quality is commonly reported with WER from an ASR model (measuring intelligibility) and UTMOS, a neural predictor of human mean-opinion scores for naturalness. RTF, or real-time factor, expresses synthesis speed as processing time divided by audio duration, so lower is faster.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/gemelo-ai/vocos">GitHub - gemelo-ai/vocos: Vocos: Closing the gap between time ...</a></li>
<li><a href="https://arxiv.org/abs/2306.00814">[2306.00814] Vocos: Closing the gap between time-domain and ... BSC-LT/vocos-mel-22khz · Hugging Face Vocos: Closing the gap between time-domain and Fourier-based ... GitHub - LqNoob/vocos: Vocos: Closing the gap between time ... vocos-mel-24khz · Models</a></li>
<li><a href="https://www.emergentmind.com/topics/utmos">UTMOS Speech Quality Metric</a></li>

</ul>
</details>

**Tags**: `#TTS`, `#model-compression`, `#quantization`, `#edge-ai`, `#speech-synthesis`

---

<a id="item-26"></a>
## [XPeng IRON runs second-gen VLA on-device, re-reasoning every 0.2 seconds](https://www.ithome.com/1/016/667.htm) ⭐️ 6.0/10

XPeng announced that its second-generation VLA (vision-language-action) model has been deployed on-device on its IRON humanoid robot, which now re-reasons from its live camera feed every 0.2 seconds and predicts motion changes up to 6 seconds into the future. This lets IRON react to sudden changes during handshakes and high-fives, such as the other person suddenly clenching a fist or shifting the target position. Running a VLA model locally on the robot rather than in the cloud is what makes sub-second reaction possible, and it signals a broader shift of robot foundation models toward edge deployment. XPeng says it plans to mass-produce the humanoid by the end of 2026 and begin deliveries in the first half of 2027, starting in stores and shopping malls, so this capability is positioned as a near-term commercial feature rather than a lab demo. XPeng disclosed the 0.2-second re-planning cadence and 6-second action prediction window but released no latency, success-rate or power benchmarks to back them up. The robot is a 22-degree-of-freedom bipedal platform that has already walked off XPeng's own production line, and the on-device inference presumably relies on XPeng's self-developed Turing chips, though the report does not specify the compute hardware.

telegram · zaihuapd · Oct 22, 13:37

**Background**: A VLA model is a multimodal foundation model that takes camera images plus a natural-language instruction as input and outputs low-level robot actions, essentially wiring perception and language understanding directly to motor control. Such models are usually large and have been run on cloud or server GPUs, but real-time physical interaction demands low latency and no dependence on network connectivity, which is why vendors are pushing to optimize them for on-device NPUs and edge chips. XPeng is an electric-vehicle maker that has extended into AI and robotics, developing IRON alongside its autonomous-driving stack.

<details><summary>References</summary>
<ul>
<li><a href="https://www.xpeng.com/technology/AI_Robot_Iron">XPENG - Official Website | XPENG Motors – XPENG</a></li>
<li><a href="https://www.xpeng.com/news/01a080371029a057bc8e8a02a2c6012b">XPENG IRON Humanoid Robot Now Walks Off the Production Line</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vision–language–action_model">Vision–language–action model - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#robotics`, `#humanoid-robots`, `#vision-language-action`, `#edge-ai`, `#xpeng`

---