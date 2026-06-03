# Microsoft Build 2026 | Opening Keynote

**Source:** https://www.youtube.com/watch?v=FFMm454fxNA  
**Video ID:** `FFMm454fxNA`

---

## Overview
Microsoft Build 2026 opened with a rallying call to developers to “participate fully in the frontier intelligence ecosystem.” Satya Nadella and other leaders walked through a layered AI stack—from edge compute to cloud services—showcasing new hardware, software tools, and an end‑to‑end platform for building, running, and governing agentic AI. The keynote highlighted groundbreaking devices (Surface RTX Spark, Project Solara form‑factors), new AI models, an expanded Azure data‑center strategy, and a suite of developer‑centric services (Foundry, Agent 365, GitHub Copilot app, Rayfin SDK, MX‑containers, Web IQ, etc.) aimed at making AI development faster, safer, and more ubiquitous.

## New Features & Announcements
- **Surface RTX Spark DevBox** — A “dream machine” with 1 PFLOP AI compute, 20 CPU cores, 128 GB unified memory; available Fall 2024 (public preview).  
- **Project Solara** — New agent‑first devices (stationary “Dedicated Ambian” and portable “badge”) built on a unified AOSP‑based platform; preview now.  
- **Windows 365 Developer Distribution** — Optimized cloud developer environment with intelligent terminal (GitHub Copilot built‑in) and expanded Linux tooling; GA later 2024.  
- **MX‑Containers (MXC)** — OS‑native policy layer for isolation of long‑running agents on Windows/WSL; GA in upcoming Windows release.  
- **Web IQ** — Model‑agnostic web‑grounding service for agents (search, images, video) with best‑in‑class quality, speed, and cost; preview now.  
- **Foundry IQ & Fabric IQ** — Unified intelligence layers combining external web data, enterprise knowledge, and operational telemetry for agents; preview today.  
- **Agent 365 SDK v1.0** — Public preview for building, securing, and managing agents across clouds (Azure, AWS, GCP).  
- **Rayfin SDK** — Agent‑first backend‑as‑a‑service enabling one‑click deployment to Azure Fabric; GA Q4 2024.  
- **MAI Model Family** — Seven new models (MAI Image 2.5/Flash, MAI Transcribe 1.5, MAI Voice 2/Flash, MAI Thinking One, MAI Code 1 Flash) released in private preview on Foundry; public rollout mid‑2025.  
- **Microsoft Discovery** — New scientific‑discovery platform that orchestrates agentic loops, HPC, and lab automation; GA announced.  
- **Majorana 2 Quantum Chip** — Next‑generation topological qubit with ~20‑second coherence, 1,000× improvement over Majorana 1; prototype announced.

## Topics Covered
- **AI Stack Overview** – Edge compute (Windows ML, local AI), model/context/tools layer, runtime for agents, security & governance.  
- **Hardware Innovation** – Intel, Qualcomm, NVIDIA SOCs; Surface Ultra and RTX Spark devices; next‑gen PC SOCs.  
- **Developer Experience** – New dev environment (vertical task bar, PowerToys, WSL containers with GPU), intelligent terminal with Copilot, local 120‑B parameter model usage.  
- **Agent Runtime & Security** – MX‑Containers for isolation, Agent 365 control plane, Defender & Purview extensions for AI workloads.  
- **Cloud Infrastructure** – Azure data‑center expansion, Fairwater AI super‑factory, new NVIDIA H100‑class GPUs, Cobalt 00 VMs for agent workloads.  
- **Project Solara** – Purpose‑built agent devices (stationary and badge) with enterprise‑grade security and context awareness.  
- **Microsoft IQ Stack** – Web IQ, Fabric IQ, Work IQ delivering unified, token‑efficient context for agents.  
- **Foundry Platform** – Toolbox, rubric evaluation, agent optimizer, auto‑tuning, long‑running agents in Teams/M365.  
- **GitHub Copilot App & Rayfin** – Multi‑session agentic coding, canvas UI, one‑click backend deployment.  
- **Security Harness (MDASH)** – Multi‑agent vulnerability scanning and auto‑remediation for code.  
- **Frontier Tuning & Custom Models** – RLEs for domain‑specific training, hill‑climbing loops, private evals.  
- **Partnerships** – NVIDIA (hardware & DGX), Mayo Clinic (healthcare frontier model), Chainsmokers (venture perspective), Fireworks AI (model catalog).  
- **Quantum Advances** – Majorana 2 chip, roadmap to scalable quantum computing.  
- **Vision & Call to Action** – Emphasis on “humanist superintelligence,” open ecosystem, and building AI that augments rather than replaces humans.

## Key Takeaways
- The future of AI development is **agent‑first**, with local, edge, and cloud agents collaborating seamlessly.  
- **Unmetered intelligence** is now possible on developer machines (Surface RTX Spark) and even on a desktop‑sized DGX‑style station.  
- Microsoft is delivering a **full stack**—hardware, OS, tooling, security, and cloud services—so developers can focus on value creation rather than infrastructure.  
- **Security and governance** are baked into the platform (MXC, Agent 365, Defender, Purview), essential for long‑running autonomous agents.  
- **Project Solara** showcases a new form‑factor paradigm: agents live on purpose‑built devices ranging from desk units to wearable badges.  
- **Foundry** and **Agent 365** provide end‑to‑end pipelines for building, testing, optimizing, and deploying agents at enterprise scale.  
- Microsoft’s **MAI model family** and **frontier tuning** let developers fine‑tune models on their own data while retaining full ownership.  
- The **quantum roadmap** (Majorana 2) signals continued investment in fundamental compute breakthroughs that will feed future AI workloads.  
- The overarching message: AI is a **tool for developers and enterprises**, not a replace‑all technology; the goal is to expand opportunity and agency.

## Notable Quotes
- “It’s not about any one piece of technology… it’s about the **value you can build** on top of the platform.”  
- “We are **extending the developer endpoints to the cloud** – Windows 365 is the developer distribution optimized for productivity.”  
- “The PC evolved from being a **personal computer to a personal AI**.” – Jensen Huang  
- “Agents change the whole nature of the device… **the agent becomes the center of your digital experience**.”  
- “The question isn’t whether we can build the next great model—**it’s how we build the frontier ecosystem together**.” – Satya Nadella  
- “We want AI that **places humanity first**, not replaces it.” – Mustafa, MAI team.

---

## Podcast Script

**JORDAN:** Welcome to Episode 20 of SlackCasts by PodSlacker — where AI does the watching so you can do the listening. If you want a richer experience with today's episode, visit PodSlacker dot com slash SlackCasts — you'll find a written summary, key frame moments from the video, and an interactive AI chat to explore the topic as deep as you like. Now let's get into it.

**MIKE:** Let’s kick off with the big picture Satya painted: an AI stack that spans from the edge all the way to the cloud, with dedicated layers for models, context, tooling, runtime, and governance. It’s a classic “full‑stack” play, but the devil is in the details.

**JORDAN:** Right, the edge compute layer now includes Windows ML on every PC, plus device‑specific NPUs from Intel, Qualcomm, and NVIDIA’s new PC‑SOC. The claim is “unmetered intelligence” on the local machine—think Outlook summarization, PowerPoint design suggestions, Teams super‑resolution—all running without a round‑trip to Azure.

**MIKE:** And that’s where the Surface RTX Spark DevBox comes in—a “dream machine” with 1 PFLOP AI compute, 20 CPU cores, and 128 GB unified memory. It’s positioned as the developer’s go‑to for training 120‑billion‑parameter models locally, which is a huge shift from today’s 10‑billion‑parameter norm.

**JORDAN:** The DevBox also ships with a pre‑configured dev environment: vertical task bar, PowerToys Grab & Move, an intelligent terminal with built‑in GitHub Copilot, and a curated set of 70+ Linux utilities—including native Homebrew. All of that is version‑controlled via a public GitHub repo so you can spin up the exact same stack on any Windows machine.

**MIKE:** Speaking of the terminal, the “intelligent terminal” lets you pick an agent—most people use Copilot, but you could swap in a custom agent that speaks your company’s internal LLM. It pipes the agent’s output to a lower pane while you keep coding in the upper pane—essentially a live “human‑in‑the‑loop” CI.

**JORDAN:** That ties directly into the new MX‑Containers (MXC) OS‑native policy layer. MXC adds process‑level and session‑level isolation for long‑running agents, enforced by the OS rather than just a hypervisor. It works across Windows, WSL, and even Windows 365 isolated VMs, giving enterprises the security guarantees needed for autonomous code.

**MIKE:** On the cloud side, Azure’s data‑center expansion is massive—over 500 regions with the “Fairwater AI super‑factory” built on NVIDIA H100‑class GPUs and the new Cobalt 00 VMs. The focus is on tokens‑per‑dollar‑per‑watt, leveraging custom power‑delivery architectures and near‑zero water cooling, which pushes the cost of token generation down by an order of magnitude.

**JORDAN:** And the hardware story doesn’t stop at GPUs. Microsoft is previewing the next‑gen NVIDIA‑in‑PC SOCs—think the Surface Ultra, which combines CPU, GPU, and AI accelerator on a single die with unified memory and DRTM. That’s the foundation for the Surface RTX Spark’s 1 PFLOP claim and the upcoming DGX‑style desktop “data center on your desk.”

**MIKE:** The next logical piece is Project Solara. It’s an agent‑first hardware platform with two form factors: the stationary “Dedicated Ambian” desk unit and the wearable “badge.” Both run on an AOSP‑based Microsoft device ecosystem, expose a just‑in‑time UI, and are designed to be secure enough for healthcare, finance, and field‑service scenarios.

**JORDAN:** Solara’s design is deliberately modular. You can swap sensors, change screen sizes, or replace the AI model bundle without rewriting the OS stack. It’s essentially a hardware abstraction layer for agents, enabling developers to target niche verticals—from nurse triage badges to retail floor‑assistant kiosks.

**MIKE:** Underpinning those edge experiences is the Microsoft IQ stack—Web IQ, Fabric IQ, and Work IQ. Web IQ is a model‑agnostic web‑grounding service that pulls in search, images, and video with best‑in‑class latency and cost. Fabric IQ merges that external knowledge with enterprise data sources, and Work IQ injects procedural knowledge from SharePoint, Teams, and Power Platform.

**JORDAN:** The stack is exposed through Foundry IQ, which aggregates the three IQ layers into a single, token‑efficient context source for agents. In the demo, an agent in a power‑grid control center queried Web IQ for external pricing, Fabric IQ for real‑time telemetry, and Work IQ for the operational playbook—all in a single, coherent request.

**MIKE:** Foundry itself is a full‑stack platform for building, testing, and deploying agents. New features include a toolbox for adding tools once and surfacing them via a single MCP endpoint, rubric‑based automatic evaluation, an agent optimizer that hill‑climbs model, prompt, and tool configurations, and built‑in microVM sandboxing for isolation.

**JORDAN:** On the developer‑productivity front, the GitHub Copilot app is now a “Copilot super app” with multi‑session canvases, integrated terminals, and one‑click deployment to Rayfin. Rayfin SDK is the BaaS layer that abstracts away the backend—spin up an Azure Fabric tenant, hook your agent’s data stores, and you’re live. Rayfin is slated GA in Q4 2024.

**MIKE:** Security got its own spotlight with MDASH, the Multimodel Agentic Security Harness. It orchestrates over a hundred specialized agents to scan code, find AI‑specific vulnerabilities, and even auto‑remediate via the Defender fix command. The idea is to have “agent‑powered” security that can keep pace with the rapid iteration of agentic code.

**JORDAN:** That dovetails with the Agent 365 SDK v1.0, which now supports cross‑cloud deployment (Azure, AWS, GCP) and integrates with Defender, Purview, and the new MXC isolation primitives. It gives each agent a first‑class identity and policy envelope, so you can enforce least‑privilege at the granularity of a single tool call.

**MIKE:** Model-wise, Microsoft announced the MAI family—seven new models covering image generation (MAI Image 2.5/Flash), transcription (MAI Transcribe 1.5), voice (MAI Voice 2/Flash), reasoning (MAI Thinking One), and coding (MAI Code 1 Flash). They’re private‑preview on Foundry now, with public rollout slated for mid‑2025, and they’re all water‑marked and hardened for enterprise use.

**JORDAN:** The frontier‑tuning capability is the real differentiator. Using Reinforcement Learning Environments (RLEs) you can fine‑tune any MAI model on your own data, keep the trained weights, and maintain full data lineage. That’s how Microsoft claims to achieve 10× cost efficiency versus GPT‑5.5 on domain‑specific tasks.

**MIKE:** Partnerships were also front‑and‑center: NVIDIA for the SOCs and the Grace Blackwell super‑computers, Mayo Clinic for a healthcare‑focused frontier model, Fireworks AI adding their model catalog to Foundry, and the Chainsmokers as investors highlighting the “agent‑as‑product” mindset.

**JORDAN:** On the quantum frontier, they unveiled Majorana 2—a topological qubit chip with coherence times up to 20 seconds, a 1,000× improvement over Majorana 1. The chip maintains the same 0.1 mm footprint, meaning you could theoretically pack a million of them on a credit‑card‑sized board.

**MIKE:** That quantum push is framed as an enabler for future AI workloads—especially scientific discovery. The new Microsoft Discovery platform stitches together agentic loops, HPC, and lab automation to run continuous hypothesis‑testing cycles. Their demo showed an agent designing a recyclable plastic protein, running molecular simulations, and auto‑generating lab protocols.

**JORDAN:** To bring all this back to developers, the key takeaways are: you can now run PFLOP‑scale models locally on a Surface RTX Spark, you have OS‑native isolation via MX‑Containers, you can tap into a unified IQ layer for context, and you can govern agents end‑to‑end with Agent 365 and MDASH. All of that sits on a cloud fabric that’s aggressively optimizing token‑per‑watt economics.

**MIKE:** And strategically, Microsoft is betting that the “agent‑first” paradigm will become the new OS abstraction. Agents become the center of the digital experience, not the screen. That means new form factors, new security models, and a new developer workflow where code generation, runtime, and governance are all AI‑augmented.

**JORDAN:** For anyone building today, the concrete steps are clear: grab the Surface RTX Spark preview or spin up a Windows 365 DevBox, enable MX‑Containers, connect to Foundry, pick a MAI model, and start iterating with Frontier Tuning. Then, if you need a custom backend, reach for Rayfin.

**MIKE:** And don’t forget the ecosystem hooks—publish your agent to Teams or Copilot, expose it via the new Copilot app marketplace, and let the autopilot “Scout” in M365 start handling routine tasks for you. The whole stack is designed for “discoverability” so your agents can be found and reused across the Microsoft graph.

**JORDAN:** In short, Build 2026 isn’t just about new silicon; it’s about a cohesive stack that lets you build, run, secure, and scale agents from a laptop to a quantum‑enabled data center. The frontier ecosystem is open, but it’s also tightly coupled—every layer reinforces the next.

**MIKE:** That’s the promise of a “humanist superintelligence”—AI that augments human agency across every tier, from the bare metal to the cloud, without extracting control. If you can keep the token economy efficient and the governance robust, the upside for developers, enterprises, and even scientific research is massive.

**JORDAN:** That wraps up our deep dive. Thanks for sticking with us through the hardware specs, the software stack, and the bold vision.

**MIKE:** As always, keep experimenting with the new tools, stay secure with MX‑Containers, and think about where you want your agents to live—maybe on a Solara badge in the field, maybe on a Surface RTX Spark on your desk.

**JORDAN:** That's a wrap on today's SlackCast. Head over to PodSlacker dot com slash SlackCasts for the written summary, visual key moments, and an AI chat to dive even deeper into today's topic. Until next time — slack off smarter.

