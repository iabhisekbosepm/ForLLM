# Usability Testing Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Test Plan**: Required fields for every usability test. Always fill this.
> - **PART B — Extended Sections**: Add for complex analysis, session scripts, or synthesis.
>
> **Rules of thumb**
> - 5 users reveal ~85% of usability issues (Nielsen's law). Do multiple rounds of 5, not one round of 20.
> - Test early and often. Wireframes are testable. Don't wait for polish.
> - Moderated for depth ("why?"), unmoderated for speed ("what happened?").
> - Every finding needs a severity rating before it becomes a recommendation.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **Moderated vs. Unmoderated**
> | | Moderated | Unmoderated |
> |---|---|---|
> | Can ask "why"? | Yes | No |
> | Timeline | 2–3 weeks | 3–5 days |
> | Cost per session | $100–300 | $10–50 |
> | Best for | Complex flows, exploratory | Rapid iteration, validation |
> | Tools | Zoom, Lookback, UserTesting | Maze, UserTesting, Lookback |

---

# PART A — CORE TEST PLAN
*(Always fill this in.)*

## 1. Test Metadata

| Field | Value |
|---|---|
| **Test ID** | *(e.g., UT-2024-Q2-Checkout-v2)* |
| **Feature / Flow tested** | |
| **Owner** | |
| **Stakeholders** | *(PM, Design Lead, Eng, Analytics…)* |
| **Test type** | Moderated / Unmoderated / Hybrid |
| **Format** | Remote / In-person |
| **Dates** | Recruiting: [dates] / Sessions: [dates] / Synthesis: [dates] |
| **Status** | Planning / Recruiting / In Progress / Analysis / Complete |
| **Links** | *(Design Brief, prototype, Figma, prior test results)* |

---

## 2. Test Objectives

**Primary objective** *(one only — the decision this test informs)*:

**Secondary objectives** *(2–3 max)*:
1. 
2. 

**Decision this test gates:**
*(e.g., "If task completion < 70%, we redesign the navigation before launch. If ≥ 80%, we ship.")*

---

## 3. Participant Profile

**Target:** *(Role, experience level, tech comfort, product familiarity)*

**Sample size:** *(5 for moderated discovery; 20–50 for unmoderated validation)*

**Diversity:**
- *(New users: N)*
- *(Experienced users: N)*
- *(Users with accessibility needs: N)* ← include at least 1

**Screener criteria:**

| Must Have | Nice to Have | Exclude |
|---|---|---|
| | | Company employees |
| | | Product team referrals |
| | | Designers/UX professionals |

**Recruitment source:** *(UserTesting, Maze panel, existing users, Respondent.io)*

**Incentive:** $_____ per session

---

## 4. Task Scenarios

*Each task must be: realistic, open-ended (no UI element names), contextual.*

| Task # | Scenario Context | Task Goal | Success Criteria | Est. Time |
|---|---|---|---|---|
| 1 | *[Realistic background — who they are, what situation they're in]* | *[Open-ended goal]* | *[Observable behavior = success]* | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

*Max 5–6 tasks. More causes fatigue and invalid feedback.*

**Anti-pattern:** "Click the blue 'Save' button at the top right."  
**Correct format:** "You've been working on this report for an hour. What would you do to make sure your progress is saved?"

---

## 5. Metrics

### Quantitative Metrics (per task)

| Metric | Definition | Target | How Measured |
|---|---|---|---|
| **Task success rate** | % completing without assistance | > 80% for core flows | Pass/fail per task |
| **Time on task** | Seconds from task brief to completion/abandonment | < X seconds | Timestamp |
| **Error rate** | Wrong clicks, failed attempts, backtracks | < Y errors/task | Observation count |
| **Aided completion** | Completed only with moderator hint | Should be < 20% | Observation |

### Session-Level Metrics

| Metric | Scale | Benchmark | When Administered |
|---|---|---|---|
| **SUS (System Usability Scale)** | 0–100 | ≥ 68 = average | Post-session, 10-question survey |
| **Task ease rating** | 1–7 | ≥ 5 = acceptable | Post each task |
| **Confidence score** | 1–5 | ≥ 3.5 | Post each task |

**SUS score benchmarks:** 80+ = Excellent, 68 = Industry average, < 50 = Major issues

---

## 6. Severity Rating Scale

*Rate every finding before including it in the report.*

| Severity | Definition | Example | Fix Priority |
|---|---|---|---|
| **Critical (1)** | Blocks task completion; user abandons | Payment button not clickable | Fix before launch |
| **Major (2)** | Significantly hinders task; workaround exists but painful | Search takes 8s; user waits, unsure | Fix in next sprint |
| **Minor (3)** | Minor confusion; task still completed | Button label slightly unclear | Prioritize based on frequency |
| **Cosmetic (4)** | Aesthetic issue only; no functional impact | Inconsistent spacing | Fix if time permits |

**Escalation rule:** Any issue appearing in 3+ sessions automatically escalates to Critical or Major regardless of initial rating.

---

## 7. Observation Guide

*Use during sessions. One copy per participant.*

```
PARTICIPANT: ___  |  DATE: ___  |  DURATION: ___  |  MODERATOR: ___

TASK 1: _______________________
Start time: ___  |  Completion: Yes / No / Partial  |  Aided: Yes / No
Time on task: ___  |  Error count: ___

Hesitations (where?):
Navigation path taken:
Verbatim quotes (exact words in quotes):
"                                                "
"                                                "
Behavioral observations:
Severity of issues observed: 1 / 2 / 3 / 4

TASK 2: _______________________
[repeat above structure]

SESSION-LEVEL OBSERVATIONS:
Mental model (how they think it works):
Repeated struggles:
Moments of delight or surprise:
Unprompted feature requests:
SUS score (post-session): ___
Post-session ease rating (1–7): ___
```

---

## 8. Pre-Test Checklist

*Complete before first session.*

- [ ] Prototype/product accessible and tested on target device
- [ ] Recording consent obtained (separate from participation consent)
- [ ] Test environment set up (quiet room, secondary mic if remote)
- [ ] Task scenarios finalized (no UI element names, open-ended)
- [ ] SUS survey configured and link tested
- [ ] Pilot session completed (1 session to catch protocol issues)
- [ ] Backup participants scheduled (1–2 extra for no-shows)
- [ ] Observers briefed: no talking, no helping, no reactions visible to participant
- [ ] Note-taking template ready for each session

---

## 9. Findings Summary Template

*Fill after all sessions are complete.*

**Test summary:**
- Participants: N = ___  |  Sessions: ___ moderated + ___ unmoderated
- Overall task success rate: ___%  |  SUS score: ___

**Severity distribution:**
- Critical: ___ issues
- Major: ___ issues
- Minor: ___ issues
- Cosmetic: ___ issues

**Top 3 findings:**
1. *(Finding — evidence — severity — recommendation)*
2. 
3. 

**Decision recommendation:** *(Ship as-is / Ship with minor fixes / Redesign before launch)*

---

# PART B — EXTENDED SECTIONS
*(Add for deeper analysis or structured reporting.)*

## B1. Session-by-Session Issue Log

| Issue | Task | Participant(s) | Severity | Quote / Evidence | Recommendation |
|---|---|---|---|---|---|
| | | | | | |

*Keep one running log across all sessions. Don't analyze session by session — look for patterns across all.*

---

## B2. Synthesis Process (Post All Sessions)

**Step 1: Affinity mapping**
1. Write one observation per sticky note
2. Group by theme (not by heuristic — by user behavior)
3. Name each cluster with a behavioral insight: "Users look for [X] before [Y]"
4. Count frequency: How many sessions mention this?

**Step 2: Priority matrix**
```
       FREQUENCY (3+ sessions)
         |
    HIGH | P1 Critical  | P2 High
         |              |
SEVERITY |______________|__________
         |              |
    LOW  | P3 Medium    | P4 Low
         |              |
```

**Step 3: Actionable recommendations**
- Not: "Users found the interface confusing"
- Yes: "3 of 5 users couldn't locate 'Save' — button uses same color as background. Recommendation: Increase contrast to 4.5:1 minimum."

**Step 4: Link to business impact**
- "This affects X% of checkout flows = estimated $Y revenue impact if fixed"

---

## B3. Full Test Report Structure

```
1. Executive Summary (1 page)
   - What was tested, N=X participants, key metric
   - Top 3 findings
   - Decision: Ship / Revise / Redesign

2. Methodology (1 page)
   - Research questions, participant profile, tasks, metrics

3. Findings by Task (main body)
   - Per task: success rate, avg time, error count, blockers, quotes

4. Severity Matrix (1 page)
   - Visual grid of all issues by severity

5. Recommendations (1 page)
   - Prioritized list: P1 (fix before launch), P2 (next sprint), P3 (backlog)

6. Appendices
   - Full session notes
   - SUS scores per participant
   - Task scripts
   - Participant demographics
```

---

## B4. Moderated Session Script (Opening)

```
"Thanks for joining. I'm [name]. We're testing [product area] — 
not testing you, testing the design. There are no right or wrong answers.

As you work, please think out loud — tell me what you're looking for, 
what's confusing, what you expect to happen. If you go quiet, I'll 
ask what you're thinking.

I won't be able to answer questions about the interface — that's 
intentional, so we can see what happens when you're on your own.

Is it OK if I record this session for our internal notes? 
[Get consent.]

Ready to start? Let me give you the first scenario."
```

**During sessions — non-directive prompts:**
- "What are you thinking right now?"
- "What would you expect to happen if you did that?"
- "What were you looking for there?"
- Never: "You're doing great" / "That's correct" / "You should try..."

---

## B5. Remote Testing Setup Checklist

- [ ] Quiet room, closed door, no interruptions
- [ ] Camera on (for emotional cues)
- [ ] Secondary microphone for clear audio
- [ ] Participant has backup phone if internet fails
- [ ] Test recording 10 min before session
- [ ] Second observer in session (silent, camera off)
- [ ] Participant confirmed: computer, browser, screen share enabled
