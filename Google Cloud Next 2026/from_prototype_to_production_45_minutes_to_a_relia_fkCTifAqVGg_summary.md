# From prototype to production: 45 minutes to a reliable Gemini Enterprise Agent Platform agent

**Source:** https://www.youtube.com/watch?v=fkCTifAqVGg  
**Video ID:** `fkCTifAqVGg`

---

## Overview  
In this session, Booking.com engineers explain how they moved from early generative‑AI experiments to a production‑grade, agent‑centric AI platform built on Gemini and Vertex AI. They walk through several customer‑facing and internal use cases, share practical lessons about model serving, governance, and developer enablement, and then hand off to Google Cloud specialists who outline best‑practice principles for evaluating, deploying, securing, and monitoring agents in production.

## Topics Covered  

- **Booking.com AI maturity journey** – From a simple ChatGPT‑style wrapper in 2023 to a multi‑provider, governed AI ecosystem with built‑in safety, monitoring, and lifecycle management.  
- **Customer‑facing agent “Know Before You Go”** – Uses Gemini, Google Maps, and search grounding to generate personalized itineraries, transport links, and travel advice between booking and departure.  
- **Internal “Big Bot” data‑registry chatbot** – Allows employees to query internal data assets and create workflows via natural language, boosting developer productivity.  
- **Partner analytics bot** – Extracts pain‑points and themes from guest reviews, helping partners prioritize improvements (e.g., pool quality, breakfast variety).  
- **Multimodal “Reels to Reality”** – Takes short‑form travel videos (YouTube URLs) as input, converts visual inspiration into concrete itineraries on the Booking.com app.  
- **Serving‑tier experimentation** – Comparison of Vertex AI serving options (on‑demand, provisioned throughput, priority processing) and how the team matched each tier to a specific use case’s latency and scalability needs.  
- **Platform ownership & knowledge sharing** – Emphasizes the need for self‑service tooling, up‑to‑date docs, hackathons, and community support to move teams from prototype to production.  
- **Google Cloud agent‑deployment principles** (presented by Manasa & Naz) – Evaluation methods (response vs. trajectory), using “LLM as judge,” automated metrics, identity & security at deployment, and observability/auditability for production agents.  
- **Demo overview** – A travel‑concierge demo featuring a London itinerary agent that orchestrates weather services, ticketing, and activity agents, illustrating end‑to‑end agent orchestration on Google Cloud (Agent Engine, Model Armor, etc.).

## Key Takeaways  

- **Governed, multi‑provider AI is essential for scale** – Booking.com now runs a unified gateway with built‑in safety guards and usage monitoring, enabling rapid rollout of diverse LLM‑based agents.  
- **One serving tier does not fit all** – Choose Vertex AI serving mode (on‑demand, provisioned throughput, priority) based on each agent’s latency, throughput, and multimodal requirements.  
- **Agent evaluation must consider both output quality and internal “trajectory”** – Combine human review, LLM‑as‑judge scoring, and automated metrics (groundedness, coherence, tool‑call correctness).  
- **Developer enablement is half the platform job** – Continuous documentation, tutorials, hackathons, and clear onboarding accelerate the move from experimentation to production.  
- **Multimodality unlocks new travel experiences** – Directly feeding video URLs to Gemini enables creative use cases like turning social‑media reels into booking‑ready itineraries.  
- **Production agents need robust identity, security, and observability** – Use Google Cloud tools (Agent Engine, Model Armor, audit logs) to enforce least‑privilege access, protect data, and debug failures.  
- **Collaboration with Google is a strategic advantage** – Booking.com’s partnership provides access to cutting‑edge models (Gemini) and infrastructure that accelerate agentic product development.

## Notable Quotes  

- “It’s not just about choosing the right model. It’s about how we serve the LLMs and make them easy to use across our organization.”  
- “One size does not fit all when it comes to serving tiers; we match the serving strategy with the production need rather than assume the default will do the trick.”  
- “Building the platform is only half the job; the other half is helping users understand what’s available, when to use which tool, and how to get started.”  
- “If I had to summarize our journey in one sentence: Booking.com has been moving from isolated Gen AI experiments to a governed multi‑provider production‑ready AI ecosystem.”

---

## Podcast Script

**JORDAN:** Hey everyone, welcome to the podcast! I’m Jordan, your resident deep‑diver into the “how” and “why” of tech.

**MIKE:** And I’m Mike, ready to bring the big picture and real‑world impact into the mix. Today we’re unpacking a talk from Booking.com about turning AI prototypes into production‑ready agents.

**JORDAN:** The speaker, Alibek, started with some impressive stats—over 6.8 billion guest arrivals, 175 000 destinations, and half a million requests per second at sub‑50 ms latency. That sets a massive scale for any AI system.

**MIKE:** Right, and they’ve been doing AI for over a decade, but the real focus is on generative AI—specifically Gemini on Vertex AI. It’s a classic “ChatGPT moment” turning into a full‑blown ecosystem.

**JORDAN:** Their evolution went from a simple wrapper in 2023 to a single gateway with governance and usage monitoring by early 2024. That governance layer is key for reliable production.

**MIKE:** Governance sounds bureaucratic, but it’s what keeps a global travel platform from spitting out weird answers or leaking data—something users would notice instantly.

**JORDAN:** Maria, their engineer, highlighted four use cases. First up, “Know Before You Go,” an agent that stitches together travel itineraries using Google Maps and search grounding. It’s essentially a reasoning pipeline that pulls external knowledge.

**MIKE:** I love that because it solves a pain point for travelers: turning the abstract excitement of a trip into concrete steps. Imagine asking, “What’s the best way from the airport to my hotel?” and getting a live, personalized plan.

**JORDAN:** Next is “Big Bot,” an internal data registry chatbot. It lets employees query data assets and even generate workflows from natural language. That’s a huge productivity booster for a company of 7,000 people.

**MIKE:** And it shows the dual benefit of LLMs—enhancing both customer‑facing and internal workflows. More efficient dev teams mean faster feature rollouts for travelers.

**JORDAN:** The third case, “Partner Analytics,” extracts pain points from reviews with LLM‑driven signal extraction. It’s not just text generation; it’s knowledge mining at scale.

**MIKE:** That directly feeds into product improvements. If a bunch of guests complain about “breakfast variety,” the partner can act, turning AI insights into better service.

**JORDAN:** Finally, “Reels to Reality” leverages multimodal AI: feed a YouTube travel reel URL, and the model produces a concrete itinerary. That’s a sophisticated use of video understanding and grounding.

**MIKE:** It taps into how modern travelers discover places—through short videos. Turning that inspiration into a bookable plan could be a game‑changer for conversion rates.

**JORDAN:** The team ran into serving challenges on Vertex AI. They tried on‑demand, then provisioned throughput, and finally priority processing for multimodal workloads. It underscores that “one size fits all” doesn’t work at scale.

**MIKE:** Exactly, and that’s a lesson for any org: match the serving tier to the latency and throughput requirements of each use case, otherwise you’ll hit bottlenecks or waste resources.

**JORDAN:** They also stressed platform adoption—building tools is half the battle, the other half is making them discoverable, providing tutorials, hackathons, and clear documentation.

**MIKE:** Which is why many companies struggle with AI adoption. If the internal community can’t find or trust the tool, it never moves from experiment to production.

**JORDAN:** To sum up, Booking.com’s journey shows a shift from isolated GenAI experiments to a governed, multi‑provider AI ecosystem, with Google’s Gemini and Vertex AI as core enablers.

**MIKE:** And the real takeaway for our listeners is that reliable agents need robust governance, the right serving strategy, and a strong internal enablement program.

**JORDAN:** That’s a wrap on today’s deep dive. Thanks for listening, and keep questioning the “how” behind the tech.

**MIKE:** Absolutely—thanks for joining us, and stay tuned for more stories on turning AI ideas into production reality. Bye!

