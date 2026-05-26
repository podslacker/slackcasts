# From prototype to production: 45 minutes to a reliable Gemini Enterprise Agent Platform agent

**Source:** https://www.youtube.com/watch?v=fkCTifAqVGg  
**Video ID:** `fkCTifAqVGg`

---

## Overview
The session walks through how Booking.com transformed a handful of GenAI prototypes into production‑ready, agentic solutions using Google Gemini, Vertex AI, and the Gemini Enterprise Agent Platform. Alibek (Engineering Manager) and Maria (Software Engineer) describe Booking.com’s scale, AI journey, and four real‑world use cases, followed by Google specialists who share best‑practice principles for evaluating, deploying, securing, and monitoring agents in production.

## Topics Covered
- **Booking.com’s scale & AI heritage** – Over 6.8 billion guest arrivals, 175 k destinations, and a decade of predictive ML serving ~500 k requests/second at <50 ms latency.  
- **Evolution of the GenAI ecosystem** – From early “wrapper” experiments (2023) → multi‑provider stack (early 2024) → unified gateway with governance and monitoring, culminating in a comprehensive AI lifecycle platform.  
- **Customer‑facing use case: “Know Before You Go”** – An itinerary‑planning agent that combines Gemini with Google Maps and search grounding to give travelers transport routes, activity suggestions, and personalized itineraries.  
- **Internal use case: “Big Bot”** – A data‑registry chatbot for Booking.com employees that retrieves internal assets and creates workflows via natural language.  
- **Partner analytics use case** – Extraction of traveler pain points from reviews/comments, turning unstructured feedback into actionable themes for partners.  
- **Multimodal use case: “Reels to Reality”** – Converts short‑form travel videos (YouTube URLs) into concrete itineraries, showcasing Gemini’s ability to ingest video alongside text.  
- **Serving‑strategy lessons** – Matching Vertex AI serving options (on‑demand, provisioned throughput, priority processing) to specific workload needs; “one size does not fit all.”  
- **Platform adoption & knowledge sharing** – Emphasis on self‑service, documentation, hackathons, and clear guidance to help teams move from experiment to production.  
- **Google Cloud production principles** – (Presented by Manasa & Naz) four pillars: evaluation (response vs. trajectory), rapid code‑to‑cloud migration, identity & security at deployment, and observability/auditability. Demonstrated with a travel‑assistant demo (London Travel Concierge) that integrates weather data, ticketing, activities, Agent Engine, and Model Armor.  
- **Evaluation techniques** – Human review, LLM‑as‑judge for response evaluation, automated metrics (hallucination, groundedness, coherence), and trajectory‑level metrics that inspect tool calls and parameter usage.  

## Key Takeaways
- Building reliable agents is as much about **serving architecture and governance** as it is about model selection.  
- **Tailored Vertex AI serving tiers** (on‑demand, provisioned, priority) are essential to meet latency, throughput, and multimodal requirements.  
- A **governed, multi‑provider ecosystem** enables rapid scaling of diverse use cases while maintaining safety and compliance.  
- Effective **knowledge sharing** (docs, hackathons, self‑service portals) accelerates adoption across large organizations.  
- **Agent evaluation** must consider both final outputs (response) and internal behavior (trajectory) to ensure correctness and tool usage.  
- Using an **LLM as a judge** provides scalable, consistent feedback for response evaluation, though it has limits for complex tasks.  
- **Security and observability** (identity, Model Armor, audit logs) are non‑negotiable for production agents handling proprietary or external data.  

## Notable Quotes
- “One size does **not** fit all when it comes to serving tiers.” – Maria, on matching Vertex AI serving options to workload needs.  
- “Building the platform is only half the job; the other half is helping users understand what’s available and how to get started.” – Maria, highlighting the importance of knowledge sharing.  
- “If I had to summarize our journey in one sentence, it would be: Booking.com has moved from isolated GenAI experiments to a governed multi‑provider production‑ready AI ecosystem.” – Maria.  
- “Agents are non‑deterministic, which brings unique challenges to evaluation – we need both response and trajectory metrics.” – Naz, on agent evaluation methodology.

---

## Podcast Script

**JORDAN:** Welcome to SlackCasts by PodSlacker — where AI does the watching so you can do the listening. If you want a richer experience with today's episode, visit PodSlacker dot com slash SlackCasts — you'll find a written summary, key frame moments from the video, and an interactive AI chat to explore the topic as deep as you like. Now let's get into it.

**MIKE:** Today we’re dissecting Booking.com’s journey from a handful of GenAI prototypes to a production‑grade, agentic ecosystem built on Google Gemini, Vertex AI, and the Gemini Enterprise Agent Platform. Let’s start with the scale that frames all of this.

**JORDAN:** Booking.com isn’t just a travel site – it’s a massive online travel platform that has facilitated over 6.8 billion guest arrivals across 175 k destinations, handling roughly half a million requests per second at sub‑50 ms latency. Those numbers drive the need for ultra‑low‑latency, high‑throughput AI serving.

**MIKE:** Right, and they’ve been running predictive ML in production for a decade, which gave them a mature data‑pipeline and monitoring stack before GenAI even arrived. That heritage is why they could pivot to a “multi‑provider” stack without rebuilding from scratch.

**JORDAN:** Their GenAI evolution is worth mapping. In 2023 they started with a simple wrapper around ChatGPT‑style models – a proof‑of‑concept “Phase 0.” By early 2024 they added internal models and built a multi‑provider abstraction layer, and then consolidated everything behind a single gateway that embeds governance, usage throttling, and audit logging.

**MIKE:** That gateway is the linchpin for a governed AI lifecycle: it lets any internal team request a model, apply safety guardrails, and push the call through a unified observability pipeline. It’s the bridge from experiment to production.

**JORDAN:** With that foundation, they rolled out four real‑world use cases. The first, “Know Before You Go,” is a customer‑facing itinerary planner. It fuses Gemini with Google Maps and search grounding, so a traveler can ask, “What’s the best route from the airport to my hotel?” and receive a multimodal plan that includes transport, activities, and time constraints.

**MIKE:** From a strategic standpoint, “Know Before You Go” demonstrates how external tool integration—maps, transport APIs, weather—extends a pure LLM into a reasoning engine. It also showcases the need for deterministic latency, which pushed them away from the default on‑demand Vertex AI endpoint.

**JORDAN:** Exactly. They moved to provisioned throughput for that workload, reserving tokens per minute to guarantee response time under heavy traffic. The second use case, “Big Bot,” is internal: a data‑registry chatbot that surfaces internal assets and can orchestrate workflows via natural language.

**MIKE:** “Big Bot” is a productivity multiplier for engineers. It shows that the same agentic stack can be repurposed for SaaS‑style internal tooling, reducing context‑switching and boosting data discoverability across a 7,000‑person org.

**JORDAN:** Third, the partner‑analytics agent extracts traveler pain points from reviews, turning unstructured feedback into actionable themes—think “breakfast variety” or “pool cleanliness.” This is a classic text‑to‑insight pipeline that leverages Gemini’s grounding and classification capabilities.

**MIKE:** That use case underscores the business value of LLM‑driven signal extraction: partners get a concise, data‑driven product backlog without manual tagging. It also raises governance concerns because you’re processing private guest feedback at scale.

**JORDAN:** Finally, the multimodal “Reels to Reality” prototype consumes YouTube URLs, parses video content, and generates concrete itineraries. It’s a perfect testbed for Gemini’s vision‑language model, and it forced Booking.com to evaluate priority processing tiers for reliable multimodal inference.

**MIKE:** Multimodal workloads are notoriously heavy on GPU memory and I/O, so they opted for Vertex AI’s priority processing tier, which guarantees dedicated compute and lower jitter—critical when you’re turning a 30‑second clip into a booking recommendation in near‑real time.

**JORDAN:** All those serving decisions tie back to a core lesson: “one size does not fit all” when picking Vertex AI serving options. On‑demand works for low‑traffic prototypes, provisioned throughput for steady‑state, latency‑sensitive agents, and priority processing for heavy multimodal or bursty traffic.

**MIKE:** Beyond serving, Booking.com emphasized platform adoption. They built self‑service documentation, hackathons, and a “knowledge‑share portal” so product teams can discover which tier, guardrails, and tooling to use without bottlenecking on the platform team.

**JORDAN:** That aligns with the “platform team = half the job” mantra—building the APIs is only half; the other half is surfacing best practices, curating sample code, and creating a community of practice. Their internal enablement reduced time‑to‑production from months to weeks.

**MIKE:** After the use cases, Google’s specialists—Manasa and Naz—laid out four production principles. First, evaluation: they split it into response evaluation (final answer quality) and trajectory evaluation (tool calls, parameters, and intermediate steps).

**JORDAN:** They highlighted human review as the gold standard but expensive, so they introduced LLM‑as‑judge for scalable response scoring. For trajectory, they use automated metrics like hallucination rate, groundedness, and coherence, plus custom checks on tool‑call correctness.

**MIKE:** The second principle is rapid code‑to‑cloud migration. By packaging agents as Docker containers with the Vertex AI Agent Engine SDK, they can push a new version to the gateway in under five minutes, preserving CI/CD pipelines and enabling canary deployments.

**JORDAN:** Third is identity and security at deployment. They bind each agent to a Google Service Account, enforce IAM roles for each downstream API (Maps, Cloud SQL, Weather MCP), and wrap the model with Model Armor to apply token‑level access controls and adversarial‑robustness checks.

**MIKE:** And the final pillar is observability and auditability. They instrument agents with Cloud Logging, Cloud Monitoring, and Vertex AI’s Trace API to capture request‑level latency, token usage, and tool‑call graphs. This lets ops teams spot drift or policy violations quickly.

**JORDAN:** In their demo, the “London Travel Concierge” agent combines a weather MCP, a ticket‑booking microservice, and an activities service, all orchestrated via the Agent Engine. The demo illustrates how Model Armor can reject out‑of‑policy queries before they hit proprietary data.

**MIKE:** From a senior practitioner’s view, the combination of trajectory metrics and Model Armor gives you a safety net against both hallucination and data leakage—a non‑negotiable requirement for any production travel assistant handling PII.

**JORDAN:** To summarize the key takeaways: serve agents with the right Vertex AI tier, embed governance in a unified gateway, invest heavily in self‑service enablement, evaluate both response and trajectory, and lock down identity & observability from day one.

**MIKE:** Those principles aren’t travel‑specific; any large enterprise looking to scale GenAI agents can borrow this blueprint. Booking.com’s shift from isolated experiments to a governed, multi‑provider production ecosystem is a template for responsible AI roll‑out.

**JORDAN:** That’s a wrap on today's SlackCast. Head over to PodSlacker dot com slash SlackCasts for the written summary, visual key moments, and an AI chat to dive even deeper into today's topic. Until next time — slack off smarter.

