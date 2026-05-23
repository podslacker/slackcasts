# What's new with Gemini Enterprise app

**Source:** https://www.youtube.com/watch?v=Tc3IiGNmXHc  
**Video ID:** `Tc3IiGNmXHc`

---

## Overview  
The session announced new capabilities for **Gemini Enterprise**, focusing on the launch of the **Gemini Enterprise Agent platform** and a suite of application‑level features that let every employee create, run, and manage AI agents across the company. Jamie Deggeer (Google Cloud AI) and a panel of customers demonstrated how the platform integrates with Google Workspace, Slack, and other tools, and showed real‑world use cases such as loan‑processing automation at a bank. The goal is to make AI‑driven workflows secure, low‑code, and enterprise‑grade.

## New Features & Announcements  

- **Gemini Enterprise Agent Platform** — Provides a cloud‑first, enterprise‑grade foundation that bundles Vertex AI models (including Anthropic Claude and open‑source options), data‑grounding tools, and new governance services (agent gateway, identity service, registry, skill registry).  
  Availability: General Preview (some components GA)

- **No‑Code Agent Designer** — Drag‑and‑drop editor that lets users build agents, define guardrails, and set policies without writing code, while still supporting long‑running, sandboxed agents that can execute code, browse the web, and access enterprise systems.  
  Availability: Public Preview  

- **Inbox** — Unified notification center where employees see all background agents, manage alerts, and respond via Slack, mobile, email, or other clients.  
  Availability: Public Preview  

- **Skills** — Personalizable reusable “skills” that encode repeatable procedures and can be attached to any agent.  
  Availability: Public Preview  

- **Canvas** – Integrated document/slide creation tool that lets agents generate rich outputs (HTML reports, PowerPoint decks) that can be opened directly in Google Workspace or Microsoft 365.  
  Availability: Public Preview  

- **Projects** – Shared spaces with persistent context, conversation history, and data, enabling collaborative work between humans and digital agents.  
  Availability: Public Preview  

- **Built‑in Connectors** – Over 50 first‑party integrations (e.g., ServiceNow, internal MCP servers) and the ability to add custom connectors, plus personalized ranking of data for each employee.  
  Availability: Public Preview  

## Topics Covered  

- **Introduction & Adoption** – Gemini Enterprise launched Oct 2023; early adopters like Anaplan (80 % employee usage) and Macquarie Bank (40 % help‑center self‑service lift).  
- **Agent Platform Architecture** – Combines Vertex AI models, grounding tools, and new governance services into a single platform.  
- **Application Layer (Gemini Enterprise app)** – How the app surfaces agents, connectors, and front‑end experiences (web, mobile, Slack, Workspace).  
- **No‑Code vs. Full‑Code Agents** – Explains the yin‑yang of long‑running sandboxed agents (full code) and policy‑driven no‑code agents, enabling deterministic outcomes.  
- **Inbox & Notification Management** – Central hub for background‑agent activity, customizable delivery channels.  
- **Skills, Canvas, Projects** – Tools for reusable procedures, rich content generation, and shared collaborative workspaces.  
- **Live Demo: Loan‑Processing Automation** – Shows a bank building a full‑code loan supervisor agent, wrapping it in a no‑code schedule/guardrail flow, creating ServiceNow incidents, summarizing results, and generating a slide deck via Canvas, all accessible through Slack mentions.  
- **Customer Perspectives** – Brief remarks from KPMG (Aaron Purcell) and Signal Iduna (Lisa Nabb) on real‑world impact.  

## Key Takeaways  

- Gemini Enterprise now offers a **single, cloud‑first platform** for building, governing, and deploying AI agents at scale.  
- The **no‑code designer** lowers the barrier for business users while still supporting sophisticated, sandboxed agents for complex tasks.  
- **Governance** (agent gateway, identity, registry) ensures security, compliance, and policy enforcement across the organization.  
- New UI features—**Inbox, Skills, Canvas, Projects**—turn AI from a chat‑based assistant into a collaborative, background workhorse.  
- Real‑world demos prove the platform can **automate high‑value, regulated processes** (e.g., loan underwriting) and integrate with existing ITSM tools like ServiceNow.  
- Employees can interact with agents **through multiple surfaces** (Workspace, Slack, mobile) without leaving their preferred workflow.  

## Notable Quotes  

- “**Gemini Enterprise is the front door to AI in the workplace** – it gives every employee the ability to leverage AI and agents connected to all of your enterprise data.”  
- “**We’re shifting from a world where employees chat with an AI assistant to a world where a team of agents works in the background** and surfaces results only when needed.”  
- “**Long‑running agents can have a sandboxed file system, run for days, execute code, use a browser, and still be governed by your security policies**.”  
- “**Inbox gives you a view of all of your agents operating in the background and the ability to manage notifications** across Slack, mobile, email, etc.”  
- “**Projects allow employees to work in one shared space with a fixed set of context and data, collaborating with both human and digital co‑workers**.”

---

## Podcast Script

**JORDAN:** Hey everyone, welcome back to the podcast! I’m Jordan, your go‑to for the nitty‑gritty of new tech.

**MIKE:** And I’m Mike, here to chew on the big picture and what it means for you at work. Today we’re diving into Google’s Gemini Enterprise launch from the recent Next conference.

**JORDAN:** The headline is the Gemini Enterprise Agent platform—basically a cloud‑first, enterprise‑grade hub that lets any employee spin up AI agents without writing code.

**MIKE:** That’s huge because it moves AI from a “specialist tool” to something every desk can tap into, like emailing a teammate but with an AI on the other end.

**JORDAN:** Exactly. The platform bundles Vertex AI, access to models like Anthropic’s Claude, and a whole suite of governance features—an agent gateway, identity service, and registries.

**MIKE:** And those governance bits are crucial for large orgs; they can finally keep a lid on what agents can do, where they pull data, and who they talk to.

**JORDAN:** They also announced a no‑code agent designer. It lets you build long‑running agents that can code, browse, and even create tools inside a secure sandbox, all while you set policy guardrails.

**MIKE:** So a loan officer could have an AI that processes applications overnight, but the bank still dictates the compliance checks and escalation paths.

**JORDAN:** Right, and the demo showed a bank creating a “loan supervisor” agent that fetched unprocessed mortgages, flagged risky cases, and even opened a ServiceNow ticket for human review.

**MIKE:** That workflow illustrates the shift from “ask‑and‑wait” chats to background agents that work autonomously and only ping you when you’re needed.

**JORDAN:** To keep track of all those silent helpers, Gemini introduces an “Inbox” view—think of it as a control center where you see every agent’s status, notifications, and can reply from Slack, email, or the mobile app.

**MIKE:** That multi‑surface integration is key for adoption; people can stay in the tools they already love while the AI does the heavy lifting.

**JORDAN:** They also rolled out “Skills” for reusable procedures, “Canvas” for generating documents and decks, and “Projects” for shared, long‑running contexts that blend human and digital teammates.

**MIKE:** In practice, a marketing team could co‑author a campaign brief with an AI, have it auto‑populate slides in PowerPoint, and push updates straight to Google Workspace—all from one project space.

**JORDAN:** Customer anecdotes reinforce the impact: Anaplan reports 80 % employee usage and thousands of no‑code agents, while Macquarie Bank saw a 40 % boost in help‑center self‑service after deploying Gemini agents.

**MIKE:** Those numbers suggest real productivity gains, not just a shiny demo. It’ll be interesting to see how quickly other sectors—like healthcare or manufacturing—catch on.

**JORDAN:** So to sum up, Gemini Enterprise gives enterprises a secure, cloud‑native stack for building, governing, and scaling AI agents, with no‑code tools and deep integration into existing workflows.

**MIKE:** And for the rest of us, that means AI assistants could become as routine as Outlook or Slack, handling complex tasks behind the scenes while we focus on the strategic work.

**JORDAN:** That’s a wrap on today’s deep dive. Thanks for listening, and keep an eye on how AI agents evolve in your own organization.

**MIKE:** Thanks, everybody! Until next time, stay curious and keep experimenting with the future of work.

