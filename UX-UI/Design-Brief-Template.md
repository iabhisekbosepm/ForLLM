# Design Brief Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Brief**: Required for every design initiative. Always fill this.
> - **PART B — Extended Sections**: Add for complex features, regulatory work, or multi-platform projects.
>
> **Rules of thumb**
> - A brief is not a PRD. It provides design direction and constraints — not functional specifications.
> - Lead with data. "28% abandonment at step 3" beats "users find checkout confusing."
> - Accessibility is a core constraint, not an afterthought. Include it in §5 from the start.
> - Every success criterion must be measurable and testable. "Users like it more" doesn't count.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **Brief vs. PRD distinction**
> | Design Brief | PRD |
> |---|---|
> | Design direction + constraints | Full functional requirements |
> | Audience: Design, UX Research | Audience: Engineering, Product |
> | Visual + interaction concepts | API specs, data schemas, edge cases |
> | User experience metrics | Business + technical metrics |

---

# PART A — CORE DESIGN BRIEF
*(Always fill this in.)*

## 1. Document Metadata

| Field | Value |
|---|---|
| **Project name** | |
| **Feature / Flow** | *(Specific scope — "Checkout Step 3" not "Checkout")* |
| **Owner / Lead Designer** | |
| **Stakeholders** | *(PM, Eng Lead, Marketing, Legal, Accessibility…)* |
| **Status** | Draft / In Review / Approved |
| **Version** | v0.1 |
| **Last updated** | YYYY-MM-DD |
| **Related links** | *(PRD, user research, analytics, competitor screens, Figma)* |

---

## 2. Executive Summary

*1 paragraph. Anyone at the company should understand what we're designing, for whom, and why — after reading this. Write it last, put it first.*

---

## 3. Design Problem Statement

*The anchor of the entire brief. Be specific, quantified, and user-centered. Not "improve UX" — that's a solution, not a problem.*

- **What's broken or missing:** *(Specific observation grounded in data, not assumption)*
- **Who experiences this:** *(Exact user segment — role, context, frequency)*
- **Measured impact:** *(Revenue loss, drop-off %, support volume, NPS delta)*
- **Evidence:** *(Data point, user quote, support ticket theme, research finding — cite source)*
- **Why now:** *(What changed? Market shift, new research, strategic priority, upcoming deadline?)*

**Good example:** "28% of first-time mobile users abandon at the payment verification step (vs. 8% site average). Post-checkout survey: 68% cite 'unclear security info' as the reason. Costs ~$2M annually in blocked transactions."

**Anti-pattern:** "Users find checkout confusing and we need to improve it."

---

## 4. Target Users

*Not generic personas — actionable ones tied to this specific problem.*

| Persona | Who they are | Job to be done | Key pain | % of affected users |
|---|---|---|---|---|
| *(Name)* | *(Role, context, device preference)* | *(What job are they hiring the product to do?)* | *(Specific frustration)* | % |

**Accessibility needs for this segment:**
- *(Vision, motor, cognitive, hearing requirements specific to these users)*
- *(e.g., "30% of users are 55+; larger touch targets and high contrast critical")*

---

## 5. Business Goals vs. User Goals

*Make the alignment explicit. Resolve conflicts here — don't let them surface during design review.*

**Business goals** *(2–4 max)*:
1. *(e.g., Increase checkout conversion from 12% → 15%)*
2. 
3. 

**User goals** *(2–4 max)*:
1. *(e.g., Complete checkout in < 2 minutes without anxiety about security)*
2. 
3. 

**Alignment:** *Which user goals directly drive which business goals?*

**Conflicts:** *Where do they compete? How will design resolve the tradeoff?*
- *Example: "Collect marketing opt-in vs. reduce form friction → use post-checkout opt-in, not at payment step"*

---

## 6. Constraints

### Technical Constraints
- *(API limitations, response time budgets, third-party integration restrictions)*
- *(Browser/device support requirements — Chrome 90+, iOS 14+, etc.)*
- *(Performance targets — page load < 3s, interaction < 100ms)*

### Brand & Design System Constraints
- *(Which components must be reused vs. can be extended vs. must be created new)*
- *(Color, typography, and interaction patterns locked vs. flexible)*
- *(Design system version — link to Figma library)*

### Accessibility Constraints
- **WCAG target:** AA *(specify if AAA required for any element)*
- **Color contrast minimum:** 4.5:1 text, 3:1 UI components
- **Specific requirements:** *(Screen readers, keyboard nav, voice control, reduced motion)*
- **Testing requirement:** *(Accessibility review at wireframe stage, not final design)*

### Timeline & Resource Constraints
- **Design exploration:** *(dates)*
- **Wireframe review:** *(date)*
- **High-fidelity handoff:** *(date)*
- **Development timeline:** *(date)*
- **Team:** *(designers, researchers, design system support available?)*

### Scope Constraints
- **In scope:** *(exact list)*
- **Out of scope:** *(explicit list — prevents scope creep)*
- **Parking lot:** *(good ideas not in this project — link to backlog)*

---

## 7. Success Criteria

*Every criterion must be measurable and testable. Define how you'll verify each one.*

**Quantitative:**
| Metric | Current Baseline | Target | How Measured | Timeframe |
|---|---|---|---|---|
| *(e.g., Checkout completion rate)* | X% | Y% | Analytics | 30 days post-launch |
| *(e.g., Task completion in usability test)* | N/A | > 80% | Moderated testing | Before launch |
| *(e.g., Error rate at payment step)* | X% | < Y% | Analytics | 30 days post-launch |

**Qualitative:**
- *(e.g., "Users feel confident their data is secure" — validated in 1:1 testing)*
- *(e.g., "Design reflects premium brand positioning" — stakeholder sign-off)*

**Accessibility:**
- Zero WCAG AA violations (automated axe scan + manual keyboard review)
- Passes screen reader test for primary flows

---

## 8. Design Principles (Project-Specific)

*Not generic ("be simple") — principles that make hard decisions easier. Each one resolves a specific tradeoff this project will face.*

**1. [Principle name]**
- *Why this project:* *(The tradeoff it resolves)*
- *Implication for design:* *(What it means in practice)*

**2. [Principle name]**
- *Why this project:*
- *Implication:*

**3. [Principle name]**
- *Why this project:*
- *Implication:*

*Example: "Clarity Over Aesthetics" — because users with low payment confidence hesitate on unclear steps. Implication: readable labels, explicit pricing breakdowns, always show security signal.*

---

## 9. Stakeholder Map

| Stakeholder | Role | Approval Rights | Key Concern | Alignment Status |
|---|---|---|---|---|
| | Decision maker | Final sign-off | | Aligned / To align |
| | Technical | Feasibility gate | | |
| | Brand | Design consistency | | |
| | Legal / Compliance | *(if applicable)* | | |

**Alignment checkpoints:**
- *(Week 1): Problem statement + research review with ...*
- *(Week 2): Design principles + scope alignment with ...*
- *(Week 3): Wireframe review with ...*
- *(Final): High-fidelity sign-off before handoff*

---

# PART B — EXTENDED SECTIONS
*(Add when complexity, risk, or multi-platform scope warrants it.)*

## B1. Research Foundation

*What we already know. Cite all sources.*

| Evidence Type | Finding | Source | Date |
|---|---|---|---|
| User interviews | | | |
| Analytics | | | |
| Support tickets | | | |
| Usability test | | | |
| Competitive analysis | | | |

**Gaps — what we still need to learn before design can finalize:**
- *(Research question → methodology → owner → date needed by)*

---

## B2. Competitive & Market Context

*Keep short. Link to full Competitive Analysis doc.*

| Competitor | How they solve it | Their gap | Our opportunity |
|---|---|---|---|
| | | | |

**Key insight:** *(What does the competitive landscape tell us about user expectations?)*

---

## B3. Multi-Platform Considerations

*(Use when the design must work across web, iOS, Android, tablet, etc.)*

| Platform | Priority | Constraints | Key Differences |
|---|---|---|---|
| Mobile web | Primary | iOS Safari, Android Chrome | Touch-first, no hover |
| Desktop web | Secondary | Chrome, Firefox, Safari, Edge | Full feature set |
| Native iOS | Tertiary | Human Interface Guidelines | Native patterns expected |
| Native Android | Tertiary | Material Design 3 | Different gestures |

---

## B4. Design System Impact

*(Document what this project adds, changes, or reuses in the design system.)*

| Component | Action | Owner | Notes |
|---|---|---|---|
| *(Button component)* | Reuse | Design Systems | No change needed |
| *(Payment card input)* | New | Lead Designer | Requires DS review before build |
| *(Error state)* | Extend | Lead Designer | Adding new variant |

---

## B5. Pre-Approval Checklist

*Review before submitting brief for stakeholder sign-off.*

- [ ] Problem statement is specific, quantified, and grounded in data
- [ ] Success metrics are measurable and testable (not "users like it more")
- [ ] Accessibility requirements are explicit (WCAG level, specific needs)
- [ ] Constraints are realistic given timeline and resources
- [ ] Design principles are project-specific (not generic)
- [ ] Scope is explicit — in, out, and parking lot all defined
- [ ] Stakeholders identified with approval rights and key concerns
- [ ] Brief avoids vague language: "modern," "clean," "intuitive" (use metrics instead)
- [ ] Dependencies identified (design system components, research gaps, regulatory review)
- [ ] Alignment checkpoints scheduled
