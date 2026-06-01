# User Flow & Customer Journey Map Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core**: Required fields for both flow and journey map. Always fill this.
> - **PART B — Extended**: Add for complex multi-role flows, service blueprints, or research-backed maps.
>
> **Key distinction**
> | | User Flow | Journey Map |
> |---|---|---|
> | **Scope** | One task in one product | Full customer lifecycle or phase |
> | **Timeframe** | Minutes–hours | Days–months–years |
> | **Emotions** | Minimal | Central |
> | **Audience** | Engineering, QA, Design | Leadership, cross-functional |
> | **Update cadence** | Per feature release | Quarterly |
>
> **Rules of thumb**
> - Map happy path first. Then 3–5 error paths. Then 2–3 edge cases per error. Never leave edge cases implicit.
> - Journey maps without research are hypotheses, not truth. Validate with 8+ user interviews before using for strategy.
> - 80% of improvement opportunities come from mapping pain points, not happy paths. Always include the churn scenario.
> - Delete this instruction block and italic *guiding prompts* once filled.

---

# PART A — CORE

## SECTION 1: USER FLOW

### 1.1 Flow Metadata

| Field | Value |
|---|---|
| **Flow ID** | *(e.g., FLOW-2024-Checkout-v2)* |
| **Title** | *(Action-oriented: "New user completes first team invite")* |
| **Owner** | |
| **Feature / Product area** | |
| **Persona(s)** | *(Whose perspective is this flow from?)* |
| **Status** | Proposed / Validated / In Design / Live |
| **Version** | v0.1 |
| **Last updated** | YYYY-MM-DD |
| **Links** | *(Figma, PRD, analytics, prior version)* |

---

### 1.2 Flow Objective

**User goal:** *(What is the user trying to accomplish?)*

**Business goal:** *(What does a successful completion mean for the business?)*

**Success criteria:** *(Observable behavior = task complete)*

**Assumptions** *(document upfront — validate later)*:
- *(e.g., "Assume user has already verified email")*
- *(e.g., "Assume user has permissions to invite")*

---

### 1.3 Happy Path

*The ideal, frictionless route. Every step must have: trigger → screen/state → user action → outcome.*

| Step | Trigger | Screen / State | User Action | Outcome |
|---|---|---|---|---|
| 1 | User lands on | | | |
| 2 | | | | |
| 3 | | | | |
| N | | | | → Task complete |

**Visual diagram:** *(Link to Figma wireflow)*

**Key annotations:**
- *(Data displayed at critical steps)*
- *(Validation rules)*
- *(Performance requirements — max load time, etc.)*

---

### 1.4 Error Paths

*Document 3–5 critical failure scenarios. Each must specify: trigger → error state → user message → recovery path.*

**Error Path 1: [Name — e.g., "Invalid email format"]**
- Trigger: *(What causes this error?)*
- User-facing message: *(Exact copy — specific, not "Invalid input")*
- Recovery: *(What can the user do? What does the system offer?)*

**Error Path 2: [Name]**
- Trigger:
- Message:
- Recovery:

**Error Path 3: [Name]**
- Trigger:
- Message:
- Recovery:

---

### 1.5 Edge Cases

*Unusual but valid scenarios. Every edge case must have an explicit expected behavior — no implicit assumptions.*

| Edge Case | Trigger | Expected Behavior | Design Response |
|---|---|---|---|
| Empty state | No data available | | |
| Timeout / slow network | API > 10s | | |
| Session expiry mid-flow | Token expires | | |
| Concurrent edits | Two users edit same record | | |
| Permission mismatch | User lacks required role | | |
| Very large dataset | 10,000+ results | | |
| Non-ASCII characters | Special chars in input | | |

**QA checklist before handoff:**
- [ ] Happy path mapped with annotations
- [ ] 3+ error paths documented
- [ ] 2+ edge cases per error documented
- [ ] Empty/zero states mapped
- [ ] Loading/wait states mapped
- [ ] Validation rules annotated
- [ ] Engineering reviewed and agreed on expected behavior

---

## SECTION 2: CUSTOMER JOURNEY MAP

### 2.1 Map Metadata

| Field | Value |
|---|---|
| **Map ID** | *(e.g., JM-2024-Onboarding-NewUser)* |
| **Title** | *(e.g., "New SMB Customer: Trial Signup → First Value → Conversion")* |
| **Owner** | |
| **Persona / Segment** | |
| **Journey scope** | Full lifecycle / Specific phase: *(e.g., "Onboarding only")* |
| **Confidence** | Generative (team assumptions) / Research-based (validated with N=___ interviews) |
| **Last validated** | YYYY-MM-DD |
| **Version** | v0.1 |
| **Links** | *(Research, analytics, Miro/Figma, prior version)* |

---

### 2.2 Journey Overview

*1–2 sentences: Who, what they're trying to do, over what timeframe, and whether this is the happy path or a variant.*

**Success looks like:** *(How does the customer measure a successful journey?)*

**Failure looks like:** *(What causes them to churn or abandon?)*

---

### 2.3 Core Journey Map (8-Row Standard)

*Build this in Figma or Miro — this table is the planning scaffold.*

#### Stages (6–8 max)

| Stage | Description | Entry signal | Exit signal |
|---|---|---|---|
| 1. Awareness | | | |
| 2. Consideration | | | |
| 3. Purchase / Signup | | | |
| 4. Onboarding | | | |
| 5. Active Use | | | |
| 6. Renewal / Advocacy | | | |

---

#### Actions Row (per stage)
*What does the customer actually DO at each stage?*

| Stage 1 | Stage 2 | Stage 3 | Stage 4 | Stage 5 | Stage 6 |
|---|---|---|---|---|---|
| | | | | | |

---

#### Touchpoints Row (per stage)
*Every way the customer interacts with you — digital and non-digital.*

| Stage | Touchpoint | Channel | Owner | Gap? |
|---|---|---|---|---|
| | | | | Yes / No |

---

#### Thoughts Row (per stage)
*What is the customer thinking? Use actual interview quotes where possible.*

| Stage | Customer Thoughts | Source (quote / research) |
|---|---|---|
| | | |

---

#### Feelings Row (per stage)
*Emotional state — specific, not generic ("nervous about ROI" not "worried").*

| Stage 1 | Stage 2 | Stage 3 | Stage 4 | Stage 5 | Stage 6 |
|---|---|---|---|---|---|
| | | | | | |

**Emotion arc:** *(Describe the emotional journey from first touchpoint to final stage — the highs and lows)*

---

#### Pain Points Row (per stage)
*Specific frictions and unmet needs. Must be grounded in research.*

| Stage | Pain Point | Evidence (source + N) | Severity |
|---|---|---|---|
| | | | High / Med / Low |

---

#### Opportunities Row (per stage)
*For each pain point: 2–3 concrete design/process improvements. Prioritized.*

| Pain Point | Opportunity | Impact | Effort | Priority |
|---|---|---|---|---|
| | | High/Med/Low | High/Med/Low | P1/P2/P3 |

---

#### Ownership Row (per stage)
*Who owns this stage? Reveals gaps and alignment needs.*

| Stage | Owner (Team) | Touchpoints Owned | Gap? |
|---|---|---|---|
| | | | |

---

### 2.4 Research Foundation

| Source | Finding | Participants / N | Date |
|---|---|---|---|
| User interviews | | | |
| Support ticket analysis | | | |
| Analytics (funnel data) | | | |
| NPS / CSAT data | | | |

**Confidence gaps** *(where we're still guessing)*:

---

# PART B — EXTENDED SECTIONS

## B1. Swimlane Diagram (Multi-Role Flows)

*Use when multiple actors own different steps. Add one row per actor.*

| Actor | Step 1 | Step 2 | Step 3 | Step 4 | Step 5 |
|---|---|---|---|---|---|
| Customer | | | | | |
| System / Automation | | | | | |
| Support Agent | | | | | |
| Internal Process | | | | | |

**Hand-off points** *(where responsibility transfers between actors)*:
- *(Step N → transition from Customer to Support → risk: no one owns the hand-off confirmation)*

*Limit to 3–5 actors. More than that = break into sub-flows.*

---

## B2. Service Blueprint Layer

*Add when the customer experience depends on internal coordination. Shows what's behind the scenes.*

```
CUSTOMER ACTIONS
        ↓
[LINE OF VISIBILITY — what customer sees vs. doesn't]
        ↓
EMPLOYEE ACTIONS & PROCESSES
        ↓
[LINE OF INTERNAL INTERACTION]
        ↓
SUPPORT SYSTEMS & TECHNOLOGY
```

**Cost insights this reveals:** *(Which stage is most expensive to support? Which has process bottlenecks?)*

---

## B3. Variant Journey Maps

*Create additional maps only when high-impact scenarios diverge significantly from the happy path.*

**Churn scenario map:**
- When: Customer churn rate > 5%
- Focus: At which stage do they drop off? What was the breaking point?
- Interview: 8–12 churned users specifically

**High-value scenario map:**
- When: Significant LTV gap between customer segments
- Focus: What made the best customers succeed? What journey did they take?

**Support-heavy scenario map:**
- When: > 20% of customers contact support in first 30 days
- Focus: Where in the journey do they hit walls requiring human support?

*Limit: 1 happy path + 1 churn scenario per product area. Three or more journey maps = analysis paralysis.*

---

## B4. Anti-Patterns

| Anti-Pattern | Impact | Fix |
|---|---|---|
| Flow with no error paths | QA confused about expected behavior; ships with gaps | Document 3+ error scenarios before handoff |
| Journey map without research | Maps what you think happens, not what actually happens | Validate with 8+ user interviews per segment |
| Too many stages (> 10) | Unreadable; loses focus | Break into sub-maps or limit to 6–8 core stages |
| No ownership row | Nobody feels responsible → nothing changes | Always identify stage owners; address gaps explicitly |
| Generic emotions ("frustrated") | No actionable insight | Use specific emotions from research with direct quotes |
| Opportunities without priority | Pretty artifact; not a strategy tool | Score every opportunity: impact × effort → P1/P2/P3 |
| Created once, never updated | Becomes "legacy research" in 6 months | Version it; update quarterly or after major product changes |
