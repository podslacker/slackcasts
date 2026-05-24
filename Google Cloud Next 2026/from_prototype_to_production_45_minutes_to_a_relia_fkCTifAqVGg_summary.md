# From prototype to production: 45 minutes to a reliable Gemini Enterprise Agent Platform agent

**Source:** https://www.youtube.com/watch?v=fkCTifAqVGg  
**Video ID:** `fkCTifAqVGg`

---

## Overview
In this session, Booking.com’s AI Platform team walks through their journey of turning generative‑AI prototypes into production‑ready, agentic solutions on Google Cloud. Alibek introduces the company’s scale, AI heritage, and the evolution of their multi‑provider AI ecosystem, while Maria showcases four real‑world use cases built with Gemini and Vertex AI. The talk then shifts to practical guidance from Google engineers on evaluating, deploying, securing, and monitoring agents in production.

## Topics Covered
- **Booking.com’s AI background** – Over a decade of predictive ML, handling ~½ million requests/sec with 50 ms latency; recent focus on GenAI.
- **Evolution of the AI stack** – From a simple “wrapper” (2023) → multi‑provider platform with a unified gateway and governance (early 2024) → full‑lifecycle, production‑grade ecosystem.
- **Customer‑facing use case: “Know Before You Go”** – An itinerary‑planning agent that blends Gemini reasoning with Google Maps and search grounding to give travelers personalized travel plans.
- **Internal use case: “Big Bot”** – A data‑registry chatbot that lets Booking.com employees query internal assets and generate workflows via natural language.
- **Partner‑facing use case: Partner Analytics** – LLM‑driven extraction of traveler pain points from reviews, turning free‑form comments into actionable insights.
- **Multimodal use case: “Reels to Reality”** – Converts short‑form travel videos (YouTube URLs) into concrete itineraries, demonstrating Gemini’s multimodal capabilities.
- **Serving‑tier lessons** – Different workloads need different Vertex AI serving options (on‑demand, provisioned throughput, priority processing); default settings rarely suffice.
- **Platform adoption strategy** – Emphasize knowledge sharing, self‑service enablement, hackathons, and up‑to‑date documentation to move teams from experimentation to production.
- **Google Cloud agents best practices** – Evaluation (response vs. trajectory), using LLMs as judges, automated metrics, identity & security at deployment, observability, and debugging techniques, illustrated with a “London Travel Concierge” demo.

## Key Takeaways
- Building reliable agents is as much about **governance, serving strategy, and developer experience** as it is about picking the right model.
- A **single gateway with built‑in governance** enables multi‑model access while maintaining compliance and usage monitoring.
- **Serving tier selection must match workload characteristics**; provisioning throughput or priority processing may be required for latency‑sensitive or multimodal tasks.
- **Self‑service enablement and continuous education** are crucial for scaling AI adoption across large organizations.
- Agent evaluation should combine **response‑level checks** (human or LLM judges) with **trajectory‑level metrics** that examine tool calls and workflow steps.
- Security and identity need to be baked into the deployment pipeline (e.g., Model Armor, scoped service accounts) to protect production agents.
- Rich observability (logs, traces, audit trails) is essential for debugging and maintaining trust in non‑deterministic agents.

## Notable Quotes
- “*One size does not fit all when it comes to serving tiers.*”
- “*Building the platform is only half the job; the other half is helping users understand what’s available and how to get started.*”
- “*If I had to summarize our journey in one sentence: Booking.com has been moving from isolated GenAI experiments to a governed multi‑provider production‑ready AI ecosystem.*”

---

## Podcast Script

**JORDAN:** Welcome back to AI Ops Deep Dive, where we unpack how industry leaders turn cutting‑edge generative AI prototypes into production‑grade agents. I’m Jordan, your resident implementation nerd.

**MIKE:** And I’m Mike, bringing the strategic lens—why these decisions matter for scaling AI across a global business. Today we’re dissecting Booking.com’s journey with Google Cloud, Gemini, and Vertex AI.

**JORDAN:** Let’s start with the scale. Booking.com processes roughly half a million requests per second at a 99.9th percentile latency of 50 ms, all driven by a decade‑long predictive ML stack. Their GenAI push had to respect that baseline.

**MIKE:** Right, and that baseline shapes every architectural choice. You can’t drop a latency‑heavy LLM into a latency‑sensitive checkout flow without a plan.

**JORDAN:** The team’s AI stack evolved in three phases. Phase 0 in 2023 was a simple wrapper around a single LLM—a proof‑of‑concept “foot in the door.”

**MIKE:** By early 2024 they migrated to a multi‑provider platform, integrating in‑house models and adding a unified gateway with built‑in governance and usage monitoring.

**JORDAN:** Today that gateway is the single point of entry for any model—Gemini, Claude, or internal embeddings—while enforcing policy, quota, and audit logs.

**MIKE:** Governance at the gateway is key for a regulated business like travel, where data residency and compliance can’t be an afterthought.

**JORDAN:** Alibek highlighted four production use cases built on Gemini. First up, “Know Before You Go,” a customer‑facing itinerary planner that fuses Gemini reasoning with Google Maps and Search grounding.

**MIKE:** The value proposition is clear: reduce the friction between booking and travel by auto‑generating personalized itineraries—airport transfers, activity sequencing—based on user constraints.

**JORDAN:** The second use case, “Big Bot,” is internal. It’s a data‑registry chatbot that lets engineers query internal assets and spin up workflows via natural language.

**MIKE:** That’s a classic productivity amplifier—turning data discoverability into a conversational interface, which can shave weeks off onboarding new team members.

**JORDAN:** Third, “Partner Analytics,” a partner‑facing LLM that extracts pain points from free‑form reviews, turning unstructured comments into actionable tags like “pool cleanliness” or “breakfast variety.”

**MIKE:** This directly feeds partner dashboards, enabling property owners to prioritize fixes that drive higher ratings and ultimately more bookings.

**JORDAN:** Finally, “Reels to Reality,” the multimodal showcase. It ingests YouTube short‑form videos, extracts visual cues, and produces concrete itineraries—leveraging Gemini’s ability to handle video URLs as context.

**MIKE:** It’s a perfect example of meeting the market where inspiration lives: short videos on TikTok or YouTube. Turning that raw visual spark into a booking funnel is a massive competitive advantage.

**JORDAN:** All four illustrate that model selection is only half the equation. Maria stressed the importance of serving tiers on Vertex AI. Their first project used default on‑demand serving, which proved insufficient for latency‑critical flows.

**MIKE:** So they switched to provisioned throughput—essentially reserving a token‑per‑minute quota—to guarantee capacity. That worked for “Know Before You Go,” but not universally.

**JORDAN:** For multimodal workloads like “Reels to Reality,” they adopted priority processing, ensuring that GPU‑accelerated video decoding and Gemini inference stay within tight SLAs.

**MIKE:** The takeaway is clear: one size does not fit all. You need to profile each agent’s token rate, latency budget, and modality to pick the right Vertex AI serving option.

**JORDAN:** Beyond serving, the platform team emphasized self‑service enablement. They don’t build the agents themselves; they provide documentation, internal hackathons, and up‑to‑date sample pipelines.

**MIKE:** That cultural shift—from a “you‑build‑it‑we‑run‑it” model to a developer‑centric enablement model—is what scales AI adoption in a 7,000‑person org.

**JORDAN:** Switching gears, the Google engineers—Manasa and Naz—walked through the four pillars of productionizing agents: evaluation, deployment, security, and observability.

**MIKE:** Starting with evaluation, they distinguished response‑level checks from trajectory‑level metrics. Response evaluation mirrors classic LLM testing—BLEU, ROUGE, human ratings—but ignores tool calls.

**JORDAN:** Trajectory evaluation digs into the agent’s workflow: which tools were invoked, with what parameters, and whether the sequence aligns with a golden path. It’s essential for debugging non‑deterministic behavior.

**MIKE:** They also advocated using an LLM‑as‑judge for scalable response evaluation—feeding the candidate response and a rubric into a secondary model to get a numeric score.

**JORDAN:** While efficient, that approach can miss domain‑specific failures—like a mis‑structured API payload—so they complement it with custom automated metrics that inspect tool invocation success rates and grounding scores.

**MIKE:** For deployment, the demo featured the “London Travel Concierge” agent orchestrating ticket, activities, and weather micro‑services via Agent Engine. They highlighted Model Armor for runtime protection.

**JORDAN:** Model Armor tightly scopes the model’s IAM role, restricting it to only the necessary Vertex AI endpoint and preventing unauthorized token extraction.

**MIKE:** Identity at deployment time is baked in through scoped service accounts and workload identity federation, ensuring that each agent runs with least‑privilege permissions.

**JORDAN:** Security doesn’t stop there—they enforce data‑in‑transit encryption, secret management via Secret Manager, and regular vulnerability scans of custom containers.

**MIKE:** Observability is tackled with structured logs, OpenTelemetry traces across tool calls, and audit logs that capture every model request, verdict, and policy check.

**JORDAN:** That full traceability is crucial for compliance audits, especially when agents generate user‑facing content that could be subject to misinformation regulations.

**MIKE:** Summing up, Booking.com’s production‑ready ecosystem hinges on three pillars: a governed multi‑model gateway, workload‑matched serving tiers, and a robust developer enablement program.

**JORDAN:** And from the Google side: systematic response and trajectory evaluation, hardened deployment pipelines with Model Armor, and end‑to‑end observability.

**MIKE:** For listeners building their own agentic products, the concrete takeaways are: profile your token throughput, pick the Vertex AI tier that matches your latency budget, instrument both outcomes and workflow steps, and embed governance at the gateway.

**JORDAN:** And never underestimate the cultural work—keeping documentation fresh, running internal hackathons, and celebrating successful migrations from experiment to production.

**MIKE:** That’s it for today’s deep dive. Thanks to Alibek, Maria, Manasa, and Naz for sharing the details, and thank you for tuning in.

**JORDAN:** Stay curious, stay secure, and keep building reliable agents. Catch you next time on AI Ops Deep Dive.

