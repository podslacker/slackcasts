# Agentic commerce: Transform the shopping experience with Google agents and open standards

**Source:** https://www.youtube.com/watch?v=GNlWClpVtcQ  
**Video ID:** `GNlWClpVtcQ`

---

## Overview  
The session introduces **agentic commerce** – a new way to let AI agents handle product discovery, recommendation, and checkout directly within a retailer’s or payment provider’s ecosystem. Google Cloud explains the market opportunity, showcases early customer successes (Wayfair and Fiserv), and walks through the core building blocks: the **Gemini Shopping Agent**, the open **Universal Commerce Protocol (UCP)**, and the **Agent Payments Protocol (AP2)**. The goal is to give brands and payments partners a transparent, standards‑based stack that removes friction and enables secure, AI‑driven purchases without vendor lock‑in.

## New Features & Announcements  
- **Gemini Shopping Agent (preview)** – A managed AI shopping assistant that can reason over multimodal inputs, suggest complete solutions, and complete purchases with user consent.  
  Timeline: preview (pilot customers)  
  Availability: Private preview  

- **Universal Commerce Protocol (UCP)** – Open‑source standard that defines a common schema and API contract for AI agents to interact with retailers, identity providers, and payment services across the full purchase journey.  
  Availability: Public on ucp.dev / GitHub  

- **Agent Payments Protocol (AP2)** – Secure, token‑based payment protocol designed for AI‑mediated transactions, adding tamper‑proof mandates to prevent fraud and hallucinated pricing.  
  Availability: Internal pilot (timeline not disclosed)

## Topics Covered  
- **Why agentic commerce now?**  
  *LLMs dramatically improve product discovery; 30 % of shoppers already start searches with AI and 40 % of AI‑driven sessions land on product detail pages.*  

- **The shopper’s pain point illustrated** – A personal “cargo‑box” story shows how AI can collapse many browsing steps (search, filters, reviews) into a single conversational request.  

- **Business opportunity for retailers & payment providers**  
  *Brands must optimize catalogs for AI agents; payment processors that offer tokenized checkout will capture the emerging channel.*  

- **Gemini Enterprise for Customer Experience (GECX)**  
  *A suite of managed AI tools that lets brands embed Gemini‑powered discovery, commerce, and support directly on their sites.*  

- **Shopping Agent capabilities**  
  *Real‑time product suggestions, cart management, checkout with consent, handling of abstract requests (e.g., “outfit a graduation party”).*  

- **Open standards: UCP**  
  *Defines interactions among four actors (platform/agent, merchant of record, credential provider, payment service). Layers include Services, Common, Capabilities (catalog, cart, checkout, order, identity linking), Extensions (discounts, fulfillment), and Transport (REST/JSON, MCP, A2A, iframe).*  

- **Open standards: AP2**  
  *Provides tamper‑proof payment mandates for AI agents, addressing fraud, chargebacks, and hallucinated pricing.*  

- **Customer case studies**  
  *Wayfair onboarded 30 M products to multiple agent services; Fiserv demonstrated how a payments platform can securely enable AI‑driven checkout.*  

- **Ecosystem vision**  
  *UCP is vendor‑agnostic, extensible to other verticals (groceries, travel), and encourages a federated commerce layer across any surface—search, Gemini app, or third‑party agents.*  

## Key Takeaways  
- AI agents are already reshaping discovery; retailers must adapt or lose a fast‑growing purchase channel.  
- Gemini Shopping Agent (preview) offers a turnkey, consent‑driven shopping assistant that can handle end‑to‑end transactions on a brand’s own property.  
- UCP provides an open, extensible contract that eliminates bespoke integrations and supports a plug‑and‑play commerce layer across retailers, identity providers, and payment processors.  
- AP2 adds the necessary security guarantees for AI‑mediated payments, mitigating hallucination and fraud risks.  
- Google’s approach is deliberately open‑source to avoid lock‑in and to foster industry‑wide adoption of common commerce standards.  
- Early adopters (Wayfair, Fiserv) show that large catalogs and complex payment ecosystems can be integrated quickly, validating the model.  

## Notable Quotes  
- “LLMs can help us sift through large amounts of data as well as constraints and preferences, and they can help us organize information from many different places, and ultimately help by driving decision.”  
- “We can collapse things like search bars, filters, browser tabs, product specs, product reviews… into a highly adaptive conversational thread.”  
- “By leveraging these transparent, vendor‑agnostic standards, you can actually build a seamless shopping ecosystem… with complete flexibility and absolutely no vendor lock‑in whatsoever.”  
- “AP2… builds trust through this agentic interface with tamper‑proof mandates, protecting against hallucinated prices and fraud.”

---

## Podcast Script

**JORDAN:** Hey folks, welcome back to the show! I’m Jordan, and today we’re diving into something that’s reshaping how we shop online—agenda commerce and the AI agents that are making it happen.

**JORDAN:** Imagine you’re planning a family road trip, juggling strollers, a golden retriever, and a million product options for a roof‑top cargo box. I was buried under tabs and reviews until I tossed all my constraints into Google’s Gemini, and in seconds it served up the perfect match. That’s the power of large language models: they can sift through oceans of data, align it with your preferences, and hand you a decision on a silver platter.

**JORDAN:** And it’s not just my personal saga. Recent research shows a ten‑fold jump in brand discovery through LLMs this year, with 30 % of shoppers kicking off product hunts via AI. In fact, 40 % of AI‑driven e‑commerce sessions land straight on product detail pages, meaning the AI is already building purchase intent before you even click “add to cart.”

**JORDAN:** So, what does this mean for retailers and payment providers? The opportunity is massive, but it comes with a responsibility to make sure AI agents can safely surface and transact on your catalog. That’s where Google Cloud’s toolkit steps in, offering open‑source protocols and managed services to bridge the gap between AI and the checkout flow.

**JORDAN:** One of the flagship offerings is Gemini Enterprise for Customer Experience—aka GECX. It’s a unified suite that lets brands embed AI‑powered discovery, commerce, and support directly into their own properties, keeping the experience on‑brand while leveraging Google’s massive AI horsepower.

**JORDAN:** At the heart of GECX is the Shopping Agent, currently in preview. Think of it as a super‑savvy concierge that can understand multimodal inputs, reason through complex requests like “outfit a graduation party,” and seamlessly move items into a cart and checkout with explicit user consent. It’s designed to strip away the endless filtering and browsing steps we all dread.

**JORDAN:** While the Shopping Agent gives you a managed, end‑to‑end solution, Google also released two open protocols: UCP—the Universal Commerce Protocol—and AP2, the Agent Payments Protocol. These standards let you build high‑code agents on top of any existing tech stack, ensuring you stay vendor‑agnostic and avoid lock‑in.

**JORDAN:** UCP tackles a major pain point: the need for bespoke integrations every time you want an AI agent to talk to a retailer or payment system. By defining a common schema for everything from product discovery to order tracking, UCP lets you plug into multiple AI surfaces—think Gemini, AI‑mode search, or even a custom chatbot—without rewriting code.

**JORDAN:** The protocol sits between the consumer‑facing surface and your back‑end, orchestrating interactions among four actors: the AI platform, the merchant of record, the credential provider, and the payment service provider. Its layered architecture—services, common, capabilities, extensions, and transport—means you can add verticals like groceries or travel without overhauling the whole stack.

**JORDAN:** And because UCP is fully open source on ucp.dev and GitHub, developers can contribute, raise issues, and even customize implementations. Google also offers an opinionated version that ships with Gemini and AI‑mode, giving early adopters a turnkey path while the community builds the surrounding ecosystem.

**JORDAN:** On the payments side, AP2 introduces tamper‑proof mandates and tokenized checkout flows to mitigate the risks of hallucinated prices or fraudulent intents that AI agents could introduce. It’s essentially the modern version of the trust infrastructure that got us past the early days of fearing to type our credit card numbers online.

**JORDAN:** To ground all this in real‑world success, Wayfair recently onboarded 30 million products across various AI services using these tools, and fintech leader Fiserv is leveraging the same protocols to streamline payments. Their stories illustrate how the blend of AI, open standards, and secure checkout can unlock scale without sacrificing control.

**JORDAN:** So, what’s the takeaway? AI agents are already reshaping discovery, and with open protocols like UCP and AP2, retailers can meet shoppers where they are, reduce friction, and keep the transaction secure—all while staying flexible and future‑proof.

**JORDAN:** That’s it for today’s deep dive into agenda commerce. Thanks for listening, and as always, keep experimenting with the new tools on the horizon. Until next time, I’m Jordan—stay curious and happy shopping!

