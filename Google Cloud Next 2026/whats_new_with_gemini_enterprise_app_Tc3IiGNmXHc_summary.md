# What's new with Gemini Enterprise app

**Source:** https://www.youtube.com/watch?v=Tc3IiGNmXHc  
**Video ID:** `Tc3IiGNmXHc`

---

## Overview
The session provides an update on **Gemini Enterprise**, focusing on the newly launched **Gemini Enterprise Agent platform** and enhancements to the Gemini Enterprise application. Jamie Deggeer, product leader on Google Cloud AI, walks through how the platform enables employees to create and use AI agents—both long‑running code‑enabled agents and no‑code agents with guardrails—across the enterprise. Real‑world examples from KPMG and Signal Iduna illustrate adoption, and a live demo shows a banking loan‑processing workflow.

## New Features & Announcements
- **Gemini Enterprise Agent Platform** — A cloud‑first, enterprise‑grade foundation that bundles Vertex AI, multiple LLM providers, an agent gateway, identity service, registry, and skill/registry tools.  
  Availability: General Availability (GA).

- **No‑Code Agent Designer** — Drag‑and‑drop UI for building agents, defining policies/guardrails, and orchestrating long‑running tasks without writing code.  
  Availability: Public Preview.

- **Inbox** — Central view for all background agents, with configurable notifications to mobile, Slack, email, etc.  
  Availability: GA.

- **Skills & Canvas** – Employees can author reusable “skills” (procedures) and generate documents/presentations directly within Gemini Enterprise.  
  Availability: GA.

- **Projects** – Shared workspaces that preserve context, conversation history, and data for collaborative human‑and‑agent teams.  
  Availability: GA.

- **Integrations** – Over 50 first‑party connectors plus ability to add custom connectors via MCP servers; seamless linking to Workspace, Slack, ServiceNow, and other enterprise tools.  
  Availability: GA.

## Topics Covered
- **Introduction & Adoption** – Gemini Enterprise launched Oct 2023; strong uptake (e.g., 80 % of Anaplan staff using it, Macquarie Bank’s 40 % help‑center self‑service lift).  
- **Agent Platform Architecture** – Combines Vertex AI models (including Anthropic Claude and open‑source) with data grounding, system connectors, and governance services (gateway, identity, registry).  
- **Application Layer Enhancements** – How the Gemini Enterprise app surfaces agents, rankings, and cross‑system connectors to end users.  
- **No‑Code vs. Code‑Enabled Agents** – Explanation of long‑running sandboxed agents that can write code, browse, and execute tools, versus no‑code agents that enforce deterministic policies.  
- **Inbox & Notification Management** – Unified dashboard for monitoring agent activity and routing updates to preferred channels.  
- **Skills, Canvas, Projects** – Tools for codifying repeatable procedures, generating artifacts, and collaborating in shared contexts.  
- **Live Demo: Loan‑Processing Use Case** – Shows creation of a full‑code loan supervisor agent, wrapping it with a no‑code scheduled agent, handling human‑review loops, auto‑creating ServiceNow incidents, summarizing results, and producing a slide deck via Canvas—all accessible from Slack/Workspace.  
- **Customer Perspectives** – Brief remarks from KPMG’s Aaron Purcell and Signal Iduna’s Lisa Nabb on enterprise adoption (details to follow in separate sessions).  

## Key Takeaways
- Gemini Enterprise now offers a **complete agent platform** that couples powerful LLMs with enterprise‑grade governance and integration capabilities.  
- **No‑code designer** lets business users build safe, policy‑driven agents without developers, while **code‑enabled agents** handle complex, long‑running tasks in secure sandboxes.  
- The **Inbox** centralizes agent monitoring and lets employees choose how and where they receive updates.  
- Integrated **Skills, Canvas, and Projects** turn AI outputs into reusable procedures, polished documents, and collaborative workspaces.  
- Real‑world demos confirm that agents can automate end‑to‑end processes (e.g., loan underwriting), trigger human review, log incidents in ServiceNow, and surface results in familiar tools like Slack and Workspace.  
- Early adopters (Anaplan, Macquarie Bank, KPMG, Signal Iduna) report significant productivity gains and higher self‑service rates, indicating strong enterprise value.

## Notable Quotes
- “Gemini Enterprise is the front door to AI in the workplace… it gives every employee the ability to leverage AI and agents connected to all of your enterprise data.”  
- “We allow you to combine long‑running agents with a no‑code editor that lets you create guardrails and policies… to have deterministic outcomes.”  
- “It shifts from a world where employees go to an AI assistant synchronously to a world where a team of agents works in the background and only surfaces when you need input.”

---

## Podcast Script

**JORDAN:** Welcome to SlackCasts by PodSlacker — where AI does the watching so you can do the listening. If you want a richer experience with today's episode, visit PodSlacker dot com slash SlackCasts — you'll find a written summary, key frame moments from the video, and an interactive AI chat to explore the topic as deep as you like. Now let's get into it.

**MIKE:** Today we’re unpacking Google Cloud’s Gemini Enterprise update—specifically the GA launch of the Gemini Enterprise Agent Platform and the slew of application‑layer features that promise to turn every employee into an AI‑augmented worker.

**JORDAN:** Let’s start with the high‑level adoption story Jamie Deggeer shared: Gemini Enterprise went live in October 2023 and already sees 80 % of Anaplan’s workforce building thousands of no‑code agents, while Macquarie Bank reports a 40 % lift in help‑center self‑service thanks to agent‑driven fraud checks and personalized recommendations.

**MIKE:** Those numbers illustrate the strategic shift: AI moves from a “help‑desk” supplement to an integral part of day‑to‑day operations. The question is, how does the new platform technically enable that scale?

**JORDAN:** The Gemini Enterprise Agent Platform is a cloud‑first, enterprise‑grade stack that bundles Vertex AI, multi‑model support—including Google’s own models, Anthropic’s Claude, and open‑source options—with an agent gateway, identity service, registry, and skill/registry tools. All of this is delivered as a single managed surface, so you don’t have to stitch together disparate services.

**MIKE:** And the governance layer is crucial. The agent gateway enforces policy at the request edge, while the identity service handles per‑user authentication and fine‑grained access controls, ensuring that an agent can’t overstep its data‑access boundaries.

**JORDAN:** Right, plus the registry maintains a catalog of agents, skills, and connectors, exposing metadata that the Gemini Enterprise app uses to surface the “right agent” for a given query. That’s why, in the demo, when the user asked for “the latest 10 unprocessed mortgage loan applications,” the system automatically recommended the loan‑supervisor agent.

**MIKE:** Speaking of the app, let’s walk through the new application‑layer features. First up: the No‑Code Agent Designer, now in public preview. Jamie described it as a drag‑and‑drop canvas where business analysts can define workflows, guardrails, and conditional logic without writing a line of code.

**JORDAN:** The Designer also lets you embed long‑running, sandboxed agents as sub‑tasks. Those sandboxed agents run in a secure, isolated environment, can spin up temporary file systems, execute code, even launch a headless browser—all under the enterprise security policies you’ve defined in the gateway.

**MIKE:** That duality—long‑running code agents plus deterministic no‑code wrappers—addresses the classic “yin‑yang” enterprise demand: the need for sophisticated reasoning alongside predictable compliance.

**JORDAN:** Next, the Inbox feature, now GA, provides a unified view of all background agents. It aggregates status, error traces, and human‑review prompts, and pushes notifications to the user’s preferred channel—mobile app, Slack, email, or even Teams.

**MIKE:** That’s a big productivity win. Instead of monitoring dozens of dashboards, an employee can triage all pending agent actions from a single pane, and respond directly from the notification channel.

**JORDAN:** Then we have Skills and Canvas, both GA. Skills are reusable procedural primitives—think “run credit‑check” or “populate loan‑risk matrix”—that can be authored by any employee and referenced across agents. Canvas, on the other hand, lets agents generate rich artifacts: PowerPoint decks, Google Slides, Word docs, even PDFs, and opens them directly in Workspace or Microsoft 365.

**MIKE:** The synergy is clear: an agent can pull data, invoke a Skill to compute risk, and then hand‑off the result to Canvas to produce a polished slide deck—all without human intervention until a policy‑driven review step.

**JORDAN:** Projects are the third GA addition. A Project bundles a persistent context, shared conversation history, and a fixed data scope, enabling both human collaborators and digital agents to work side‑by‑side over weeks or months. Think of it as a version‑controlled AI workspace.

**MIKE:** That solves the “context loss” problem we’ve seen in earlier assistant models where each new chat starts from a clean slate. Projects keep the memory alive, which is essential for multi‑stage workflows like loan underwriting.

**JORDAN:** Let’s dive into the live demo. Jamie built a full‑code loan‑supervisor agent that runs in a sandbox, accesses a document retriever, calls a risk‑assessment sub‑agent, and validates compliance. The agent can run for days, persisting state across sessions.

**MIKE:** Then he wrapped that agent with a no‑code scheduler: a daily trigger that pulls the latest loan applications, feeds them to the code agent, and applies conditionals—if flagged for human review, fire a Slack notification and create a ServiceNow incident.

**JORDAN:** The demo showcased the end‑to‑end loop: the incident appears in ServiceNow, an email with a deep‑link lands in the loan officer’s inbox, and the officer can approve or deny directly from the notification, feeding a quality signal back into the agent’s reinforcement loop.

**MIKE:** That feedback loop is vital for continuous improvement. Over time the platform can adjust its confidence thresholds based on human approvals, reducing false positives without sacrificing compliance.

**JORDAN:** After the processing step, the loan supervisor emitted an HTML summary report, which the user immediately opened in Canvas to generate a slide deck. The slides were editable on the fly and then pushed to Google Workspace for sharing.

**MIKE:** And the cross‑surface integration? Jamie demonstrated an at‑mention of the loan‑supervisor agent inside a Slack channel, pulling the latest stats without leaving the chat. That’s the “agent as a first‑class citizen” model—agents can be invoked from any connected surface, be it Slack, Workspace, or a custom MCP connector.

**JORDAN:** On the connector side, Gemini Enterprise now supports over 50 first‑party integrations out of the box—ServiceNow, Salesforce, SAP, Snowflake, you name it—and you can add custom connectors via MCP servers, extending the agent’s reach to virtually any legacy system.

**MIKE:** The extensibility is a strategic differentiator. Enterprises can onboard legacy mainframes through a custom MCP shim, surface those APIs as Skills, and then let agents orchestrate across modern SaaS and on‑prem endpoints without rewriting business logic.

**JORDAN:** Jamie also highlighted DeepMind‑derived quality‑at‑scale innovations: automated evaluation pipelines that score agent outputs against ground‑truth datasets, feeding into a continuous model‑fine‑tuning loop. That’s how they maintain high fidelity across heterogeneous LLMs.

**MIKE:** Summarizing the key takeaways: GA of the Agent Platform gives us a unified, secure backbone; the No‑Code Designer democratizes agent creation; Inbox centralizes monitoring; Skills, Canvas, and Projects turn raw AI output into reusable, collaborative artifacts; and the demo proves that end‑to‑end loan processing—including human review, incident creation, and reporting—can be fully automated.

**MIKE:** For senior practitioners, the strategic implication is clear: you can now design a “team of agents” that operate asynchronously, only surfacing to humans when policy or judgment is required, dramatically reducing cycle time for high‑volume, compliance‑heavy processes.

**JORDAN:** And the early adopters—KPMG, Signal Iduna, Anaplan, Macquarie—are already reporting measurable productivity gains, which suggests that the platform is not just a proof‑of‑concept but a production‑ready foundation for AI‑first enterprises.

**JORDAN:** That's a wrap on today's SlackCast. Head over to PodSlacker dot com slash SlackCasts for the written summary, visual key moments, and an AI chat to dive even deeper into today's topic. Until next time — slack off smarter.

