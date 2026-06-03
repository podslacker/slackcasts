# Microsoft Build 2026 | Opening Keynote

**Source:** https://www.youtube.com/watch?v=FFMm454fxNA  
**Video ID:** `FFMm454fxNA`

---

## Overview  
The opening keynote at Microsoft Build 2026 set the stage for a “frontier intelligence ecosystem,” emphasizing that value comes not from a single technology but from what developers build on top of the AI stack. Satya Nadella and the engineering team walked through the full AI stack—from ubiquitous edge‑to‑cloud compute, through models, tooling, runtime, and governance—highlighting new Windows‑based AI capabilities, next‑gen hardware, and a suite of developer tools designed to enable un‑metered, locally‑run intelligence.

## New Features & Announcements  

- **Windows AI Models (INVOX‑Eye On Instruct & INVOX‑Eye Plan)** – Local reasoning and planning models that run fully on Windows devices, enabling agentic applications without cloud calls.  
- **Surface Ultra** – New Windows PC built on NVIDIA’s next‑gen AI‑centric SoC with 128 GB unified memory, 2K display, and all‑day battery. Timeline: Fall 2026. Availability: General.  
- **Surface RTX DevBox (Spark)** – “Dream machine” developer workstation with 1 peta‑FLOP AI compute, 20 CPU cores, 128 GB unified memory. Timeline: Fall 2026. Availability: Private preview → General.  
- **Intelligent Terminal with GitHub Copilot** – Integrated terminal that hosts a Copilot‑powered AI agent to assist code writing, debugging, and command execution. Availability: Public preview.  
- **Vertical Task Bar** – New UI option in Windows Insider builds allowing the task bar to be docked on the left side. Availability: Insider now, GA later.  
- **Full Linux Tooling & 70+ CLI Utilities on Windows** – Native support for utilities (e.g., `grep`, `head`, `touch`) and package managers like Homebrew, plus first‑class container support leveraging GPU acceleration. Availability: Public preview.  
- **Windows 365 Developer Distribution** – Cloud‑based Windows environment optimized for developer productivity, featuring the same tooling as the local RTX DevBox. Availability: General now.  

## Topics Covered  

- **The AI Stack** – Described as layers of compute fabric (edge + cloud), models & context, runtime agents, tooling, and governance.  
- **Edge Compute on Windows** – Examples of on‑device AI in Outlook, PowerPoint, Teams, and the broader Windows ML ecosystem.  
- **Partner Hardware Ecosystem** – Highlights of Intel, Qualcomm, and NVIDIA contributions, culminating in the NVIDIA‑based SoC powering Surface devices.  
- **Surface RTX DevBox Demo** – Live showcase of configuring a dev environment (vertical task bar, PowerToys, WSL containers, GPU‑accelerated local LLMs up to 120 B parameters).  
- **Intelligent Development Experience** – Demonstrated Copilot‑driven terminal, voice‑activated coding, and local log‑analysis using the INVOX models.  
- **Azure Data Center Strategy** – Discussed token‑per‑dollar‑per‑watt optimization, sustainability principles, and the “AI super‑factory” design (two‑story NVIDIA‑dense architecture, zero‑water‑consumption cooling).  
- **Silicon Partnerships** – Collaboration with NVIDIA, AMD (NX generation GPU) to deliver higher token efficiency for cloud workloads.  

## Key Takeaways  

- The future of AI development is a seamless blend of edge and cloud, with Windows positioned as the unifying platform.  
- New local AI models (INVOX) enable full‑agentic loops on devices, eliminating the need for constant cloud calls.  
- The Surface RTX DevBox provides unprecedented on‑premise compute for developers, supporting massive local LLMs and GPU‑accelerated containers.  
- Integrated developer tools—Intelligent Terminal, vertical task bar, extensive Linux utilities—create a frictionless dev experience on Windows.  
- Azure’s data‑center expansion is guided by sustainability and community impact while delivering massive token‑efficiency gains.  
- Partner hardware (NVIDIA, AMD, Qualcomm, Intel) is critical to delivering the unified memory, AI‑centric SoC, and performance needed for un‑metered intelligence.  

## Notable Quotes  

- “It is not about any one piece of technology… it is about the value that you can build, you can compound, you can create on top of the platform.”  
- “We are delivering a dream machine… 1 peta‑flop of AI compute, 20 CPU cores, 128 GB of unified memory.”  
- “The beginning of un‑metered intelligence—models and agents running in parallel on the device and in the cloud.”  
- “Tokens per dollar per watt is the driving equation; everything we build is optimized around that metric.”

---

## Podcast Script

**JORDAN:** Welcome to Episode 20 of SlackCasts by PodSlacker — where AI does the watching so you can do the listening. If you want a richer experience with today's episode, visit PodSlacker dot com slash SlackCasts — you'll find a written summary, key frame moments from the video, and an interactive AI chat to explore the topic as deep as you like. Now let's get into it.

**MIKE:** Satya's keynote framed the whole Build as a “frontier intelligence ecosystem.” It wasn’t just hype; he emphasized that real value emerges from the layers developers stitch together on top of the AI stack.

**JORDAN:** Right, the stack he outlined starts with a ubiquitous compute fabric that stretches from edge devices all the way to Azure’s hyperscale data centers, then layers models, context, tooling, runtime agents, and finally governance.

**MIKE:** That hierarchy is crucial because it tells us where to invest our effort. If you can push compute to the edge, you reduce latency and token costs, which aligns with the “tokens per dollar per watt” metric they keep repeating.

**JORDAN:** Speaking of edge, Microsoft showcased on‑device AI already baked into Outlook summarization, PowerPoint text‑to‑speech, and Teams super‑resolution—all powered by Windows ML and the GPU/NPU pool on every Windows PC.

**MIKE:** It’s a bold claim: “full install base of GPUs” meaning even a mid‑range Surface can host local inference. That opens the door to truly offline experiences.

**JORDAN:** The first concrete manifestation of that claim are the INVOX‑Eye On Instruct and INVOX‑Eye Plan models. Both run entirely on Windows devices, giving you a reasoning engine and a planning engine without a single cloud round‑trip.

**MIKE:** And because they’re local, you can close the agentic loop—grant the model tool‑access, let it read files, call APIs, and act autonomously, all while staying on‑prem. That’s a game‑changer for regulated industries.

**JORDAN:** To make those models practical, Microsoft introduced two new hardware platforms. The Surface Ultra, built on NVIDIA’s next‑gen AI‑centric SoC, ships with 128 GB of unified memory and a 2K display, targeting power users who need on‑device reasoning.

**MIKE:** Then there’s the Surface RTX DevBox, code‑named “Spark.” It’s marketed as a “dream machine” with 1 peta‑FLOP AI compute, 20 CPU cores, and the same 128 GB unified memory. That’s essentially a desktop‑sized AI super‑computer.

**JORDAN:** The DevBox isn’t just raw silicon; they shipped a pre‑configured dev environment. Python, Node, PowerToys, the vertical task bar, and a WSL2 container stack that can run GPU‑accelerated workloads out of the box.

**MIKE:** The vertical task bar is a small UI tweak, but it signals a broader shift toward developer ergonomics on Windows—customizable, distraction‑free workspaces that feel native.

**JORDAN:** And they didn’t stop at UI. The Intelligent Terminal now embeds a GitHub Copilot agent. You can summon the agent, have it write or refactor code, debug, even execute shell commands—all from within the same pane.

**MIKE:** That tight integration reduces context switching. I liked the demo where they used voice‑activated Copilot to refactor logging statements across a codebase, delegating sub‑tasks to the local INVOX model.

**JORDAN:** Under the hood, the terminal also pulls in a massive Linux tooling set—over 70 CLI utilities like `grep`, `head`, `touch`, plus Homebrew support, all natively on Windows. That bridges the Windows‑Linux developer divide.

**MIKE:** It’s a strategic move for cross‑platform teams. You can spin up a container, leverage the GPU, and use familiar Linux tools without leaving the Windows ecosystem.

**JORDAN:** The demo also showed loading a 120‑billion‑parameter LLM locally on the RTX DevBox, consuming about 90 GB of GPU RAM and processing 3.4 million tokens on‑device. That’s unprecedented for a laptop‑class form factor.

**MIKE:** When you think about token cost, running that locally eliminates any Azure egress fees and dramatically cuts latency for code‑completion or log‑analysis workloads.

**JORDAN:** Speaking of Azure, Satya pivoted to the data‑center strategy, reinforcing the token‑per‑dollar‑per‑watt equation. They highlighted the “AI super‑factory” in Georgia and Wisconsin—a two‑story, NVIDIA‑dense architecture with zero‑water cooling.

**MIKE:** The sustainability angle is more than PR. Zero water consumption, localized power delivery, and community investment are now part of the business case for scaling AI workloads.

**JORDAN:** They also mentioned the massive expansion—over 500 Azure regions, with more capacity added in the last 18 months than in the previous decade. That infrastructure underpins the hybrid edge‑cloud model they’re advocating.

**MIKE:** The hybrid model relies heavily on silicon partners. NVIDIA provides the AI‑centric SoC for Surface devices, while AMD’s upcoming NX‑generation GPU promises a 30 % improvement in tokens per dollar versus current leading GPUs.

**JORDAN:** Intel and Qualcomm were also referenced. Qualcomm’s Snapdragon X targets high‑end laptops, and their lower‑tier roadmap aims at sub‑$500 PCs, widening the edge compute envelope.

**MIKE:** It’s a clear signal that Microsoft is not playing a single‑vendor game; they’re building a hardware‑agnostic stack that can ingest compute from any partner SoC.

**JORDAN:** Another interesting piece is Windows 365 Developer Distribution. It mirrors the RTX DevBox toolchain in the cloud, letting developers spin up identical environments without provisioning physical hardware.

**MIKE:** That’s critical for team consistency. If you develop locally on a Surface Ultra and test in Windows 365, you get the same unified memory, same model versions, same tooling—no “works on my machine” surprises.

**JORDAN:** The keynote also introduced the “Intelligent Terminal” as a public preview, and the vertical task bar is already rolling out to Insider builds. Both are tangible, near‑term developer efficiencies.

**MIKE:** From a strategic standpoint, those incremental upgrades lower the barrier for adoption of on‑device AI, moving the market from cloud‑only inference toward a truly distributed intelligence fabric.

**JORDAN:** To sum up the new features: INVOX local models, Surface Ultra hardware, Surface RTX DevBox with petaflop compute, Copilot‑powered terminal, vertical task bar, 70+ native Linux CLI tools, and Windows 365 developer distro—all aimed at un‑metered intelligence.

**MIKE:** The big picture is that Microsoft wants Windows to be the universal substrate where edge, cloud, and developer tooling converge, with sustainability and community impact baked into the data‑center roadmap.

**JORDAN:** For engineers, the immediate takeaways are: start experimenting with INVOX models on any Windows machine, explore the Intelligent Terminal for AI‑assisted scripting, and consider the RTX DevBox or Windows 365 for large‑scale local model work.

**MIKE:** And for architects, factor in token‑per‑dollar‑per‑watt when sizing workloads—leveraging on‑device inference wherever possible, and reserving cloud bursts for training or heavy inference that truly need scale.

**JORDAN:** That aligns with the “frontier intelligence ecosystem” mantra—value isn’t in any single component but in how we compose them into end‑to‑end solutions.

**MIKE:** Exactly. If you can compose edge compute, local models, unified tooling, and cloud‑scale back‑ends, you’ll unlock new business models that were impossible a year ago.

**JORDAN:** Before we close, a quick nod to the community commitments—zero‑water data centers, local job creation, and training programs—those are the social contracts that allow such aggressive infrastructure rollouts.

**MIKE:** It’s a reminder that technology and policy are intertwined. Sustainable, community‑first data centers make the whole ecosystem viable long term.

**JORDAN:** That’s a wrap on today’s SlackCast. Head over to PodSlacker dot com slash SlackCasts for the written summary, visual key moments, and an AI chat to dive even deeper into today's topic. Until next time — slack off smarter.

