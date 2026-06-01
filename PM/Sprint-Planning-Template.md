# Sprint Planning Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Sprint Plan**: The essentials every sprint needs. Always fill this.
> - **PART B — Extended Sections**: Add for mature teams, complex dependencies, or post-sprint analysis.
>
> **Rules of thumb**
> - Refine the backlog the sprint *before* you plan it. Refining and planning in the same session is too much context to hold.
> - Goals are outcomes, not task lists. "Reduce checkout abandonment" beats "build dropdown component."
> - Add story = remove story. Sprint capacity is fixed. Don't absorb scope without swapping.
> - Version this doc when scope changes mid-sprint (v0.1 → v0.2). Note what changed and why.
> - Delete this instruction block and italic *guiding prompts* once filled.

---

# PART A — CORE SPRINT PLAN
*(Always fill this in.)*

## 1. Sprint Metadata

| Field | Value |
|---|---|
| **Sprint name / number** | *(e.g., "Sprint 42: Q2 Checkout Optimization")* |
| **Dates** | YYYY-MM-DD → YYYY-MM-DD |
| **Sprint length** | 1 / 2 / 3 weeks *(2 weeks is the standard)* |
| **Owner / Scrum Master** | |
| **Team** | *(List all members)* |
| **Version** | v0.1 |
| **Status** | Planning / In Progress / Review / Closed |
| **Links** | *(Jira/Linear board, Slack channel, design files, retro notes)* |

---

## 2. Sprint Goals (1–3 Outcomes)

*Goals are outcomes, not tasks. Write goals first, before breaking down stories.*

**Goal 1:**
- **Statement:** *(What outcome are we trying to achieve?)*
- **Rationale:** *(Why this sprint? Link to roadmap, OKR, customer feedback, or risk.)*
- **Success definition:** *(How will we know we hit it — metric, acceptance criteria, or demo-able outcome?)*
- **Owner / DRI:** *(Directly Responsible Individual)*

**Goal 2:** *(optional)*
- **Statement:**
- **Rationale:**
- **Success definition:**
- **Owner:**

**Goal 3:** *(optional)*
- **Statement:**
- **Rationale:**
- **Success definition:**
- **Owner:**

*If you have more than 3 goals, half are nice-to-haves masquerading as goals. Cut to 3.*

---

## 3. Capacity Planning

### Team Velocity

| Metric | Value | Notes |
|---|---|---|
| **Historical velocity** | *(last 3–5 sprints average, in story points)* | |
| **Velocity trend** | ↑ Improving / ↓ Declining / → Stable | |
| **Forecast this sprint** | *(story points — use historical, not optimism)* | |
| **Confidence in forecast** | High / Medium / Low | |

### Team Availability

| Name | Role | Availability % | Notes |
|---|---|---|---|
| | | 100% | |
| | | | *(PTO, on-call rotation, shared allocation — be specific)* |
| | | | |

*Formula: Real capacity = (team size × hours/week × sprint weeks) adjusted for availability %.*  
*Example: 4 people × 35h × 2 weeks = 280h. At 80% availability = 224h ≈ 35–45 story points.*

---

## 4. Committed Stories

*List only stories that are refined (have title, acceptance criteria, estimates). No vague items.*

| ID | Title | Points | Owner | Priority | Status |
|---|---|---|---|---|---|
| | | | | P0 / P1 / P2 | To Do |
| | | | | | |
| | | | | | |
| | | | | | |
| **Total** | | **Σ pts** | | | |

*Target: Total points ≤ velocity forecast. Leave 10–15% buffer for unplanned work.*

---

## 5. Risks & Mitigation

*Identify uncertainty upfront. If a story has 3+ high risks, park it for next sprint.*

| Risk | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|
| *(Unknown API, unclear design, untested integration…)* | High / Med / Low | High / Med / Low | | |
| | | | | |

**Red flags → de-risk or remove from sprint:**
- Story requires design not yet finalized
- Integration with a third party not yet tested
- Only one person knows the codebase area
- Performance requirements unknown

---

## 6. Dependencies & Blockers

| Story | Depends On | Blocking | Risk | Mitigation |
|---|---|---|---|---|
| | *(Team / story / infra)* | *(Other story)* | | |

*Anti-pattern: "We'll deal with dependencies mid-sprint." Surface all of them now.*

---

## 7. Definition of Done

*Team-wide standard. Story is not Done until all apply.*

**Code**
- [ ] Code reviewed by 1+ person (not author)
- [ ] Linter / CI pipeline passes
- [ ] Edge cases handled (empty, error, loading, success states)

**Testing**
- [ ] Unit tests written (>80% coverage on changed code)
- [ ] Integration tests pass
- [ ] QA tested on staging

**Product Readiness**
- [ ] Acceptance criteria met
- [ ] Product owner sign-off received
- [ ] Feature flag / release plan documented *(if applicable)*
- [ ] Analytics instrumented *(if metric-tracked)*

---

## 8. Sprint Review & Retrospective

| Artifact | When | Owner |
|---|---|---|
| **Sprint review** *(demo completed work)* | *(Date, time)* | PM |
| **Retrospective** *(what went well / to improve)* | *(Date, time)* | Scrum Master |
| **Velocity report** *(update trend)* | EOD last day | Scrum Master |
| **Metrics check** *(goals vs. actual)* | First day of next sprint | PM |

---

# PART B — EXTENDED SECTIONS
*(Add as your team matures or for complex sprints.)*

## B1. Sprint Kickoff Agenda (2–3 Hours)

*Run this at the start of the sprint.*

| Time | Activity | Purpose |
|---|---|---|
| 0:00–0:15 | Goals reconnect | Recap why these goals, link to roadmap |
| 0:15–1:15 | Backlog walkthrough & estimation | Review top stories, estimate, flag risks |
| 1:15–1:30 | Capacity review | Confirm availability, PTO, on-call |
| 1:30–2:00 | Task breakdown | Deep-dive first 3–4 stories, break to tasks, assign owners |
| 2:00–2:15 | Risk & dependency review | Walk through risk table, assign mitigations |
| 2:15–2:25 | Definition of Done sign-off | Confirm everyone agrees on the bar |
| 2:25–2:30 | Logistics | Standup time, Slack channel, Jira board link |

**Pre-planning checklist** *(PM/Scrum Master, 48h before):*
- [ ] Top 15 stories refined (title, AC, estimates, design linked)
- [ ] High-risk stories flagged; mitigations drafted
- [ ] Team availability confirmed
- [ ] Previous retro notes reviewed; improvements to test this sprint
- [ ] Backlog prioritized (RICE or value/effort)

---

## B2. Task Breakdown (Within Stories)

*Break committed stories into tasks (subtasks) to create daily visibility.*

| Task | Owner | Estimate | Status |
|---|---|---|---|
| T1: *(e.g., API design)* | | 2h | Open |
| T2: *(e.g., Implement endpoint)* | | 4h | Open |
| T3: *(e.g., Unit tests)* | | 2h | Open |
| T4: *(e.g., Frontend component)* | | 3h | Open |
| T5: *(e.g., QA testing)* | | 2h | Open |
| **Total** | | **Σh** | |

*Tasks create visibility. A story "looks done" when the PR merges — tasks show where blockers are.*

---

## B3. Mid-Sprint Check-In (Day 5 of 10)

*Run on Wednesday of a 2-week sprint. 30 minutes.*

| Check | Status | Action Needed |
|---|---|---|
| On track for velocity? *(~60% complete by day 5)* | ✓ / ⚠ / ✗ | |
| Risk mitigations working? | ✓ / ⚠ / ✗ | |
| Team capacity holding? *(anyone overloaded?)* | ✓ / ⚠ / ✗ | |
| Scope holding? *(any requests to add stories?)* | ✓ / ⚠ / ✗ | |

---

## B4. Scope Change Protocol

*How to handle requests that arrive mid-sprint.*

| Trigger | Decision | Action |
|---|---|---|
| Production bug / security issue | ACCEPT | Remove equivalent-sized story; document the swap |
| New feature request from sales/GTM | REJECT | Add to backlog; enters planning next sprint |
| Design feedback during QA | DEPENDS | If blocking QA: merge now. If polish: defer to next sprint. |
| Performance issue discovered | ACCEPT | Reduce scope of other story or extend sprint by 1 day; document learnings |

*Document every swap: update sprint plan version (v0.1 → v0.2), note what was removed/added and why.*

---

## B5. Sprint Metrics Tracker

*Update daily during sprint; review in retrospective.*

| Metric | Target | Day 1 | Day 5 | Day 10 | Final |
|---|---|---|---|---|---|
| Velocity *(points completed)* | *(forecast)* | | | | |
| Burn-down *(remaining pts)* | *(ideal line)* | | | | |
| Blocked stories *(count)* | 0 | | | | |
| Scope changes *(adds/removes)* | 0 | | | | |
| Cycle time *(days, avg)* | < 5 days | | | | |

**Post-sprint reflection:**

| Metric | Value | Notes |
|---|---|---|
| Goals achieved | X of Y | |
| Stories completed | X of Y (% points) | |
| Unplanned work | % of sprint | |
| Team happiness *(1–10 poll)* | | |
| Top retro theme | | |

---

## B6. Decision Log

*Track mid-sprint decisions that affect future work.*

| Date | Decision | Rationale | Owner | Impact |
|---|---|---|---|---|
| | | | | |

---

## B7. Sprint Anti-Patterns to Avoid

| Anti-Pattern | Why It Hurts | Fix |
|---|---|---|
| Always miss velocity | Teaches team commitments don't matter | Use actual historical velocity; investigate why estimates miss |
| Story in code review 3+ days | Bottleneck; single PR blocks the team | Set 24h code review SLA; pair on complex PRs |
| No Definition of Done | "Done" means different things to everyone | Document and review DoD in kickoff |
| Retros with no action | Becomes theater | Pick 1–2 concrete experiments per sprint; assign owner |
| 5+ sprint goals | All goals become meaningless | Cap at 3; be ruthless |
| Backlog > 100 stories | Decision fatigue | Archive anything untouched for 3+ months; reprioritize |
| New tasks added without removing old ones | Sprint capacity expands invisibly | Maintain the swap rule: add = remove |
