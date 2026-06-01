# Feature Prioritization Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Prioritization**: Essential scoring for every feature. Use this always.
> - **PART B — Extended Frameworks**: Add when multiple frameworks are needed, or when presenting to leadership.
>
> **Rules of thumb**
> - Score features before committing to build. Never "we'll figure it out in planning."
> - No success metric = auto-deprioritize regardless of score.
> - Re-evaluate scores monthly; market and priorities shift.
> - Delete this instruction block and italic *guiding prompts* once filled in.
>
> **Framework selection**
> | Situation | Use |
> |---|---|
> | Standard product backlog | RICE (default) |
> | Rapid growth / startup | ICE |
> | Fixed-deadline launch | MoSCoW |
> | Multi-stakeholder alignment | Weighted Matrix |

---

# PART A — CORE PRIORITIZATION
*(Always fill this in.)*

## 1. Feature Metadata

| Field | Value |
|---|---|
| **Feature name** | |
| **Owner / DRI** | |
| **Status** | New / Validation / Estimated / In Progress / Shipped / Deprioritized |
| **Submitted by** | *(who requested this — customer, sales, eng, PM…)* |
| **Last scored** | YYYY-MM-DD |
| **Related links** | *(PRD, research, tickets, designs)* |

---

## 2. Business Case (One Paragraph)

*What user or business problem does this solve? Why should we build it over other things? Include the evidence — data, quotes, research. If you can't write this paragraph convincingly, deprioritize until you can.*

---

## 3. Strategic Alignment

| OKR / Goal | Alignment | Notes |
|---|---|---|
| *(Quarterly OKR 1)* | High / Medium / Low / None | |
| *(Quarterly OKR 2)* | High / Medium / Low / None | |

*Features with no OKR alignment are automatically P2 or lower, unless they are tech debt, compliance, or foundational.*

---

## 4. RICE Score (Primary Scoring Method)

**Formula:** `RICE = (Reach × Impact × Confidence) / Effort`

| Component | Value | Reasoning |
|---|---|---|
| **Reach** | *(users/quarter)* | *How many users will experience this in 90 days? Be literal — if 30% of 1M users touch this area, Reach = 300K.* |
| **Impact** | *(3 / 2 / 1 / 0.5 / 0.25)* | *3 = transforms behavior, 2 = high, 1 = medium, 0.5 = low, 0.25 = minimal* |
| **Confidence** | *(100% / 75% / 50% / 25%)* | *100% = validated data, 75% = reasonable evidence, 50% = assumption, 25% = guess* |
| **Effort** | *(person-weeks)* | *Include design + engineering + QA + deployment. Not hours.* |
| **RICE Score** | **= (R × I × C) / E** | |

**Interpretation:**
| RICE Score | Priority Signal |
|---|---|
| > 500K | Exceptional — do now |
| 200K–500K | High — next cycle |
| 50K–200K | Medium — backlog |
| < 50K | Low — deprioritize unless strategic |

---

## 5. Effort Breakdown

| Area | Estimate | Notes |
|---|---|---|
| Design | *days* | |
| Engineering | *days* | |
| QA / Testing | *days* | |
| Deployment / Infra | *days* | |
| Post-launch monitoring | *days* | |
| Contingency (20%) | *days* | |
| **Total** | **days → person-weeks** | |

*If effort estimate is a guess, mark Confidence at 50% or lower until engineering reviews it.*

---

## 6. Success Metric

*One measurable outcome. If you can't define this, stop — don't build until you can.*

| Metric | Baseline | Target | Timeframe | How Measured |
|---|---|---|---|---|
| | | | *30 / 60 / 90 days* | |

**Failure signal:** *What would tell us this feature didn't work? Define this upfront.*

---

## 7. Decision Gates

*Must pass all before committing to build.*

- [ ] Aligns to a current OKR or goal
- [ ] Addresses a validated user/business problem (not assumption)
- [ ] Has a clear, measurable success metric
- [ ] Effort estimate is within available capacity
- [ ] No blocking dependencies unresolved
- [ ] Does not significantly increase technical debt

---

## 8. Risk Assessment

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Technical | | | |
| Adoption | | | |
| Competitive | | | |
| Dependency | | | |

*If 3+ risks are High/High, don't commit — break scope or park for next cycle.*

---

## 9. Prioritization Decision

| Field | Value |
|---|---|
| **Recommended cycle** | Q__ / Sprint __ / Backlog / Deprioritized |
| **Rank (vs. other features)** | *(e.g., #3 of 12 in backlog)* |
| **Reasoning** | *Why this position relative to peers?* |
| **Trigger to reconsider** | *What data or event would move this up? (e.g., "if 3 more enterprise deals blocked")* |

---

## 10. Sign-Off

| Field | Value |
|---|---|
| **Approved by** | |
| **Date** | YYYY-MM-DD |
| **Review date** | *When to re-evaluate if not yet built* |

---

# PART B — EXTENDED FRAMEWORKS
*(Add when comparing multiple features, presenting to leadership, or using alternative scoring.)*

## B1. ICE Score (Alternative — Use for Rapid Iteration / Startup Context)

**Formula:** `ICE = Impact × Confidence × Ease`  *(all 1–10 scale)*

| Component | Score (1–10) | Reasoning |
|---|---|---|
| **Impact** | | *10 = transforms key metric, 5 = meaningful improvement, 1 = minimal change* |
| **Confidence** | | *10 = validated data, 5 = some evidence, 1 = hypothesis only* |
| **Ease** | | *10 = 1–2 days, 7 = 2–3 weeks, 5 = 1 month, 3 = 6+ weeks, 1 = 3+ months* |
| **ICE Score** | **= I × C × E** | |

---

## B2. MoSCoW Categorization (Use for Fixed-Deadline Launches)

| Category | Definition | This Feature? |
|---|---|---|
| **Must Have** | Product fails without it; legal/revenue/safety blocker | ☐ Yes / ☐ No |
| **Should Have** | High impact; significant delivery risk if missing | ☐ Yes / ☐ No |
| **Could Have** | Nice-to-have; won't break launch if absent | ☐ Yes / ☐ No |
| **Won't Have (This Time)** | Explicitly deferred; prevents scope creep | ☐ Yes / ☐ No |

**MoSCoW Rationale:**
- Must because: *…*
- Deferred because: *…*
- Trigger to reconsider Won't: *…*

*Rule of thumb: Must ≤ 20% of backlog, Should ≤ 40%, Could ≤ 40%. If 50%+ are Must, you haven't prioritized.*

---

## B3. Weighted Scoring Matrix (Use for Multi-Stakeholder Alignment)

*Agree on criteria weights before scoring. Weights must sum to 100%.*

| Criteria | Weight | Score (1–10) | Weighted Score |
|---|---|---|---|
| User impact *(% affected, depth of value)* | % | | |
| Revenue / business value | % | | |
| Strategic alignment *(OKR fit)* | % | | |
| Effort *(lower effort = higher score)* | % | | |
| Risk *(lower risk = higher score)* | % | | |
| **Total** | **100%** | | **Σ** |

*Score guide: 10 = exceptional, 7 = strong, 5 = moderate, 3 = weak, 1 = minimal.*

---

## B4. Prioritization Comparison Table (Backlog View)

*Use to rank multiple features side-by-side.*

| Feature | RICE Score | MoSCoW | Effort (weeks) | OKR Alignment | Rank | Decision |
|---|---|---|---|---|---|---|
| | | | | | | |
| | | | | | | |
| | | | | | | |

---

## B5. Red Flags — Deprioritize Even if Score is High

*If any of the following are true, halt and resolve before scoring or committing:*

| Red Flag | Action |
|---|---|
| No success metric defined | Define metric or deprioritize |
| Effort is a guess (no engineering review) | Get estimate; reduce Confidence % |
| User problem is unvalidated assumption | Require research or evidence first |
| Blocking dependency unresolved | Park until dependency clears |
| Stakeholder conflict on priority | Resolve via OKR alignment, then re-score |
| Estimate is 2× worse than similar past features | Re-estimate with engineering; split scope |
| Introduces significant technical debt | Bundle with debt task or deprioritize |

---

## B6. Post-Build Retrospective (Fill After Launch)

*Close the loop — did this feature deliver what we scored it for?*

| Field | Estimate (pre-build) | Actual (post-launch) |
|---|---|---|
| Reach | | |
| Impact | | |
| Effort | | |
| Success metric result | | |
| RICE Score (retroactive) | | |

**Lessons:** *What was wrong in our estimate? How do we calibrate next time?*
