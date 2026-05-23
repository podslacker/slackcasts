# What's new in Google Cloud's agent platform

**Source:** https://www.youtube.com/watch?v=FxnjRYo3fpU  
**Video ID:** `FxnjRYo3fpU`

---

## Overview  
The session provides a deep dive into Google Cloud’s **Agent Platform**, showing how it has evolved from the early Agent Development Kit (ADK) demos to a full‑stack, production‑grade solution. Aman Khan (Product Manager) and Lavi (DevRel) walk through new capabilities, real‑world customer use cases, and the integrated governance, scaling, and optimization tools that let enterprises move agents from prototype to enterprise‑wide deployment. The talk emphasizes the platform’s end‑to‑end nature—combining Gemini Enterprise, a unified runtime, and built‑in security—to turn “race‑car” AI agents into reliable, governed business assets.

## New Features & Announcements  

- **Graph‑based orchestration** – Model business processes with branches, loops, and conditional paths.  
- **Agent collaboration** – Decompose complex tasks across specialized agents instead of a single monolith.  
- **Batch & event‑driven workflows** – Enable real‑time reactions to system events, not just human prompts.  
- **Native skill definitions** – Define a skill once in ADK and reuse it across all agents.  
- **Agent CLI & built‑in skills** – One‑stop command‑line tool for scaffolding, evaluating, deploying, and observing agents; works with Cloud Code, Gemini CLI, etc., or directly from a terminal.  
- **Sub‑second cold‑start runtime** – Faster start‑up for production agents serving thousands to millions of users.  
- **Bring‑Your‑Own‑Container support** – Run agents in custom environments when strict requirements exist.  
- **Long‑running single‑plan execution (up to 7 days)** – Agents can operate autonomously without human intervention.  
- **Bidirectional streaming** – Low‑latency, two‑way communication for more interactive use cases.  
- **Session service & memory bank** – Persistent, framework‑agnostic memory so agents retain context across sessions.  
- **Code‑execution sandboxes & GUI interaction sandbox** – Secure environments where agents can run code or control desktop‑style interfaces.  
- **Agent Identity (GA)** – Granular, auditable permission management for agents, like any other org user.  
- **Agent Registry (GA)** – Central inventory of all registered agents, their tools, and service access.  
- **Model armor** – Real‑time protection against prompt injection and data leakage.  
- **Proactive threat management** – Built‑in monitoring for suspicious agent behavior.  
- **Agent Gateway (GA)** – Control plane for routing and securing agent traffic with fine‑grained tool access and extensibility.  

## Topics Covered  

- **Historical context** – Recap of ADK launch, early demos (autonomous plant store), and the shift from chatbot‑centric demos to full‑stack agents.  
- **Strategic vision** – Analogy of “race‑car” agents vs. traditional software; need for step‑function improvements and integrated governance.  
- **Architecture overview** – How Gemini Enterprise feeds users, while the Agent Platform provides runtime, registry, gateway, identity, observability, and evaluation on top of Google Cloud’s AI stack (Hypercomputer, Agentic Data Cloud, Agent Defense).  
- **Developer experience** – Emphasis on ease of use, open‑source tooling, and collaborative environment for AI engineers, product managers, and developers.  
- **ADK enhancements** – Graph orchestration, agent collaboration, event‑driven workflows, reusable skill definitions.  
- **Agent CLI** – Scaffolding, evaluation, deployment, observability; integration paths with existing coding agents or direct terminal use.  
- **Production scalability** – Sub‑second cold starts, BYOC, long‑running autonomous plans, bidirectional streaming.  
- **Memory & context** – Session service, persistent memory bank, custom session fields for feedback signals.  
- **Sandbox capabilities** – Secure code execution, custom containers, GUI automation sandbox.  
- **Governance stack** – End‑to‑end identity, registry, model armor, threat management, and Agent Gateway as a unified control plane; focus on making governance built‑in rather than an afterthought.  
- **Optimization & evaluation** – Leveraging DeepMind research tools for online/offline evals, continuous monitoring, and automated performance tuning.  
- **Customer examples** – Brief mentions of L’Oréal, Gautier, and Thomas using the platform in production workflows.  

## Key Takeaways  

- The Agent Platform is now a vertically integrated, production‑ready stack that lets enterprises build, scale, govern, and optimize AI agents without stitching together multiple vendors.  
- New ADK features (graph orchestration, collaboration, event‑driven flows) enable modeling of real‑world business processes.  
- The Agent CLI dramatically simplifies the end‑to‑end lifecycle—from scaffolding to observability.  
- Runtime improvements (sub‑second cold starts, BYOC, 7‑day autonomous execution) make large‑scale deployments feasible.  
- Persistent memory and sandboxed execution turn agents from simple chatbots into autonomous, context‑aware workers.  
- Governance is baked in: identity, registry, model armor, threat management, and the Agent Gateway provide enterprise‑grade security and auditability out of the box.  
- Optimization tools inherited from DeepMind give teams research‑grade evaluation without needing internal AI‑labs.  

## Notable Quotes  

- “Everyone can get in a Toyota Camry and drive it… but with agents we’re building Formula 1 race cars.”  
- “Agents shouldn’t start from scratch with every conversation. Without memory, your agent has no idea what happened yesterday.”  
- “Governance should span from prototype to production, and it includes the perimeters and boundaries to define what your agent can and cannot do.”  
- “We provide you with an army of researchers throughout the Agent Platform so you don’t have to staff one yourself.”

---

## Podcast Script

**JORDAN:** Hey everyone, welcome back to the podcast! I'm Jordan, your detail‑driven host, and today we're breaking down the latest Google Agent Platform announcement.

**MIKE:** And I’m Mike, here to connect the dots to the real world. We’ve got a big room‑scale update to unpack—governance, production‑grade agents, and even a demo from L’Oréal. Let’s dive in.

**JORDAN:** The keynote reminded us that a year ago we were all about the Agent Development Kit, the ADK, and simple chatbot demos. Since then, Google added governance layers and deployment tools to take prototypes to production.

**MIKE:** Right, and that shift is huge for businesses. Moving from a “toy car” chatbot to a “Formula 1” autonomous agent means you can actually put AI on the front line of revenue‑generating processes.

**JORDAN:** They used a car analogy—Camry versus race car—to illustrate the difference between traditional software and these new agents. The point is you can’t just floor it; you need guardrails.

**MIKE:** Which brings us to the guardrails: the platform now bundles Gemini Enterprise for user access and the Agent Platform for developers, so data and agents flow without that “hand‑off tax.”

**JORDAN:** At the core, the stack includes runtime, registry, gateway, identity, observability, and evals, all on Google Cloud’s AI hypercomputer. It’s a vertically integrated solution, eliminating the need to stitch together five vendors.

**MIKE:** That integration is a game‑changer for enterprises. Less vendor sprawl means faster time‑to‑value and tighter security—something every CISO is itchy to hear about.

**JORDAN:** Speaking of security, the new Agent Identity feature lets you manage permissions just like any other user, with granular controls. Plus, model armor blocks prompt injection and data leaks in real time.

**MIKE:** And the Agent Gateway acts as a control plane, letting you set policies on tool access. Imagine being able to enforce compliance across thousands of agents with a single dashboard.

**JORDAN:** On the developer side, the ADK now supports graph‑based orchestration, agent collaboration, and batch/event‑driven workflows. You can define reusable skills once and plug them everywhere.

**MIKE:** That reusability is key for scaling. A marketing team could spin up a campaign‑assistant agent, then hand it off to support without rebuilding the whole pipeline.

**JORDAN:** They also introduced an Agent CLI that scaffolds, evaluates, deploys, and monitors agents—either through existing coding agents like Cloud Code or directly from the terminal. It even supports bring‑your‑own‑container for custom runtimes.

**MIKE:** That flexibility means teams don’t have to lock into one stack. Whether you’re a Python shop or a Java shop, you can get sub‑second cold starts and run agents continuously for up to seven days.

**JORDAN:** Memory and session management have been upgraded, too. Agents now have persistent memory banks, so they remember user preferences across sessions and can learn over time.

**MIKE:** Persistent memory turns a one‑off chatbot into a personal assistant that actually improves, which is exactly what enterprises need to justify AI spend.

**JORDAN:** Finally, the optimization layer pulls in DeepMind‑style evals, both online and offline, giving you continuous monitoring without hiring a research army.

**MIKE:** So in a nutshell, Google’s platform is stacking building, scaling, governing, and optimizing into one cohesive offering—making it easier for anyone from engineers to compliance officers to ship trustworthy agents.

**JORDAN:** That’s the takeaway: a unified stack that takes you from idea to production with built‑in governance and performance.

**MIKE:** And with all those guardrails, real‑world teams can finally let agents drive business outcomes without worrying about flying blind.

**JORDAN:** Thanks for joining us, and a big thanks to the Google team for the deep dive.

**MIKE:** We’ll be back soon with more tech breakdowns—stay curious, stay safe, and see you next time!

