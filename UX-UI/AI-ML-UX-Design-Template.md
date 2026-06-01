# AI/ML Feature UX Design Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core AI/ML UX**: Required for every AI feature. Covers loading, errors, transparency, feedback loops.
> - **PART B — Extended Patterns**: Add for conversational UI, multi-turn flows, agents, domain-specific AI types.
>
> **How this fits with the PRD**
> The PRD (Section B6) covers the *technical* side of AI features: model selection, evaluation metrics, safety guardrails. This template covers the *UX* side: how users interact with, perceive, and trust the AI. They reference each other but don't overlap.
>
> **Rules of thumb**
> - Design for uncertainty. AI is not deterministic — every state must handle the case where the AI is wrong, slow, or unavailable.
> - Trust is fragile. One unexplained hallucination can permanently reduce a user's trust. Design for calibrated trust — not over or under.
> - Always have a fallback. If the AI fails, users must have a manual path. No feature should be blocked by AI unavailability.
> - Never hide AI involvement. Disclose upfront or contextually — not burying it in terms of service.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **AI type quick selector**
> | AI Type | Key UX Concerns | Primary Sections |
> |---|---|---|
> | Generative text (LLM) | Streaming, hallucination, regeneration | A3, A4, A5, B1 |
> | Classification / Tagging | Confidence display, quick override | A2, A5, B3 |
> | Recommendations | Acceptance patterns, personalization | A5, B3 |
> | RAG / Search augmentation | Citations, source quality | A5, A6, B4 |
> | Agents (action-taking) | Approval gates, audit log, rollback | A4, B5 |
> | Conversational UI | Turn management, context, history | B1, B2 |

---

# PART A — CORE AI/ML UX
*(Always fill this in.)*

## 1. Feature Metadata

| Field | Value |
|---|---|
| **Feature name** | |
| **AI type** | Generative text / Classification / Recommendation / RAG / Agent / Conversational / Other |
| **Owner** | |
| **Links** | *(PRD with B6 section, design specs, model eval doc, Figma)* |
| **Status** | Concept / Design / Build / Live |
| **Last updated** | YYYY-MM-DD |

---

## 2. AI Capability & Confidence Model

*Define the boundaries before designing the UI. What can the AI reliably do — and what can't it?*

**What this AI reliably does:**
- *(Be specific — "summarizes documents up to 10,000 tokens" not "understands text")*

**What it cannot do** *(hard limits)*:
- 
- 

**Failure modes specific to this feature:**
| Failure Mode | Probability | User Impact | UX Response |
|---|---|---|---|
| Hallucination / incorrect output | | | Show confidence signal; link to source |
| Low confidence / uncertain result | | | Show "uncertain" badge; offer regeneration |
| No result / out of scope | | | "I couldn't find this" + guidance |
| Timeout / API failure | | | Retry with backoff; fallback path |
| Rate limit / service down | | | Queue or graceful degradation |
| Input rejected (safety filter) | | | Why rejected + what to try instead |

**Confidence thresholds:**
| Score | Display | Action |
|---|---|---|
| > 0.85 | High confidence — show result | |
| 0.60–0.85 | Show result with caveat | Add "uncertain" indicator |
| < 0.60 | Low confidence — degrade gracefully | Offer manual alternative |

---

## 3. Loading States & Progressive Output

*AI latency is different from regular loading. Users need honest timing signals.*

| Scenario | Duration | Loading Pattern | User Experience |
|---|---|---|---|
| Instant | 0–100ms | No indicator needed | Instant result |
| Short | 100ms–1s | Spinner or skeleton | Feels responsive |
| Medium | 1–3s | Skeleton + "Thinking…" label | Show content shape |
| Long | 3–10s | Progress indicator + time estimate | "~5 seconds remaining" |
| Very long | 10s+ | "Still working…" + cancel option | User must be able to cancel |

**Progressive text streaming** *(for generative text features)*:
- Render text incrementally as tokens arrive — don't wait for full response
- Show cursor/blinking indicator to signal active generation
- Allow user to cancel mid-stream (stop generation)
- If streaming, show partial result — partial is better than waiting

**Skeleton loader specs:**
- Match the shape of the expected content (not a generic spinner)
- Skeleton color: use neutral gray (not brand color — avoids false positive impression)
- Animate with subtle pulse — respect `prefers-reduced-motion`

**Loading state copy:**
- Avoid: "Loading…" (generic)
- Prefer: "Analyzing your document…" / "Finding matches…" / "Writing your summary…"

---

## 4. Error States & Failure Handling

*Every failure mode must have a specific UX response. "Something went wrong" is not acceptable.*

| Error Type | User-Facing Message | Recovery Action | Tone |
|---|---|---|---|
| **Hallucination / wrong answer** | "This response may contain errors. Verify before using." | Show sources; offer regeneration | Honest, not alarmist |
| **Low confidence** | "I'm not certain about this — here are my best guesses." | Confidence badge; regenerate option | Transparent |
| **No result** | "I couldn't find anything matching your request." | Suggest how to refine; offer manual path | Helpful |
| **Input too long** | "Your input is too long. Try shortening to [X] words." | Character counter; trim suggestion | Constructive |
| **Input rejected (safety)** | "I can't help with that request. Try asking about [alternative]." | Guidance on reformulation | Clear, non-judgmental |
| **Timeout** | "This is taking longer than expected. [Retry] or [Do manually]" | Retry button; fallback action | Honest |
| **Service unavailable** | "AI features are temporarily unavailable. You can [do X manually] in the meantime." | Clear manual path | Honest; never hide AI downtime |
| **Rate limited** | "You've reached your limit. [Upgrade] or try again in [time]." | Upgrade path or timer | Non-punishing |

**Design rule:** AI errors must be distinct from system errors. Don't use the same red error state for "database down" and "AI returned uncertain result." These are different situations requiring different responses.

---

## 5. AI vs. Human Content Attribution

*Users must know what was generated by AI vs. what was written by a human or verified by a system.*

**Disclosure triggers:**
- Always disclose when: content is entirely AI-generated, AI made a decision, AI took an action
- Contextual disclosure: AI-assisted suggestions, completions, recommendations
- Minimum: visible indicator on hover or adjacent to content

**Attribution patterns:**
| Content Type | Visual Treatment | Text Label |
|---|---|---|
| Fully AI-generated | Badge / colored border | "AI-generated" |
| AI-assisted (human edited) | Subtle indicator | "Written with AI" |
| AI suggestion (not yet accepted) | Ghost text / suggestion chip | "Suggested by AI" |
| Verified / human-reviewed | Checkmark indicator | "Verified" |
| Citations / sources (RAG) | Inline footnote or hover | "[Source]" or "Based on: [title]" |

---

## 6. Transparency & Trust Signals

*Trust is built through honesty, not by hiding AI limitations.*

**Disclosure format:**
- Upfront: "This feature uses AI. It may occasionally make mistakes." *(first use or onboarding)*
- Contextual: Confidence badge next to each result
- On-demand: "Why did AI suggest this?" link or tooltip

**What to disclose:**
- [ ] That AI is involved (who / what is generating this)
- [ ] Data cutoff or knowledge limits ("Based on data as of [date]")
- [ ] Known limitations for this feature
- [ ] How user feedback is used (will this train the model?)
- [ ] For high-stakes actions: human review option or approval gate

**Trust calibration — design for neither extreme:**

| Over-trust risk | Under-trust risk |
|---|---|
| Users treat all AI output as fact | Users ignore all AI suggestions |
| Fix: Show confidence + citations | Fix: Default to showing results; easy accept pattern |
| Fix: Require verification for high-stakes | Fix: Show examples of AI succeeding |

---

## 7. User Feedback Loop

*Every AI feature needs a feedback mechanism to improve quality and build trust.*

**Feedback options (choose appropriate level):**

| Feedback Type | Effort | When to Use | Implementation |
|---|---|---|---|
| Thumbs up / thumbs down | Low | All AI responses | Icon buttons adjacent to result |
| Explicit correction | Medium | When accuracy matters | "That's wrong — here's correct" input |
| Regenerate | Low | Generative content | "Regenerate" / "Try again" button |
| Not helpful | Low | Recommendation systems | "Not helpful" / "Show less like this" |

**Feedback UX rules:**
- Don't ask for feedback on every response — sample or offer in settings
- Acknowledge feedback: "Thanks — we'll use this to improve"
- If feedback changes future behavior, show it: "We've updated your recommendations"
- Don't use feedback data for model training without explicit consent disclosure

---

## 8. Empty States for AI Features

| State | When | UX Response |
|---|---|---|
| **First use / cold start** | No history, no context | Show example prompts; explain what AI can help with |
| **No results** | AI found nothing | Explain why; suggest how to refine query |
| **Cleared history** | User cleared conversation | Confirmation + undo option; fresh start CTA |
| **AI feature disabled** | User opted out or not yet available | Explain why; show manual alternative |
| **Waiting for data** | Model needs more context to be useful | Show what data helps improve results |

---

## 9. Prompt Input Design

*(For features with user-facing text input — search, chat, generation prompts)*

**Input field specs:**
- Placeholder: Show example prompt, not just "Type here…"
- Label: Always visible label (not placeholder-only — fails accessibility)
- Character / token limit: Show counter when approaching limit
- Format support: Document if markdown, code blocks, or attachments are supported
- Submit behavior: Enter to submit vs. button (document clearly; match user mental model)
- Multiline: Allow Shift+Enter for line breaks if Enter submits

**Input accessibility:**
- `<label>` visible and associated with input
- `aria-describedby` for hint text and format guidance
- `aria-live` on character counter for screen reader announcement

---

# PART B — EXTENDED AI/ML UX PATTERNS

## B1. Conversational UI Patterns

*Use when the feature involves multi-turn back-and-forth with the AI.*

**Turn structure:**
- User message → AI response → Pause (user initiates next)
- Never auto-advance to next question without user action

**Context management:**
| Scenario | Design Response |
|---|---|
| Context window limit reached | Show warning: "This conversation is getting long — start fresh for best results" |
| User wants to start over | "New conversation" button; confirm loss of history |
| User edits a past message | Show fork / branch clearly; "Regenerating from this point…" |
| Long session (30+ turns) | Option to summarize or export conversation |

**History sidebar:**
- Auto-generate conversation titles from first message
- Group by date (Today / Yesterday / Last 7 Days)
- Search within conversation history
- Delete conversation with confirmation

---

## B2. AI Feature Onboarding

*Progressive disclosure — don't explain everything upfront.*

| Moment | Onboarding Content | Format |
|---|---|---|
| First launch | "What is this AI? What can it help with?" | Modal or inline callout |
| Before first use | Example prompts (good + bad) | Inline examples in empty state |
| After first error | "What went wrong + how to improve" | Inline guidance |
| After successful use | Skip or subtle celebration | Toast or inline |
| Power user (10+ uses) | Show advanced features | Tooltip or discovery prompt |

**Example prompts format:**
- Show 3–4 real example prompts users can click to try
- Label them: "Summarize a document" / "Find similar cases" / "Draft an email"
- Update examples based on user's context or role

---

## B3. Patterns by AI Type

**Classification / Tagging (e.g., email spam, content categorization)**
- Show category + confidence: "Likely spam · 87%"
- Quick override: "Not spam" removes from category, trains filter
- Settings to adjust sensitivity: "Filter strictly" / "Be lenient"
- Bulk action: "Mark all as [category]"

**Recommendations (e.g., Copilot, GitHub suggestions)**
- Show top N suggestions with confidence-ranked ordering
- Accept with Tab / shortcut key (muscle memory)
- Cycle suggestions: Arrow keys to see alternatives
- "Not helpful" removes type from future suggestions
- Track acceptance rate as design quality metric

**RAG / Search augmentation**
- Show both: retrieved source documents AND AI synthesis
- Citation format: hover = see source excerpt, click = open source
- Source quality indicators: verified vs. user-generated vs. external
- Two separate confidence signals: "retrieval confidence" + "synthesis confidence"

---

## B4. Trust Calibration Checklist

*Run this checklist before any AI feature ships.*

**Over-trust prevention:**
- [ ] Confidence score or indicator visible on results
- [ ] Citations or sources linked for factual claims
- [ ] "Verify before using" notice for high-stakes outputs
- [ ] Human approval gate for irreversible actions (email send, file delete, etc.)
- [ ] "AI can make mistakes" disclosure in onboarding or adjacent to results

**Under-trust prevention:**
- [ ] AI results visible by default (not hidden behind "Show AI" toggle)
- [ ] Accept pattern is easy and fast (Tab, click, or one button)
- [ ] Success examples shown during onboarding
- [ ] Feedback loop shows AI improving over time
- [ ] Error messages don't catastrophize ("may contain errors" not "WARNING: AI ERROR")

---

## B5. Agentic AI UX (Action-Taking AI)

*Use when the AI takes actions on behalf of the user (sends emails, modifies files, calls APIs).*

**Core principle:** Show what the AI plans to do BEFORE it does it. Require human approval for any irreversible action.

**Pre-action preview:**
```
The AI will:
1. Retrieve the Q3 sales data from your CRM
2. Generate a summary report (3-5 pages)
3. Send it to: [recipients]

[Approve] [Edit] [Cancel]
```

**Action audit log:**
- Timestamped log of all AI actions
- "Undone by user" flag if applicable
- Export / download log option

**Rollback capability:**
- For reversible actions: "Undo" button within [time window]
- For irreversible: Require explicit double-confirmation + show consequences

**Error in agent flow:**
- Stop the sequence; never auto-proceed past an error
- Show exactly where it failed and why
- Offer: Retry from failure point / Skip step / Cancel entire sequence

---

## B6. AI UX Anti-Patterns

| Anti-Pattern | Why It Fails | Fix |
|---|---|---|
| No loading state | User thinks nothing happened | Always show feedback within 100ms |
| "Something went wrong" for AI errors | Unhelpful; no recovery path | Specific error + specific recovery action |
| Hallucination without signals | User treats fiction as fact | Confidence indicator + citations always |
| No fallback if AI unavailable | Feature completely blocked | Manual alternative must always exist |
| Feedback black hole | User rates, nothing changes | Acknowledge feedback; show it influencing results |
| Unclear AI involvement | User doesn't know AI generated this | Disclose upfront or contextually — always |
| Over-promising capability | "AI will always get this right" | Set realistic expectations in onboarding |
| No permissions/context awareness | AI suggests based on data user can't see | Only surface AI suggestions from data the user can access |
| Agent auto-proceeds past errors | Data corruption or partial actions | Always stop on error; require human decision |
| Streaming text that can't be stopped | User trapped reading unwanted output | Cancel / Stop button always visible during generation |

---

## B7. AI UX Metrics

| Metric | Definition | Target | What It Signals |
|---|---|---|---|
| Adoption rate | % eligible users who try AI feature | Depends on context | Feature discoverability + trust |
| Frequency (DAU/WAU) | How often users return | Upward trend | Feature value + habit forming |
| Thumbs up ratio | Positive / total feedback | > 70% | Output quality |
| Correction rate | % results user explicitly corrects | < 10% | Model accuracy |
| Abandonment after error | % who give up after first error | < 20% | Error recovery UX quality |
| Generation latency (P95) | Time from request to first token | < 2s | Perceived responsiveness |
| Fallback usage rate | % sessions that use manual fallback | < 5% | AI reliability |
| Acceptance rate (recommendations) | % suggestions accepted | > 30% | Suggestion relevance |
