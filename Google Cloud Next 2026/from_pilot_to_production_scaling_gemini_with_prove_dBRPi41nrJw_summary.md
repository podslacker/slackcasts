# From pilot to production: Scaling Gemini with proven practices

**Source:** https://www.youtube.com/watch?v=dBRPi41nrJw  
**Video ID:** `dBRPi41nrJw`

---

## Overview  
The panel, moderated by Google Applied AI leader **Donna**, brings together experts from DeepMind, JetBrains, and Roblox to discuss how they moved Gemini from experimental pilots to large‑scale production. Each speaker describes their organization’s use‑cases, the engineering challenges they faced—latency, cost, reliability, and prompt tuning—and the practices that helped them turn promising prototypes into reliable services.

## Topics Covered
- **Introductions & company context** – Arca (DeepMind), Nick (JetBrains), Naren (Roblox) outline their roles and why Gemini matters to them.  
- **How Gemini is used today**  
  - **Roblox**: safety pipeline (text, image, video, 3‑D) that routes ambiguous content to Gemini for high‑recall/precision decisions.  
  - **JetBrains**: the **Junior** AI development assistant uses **Gemini Flash** as its default model for cost‑effective code generation, achieving top‑rank benchmark scores.  
  - **DeepMind Applied AI**: Gemini assists in domain‑expert discovery, synthetic user studies, code generation, vulnerability detection, and brainstorming product strategy.  
- **From pilot to production – engineering constraints**  
  - **JetBrains**: agentic software brings variable model behavior; solution = close partnership with ML research, deep analysis of inference paths, token usage, and iterative prompt optimization.  
  - **Roblox**: real‑time content moderation required precise recall/false‑positive control, latency budgeting, and cost containment; they iterated on prompt engineering, load‑testing, and traffic routing.  
  - **DeepMind**: maturity of supporting scaffolding (observability, drift detection, serving infra) is still evolving; investments in Vertex AI and other serving platforms are crucial.  
- **Best practices & observability** – need for robust monitoring, drift tracking, rapid root‑cause analysis, and patching mechanisms; migration from Gemini 1.5 → 2.0 taught hard lessons, but moving to 3.0 feels smoother.  
- **Evaluating models for real‑world ROI** – academic benchmarks don’t reflect production needs; evaluate against **hard, domain‑specific test sets**, measure recall/false‑positive rates, and treat metrics as “gameable” unless the evaluation data is sufficiently challenging.  

## Key Takeaways
- **Hybrid approach works best** – combine specialized in‑house models for high‑confidence decisions with Gemini for ambiguous cases.  
- **Prompt engineering is an art**; ongoing collaboration with DeepMind’s experts (or internal ML researchers) is essential to achieve the required precision without exploding false positives.  
- **Latency and cost are trade‑offs**; monitor P90/P75 latency distributions and keep Gemini traffic proportionate to budget constraints.  
- **Observability stacks must evolve** – drift detection, uptime dashboards, and rapid rollback/patching are non‑negotiable for production‑grade agentic systems.  
- **Benchmarks alone are insufficient**; build internal, hard evaluation suites that mirror the live workload to prevent “gameable” metric pitfalls.  
- **Maturity of serving infrastructure is catching up**; leveraging Google Cloud services (Vertex AI, dedicated serving platforms) eases migration and scaling.  

## Notable Quotes
- “**We almost always have a high‑recall and a high‑precision model.** When they’re unsure, that’s when we send them to Gemini.” – Naren, Roblox  
- “**Prompt tuning is still an art.** We get a lot of help from the DeepMind teams, but achieving super‑high precision requires manual iteration." – Naren, Roblox  
- “**The initial prototypes are easy.** Taking them to production is really hard." – Naren, Roblox  
- “**Observability, drift measurement, and quick root‑cause analysis** are the pillars that turn an MVP into a reliable service." – Arca, DeepMind  
- “**Academic benchmarks don’t reflect real‑world ROI.** Building a hard evaluation set is the hardest part." – Naren, Roblox

---

## Podcast Script

**JORDAN:** Hey everyone, welcome back to the podcast. I’m Jordan, your go‑to for the nuts and bolts of how these AI systems actually work.

**MIKE:** And I’m Mike, here to explore why it matters for you, the developer or product leader listening in. Today we’re breaking down a panel on “Scaling Gemini with Proven Practices.”

**JORDAN:** The panel featured Arca from DeepMind, Nick from JetBrains, and Naren from Roblox. They each gave quick intros—DeepMind’s applied AI team, JetBrains’ Junior AI development agent, and Roblox’s safety engineering.

**MIKE:** Right, and the common thread was how they’re using Google’s Gemini models in production, not just in labs.

**JORDAN:** Let’s start with Naren. He explained that Roblox streams up to 700 k requests per second, needing both high recall and high precision for content safety. They use their own specialized models for confident decisions, and fall back to Gemini for the ambiguous cases.

**MIKE:** That’s a clever cascade—keep your cheap, fast models in the front line, and only call Gemini when you really need its broader knowledge. Makes sense for a platform with user‑generated text, images, videos, and even 3D worlds.

**JORDAN:** Nick’s story from JetBrains was all about cost‑effectiveness. They chose Gemini Flash as the default because the quality‑to‑cost ratio nailed their budget, letting them hit top‑two on terminal benchmarks and match Claude 2 on software‑dev tasks—all while slashing per‑task cost by tenfold.

**MIKE:** Ten times cheaper and still competitive on real dev workloads? That’s the kind of ROI developers care about. It shows you don’t always need the biggest model to get the biggest impact.

**JORDAN:** Arca from DeepMind painted a broader picture—Gemini as a partner throughout the product lifecycle, from understanding domain terminology like “block trade” to generating synthetic user studies for product validation. They also use it for code generation, vulnerability detection, and bug triage.

**MIKE:** So it’s not just a content filter or a coding assistant; it’s a full‑stack collaborator that helps engineers and product teams talk the language of their business domains.

**JORDAN:** When the panel moved to engineering constraints, Nick highlighted that agentic software isn’t like traditional apps. You have to monitor prompt behavior, inference latency, token usage, and iterate on prompts constantly. That deep observability let them succeed on benchmarks.

**MIKE:** That resonates with anyone who’s tried to ship an LLM feature—prompt engineering is an ongoing art, not a set‑and‑forget step.

**JORDAN:** Naren added that scaling from a prototype to production introduced four hard metrics: recall, false‑positive rate, latency, and cost. Their P90 latency jumped from 30 ms to a second after adding Gemini, which was acceptable for some use cases but required careful budgeting.

**MIKE:** It’s a classic trade‑off: you get higher recall, but you pay in latency and dollars. The key is to measure those numbers yourself and decide where the premium is worth it.

**JORDAN:** Arca pointed out that the ecosystem is still maturing—observability, drift detection, and automated patching aren’t fully baked yet. Google’s Vertex AI and other serving platforms are trying to fill those gaps, but organizations still need to build internal scaffolding.

**MIKE:** In other words, the tools are getting better, but the responsibility to stitch them together still sits on the engineering team.

**JORDAN:** The panel also touched on evaluation. Naren warned that benchmark scores are gameable and emphasized building hard, realistic eval sets in three phases to truly test recall and false positives.

**MIKE:** That’s a solid framework—don’t rely on public leaderboards; craft your own test suite that mirrors the messiness of production data.

**JORDAN:** Summing up, the takeaways are: use a layered model approach for cost and latency, invest in prompt observability, treat evaluation as a custom, evolving process, and expect to build your own production scaffolding around Gemini.

**MIKE:** And from a big‑picture view, those practices let you turn a shiny LLM into a reliable product feature that actually moves the needle for users—whether they’re building games, writing code, or launching new services.

**JORDAN:** Thanks for tuning in, everyone. Keep digging into the how, and we’ll see you next time.

**MIKE:** Appreciate you listening. Stay curious, stay practical, and catch you on the next episode.

