# Product Analytics Plan (Tracking Plan) — Reusable Template

> **How to use this template**
> A tracking plan is the **single source of truth** for what user behavior you capture, why it matters, and exactly how each event is defined. It's shared across product, engineering, marketing, and data — so everyone instruments and analyzes consistently.
> - **PART A — Core**: fill in for every feature/product you instrument.
> - **PART B — Extended**: governance, identity, and lifecycle depth for scaling orgs.
>
> **The rule that prevents a mess: start from questions, not events.** Define the decisions and metrics you need to answer *first*, then derive only the events that serve them. Tracking everything "just in case" creates noise no one trusts.
>
> **Naming & convention rules (set once, never deviate)**
> - **Object-Action pattern:** `Object Action`, action in past tense — e.g., `Order Completed`, `Feature Activated`, `Signup Started`.
> - **Consistency beats the specific choice.** Pick one casing and tense and enforce it. **snake_case** (`order_completed`) is safest if data flows to a warehouse; Title Case is common in Mixpanel/Amplitude UIs.
> - **Properties** use the same casing as events; booleans start with `is_`/`has_`.
> - **Every event has an owner.** Untracked ownership = data rot.
> - **Living document.** Add events via the instrumentation process (B), not ad hoc. Review quarterly; archive dead events.
> - Fill the convention choices in §2, then follow them everywhere. Delete this block and italic *prompts* once written.

---

# PART A — CORE

## 1. Metadata

| Field | Value |
|---|---|
| **Product / feature** | |
| **Owner (data/PM)** | |
| **Analytics tool(s)** | *(Amplitude / Mixpanel / Segment / GA4 / warehouse)* |
| **Status** | Draft / In Review / Implemented |
| **Version** | v0.1 |
| **Last updated** | YYYY-MM-DD |

---

## 2. Conventions (decide these first)

- **Event naming pattern:** Object-Action, past tense *(e.g., `Project Created`)*.
- **Casing:** snake_case / Title Case / camelCase → **chosen:** ______
- **Property casing:** ______
- **Boolean prefix:** `is_` / `has_`
- **Reserved / standard properties** *(attached to every event):* `user_id`, `timestamp`, `platform`, `app_version`, …

---

## 3. Goals — What questions must this answer?

*List the decisions/metrics first. Each event below should trace to one of these.*

| # | Question / metric we need | Why it matters | Events that serve it |
|---|---|---|---|
| 1 | *(e.g., What's our activation rate?)* | | |
| 2 | | | |

- **North Star / key metric this supports:** …

---

## 4. Key Funnels & User Journeys

*The flows you'll analyze. Helps ensure events cover each step.*

- **Funnel 1:** step → step → step *(e.g., Visit → Signup Started → Signup Completed → Activated)*
- **Funnel 2:** …

---

## 5. Event Dictionary

*The core of the plan. One row per event. Keep events to what answers §3.*

| Event name | Trigger (when it fires) | Properties (name : type : req?) | Serves question # | Owner | Platform(s) |
|---|---|---|---|---|---|
| `Signup Completed` | User finishes signup | `method:string:req`, `referrer:string:opt` | 1 | | Web/iOS/Android |
| | | | | | |
| | | | | | |

*Data types: string, number, boolean, datetime, array, object. Mark each required (req) or optional (opt).*

---

## 6. Event Detail (for complex/critical events)

*Expand the few events that need it. Repeat per event.*

### Event: `[Event Name]`
- **Description / when it fires:** …
- **Do NOT fire when:** *(disambiguate from similar events.)*
- **Properties:**

| Property | Type | Required | Description | Example |
|---|---|---|---|---|
| | | | | |

- **Sample payload:**
```json
{ "event": "order_completed", "order_id": "A123", "total_amount": 49.0, "currency": "USD" }
```

---

## 7. User & Account Properties (traits)

*Attributes about the user/account (not events) — set on identify.*

| Property | Type | Description | Example | PII? |
|---|---|---|---|---|
| `plan_tier` | string | Subscription tier | "pro" | No |
| | | | | |

---

## 8. Ownership & Open Questions

| # | Item / question | Owner | Status |
|---|---|---|---|
| 1 | | | Open |

---

# PART B — EXTENDED SECTIONS
*(Add as the org and data stack mature.)*

## B1. Instrumentation & QA Process
*How new events get added and verified — the discipline that keeps data trustworthy.*
- Request/approval flow for new events *(who reviews against this plan).*
- Implementation: client vs. server-side; SDK; where the call lives.
- **Validation/QA:** how events are tested before release *(debugger, staging, payload checks).*
- Definition of done for instrumentation.

## B2. Identity & Session Model
- How users are identified (anonymous → logged-in stitching).
- `user_id` vs. `anonymous_id`; account/group association.
- Session definition.

## B3. Data Governance
- Naming/taxonomy enforcement *(Amplitude Govern, Mixpanel Lexicon, Avo, etc.).*
- Event lifecycle: proposed → live → deprecated → archived.
- Versioning & change log for the schema.
- Review cadence and owner.

## B4. Privacy & Compliance
- PII handling: what's collected, masked, or excluded.
- Consent management (GDPR/CCPA), opt-out behavior, data retention.
- Region/data-residency notes.

## B5. Destinations & Data Flow
- Where data is sent (warehouse, BI, marketing tools) and how it maps.
- Diagram or description of the pipeline.

## B6. Appendix & History
- Glossary of metrics & terms.
- Source/reference links.

| Version | Date | Author | Change |
|---|---|---|---|
| v0.1 | YYYY-MM-DD | | Initial draft |
