# Heuristic Evaluation Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Evaluation**: The essential framework for any heuristic evaluation. Always complete this.
> - **PART B — Extended Sections**: Add for detailed issue registry, per-heuristic deep dives, or remediation planning.
>
> **Rules of thumb**
> - 3–5 evaluators find ~85–95% of issues. More evaluators give diminishing returns.
> - Evaluate INDEPENDENTLY first. Never discuss findings before consolidation — groupthink kills minority insights.
> - Severity is about user impact, not whether YOU noticed it. An expert finding an issue doesn't mean users won't struggle badly.
> - Heuristic evaluation ≠ usability testing. Use this to find issues fast and cheap. Use usability testing to validate that fixes worked.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **Heuristic eval vs. Usability testing**
> | | Heuristic Eval | Usability Testing |
> |---|---|---|
> | Cost | $2K–5K | $5K–15K |
> | Timeline | 1–2 weeks | 3–6 weeks |
> | Participants | 3–5 UX experts | 5–8 real users |
> | Best for | Finding issues fast, pre-user-testing | Validating fixes, real behavior |
> | Misses | User mental models, actual priorities | Issues experts catch but users normalize |

---

# PART A — CORE EVALUATION
*(Always complete this.)*

## 1. Evaluation Metadata

| Field | Value |
|---|---|
| **Evaluation ID** | *(e.g., HE-2024-06-Dashboard-v2)* |
| **Product / Feature** | |
| **Scope** | *(Which flows/screens are in/out of scope)* |
| **Evaluators** | *(Names + roles — see §2)* |
| **Evaluation date** | YYYY-MM-DD |
| **Scenario used** | *(User scenario evaluated — see §3)* |
| **Status** | In Progress / Consolidation / Complete |
| **Overall recommendation** | Pass / Conditional Pass / Fail |
| **Related links** | *(Prototype/product, prior evaluation, design file)* |

---

## 2. Evaluator Profiles

*3–5 evaluators. Mix of UX specialists, domain experts, and end-user proxies.*

| Name | Role | Expertise | Internal/External | Prior product knowledge |
|---|---|---|---|---|
| | UX Specialist | | | High / Low |
| | Domain Expert | | | |
| | End-user Proxy | | | Low (ideal) |
| | *(optional)* External | | External | None (ideal) |

**Bias note:** *All evaluators evaluated independently before consolidation. No discussion until deduplication phase.*

---

## 3. Evaluation Scenario

*Task-based context given to every evaluator. Without this, evaluators test different things and results aren't comparable.*

```
You are a [user role] at a [company type]. You have [experience level] with this type of tool.

Your goal: [Realistic, open-ended task]

Context: [Any background needed to make the scenario real]
```

**Scope reminder for evaluators:**
- In scope: *(specific screens/flows)*
- Out of scope: *(don't evaluate)*
- Focus on: *(primary user journey)*

---

## 4. Nielsen's 10 Heuristics Reference

*Include this in evaluator briefing materials.*

| # | Heuristic | One-Line Test |
|---|---|---|
| 1 | **Visibility of System Status** | "When I act, do I know what's happening?" |
| 2 | **Match Between System & Real World** | "Does this use language and concepts I know?" |
| 3 | **User Control & Freedom** | "Can I easily undo mistakes and exit unwanted states?" |
| 4 | **Consistency & Standards** | "Do similar actions work the same way everywhere?" |
| 5 | **Error Prevention** | "Does the design prevent me from making mistakes?" |
| 6 | **Recognition vs. Recall** | "Can I see my options, or must I remember them?" |
| 7 | **Flexibility & Efficiency** | "Can expert users work faster?" |
| 8 | **Aesthetic & Minimalist Design** | "Does the UI show only what I need right now?" |
| 9 | **Help Users Recognize, Diagnose & Recover from Errors** | "If I get an error, do I understand what happened and how to fix it?" |
| 10 | **Help & Documentation** | "If I'm stuck, can I find clear, task-based help?" |

---

## 5. Severity Rating Scale

| Rating | Label | Definition | Action |
|---|---|---|---|
| **4** | Catastrophe | Prevents task completion; user abandons; data loss risk | Fix immediately; launch blocker |
| **3** | Major | Significantly hinders task; painful workaround exists; high frequency | Fix before launch or within 1 week |
| **2** | Minor | Causes confusion; task still completed; workaround obvious | Schedule for next sprint |
| **1** | Cosmetic | Aesthetic issue only; no functional impact | Backlog; fix if time allows |
| **0** | Not an issue | Evaluator noted but no usability impact | Document; no action |

**Escalation rule:** Any issue found by 3+ evaluators escalates to severity 3 or 4 regardless of individual ratings.

---

## 6. Issue Log (Per Evaluator)

*Each evaluator completes this independently. Combine in §8.*

**Evaluator:** ____________  |  **Date:** ____________  |  **Duration:** ____________

| Issue # | Title (1 line) | Heuristic(s) | Severity | Location / Screenshot | Description | User Impact |
|---|---|---|---|---|---|---|
| E1-001 | | H1 / H2 / … | 4/3/2/1/0 | *(Screen + URL)* | *(What's wrong and why)* | *(Who's affected, how badly)* |
| E1-002 | | | | | | |

---

## 7. Consolidated Issue Registry

*Compiled after all evaluators complete. Deduplicated and consolidated.*

| Issue ID | Title | Heuristic(s) | Severity | Priority | Location | Found By | Status |
|---|---|---|---|---|---|---|---|
| HE-001 | | | 4 | P0 | | All evaluators | Open |
| HE-002 | | | 3 | P1 | | 2 evaluators | Open |
| HE-003 | | | 2 | P2 | | 1 evaluator | Open |

**Deduplication log:**

| Final Issue ID | Merged Issues | Evaluators | Merge Rationale |
|---|---|---|---|
| HE-002 | "Error message vague", "No guidance on fixing", "Unclear error text" | A, B, C | Same root cause: lack of helpful error guidance |

---

## 8. Severity Distribution

**Issue count by severity:**
- Severity 4 (Catastrophe): ___
- Severity 3 (Major): ___
- Severity 2 (Minor): ___
- Severity 1 (Cosmetic): ___
- Severity 0 (Not an issue): ___
- **Total unique issues:** ___

**Heuristic hit list** *(which heuristics have the most violations)*:

| Heuristic | # Issues | Dominant Severity | Trend vs. Prior Eval |
|---|---|---|---|
| H8 — Aesthetic & Minimalist | | | |
| H7 — Flexibility & Efficiency | | | |
| H2 — Match, Real World | | | |
| H4 — Consistency | | | |
| H3 — User Control | | | |

---

## 9. Launch Recommendation

| Scenario | Recommendation |
|---|---|
| 0 Severity 4, few Severity 3 | **PASS** — Ship with minor fixes in next sprint |
| 1–2 Severity 4, several Severity 3 | **CONDITIONAL PASS** — Fix P0 items before launch |
| 3+ Severity 4, or critical flow blocked | **FAIL** — Do not ship; major redesign needed |

**This evaluation:** *(Paste recommendation and rationale)*

---

# PART B — EXTENDED SECTIONS

## B1. Per-Heuristic Deep Dives

*For each heuristic with 3+ issues, write a summary and recommendation.*

**Heuristic [N] — [Name]**
*Score: [Good / Needs Work / Critical]*

Issues found:
- HE-XXX: *(title)* — Severity ___
- HE-XXX: *(title)* — Severity ___

Pattern: *(What's the underlying design problem causing multiple violations?)*

Recommendation: *(Systemic fix — not just patching individual issues)*

---

## B2. Severity Examples by Heuristic

*Use these to calibrate ratings during evaluation.*

**H1 — Visibility of System Status**
- Severity 4: Form submits with no feedback — user refreshes and creates duplicate
- Severity 3: Long operation shows spinner but no time estimate — users unsure if hung
- Severity 2: Success toast disappears in 1.5s before user reads it
- Severity 1: Status message uses technical jargon ("Process initializing")

**H3 — User Control & Freedom**
- Severity 4: Multi-step wizard with no back button — user must restart entire flow
- Severity 3: No undo for delete — users lose important data
- Severity 2: Cancel button is low-contrast link, not obvious
- Severity 1: Undo keyboard shortcut is non-standard

**H5 — Error Prevention**
- Severity 4: Bulk delete with no confirmation — user accidentally destroys 500 records
- Severity 3: Credit card form only validates on submit, not inline — user wastes time
- Severity 2: Date picker allows past dates for future-only bookings
- Severity 1: Form doesn't trim whitespace in email field silently

**H9 — Help Recognize, Diagnose & Recover from Errors**
- Severity 4: Error displays only "Error 40304" — user has no idea what happened
- Severity 3: "Invalid input. Please try again." — which field? Why?
- Severity 2: Error explains problem but not fix: "Password too weak"
- Severity 1: Error message technically correct but uses jargon

---

## B3. Remediation Roadmap

| Phase | Target | Issues | Fix Effort | Timeline | Owner |
|---|---|---|---|---|---|
| **Pre-launch (P0)** | All Severity 4 | ___ issues | | 1 week | |
| **Sprint 1 (P1)** | Top 5 Severity 3 | ___ issues | | 2 weeks | |
| **Post-launch (P2)** | Remaining Severity 3 + High-frequency Severity 2 | | | Next quarter | |
| **Backlog (P3)** | Severity 2 (low frequency) + Severity 1 | | | Future | |

**Priority scoring formula:**
```
Priority = Severity × Frequency
Severity 4 × Any frequency = P0 (always)
Severity 3 × High frequency = P1
Severity 3 × Low frequency = P1-P2 (based on effort)
Severity 2 × High frequency = P2
Severity 1 × Any = P3
```

---

## B4. Heuristic Evaluation Anti-Patterns

| Mistake | Why It Fails | Fix |
|---|---|---|
| All evaluators from same team | Groupthink; same blind spots | Mix: UX specialist + domain expert + user proxy + external |
| Evaluators discuss before consolidation | Minority views suppressed | Strictly independent evaluation; consolidate after |
| Severity based on "I found it easily" | Expert finding ≠ low user impact | Rate on USER impact, not evaluator experience |
| No user scenario provided | Evaluators test different things | Always provide realistic task scenario |
| Not deduplicating | 80+ raw issues overwhelm team | Consolidate before reporting; target 25–40 unique issues |
| No recommendations | Stakeholders debate; nothing gets fixed | Explicit P0/P1/P2 roadmap with owners |
| Expecting this to replace user testing | Misses real user priorities and mental models | Use HE as complement, not replacement |
