# Agentic commerce: Transform the shopping experience with Google agents and open standards

**Source:** https://www.youtube.com/watch?v=GNlWClpVtcQ  
**Video ID:** `GNlWClpVtcQ`

---

## Overview  
The session introduces **Agentic Commerce**, Google Cloud’s vision for AI‑driven shopping experiences that combine large language models, open commerce standards, and secure payment protocols. After highlighting the exploding consumer demand for AI‑powered product discovery, the talk walks through Google’s tooling (Gemini Enterprise, Shopping Agent), the open **Universal Commerce Protocol (UCP)**, and the **Agent Payments Protocol (AP2)**. Real‑world examples from Wayfair and Fiserv illustrate how retailers and payment providers can adopt these building blocks to create frictionless, vendor‑agnostic checkout flows.

## New Features & Announcements  
- **Gemini Enterprise for Customer Experience (GECX)** – A managed suite that lets brands embed Gemini‑powered AI (product discovery, support, commerce) on their own properties.  
  Availability: Private preview (piloted with select customers).  

- **Shopping Agent (preview)** – A Gemini‑driven conversational shopping assistant that can handle multimodal queries, recommend complete solutions, and execute consent‑based purchases end‑to‑end.  
  Availability: Private preview (piloted).  

- **Universal Commerce Protocol (UCP)** – Open‑source, vendor‑agnostic standard that defines a common schema and API set for AI agents to interact with retailers, identity providers, and payment processors across the full purchase journey.  
  Availability: Public on ucp.dev and GitHub.  

- **Agent Payments Protocol (AP2)** – Secure, tamper‑proof protocol that adds tokenized checkout, fraud mitigation, and consent proof for agent‑mediated transactions.  
  Availability: Early pilot phase (timeline not disclosed).

## Topics Covered  
- **Why AI agents matter now** – 10× rise in brand discovery via LLMs (2025), 30 % of shoppers start product discovery with AI, and AI condenses search, filters, reviews, etc., into a single conversational step.  
- **Real‑world story** – Presenter uses Gemini to pick a cargo‑box, demonstrating how LLMs synthesize constraints and deliver instant, purchase‑ready recommendations.  
- **Opportunity for retailers & payment providers** – Brands must expose clean, tokenizable catalogs; payment firms must support secure, consent‑driven checkout to win in the agentic channel.  
- **Gemini Enterprise & Shopping Agent** – Managed solutions that let companies deploy sophisticated, multimodal shopping assistants on their own sites, handling everything from discovery to cart creation and checkout.  
- **Limitations of proprietary integrations** – Prior to UCP, each retailer/payment partner built bespoke APIs, leading to fragmentation and high maintenance overhead.  
- **UCP architecture** – Defines four actors (platform/agent, merchant of record, credential provider, payment service provider) and three layers (service, common, capabilities) plus extensions (discounts, fulfillment) and transport options (REST/JSON, MCP, A2A, iframe).  
- **Open‑source nature of UCP** – Hosted on ucp.dev and GitHub to encourage community contributions and avoid vendor lock‑in.  
- **AP2 for secure payments** – Addresses hallucination, price‑mismatch, and fraud risks by using tamper‑proof mandates and tokenized checkout, building on the trust infrastructure pioneered by the broader payments industry.  
- **Customer case studies** – Wayfair’s onboarding of 30 M products to multiple agent services; Fiserv’s integration of AP2 to enable tokenized payments for AI agents.  

## Key Takeaways  
- AI agents are rapidly becoming a primary discovery channel; merchants must adapt or lose traffic.  
- Google’s Gemini Enterprise and Shopping Agent provide managed ways to deliver AI‑driven commerce on brand‑owned surfaces.  
- The **Universal Commerce Protocol (UCP)** offers a standardized, open‑source contract that eliminates brittle, custom integrations across retailers, identity providers, and payment processors.  
- **AP2** extends this trust model to payments, ensuring consent, tokenization, and fraud protection for agent‑initiated purchases.  
- Open standards keep the ecosystem interoperable and prevent lock‑in, allowing merchants to choose any front‑end (search, Gemini, third‑party agents).  
- Early adopters like Wayfair and Fiserv demonstrate that large‑scale catalog integration and secure tokenized checkout are already feasible.  

## Notable Quotes  
- “LLMs can help us sift through large amounts of data as well as constraints and preferences, and they can help us organize information from many different places, and ultimately help by driving decision.”  
- “40 % of all AI‑driven e‑commerce sessions land directly on product‑detail pages – AI is actually helping develop a fully formed purchase intent.”  
- “We built UCP with industry leaders so it isn’t our idea in isolation – it’s a common language for AI agents to solve fragmented online shopping.”  
- “AP2 builds trust through tamper‑proof mandates, protecting both consumers and merchants from hallucinated prices or fraudulent intent.”

---

## Podcast Script

**JORDAN:** Welcome to the AI Commerce Pulse, where we unpack the latest in agent‑driven shopping. I’m Jordan, your deep‑dive analyst, and with me is Mike, the strategic‑vision guy. Today we’re dissecting Google Cloud’s “Agentic Commerce” announcement—a stack that bundles Gemini Enterprise, the Shopping Agent, the Universal Commerce Protocol, and the new Agent Payments Protocol.

**MIKE:** Thanks, Jordan. The headline here is that AI agents are moving from novelty to a primary discovery channel. With a ten‑fold jump in LLM‑based brand discovery and 30 % of shoppers starting their journey with AI, retailers can’t afford to ignore the shift. Let’s start by grounding the conversation in that consumer demand.

**JORDAN:** Absolutely. The presenter’s cargo‑box anecdote illustrates the core value proposition: a multimodal LLM can ingest constraints—fit, safety, budget, aerodynamics—and synthesize a purchase‑ready recommendation in seconds. Technically, Gemini parses structured attributes, runs a constraint‑satisfaction routine, and surfaces a single SKU with a price, eliminating the traditional filter‑and‑sort loop.

**MIKE:** That compression of the funnel is what drives the 40 % statistic they cited—AI‑driven sessions landing directly on product‑detail pages. It signals a mature intent signal, which is gold for conversion optimization. From a business perspective, that intent is already monetizable, but only if the backend can keep up.

**JORDAN:** Which brings us to the first building block: Gemini Enterprise for Customer Experience, or GECX. It’s a managed suite that lets brands embed Gemini‑powered agents on their own domains while retaining brand identity and data sovereignty. Under the hood, GECX exposes a set of fine‑tuned LLM endpoints, custom tokenizers for product taxonomies, and a consent‑aware action API that can trigger cart mutations.

**MIKE:** And the fact it’s in private preview means early adopters can experiment with end‑to‑end flows without building the inference stack themselves. For a retailer, that reduces time‑to‑value from months to weeks, especially when you factor in the pre‑built connectors to Google Marketing Platform for attribution.

**JORDAN:** The second managed offering is the Shopping Agent, also in preview. It extends GECX by adding a conversational orchestrator that can handle multimodal inputs—text, images, even voice—and execute end‑to‑end purchases with explicit consent. Technically, it pipelines Gemini’s generation output into a state machine that validates product availability, price, and compliance before invoking the checkout API.

**MIKE:** From a strategy angle, the Shopping Agent is a white‑label solution for brands that want a “Shopify‑like” experience but powered by AI. It can substitute the traditional search bar, category pages, and even the “add‑to‑cart” button with a natural language flow, which is a huge shift in UX design.

**JORDAN:** The real game‑changer, however, is the Universal Commerce Protocol—UCP. It’s an open‑source, vendor‑agnostic schema that defines a common contract between four actors: the platform/agent, the merchant of record, the credential provider, and the payment service provider. The protocol is split into three semantic layers—Service, Common, and Capabilities—plus an Extensions layer for things like discounts and fulfillment.

**MIKE:** Right, and because it’s open on ucp.dev and GitHub, any retailer or PSP can adopt it without a lock‑in. The design deliberately abstracts transport: you can use plain REST/JSON, Google’s MCP, A2A, or even embed the flow in an iframe for human‑in‑the‑loop approvals. That flexibility is crucial for legacy ERP integrations.

**JORDAN:** Let’s unpack the Service layer first. It defines vertical‑specific domains—currently Shopping, but the spec is built to extend to groceries, travel, or even B2B procurement. Each service bundles a set of Capabilities: Catalog, Cart, Checkout, Order, and Identity Linking. Those Capabilities are expressed as JSON‑RPC contracts, versioned to support backward compatibility.

**MIKE:** The Common layer, on the other hand, provides cross‑service primitives like authentication tokens, session identifiers, and audit trails. By reusing the same identity‑linking model across services, merchants can maintain a single customer profile even when the purchase originates from a Google Gemini surface versus a third‑party voice assistant.

**JORDAN:** Extensions act as decorators. For example, the Discount extension can be attached to a Cart Capability without altering the core Checkout contract. This pattern avoids protocol bloat while allowing rapid feature rollout—think time‑limited promos or bundle pricing.

**MIKE:** The transport independence also means a retailer can stay on their existing API gateway—say, Kong or Apigee—and simply map UCP contracts to internal microservices. That lowers integration cost dramatically compared to the “custom API per partner” model that has plagued the industry.

**JORDAN:** Speaking of “custom APIs,” the presenter highlighted the fragmentation problem before UCP: each retailer‑payment pairing required bespoke adapters, leading to high OPEX and brittle version drift. With UCP, the contract is stable, and any new agent—Google Gemini, Microsoft Copilot, or a custom in‑house model—can plug in as long as it adheres to the schema.

**MIKE:** That standardization is a strategic moat for both merchants and PSPs. It lets payment providers like Fiserv focus on tokenization and fraud detection rather than building per‑agent adapters, and it lets retailers expose a clean, tokenizable catalog that agents can consume without negotiating terms each time.

**JORDAN:** Which segues into the Agent Payments Protocol, AP2. AP2 builds on the trust infrastructure of the payments industry—tokenized card numbers, dynamic authentication, and mandate signatures—to secure agent‑initiated transactions. The core innovation is the tamper‑proof mandate, a cryptographically signed intent object that binds the shopper’s consent, the agreed price, and the merchant’s SKU ID.

**MIKE:** In practice, AP2 mitigates three big risks: hallucinated prices (the LLM outputting a wrong amount), intent spoofing (an agent acting without explicit consent), and chargeback exposure. By anchoring the transaction in a signed mandate, downstream processors can verify that the price and SKU match the original shopper agreement before settlement.

**JORDAN:** Technically, AP2 uses a combination of JSON Web Tokens (JWT) for the mandate and a server‑side verification service that checks the signature against the merchant’s public key. It also integrates with token vaults to retrieve a one‑time-use payment token, ensuring PCI‑DSS compliance without ever exposing the raw PAN.

**MIKE:** From a market standpoint, early pilots—like the one with Fiserv—show that tokenized AP2 flows can be retrofitted onto existing digital wallets (Google Pay, Apple Pay) while still honoring the agent‑generated consent. That’s a big win for conversion, because shoppers don’t have to re‑enter payment details during the hand‑off from chat to checkout.

**JORDAN:** The Wayfair case study gives us a concrete scalability benchmark: they onboarded 30 million SKUs across multiple agent services using the UCP stack. They leveraged the Catalog Capability’s bulk upload endpoint, which accepts delta‑encoded CSV or Parquet files, and then mapped the product attributes to the UCP schema—essentially normalizing disparate vendor feeds into a single source of truth.

**MIKE:** Wayfair also demonstrated cross‑agent consistency. Whether a shopper interacted via Gemini on Wayfair.com, an Alexa skill, or a third‑party chatbot, the same SKU ID, price, and inventory level were returned, thanks to UCP’s centralized identity linking. That eliminates the “price surprise” problem that plagues omnichannel retail.

**JORDAN:** On the payments side, Fiserv’s integration with AP2 involved extending their existing token issuance service to emit AP2‑compatible mandates. They added a “price‑hash” field to the mandate payload, which is a SHA‑256 of the offered price and currency, preventing downstream tampering. Their pilot showed a 25 % reduction in fraud‑related chargebacks for agent‑initiated sales.

**MIKE:** Those numbers are compelling for any fintech looking to stay relevant as AI agents become the primary sales channel. It also underscores why tokenization and mandate‑based consent are non‑negotiable for the next wave of commerce.

**JORDAN:** Let’s not overlook the open‑source aspect. The UCP repository includes a conformance test suite, CI pipelines, and sample SDKs in Java, Python, and Go. That encourages community contributions—think of extensions for subscription billing or rental services—without waiting for Google to ship updates.

**MIKE:** And that openness mitigates vendor lock‑in, a critical concern for enterprise CIOs. By adopting a community‑driven protocol, a retailer can switch between AI providers—say from Gemini to Claude—without re‑architecting the backend, as long as the new provider speaks UCP.

**JORDAN:** Summarizing the technical stack: GECX provides the managed LLM layer; Shopping Agent adds conversation orchestration and consent handling; UCP supplies the lingua franca for catalog, cart, checkout, and order operations; AP2 secures the final payment handshake. Together they form an end‑to‑end, vendor‑agnostic pipeline for agentic commerce.

**MIKE:** Strategically, the message to senior leaders is clear: if you’re not exposing a tokenizable, schema‑aligned catalog today, you’ll be invisible to AI agents tomorrow. Investing in UCP compliance and AP2 readiness is a prerequisite for capturing that 30 % AI‑initiated shopper segment.

**JORDAN:** For engineers, the immediate action items are: audit your product feed for UCP schema compatibility, implement the JWT‑based mandate flow for payments, and prototype a Gemini‑driven Shopping Agent on a sandbox environment to validate the end‑to‑end experience.

**MIKE:** And for product leaders, start dialogue with your payment processor about AP2 support, and pilot a private‑preview GECX deployment on a low‑risk property—maybe a promotional landing page—to measure conversion lift versus your traditional funnel.

**JORDAN:** Before we wrap, a quick note on timelines: Gemini Enterprise and Shopping Agent are still in private preview, so access is limited. UCP is publicly available now; you can clone the repo and run the conformance tests today. AP2 is in early pilot, with broader rollout expected later this year.

**MIKE:** The upside is huge—AI agents are compressing the purchase funnel from weeks of research to minutes of conversation. With open standards like UCP and secure protocols like AP2, the ecosystem is finally ready for scale.

**JORDAN:** Key takeaways: (1) AI agents are the emerging primary discovery channel; (2) Google’s managed offerings give you a fast path to embed LLM‑driven assistants; (3) UCP eliminates brittle custom integrations; (4) AP2 secures the checkout against hallucination and fraud; and (5) Open standards ensure interoperability and future‑proofing.

**MIKE:** That’s the playbook for any retailer or payments provider that wants to stay competitive in the agentic commerce era. Thanks for joining us—catch the next episode where we’ll dissect real‑world performance metrics from the Wayfair pilot.

**JORDAN:** Until then, keep building, keep standardizing, and keep your customers’ consent at the core. See you next time.

