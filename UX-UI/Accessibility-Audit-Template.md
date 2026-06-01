# Accessibility Audit Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Audit**: The essential WCAG 2.1 AA checklist and issue log. Always complete this.
> - **PART B — Extended Sections**: Add for detailed ARIA specs, form audits, motion testing, or remediation planning.
>
> **Rules of thumb**
> - Automated tools catch only ~35% of issues. Always follow with manual keyboard + screen reader testing.
> - Severity 4 issues are launch blockers. No exceptions.
> - Accessibility is built in from design — not bolted on in QA.
> - Re-audit every 6 months minimum; re-test after any major redesign.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **Testing protocol order**
> 1. Automated scan (axe, WAVE, Lighthouse) — 30 min
> 2. Keyboard navigation (tab through everything) — 30 min
> 3. Screen reader (NVDA on Windows / VoiceOver on Mac) — 60 min
> 4. Visual assessment (zoom, contrast, motion, high contrast mode) — 30 min
> 5. Mobile/touch testing — 30 min

---

# PART A — CORE AUDIT
*(Always complete this.)*

## 1. Audit Metadata

| Field | Value |
|---|---|
| **Audit ID** | *(e.g., ACC-2024-06-Checkout)* |
| **Product / Feature** | |
| **Scope** | *(Full site / Specific flow / New feature)* |
| **Compliance target** | WCAG 2.1 AA |
| **Audit date** | YYYY-MM-DD |
| **Auditor(s)** | |
| **Tools used** | *(axe, WAVE, Lighthouse, NVDA, VoiceOver, Accessibility Insights…)* |
| **Test environment** | *(Browser versions, OS, screen reader versions)* |
| **Status** | In Progress / Complete |
| **Overall result** | Pass / Conditional Pass / Fail |

---

## 2. Executive Summary

**Issue counts:**
- Critical (Severity 4 — launch blockers): ___
- Major (Severity 3 — high priority): ___
- Moderate (Severity 2 — medium priority): ___
- Minor (Severity 1 — cosmetic): ___
- **Total:** ___

**Top 3 critical findings:**
1. *(Issue — impact — location)*
2. 
3. 

**Launch recommendation:** *(Approved / Conditional — fix X before launch / Blocked)*

---

## 3. WCAG 2.1 AA Compliance Matrix

### Perceivable

| Criterion | Status | Notes |
|---|---|---|
| **1.1 Text Alternatives** — Alt text on all images; `alt=""` for decorative | ✓ / ✗ / Partial | |
| **1.2 Captions & Transcripts** — Captions for video, transcripts for audio | ✓ / ✗ / N/A | |
| **1.3 Adaptable** — No loss of info at 200% zoom; content reflows correctly | ✓ / ✗ / Partial | |
| **1.4.1 Use of Color** — Color alone not used to convey info | ✓ / ✗ / Partial | |
| **1.4.3 Contrast (Text)** — 4.5:1 normal text; 3:1 large text (18pt+ or 14pt+ bold) | ✓ / ✗ / Partial | |
| **1.4.4 Resize Text** — No loss of function at 200% text size | ✓ / ✗ / Partial | |
| **1.4.11 Non-text Contrast** — 3:1 for UI components and graphical objects | ✓ / ✗ / Partial | |
| **1.4.12 Text Spacing** — No loss of content when spacing adjusted | ✓ / ✗ / Partial | |

### Operable

| Criterion | Status | Notes |
|---|---|---|
| **2.1.1 Keyboard** — All functionality available via keyboard | ✓ / ✗ / Partial | |
| **2.1.2 No Keyboard Trap** — Users can navigate away from any component | ✓ / ✗ / Partial | |
| **2.4.1 Skip Blocks** — Skip link to main content exists and works | ✓ / ✗ / Partial | |
| **2.4.3 Focus Order** — Logical, intuitive tab order | ✓ / ✗ / Partial | |
| **2.4.4 Link Purpose** — Link text describes destination | ✓ / ✗ / Partial | |
| **2.4.6 Headings & Labels** — Descriptive headings and labels | ✓ / ✗ / Partial | |
| **2.4.7 Focus Visible** — Visible focus indicator on all interactive elements | ✓ / ✗ / Partial | |
| **2.5.3 Label in Name** — Accessible name contains visible label text | ✓ / ✗ / Partial | |

### Understandable

| Criterion | Status | Notes |
|---|---|---|
| **3.1.1 Language** — `lang` attribute on `<html>`; language changes marked | ✓ / ✗ / Partial | |
| **3.2.1 On Focus** — No unexpected context change on focus | ✓ / ✗ / Partial | |
| **3.3.1 Error Identification** — Errors clearly identified; not color-only | ✓ / ✗ / Partial | |
| **3.3.2 Labels & Instructions** — Explicit `<label>` associations; clear instructions | ✓ / ✗ / Partial | |
| **3.3.3 Error Suggestion** — Error messages suggest how to fix | ✓ / ✗ / Partial | |

### Robust

| Criterion | Status | Notes |
|---|---|---|
| **4.1.1 Parsing** — Valid HTML; no duplicate IDs | ✓ / ✗ / Partial | |
| **4.1.2 Name, Role, Value** — ARIA implemented correctly; states update | ✓ / ✗ / Partial | |
| **4.1.3 Status Messages** — Status messages programmatically determined | ✓ / ✗ / Partial | |

---

## 4. Issue Registry

*One row per unique issue. Sort by severity.*

| ID | Title | WCAG Criterion | Severity | Location / Screenshot | Affected Users | Recommendation | Owner | Status |
|---|---|---|---|---|---|---|---|---|
| ACC-001 | | | 4 / 3 / 2 / 1 | | | | | Open |
| ACC-002 | | | | | | | | |

---

## 5. Severity Definitions

| Severity | Definition | Fix Timeline |
|---|---|---|
| **4 — Critical (Launch Blocker)** | Completely prevents a user from completing a task | Fix immediately; no launch until resolved |
| **3 — Major** | Significant impact on usability; workaround is painful or unclear | Fix before launch or within 1 week |
| **2 — Moderate** | Noticeable issue; workaround exists | Fix within 1 month |
| **1 — Minor** | Cosmetic only; no functional impact | Backlog; fix if time allows |

---

## 6. Color Contrast Audit

*Test all text, interactive elements, and graphical objects.*

| Element | Foreground | Background | Ratio | Required | Status |
|---|---|---|---|---|---|
| Body text | `#hex` | `#hex` | X:1 | 4.5:1 | ✓ / ✗ |
| Heading text | | | | 4.5:1 | |
| Link text | | | | 4.5:1 | |
| Link hover | | | | 4.5:1 | |
| Button text | | | | 4.5:1 | |
| Button border | | | | 3:1 | |
| Input border | | | | 3:1 | |
| Focus indicator | | | | 3:1 | |
| Error message | | | | 4.5:1 | |
| Disabled (special) | | | | N/A (must look inactive) | |
| *(Dark mode — if applicable)* | | | | | |

---

## 7. Keyboard Navigation Audit

*Tab through the entire interface with mouse disabled.*

| Component | Expected Behavior | Actual Behavior | Status |
|---|---|---|---|
| Skip link | First element; jumps to `<main>` | | ✓ / ✗ |
| Navigation links | Tab to navigate; Enter to activate | | |
| Buttons | Tab to focus; Enter or Space to activate | | |
| Form inputs | Tab to focus; type to enter | | |
| Dropdowns | Tab to open; Arrow keys to navigate; Enter to select | | |
| Modals | Focus trapped inside; Escape to close; focus restored on close | | |
| Radio groups | Arrow keys to switch between options | | |
| Checkboxes | Space to toggle; Tab to navigate | | |
| Carousels / sliders | Arrow keys to navigate; auto-play can be paused | | |

**Focus indicator quality:**
- Visible: ✓ / ✗
- Contrast ≥ 3:1 against all backgrounds: ✓ / ✗
- Minimum size (2px+): ✓ / ✗
- Consistent across all elements: ✓ / ✗

---

## 8. Screen Reader Testing

*Test with NVDA (Windows) + VoiceOver (Mac) minimum.*

| Element | Expected Announcement | NVDA Result | VoiceOver Result | Status |
|---|---|---|---|---|
| Page title | Announced on load | | | |
| Headings | "Heading level X: [text]" | | | |
| Links | Link purpose from text or aria-label | | | |
| Buttons | Label + state | | | |
| Form fields | Label + required + type | | | |
| Images | Alt text or "image" (decorative) | | | |
| Error messages | Announced live (aria-live) | | | |
| Modals | Title announced; close action clear | | | |
| Icon-only buttons | aria-label providing purpose | | | |

---

## 9. Touch Target Size Audit

*Minimum 44×44px for all interactive elements.*

| Element | Actual Size | Min Required | Status |
|---|---|---|---|
| Primary buttons | | 44×44px | ✓ / ✗ |
| Navigation links | | 44×44px | |
| Form inputs (height) | | 44px tall | |
| Checkboxes | | 44×44px | |
| Close buttons | | 44×44px | |
| Icon-only buttons | | 44×44px | |
| Spacing between targets | | ≥ 8px | |

---

# PART B — EXTENDED SECTIONS

## B1. ARIA Implementation Review

*Check for correct ARIA usage. Prefer semantic HTML over ARIA.*

**ARIA preference hierarchy:**
```
<button>       > <div role="button">
<a href>       > <div role="link">
<nav>          > <div role="navigation">
<form>         > <div role="form">
<fieldset>     > <div role="group">
```

**Common ARIA issues to check:**

| Issue | Anti-Pattern | Fix |
|---|---|---|
| Missing button label | `<button>✕</button>` (icon only) | `<button aria-label="Close dialog">✕</button>` |
| Wrong aria-hidden | `<button aria-hidden="true">` | Remove aria-hidden from focusable elements |
| Missing expanded state | Toggle button with no state | `aria-expanded="false"` toggled to `true` on open |
| No live region | Dynamic content updates silently | `aria-live="polite"` on status messages |
| Redundant aria-label | `<button aria-label="Save">Save</button>` | Remove redundant label; visible text is sufficient |

---

## B2. Form Accessibility Audit

| Field Type | Requirement | Status |
|---|---|---|
| Text inputs | `<label for="id">` linked to `<input id="id">` | ✓ / ✗ |
| Checkboxes | Label wraps or associated via `for` | |
| Radio groups | `<fieldset><legend>` wraps the group | |
| Required fields | `aria-required="true"` + visual indicator | |
| Error states | `aria-invalid="true"` + `aria-describedby="error-id"` | |
| Error messages | Specific text — not "Invalid input" | |
| Format hints | Shown before submission, not just on error | |

---

## B3. Motion & Animation Audit

| Element | Current Behavior | With prefers-reduced-motion | Status |
|---|---|---|---|
| Page transitions | | Instant / removed | |
| Hover animations | | Minimal or removed | |
| Loading animations | | Static or simple pulse | |
| Autoplay carousels | | Manual only | |
| Parallax effects | | Disabled | |
| `scroll-behavior: smooth` | | `scroll-behavior: auto` | |

**CSS implementation:**
```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
  html { scroll-behavior: auto; }
}
```

---

## B4. Remediation Roadmap

| Priority | Issues | Fix Timeline | Owner | Status |
|---|---|---|---|---|
| **P0 — Before launch** | All Severity 4 | 24–72 hours | | |
| **P1 — Sprint 1** | Severity 3 | 1–2 weeks | | |
| **P2 — Next month** | Severity 2 (high frequency) | 2–4 weeks | | |
| **P3 — Backlog** | Severity 1 + 2 (low frequency) | Future sprint | | |

**30-day follow-up:** Verify all P0/P1 fixes are working with the same testing tools. Document in "Fixed" column.
