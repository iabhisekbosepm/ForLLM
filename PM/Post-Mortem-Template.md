# Post-Mortem Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Post-Mortem**: The essential sections for every SEV-1 or SEV-2 incident.
> - **PART B — Extended Sections**: Add for launch retrospectives, multi-team incidents, or pattern analysis.
>
> **Rules of thumb**
> - Write within 24–48 hours of resolution. Memory fades; urgency creates better action items.
> - Blameless means: focus on system failures, not individual mistakes. "The deploy process lacked safeguards" not "the developer shipped broken code."
> - Every action item needs: owner, deadline, success criteria. Orphaned action items die.
> - Integrate P0/P1 action items into the team's regular sprint/backlog — not a separate system.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **Severity levels**
> | Severity | Definition | Post-Mortem Required? |
> |---|---|---|
> | SEV-1 | Full outage, all users affected | Yes — within 24h |
> | SEV-2 | Partial outage, significant degradation | Yes — within 48h |
> | SEV-3 | Minor impact, workaround exists | Recommended |
> | SEV-4 | Cosmetic / low user impact | Optional |

---

# PART A — CORE POST-MORTEM
*(Always fill this in.)*

## 1. Document Metadata

| Field | Value |
|---|---|
| **Incident ID** | INC-YYYY-MMM-XXX |
| **Title** | *(Brief: "[Service]: [What happened]" — e.g., "Auth Service: Connection pool exhaustion")* |
| **Service(s) Affected** | |
| **Date / Time** | YYYY-MM-DD HH:MM–HH:MM UTC |
| **Duration** | *X minutes* |
| **Severity** | SEV-1 / SEV-2 / SEV-3 |
| **Detection Time** | HH:MM UTC *(when first signal appeared)* |
| **Time to Acknowledge** | *X min after detection* |
| **Time to Mitigation** | *X min after detection* |
| **Customer Impact** | *(# users affected, % of traffic, type of impact)* |
| **Financial Impact** | *(Revenue, SLA credits — "unknown" is OK)* |
| **Participants** | *(Name + role: oncall eng, DBA, infra lead, manager…)* |
| **Author** | |
| **Date Written** | YYYY-MM-DD |
| **Status** | Draft / In Review / Final |
| **Related Links** | *(Slack thread, monitoring dashboard, Git commit, runbook)* |

---

## 2. Executive Summary (TL;DR)

*2–3 sentences. Anyone at the company should understand what happened after reading this. Write it last, put it first.*

*Cover: what happened, how long, customer impact, one-sentence root cause, and resolution approach.*

---

## 3. Customer & Business Impact

### Customer Impact
- **Affected users:** *(number and % of DAU / total users)*
- **Affected transactions / requests:** *(type, volume, failure rate)*
- **Service degradation:** *(latency, error rate, throughput — baseline vs. peak)*
- **User-visible symptoms:** *(errors, timeouts, blank states, incorrect data)*

### Business Impact
- **Revenue impact:** *(quantified if possible; "estimated" is OK)*
- **Support load:** *(inbound tickets, emails, escalations)*
- **Brand / trust impact:** *(social mentions, NPS signals, account escalations)*
- **Team opportunity cost:** *(eng hours diverted from planned work)*

### System Impact
- **Primary service:** *(name, degradation metrics)*
- **Cascading impact:** *(dependent services affected)*
- **Infrastructure strain:** *(CPU, memory, DB connections, network)*

---

## 4. Timeline

*Use absolute UTC timestamps. Include: events observed, actions taken, decisions made. Pull from logs, Slack, alerts, Git commits.*

| Time (UTC) | Event Type | What Happened | Detected By | Source |
|---|---|---|---|---|
| HH:MM | START | *(Incident begins — may not be immediately noticed)* | *(Auto / Manual)* | *(Log / Alert / User report)* |
| HH:MM | SIGNAL | *(Early indicator missed or seen)* | | |
| HH:MM | ALERT | *(First automated alert fired)* | *(Alert system)* | *(PagerDuty / CloudWatch…)* |
| HH:MM | ACK | *(Oncall acknowledged)* | *(Name)* | *(PagerDuty)* |
| HH:MM | TRIAGE | *(Initial diagnosis — what did they check first?)* | *(Name)* | *(Logs / Runbook)* |
| HH:MM | ESCALATION | *(Escalated to specialist or second-line)* | *(Name)* | *(Slack)* |
| HH:MM | ROOT CAUSE | *(Root cause identified)* | *(Name)* | *(Tool / Analysis)* |
| HH:MM | MITIGATION | *(Action taken — incident fixed)* | *(Name)* | *(Terminal / Tool)* |
| HH:MM | RECOVERY | *(Metrics normalize)* | *(Monitoring)* | *(Dashboard)* |
| HH:MM | ALL-CLEAR | *(Incident resolved)* | *(Name)* | *(Dashboard / Slack)* |

**Timeline analysis:**
- Time to detection: *X min* — Was monitoring sufficient?
- Time to diagnosis: *X min* — Was the runbook helpful? Was escalation clear?
- Time to mitigation: *X min* — Was the fix obvious? Resources available?
- Any early signals that were missed? *(These become action items.)*

---

## 5. Root Cause & Contributing Factors

### Root Cause (Deepest Systemic Issue)

*One sentence naming the systemic failure — not the proximate technical cause, but why the system didn't prevent it.*

*Example: "No schema change review process meant a non-performant query design reached production undetected."*

### Contributing Factors

*List 3–5 factors, each of which — independently — could have prevented the incident if fixed.*

#### 1. [Factor name]
- **What:** *(Description of the gap or failure)*
- **Impact:** *(How did this contribute to the incident?)*
- **Evidence:** *(What data or observation confirms this mattered?)*

#### 2. [Factor name]
- **What:**
- **Impact:**
- **Evidence:**

#### 3. [Factor name]
- **What:**
- **Impact:**
- **Evidence:**

### 5-Why Analysis

```
Why did [incident] happen?
A: [Proximate cause]

Why did [proximate cause] occur?
A: [Intermediate cause]

Why did [intermediate cause] occur?
A: [Contributing factor]

Why did [contributing factor] exist?
A: [Systemic gap]

Why does [systemic gap] exist?
A: [Root cause — the deepest preventable issue]
```

---

## 6. Action Items

*Every item must have: what, why, owner, deadline, success criteria. No orphaned items.*

### P0 — Immediate Fix (Do This Week)
*Prevent the exact same incident from recurring immediately.*

| Field | Value |
|---|---|
| **What** | *(Specific, actionable fix)* |
| **Why** | *(Why this prevents recurrence)* |
| **Owner** | *(Name + @handle)* |
| **Deadline** | YYYY-MM-DD |
| **Success criteria** | *(How do we know it's done? Measurable.)* |
| **Type** | Technical Fix / Monitoring / Process / Documentation / Training |

### P1 — System Safeguard (Do This Month)
*Prevent a class of related incidents.*

| Field | Value |
|---|---|
| **What** | |
| **Why** | |
| **Owner** | |
| **Deadline** | YYYY-MM-DD |
| **Success criteria** | |
| **Estimated effort** | *hours* |
| **Type** | |
| **Blockers** | *(Dependencies if any)* |

### P2 — Enhancement (Do This Quarter)

| Field | Value |
|---|---|
| **What** | |
| **Owner** | |
| **Deadline** | YYYY-MM-DD |
| **Success criteria** | |

### P3 — Nice-to-Have (Backlog)

| Field | Value |
|---|---|
| **What** | |
| **Owner** | |
| **Defer reason** | |

---

## 7. How to Prevent Recurrence

*Three layers:*

**Immediate (24–48 hours):** *(P0 actions — stop the bleeding)*

**Short-term (2–4 weeks):** *(P1 actions — monitoring, documentation, process fixes)*

**Medium-term (4–12 weeks):** *(P2 actions — organizational changes, training, architecture)*

**Key lessons:**
- *(What do we do differently next time?)*
- *(What assumption was wrong?)*
- *(What did this reveal about our system?)*

---

# PART B — EXTENDED SECTIONS
*(Add for complex incidents, launch retrospectives, or pattern analysis.)*

## B1. Monitoring & Alerting Gaps

### What Alerted
| Alert Rule | Fired At | Threshold | What It Measures |
|---|---|---|---|
| | | | |

### What Didn't Alert (Gaps)
| Metric | Why It Should Have Alerted | Why It Didn't | Action Item |
|---|---|---|---|
| | | | |

### Improvements
- *New alert to create:*
- *Thresholds to adjust:*
- *Dashboard to update:*

---

## B2. Runbook Review

| Runbook | Did It Help? | What Was Missing | Update Required |
|---|---|---|---|
| | Yes / Partial / No | | |

*Add or update runbook steps as a P1 action item.*

---

## B3. Launch Retrospective (Feature-Related Incidents)

*Use when an incident is caused by a product launch or deployment. Answer both incident AND process questions.*

| Question | Answer |
|---|---|
| Why wasn't this caught in staging? | |
| Did rollback fail? Why? | |
| Was the launch scope too large? | |
| Were there missing feature flags or kill switches? | |
| Were success metrics and alerts configured pre-launch? | |
| What would have changed the launch decision? | |

---

## B4. Blameless Culture Checklist

*Use this checklist to evaluate the quality of your post-mortem process:*

- [ ] Language focuses on systems and processes, not individuals
- [ ] No "user error" root causes (user behavior is a signal to improve UX or documentation)
- [ ] Action items target processes, automation, and monitoring — not "be more careful"
- [ ] All participants felt safe speaking honestly
- [ ] Incident will NOT affect performance reviews (confirm this explicitly)
- [ ] Leadership participated and modeled blameless behavior

*If any item is unchecked, address it before publishing the post-mortem.*

---

## B5. Quarterly Pattern Analysis

*Review all post-mortems quarterly. Group by pattern. Prioritize systemic investments.*

| Pattern / Category | Incident Count (Qtr) | Top Root Cause | Systemic Investment Needed |
|---|---|---|---|
| *(e.g., Missing monitoring)* | | | |
| *(e.g., Schema changes without review)* | | | |
| *(e.g., Runbook gaps)* | | | |

*If the same root cause appears 3+ times in a quarter, treat it as a roadmap item — not a one-off fix.*

---

## B6. Post-Mortem Follow-Up (30-Day Check)

*Schedule a 30-day follow-up to verify prevention measures worked.*

| Action Item | Owner | Completed? | Verified Working? | Notes |
|---|---|---|---|---|
| P0 — *(name)* | | ✓ / ✗ | ✓ / ✗ | |
| P1 — *(name)* | | ✓ / ✗ | ✓ / ✗ | |

**Did the incident recur?** Yes / No  
**Did any prevention measure stop a near-miss?** *(Document and share — this builds culture.)*
