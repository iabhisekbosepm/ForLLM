# A/B Test Plan Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Test Plan**: The minimum required for every experiment. Always fill this.
> - **PART B — Extended Sections**: Add for complex multi-variant tests, segment analysis, or high-stakes decisions.
>
> **Rules of thumb**
> - Lock hypothesis, metrics, and duration BEFORE launch. Changing them mid-test invalidates results.
> - One primary metric only. Multiple primary metrics inflate false positive rate.
> - No peeking. Stopping early when p < 0.05 inflates your false positive rate to 25–50%.
> - Minimum 14 days. Captures full weekly cycle and allows novelty effect to settle.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **Key formulas**
> ```
> Relative Lift = (Treatment − Control) / Control × 100%
> Sample Size  = (Z_α + Z_β)² × 2p(1−p) / (T − C)²
> RICE Score  = (Reach × Impact × Confidence) / Effort
> ```
> *(Use [evanmiller.org/ab-testing](https://www.evanmiller.org/ab-testing/sample-size.html) for sample size calculator)*

---

# PART A — CORE TEST PLAN
*(Always fill this in before launching.)*

## 1. Test Metadata

| Field | Value |
|---|---|
| **Test ID** | *(e.g., EXP-2024-001-CTA-Button-Position)* |
| **Product Area** | |
| **Owner / PM** | |
| **Stakeholders** | *(Design, Eng, Analytics, Marketing…)* |
| **Launch Date** | YYYY-MM-DD |
| **End Date** | YYYY-MM-DD |
| **Duration** | *X days* |
| **Status** | Planning / QA / Live / Closed |
| **Links** | *(Feature flag, analytics dashboard, Figma, Slack thread)* |

---

## 2. Problem & Hypothesis

### Business Context
*Why are we running this test? What problem or opportunity does it address? Include supporting data.*

### Hypothesis

```
If we [SPECIFIC CHANGE],
then we expect [METRIC] to [DIRECTION] by [AMOUNT],
because [CAUSAL REASONING].
```

*Good example: "If we move the CTA button to center-aligned above the fold, then we expect click-through rate to increase by 8% within 21 days, because heatmaps show 60% of users never scroll past the fold and centered CTAs outperform right-aligned CTAs on mobile by 6–12% (competitor benchmark)."*

**Expected Business Impact:** *(Revenue, engagement, retention — quantify if possible)*

**Implementation Effort:** *(Engineering estimate)*

---

## 3. Variant Definitions

### Control (50% of traffic)
*Describe the current production state exactly.*

| Element | Specification |
|---|---|
| Description | *(Current state)* |
| Code reference | *(Branch / file / feature flag)* |
| Rollback | *(Steps to revert)* |

### Treatment (50% of traffic)
*Describe the proposed change exactly.*

| Element | Specification |
|---|---|
| Description | *(What changes — be specific)* |
| Code reference | *(Branch / file / feature flag)* |
| Rollback | *(Steps to revert)* |

**Variant Assignment Method:** *(e.g., user_id % 2 — stable user-level bucketing)*

*Both variants must have identical tracking/logging. Asymmetric tracking invalidates results.*

---

## 4. Metrics

### Primary Metric (1 only)

| Field | Value |
|---|---|
| **Metric name** | |
| **Definition** | *(Precise calculation — no ambiguity)* |
| **Baseline** | *(Last 30-day average)* |
| **Minimum Detectable Effect (MDE)** | *% relative improvement (e.g., 5% relative = from 4.2% to 4.41%)* |
| **Calculation method** | Chi-square *(binary outcomes)* / T-test *(continuous metrics)* |
| **Confidence level** | 95% (α = 0.05) |
| **Statistical power** | 80% (β = 0.20) |
| **Analytics owner** | |

### Guardrail Metrics (3–5)

*Prevent unintended negative consequences. Alert threshold = % decline that triggers review.*

| Metric | Baseline | Alert Threshold | Definition |
|---|---|---|---|
| *(e.g., Session duration)* | | *>5% relative decrease* | |
| *(e.g., Bounce rate)* | | *>5% relative increase* | |
| *(e.g., 7-day retention)* | | *>3% relative decrease* | |
| | | | |

*If any guardrail breaches its alert threshold, halt the test and investigate.*

---

## 5. Sample Size & Duration

### Calculation

| Input | Value |
|---|---|
| Daily active users (traffic pool) | |
| Traffic split | 50% / 50% |
| Baseline conversion rate | % |
| Minimum Detectable Effect | % relative |
| Confidence level | 95% |
| Power | 80% |
| **Required sample per variant** | *(from calculator)* |
| **Required total sample** | *(× 2)* |
| **Days to reach sample size** | total sample / daily users |

### Duration Decision

```
MIN DURATION = MAX(
  Days to reach sample size,
  7 days  (full weekly cycle),
  14 days (recommended — allows novelty effect to settle)
)
```

**Planned duration:** *(days)*  
**Rationale:** *(Why this duration?)*

---

## 6. Pre-Launch QA Checklist

*Complete before setting test live.*

- [ ] Variant code reviewed and deployed to staging
- [ ] Feature flag configured correctly
- [ ] Variant assignment verified (50/50 split in test traffic)
- [ ] Tracking events firing in both variants (sample events confirmed in logs)
- [ ] Primary metric dashboard configured
- [ ] Guardrail metric alerts configured
- [ ] Sample size calculation peer-reviewed
- [ ] Stakeholder sign-off on duration and success criteria
- [ ] Rollback plan documented and tested
- [ ] No concurrent tests on same user population

---

## 7. Success Criteria & Go/No-Go Decision

*Pre-commit to these criteria before launch. Don't define them after seeing results.*

**Launch criteria (ALL must be met):**
- [ ] Primary metric: p < 0.05 AND 95% CI doesn't include zero
- [ ] Practical significance: Relative lift ≥ MDE target
- [ ] All guardrails: p > 0.05 (clean) OR directionally positive
- [ ] Results stable in final 7 days vs. first 7 days

**Decision table:**

| Scenario | Decision | Action |
|---|---|---|
| Primary p < 0.05, guardrails clean, lift ≥ MDE | **SHIP** | Roll out to 100%; monitor Day 7 post-launch |
| Primary p < 0.05, guardrail minor concern | **INVESTIGATE** | Analyze tradeoff; ship with close monitoring if unrelated |
| Primary p > 0.05 (no significance) | **NO SHIP** | Archive test; document null result; plan next hypothesis |
| Primary negative direction, guardrails violated | **STOP** | Halt immediately; investigate root cause |
| Mixed results across segments | **SEGMENT SHIP** | Ship to segments with p < 0.05 effect; exclude others |

---

## 8. Results (Fill After Test)

| Metric | Control | Treatment | Lift | P-value | CI (95%) | Significant? |
|---|---|---|---|---|---|---|
| *(Primary)* | | | | | | |
| *(Guardrail 1)* | | | | | | |
| *(Guardrail 2)* | | | | | | |

**Sample sizes:** Control: _____ / Treatment: _____  
**Test duration:** _____ days  
**Decision:** SHIP / NO SHIP / INVESTIGATE  
**Rationale:**

**Learnings:** *(What did we learn? What's the next hypothesis?)*

---

# PART B — EXTENDED SECTIONS
*(Add for complex tests or high-stakes decisions.)*

## B1. Segmentation Plan

*Pre-define segments before analyzing. Post-hoc segment selection inflates false positive rate.*

| Segment | Split Rationale | Min Sample Needed |
|---|---|---|
| *(e.g., Mobile vs. Desktop)* | *(UX impact differs by screen size)* | 5,000 per segment |
| *(e.g., New vs. Returning users)* | *(Onboarding path may respond differently)* | 5,000 per segment |

**Multiple comparison correction:** Bonferroni adjusted α = 0.05 / number of segments  
*Example: 2 segments → require p < 0.025 per segment for significance.*

**Warning:** If you only see a significant effect in one segment, that's exploratory — not conclusive. Plan a follow-up test to confirm.

---

## B2. Novelty Effect Analysis

*Users click new UI elements out of curiosity; effect fades after 3–7 days.*

**Detection plan:**
- Compare Day 1–3 results vs. Day 8–14 results
- If Day 1–3 lift is > 1.5× Day 8–14 lift, novelty effect is significant

| Period | Control Rate | Treatment Rate | Lift |
|---|---|---|---|
| Day 1–3 | | | |
| Day 4–7 | | | |
| Day 8–14 | | | |
| Day 15–21 | | | |

**Decision:** Base launch decision on stable period (Day 8+), not total average.

---

## B3. Pre-Mortem (Run Before Launch)

*Team exercise: "Imagine this test fails. What went wrong?"*

| Risk Category | Potential Failure | Severity | Mitigation |
|---|---|---|---|
| Technical | Incorrect 50/50 split (assignment bug) | High | Day-1 sanity check: verify split in logs |
| Technical | Tracking misconfiguration (events not firing) | High | Pre-launch: verify event payloads in staging |
| Analytical | Outlier days skew results | Medium | Document anomalies; report both with/without outliers |
| Product | Novelty effect masks true effect | Medium | Plan 14-day minimum; segment Day 1–3 |
| Organizational | Stakeholder pressure to call winner early | High | Pre-agree on full duration; show peeking risk |
| Confounding | Promo or launch coincides with test | High | Check marketing calendar; pause test if needed |

---

## B4. Common Pitfalls Reference

| Pitfall | Problem | Fix |
|---|---|---|
| **Peeking** | Stopping at p < 0.05 inflates false positive rate to 25–50% | Pre-commit to duration; don't check significance mid-test |
| **Multiple primary metrics** | Testing 10 metrics → ~0.5 false positives by chance | One primary metric; the rest are guardrails or exploratory |
| **Survivorship bias** | If treatment causes churn, only engaged users remain — skewing results positive | Track churn/retention as guardrail; analyze all users (intent-to-treat) |
| **Sample ratio mismatch** | Control gets 52%, treatment gets 48% — randomization failed | Day-1 check: verify split with chi-square goodness-of-fit |
| **Metric defined post-test** | Picking the metric that happened to be significant | Pre-register metrics before launch; label post-hoc analysis as exploratory |
| **Simpson's Paradox** | Overall result positive, all segments negative | Always report segment-level results alongside aggregate |
| **Too-short tests** | Missing weekly cycles or novelty effect | 14-day minimum for most product changes |

---

## B5. Statistical Reference

```
Chi-square (binary metrics: conversion, click):
  χ² = Σ [(Observed − Expected)² / Expected]
  Use when: metric is proportional (CTR, conversion rate)

T-test (continuous metrics: revenue, session time):
  t = (x̄₁ − x̄₂) / √(s₁²/n₁ + s₂²/n₂)
  Use when: metric is a continuous value

Relative Lift:
  Lift = (Treatment − Control) / Control × 100%

Sample size (two proportions):
  N = (Z_α/2 + Z_β)² × 2p(1−p) / (p₁ − p₂)²
  Z_α/2 = 1.96 (95% CI)  |  Z_β = 0.84 (80% power)

Bonferroni correction (multiple comparisons):
  α_adjusted = 0.05 / k   where k = number of tests
```
