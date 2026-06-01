# PM Template Library — Usage Guide

A complete toolkit for product managers. 16 templates covering the full PM lifecycle — from discovery to execution to communication.

Use the decision tree below to find the right template for any situation.

---

## Quick Decision Tree

```
WHAT ARE YOU TRYING TO DO?

├── Understand users or a problem?
│   ├── Talk to users → Discovery-Interview-Template.md
│   └── Map the competitive landscape → Competitive-Analysis-Template.md
│
├── Define what to build?
│   ├── Write a full feature spec → PRD-Template.md
│   └── Decide which features to build first → Feature-Prioritization-Template.md
│
├── Plan work with your team?
│   ├── Write a story for engineering → User-Story-Template.md
│   ├── Plan the upcoming sprint → Sprint-Planning-Template.md
│   └── Plan the quarter / year → Product-Roadmap-Template.md
│
├── Measure and experiment?
│   ├── Run an A/B test → AB-Test-Plan-Template.md
│   ├── Define OKRs and KPIs → OKRs-and-KPIs-Template.md
│   └── Track product analytics → Product-Analytics-Tracking-Plan-Template.md
│
├── Communicate and align?
│   ├── Update leadership / stakeholders → Stakeholder-Update-Template.md
│   ├── Justify a large investment → Business-Case-Template.md
│   └── After an incident → Post-Mortem-Template.md
│
└── Think strategically?
    ├── Define product vision → Product-Strategy-and-Vision-Template.md
    ├── Plan a product launch → Go-To-Market-Strategy-Template.md
    └── Understand your target users → Persona-Profiles-Template.md
```

---

## Full Template Map

### Stage 1 — Discover

> *Before writing a single requirement, understand the problem and the users.*

---

#### [Discovery-Interview-Template.md](./Discovery-Interview-Template.md)
**What it is:** A structured framework for running user research interviews — from screener criteria to synthesis.

**When to use:**
- Before writing a PRD or feature spec
- When validating or invalidating a problem assumption
- When you don't understand WHY users churn, drop off, or don't adopt a feature
- Weekly, as part of continuous discovery (minimum 1 interview/week)

**What it gives you:**
- Interview flow (opening → problem exploration → current solutions → decision factors → close)
- Note-taking structure that separates facts from opinions
- Question types: open-ended, probing, clarifying — with examples
- The Mom Test principles (avoid leading questions)
- JTBD framing (jobs-to-be-done)
- Synthesis method (affinity mapping, insight board)
- Saturation guide: when you've interviewed enough

**Key insight:** People lie about future behavior but can't lie about past behavior. This template forces past-behavior questions.

---

#### [Persona-Profiles-Template.md](./Persona-Profiles-Template.md)
**What it is:** A structured format for defining the users your product serves.

**When to use:**
- At the start of a new product area or feature initiative
- When the team has conflicting assumptions about "who the user is"
- Before writing a PRD or GTM strategy

**What it gives you:**
- Demographics, goals, pain points, and behavior patterns per persona
- Jobs-to-be-done framing per segment
- Prioritization of which persona to serve first

---

#### [Competitive-Analysis-Template.md](./Competitive-Analysis-Template.md)
**What it is:** A framework for mapping the competitive landscape and identifying differentiation opportunities.

**When to use:**
- Entering a new market or segment
- Before a product strategy review
- When positioning a new feature against alternatives users already have

**What it gives you:**
- Feature-by-feature comparison matrix
- Competitor positioning and strategy analysis
- Gap map: what you can own that others don't

---

### Stage 2 — Define

> *Translate discoveries into clear, prioritized, buildable requirements.*

---

#### [PRD-Template.md](./PRD-Template.md)
**What it is:** The definitive product requirements document. The north star for a feature from kickoff to launch.

**When to use:**
- Any time you're building something non-trivial (>1 sprint of work)
- When multiple teams need alignment on scope, goals, and success metrics
- As the single source of truth through planning, build, and launch

**What it gives you:**
- Problem statement, goals, success metrics, non-goals
- User scenarios, requirements table (P0/P1/P2), solution & UX
- Release plan, risk table, open questions tracker
- Extended sections for AI/ML, compliance, GTM, technical architecture

**Stage map:** Fill in passes — don't try to complete it all upfront. Problem + Goals first. Requirements + Solution during kickoff. Release plan pre-ship.

---

#### [Feature-Prioritization-Template.md](./Feature-Prioritization-Template.md)
**What it is:** A scoring framework for deciding which features to build, in what order, with what rationale.

**When to use:**
- Quarterly backlog grooming
- Before sprint planning when the backlog has more items than capacity
- When stakeholders are pushing competing priorities
- To bring data to a "gut feel" debate about what to build

**What it gives you:**
- RICE scoring (Reach × Impact × Confidence / Effort) — the default
- ICE scoring (for fast-moving startup environments)
- MoSCoW categorization (for fixed-deadline launches)
- Weighted scoring matrix (for multi-stakeholder alignment)
- Decision gates checklist
- Red flags that should block prioritization even if score is high
- Post-build retrospective to calibrate future estimates

**Key formulas:**
```
RICE = (Reach × Impact × Confidence) / Effort
ICE  = Impact × Confidence × Ease
```

---

### Stage 3 — Deliver

> *Plan and execute the work with engineering, design, and QA.*

---

#### [User-Story-Template.md](./User-Story-Template.md)
**What it is:** A reusable format for writing user stories that are ready for engineering — with acceptance criteria, edge cases, and a definition of done.

**When to use:**
- Every time you hand off a feature to engineering
- During sprint refinement (the sprint before planning)
- When a story comes back from QA because requirements were unclear

**What it gives you:**
- Story format: "As a [user], I want [action], so that [outcome]"
- BDD acceptance criteria (Given / When / Then)
- INVEST checklist (Independent, Negotiable, Valuable, Estimable, Small, Testable)
- Edge cases and error scenarios section
- Definition of Done checklist
- Variant templates: UI story / API story / backend processing story
- Story-splitting guide (when a story is too large)

**Rule:** If a story has no acceptance criteria, it's not ready for a sprint. Full stop.

---

#### [Sprint-Planning-Template.md](./Sprint-Planning-Template.md)
**What it is:** A complete sprint planning document — from goals and capacity to committed stories, risks, and retrospective links.

**When to use:**
- At the start of every sprint
- When planning a particularly complex sprint (many dependencies, new team members, high-risk work)
- When sprint quality is inconsistent and the team needs more structure

**What it gives you:**
- Sprint goals (outcome-based, not task-based)
- Capacity planning with team availability table
- Committed stories table with points and owners
- Risk and dependency tables
- Definition of Done checklist
- Kickoff agenda (2–3 hour meeting structure)
- Mid-sprint check-in format
- Scope change protocol (add = remove)
- Sprint anti-patterns and how to fix them

**Key rule:** Goals are outcomes. "Reduce checkout abandonment by 5%" is a goal. "Build dropdown component" is a task. Never confuse the two.

---

#### [Product-Roadmap-Template.md](./Product-Roadmap-Template.md)
**What it is:** A structured format for planning and communicating the product roadmap across quarters.

**When to use:**
- Quarterly planning
- When communicating strategy to leadership, sales, or customers
- When the team needs a shared view of what's coming and why

**What it gives you:**
- Themes-based and timeline-based roadmap formats
- Prioritization criteria and trade-off documentation
- Communication-ready views per audience (exec, engineering, customers)

---

### Stage 4 — Measure

> *Run experiments, track results, and know if what you built worked.*

---

#### [AB-Test-Plan-Template.md](./AB-Test-Plan-Template.md)
**What it is:** A rigorous, stats-correct A/B testing plan — from hypothesis to results to launch decision.

**When to use:**
- Before changing a high-traffic UI element, pricing page, onboarding flow, or checkout
- When you need data to justify a product decision (not just intuition)
- When the team is debating two design or copy directions

**What it gives you:**
- Hypothesis format (If… then… because…)
- Variant definition (control vs. treatment, exact specification)
- Primary metric + guardrail metrics (with alert thresholds)
- Sample size calculation and duration planning
- Pre-launch QA checklist
- Decision table (when to ship, when not to, when to investigate)
- Novelty effect analysis (Day 1–3 vs. Day 8–14)
- Pre-mortem (what could go wrong before it does)
- Common pitfalls: peeking, multiple comparisons, survivorship bias, Simpson's Paradox

**Key formulas:**
```
Relative Lift     = (Treatment − Control) / Control × 100%
Minimum duration  = MAX(days to reach sample, 7 days, 14 days)
Bonferroni        = α / number of segments or metrics
```

**Non-negotiable:** Lock hypothesis, metrics, and duration BEFORE launching. Defining them after seeing results invalidates everything.

---

#### [OKRs-and-KPIs-Template.md](./OKRs-and-KPIs-Template.md)
**What it is:** A framework for setting measurable objectives and tracking key results and performance indicators.

**When to use:**
- Quarterly goal-setting
- When aligning product goals with company strategy
- When the team doesn't have a shared definition of success

**What it gives you:**
- OKR structure (Objective + Key Results)
- KPI definition with baseline, target, and ownership
- Leading vs. lagging indicator framework

---

#### [Product-Analytics-Tracking-Plan-Template.md](./Product-Analytics-Tracking-Plan-Template.md)
**What it is:** A specification for what events to track, how to name them, and what properties to capture.

**When to use:**
- Before launching a new feature (not after — instrument before you ship)
- When analytics data is inconsistent or teams disagree on definitions
- When setting up a new analytics pipeline or tool

**What it gives you:**
- Event taxonomy (naming conventions)
- Event schema (event name, trigger, properties, owner)
- Funnel definition for feature adoption
- Data quality checklist

---

### Stage 5 — Communicate

> *Update stakeholders, justify investments, and learn from failures.*

---

#### [Stakeholder-Update-Template.md](./Stakeholder-Update-Template.md)
**What it is:** A structured format for weekly and monthly stakeholder communications — from direct manager to board level.

**When to use:**
- Weekly: update your manager and immediate stakeholders
- Monthly: update leadership and cross-functional partners
- Immediately: when any RAG status changes to Amber or Red (don't wait for the monthly review)

**What it gives you:**
- RAG status across 6 dimensions (Timeline / Budget / Scope / Quality / Dependencies / Team)
- Key metrics table with trend and "why it matters" column
- Accomplishments and upcoming priorities in outcome-first format
- Risk and mitigation table
- Decision ask format (options, recommendation, deadline, owner)
- SBAR format for escalation scenarios
- Audience calibration guide (manager vs. VP vs. board)

**Key principle:** Structure for skimmers. Assume your executive will spend 2 minutes. First 30 seconds = full status picture.

---

#### [Business-Case-Template.md](./Business-Case-Template.md)
**What it is:** A financial and strategic justification document for major investments — built to survive CFO scrutiny.

**When to use:**
- When requesting > $100K in budget or headcount
- When proposing a new product line, market entry, or platform investment
- When leadership needs to choose between 2–3 competing initiatives
- Board presentations for strategic bets

**What it gives you:**
- Executive summary (1-page version for fast reads)
- Problem statement in dollar terms
- Market sizing (TAM / SAM / SOM) with bottom-up methodology
- 3–4 solution options with decision matrix
- 5-year financial model: revenue projections, cost structure, cost-benefit table
- NPV, IRR, payback period, ROI formulas and examples
- Sensitivity analysis (pessimistic / base / optimistic)
- Risk matrix with probability × impact scoring
- Kill criteria definition
- Common mistakes section (what gets business cases rejected)

**Key formulas:**
```
NPV     = Σ [CFt / (1+r)^t] − Initial Investment
IRR     = Discount rate where NPV = 0
Payback = Investment / Annual Cash Flow
ROI     = (Gain − Cost) / Cost × 100%
LTV     = (ARPU × Gross Margin) / Churn Rate
```

---

#### [Post-Mortem-Template.md](./Post-Mortem-Template.md)
**What it is:** A blameless incident retrospective template — for production outages, major bugs, and failed launches.

**When to use:**
- Within 24–48 hours of any SEV-1 or SEV-2 incident
- After a failed launch (product or feature)
- Anytime a critical bug reaches production and affects users
- Quarterly, to review patterns across incidents (Part B)

**What it gives you:**
- Incident metadata and severity classification
- Timeline reconstruction (with event types, sources, detection gaps)
- Root cause analysis using 5-Why method
- Contributing factors framework (why it wasn't caught, not just what went wrong)
- Customer and business impact quantification
- Action item format: P0 / P1 / P2 / P3 with owner + deadline + success criteria
- Blameless culture checklist
- Launch retrospective variant (for feature-related incidents)
- Quarterly pattern analysis table
- 30-day follow-up format (verify prevention measures worked)

**Key principle:** The root cause is never a person. It's a process, system, or monitoring gap. "The developer missed a bug" → "The deploy process had no automated test for this case."

---

### Stage 6 — Strategy

> *Set direction, define positioning, and plan go-to-market.*

---

#### [Product-Strategy-and-Vision-Template.md](./Product-Strategy-and-Vision-Template.md)
**What it is:** A framework for articulating long-term product direction, positioning, and strategic bets.

**When to use:**
- Annual or semi-annual strategy planning
- When onboarding new leadership or team members
- When the team has lost alignment on "where we're going"

**What it gives you:**
- Vision statement, mission, and north star metric
- Strategic bets (what you're betting on and why)
- Positioning and differentiation
- Resource allocation guidance

---

#### [Go-To-Market-Strategy-Template.md](./Go-To-Market-Strategy-Template.md)
**What it is:** A launch plan covering positioning, ICP, channels, pricing, enablement, and success metrics.

**When to use:**
- Before any major feature launch or new product release
- When entering a new market or customer segment
- When aligning sales, marketing, and product on launch timing and messaging

**What it gives you:**
- ICP (Ideal Customer Profile) definition
- Positioning statement and messaging framework
- Channel strategy and launch phases
- Pricing and packaging considerations
- Sales enablement and support readiness checklist
- Launch success metrics and post-launch review cadence

---

## Template Dependencies

Some templates work best in sequence:

```
Discovery-Interview → Persona-Profiles → PRD → Feature-Prioritization
                                              ↓
                                         User-Story → Sprint-Planning
                                              ↓
                               AB-Test-Plan ← Product-Analytics-Tracking-Plan
                                              ↓
                                    Stakeholder-Update (ongoing)

Business-Case → PRD → Go-To-Market-Strategy

Post-Mortem → OKRs-and-KPIs (update based on learnings)
```

---

## Cheat Sheet: Template by Situation

| Situation | Template |
|---|---|
| "I need to talk to users before we build this" | Discovery-Interview-Template.md |
| "I need to write the spec for engineering" | PRD-Template.md |
| "We have 20 backlog items and need to pick 5" | Feature-Prioritization-Template.md |
| "Engineering needs a story to estimate" | User-Story-Template.md |
| "Sprint starts Monday — need to plan" | Sprint-Planning-Template.md |
| "We want to test two versions of the checkout" | AB-Test-Plan-Template.md |
| "My VP wants a weekly update" | Stakeholder-Update-Template.md |
| "We need $2M to build this — how do I justify it?" | Business-Case-Template.md |
| "Production went down last night" | Post-Mortem-Template.md |
| "What should we build for the next 12 months?" | Product-Roadmap-Template.md + Product-Strategy-and-Vision-Template.md |
| "We're launching next month — are we ready?" | Go-To-Market-Strategy-Template.md |
| "What are our goals this quarter?" | OKRs-and-KPIs-Template.md |
| "Are we tracking the right things?" | Product-Analytics-Tracking-Plan-Template.md |
| "Who are we building this for?" | Persona-Profiles-Template.md |
| "What are competitors doing?" | Competitive-Analysis-Template.md |

---

## How These Templates Were Built

Every template in this library follows the same principles:

1. **Two-tier structure** — Part A (core, always fill) + Part B (extended, add when needed). Use Part A for speed; add Part B for rigor.
2. **Outcome-first** — Sections are ordered by decision-making value, not completeness.
3. **No-fluff fields** — Every field exists because removing it would cause a specific failure mode.
4. **Guiding prompts** — Italic *prompts* show what good looks like. Delete them once the doc is written.
5. **Real formulas and examples** — Not "insert metric here" but `RICE = (R × I × C) / E` with a worked example.
