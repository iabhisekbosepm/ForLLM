# Stakeholder Update Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Update**: The essential sections for every weekly or monthly stakeholder update.
> - **PART B — Extended Sections**: Add for monthly executive reviews, escalation scenarios, or multi-project reporting.
>
> **Rules of thumb**
> - Lead with status, not narrative. Executives skim; structure for 2-minute reads.
> - Every metric needs a "why it matters" layer. "Velocity: 47 SP" is useless without context.
> - Escalate Amber/Red status the week it becomes Amber/Red — not at the monthly review.
> - Every decision ask needs a deadline and an owner. Vague asks get ignored.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **Audience calibration**
> | Audience | Depth | Focus |
> |---|---|---|
> | Direct manager | Full depth | Risks, decisions, dependencies |
> | Skip-level / VP | Medium | Strategic implications, escalations |
> | Executive / Board | Light | Business impact, top risks, asks only |

---

# PART A — CORE UPDATE
*(Always fill this in.)*

## 1. Update Metadata

| Field | Value |
|---|---|
| **Project / Product** | |
| **Period** | Week of YYYY-MM-DD / Month of YYYY-MM |
| **Author** | |
| **Audience** | *(Direct manager / VP / Exec team / Board)* |
| **Date sent** | YYYY-MM-DD |
| **Links** | *(Dashboard, roadmap, Jira/Linear board, previous update)* |

---

## 2. Executive Summary

*2–3 sentences. A busy executive should understand the full status after reading this. Write it last, put it first.*

*Must include: current status, one key metric or milestone, one risk or ask if urgent.*

*Example: "Project Aurora on track for Q3 launch — 70% of features shipped. Two API dependencies delayed by 2 weeks; recommending scope adjustment for Phase 1. Decision needed by Friday on whether to cut feature X or slip the launch date."*

---

## 3. RAG Status

*Overall health across six dimensions. Be honest — everything green is a red flag.*

| Dimension | Status | One-Line Summary |
|---|---|---|
| **Timeline** | 🟢 Green / 🟡 Amber / 🔴 Red | |
| **Budget** | 🟢 / 🟡 / 🔴 | |
| **Scope** | 🟢 / 🟡 / 🔴 | |
| **Quality** | 🟢 / 🟡 / 🔴 | |
| **Dependencies** | 🟢 / 🟡 / 🔴 | |
| **Team** | 🟢 / 🟡 / 🔴 | |

*🟢 On track, no concerns. 🟡 At risk; mitigation in progress. 🔴 Off track; escalation needed.*

---

## 4. Key Metrics

*4–6 metrics maximum. Every metric must include trend and "why it matters."*

| Metric | Current | vs. Last Period | Trend | Why It Matters |
|---|---|---|---|---|
| | | | ↑ / ↓ / → | |
| | | | | |
| | | | | |
| | | | | |

*Don't include metrics without action implications. If it doesn't inform a decision, cut it.*

---

## 5. Accomplishments (This Period)

*3–5 bullets. Focus on outcomes, not activities. Include business context.*

- *(Milestone / feature / risk mitigated)* — *(business impact: what this enables or unlocks)*
- 
- 

*Omit: routine work, daily standups, individual contributor details. Roll up to team-level outcomes.*

---

## 6. Upcoming Priorities (Next Period)

*3–5 bullets. Format: "By [date]: [deliverable] — impacts [business outcome]"*

- By [date]: *(what's shipping)* — *(impact)*
- By [date]: *(decision needed)* — *(impact if delayed)*
- By [date]: *(dependency milestone)* — *(impact)*

---

## 7. Risks & Mitigation

*Only list risks that are Amber or Red. Green risks don't belong here.*

| Risk | Probability | Business Impact | Mitigation | Owner | Escalation Trigger |
|---|---|---|---|---|---|
| | High / Med / Low | *(revenue, timeline, quality)* | | | *(What makes this a blocker?)* |
| | | | | | |

*Escalate same week a risk becomes Amber. Don't save it for the monthly report.*

---

## 8. Decisions Needed

*If no decisions needed this period, write "None." If there are, be explicit.*

**Decision 1:** *(What needs to be decided?)*
- **Options:**
  - Option A: *(description — tradeoff)*
  - Option B: *(description — tradeoff)*
- **Recommendation:** *(Your advised choice and reasoning)*
- **Deadline:** *(When is this needed — and what happens if delayed?)*
- **Owner:** *(Who makes the final call?)*

---

## 9. Dependencies & Blockers

*Only include items that are currently at risk or require action.*

| Item | Needed From | By Date | Status | Action Needed |
|---|---|---|---|---|
| | *(Team / person)* | | Blocked / At Risk / Resolved | |

---

# PART B — EXTENDED SECTIONS
*(Add for monthly reviews, multi-project updates, or executive escalations.)*

## B1. Budget & Headcount

*(Include only when relevant to the update cycle or when status is Amber/Red.)*

| Field | Plan | Actual | Variance | Notes |
|---|---|---|---|---|
| Budget spent YTD | $X | $Y | +/-% | |
| Budget forecast to EOP | $X | $Y | | |
| Headcount (current) | X | Y | | |
| Open roles / hiring | | | | |

---

## B2. Team Health

*(Include in monthly updates or when there are concerns.)*

- **Departures / attrition:** *(any risks to team continuity?)*
- **Hiring pipeline:** *(open roles, timeline to fill)*
- **Morale / workload:** *(any concerns — keep it team-level, not personal)*
- **Recognition:** *(one callout for strong team contribution)*

---

## B3. Monthly Executive Review Format

*Full structure for monthly leadership updates. Use the 6-section framework: Summary → Status → Metrics → Accomplishments → Priorities → Risks + Decisions.*

**30-Day Metrics Review**

| Metric | 30 Days Ago | Today | Δ | Target | On Track? |
|---|---|---|---|---|---|
| | | | | | ✓ / ⚠ / ✗ |

**Forward-Looking Roadmap (Next 90 Days)**

| Phase | Scope | Target Date | Owner | Status |
|---|---|---|---|---|
| | | | | |

**Strategic Alignment Check**
- **OKR progress:** *(X of Y key results on track)*
- **Strategic bets: on or off track?**
- **What to watch for next month:**

---

## B4. Communication Principles (Reference)

*Internalize these before writing each update.*

| Principle | Wrong | Right |
|---|---|---|
| Lead with impact | "We completed API refactoring" | "API refactoring → 30% latency reduction → on track for Performance OKR" |
| Quantify risks | "Timeline is at risk" | "2-week slip if API dependency doesn't land by June 10 — impacts Q3 launch" |
| Specific asks | "Need help on the timeline" | "Need VP Engineering decision: cut Phase 2 scope (ship June) vs. keep scope and ship July. Recommend June. Decide by Wednesday." |
| Context on metrics | "Velocity: 47 SP" | "Velocity 47 SP (down 15% due to 2 people on jury duty — normalizes next sprint)" |
| Early escalation | Mentioning Amber risk for the first time at monthly review | Escalating same week it becomes Amber |
| Passive → active | "Issues were encountered with the API" | "We found a critical API bug Tuesday. Mitigation: [plan]. Impact: 3-day slip. Owner: Sarah." |

---

## B5. SBAR Format (For Escalations or Issue-Specific Updates)

*Use when something specific needs leadership attention — not for standard status updates.*

**Situation** *(What is happening now? Lead with the most critical information.)*

**Background** *(Why is this happening? Historical context, decisions that led here, dependencies.)*

**Assessment** *(What does it mean? Business impact, risks, RAG status, options.)*

**Recommendation** *(What should we do? 2–3 options with tradeoffs and your clear recommendation. Include the deadline.)*
