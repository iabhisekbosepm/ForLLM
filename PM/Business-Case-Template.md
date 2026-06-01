# Business Case Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Business Case**: The essential sections for any executive ask. Always fill this.
> - **PART B — Extended Sections**: Add for board-level presentations, complex financial modeling, or build/buy/partner decisions.
>
> **Rules of thumb**
> - Lead with the problem in dollars. "40% cart abandonment = $20M annual revenue loss" beats "checkout UX is poor."
> - Present 3–4 options (including "do nothing"). One option looks like you haven't done the analysis.
> - Model conservatively. CFOs discount aggressive projections by 30%. Surprise upside is better than missed targets.
> - Define kill criteria. "We stop if adoption is < 40% by Month 6" builds confidence, not fear.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **CFO scrutiny questions to prepare for:**
> - "Walk me through your revenue assumptions."
> - "What if we only hit 70% of target customers?"
> - "Why this vs. buying it?"
> - "What's our exit if this fails?"
> - "Is this validated by customers?"

---

# PART A — CORE BUSINESS CASE
*(Always fill this in.)*

## 1. Document Metadata

| Field | Value |
|---|---|
| **Initiative name** | |
| **Author / Owner** | |
| **Stakeholders** | *(Exec sponsor, CFO, CTO, legal, sales…)* |
| **Status** | Draft / In Review / Approved / Rejected |
| **Version** | v0.1 |
| **Last updated** | YYYY-MM-DD |
| **Related links** | *(Research, PRD, competitive analysis, financial model)* |

---

## 2. Executive Summary

*1 page maximum. A CFO should understand the entire case in 60 seconds.*

| Field | Value |
|---|---|
| **Problem** | *(One sentence: what is the business losing or missing?)* |
| **Proposed solution** | *(Brief description of the recommended option)* |
| **Investment required** | $X total *(Year 1: $X / 5-year total: $X)* |
| **Expected NPV (5-year)** | $X |
| **Payback period** | *X months* |
| **IRR** | X% |
| **Recommendation** | PROCEED / PILOT / DEFER |
| **Risk level** | High / Medium / Low |

---

## 3. Problem Statement

*Anchor the entire case here. Be specific and quantified.*

- **Current state:** *(Measurable baseline — "40% of checkout attempts fail at step 3")*
- **Gap / problem:** *(What's broken and why it matters)*
- **Business impact:** *(Revenue loss, cost, efficiency drag, competitive threat — in dollars or %)*
- **Why now:** *(What changed? Market shift, data signal, regulatory deadline, competitive pressure?)*
- **What happens if we do nothing:** *(Force yourself to justify urgency)*
- **Evidence:** *(Data, customer quotes, support tickets, analyst reports — cite sources)*

*Formula to internalize: Current State → Gap → Annual Cost of Gap → Why It's Worse Over Time.*

---

## 4. Market Opportunity

*Justify the size of the investment. CFOs want to know the ceiling.*

| Market | Definition | Size | Source |
|---|---|---|---|
| **TAM** *(Total Addressable Market)* | Entire market if you captured 100% | $X | *(Gartner / IDC / analyst report)* |
| **SAM** *(Serviceable Addressable Market)* | Realistic reach given your segment, geography, channel | $X | *(Bottom-up: segment × ACV)* |
| **SOM** *(Serviceable Obtainable Market)* | Your realistic 3–5 year target | $X | *(Sales funnel analysis)* |

*Bottom-up is more credible than top-down. Show your math: "500 enterprise customers × $50K ACV = $25M SAM."*

---

## 5. Solution Options

*Present 3–4 distinct options. Always include "Do Nothing" as a baseline.*

### Option A: [Name] *(e.g., Build In-House)*
- **Description:**
- **Pros:**
- **Cons:**
- **Cost:** $X upfront + $Y/year recurring
- **Timeline:** X months to first value
- **Risk:** *(technical, resource, market)*

### Option B: [Name] *(e.g., Partner / Co-Build)*
- **Description:**
- **Pros:**
- **Cons:**
- **Cost:**
- **Timeline:**
- **Risk:**

### Option C: [Name] *(e.g., Buy / Acquire)*
- **Description:**
- **Pros:**
- **Cons:**
- **Cost:**
- **Timeline:**
- **Risk:**

### Option D: Do Nothing (Status Quo Baseline)
- **Cost:** $0 incremental
- **Annual loss:** *(from problem statement — the opportunity cost of inaction)*
- **Risk:** *(competitive, revenue erosion, regulatory)*

### Decision Matrix

| Criteria | Weight | Option A | Option B | Option C | Option D |
|---|---|---|---|---|---|
| Speed to market | % | /5 | /5 | /5 | /5 |
| Cost efficiency | % | /5 | /5 | /5 | /5 |
| Risk level | % | /5 | /5 | /5 | /5 |
| Strategic value | % | /5 | /5 | /5 | /5 |
| IP / control | % | /5 | /5 | /5 | /5 |
| **Weighted score** | **100%** | | | | |

---

## 6. Financial Model

### Revenue Projections (5-Year)

*Use bottom-up approach: number of customers × ACV, not "X% of TAM."*

| Year | New Customers | Total Customers | ACV | Revenue |
|---|---|---|---|---|
| Y1 | | | $X | $X |
| Y2 | | | $X | $X |
| Y3 | | | $X | $X |
| Y4 | | | $X | $X |
| Y5 | | | $X | $X |

### Cost Structure

| Category | Y1 | Y2 | Y3 | Y4 | Y5 |
|---|---|---|---|---|---|
| Personnel *(headcount × salary)* | | | | | |
| Infrastructure / hosting | | | | | |
| Third-party licenses | | | | | |
| Marketing / GTM | | | | | |
| Contingency (15%) | | | | | |
| **Total costs** | | | | | |

### Cost-Benefit Summary

| Year | Revenue | Costs | Net Benefit | Cumulative |
|---|---|---|---|---|
| 0 | $0 | -$X *(initial investment)* | -$X | -$X |
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

### Key Financial Metrics

| Metric | Value | Formula | Target Threshold |
|---|---|---|---|
| **NPV** | $X | `Σ [CF_n / (1+r)^n] − Investment` *(r = 10–15% WACC)* | Positive |
| **IRR** | X% | Discount rate where NPV = 0 *(Excel: =IRR(...))* | > 20% |
| **Payback Period** | X months | `Investment / Avg Annual Cash Flow` | < 18 months |
| **5-Year ROI** | X% | `(Total Profit / Total Investment) × 100%` | > 300% |

### Sensitivity Analysis

*CFOs always ask: what if assumptions are wrong?*

| Scenario | Assumption | NPV | Payback |
|---|---|---|---|
| **Pessimistic** | Revenue −20%, costs +15% | $X | X months |
| **Base case** | Plan | $X | X months |
| **Optimistic** | Revenue +20%, costs −10% | $X | X months |

**Break-even:** Revenue can decline by _X_% before NPV turns negative.

---

## 7. Risk Assessment

| Risk | Probability | Impact ($) | Severity | Mitigation | Owner |
|---|---|---|---|---|---|
| | High / Med / Low | $X | High / Med / Low | | |
| | | | | | |

*Severity = Probability × Impact. Anything High/High requires a dedicated mitigation plan.*

**Kill criteria:** *(What would make us stop this initiative? Be specific.)*  
*Example: "Halt if < 40% beta adoption by Month 6" or "Stop if COGS exceeds 45% by Q3 Y2."*

---

## 8. Resource Requirements

### Headcount

| Role | Type | Year 1 | Year 2–3 | Annual Cost |
|---|---|---|---|---|
| *(e.g., PM)* | New hire / Reallocation | | | $X |
| *(e.g., Engineers)* | New hire / Contractor | | | $X |
| | | | | |

### Budget Allocation (Year 1)

| Category | Amount | % of Total |
|---|---|---|
| Personnel | $X | % |
| Infrastructure | $X | % |
| Marketing / Launch | $X | % |
| Contingency | $X | % |
| **Total** | **$X** | **100%** |

### Milestones & Timeline

| Milestone | Scope | Target Date | Budget Spend | Owner |
|---|---|---|---|---|
| | | | $X | |

---

## 9. Success Metrics

*Tie each metric back to the financial model.*

| Metric | Definition | Y1 Target | Y3 Target | Y5 Target | How Measured |
|---|---|---|---|---|---|
| ARR *(Annual Recurring Revenue)* | | $X | $X | $X | |
| Customer count | | X | X | X | |
| CAC *(Customer Acquisition Cost)* | Total sales+mktg / new customers | < $X | < $X | | |
| LTV *(Lifetime Value)* | ACV × avg tenure | $X | $X | | |
| LTV:CAC ratio | | > 3:1 | > 5:1 | | |
| Gross margin | | X% | X% | | |
| Net revenue retention | | > 100% | > 110% | | |

---

## 10. Recommendation

**Recommended option:** *(Option X — name)*

**Rationale:**
1. *(Highest risk-adjusted NPV at $X vs. alternatives)*
2. *(Fastest path to revenue — X months vs. Y months)*
3. *(Best fit to current team capacity and strategic priorities)*
4. *(Payback in X months; IRR of X%)*

**Decision criteria met:**
- [ ] NPV > $X *(actual: $X)*
- [ ] IRR > X% *(actual: X%)*
- [ ] Payback < 18 months *(actual: X months)*
- [ ] Fits strategic priorities *(OKR: …)*
- [ ] Mitigates key risks *(…)*

**Conditions for approval:**
- *(Contract signed by Month 1)*
- *($X budget committed)*
- *(Steering committee review: monthly)*

**Kill criteria:** *(Define what would make us stop — specific metric + date)*

**Next steps:**
1. *(Immediate action — by whom, by when)*
2. 
3. 

---

# PART B — EXTENDED SECTIONS
*(Add for board presentations, complex modeling, or regulated environments.)*

## B1. Customer Validation Evidence

*The single most credibility-building section. CFOs and CEOs discount unvalidated financials.*

| Evidence Type | Details | Source |
|---|---|---|
| Customer interviews | *N interviews; X of N confirmed they'd pay $Y* | *(Linked)* |
| Pilot / beta data | *X customers tested; Y% converted at $Z ACV* | *(Linked)* |
| Lost deal analysis | *X deals lost to [competitor] citing [gap]* | *(CRM data)* |
| NPS / CSAT signal | | |
| Support ticket theme | | |

---

## B2. Competitive Analysis (Summary)

*Why this beat the alternatives. Keep short — link to full Competitive Analysis doc.*

| Competitor | How They Solve It | Their Gap | Our Differentiation |
|---|---|---|---|
| | | | |

---

## B3. Financial Formulas Reference

```
NPV         = Σ [CFt / (1+r)^t] − Initial Investment
              r = WACC (typically 10–15%)

IRR         = Discount rate where NPV = 0
              Excel: =IRR(array of cash flows)

Payback     = Initial Investment / Annual Cash Flow (if constant)
              or cumulative cash flow table for variable flows

ROI         = (Total Gain − Total Cost) / Total Cost × 100%

LTV         = (ARPU × Gross Margin %) / Monthly Churn Rate

CAC Payback = CAC / (ARPU × Gross Margin %)  [in months]

NRR         = (Beginning ARR + Expansion − Churn) / Beginning ARR

Break-even  = Fixed Costs / Contribution Margin %
```

---

## B4. Common Business Case Mistakes

| Mistake | Why It Fails | Fix |
|---|---|---|
| No quantified problem | "UX is poor" tells executives nothing | Lead with $X annual impact |
| Only one option | Looks like you haven't done analysis | Present 3–4 options including Do Nothing |
| Overly optimistic projections | CFOs discount by 30%; loses credibility | Model at 60–70% of target; let upside surprise |
| No sensitivity analysis | Assumes best case only | Always show pessimistic / base / optimistic |
| Missing kill criteria | Sounds like you'll continue regardless of results | Define stop criteria upfront |
| Vague resource plan | "$2M budget" without detail | Itemize headcount + tools by quarter |
| Disconnected success metrics | KPIs don't tie to financial model | Every metric should trace back to revenue or cost line |
| Ignoring competitive response | Assumes market stays static | Address how competitors react; show sustained advantage |
| 10-page executive summary | Defeats the purpose | 1 page max; back up with appendix |
| No customer validation | "We think customers want this" | Add even 5 interview quotes; dramatically increases credibility |
