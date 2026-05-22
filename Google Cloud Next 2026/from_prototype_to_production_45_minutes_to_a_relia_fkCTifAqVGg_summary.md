# From prototype to production: 45 minutes to a reliable Gemini Enterprise Agent Platform agent

**Source:** https://www.youtube.com/watch?v=fkCTifAqVGg  
**Video ID:** `fkCTifAqVGg`

---

## Overview  
In this session, Booking.com’s AI Platform team shares how they moved from early Gen‑AI experiments to a production‑grade, agent‑centric solution built on Google Gemini and Vertex AI. Alibek introduces the company’s scale and AI maturity, while Maria walks through four real‑world use cases (customer‑facing, internal, partner analytics, and multimodal). The talk then shifts to practical guidance from Google engineers on evaluating, deploying, securing, and observing agents in production.

## Topics Covered
- **Booking.com’s AI journey** – From a simple ChatGPT‑style wrapper in 2023 to a governed, multi‑provider AI ecosystem with built‑in safety and lifecycle management.  
- **Use‑case showcase**  
  1. **Know Before You Go** – Customer‑facing travel assistant that combines Gemini with Google Maps and search grounding to generate itineraries and airport‑to‑hotel directions.  
  2. **Big Bot** – Internal data‑registry chatbot that lets employees locate data assets and create workflows via natural language.  
  3. **Partner Analytics** – Host‑facing tool that extracts traveler pain points from reviews, turning unstructured feedback into actionable themes.  
  4. **Reels to Reality** – Multimodal agent that ingests short‑form travel videos (YouTube URLs) and turns the inspiration into concrete itineraries on the Booking.com app.  
- **Serving strategies on Vertex AI** – Comparison of on‑demand, provisioned throughput, and priority processing tiers; importance of matching the tier to latency and scale requirements of each use case.  
- **Platform ownership vs. self‑service** – The AI platform team provides the infrastructure, documentation, hackathons, and support to enable product teams to move from prototype to production independently.  
- **Google Cloud best practices** (presented by Manasa & Naz)  
  - Evaluating agents: response‑level (LLM‑as‑judge) vs. trajectory‑level metrics that inspect tool calls and workflow.  
  - Rapid code‑to‑cloud migration using Agent Engine and Model Armor.  
  - Defining agent identity at deployment time for governance and traceability.  
  - Security controls for production agents (IAM, VPC Service Controls, secrets management).  
  - Observability & auditability: logging, tracing, and debugging tools for non‑deterministic agent behavior.  

## Key Takeaways
- Successful production agents require **both the right model and the right serving strategy**; default on‑demand serving is often insufficient for latency‑sensitive or multimodal workloads.  
- **Governance and visibility** are as critical as model performance—centralized monitoring, safety guardrails, and clear documentation enable scalable self‑service across the organization.  
- Multi‑modal capabilities (e.g., processing YouTube URLs) unlock novel travel experiences and illustrate Gemini’s strength in grounding visual content to actionable recommendations.  
- **Evaluation must go beyond surface responses**; trajectory metrics that track tool usage and data flow provide deeper insight into agent reliability.  
- Google Cloud offers a suite of tools (Vertex AI, Agent Engine, Model Armor) that streamline the end‑to‑end lifecycle—from prototyping to secure, observable production deployments.  

## Notable Quotes
- “*It’s not just about choosing the right model. It’s about how we serve the LLMs and make them easy to use across our organization.*” – Maria  
- “*One size does not fit all when it comes to serving tiers.*” – Maria  
- “*If I had to summarize our journey in one sentence, it would be this: Booking.com has been moving from isolated GenAI experiments to a governed multi‑provider production‑ready AI ecosystem.*” – Maria  
- “*Agents are non‑deterministic, which brings unique challenges to evaluation—hence the need for trajectory‑level metrics.*” – Naz Bayraktar  

---  

*This summary captures the main points of the 45‑minute presentation on moving from prototype to production with Gemini Enterprise Agent Platform agents.*

---

## Podcast Script

**JORDAN:** Hey everyone, welcome back to the show! I’m Jordan, your go‑to for the nitty‑gritty of how these AI systems actually work.

**MIKE:** And I’m Mike, here to keep an eye on the big picture and what all of this means for travelers and developers alike. Today we’re diving into Booking.com’s journey from a prototype AI agent to a production‑grade, Google‑powered platform.

**JORDAN:** Right, Alibek kicked things off by showing how Booking.com isn’t just a hotel site—they’ve moved 6.8 billion guest arrivals across 175 k destinations, handling half a million requests per second with sub‑50 ms latency. That’s the kind of scale where any AI hiccup shows up fast.

**MIKE:** Exactly, and that massive traffic is why they needed a robust AI ecosystem, not just a single chatbot. They evolved from a simple wrapper in 2023 to a full‑blown multi‑provider gateway with governance and monitoring baked in.

**JORDAN:** Governance is key. They built a single gateway that logs every model call, enforces safety guardrails, and lets internal teams pick the best model for the job. It’s a classic “serve the model, not the model serves you” approach.

**MIKE:** Speaking of “best model,” Maria walked us through four real use cases—‘Know Before You Go,’ ‘Big Bot,’ partner analytics, and the multimodal ‘Reels to Reality.’ Each one leverages Gemini in a different way, from grounding travel itineraries with Google Maps to parsing YouTube videos into booking recommendations.

**JORDAN:** What stood out to me was the serving strategy shift. For the itinerary bot they moved from on‑demand Vertex AI to provisioned throughput because latency mattered. Then for the video‑to‑itinerary pipeline they tried priority processing to handle the multimodal load. It’s a reminder that “default” is rarely good enough at scale.

**MIKE:** And the internal “Big Bot” is a neat example of AI boosting developer productivity. A natural‑language data‑registry chatbot that can spin up workflows—imagine cutting down weeks of onboarding to minutes for a new data engineer.

**JORDAN:** They also emphasized knowledge sharing. The platform team isn’t just building the tech; they’re curating docs, running hackathons, and making sure every product team knows which serving tier to pick and how to add guardrails. That cultural layer often gets ignored but is vital for production success.

**MIKE:** From a user standpoint, the multimodal “Reels to Reality” is exciting. Travel inspiration is visual, and letting a traveler drop a short YouTube clip and get a ready‑to‑book itinerary flips the traditional search model on its head. That’s the kind of frictionless experience people actually talk about on social media.

**JORDAN:** The underlying lesson is that agent reliability is a stack: model selection, serving tier, governance, observability, and finally, user‑centric design. Booking.com’s partnership with Google gave them the tooling—Gemini, Vertex AI, and Model Armor—to align all those layers.

**MIKE:** So if we sum it up, the key takeaways are: match your serving strategy to the use case, build a self‑service platform with strong governance, and always keep the end‑user experience front and center. That’s how you turn a prototype into a production‑ready travel assistant.

**JORDAN:** Thanks for listening! I’m Jordan, and I hope you got a deeper understanding of the “how” behind reliable AI agents.

**MIKE:** And I’m Mike—keep asking the big questions about how these tech moves impact real travelers and developers. Until next time, stay curious!

