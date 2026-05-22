# What's new in Google Cloud's agent platform

**Source:** https://www.youtube.com/watch?v=FxnjRYo3fpU  
**Video ID:** `FxnjRYo3fpU`

---

## Overview  
The session introduces the latest advancements in Google Cloud’s **Agent Platform**, showing how it has evolved from early chatbot‑centric demos to a full‑stack, production‑ready environment for building, deploying, and governing autonomous AI agents. Aman Khan (Product Manager, Agent Governance) and Lavi (DevRel) walk through new capabilities, real‑world customer adoptions, and the integrated “Gemini Enterprise + Agent Platform” experience that links end‑user surfaces with a unified backend. Emphasis is placed on stepping‑function improvements—governance, scalability, observability, and optimization—that let enterprises move safely from prototype to large‑scale, mission‑critical agents.

## New Features & Announcements  

- **Graph‑Based Orchestration** – Model business processes with branches, loops, and conditionals.  
  Availability: General  

- **Agent Collaboration** – Decompose complex tasks across specialized agents rather than a monolith.  
  Availability: General  

- **Batch & Event‑Driven Workflows** – Enable agents to react to real‑time system events.  
  Availability: General  

- **Native Skill Definitions in ADK** – Define a skill once and reuse it across all agents.  
  Availability: General  

- **Agent CLI & Built‑In Skills** – Command‑line tool for scaffolding, evaluating, deploying, and observing agents; works with Cloud Code, Gemini CLI, etc.  
  Availability: General  

- **Improved Runtime** – Sub‑second cold starts, “bring‑your‑own‑container” support, and single‑plan execution for up to 7 days without human intervention.  
  Availability: General  

- **Bidirectional Streaming** – Low‑latency, real‑time interaction streams for complex use cases.  
  Availability: General  

- **Sessions & Memory Bank** – Persistent, framework‑agnostic memory for agents to retain context, preferences, and feedback across conversations.  
  Availability: General  

- **Code Execution & GUI Sandboxes (GA)** – Secure environments where agents can run code or interact with graphical interfaces.  
  Availability: General  

- **Agent Identity (GA)** – Granular, auditable permission management for agents, similar to user IAM.  
  Availability: General  

- **Agent Registry (GA)** – Central inventory of all deployed agents, their tools, and service accesses.  
  Availability: General  

- **Model Armor & Proactive Threat Management** – Real‑time protection against prompt injection and data leakage.  
  Availability: General  

- **Agent Gateway** – Control plane for securing and governing agent traffic with extensible policies.  
  Availability: General  

- **DeepMind‑Backed Eval Framework** – Integrated online/offline evaluation and continuous monitoring tools for optimization.  
  Availability: General  

## Topics Covered  

- **Recap of the past year** – From ADK and early Agent Engine demos to the Agentic AI Cloud launch.  
- **Why agents now matter** – Analogy of race cars vs. regular cars; agents as high‑performance business engines needing guardrails.  
- **Unified stack vision** – Gemini Enterprise as the entry point for users; Agent Platform as the developer layer; underlying Google Cloud AI stack (Hypercomputer, Agentic Data Cloud, Agent Defense).  
- **Three pillar strategy** – Ecosystem & interoperability, ease of use/collaboration, and deep customizability.  
- **ADK enhancements** – Graph orchestration, collaboration, batch/event workflows, native skill definitions.  
- **Developer experience** – New Agent CLI, integration with existing coding agents, out‑of‑the‑box primitives.  
- **Production scaling** – Fast cold starts, container flexibility, long‑running single‑plan agents, bidirectional streaming.  
- **Memory & context** – Sessions, memory banks, custom session fields, enabling cumulative intelligence.  
- **Sandbox capabilities** – Code execution, custom containers, GUI interaction for real‑world task execution.  
- **Governance end‑to‑end** – Agent identity, registry, model armor, threat management, Agent Gateway; governance built into runtime, not an afterthought.  
- **Optimization & evaluation** – Leveraging DeepMind research, built‑in eval tools for continuous performance monitoring.  
- **Customer showcase** – Brief mentions of L’Oréal, Gautier, and Thomas using the platform in production workflows.  

## Key Takeaways  

- The Agent Platform now provides a **complete, vertically integrated stack** that takes agents from idea to production without stitching together multiple vendors.  
- **Governance, security, and compliance** are baked into the platform (identity, registry, model armor, gateway), making enterprise adoption safer.  
- New **developer tooling** (Agent CLI, native skill definitions) dramatically lowers the barrier to build, test, and deploy agents.  
- **Scalability improvements** (sub‑second cold starts, BYOC, 7‑day autonomous runs) enable agents to serve thousands to millions of users reliably.  
- Persistent **memory and session services** give agents long‑term context, turning them from simple chatbots into autonomous workhorses.  
- **Sandboxed execution** and GUI interaction expand agents’ ability to perform real‑world tasks while staying secure.  
- Integrated **evaluation and optimization** (DeepMind‑backed) lets teams continuously monitor and improve agent performance without deep research expertise.  

## Notable Quotes  

- “Everyone can get in a Toyota Camry and drive it… but with agents, we’re building Formula 1 race cars.”  
- “You can’t just put an electric car in self‑driving mode and floor it—that’s why we need guardrails.”  
- “Governance shouldn’t be bolted on as an afterthought; it has to span from prototype to production.”  
- “Agents shouldn’t start from scratch with every conversation—memory lets them remember yesterday’s preferences and learn over time.”

---

## Podcast Script

**JORDAN:** Hey everyone, welcome back to the podcast! I’m Jordan, here to dig into the nitty‑gritty of today’s tech news.

**MIKE:** And I’m Mike, ready to explore why it matters to you and your business. Today we’re breaking down Google’s new Agent Platform update that just dropped at their keynote.

**JORDAN:** The highlight is this vertically integrated stack that promises to take agents from a prototype straight to production without rebuilding the plumbing each time.

**MIKE:** That sounds like a game‑changer for companies trying to move beyond basic chatbots into real‑world automation.

**JORDAN:** Exactly. A year ago they introduced the Agent Engine and a bunch of demos, but now they’ve added governance, deployment, and a whole suite of runtime features.

**MIKE:** So it’s not just a fancy demo anymore—it’s meant for enterprise folks who need compliance, security, and scalability baked in.

**JORDAN:** One analogy that stuck with me was the Toyota Camry versus a Formula 1 race car. Traditional software is the Camry: reliable and steady. Agents are the race car—high‑performance but needing guardrails.

**MIKE:** Which is why the new governance layer is crucial. They talk about identity, permission granularity, and even model armor to block prompt injection.

**JORDAN:** The platform also introduces a new Agent CLI that scaffolds, evaluates, deploys, and monitors agents—all from the terminal or integrated into tools like Cloud Code.

**MIKE:** That lowers the barrier for dev teams that aren’t AI specialists, letting them spin up agents with familiar tooling.

**JORDAN:** On the scalability side, they’ve built sub‑second cold starts, support for bring‑your‑own containers, and even 7‑day autonomous runs without human touch.

**MIKE:** Imagine a customer‑service bot that can handle a surge of queries for a week straight, learning as it goes, without any manual redeployment.

**JORDAN:** Persistent memory is another key upgrade—sessions and a memory bank let agents remember preferences, past interactions, and even custom signals.

**MIKE:** That moves us from “answering questions” to truly autonomous assistants that can act on behalf of users over time.

**JORDAN:** Governance isn’t an afterthought either; the Agent Registry gives a global view of every agent, its tools, and its permissions, while the Agent Gateway acts as a control plane for traffic.

**MIKE:** In practice, a compliance officer could audit all agent activity across the company from a single dashboard—no more piecing together logs from disparate systems.

**JORDAN:** Finally, the optimization stack leverages DeepMind’s evaluation tools, providing online and offline evals, continuous monitoring, and research‑grade metrics without needing an internal AI lab.

**MIKE:** That means businesses can iterate faster, knowing their agents are meeting performance and safety benchmarks as they evolve.

**JORDAN:** To sum up, Google’s Agent Platform now offers a full lifecycle: build with ADK and the new CLI, scale with robust runtimes, govern end‑to‑end, and optimize with DeepMind‑backed evals.

**MIKE:** If you’ve been waiting for a trustworthy, production‑ready way to deploy AI agents, this might be the moment to start experimenting.

**JORDAN:** Thanks for tuning in, everyone. We’ll keep an eye on how early adopters like L’Oréal and Thomas roll this out in real workflows.

**MIKE:** Absolutely. Catch you next time for more deep dives into the tech shaping our future. Bye!

