# Agentic commerce: Transform the shopping experience with Google agents and open standards

**Source:** https://www.youtube.com/watch?v=GNlWClpVtcQ  
**Video ID:** `GNlWClpVtcQ`

---

## Overview  
The session introduces **agentic commerce**, explaining how AI agents (like Google Gemini) can transform product discovery and checkout by consolidating search, filters, reviews and payment into a single conversational flow. Google Cloud showcases its toolkits—Gemini Enterprise for Customer Experience, the Shopping Agent preview, and open standards **UCP (Universal Commerce Protocol)** and **AP2 (Agent Payments Protocol)**—that let retailers and payment providers build secure, vendor‑agnostic AI‑driven shopping experiences. Real‑world examples from Wayfair and Fiserv illustrate large‑scale product onboarding and tokenized checkout in this new paradigm.

## New Features & Announcements  
- **Gemini Enterprise for Customer Experience (GECX)** – A managed suite that lets brands deploy AI‑powered product discovery, commerce and support on their own properties.  
- **Shopping Agent (preview)** – Google‑managed conversational shopping assistant that handles end‑to‑end purchase journeys, including multimodal inputs, cart management and consent‑based checkout.  
- **Universal Commerce Protocol (UCP)** – Open‑source, vendor‑agnostic API schema for AI‑driven commerce covering discovery, cart, checkout, order, identity linking and extensions (discounts, fulfillment).  
- **Agent Payments Protocol (AP2)** – Secure, tokenized payment protocol designed for AI agents, providing tamper‑proof mandates to mitigate fraud and hallucination risks.

## Topics Covered  
- **Why AI agents matter for retail** – 10× rise in brand discovery via LLMs (2025); 30 % of shoppers start product search with AI; agents compress the buying funnel into a single conversational step.  
- **The “cargo‑box” story** – Demonstrates how Gemini can synthesize constraints, budget and preferences to deliver a perfect product recommendation instantly.  
- **Opportunity & responsibility** – Brands must expose clean, searchable catalogs; payment providers need tokenized checkout to succeed in the agentic ecosystem.  
- **Gemini Enterprise & Shopping Agent** – Managed solutions that bring AI‑driven discovery and checkout to a merchant’s own site, with real‑time suggestions, consent‑based actions, and handling of complex queries (e.g., “outfit a graduation party”).  
- **Open standards (UCP & AP2)** – Architecture that sits between consumer‑facing AI surfaces (search, Gemini, merchant sites) and back‑end systems, defining four actors (platform, merchant of record, credential provider, payment service provider) and layered capabilities (catalog, cart, checkout, order, identity linking, extensions).  
- **Technical layers** – Service layer (vertical‑specific), common layer (shared functions like identity), capabilities, extensions, and transport layer (REST/JSON, MCP, A2A, iframe).  
- **Open‑source nature** – UCP code available at ucp.dev and GitHub; encourages community contributions and avoids vendor lock‑in.  
- **Payments security** – AP2 introduces tamper‑proof mandates to protect against hallucinated prices or fraudulent intents, building on the trust infrastructure of traditional e‑commerce.  
- **Customer case studies** – Wayfair onboarding 30 M products via agent services; Fiserv leveraging tokenized checkout for AI‑driven payments.

## Key Takeaways  
- AI agents can collapse the traditional e‑commerce funnel, delivering hyper‑relevant product recommendations and completing purchases in a single conversational exchange.  
- Retailers need well‑structured, AI‑ready catalogs; payment providers must adopt tokenized, secure checkout to thrive in the agentic commerce model.  
- Google’s Shopping Agent (preview) and Gemini Enterprise provide managed, brand‑centric ways to embed AI shopping experiences on merchant properties.  
- The **Universal Commerce Protocol (UCP)** offers an open, extensible standard for end‑to‑end commerce, ensuring interoperability and avoiding bespoke integrations.  
- **AP2** secures the payment leg of agent interactions, mitigating risks of hallucination and fraud with tamper‑proof mandates.  
- Open‑source availability of UCP empowers developers worldwide to build flexible, vendor‑agnostic commerce agents across any surface.  
- Early adopters like Wayfair and Fiserv demonstrate the scalability and real‑world impact of agentic commerce.

## Notable Quotes  
- “LLMs can help us sift through large amounts of data as well as constraints and preferences, and they can help us organize information from many different places, and ultimately help by driving decision.”  
- “We can collapse things like search bars, filters, browser tabs, product specs, product reviews… into a highly adaptive conversational thread.”  
- “Agents break that fundamental thing… we’re building trust through tamper‑proof mandates.”  
- “UCP creates a common language for AI agents to solve fragmented online shopping… with minimal custom code.”

---

## Podcast Script

**JORDAN:** Welcome to the AI Commerce Lab, where we unpack the cutting edge of agentic shopping. I’m Jordan, your deep‑dive host, and with me is Mike, who keeps an eye on strategy and impact. Today we’re breaking down Google Cloud’s latest “agentic commerce” announcement—Gemini Enterprise, the Shopping Agent preview, plus the open Universal Commerce Protocol and Agent Payments Protocol.

**MIKE:** Thanks, Jordan. The headline is simple: AI agents are about to collapse the entire e‑commerce funnel into a single conversational exchange. That’s a massive shift for retailers, payment processors, and the consumer experience alike. Let’s start with the why—what’s driving this urgency?

**JORDAN:** The data speaks volumes. In 2025 we’ve already seen a ten‑fold increase in brand discovery via LLMs, and roughly 30 % of shoppers now kick off product searches with an AI. More striking, 40 % of AI‑driven sessions land straight on a product detail page, indicating that the conversation is already generating purchase intent without a traditional browse‑and‑click path.

**MIKE:** That aligns with what we’re hearing from CMO circles—customers expect hyper‑relevant recommendations, and agents can synthesize constraints, budget, and preferences instantly. The “cargo‑box” story from the session illustrated that perfectly: dump a handful of requirements into Gemini and get a fully vetted product in seconds.

**JORDAN:** Exactly. And that compression of the funnel is what Google calls “agentic commerce.” The idea is to replace search bars, filters, multiple tabs, and review aggregators with a single, adaptive dialogue. But the technology stack to make that happen is non‑trivial. That’s where Gemini Enterprise for Customer Experience—GECX—enters.

**MIKE:** GECX is a managed suite, right? It lets brands run Gemini‑powered discovery, support, and checkout on their own domains, preserving brand identity and data ownership. How does that differ from the Shopping Agent preview?

**JORDAN:** GECX is the brand‑centric, self‑hosted offering. The Shopping Agent, on the other hand, is a Google‑managed conversational assistant that handles end‑to‑end purchase journeys on the merchant’s site. It supports multimodal inputs—text, images, even voice—and can orchestrate cart management, consent‑based checkout, and out‑of‑stock substitutions, all within a single thread. Think “how do I outfit a graduation party?” and the agent returns a curated set, adds items to the cart, and prompts for checkout.

**MIKE:** So merchants can choose between a fully managed agent or embedding the same capabilities via the open protocols. Speaking of which, the Universal Commerce Protocol—UCP—seems like the linchpin for interoperability. Walk us through its architecture.

**JORDAN:** UCP is a vendor‑agnostic API schema that sits between consumer‑facing AI surfaces (Gemini, AI‑Mode search, merchant sites) and the back‑end commerce stack. It defines four actors: the platform/agent, the merchant of record, the credential provider, and the payment service provider. The protocol is layered: a service layer for vertical‑specific use cases, a common layer for shared functions like identity linking, core capabilities (catalog, cart, checkout, order, identity), and extensions such as discounts or fulfillment. Transport is flexible—REST/JSON, Google’s MCP, A2A, or even an iframe for human‑in‑the‑loop approvals.

**MIKE:** That flexibility is crucial for enterprises that already have legacy integrations. By providing a common schema, UCP eliminates the “bespoke glue code” problem that has plagued AI‑driven checkout implementations. And the open‑source nature—code at ucp.dev and GitHub—means the community can extend it to verticals like groceries or travel without waiting on Google.

**JORDAN:** Right. The open‑source model also avoids vendor lock‑in, which is a common concern for large retailers. Now, on the payments side, Google introduced the Agent Payments Protocol—AP2. The core challenge is trust: agents could hallucinate prices or intents, leading to fraud.

**MIKE:** AP2 tackles that with tamper‑proof mandates, correct? How does that work in practice?

**JORDAN:** AP2 creates a cryptographically signed mandate that binds the shopper’s intent, the agreed price, and the payment token. The mandate travels alongside the checkout request, and any alteration—whether accidental or malicious—invalidates the transaction. This mirrors the trust infrastructure of traditional e‑commerce, but is designed for the stateless, conversational nature of agents.

**MIKE:** So from a risk management perspective, AP2 gives payment processors a way to enforce compliance and reduce chargeback exposure, even when the UI is an AI chat. That’s a game‑changer for fintechs. Speaking of real‑world validation, the session featured two case studies: Wayfair and Fiserv. What stood out?

**JORDAN:** Wayfair demonstrated massive catalog onboarding—30 million SKUs—through the agentic services. They leveraged UCP’s catalog and cart capabilities to expose their inventory to Gemini, enabling the agent to recommend items across categories in real time. The result was a seamless, AI‑driven discovery layer on top of an existing retail platform.

**MIKE:** And Fiserv showed how tokenized checkout can be integrated via AP2, offering a secure, frictionless payment flow for AI‑initiated purchases. Their implementation highlighted the importance of credential providers issuing payment tokens that are compatible with the tamper‑proof mandates.

**JORDAN:** Both examples underscore the dual responsibility: retailers must expose clean, searchable, AI‑ready catalogs, while payment providers must adopt tokenized, mandate‑backed checkout. Without both, the agentic loop breaks.

**MIKE:** Let’s circle back to the strategic implications. If agents can close a sale in one conversational turn, how does that reshape a retailer’s acquisition funnel?

**JORDAN:** Funnel metrics will shift from click‑through rates to conversational conversion rates. Brands will need to invest in catalog enrichment—semantic tagging, attribute normalization—and in real‑time inventory signals so the agent can guarantee availability. Moreover, the consent model becomes paramount; agents must explicitly capture purchase intent before invoking AP2.

**MIKE:** That also raises UX considerations. Consent dialogs need to be unobtrusive yet legally robust, especially across jurisdictions with PSD2 or CCPA constraints. The Shopping Agent’s built‑in consent framework seems to address that, but developers building custom agents via UCP must implement similar safeguards.

**JORDAN:** Exactly. The protocol includes “identity linking” as a core capability, enabling a secure mapping between the shopper’s AI session and their payment credentials without exposing raw data. This is where the credential provider—often a digital wallet—plays a pivotal role.

**MIKE:** From a product roadmap angle, the extensibility of UCP means we’ll likely see new capabilities added—think subscriptions, rentals, or even dynamic pricing based on context. The extensions layer already supports discounts and fulfillment, so adding a “lease” capability would fit neatly.

**JORDAN:** And because extensions are decorators rather than core capabilities, they can be injected at the appropriate stage—say, applying a promotional discount right after cart formation but before checkout. This modularity reduces the need for monolithic, hard‑to‑maintain APIs.

**MIKE:** Summing up, the key takeaways are: AI agents can compress the entire e‑commerce journey into a single, context‑rich conversation; retailers must prepare AI‑ready catalogs; payment providers need tokenized, mandate‑protected checkout; and Google’s managed solutions—GECX and Shopping Agent—offer quick entry points, while UCP and AP2 provide the open, extensible foundation for long‑term, vendor‑agnostic deployments.

**JORDAN:** Absolutely. The open‑source availability of UCP invites the community to contribute and adapt the protocol for niche verticals, ensuring we avoid a new wave of siloed integrations. Meanwhile, AP2 gives the trust layer needed for large‑scale adoption.

**MIKE:** For anyone listening—whether you’re a CTO, a Head of Commerce, or a fintech product lead—the message is clear: start auditing your product data pipelines now, and explore tokenized checkout options if you haven’t already. The agentic commerce window is opening, and early adopters like Wayfair and Fiserv are already reaping efficiency gains.

**JORDAN:** That wraps our deep dive into Google Cloud’s agentic commerce ecosystem. Thanks for joining us, and stay tuned for our next episode where we’ll hear from developers building custom agents on top of UCP.

**MIKE:** Until then, keep experimenting, stay secure, and let the agents do the heavy lifting. Catch you next time.

