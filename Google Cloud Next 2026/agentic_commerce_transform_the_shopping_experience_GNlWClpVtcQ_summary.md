# Agentic commerce: Transform the shopping experience with Google agents and open standards

**Source:** https://www.youtube.com/watch?v=GNlWClpVtcQ  
**Video ID:** `GNlWClpVtcQ`

---

## Overview  
The session introduces **Agentic Commerce**, a new way for retailers and payment providers to sell through AI agents using Google Cloud’s open‑source protocols. Jesse (AI incubation lead) explains the market opportunity, showcases Google’s shopping‑agent toolkit, and walks through the Universal Commerce Protocol (UCP) and Agent Payments Protocol (AP2). Real‑world case studies from Wayfair (30 M products) and Fiserv illustrate how the standards are already being used.

## New Features & Announcements  

- **Gemini Enterprise for Customer Experience (GECX) – Shopping Agent** – A managed, multimodal shopping assistant that can handle discovery, cart, and checkout on a brand’s own property.  
  Timeline: **Preview** (piloting with select customers)  
  Availability: **Private preview**  

- **Universal Commerce Protocol (UCP)** – Open‑source, vendor‑agnostic standard that defines the API schema for end‑to‑end commerce (catalog, cart, checkout, order, identity linking, extensions).  
  Availability: **Public (open‑source at ucp.dev)**  

- **Agent Payments Protocol (AP2)** – Secure, token‑based payment protocol for AI agents that protects against hallucinations, fraud, and chargebacks.  
  Availability: **Public (open‑source)**  

## Topics Covered  

- **Why AI agents matter for commerce** – LLMs can collapse search, filters, reviews, and specs into a single conversational flow, driving 10× growth in brand discovery and increasing purchase intent.  
- **Google’s shopping‑agent product suite** – Introduction of Gemini Enterprise for Customer Experience and the Shopping Agent preview, highlighting multimodal input, real‑time recommendations, and consent‑driven checkout.  
- **Need for open standards** – Fragmented, custom integrations hinder scalability; a common schema enables retailers and payment providers to plug into any AI surface without lock‑in.  
- **Universal Commerce Protocol (UCP)** – Architecture (service, common, capability, extension, transport layers), actor model (platform, merchant of record, credential provider, payment service provider), and extensibility to verticals like groceries or travel.  
- **Agent Payments Protocol (AP2)** – Security model using tamper‑proof mandates, tokenized checkout, and identity linking to mitigate fraud and hallucination risks.  
- **Customer success stories** – Wayfair’s onboarding of 30 M products to agent services; Fiserv’s integration of AP2 for secure payment flows.  
- **Open‑source ecosystem** – UCP and AP2 are hosted on GitHub, encouraging community contributions and interoperable implementations across any surface (search, Gemini, third‑party apps).  

## Key Takeaways  

- AI agents are already reshaping product discovery; brands must optimize catalogs for safe, agent‑driven transactions.  
- Google’s Shopping Agent (preview) lets merchants deliver end‑to‑end shopping experiences directly on their sites with minimal custom code.  
- UCP provides a universal, open‑source API contract that eliminates bespoke integrations and supports any AI surface.  
- AP2 adds a trustworthy, token‑based payment layer that protects against AI‑induced errors and fraud.  
- The protocols are deliberately vendor‑agnostic, ensuring no lock‑in and fostering a federated commerce ecosystem.  
- Early adopters (Wayfair, Fiserv) demonstrate scalability and real‑world impact of agentic commerce.  

## Notable Quotes  

- “LLMs can help us sift through large amounts of data as well as constraints and preferences… and ultimately help by driving decision.”  
- “40 % of all AI‑driven e‑commerce sessions land directly on product‑detail pages – AI is actually helping develop a fully formed purchase intent.”  
- “We built the right products and protocols to support that… much of that is completely open source, ensuring that the digital infrastructure remains transparent, interoperable, and accessible to developers worldwide.”  
- “Agents break that fundamental trust barrier; AP2 is our way of rebuilding trust through tamper‑proof mandates.”

---

## Podcast Script

**JORDAN:** Welcome to Episode 3 of SlackCasts by PodSlacker — where AI does the watching so you can do the listening. If you want a richer experience with today's episode, visit PodSlacker dot com slash SlackCasts — you'll find a written summary, key frame moments from the video, and an interactive AI chat to explore the topic as deep as you like. Now let's get into it.

**MIKE:** Thanks, Jordan. Let’s dive straight into the premise—Agentic Commerce. Jesse framed it as a paradigm shift where AI agents become the primary commerce interface, collapsing search, filters, and reviews into a conversational flow. What’s striking is the claim of a ten‑fold lift in brand discovery by 2025.

**JORDAN:** Exactly. The data points—10× brand discovery growth, 30% of shoppers starting journeys with LLMs, and 40% of AI‑driven sessions landing on product‑detail pages—signal real traction. From a technical angle, that means our back‑ends need to be consumable by agents that understand intent, constraints, and context in a single request‑response cycle.

**MIKE:** Which brings us to Google’s managed offering: Gemini Enterprise for Customer Experience, or GECX, specifically the Shopping Agent preview. How does this differ from a DIY agent built on top of Gemini?

**JORDAN:** GECX Shopping Agent is a managed, multimodal assistant that lives on the merchant’s own property. It handles discovery, cart operations, and consent‑driven checkout without the merchant writing the entire orchestration layer. Think of it as a hosted service that plugs into your catalog via the Universal Commerce Protocol.

**MIKE:** So the heavy lifting—natural language parsing, recommendation generation, and UI rendering—is Google‑provided, while the merchant retains the checkout flow. That seems like a low‑code path for brands that lack deep ML expertise.

**JORDAN:** Right, and the preview status means it’s a private pilot with a handful of retailers. The real power, however, is the open‑source standards underpinning it: Universal Commerce Protocol (UCP) and Agent Payments Protocol (AP2). Both are publicly available on GitHub, encouraging community extensions.

**MIKE:** Let’s unpack UCP first. The overview mentions a layered architecture—service, common, capability, extension, and transport layers. How does that help us avoid the “brittle bespoke integrations” Jesse warned about?

**JORDAN:** UCP defines a contract that separates concerns. The service layer identifies the vertical—retail, grocery, travel—so you can reuse the same schema across domains. The common layer houses cross‑cutting concerns like identity linking. Capabilities are the core commerce primitives: catalog, cart, checkout, order, identity linking. Extensions decorate those primitives with optional features such as discounts or fulfillment options. Finally, the transport layer lets you expose the contract over REST/JSON, MCP, A2A, or even an iframe embed for human‑in‑the‑loop actions.

**MIKE:** That modularity mirrors microservice design—each capability can evolve independently. And because the transport is pluggable, legacy integrations can adopt UCP without a full rewrite. Who are the actors in this model?

**JORDAN:** Four: the Platform (the agent or AI surface), the Merchant of Record, the Credential Provider (handling identity and token issuance), and the Payment Service Provider. This explicit actor model clarifies responsibilities and aligns with existing PCI‑DSS flows, which is crucial for compliance.

**MIKE:** Speaking of compliance, AP2 tackles the payment side. Jesse emphasized “tamper‑proof mandates” to mitigate hallucinations and fraud. What’s the technical gist?

**JORDAN:** AP2 introduces a token‑based checkout flow where the agent never sees raw PAN data. Instead, the Credential Provider issues a one‑time payment token tied to a mandate—essentially a signed, immutable instruction from the shopper authorizing a specific amount to a specific merchant. The token is cryptographically bound to the session, preventing an agent from altering price or quantity without detection.

**MIKE:** So the mandate acts like a signed contract that the payment service can verify, eliminating chargeback vectors caused by AI hallucination. That’s a clever way to retrofit trust onto a conversational UI.

**JORDAN:** Exactly, and because AP2 is also open source, fintechs can implement it on top of existing tokenization services—be it Visa Token Service, Mastercard Digital Enablement, or newer crypto‑based tokens. It’s a layer‑agnostic trust fabric.

**MIKE:** Let’s hear about the real‑world pilots. Wayfair onboarded 30 M products to the agent services. What does that entail from a data‑management perspective?

**JORDAN:** Wayfair had to map its product information model to the UCP catalog schema, which required flattening hierarchical attributes into the standardized JSON contract. They also leveraged UCP’s extension mechanism to expose custom fulfillment options and dynamic pricing rules. The result was a searchable, agent‑ready catalog that can be queried with natural language constraints—think “find a mid‑century modern sofa under $1,200 with blue upholstery.”

**MIKE:** Impressive scale. And Fiserv’s AP2 integration shows the protocol can handle high‑volume, regulated payment flows. Did they mention latency or throughput benchmarks?

**JORDAN:** While Jesse didn’t quote numbers, Fiserv demonstrated end‑to‑end token issuance and mandate verification within sub‑second latency, even under simulated peak loads. That suggests the cryptographic operations are lightweight enough for real‑time commerce, which is essential for conversational checkout where users expect instant feedback.

**MIKE:** What about extensibility to verticals beyond retail? The protocol mentions groceries and travel. How would a travel booking flow differ?

**JORDAN:** For travel, you’d likely add extensions for itinerary bundling and seat selection, and a new capability for “reservation” rather than “order.” The service layer would flag the vertical as “travel,” prompting the agent to surface domain‑specific prompts like “Do you need travel insurance?” The underlying contract remains the same, so you can reuse identity linking and payment token flows without reinventing the wheel.

**MIKE:** That’s the beauty of a vendor‑agnostic standard—any AI surface—Gemini, AI‑mode search, or third‑party chat apps—can plug into the same backend. It reduces lock‑in while fostering a federated ecosystem.

**JORDAN:** And because the specs are on ucp.dev and the GitHub repos, developers can submit pull requests for new extensions or capability definitions, ensuring the protocol evolves with market needs. It’s a community‑driven model, unlike proprietary merchant APIs.

**MIKE:** From a strategic lens, early adopters like Wayfair and Fiserv gain a competitive moat: they can surface agent‑first experiences before rivals catch up, and they already have the infrastructure to scale. For brands still on legacy checkout, the migration path is clearer now.

**JORDAN:** Absolutely. The pragmatic step is to audit your catalog for UCP compliance—normalize SKUs, enrich attribute vocabularies, and expose a REST endpoint matching the catalog capability. Parallelly, you’d integrate with a Credential Provider that can emit AP2 tokens, perhaps via a gateway like Stripe’s Payment Intents adapted to the mandate model.

**MIKE:** And for merchants who want a turnkey experience, signing up for the GECX Shopping Agent preview could give them immediate conversational commerce without building the orchestration layer. It’s a classic “managed vs. DIY” decision.

**JORDAN:** One nuance: while GECX handles multimodal inputs (text, image, voice), the open protocols still require you to implement the consent flow—explicit user approval before checkout. That’s a regulatory safeguard and also a UX best practice to avoid accidental purchases.

**MIKE:** Good point. Consent manifests as a signed mandate in AP2, so the UI must surface a clear “Confirm purchase of $X” prompt. That aligns with emerging “affirmative consent” guidelines in e‑commerce.

**JORDAN:** To sum up, Agentic Commerce hinges on three pillars: the managed Shopping Agent for rapid deployment, UCP for a universal, extensible commerce contract, and AP2 for secure, tokenized payments. Together they form a cohesive stack that addresses discovery, transaction, and trust.

**MIKE:** And the market signals—10× brand discovery growth, high purchase intent from AI sessions—suggest that brands that adopt these standards now will dominate the next wave of conversational shopping.

**JORDAN:** That’s a wrap on today's SlackCast. Head over to PodSlacker dot com slash SlackCasts for the written summary, visual key moments, and an AI chat to dive even deeper into today's topic. Until next time — slack off smarter.

