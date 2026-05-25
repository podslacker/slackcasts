# Agentic commerce: Transform the shopping experience with Google agents and open standards

**Source:** https://www.youtube.com/watch?v=GNlWClpVtcQ  
**Video ID:** `GNlWClpVtcQ`

---

## Overview  
This breakout session introduces **agentic commerce** – the use of AI agents to guide shoppers from product discovery through checkout. Jesse (AI Incubation Lead, Google Cloud) explains why large language models (LLMs) are reshaping retail, presents Google’s tooling (Gemini Enterprise, Shopping Agent, Universal Commerce Protocol (UCP) and Agent Payments Protocol (AP2)), and shares real‑world examples from Wayfair and Fiserv. The goal is to show how open, vendor‑agnostic standards can create a frictionless, secure buying experience across any surface.

## New Features & Announcements  

- **Gemini Enterprise for Customer Experience (GECX)** – A managed suite that lets brands run AI‑driven discovery, commerce, and support on their own properties.  
  Availability: Private preview, pilot customers.  

- **Shopping Agent (preview)** – A Google‑managed, multimodal shopping assistant that can understand complex queries, suggest products, manage carts, and complete purchases with user consent.  
  Availability: Private preview, piloted with select merchants.  

- **Universal Commerce Protocol (UCP)** – Open‑source standard that defines a common schema for AI agents to communicate with retailer, identity‑provider, and payment‑service back‑ends.  
  Availability: Public on ucp.dev and GitHub.  

- **Agent Payments Protocol (AP2)** – Open protocol that adds tamper‑proof mandates and tokenized checkout to secure AI‑driven transactions.  
  Availability: Early pilot stage (timeline not disclosed).

## Topics Covered  

- **Why AI agents matter** – LLMs can collapse traditional search, filters, reviews, and specs into a single conversational thread, compressing the funnel and driving higher purchase intent.  
- **Market data** – 10× increase in brand discovery via LLMs (2025), 30% of shoppers start discovery with AI, 40% of AI‑driven sessions land on product‑detail pages.  
- **Google’s tooling stack**  
  - *Gemini Enterprise* provides the underlying LLM power.  
  - *Shopping Agent* showcases a ready‑to‑deploy assistant.  
  - *UCP* creates a universal, extensible API schema (catalog, cart, checkout, order, identity linking, plus decorators like discounts/fulfillment).  
  - *AP2* secures the payment leg with tokenization and mandates.  
- **Architecture overview** – Four actors (platform/agent, merchant‑of‑record, credential provider, payment service) interact through layered protocols (service, common, capabilities, extensions, transport). Supports REST/JSON, MCP, A2A, and iframe embeds.  
- **Open‑source & interoperability** – UCP and AP2 are fully open, encouraging community contributions and avoiding vendor lock‑in while integrating with existing standards (MCP, A2A).  
- **Real‑world case studies**  
  - *Wayfair* onboarded 30 M products into agent‑driven services.  
  - *Fiserv* demonstrated tokenized checkout flow for payments via AP2.  

## Key Takeaways  

- AI agents can dramatically reduce shopping friction by handling discovery, recommendation, and checkout in a single conversational flow.  
- Retailers must expose clean, standardized product and checkout data so agents can safely transact on their behalf.  
- Open protocols (UCP, AP2) provide a vendor‑neutral foundation that works across any surface—search, Gemini apps, third‑party agents, or embedded iframes.  
- Security and trust are critical; tokenized, mandatable payment flows (AP2) protect both consumers and merchants from hallucinations or fraud.  
- Google’s managed services (Gemini Enterprise, Shopping Agent) give early adopters a fast path, while the open standards let developers build custom, high‑code solutions.  
- The ecosystem is built to be vertically extensible—future expansions could cover groceries, travel, etc.

## Notable Quotes  

- “LLMs can help us sift through large amounts of data as well as constraints and preferences, and they can help us organize information from many different places, and ultimately help by driving decision.”  
- “AI is actually helping develop a fully formed purchase intent… we can collapse search bars, filters, product specs, reviews… into a highly adaptive conversational thread.”  
- “We believe that by leveraging these transparent, vendor‑agnostic standards, you can actually build a seamless shopping ecosystem with complete flexibility and absolutely no vendor lock‑in whatsoever.”  
- “Agents break that fundamental thing… we’re building trust through a tamper‑proof mandate‑based payment protocol.”

---

## Podcast Script

**JORDAN:** Welcome to the AI Commerce Lab, where we dissect how large language models are redefining retail. I’m Jordan, your deep‑dive host, and with me is Mike, who always asks where the business impact lands. Today we’re unpacking Google Cloud’s breakout on agentic commerce—LLM‑powered agents that shepherd shoppers from discovery all the way to checkout.

**MIKE:** Thanks, Jordan. The headline here is huge: agents that can compress the entire funnel into a single conversational thread. That’s a shift from the classic search‑filter‑review‑cart pipeline to a unified, intent‑driven flow. Let’s start by grounding the market context the session presented.

**JORDAN:** Right. Jesse cited a 10× lift in brand discovery via LLMs projected for 2025, plus 30 % of shoppers already initiating product hunts with AI. Even more striking, 40 % of those AI‑driven sessions land directly on product‑detail pages, indicating that agents are not just browsers but purchase catalysts.

**MIKE:** Those numbers tell a story: the discovery surface is moving to the chat interface. For senior merchandisers, that means catalog exposure has to be AI‑ready, otherwise you’re invisible to the very first point of contact.

**JORDAN:** Exactly, and that’s where the first pillar—**Gemini Enterprise for Customer Experience (GECX)**—comes in. It’s a managed suite that lets brands run discovery, commerce, and support on their own domains, leveraging Gemini’s underlying LLM. It’s still in private preview, but the architecture is clear: your brand’s data stays on your property while Gemini provides the reasoning engine.

**MIKE:** The managed angle lowers the barrier to entry. Companies can spin up an agent without building the whole LLM stack. Yet the session also stressed a parallel path: open, vendor‑agnostic standards for those who want full control.

**JORDAN:** That’s the **Universal Commerce Protocol (UCP)**. It defines a JSON‑based schema that covers catalog, cart, checkout, order, and identity linking, plus extensible decorators like discounts and fulfillment. It abstracts the four key actors: the agent platform, the merchant‑of‑record, the credential provider, and the payment service provider.

**MIKE:** By keeping the protocol open on ucp.dev and GitHub, Google is encouraging community contributions. From a strategic standpoint, it avoids lock‑in and lets you plug in existing MCP or A2A integrations without rewiring your back‑ends.

**JORDAN:** The layering is worth noting. At the top you have the **service layer** (vertical‑specific flows—currently shopping, but extensible to groceries, travel, etc.). Below that, the **common layer** houses shared primitives like identity linking. The **capabilities layer** exposes core operations—catalog, cart, checkout, order. Finally, **extensions** act as decorators, injecting discounts or fulfillment steps without bloating the core API.

**MIKE:** That decorator pattern is clever. It means a retailer can add a seasonal promotion as a lightweight extension rather than redesigning the checkout capability. It also aligns with micro‑service principles, easing versioning and rollout.

**JORDAN:** Transport flexibility is another design choice. UCP contracts can be materialized over classic REST/JSON, Google’s MCP, A2A, or even an iframe embed for human‑in‑the‑loop approvals. That last option solves the “agent‑initiated purchase” compliance concern by forcing an explicit user click.

**MIKE:** Speaking of compliance, the **Agent Payments Protocol (AP2)** addresses the trust gap. Agents could hallucinate prices or intents, so AP2 introduces tamper‑proof mandates and tokenized checkout flows. It essentially gives the merchant a cryptographically signed order authorisation that can’t be altered downstream.

**MIKE:** Security aside, the user experience is smoother. No more re‑entering card details; the agent can invoke the token with user consent, and the mandate guarantees the amount and merchant match the displayed UI.

**JORDAN:** Let’s pivot to the **Shopping Agent** preview. Unlike building a custom agent on top of Gemini, this is a Google‑managed multimodal assistant that can ingest images, natural language, and even complex constraints—think “outfit an entire graduation party” in one go.

**MIKE:** The demo highlighted how the agent can move items into a cart, suggest alternatives for out‑of‑stock SKUs, and finalize checkout with a single consent flow. For a CMO, that translates to higher conversion rates because friction is removed at the decision point.

**JORDAN:** And the Shopping Agent leverages the same UCP/AP2 stack under the hood, meaning it’s a reference implementation of the open standards. That gives early adopters a low‑code path while still exposing the protocols for high‑code custom agents.

**MIKE:** The session also featured **Wayfair’s** onboarding of 30 million SKUs into the agent‑driven pipeline. That scale test proves the catalog component of UCP can handle massive product graphs, which is critical for enterprises with extensive assortments.

**JORDAN:** Wayfair used UCP’s catalog capabilities to expose structured product attributes, images, and constraints. The agents could then reason over those attributes in real time, essentially performing a joint retrieval‑generation step without bespoke indexing.

**MIKE:** For payments, the **Fiserv** pilot showed AP2’s token lifecycle: the credential provider issues a payment token, the agent signs a mandate, and the PSP executes a tokenized transaction. That mirrors the card‑on‑file tokenization model but adds an agent‑level attestation layer.

**JORDAN:** It’s also worth noting the architecture’s support for both **consumer‑initiated** and **agent‑initiated** flows. In the former, the user actively clicks “buy”; in the latter, the agent can auto‑submit the mandate after explicit consent, which is crucial for voice‑first or UI‑less experiences.

**MIKE:** From an operational perspective, that raises new telemetry requirements. Merchants will need to log mandate IDs, token usage, and correlation IDs across the UCP layers to reconcile audits and dispute management.

**JORDAN:** Absolutely, and because the protocols are versioned and extensible, you can introduce new audit fields without breaking existing integrations—something that’s been a pain point with legacy payment gateways.

**MIKE:** Let’s talk about the **open‑source** angle again. By publishing UCP and AP2, Google invites ecosystem players—PIM vendors, ERP systems, digital wallet providers—to implement adapters. That could lead to a marketplace of certified UCP connectors, accelerating adoption.

**JORDAN:** The community can also propose new capabilities. For example, a “rental” capability could be added as a decorator on top of the checkout flow, enabling agents to handle lease agreements for equipment or vehicles without reinventing the core protocol.

**MIKE:** That extensibility aligns with a long‑term vision: a universal commerce layer that works across any surface—search, Gemini apps, third‑party assistants like Alexa, or even in‑car infotainment systems.

**JORDAN:** And because the transport layer supports iframe embedding, legacy web merchants can embed an agent UI without touching their backend, simply by exposing an endpoint that satisfies the UCP contract.

**MIKE:** The trade‑off, of course, is that merchants must expose clean, normalized product data. If your catalog is a mess of legacy SKUs and inconsistent attribute naming, the agent can’t surface accurate recommendations, and you risk hallucinations.

**JORDAN:** That’s why the session emphasized **catalog hygiene** as a prerequisite. Tools like Google Cloud’s Dataplex can help orchestrate a unified product data lake, feeding a canonical schema into the UCP catalog endpoint.

**MIKE:** Summing up the strategic impact: agents can compress the funnel, boost conversion, and open new discovery channels—think voice‑first or AR/VR overlays—while open standards keep the ecosystem flexible and secure.

**JORDAN:** And the concrete takeaways for practitioners are: (1) audit and normalize your catalog; (2) implement the UCP endpoints for catalog, cart, checkout, and identity; (3) integrate AP2 for tokenized, mandate‑based payments; (4) evaluate the Shopping Agent preview for a quick‑start proof of concept; and (5) contribute back to the open‑source repos to shape future extensions.

**MIKE:** If you’re a retailer watching this, the immediate next step is a pilot: expose a read‑only UCP catalog and run a limited‑scope agent—maybe a “gift‑finder” bot—using Gemini Enterprise. Measure conversion uplift, then layer in AP2 for end‑to‑end checkout.

**JORDAN:** For developers, the GitHub repos contain OpenAPI specs and sample clients in Python, Java, and Go. The transport abstraction means you can start with a simple REST mock and later migrate to MCP for higher throughput.

**MIKE:** And for payments architects, the AP2 mandate format is a signed JSON Web Token (JWT) that includes merchant ID, amount, currency, and a nonce. It’s validated by the PSP before token redemption, which gives you the audit trail you need for charge‑back protection.

**JORDAN:** Before we close, a quick nod to the broader ecosystem. By aligning with existing standards like MCP and A2A, UCP doesn’t replace legacy commerce APIs—it decorates them, providing a common conversational contract while preserving your investment in existing infrastructure.

**MIKE:** That’s the sweet spot: innovation without disruption. As agents become the default discovery surface, retailers that adopt open standards early will capture the next wave of AI‑driven commerce.

**JORDAN:** Thanks for joining us on this deep dive into agentic commerce. We’ll be back with more analyses of emerging retail tech. Until next time, stay curious and keep building.

**MIKE:** Catch you on the next episode.

