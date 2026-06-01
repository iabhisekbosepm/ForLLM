# UX/UI Template Library — Usage Guide

A complete toolkit for UX designers, product designers, and design leads. 10 templates covering the full design lifecycle — from research through delivery, including a dedicated template for AI/ML feature UX.

Use the decision tree below to find the right template for any situation.

---

## Quick Decision Tree

```
WHAT ARE YOU TRYING TO DO?

├── Plan or conduct research?
│   ├── Plan a research study → UX-Research-Plan-Template.md
│   └── Run a usability test → Usability-Testing-Template.md
│
├── Define the design problem?
│   └── Write a design brief → Design-Brief-Template.md
│
├── Map flows and experiences?
│   ├── Map screen-to-screen navigation → User-Flow-and-Journey-Map-Template.md (User Flow section)
│   └── Map end-to-end customer experience → User-Flow-and-Journey-Map-Template.md (Journey Map section)
│
├── Evaluate existing design?
│   ├── Quick expert review against principles → Heuristic-Evaluation-Template.md
│   └── Check for accessibility violations → Accessibility-Audit-Template.md
│
├── Design or document components?
│   ├── Spec a design system component → Design-System-Component-Spec-Template.md
│   └── Plan content structure / navigation → Information-Architecture-Template.md
│
├── Hand off to engineering?
│   └── Package specs for developers → Design-Handoff-Template.md
│
└── Design an AI/ML feature?
    └── AI loading states, errors, trust, feedback loops → AI-ML-UX-Design-Template.md
```

---

## Full Template Map

### Phase 1 — Understand

> *Before designing anything, understand the users, the problem, and the context.*

---

#### [UX-Research-Plan-Template.md](./UX-Research-Plan-Template.md)
**What it is:** A structured plan for any UX research initiative — from research questions through methodology, participant criteria, and synthesis.

**When to use:**
- Before starting any significant design project
- When validating or invalidating a product assumption
- When you need to understand *why* users behave a certain way
- Before writing a design brief or PRD
- As the foundation for continuous discovery (minimum 1 study per quarter)

**What it gives you:**
- Problem statement + "So What?" test (forces you to define what decision the research informs)
- Research objectives (primary + secondary, mapped to decision thresholds)
- Methodology selection guide — when to use interviews vs. usability tests vs. surveys
- Participant criteria table with diversity requirements
- Screener design (5–8 questions to find the right participants without biasing them)
- Pre-defined success thresholds ("If 6 of 8 users fail, we redesign")
- Ethics and data handling framework
- Extended methodology protocols: contextual inquiry, diary studies, card sorting, surveys

**Key insight:** The "So What?" test is the most important field. If you can't answer "What product decision changes based on this research?", the study isn't ready.

---

#### [Usability-Testing-Template.md](./Usability-Testing-Template.md)
**What it is:** A complete plan for running moderated or unmoderated usability tests — from test objectives through synthesis and reporting.

**When to use:**
- Before launching any significant new feature or redesign
- After a heuristic evaluation (to validate expert findings with real users)
- When analytics show a drop-off but don't explain why
- Every sprint for rapid iteration (unmoderated, 5 users, 3 days)

**What it gives you:**
- Task scenario format (realistic, open-ended — never mentioning UI elements)
- Severity rating scale (Critical / Major / Minor / Cosmetic) with escalation rules
- Session-by-session observation guide
- Metrics: task success rate, time-on-task, error rate, SUS score (System Usability Scale)
- SUS benchmarks: 80+ = Excellent, 68 = Industry average, < 50 = Major issues
- Synthesis process: affinity mapping → priority matrix → actionable recommendations
- Full test report structure
- Remote testing setup checklist

**Nielsen's law:** 5 users find 85% of usability issues. Run multiple rounds of 5 — not one round of 20.

---

### Phase 2 — Define

> *Translate research into a clear, constrained design direction.*

---

#### [Design-Brief-Template.md](./Design-Brief-Template.md)
**What it is:** A concise, actionable document that provides design direction and constraints before design begins.

**When to use:**
- At the start of every design initiative (before wireframes)
- When multiple teams need alignment on what's being designed and why
- When stakeholders have conflicting goals — the brief forces explicit resolution
- As the companion to a PRD (PRD covers requirements; brief covers design direction)

**What it gives you:**
- Problem statement grounded in data (not "improve UX" — "28% abandonment at step 3 = $2M/year")
- Business goals vs. user goals alignment table (with explicit conflict resolution)
- Constraints: technical, brand, accessibility, timeline, scope
- Accessibility built in from §1 — not bolted on at QA
- Success criteria that are measurable and testable
- Project-specific design principles (not generic — each one resolves a tradeoff)
- Stakeholder map with approval rights and alignment checkpoints

**Brief vs. PRD:** The design brief tells designers *how to approach* the problem. The PRD tells engineers *what to build*. Both reference each other.

---

#### [Information-Architecture-Template.md](./Information-Architecture-Template.md)
**What it is:** A framework for planning and documenting how content is organized, labeled, and navigated.

**When to use:**
- Launching a new product section or feature set
- When task completion rates are < 60% (users can't find things)
- When content has grown significantly (> 40% new content)
- Before designing any navigation pattern
- When the team disagrees about "where things should live"

**What it gives you:**
- Site map structure with primary, secondary, and utility navigation
- Taxonomy and labeling system (user vocabulary vs. internal vocabulary)
- Wayfinding strategy (breadcrumbs, active states, page titles)
- Search design specs (scope, autocomplete, filters, no-results handling)
- IA decisions log (why you made each structural choice)
- Card sort methodology (open for discovery, closed for validation)
- Tree testing framework (validate before building)
- SEO-IA alignment guide (category labels = search intent keywords)
- Common IA failures and remedies

**IA rule:** Organize by user goal, not org chart. "Run Campaigns" beats "Marketing Campaigns."

---

### Phase 3 — Design

> *Map the experience and design the components.*

---

#### [User-Flow-and-Journey-Map-Template.md](./User-Flow-and-Journey-Map-Template.md)
**What it is:** Two complementary tools in one template — user flows (screen-to-screen) and customer journey maps (end-to-end experience).

**When to use user flows:**
- Before handing any feature to engineering
- When multiple teams need to agree on edge cases and error states
- For QA test coverage planning
- For API/backend design (what states does the system need to handle?)

**When to use journey maps:**
- For strategy and stakeholder alignment (make pain points visible to decision-makers)
- When churn > 5% and you don't know where/why users are leaving
- For cross-functional alignment (reveals who owns what — and who owns nothing)
- Quarterly, as a living document tied to product strategy

**What it gives you:**
- User flow: happy path + 3–5 error paths + edge case inventory (never leave these implicit)
- QA handoff checklist (every edge case must have documented expected behavior)
- Swimlane diagram format (multi-role flows with hand-off points)
- Journey map: 8-row standard (stages, touchpoints, actions, thoughts, feelings, pain points, opportunities, ownership)
- Service blueprint layer (behind-the-scenes processes that affect customer experience)
- Research requirements (how many interviews needed to validate each map)

**Key distinction:** User flows tell engineering what to build. Journey maps tell leadership where to invest.

---

#### [Design-System-Component-Spec-Template.md](./Design-System-Component-Spec-Template.md)
**What it is:** The single source of truth for a design system component — covering anatomy, states, props, accessibility, tokens, and implementation.

**When to use:**
- When adding a new component to the design system
- When documenting an existing component for engineering
- When a component has inconsistent implementations across products
- Before any major component update (version the spec first)

**What it gives you:**
- Anatomy diagram with labeled parts (optional vs. required, with token references)
- Complete state matrix: Default × Hover × Focus × Active × Disabled × Loading × Error — for EVERY variant
- Props table with TypeScript types, defaults, and constraint rules
- ARIA attributes table and keyboard navigation matrix
- Color contrast requirements per state
- Touch target size specs (44×44px minimum)
- Design tokens map (every property → token → value)
- Responsive breakpoint behavior table
- Changelog with migration guides

**Rule:** Never document "the component has a hover state." Document: background → token, duration → 150ms, easing → ease-out, affected properties.

---

### Phase 4 — Evaluate

> *Find problems before they ship.*

---

#### [Heuristic-Evaluation-Template.md](./Heuristic-Evaluation-Template.md)
**What it is:** A structured expert review of a product against Nielsen's 10 usability heuristics — the fastest and cheapest way to find design problems.

**When to use:**
- Before investing in user testing (fix obvious issues first)
- At the end of a design phase (before handoff)
- For continuous product quality audits
- When budget/timeline doesn't allow full user testing
- As a complement to usability testing (not a replacement)

**What it gives you:**
- All 10 heuristics with one-line test questions
- Severity rating scale (0–4) with real examples per heuristic
- Independent evaluation protocol (evaluators work alone before consolidation)
- Optimal evaluator composition (UX specialist + domain expert + user proxy + external)
- Deduplication process (consolidate 80 raw issues → 25–40 unique issues)
- Heuristic hit list (which heuristics have the most violations = systemic design gaps)
- Remediation roadmap template (P0/P1/P2/P3 with owners and timelines)

**Evaluator sweet spot:** 3–5 evaluators find 85–95% of issues. The mix matters more than the number.

---

#### [Accessibility-Audit-Template.md](./Accessibility-Audit-Template.md)
**What it is:** A comprehensive WCAG 2.1 AA audit framework — covering automated scanning, keyboard testing, screen reader testing, and visual assessment.

**When to use:**
- Before any product launch or major release
- After any significant redesign
- Quarterly as part of ongoing quality maintenance
- When a legal or compliance requirement mandates WCAG conformance
- When adding new components or interaction patterns

**What it gives you:**
- Full WCAG 2.1 AA compliance matrix (Perceivable, Operable, Understandable, Robust)
- Color contrast audit table (text, links, buttons, focus indicators — all states)
- Keyboard navigation test matrix (every interactive component)
- Screen reader testing log (NVDA + VoiceOver, expected vs. actual announcements)
- ARIA implementation review (correct usage vs. anti-patterns)
- Touch target size audit (44×44px minimum)
- Form accessibility audit (labels, errors, required fields)
- Motion & animation audit (prefers-reduced-motion testing)
- Severity classification (4 = launch blocker, 3 = fix within 1 week)
- Remediation roadmap

**Automated tools detect only ~35% of issues.** Always follow automated scans with manual keyboard and screen reader testing.

---

### Phase 5 — Deliver

> *Hand off to engineering with zero ambiguity.*

---

#### [Design-Handoff-Template.md](./Design-Handoff-Template.md)
**What it is:** A comprehensive design-to-development handoff package — covering all specs, assets, interactions, and accessibility requirements.

**When to use:**
- Before any feature moves from design to engineering
- When a previous handoff caused rework, bugs, or missed states
- For new team members who haven't seen the design before
- As the source of truth for QA acceptance criteria

**What it gives you:**
- Full design specifications: colors, typography, spacing, shadows, border radius — all from design tokens
- Component and state inventory (every component × every state — nothing implicit)
- Responsive breakpoint table with specific changes per breakpoint
- Interaction specification: trigger → visual change → duration → easing → reduced motion handling
- Asset export specs: icons (SVG + PNG), images (WebP + fallback), naming conventions, file size targets
- Accessibility handoff notes (aria-label requirements, contrast table, focus order)
- Pre-handoff designer sign-off checklist
- QA acceptance criteria (designer reviews engineering's implementation against this)

**The 70% rule:** 70% of project delays happen at handoff. This template prevents all the common failures: missing states, unclear interactions, no error states, wrong asset formats.

---

### Special — AI/ML Features

> *AI features need different UX patterns. Standard templates don't cover them.*

---

#### [AI-ML-UX-Design-Template.md](./AI-ML-UX-Design-Template.md)
**What it is:** A comprehensive UX design framework specifically for AI/ML features — covering loading states, error handling, transparency, trust calibration, feedback loops, and AI-type-specific patterns.

**When to use:**
- Designing any feature that uses AI/ML (generative text, classification, recommendations, search augmentation, agents)
- When adding AI capabilities to an existing product
- As a companion to the PRD's B6 (AI/ML) section — PRD covers technical; this covers UX
- For onboarding, conversational UI, or multi-turn interaction flows

**What it gives you:**
- AI capability & confidence model (define what the AI can and can't do before designing UI)
- Loading states for different latency windows (0ms → instant; 1–3s → skeleton; 3s+ → cancel option)
- Progressive streaming text patterns (render incrementally, don't wait for full response)
- Error handling per failure mode: hallucination, low confidence, no result, timeout, safety filter
- AI vs. human content attribution (badges, disclosure, citation formats)
- Trust calibration design (prevent over-trust AND under-trust)
- User feedback loop (thumbs up/down, corrections, regenerate)
- Empty states for AI features (cold start, no results, first use)
- Prompt input design (placeholder, token limits, accessibility)
- Patterns by AI type: generative text, classification, recommendations, RAG, agents
- Agentic AI UX (pre-action preview, approval gates, audit log, rollback)
- Anti-patterns with fixes (10 common AI UX mistakes)
- AI UX metrics (adoption, correction rate, acceptance rate, latency)

**Key principle:** Every AI feature must have a fallback. If the AI fails, users must have a manual path. No feature should be blocked by AI unavailability.

---

## Template Dependencies & Workflow

These templates work best in sequence:

```
UX-Research-Plan → Usability-Testing → Design-Brief
                                              ↓
              Information-Architecture → User-Flow-and-Journey-Map
                                              ↓
                       Design-System-Component-Spec → Design-Handoff
                                              ↓
                  Heuristic-Evaluation ← Accessibility-Audit
                                              ↑
                              AI-ML-UX-Design (if AI feature)
```

**Standard feature flow:**
1. `UX-Research-Plan` → understand the problem
2. `Design-Brief` → define the design direction
3. `User-Flow-and-Journey-Map` → map the experience
4. `Heuristic-Evaluation` → find issues before user testing
5. `Usability-Testing` → validate with real users
6. `Design-System-Component-Spec` → spec the components
7. `Accessibility-Audit` → verify compliance
8. `Design-Handoff` → ship to engineering

---

## Cheat Sheet: Template by Situation

| Situation | Template |
|---|---|
| "I need to understand why users are dropping off" | UX-Research-Plan-Template.md |
| "I need to run a usability test before we launch" | Usability-Testing-Template.md |
| "The team disagrees on what we're designing" | Design-Brief-Template.md |
| "We need to reorganize the navigation" | Information-Architecture-Template.md |
| "Engineering needs every screen state documented" | User-Flow-and-Journey-Map-Template.md (User Flow) |
| "Leadership needs to understand the customer experience" | User-Flow-and-Journey-Map-Template.md (Journey Map) |
| "I want to find design problems quickly without users" | Heuristic-Evaluation-Template.md |
| "We need to check accessibility before launch" | Accessibility-Audit-Template.md |
| "We're adding a new component to our design system" | Design-System-Component-Spec-Template.md |
| "Design is done — ready to hand off to engineering" | Design-Handoff-Template.md |
| "We're adding AI/ML to a feature" | AI-ML-UX-Design-Template.md |
| "AI feature shows loading states / errors / confidence" | AI-ML-UX-Design-Template.md |
| "We need to design a chatbot or conversational UI" | AI-ML-UX-Design-Template.md (Part B) |
| "We're designing an agent that takes actions" | AI-ML-UX-Design-Template.md (Part B5) |

---

## How These Templates Were Built

Every template in this library follows the same principles:

1. **Two-tier structure** — Part A (core, always fill) + Part B (extended, add when needed)
2. **Research-backed** — grounded in best practices from Nielsen Norman Group, Google, Apple, Airbnb, OpenAI, Anthropic, and industry standards (WCAG 2.1, Nielsen's 10 Heuristics)
3. **Decision-first** — every template starts with "what decision does this inform?"
4. **Anti-pattern sections** — each template documents what NOT to do
5. **AI-inclusive** — AI/ML UX has its own dedicated template covering patterns that generic templates miss
6. **Guiding prompts** — italic *prompts* show what good looks like; delete them once written
