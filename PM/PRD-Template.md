# Product Requirements Document (PRD) — Reusable Template

> **How to use this template**
> This file contains two tiers in one place:
> - **PART A — Core PRD**: the 10 sections you fill in for *every* project. Keep it lean.
> - **PART B — Extended sections**: add these only for larger bets, regulated work, or client/handoff-heavy projects.
>
> **Rules of thumb**
> - Write the **Problem** and **Goals** sections first and well. They are ~80% of the value. Everything else serves them.
> - A PRD is a *living document*. Update it when decisions change — don't write it once and abandon it.
> - If a section doesn't apply, write "N/A — because…" rather than deleting it. The reason is information.
> - Delete this instruction block and any italic *guiding prompts* once the doc is written.
>
> **Stage map — a PRD is written in passes, not all at once.** Don't try to complete everything up front:
> | Stage | When | Fill in |
> |---|---|---|
> | **1. Planning** | Exploring the problem space | §1 Metadata, §2 TL;DR, §3 Problem, §4 Goals, §5 Non-Goals |
> | **2. Kickoff** | Confident in the problem, moving to solution | §6 Users, §7 Requirements, §8 Solution & UX |
> | **3. Solution Review** | Design/scope changes during build | Update §7, §8; keep §10 Open Questions live |
> | **4. Launch Readiness** | Pre-ship | §9 Risks, §11 Release Plan; finalize Part B as needed |

---

# PART A — CORE PRD
*(Always fill this in.)*

## 1. Document Metadata

| Field | Value |
|---|---|
| **Product / Feature name** | |
| **Author / Owner** | |
| **Stakeholders** | *(Eng lead, Design, PM, QA, GTM…)* |
| **Status** | Draft / In Review / Approved / In Build / Shipped |
| **Version** | v0.1 |
| **Last updated** | YYYY-MM-DD |
| **Related links** | *(Designs, tickets, research, dashboards)* |

---

## 2. TL;DR

*One short paragraph (3–4 sentences) anyone in the company could read and understand: what we're building, for whom, and why. Write this last, but put it first.*

---

## 3. Problem & Why Now

*The anchor of the whole document. Be specific.*

- **What is the problem?** *(Describe the user/business pain, not the solution.)*
- **Who has it?** *(Which users or segments, and how often.)*
- **Why does it matter now?** *(What changed — market, data, strategy, deadline?)*
- **What happens if we do nothing?** *(Force yourself to justify the work.)*
- **Evidence** *(Data points, quotes, support tickets, research that prove this is real.)*

---

## 4. Goals & Success Metrics (Hypothesis)

*Frame the work as a testable bet, not a wish list.*

> **Hypothesis:** We believe that **[building X]** for **[these users]** will result in **[outcome Y]**, which we'll measure by **[metric Z]**. We'll know we're right if **[target]** within **[timeframe]**.

| Goal | Metric | Baseline | Target | How measured |
|---|---|---|---|---|
| | | | | |

- **How will we know if we were wrong?** *(Define the failure signal up front.)*
- **Guardrail metrics** *(What must NOT get worse — e.g., latency, churn, support load.)*

---

## 5. Non-Goals / Out of Scope

*Explicitly list what this PRD is **not** doing. This is the single best defense against scope creep — be generous here.*

- Not doing: …
- Not doing: …
- Deferred to later: …

---

## 6. Users & Key Scenarios

**Target users / personas**

| Persona | Who they are | Their job-to-be-done | Key pain |
|---|---|---|---|
| | | | |

**Key scenarios / use cases**

1. **As a** [user] **I want to** [action] **so that** [outcome].
2. …
3. *(Cover the primary happy path + the 1–2 most important edge cases.)*

---

## 7. Requirements

*Prioritize ruthlessly. P0 = launch blocker, P1 = important but shippable without, P2 = nice-to-have.*

| ID | Requirement | Priority | Notes / Acceptance criteria |
|---|---|---|---|
| R1 | | P0 | |
| R2 | | P1 | |
| R3 | | P2 | |

*Non-functional requirements that are critical to this feature (fold the rest into Part B):*
- Performance: …
- Security / privacy: …
- Accessibility: …

---

## 8. Solution & UX

- **Proposed solution** *(High-level approach — how the requirements come together.)*
- **User flows** *(Step-by-step, or link to flow diagram.)*
- **Designs** *(Figma / wireframe links. Embed key screens if helpful.)*
- **Key states to cover:** empty, loading, error, success, edge cases.

---

## 9. Risks, Dependencies & Assumptions

| Type | Item | Impact | Mitigation / Owner |
|---|---|---|---|
| Risk | | | |
| Dependency | | | |
| Assumption | | | |

---

## 10. Open Questions

*Keep this visible and current — it's the highest-traffic section during build.*

| # | Question | Owner | Status / Answer |
|---|---|---|---|
| 1 | | | Open |

---

## 11. Release Plan & Milestones

| Phase / Milestone | Scope | Target date | Owner | Status |
|---|---|---|---|---|
| | | | | |

- **Rollout approach:** *(Internal → beta → GA? Feature flag? % rollout?)*
- **Launch dependencies / gates:** …

---

# PART B — EXTENDED SECTIONS
*(Add only when the project warrants it — large bets, regulated domains, external client work, or heavy engineering handoffs. Skip what doesn't apply.)*

## B1. Detailed Non-Functional Requirements
- **Performance & scale:** *(Expected load, response-time SLAs, concurrency.)*
- **Security:** *(Authn/authz, data handling, threat considerations.)*
- **Privacy & compliance:** *(GDPR, SOC 2, HIPAA, data residency, retention.)*
- **Reliability:** *(Uptime SLA, failover, backups.)*
- **Accessibility:** *(WCAG level, keyboard nav, screen reader.)*
- **Internationalization / localization:** …

## B2. Technical Design & Architecture
- **Architecture overview** *(Diagram or description.)*
- **APIs / contracts** *(New or changed endpoints, schemas.)*
- **Data model** *(New tables/fields, migrations.)*
- **Third-party / integration points** …
- **Tech debt / refactors implied** …

## B3. Competitive & Market Context
- **Alternatives users have today** *(Competitors, workarounds, status quo.)*
- **Our differentiation** …
- **Market / strategic fit** …

## B4. Analytics & Instrumentation Plan
- **Events to track** *(Name, trigger, properties.)*
- **Dashboards / reports** *(Where success metrics will be monitored.)*
- **Experiment design** *(A/B test, success criteria, sample size, duration.)*

## B5. Go-to-Market & Launch Checklist
- **Positioning / messaging** …
- **Docs & support enablement** …
- **Pricing / packaging impact** …
- **Launch checklist:** marketing, sales enablement, support runbook, legal sign-off.

## B6. AI / ML Feature Considerations
*(Add this block when the feature uses AI/ML — LLMs, classifiers, recommenders, generative, or agents. These are **questions you must answer**, not authoritative compliance guidance; AI regulation moves fast and varies by domain. Cost, latency, privacy and compliance live in B1 — reference them, don't duplicate.)*

**B6.0 — Gate: should this even be AI?**
- **Type of AI:** Classification / Recommendation / Generative (text/image) / RAG / Agent (takes actions) / Other.
- **Why AI over rules?** *(Would a deterministic/rules-based approach be simpler, cheaper, more predictable? Justify the ML choice — most failed AI features fail here.)*
- *(Fill only the subsections below that fit your AI type. An agent needs B7.4 heavily; a spam classifier barely.)*

**B6.1 — Model & approach**
- Build vs. buy *(in-house model vs. third-party API/provider)*.
- Required model **capabilities** *(reasoning, multimodal, context length…) — describe needs, not a specific model name.*
- Technique: prompting / RAG / fine-tune / classical ML.

**B6.2 — Data**
- Training / grounding / retrieval data sources.
- Rights to use the data; PII handling; freshness & update cadence.
- Cold-start strategy *(what happens before you have data).*

**B6.3 — Evaluation (how we measure "good")**
- **Eval dataset & baseline** *(what you test against; current/comparison performance).*
- **Metrics:** accuracy (precision/recall/F1, factual correctness), quality (coherence, tone), operational.
- **Thresholds:** launch (minimum to ship) / target / aspirational.
- **Offline (pre-launch) vs. online (post-launch)** evaluation method + A/B design.

**B6.4 — Safety, failure modes & guardrails**
- Failure modes: hallucination, bias/fairness, toxic/unsafe output, prompt injection, adversarial input.
- Guardrail / mitigation for each.
- **Fallback behavior for every failure mode** *(what the user sees when the model is wrong, low-confidence, or unavailable).*
- **Human-in-the-loop:** review/approve before action? When can the user override? *(Critical for agents.)*

**B6.5 — Transparency & UX**
- Does the user know it's AI? How are confidence, citations/sources, and errors surfaced?

**B6.6 — Post-launch quality ownership (the part that kills AI features)**
- **Who owns quality over time** *(model degrades — name an owner).*
- **Ground-truth source** *(where labeled data for ongoing eval comes from).*
- **Feedback loop:** thumbs up/down, drift detection, re-evaluation cadence, retraining trigger.

---

## B7. Appendix & Revision History
- **Research & references** *(Links, attachments.)*
- **Glossary** *(Domain terms.)*

| Version | Date | Author | Change |
|---|---|---|---|
| v0.1 | YYYY-MM-DD | | Initial draft |
