# Agentic commerce: Transform the shopping experience with Google agents and open standards

**Source:** https://www.youtube.com/watch?v=GNlWClpVtcQ  
**Video ID:** `GNlWClpVtcQ`

---

## Overview
In this breakout session Google Cloud introduces **Agentic Commerce**, a new way to let shoppers interact with retail and payment services through conversational AI agents. Jesse, an AI incubation lead, outlines the market opportunity, showcases Google’s tooling (Gemini Enterprise, Shopping Agent, Universal Commerce Protocol [UCP] and Agent Payments Protocol [AP2]), and shares real‑world case studies from Wayfair and Fiserv. The goal is to demonstrate how open, standards‑based APIs can enable seamless, secure buying experiences that live wherever the consumer is—search, Gemini, or a merchant’s own site.

## New Features & Announcements
- **Gemini Enterprise for Customer Experience (GECX)** – A managed suite that lets brands embed Gemini‑powered AI experiences (discovery, commerce, support) on their own properties.  
- **Shopping Agent (preview)** – A Google‑managed, multimodal shopping assistant that can understand complex requests, suggest products, manage carts, and complete consent‑based checkout.  
- **Universal Commerce Protocol (UCP)** – Open‑source, vendor‑agnostic standard for end‑to‑end AI‑driven commerce (catalog, cart, checkout, order, identity linking, extensions).  
- **Agent Payments Protocol (AP2)** – Open protocol that adds tamper‑proof, tokenized payment mandates to protect against fraud and hallucinated pricing in agent interactions.

## Topics Covered
- **Why agentic commerce matters** – LLMs compress the purchase funnel, turning many search/filter steps into a single conversational thread; research shows a 10× rise in AI‑driven brand discovery and 30 % of shoppers now start product searches with AI.  
- **Consumer expectations & retailer responsibility** – Brands must curate clean, AI‑ready catalogs; payment providers need secure tokenized checkout to win in an agent‑first world.  
- **Gemini Enterprise & Shopping Agent** – Demonstrated how a managed shopping assistant can handle complex queries (e.g., “outfit an entire graduation party”), suggest alternatives, and execute consented purchases.  
- **Open standards: UCP architecture** – Describes the four actors (platform/agent, merchant of record, credential provider, payment service provider) and the layered stack (service, common, capabilities, extensions, transport). Emphasizes minimal custom code, REST/JSON, MCP, A2A, or iframe transports.  
- **Open‑source nature** – UCP is published at ucp.dev and GitHub, encouraging community contributions and federation across any surface or agent.  
- **Payments security with AP2** – Introduces tamper‑proof mandates and tokenization to mitigate fraud, chargebacks, and AI hallucinations during checkout.  
- **Case studies** – Wayfair’s onboarding of 30 M products into multiple agent channels; Fiserv’s integration of secure tokenized payments for AI‑driven checkout.  
- **Future outlook** – Plans to extend UCP to verticals like groceries and travel, and to broaden the set of capabilities (discounts, fulfillment, etc.).

## Key Takeaways
- AI agents are already reshaping discovery; retailers must adapt or lose traffic to AI‑first experiences.  
- Google’s Shopping Agent (preview) shows that a single conversational interface can replace traditional search, filters, and cart pages.  
- The **Universal Commerce Protocol (UCP)** provides a common, extensible schema that eliminates bespoke, fragile integrations across retailers and payment providers.  
- **AP2** adds a secure, tokenized layer to protect both merchants and consumers in an agent‑driven checkout flow.  
- All protocols are open source, ensuring interoperability, avoiding vendor lock‑in, and allowing developers to build on any tech stack.  
- Real‑world pilots (Wayfair, Fiserv) prove the model works at scale—tens of millions of SKUs and secure payments across multiple agent surfaces.  
- The ecosystem is designed to be vertically extensible, paving the way for AI‑powered commerce in groceries, travel, and beyond.

## Notable Quotes
- “LLMs can help us sift through large amounts of data as well as constraints and preferences, and they can help us organize information from many different places, and ultimately help by driving decision.”  
- “40 % of all AI‑driven e‑commerce sessions land directly on product‑detail pages – AI is actually helping develop a fully formed purchase intent.”  
- “We built UCP with industry leaders so it’s not an isolated Google‑only solution – it’s a vendor‑agnostic standard for AI commerce.”  
- “AP2 creates tamper‑proof mandates to ensure agents can’t hallucinate prices or intent, keeping the checkout experience trustworthy.”

---

## Podcast Script

**JORDAN:** Hey everyone, welcome back to the podcast. I’m Jordan, your detail‑driven host, and with me as always is the big‑picture guy, Mike.

**MIKE:** Hey folks! Today we’re diving into “agenda commerce” and how AI agents are reshaping the whole shopping experience, straight from a Google Cloud breakout session.

**JORDAN:** The session kicked off with Jesse, an AI incubation lead at Google Cloud, laying out the agenda: opportunity, building blocks, a Wayfair case study, and a Fiserv payment story.

**MIKE:** Right, and the hook was a personal story about packing a cargo box for a family road trip—until an LLM named Gemini whipped up the perfect recommendation in seconds.

**JORDAN:** That anecdote illustrates the core argument: large language models can sift through massive product catalogs, constraints, and reviews to surface a single, hyper‑relevant suggestion.

**MIKE:** Which is exactly what shoppers are already doing—research shows a 10× jump in brand discovery via LLMs and 30% of shoppers start product discovery with AI.

**JORDAN:** Those numbers are backed by stats like 40% of AI‑driven e‑commerce sessions landing directly on product detail pages, indicating strong purchase intent.

**MIKE:** So the question is, how do retailers meet shoppers where they are, without creating a new, fragmented checkout flow?

**JORDAN:** Google’s answer is the Gemini Enterprise for Customer Experience—GECX—a managed suite that includes a “shopping agent” preview. It can handle multimodal queries, suggest whole outfits, and even move items to cart with consent.

**MIKE:** And the real kicker is that it’s not a closed black box; Google also released open protocols—UCP and AP2—to let anyone build their own agents on top of existing back‑ends.

**JORDAN:** The Universal Commerce Protocol (UCP) standardizes the schema between four actors: the platform (the agent), the merchant of record, the credential provider, and the payment service provider. That eliminates the need for bespoke integrations.

**MIKE:** It’s like giving every AI assistant a common language, so whether you’re on Gemini, AI‑mode search, or a retailer’s own site, the transaction flow stays consistent and secure.

**JORDAN:** UCP’s architecture splits into a services layer, a common layer, capabilities (catalog, cart, checkout, order, identity linking), and extensions like discounts. All communicated via JSON over REST, MCP, A2A, or even an iframe for human‑in‑the‑loop scenarios.

**MIKE:** And because it’s open source—ucp.dev and on GitHub—developers can contribute, fork, or adapt it, keeping the ecosystem transparent and vendor‑agnostic.

**JORDAN:** On the payments side, AP2 (Agent Payments Protocol) adds tamper‑proof mandates to prevent hallucinated prices or unintended purchases, building on the trust infrastructure the payment industry established years ago.

**MIKE:** In practice that means a shopper can say “buy this” to an AI, and the payment token is verified against a credential provider before any funds move—reducing fraud and chargeback risk.

**JORDAN:** Wayfair’s case study showed they successfully onboarded 30 million products into multiple agenda services using these tools, proving the model scales to massive catalogs.

**MIKE:** And Fiserv’s involvement highlighted how payment processors can leverage AP2 to offer tokenized checkout across any AI surface, turning a potential security nightmare into a competitive advantage.

**JORDAN:** So the takeaway: AI agents are compressing the buying funnel, but to do it responsibly retailers need standardized, open protocols for catalog, checkout, and payments.

**MIKE:** And for shoppers, that means less friction, more personalized recommendations, and a safer checkout—even if you’re just trying to find the perfect cargo box for a road trip.

**JORDAN:** That wraps up our deep dive into agenda commerce—thanks to the Google Cloud team for the insights and to you for listening.

**MIKE:** Stay curious, stay secure, and we’ll see you next time. Bye!

