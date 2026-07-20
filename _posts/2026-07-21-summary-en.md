---
layout: default
title: "Horizon Summary: 2026-07-21 (EN)"
date: 2026-07-21
lang: en
---

> From 33 items, 13 important content pieces were selected

---

1. [Leaked Altman Email: OpenAI Weighed Local GPT-3 Release to Thwart Competitors](#item-1) ⭐️ 9.0/10
2. [Critical RCE in Fastjson 1.x Without Gadget](#item-2) ⭐️ 9.0/10
3. [China's open-weights AI strategy gains edge](#item-3) ⭐️ 8.0/10
4. [Hacker wipes Romania's land registry database](#item-4) ⭐️ 8.0/10
5. [Measuring AI writing on arXiv: detection accuracy and limits](#item-5) ⭐️ 8.0/10
6. [Poor LED Design Worsens Light Pollution, Wasting Night Sky Potential](#item-6) ⭐️ 8.0/10
7. [EU Biometric Data Sharing with US for Visa-Free Travel Sparks Privacy Debate](#item-7) ⭐️ 8.0/10
8. [Kimi K3, Qwen 3.8 Open-Source Releases; Anthropic Tensions](#item-8) ⭐️ 8.0/10
9. [Ben Thompson Proposes Fair Use Law for AI Training](#item-9) ⭐️ 8.0/10
10. [Hugging Face Discloses AI Agent Attack, Commercial LLM Refuses Forensics Help](#item-10) ⭐️ 8.0/10
11. [US may restrict firms from using Chinese open-weight AI models](#item-11) ⭐️ 8.0/10
12. [US military apps found embedded with Chinese/Russian code](#item-12) ⭐️ 8.0/10
13. [Zhipu AI Completes All-Domestic Chip Datacenter](#item-13) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Leaked Altman Email: OpenAI Weighed Local GPT-3 Release to Thwart Competitors](https://simonwillison.net/2026/Jul/20/sam-altman/#atom-everything) ⭐️ 9.0/10

A leaked email from Sam Altman to OpenAI's board, dated October 1, 2022, reveals that OpenAI considered releasing a local, consumer-hardware-runnable model with GPT-3-level capability to discourage competitors like Stability AI from funding similar open-source efforts. This email provides rare, direct insight into OpenAI's strategic thinking about open-sourcing models as a competitive tactic, highlighting how major AI labs view open-source releases as moves to shape the market and defund rivals. The email was exposed during the 2026 Musk v. Altman legal case, and specifically mentions releasing the model 'before Stability or someone else does' to make it harder for new efforts to get funded.

rss · Simon Willison · Jul 20, 03:47

**Background**: Stability AI is a UK company known for open-source models like Stable Diffusion, which challenged proprietary AI from OpenAI. At the time, open-source AI models were growing in capability, and labs like OpenAI saw them as both opportunities and threats. The idea of a locally-run model would allow users to run powerful AI without cloud dependencies.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Stability_AI">Stability AI</a></li>
<li><a href="https://github.com/PromtEngineer/localGPT">PromtEngineer/localGPT: Chat with your documents on your local ...</a></li>

</ul>
</details>

**Tags**: `#openai`, `#sam-altman`, `#ai open source`, `#gpt-3`, `#ai strategy`

---

<a id="item-2"></a>
## [Critical RCE in Fastjson 1.x Without Gadget](https://x.com/k_firsov/status/2078872293745570032) ⭐️ 9.0/10

Security researcher Kirill Firsov disclosed a critical remote code execution vulnerability affecting Fastjson versions 1.2.68 through 1.2.83, which can be exploited without enabling autoType or relying on classpath gadgets, and works on JDK 8, 17, and 21. This vulnerability is severe because it requires no gadget chain, lowering the exploitation barrier for attackers, and affects the end-of-life Fastjson 1.x line with no official patch expected, forcing users to urgently migrate to Fastjson2 or enable SafeMode. The vulnerability was disclosed after Fastjson 1.x reached end-of-life in October 2024. To mitigate, users can upgrade to Fastjson2 or enable SafeMode via JVM parameter -Dfastjson.parser.safeMode=true or by configuring ParserConfig.

telegram · zaihuapd · Jul 20, 14:32

**Background**: Fastjson is a popular JSON library in Java, known for its autoType feature that includes type information in serialized data, which has historically led to deserialization vulnerabilities. SafeMode was introduced in version 1.2.68 to completely disable autoType and prevent such attacks. The disclosed vulnerability bypasses existing restrictions without needing any specific classpath gadgets, making it particularly dangerous.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/alibaba/fastjson/wiki/fastjson_safemode_en">fastjson_safemode_en · alibaba/fastjson Wiki</a></li>
<li><a href="https://github.com/alibaba/fastjson/wiki/enable_autotype">enable_autotype · alibaba/fastjson Wiki · GitHub</a></li>
<li><a href="https://www.huaweicloud.com/intl/en-us/notice/20220523153626935.html">Fastjson <= 1.2.80 Deserialization Remote Code Execution Vulnerability_HUAWEI CLOUD</a></li>

</ul>
</details>

**Tags**: `#security`, `#fastjson`, `#rce`, `#vulnerability`, `#java`

---

<a id="item-3"></a>
## [China's open-weights AI strategy gains edge](https://werd.io/american-ai-is-locked-down-and-proprietary-its-losing/) ⭐️ 8.0/10

A recent article argues that China's open-weights AI models are gaining competitive advantage over proprietary US models, drawing parallels to historical market dynamics where open and low-cost solutions eventually dominate. This trend could reshape the global AI landscape by democratizing access to powerful models, potentially undermining the market position of US tech giants and accelerating AI adoption in cost-sensitive applications. The article claims 80% of startups use Chinese models, a figure questioned by commenters. Leading open-weights models like Qwen and DeepSeek rank high on various AI leaderboards.

hackernews · benwerd · Jul 20, 14:21 · [Discussion](https://news.ycombinator.com/item?id=48979269)

**Background**: Open-weights models release trained neural network weights publicly, allowing fine-tuning and deployment without full transparency of training data or code. This contrasts with proprietary models like GPT-4, which are accessed via APIs. Historically, low-cost or free solutions (e.g., PCs vs. mainframes, Linux vs. Unix) have often won in the marketplace.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@aruna.kolluru/exploring-the-world-of-open-source-and-open-weights-ai-aa09707b69fc">Exploring the World of Open Source and Open Weights AI | Medium</a></li>
<li><a href="https://llm-stats.com/">AI Leaderboard 2026: Compare & Rank 300+ Top AI Models by...</a></li>
<li><a href="https://artificialanalysis.ai/models">Comparison of AI Models across Intelligence, Performance, and Price</a></li>

</ul>
</details>

**Discussion**: Commenters expressed skepticism about the claim that 80% of startups use Chinese models, citing their own experiences with US models. Some noted that enterprises prioritize data retention and vendor relationships over openness.

**Tags**: `#AI`, `#open-source`, `#China`, `#machine learning`, `#industry trends`

---

<a id="item-4"></a>
## [Hacker wipes Romania's land registry database](https://news.risky.biz/risky-bulletin-hacker-wipes-romanias-entire-land-registry-database/) ⭐️ 8.0/10

A hacker breached and wiped Romania's land registry database, claiming to have deleted backups, though officials report an offline copy survived and are migrating to government cloud infrastructure. This incident threatens societal stability by potentially disrupting land ownership verification, and it underscores critical vulnerabilities in government IT security, especially around password practices and backup strategy. The attacker allegedly used weak credentials like 'P@ssw0rd' to gain access, and security firm KELA identified the hacker as Zakaria Mahdjoub from Algeria. An offline copy of the data allowed officials to avoid complete loss.

hackernews · speckx · Jul 20, 13:28 · [Discussion](https://news.ycombinator.com/item?id=48978605)

**Background**: Land registries are critical for proving property ownership, and their compromise can lead to legal chaos. Romanian government IT has reportedly suffered from corruption and poor security practices, with contracts awarded to cronies who neglect proper protections.

**Discussion**: Community comments highlight corruption as a root cause, with contracts going to cronies who neglect security. There is relief that an offline backup exists, but skepticism remains about the government's response and long-term security improvements.

**Tags**: `#cybersecurity`, `#data breach`, `#land registry`, `#Romania`, `#security incident`

---

<a id="item-5"></a>
## [Measuring AI writing on arXiv: detection accuracy and limits](https://unslop.run/blog/measuring-ai-writing-on-arxiv) ⭐️ 8.0/10

An analysis of over 12,000 arXiv papers from 2021 to 2026 found that by January 2026, about 39% of papers were flagged as AI-written, with computer science peaking at 65%. The author tuned the detector to minimize false positives, yet highlights where the measurement method breaks, especially on older human-written papers that receive high AI scores. This analysis quantifies the rapid increase of AI-written content in academic papers, raising concerns about the reliability of detection methods and their implications for scholarly publishing, peer review, and trust in scientific literature. The detector achieved a very low false positive rate (0.4% pre-ChatGPT), yet it flagged some pre-LLM papers as AI-written—e.g., a 2011 workshop paper at 27% and a 2015 cluster paper at 74%—indicating that human writing can overlap with LLM patterns. The analysis also shows strong disciplinary variation, with computer science papers reaching 65% AI-writing detection and mathematics barely changing from base rates.

hackernews · dopamine_daddy · Jul 20, 16:36 · [Discussion](https://news.ycombinator.com/item?id=48981206)

**Background**: LLM-generated text detection typically uses black-box or white-box methods that analyze statistical patterns such as word choice, perplexity, and burstiness. However, these detectors often suffer from false positives, especially for highly technical or non-native English writing, and can be circumvented by targeted editing. The growing integration of LLMs in academic writing has spurred efforts to measure and detect AI-generated content, but the accuracy and reliability of such detection remain active areas of debate and research.

<details><summary>References</summary>
<ul>
<li><a href="https://cacm.acm.org/research/the-science-of-detecting-llm-generated-text/">The Science of Detecting LLM -Generated Text – Communications of...</a></li>
<li><a href="https://www.linkedin.com/pulse/limitations-ai-detection-academic-writing-maindze-mphil-mbcs--0olfe">The Limitations of AI Detection in Academic Writing .</a></li>
<li><a href="https://arxiv.org/pdf/2406.09056">Towards Reliable Detection of LLM -Generated Texts...</a></li>

</ul>
</details>

**Discussion**: Community comments express significant skepticism about the detection method. Users report that their own pre-2010 papers were flagged as AI-written, suggesting widespread false positives. Some argue the problem may be overstated, while others discuss strategic implications of LLM use in corporate and academic settings.

**Tags**: `#AI writing`, `#arXiv`, `#LLM detection`, `#academic publishing`, `#measurement`

---

<a id="item-6"></a>
## [Poor LED Design Worsens Light Pollution, Wasting Night Sky Potential](https://spectrum.ieee.org/led-light-pollution) ⭐️ 8.0/10

An article on IEEE Spectrum argues that poorly designed LED lighting, focused on cost minimization and simplistic ground-level lux measures, increases light pollution by producing glare and skyglow, contrary to the potential of LEDs to preserve night skies. This matters because light pollution disrupts ecosystems, harms astronomical observations, and diminishes cultural connection to the night sky; better engineering standards could mitigate these impacts while still providing effective outdoor lighting. The article highlights that bare bulbs mounted high with brutal intensity create direct glare, which worsens night blindness and is often 'fixed' by adding even more light, whereas proper design should shield the bulb from direct view and use presence sensors for adaptive lighting.

hackernews · defrost · Jul 20, 13:07 · [Discussion](https://news.ycombinator.com/item?id=48978350)

**Background**: LEDs are energy-efficient lighting that can be precisely controlled, but poor implementation often leads to excessive blue-rich light that scatters in the atmosphere, creating skyglow. The International Dark-Sky Association and Illuminating Engineering Society have developed model ordinances and standards to address light pollution, but many municipalities lack updated codes. Presence-sensing lights, as mentioned in community comments, can reduce energy use and light pollution by only lighting when needed.

<details><summary>References</summary>
<ul>
<li><a href="https://mrsc.org/explore-topics/code-enforcement/nuisances/light-nuisances">MRSC - Light Nuisances - Ambient Light, Light Pollution, Glare</a></li>
<li><a href="https://www.ekinex.com/en/ekinex-solutions-for-smart-lighting-control/presence-sensors.html">Presence sensors | Smartlighting | Ekinex</a></li>

</ul>
</details>

**Discussion**: Comments express concern about societal apathy toward the night sky, with one user noting that greenhouses in British Columbia cause devastating light pollution. Another user praises presence-sensing lights in a park that turn on only when people walk by, preserving darkness for wildlife. Users also call for better engineering standards, arguing that glare from bare bulbs could be reduced by preventing direct line-of-sight to the light source.

**Tags**: `#light pollution`, `#LED lighting`, `#astronomy`, `#urban planning`, `#environmental impact`

---

<a id="item-7"></a>
## [EU Biometric Data Sharing with US for Visa-Free Travel Sparks Privacy Debate](https://edri.org/our-work/the-eu-is-about-to-sell-our-most-sensitive-data-to-the-us-for-visa-free-travel/) ⭐️ 8.0/10

The European Union is moving to share biometric data of travelers with the US to maintain visa-free travel under the Visa Waiver Program, sparking privacy concerns. This decision could set a precedent for mass cross-border sharing of sensitive biometric data, affecting millions of travelers and potentially eroding privacy protections in the EU. The data includes facial images and fingerprints, which are already collected at US borders for visa applicants and at EU borders under the new Entry/Exit System (EES).

hackernews · rapnie · Jul 20, 12:14 · [Discussion](https://news.ycombinator.com/item?id=48977711)

**Background**: The Visa Waiver Program allows citizens of participating countries to travel to the US for up to 90 days without a visa, but requires travelers to obtain an ESTA authorization online. Currently, biometric data (fingerprints and photo) are collected upon arrival in the US for most travelers. The EU's proposed data sharing would transmit this data in advance, potentially reducing border processing time but raising privacy concerns.

<details><summary>References</summary>
<ul>
<li><a href="https://fastercapital.com/content/Data-sharing--Data-Sharing-Agreements-and-Protocols-for-Business-Data-Privacy.html">Data sharing : Data Sharing Agreements and... - FasterCapital</a></li>
<li><a href="https://www.travelandtourworld.com/news/article/uk-tourists-to-face-biometric-registration-in-italy-greece-france-spain-and-portugal-as-new-border-rules-take-effect/">UK Tourists To Face Biometric Registration... - Travel And Tour World</a></li>
<li><a href="https://www.hindustantimes.com/world/eu-threatens-to-suspend-data-sharing-with-us/story-y0vazdh1OzoDn7jDTx1mjI.html">EU threatens to suspend data - sharing with US - Hindustan Times</a></li>

</ul>
</details>

**Discussion**: Comments highlight that biometric data is already collected at borders, framing the debate as convenience vs. privacy. Some question the scope of data sharing and whether it differs from current practices, while others argue that visa-free travel already requires extensive data disclosure.

**Tags**: `#privacy`, `#EU-US data sharing`, `#biometric data`, `#travel policy`, `#surveillance`

---

<a id="item-8"></a>
## [Kimi K3, Qwen 3.8 Open-Source Releases; Anthropic Tensions](https://www.emergingtrajectories.com/lh/frontier-lab-economics/) ⭐️ 8.0/10

Moonshot AI released Kimi K3, a 2.8-trillion-parameter open-source model, and Alibaba released Qwen 3.8, a 2.4-trillion-parameter multimodal model, within days of each other. Meanwhile, controversy surrounds Anthropic over the departure of its CPO from Figma's board amid the launch of a competing tool. These releases signal a trend of frontier-level open-weight models becoming freely available, intensifying competition and potentially commoditizing AI capabilities. The Anthropic-Figma incident highlights growing tensions around product strategy and trust in the AI industry. Kimi K3 is the largest open-source model to date with 2.8 trillion parameters, while Qwen 3.8 uses a sparse Mixture-of-Experts architecture and supports text, images, video, and documents. Both feature 1-million-token context windows, rivaling top proprietary models.

hackernews · cl42 · Jul 20, 15:13 · [Discussion](https://news.ycombinator.com/item?id=48980019)

**Background**: Open-weight models are AI models whose parameters are publicly released, allowing anyone to download, fine-tune, and deploy them. Frontier AI labs have been debating whether to open-source their most capable models, with China's firms often taking a more open approach. The Anthropic-Figma controversy involves potential conflicts of interest when a board member resigns before a competing product launch.

<details><summary>References</summary>
<ul>
<li><a href="https://venturebeat.com/technology/chinas-moonshot-ai-releases-kimi-k3-the-largest-open-source-model-ever-rivaling-top-u-s-systems">China’s Moonshot AI releases Kimi K3, the largest open-source model ever, rivaling top U.S. systems | VentureBeat</a></li>
<li><a href="https://the-decoder.com/alibabas-qwen-takes-on-kimi-k3-with-open-weight-qwen-3-8-says-model-is-second-only-to-fable-5/">Alibaba's Qwen takes on Kimi K3 with open-weight Qwen 3.8, says model is "second only to Fable 5"</a></li>
<li><a href="https://mlq.ai/news/alibaba-launches-qwen-38-with-24-trillion-parameters-claims-near-frontier-performance/">Alibaba Launches Qwen 3.8 With 2.4 Trillion Parameters, Claims Near-Frontier Performance | MLQ News</a></li>

</ul>
</details>

**Discussion**: Community comments highlight the potential for ASIC specialization to become a key differentiator, with LLMs aiding chip design. Others discuss the Figma controversy as a breach of trust, while some argue that the value of frontier models justifies their cost and that hype cycles are shortening, possibly indicating a plateau.

**Tags**: `#AI`, `#open-source`, `#frontier labs`, `#business strategy`, `#community discussion`

---

<a id="item-9"></a>
## [Ben Thompson Proposes Fair Use Law for AI Training](https://simonwillison.net/2026/Jul/20/afraid-of-chinese-models/#atom-everything) ⭐️ 8.0/10

Ben Thompson proposes that the U.S. pass a law making data collection for AI training explicitly fair use and barring terms of service that forbid model distillation, aiming to help U.S. open-weight models compete with Chinese counterparts. This proposal addresses the hypocrisy of AI labs that ban distillation on their models while training on unlicensed data, and could level the playing field by fostering innovation through open-weight models, impacting the global AI competition between the U.S. and China. Ben Thompson also theorizes that Alibaba's reversal to release Qwen 3.8 Max as open weights may have been influenced by a recent speech from Xi Jinping encouraging open source and sharing.

rss · Simon Willison · Jul 20, 17:09

**Background**: Model distillation is a technique where knowledge from a large 'teacher' model is transferred to a smaller 'student' model, often by querying the teacher's API. The legal status of using copyrighted data for AI training under fair use is currently contested. Open-weight models allow anyone to download and run the model, democratizing access. This proposal aims to balance copyright concerns with the need for innovation in AI.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>
<li><a href="https://www.skadden.com/insights/publications/2025/05/copyright-office-report">Copyright Office Weighs In on AI Training and Fair Use | Skadden, Arps, Slate, Meagher & Flom LLP</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#open weights`, `#distillation`, `#fair use`, `#Chinese AI models`

---

<a id="item-10"></a>
## [Hugging Face Discloses AI Agent Attack, Commercial LLM Refuses Forensics Help](https://huggingface.co/blog/security-incident-july-2026) ⭐️ 8.0/10

Hugging Face disclosed a security incident in July 2026 where attackers exploited code execution vulnerabilities in the dataset processing pipeline, using an autonomous AI agent framework to move laterally and steal credentials and datasets. During incident response, a commercial LLM API refused to assist forensic analysis due to safety guardrails, forcing Hugging Face to switch to a locally deployed GLM 5.2 model, which successfully analyzed over 17,000 attack records. This incident highlights the emerging threat of AI-agent-driven attacks on AI infrastructure and the limitations of closed-source commercial LLMs in security-critical forensic tasks. It underscores the importance of open-source models that can be deployed locally for sensitive operations without restrictive guardrails. The attack exploited two code execution vulnerabilities in Hugging Face's dataset processing pipeline, performed tens of thousands of operations over a weekend, and stole some internal datasets and service credentials. Hugging Face confirmed that public models, datasets, and Spaces were not tampered with, and the software supply chain showed no anomalies.

telegram · zaihuapd · Jul 20, 10:41

**Background**: Hugging Face is a major platform for hosting and sharing machine learning models and datasets. AI agents are autonomous systems that can execute tasks like browsing the web or calling APIs, and they face novel attack surfaces such as prompt injection. GLM 5.2 is a large language model developed by Z.ai (formerly Zhipu AI), released under the MIT License, supporting a 1M-token context and designed for long-horizon tasks. The incident shows how open-source models can be crucial for forensic analysis when commercial APIs impose restrictions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GLM_5.2">GLM 5.2</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/GLM-5.2 · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#AI安全`, `#Hugging Face`, `#安全事件`, `#大模型`, `#取证`

---

<a id="item-11"></a>
## [US may restrict firms from using Chinese open-weight AI models](https://www.axios.com/2026/07/20/ai-us-china-open-source-kimi) ⭐️ 8.0/10

Axios reported that the Trump administration is considering re-imposing restrictions on American companies using cost-effective Chinese open-weight AI models like Kimi K3, citing the model's strong performance. This could reshape the global AI competitive landscape, potentially forcing US companies away from cheaper, high-performing open-weight models and reinforcing the dominance of closed-source providers like OpenAI and Anthropic. The administration may use soft measures like procurement rules, entity list threats, and public pressure rather than a hard ban; White House AI advisor David Sacks criticized the move as an attempt by closed-source giants to eliminate open-source competition.

telegram · zaihuapd · Jul 20, 11:49

**Background**: Open-weight AI models provide access to trained weights, offering more control and cost efficiency than fully closed models, but are not fully open-source. Kimi K3, a Chinese model with nearly 3 trillion parameters and a 1M token context, has demonstrated frontier-level performance rivaling US counterparts at a lower cost. US-China tech rivalry has intensified, with previous attempts to restrict Chinese AI being blocked by officials favoring deregulation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/open-weight-ai-what-we-finally-opened-bonnet-nicolas-pistorio-n3ulf">Open - weight AI : what if we finally opened the bonnet ?</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2025/04/open-weight-models/">What are Open Source and Open Weight Models ? | Analytics Vidhya</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/worlds-largest-agent-from-china-challenge-us">World's first 3-trillion model from China does weeks of work in hours</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#open-source models`, `#geopolitics`, `#Kimi K3`, `#US-China tech rivalry`

---

<a id="item-12"></a>
## [US military apps found embedded with Chinese/Russian code](https://www.wired.com/story/apps-marketed-to-us-troops-are-shipping-chinese-and-russian-code/) ⭐️ 8.0/10

A new study from Purdue University and others found that nearly two-thirds of over 220 apps promoted to US troops contain third-party code from China and Russia, including Huawei's SDK, raising national security concerns. This exposes software supply chain vulnerabilities in military-related apps, potentially allowing adversaries to access sensitive data or activate hidden code remotely, threatening operational security. The study analyzed 220+ apps including base reviews, uniforms, banking, and dating services. While no data was observed flowing to Huawei servers yet, the SDK can receive remote updates that could activate dormant malicious code.

telegram · zaihuapd · Jul 20, 13:42

**Background**: Software supply chain security involves ensuring that third-party components integrated into an application do not introduce vulnerabilities. The US military has previously reported adversaries using commercial location data to surveil troops in the Middle East. The Huawei SDK is particularly concerning because Huawei is designated a national security threat by the US government.

<details><summary>References</summary>
<ul>
<li><a href="https://www.darkreading.com/vulnerabilities-threats/rising-tide-of-software-supply-chain-attacks">The Rising Tide of Software Supply Chain Attacks</a></li>
<li><a href="https://developer.huawei.com/consumer/en/">HUAWEI Developers</a></li>

</ul>
</details>

**Tags**: `#supply chain security`, `#national security`, `#mobile apps`, `#Huawei SDK`, `#software vulnerabilities`

---

<a id="item-13"></a>
## [Zhipu AI Completes All-Domestic Chip Datacenter](https://www.bloomberg.com/news/articles/2026-07-20/z-ai-completes-giant-data-center-with-chinese-chips-to-train-ai) ⭐️ 8.0/10

Zhipu AI has completed a 1-gigawatt data center powered entirely by Chinese-made chips, one of the largest facilities built by an AI lab in China, and has begun partial operations. This milestone demonstrates China's growing ability to build large-scale AI infrastructure without relying on foreign chips, reducing vulnerability to export restrictions and advancing domestic AI self-sufficiency. The data center has a power capacity of 1 GW, enough to supply about 750,000 households, and will support the development of Zhipu's GLM model family. Zhipu AI already operates multiple computing clusters each with over 10,000 chips.

telegram · zaihuapd · Jul 20, 15:43

**Background**: Zhipu AI is a leading Chinese AI company behind the GLM series of large language models, including the open-source GLM-4.5 and the 745-billion-parameter GLM-5. US sanctions have restricted exports of advanced chips like NVIDIA GPUs to China, prompting Chinese AI labs to develop alternatives using domestic processors such as Huawei Ascend and Cambricon.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Z.ai">Z. ai - Wikipedia</a></li>
<li><a href="https://glm5.ai/">GLM -5 - Zhipu AI 's Flagship Foundation Model</a></li>
<li><a href="https://glm45.org/">GLM -4.5 - by Zhipu AI</a></li>

</ul>
</details>

**Tags**: `#AI`, `#datacenter`, `#domestic chips`, `#China`, `#infrastructure`

---