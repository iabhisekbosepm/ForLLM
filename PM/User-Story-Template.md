# User Story Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Story**: Minimum fields required for every story. Always fill this.
> - **PART B — Extended Sections**: Add for complex features, API work, or backend processing.
>
> **Rules of thumb**
> - A story should be completable by one person in 3–5 days. If not, split it.
> - Write acceptance criteria as Given/When/Then (BDD). Each scenario = testable.
> - No acceptance criteria = not ready for sprint. Don't estimate without them.
> - Delete this instruction block and italic *guiding prompts* once written.
>
> **INVEST check before writing**
> | Criterion | Question |
> |---|---|
> | **I**ndependent | Can this be developed without blocking another story? |
> | **N**egotiable | Is the "how" (design/tech) flexible, while the "what" is fixed? |
> | **V**aluable | Does this deliver user or business value on its own? |
> | **E**stimable | Can the team reasonably estimate effort? |
> | **S**mall | Completable in 1–5 days by one person? |
> | **T**estable | Do clear pass/fail criteria exist? |

---

# PART A — CORE STORY
*(Always fill this in.)*

## 1. Story Metadata

| Field | Value |
|---|---|
| **Story ID** | *(e.g., US-0124)* |
| **Title** | *(Action-oriented: "Display X for Y in Z context")* |
| **Epic** | *(Link to parent epic)* |
| **Feature Area** | *(Product / Platform / Growth / Infrastructure)* |
| **Priority** | P0 / P1 / P2 / P3 |
| **Story Points** | *(1 / 2 / 3 / 5 / 8 / 13 — if 13+, split the story)* |
| **Status** | To Do / In Progress / In Review / Done |
| **Sprint** | |
| **Owner / Assignee** | |

---

## 2. User Story Statement

```
As a [user persona / role]
I want [specific action or capability]
So that [business value / outcome]
```

*Good examples by type:*
- *UI:* "As a logged-in user, I want to filter results by price range, so I can find items within my budget quickly."
- *API:* "As a third-party developer, I want to fetch user profiles via REST, so I can personalize my integration."
- *Backend:* "As a system, I want to generate a daily summary email, so users stay informed without checking the app."

---

## 3. Context & Background

*Why does this story exist? What problem does it solve? Link to user research, support tickets, or analytics that validate the need.*

- **Current state:** *(What exists today, or what gap exists?)*
- **User pain:** *(What frustrates or blocks users without this?)*
- **Evidence:** *(Data point, customer quote, or research link)*

---

## 4. Acceptance Criteria

*Use Given/When/Then (BDD) format. Aim for 3–7 scenarios. Each must be testable with a clear pass/fail.*

**Scenario 1: [Primary happy path]**
```
Given [initial state / precondition]
When [user action or event]
Then [expected outcome / visible result]
```

**Scenario 2: [Error or edge case]**
```
Given [error condition or edge state]
When [user action]
Then [error message, fallback, or recovery behavior]
```

**Scenario 3: [Secondary flow or state]**
```
Given [...]
When [...]
Then [...]
```

*Add more scenarios for: empty state, loading state, permission edge case, network failure, large data.*

---

## 5. Edge Cases & Error Scenarios

*Explicitly list edge cases. Don't leave these implicit — disagreements about edge cases are the #1 cause of story rejection.*

| Edge Case | Expected Behavior |
|---|---|
| Empty input / no data | |
| Network failure / timeout | |
| Invalid or malformed input | |
| User session expired | |
| Permissions mismatch | |
| Large dataset / pagination | |
| Concurrent edits | |

---

## 6. Definition of Done

*Story is not Done until all of these are checked.*

**Code & Development**
- [ ] Code reviewed by 1+ person (not the author)
- [ ] Linter / CI pipeline passes
- [ ] No console errors or warnings
- [ ] Edge cases from §5 handled

**Testing**
- [ ] Unit tests written (>80% coverage on changed code)
- [ ] Integration tests pass
- [ ] QA tested on staging
- [ ] Browser / device compatibility verified *(if UI)*

**Product Readiness**
- [ ] All acceptance criteria met
- [ ] Product owner sign-off received
- [ ] Feature flag / release plan documented *(if applicable)*
- [ ] Analytics events instrumented *(if metric-tracked feature)*

---

## 7. Dependencies & Blockers

| Dependency | Type | Status | Notes |
|---|---|---|---|
| *(Story / API / team)* | Blocked by / Blocks / External | Open / Resolved | |

---

## 8. Success Metrics

*How will we know this story delivered value after it ships?*

| Metric | Baseline | Target | Timeframe |
|---|---|---|---|
| | | | *30 days post-launch* |

---

# PART B — EXTENDED SECTIONS
*(Add based on story type. Use only the section that applies.)*

## B1. UI / Frontend Story (Add for visual features)

**Design Artifacts**
- Figma file: *(link)*
- Current state screenshot: *(link or embed)*
- Mobile variant: *(link)*

**Technical Considerations**
- Browser compatibility: Chrome, Firefox, Safari, Edge
- Mobile breakpoints: 320px, 768px, 1024px
- Accessibility: WCAG 2.1 AA *(contrast ratio, keyboard nav, screen reader)*
- Performance target: Initial load < 3s, interactions < 100ms

---

## B2. API / Backend Story (Add for endpoint or integration work)

**API Contract**

```
Method + Path: [POST /api/v1/resource]
Auth: [JWT bearer token / API key / none]
Rate limit: [X req/min]

Request:
{
  "field": "value"
}

Response (2XX):
{
  "id": "...",
  "created_at": "..."
}

Error responses:
400 Bad Request — [when]
401 Unauthorized — [when]
409 Conflict — [when]
500 Internal Server Error — [when]
```

**Performance Requirements**
- Response time: < 500ms (p95)
- Throughput target: *(req/hour)*
- Payload size: < 10KB *(adjust as needed)*

**Security Checklist**
- [ ] Input validated and sanitized
- [ ] Auth enforced on endpoint
- [ ] Rate limiting configured
- [ ] No sensitive data in response logs

---

## B3. Backend Processing / Batch Job (Add for scheduled jobs or data pipelines)

**Processing Spec**
- Frequency: *(Daily at HH:MM UTC / triggered by event)*
- Data volume: *(~X records/run)*
- SLA: *(Complete within X minutes)*
- Failure behavior: *(Retry X times, then alert / fail silently)*
- Idempotent: *(Yes / No — safe to retry same data?)*

**Monitoring**
- Success rate metric: *tracked in…*
- Processing time per record: *tracked in…*
- Error rate alert threshold: *(e.g., >2% failure = alert)*

---

## B4. Story Splitting Guide (Use when story is too large)

*If a story is > 8 points or takes > 5 days, split using one of these patterns:*

| Splitting Pattern | How | Example |
|---|---|---|
| **By user journey phase** | Split by what user does first vs. next | "View plan" story → "Select plan" story |
| **By feature area** | Frontend story vs. backend story *(only if separately deployable)* | UI component + API endpoint |
| **By happy path vs. edge cases** | Ship happy path first; edge cases as follow-up | "Basic checkout" + "Guest checkout" |
| **By value tier** | MVP version + enhanced version | "Basic search" + "Filtered search" |

*Rule: Each split story must independently pass the INVEST criteria.*

---

## B5. Anti-Patterns Checklist

*Check before finalizing the story:*

| Anti-Pattern | How to Fix |
|---|---|
| Story covers multiple user journeys | Split into separate stories |
| Acceptance criteria are vague ("system should be fast") | Specify measurable outcome ("API < 500ms p95") |
| Acceptance criteria mention implementation ("use Redis") | Focus on behavior, not tech — move to tech notes |
| No edge cases documented | Add §5 Edge Cases section |
| More than 7 acceptance criteria | Story is too big — split it |
| "Nice-to-have" mixed with must-have | Separate into a second story |
| No design attached for UI story | Block until Figma link is provided |
| Story says "as a system" for a user-facing feature | Reframe from user's perspective |
