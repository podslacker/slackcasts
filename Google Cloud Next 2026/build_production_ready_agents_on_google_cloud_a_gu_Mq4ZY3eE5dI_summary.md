# Build production-ready agents on Google Cloud: A guide for architects and CTOs

**Source:** https://www.youtube.com/watch?v=Mq4ZY3eE5dI  
**Video ID:** `Mq4ZY3eE5dI`

---

## Overview  
The session walks through how to design, build, and operate production‑ready AI agents on Google Cloud. Sita (Developer Relations), Kanchana Patola (Google Cloud), and Siddharth Jain (Ford Credit) share the four‑stage lifecycle—build, scale, govern, and optimize—along with concrete tools, architectural patterns, and real‑world lessons from Ford.  Emphasis is on making agents resilient, secure, and maintainable at scale.

## Topics Covered  

- **Agent development lifecycle** – Four buckets: **Build**, **Scale**, **Govern**, **Optimize**.  
- **Choosing the right “studio” for different personas** –  
  * *Agent Studio*: visual drag‑and‑drop for non‑coders.  
  * *Agent Garden*: pre‑built samples for low‑code users.  
  * *Agent Development Kit (ADK) + Agent CLI*: full‑code framework for engineers.  
- **Separating concerns** – Introduce three coordination layers:  
  * **MCP (Micro‑service Control Plane)** abstracts tool APIs from agents.  
  * **A2A (Agent‑to‑Agent)** protocol lets agents delegate work without custom glue code.  
  * **Skills** (markdown‑based rule packages) keep business logic out of LLM prompts, preserving context windows and cost.  
- **Scaling agents** – Decisions around **memory** (short‑term sessions vs. long‑term Memory Bank), **runtime** (local, Agent Platform Runtime, Cloud Run, GKE), and **build‑vs‑buy** trade‑offs.  Highlights the ready‑made **Agent Platform Sessions** (365‑day TTL) and **Memory Bank** (vector DB with async indexing).  
- **Governance by infrastructure** –  
  * **Agent Identity** (SPIFFE‑backed, automatic OAuth2/key handling).  
  * **Agent Registry** (single pane of glass for agents & tools).  
  * **Agent Policies** (IAM‑style and NL policies).  
  * **Agent Gateway** (central traffic monitor enforcing policies).  
- **Observability & evaluation** – Need logs, traces, metrics, plus systematic evaluation of an agent’s *trajectory* (not just output). Google Cloud’s monitoring suite provides the required telemetry.  
- **Ford Credit case study** – Siddharth demonstrates how Ford moved a loan‑approval workflow from prototype to production using the above stack, illustrating real‑world trade‑offs and ROI.  

## Key Takeaways  

- **Pick the right tool for the user**: visual canvas for SMEs, low‑code samples for developers, full SDK/CLI for engineers.  
- **Never tightly couple agents to external APIs**; use MCP as an abstraction layer to protect against schema changes.  
- **Use A2A and Skills to keep agents modular and context‑efficient**; put business rules in markdown files and let the platform load them on demand.  
- **Adopt the built‑in memory services first** (Agent Platform Sessions & Memory Bank) before rolling your own RAG pipelines.  
- **Select a runtime that matches feature needs, not just scale** – start with Agent Platform Runtime, move to Cloud Run or GKE only when required.  
- **Govern through identity, registry, policies, and gateway** rather than relying on prompt engineering; this yields reliable security and auditability.  
- **Instrument every agent** with logs, traces, and custom metrics; evaluate both *what* the agent returns and *how* it got there.  

## Notable Quotes  

- “If you write a Python call to an API directly inside the agent, you’re coupling the agent to that tool. When the API changes you have to rebuild the agent.”  
- “Skills are just a markdown file, but they let you keep business rules out of the LLM’s context window, saving latency and cost.”  
- “Agent governance is not a prompt‑engineering problem. You can’t just say ‘don’t delete the database’ and expect it to work every time.”  
- “The key is to build the logic, not the glue.”  
- “Observability and evaluation go hand‑in‑hand; you need to watch the agent’s trajectory, not just its final answer.”

---

## Podcast Script

**JORDAN:** Welcome to SlackCasts by PodSlacker — where AI does the watching so you can do the listening. If you want a richer experience with today's episode, visit PodSlacker dot com slash SlackCasts — you'll find a written summary, key frame moments from the video, and an interactive AI chat to explore the topic as deep as you like. Now let's get into it.

**MIKE:** Great to be back for the final session. I’m curious, Jordan—what’s the high‑level framing they gave at the start?

**JORDAN:** The speakers broke the agent lifecycle into four buckets: Build, Scale, Govern, and Optimize. It’s a clean lens to evaluate every decision, from tooling to observability.

**MIKE:** Right, and they emphasized that building agents isn’t just code anymore; it’s about the surrounding system. Let’s dive into the first bucket—building. What tooling options did they highlight for different personas?

**JORDAN:** They presented three tiers. Agent Studio is a drag‑and‑drop canvas for non‑technical subject‑matter experts. Agent Garden offers low‑code, pre‑built sample agents that can be deployed with a click. And the Agent Development Kit (ADK) plus the new Agent CLI give engineers a full‑code framework with primitives like complex graphs, human‑in‑the‑loop hooks, and sandboxed execution.

**MIKE:** That triage makes sense—match the tool to the user’s expertise. Did they say anything about moving assets between those tiers?

**JORDAN:** Yes. An SME can prototype in Studio, export the definition as an ADK‑compatible artifact, and hand it off to engineers for refinement and productionized deployment. The workflow is designed to be reversible, so code‑first agents can be visualized in Studio for stakeholder review.

**MIKE:** Nice. After you have an agent, the next principle is about “giving it skills.” How did they define that separation of concerns?

**JORDAN:** They introduced three coordination layers. First, MCP—the Micro‑service Control Plane—acts as an API abstraction so agents never call external services directly. Second, A2A—the Agent‑to‑Agent protocol—lets one agent delegate a sub‑task to another without custom glue code. Third, Skills are markdown‑based rule packages that house business constraints, keeping them out of the LLM prompt window.

**MIKE:** The MCP idea feels like a service mesh for agents. Did they give any concrete examples of MCP in action?

**JORDAN:** In the demo they showed a loan‑approval agent calling a credit‑check service. Instead of embedding the Python HTTP client, the agent issued a “invoke” to MCP, which routed the request, performed auth via SPIFFE, and returned a normalized response. When the credit API schema changed, only MCP needed updating.

**MIKE:** That eliminates the classic “break‑everything‑when‑the‑API‑evolves” problem. How about A2A—any real‑world delegation scenario?

**JORDAN:** They modeled a “document‑review” workflow where a front‑line chatbot hands off legal compliance verification to a specialized compliance agent. The handoff is a single A2A message containing the context ID; the compliance agent processes and returns a verdict, all tracked by the Agent Gateway.

**MIKE:** Speaking of the Gateway, that brings us into the Governance bucket. What pillars of governance did they outline?

**JORDAN:** Four pillars: Agent Identity, built on SPIFFE, which automatically provisions OAuth2 tokens and API keys; Agent Registry, a central inventory of agents and tools; Agent Policies, which can be IAM‑style or natural‑language rules; and Agent Gateway, which sits at ingress/egress, enforcing those policies and providing traffic visibility.

**MIKE:** I liked the comment that governance isn’t a prompt‑engineering fix. Did they illustrate any failure mode that prompting can’t solve?

**JORDAN:** They recounted an attempt to embed “never delete the database” in the system prompt. The LLM occasionally obeyed but also hallucinated, leading to accidental data loss. The takeaway: enforce such constraints via IAM policies on the Agent Gateway, not trust the LLM’s internal “ethics.”

**MIKE:** That’s a hard lesson. Moving on to scaling—what memory options are available out of the box?

**JORDAN:** Two services: Agent Platform Sessions for short‑term memory (default 365‑day TTL, auto‑provisioned for agents on the runtime) and Memory Bank, a managed vector store with asynchronous indexing for long‑term, retrieval‑augmented generation. Both integrate natively with ADK, so you don’t need to spin up a custom Pinecone or FAISS cluster.

**MIKE:** And they warned against over‑engineering memory. How do you decide whether you need short‑term versus long‑term storage?

**JORDAN:** First, ask if the agent’s use case truly depends on context. Stateless lookup agents can skip memory entirely. If you need to retain state across turns, use Sessions. If you need historical knowledge beyond a few hours—like compliance audit trails—or you want semantic search over prior interactions, enable Memory Bank.

**MIKE:** Got it. What about runtime choices? I recall they compared localhost, Agent Platform Runtime, Cloud Run, and GKE.

**JORDAN:** Exactly. Localhost is for dev and debugging. Agent Platform Runtime is the default production environment—provides built‑in memory, security, and human‑in‑the‑loop hooks. Cloud Run is the next step if you need container portability or custom dependencies. GKE is reserved for massive fleets where you need fine‑grained autoscaling, pod‑level networking, or custom GPUs. They emphasized “don’t over‑engineer the runtime before you have traffic.”

**MIKE:** Did they share any best‑practice regarding where to place the MCP component?

**JORDAN:** Yes. MCP runs as a Cloud Run service, which decouples the control plane from the agent runtime. This lets you update MCP independently, scale it horizontally, and keep the agent runtime stateless. The agents just reference the MCP endpoint via environment variables.

**MIKE:** That aligns with the micro‑services principle: separate data plane from control plane. Let’s talk about observability—the final principle. What telemetry stack did they recommend?

**JORDAN:** They leveraged Google Cloud’s Operations suite: Cloud Logging for structured logs, Cloud Trace for end‑to‑end request latency, Cloud Monitoring for custom metrics (e.g., “agent‑fallback‑rate”), and Cloud Profiler for CPU/memory hotspots. Additionally, they introduced an “Agent Evaluation” framework that records the decision trajectory—each state transition, tool invocation, and A2A delegation—to be scored either by predefined business KPIs or a secondary LLM.

**MIKE:** So you can measure not just the final answer but the path taken. Did they discuss any alerting patterns?

**JORDAN:** They set up alerts on policy violations detected by the Gateway, abnormal latency spikes in MCP calls, and sudden drops in success‑rate of Memory Bank lookups. Those alerts feed into PagerDuty for rapid incident response.

**MIKE:** That’s a comprehensive safety net. Now, the case study—what did Ford Credit actually build, and how did they apply all these concepts?

**JORDAN:** Siddharth walked through a loan‑approval pipeline. Initially, they built a prototype in Agent Studio that collected applicant data and called an internal credit‑score API directly. When they moved to production, they refactored the API calls into MCP, added an A2A handoff to a risk‑assessment agent, and stored applicant interaction history in Memory Bank for audit. They deployed the main agent on Agent Platform Runtime, used Cloud Run for the MCP, and enforced IAM policies via the Agent Gateway to restrict credit‑score access to the finance team’s service account.

**MIKE:** Any numbers on ROI or performance gains?

**JORDAN:** They reported a 40% reduction in average approval time, mainly due to eliminating manual handovers, and a 25% cost saving on LLM usage because Skills removed redundant business rules from the prompt. Plus, compliance audit time dropped because Memory Bank provided an immutable trace of every decision.

**MIKE:** Impressive. Did they mention any pitfalls they ran into during that migration?

**JORDAN:** Two main issues: first, they initially tried to embed all compliance clauses in the prompt, which blew up the context window and caused timeout errors. Switching to markdown Skills fixed that. Second, they underestimated the latency of MCP calls during peak loads, so they added a Cloud Run autoscaling rule with a minimum of 5 instances, which stabilized response times.

**MIKE:** Those are classic scaling lessons. Before we wrap, what are the key takeaways we want our listeners to remember?

**JORDAN:** 1) Match tooling to persona—Studio, Garden, or ADK. 2) Decouple agents from external APIs via MCP and keep inter‑agent communication standardized with A2A. 3) Externalize business rules into markdown Skills to protect context windows and reduce latency. 4) Start with built‑in memory services (Sessions, Memory Bank) before engineering custom RAG pipelines. 5) Choose the simplest runtime that satisfies security and human‑in‑the‑loop needs; upgrade to Cloud Run or GKE only when traffic demands. 6) Govern through SPIFFE‑backed identity, a central registry, policy enforcement, and a gateway—not via prompt tricks. 7) Instrument every layer—logs, traces, metrics—and evaluate the agent’s trajectory, not just its final answer.

**MIKE:** That’s a solid checklist for anyone looking to go from prototype to production. Any final thoughts from the panel?

**JORDAN:** Siddharth closed by reminding us that the “logic” is the differentiator; the “glue” should be reusable platform services. If you can offload glue to MCP, A2A, and the governance stack, you free up engineering bandwidth to innovate on the agent’s core intelligence.

**MIKE:** Well said. Thanks, Jordan, for dissecting this dense session.

**JORDAN:** My pleasure.

**JORDAN:** That's a wrap on today's SlackCast. Head over to PodSlacker dot com slash SlackCasts for the written summary, visual key moments, and an AI chat to dive even deeper into today's topic. Until next time — slack off smarter.

