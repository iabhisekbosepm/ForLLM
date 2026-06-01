# Design Handoff Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Handoff**: Required for every feature handoff. Always complete this.
> - **PART B — Extended Sections**: Add for complex interactions, animation specs, or full asset packages.
>
> **Where 70% of project delays happen**
> Missing states, unclear interactions, no error states, wrong asset formats. This template prevents all of them.
>
> **Rules of thumb**
> - Ship no design without all states documented: default, hover, focus, active, disabled, loading, error, empty.
> - Text must be final. No "Lorem ipsum" in handoff. Ever.
> - Developers need exact values, not descriptions. "big button" → "height: 48px; padding: 12px 24px"
> - Every interaction needs: trigger → visual change → duration → easing. Not just "button animates on click."
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **Pre-handoff designer checklist (quick version)**
> - [ ] All states designed (default, hover, focus, active, disabled, loading, error, empty)
> - [ ] All text finalized (no placeholders)
> - [ ] All assets exported and named
> - [ ] Responsive layouts verified at all breakpoints
> - [ ] Accessibility reviewed (contrast, focus indicators, aria-label for icon-only)
> - [ ] Design tokens used (no hardcoded values)
> - [ ] Interactions documented with timing and easing

---

# PART A — CORE HANDOFF
*(Always complete this.)*

## 1. Handoff Metadata

| Field | Value |
|---|---|
| **Feature / Flow** | |
| **Version** | v1.0 |
| **Handoff date** | YYYY-MM-DD |
| **Lead Designer** | |
| **Engineering Lead** | |
| **Stakeholders** | |
| **Status** | Draft / Ready for Dev / In QA / Shipped |
| **Links** | *(Figma file, design system, prototype, Jira/Linear tickets)* |

**Scope summary:**
- **In scope:** *(exact list of screens/components)*
- **Not in scope:** *(explicit list — prevents scope creep)*

**Success criteria:** *(How do we know the implementation is complete and correct?)*

---

## 2. Design Specifications

### Colors

| Token Name | Hex | RGB | CSS Variable | Used Where |
|---|---|---|---|---|
| Primary action | `#0066CC` | `0, 102, 204` | `--color-primary` | Buttons, links |
| Error | `#D93025` | `217, 48, 37` | `--color-error` | Error states |
| *(add all colors used in this feature)* | | | | |

*All colors must reference design tokens. No hardcoded hex values in implementation.*

### Typography

| Token | Font | Weight | Size | Line-height | Letter-spacing | Used Where |
|---|---|---|---|---|---|---|
| `--type-heading-1` | Inter | 700 (Bold) | 48px | 1.2 | -0.5px | Page titles |
| `--type-body-md` | Inter | 400 (Regular) | 16px | 1.5 | 0 | Body copy |
| *(add all text styles used)* | | | | | | |

**Font stack:** `'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`

**Web font loading:** `font-display: swap` *(or specify loading strategy)*

### Spacing & Grid

| Token | Value | Used For |
|---|---|---|
| `--space-xs` | 4px | Icon gaps |
| `--space-sm` | 8px | Tight padding |
| `--space-md` | 16px | Standard padding |
| `--space-lg` | 24px | Section spacing |
| `--space-xl` | 32px | Component separation |
| `--space-2xl` | 48px | Page section gaps |

**Grid:** *(X columns, Y px gutters, Z px edge margins — per breakpoint)*

### Shadows & Elevation

| Token | CSS Value | Used Where |
|---|---|---|
| `--shadow-sm` | `0 1px 2px rgba(0,0,0,0.05)` | Cards, dropdowns |
| `--shadow-md` | `0 4px 6px rgba(0,0,0,0.10)` | Modals, popovers |
| `--shadow-lg` | `0 10px 15px rgba(0,0,0,0.15)` | Drawers, elevated panels |

### Border Radius

| Token | Value | Used Where |
|---|---|---|
| `--radius-sm` | 4px | Tags, badges |
| `--radius-md` | 8px | Buttons, inputs |
| `--radius-lg` | 12px | Cards |
| `--radius-full` | 9999px | Pills, avatars |

---

## 3. Component & State Inventory

*Every component that appears in this feature. Every state that component can be in.*

| Component | States Designed | Figma Frame | Notes |
|---|---|---|---|
| *(e.g., Primary Button)* | Default, Hover, Focus, Active, Disabled, Loading | *(link)* | |
| *(e.g., Email Input)* | Default, Focused, Filled, Error, Disabled | *(link)* | Validation: real-time on blur |
| *(e.g., Dropdown)* | Closed, Open, Hover item, Selected, Disabled | *(link)* | |
| *(e.g., Modal)* | Open, Loading, Error, Success | *(link)* | Focus trap required |

**States checklist for every interactive element:**
- [ ] Default (initial state)
- [ ] Hover (desktop)
- [ ] Focus (keyboard navigation — focus ring visible)
- [ ] Active / Pressed (during click/tap)
- [ ] Disabled (non-interactive)
- [ ] Loading (async operation in progress)
- [ ] Error (validation failure or system error)
- [ ] Empty (no data / first use)
- [ ] Success (action completed)

---

## 4. Responsive Breakpoints

| Breakpoint | Range | Layout Changes | Font Changes | Spacing Changes |
|---|---|---|---|---|
| Mobile | < 480px | Single column; full-width CTAs | H1: 32px; body: 14px | Margins: 16px |
| Tablet | 480–768px | 2-column where applicable | H1: 40px | Margins: 24px |
| Desktop | 768–1024px | Full layout | Standard | Standard |
| Wide | > 1024px | Max-width container | Standard | Standard |

**Per-component responsive notes:**
- *(e.g., "Navigation: hamburger menu below 768px; full nav above")*
- *(e.g., "Data table: scrollable on mobile; full columns on desktop")*

**Mobile-specific:**
- Touch targets: minimum 44×44px
- No hover-only states (touch has no hover)
- Thumb zone: primary CTAs in bottom 60% of screen

---

## 5. Interaction Specifications

*For each interactive element: what triggers the interaction, what changes visually, how long, what easing.*

| Component | Interaction | Trigger | Visual Change | Duration | Easing | Notes |
|---|---|---|---|---|---|---|
| Button | Hover | Mouse enter | Background darkens | 150ms | `ease-out` | |
| Button | Active | Mouse/tap down | scale(0.98) | 100ms | `cubic-bezier(0.4,0,1,1)` | |
| Modal | Open | Button click | Fade in + slide up 8px | 200ms | `ease-out` | Focus moves to modal |
| Modal | Close | Escape / close button | Fade out | 150ms | `ease-in` | Focus returns to trigger |
| Toast | Appear | System event | Slide in from right | 250ms | `ease-out` | Auto-dismiss after 4s |
| Dropdown | Open | Button click | Fade in + scale from 0.95 | 150ms | `ease-out` | |

**Reduced motion:** All transitions must use:
```css
@media (prefers-reduced-motion: reduce) {
  * { transition: none; animation: none; }
}
```

---

## 6. Asset Export Specifications

### Icons

| Export | Format | Sizes | Naming | Notes |
|---|---|---|---|---|
| UI icons | SVG | 24×24 (primary), 16×16, 32×32 | `icon-[name].svg` | Remove fills; use `currentColor` |
| PNG fallback | PNG | 24×24, 48×48 | `icon-[name]-24.png` | For legacy browsers |

**SVG requirements:**
- Use `currentColor` for fill (color applied via CSS)
- ViewBox: `0 0 24 24`
- Remove unnecessary groups and metadata
- Optimize with SVGO (< 2KB per icon)

### Images & Illustrations

| Type | Format | Max Size | Naming | Notes |
|---|---|---|---|---|
| Photos | WebP + PNG fallback | 200KB | `photo-[context].webp` | 1× and 2× variants |
| Illustrations | SVG (vector) or WebP | 100KB | `illustration-[name].webp` | |
| Hero images | WebP | 300KB | `hero-[name]-[breakpoint].webp` | Mobile + Desktop variants |

---

## 7. Accessibility Handoff Notes

| Element | Requirement | ARIA / HTML Notes |
|---|---|---|
| *(Icon-only button)* | `aria-label` required | `<button aria-label="Close dialog">` |
| *(Form inputs)* | Visible `<label>` linked to input | `<label for="email">` + `<input id="email">` |
| *(Error messages)* | Linked to field | `aria-describedby="email-error"` |
| *(Images)* | Alt text specified | See Figma annotations |
| *(Focus order)* | Matches reading order | Tab sequence documented in Figma |
| *(Color contrast)* | All combinations checked | See contrast table below |

**Color contrast summary:**
| Element | Ratio | Pass? |
|---|---|---|
| Body text on white | X:1 | ✓ / ✗ |
| Button text on primary | X:1 | |
| Error text on white | X:1 | |
| Focus ring on background | X:1 | |

---

## 8. Pre-Handoff Checklist (Designer Sign-Off)

**Content & Text**
- [ ] All text finalized — no "Lorem ipsum" or "TBD"
- [ ] Character counts documented (buttons, labels, error messages)
- [ ] Microcopy final: error messages, empty states, loading states, confirmations

**States**
- [ ] Default, Hover, Focus, Active, Disabled, Loading, Error, Empty — all designed
- [ ] States designed for EVERY component variant
- [ ] States visible in Figma (not just implied)

**Responsive**
- [ ] Mobile (< 480px) verified
- [ ] Tablet (480–768px) verified
- [ ] Desktop (≥ 768px) verified
- [ ] No horizontal scrolling at any breakpoint

**Accessibility**
- [ ] Color contrast ≥ 4.5:1 for text, ≥ 3:1 for UI components
- [ ] Focus indicators designed (visible, min 2px)
- [ ] Icon-only buttons have `aria-label` noted in Figma annotations
- [ ] Form labels associated with inputs

**Assets**
- [ ] All icons exported (SVG + PNG fallback)
- [ ] All images exported and optimized
- [ ] Asset naming consistent and documented
- [ ] File sizes within targets

**Design Tokens**
- [ ] All colors from token system (no hardcoded hex)
- [ ] All spacing from token system
- [ ] Typography from token system
- [ ] Shadows from token system

**Interactions**
- [ ] All interactive states documented
- [ ] Hover effects specified (duration + easing)
- [ ] Animations: duration, easing, `prefers-reduced-motion` noted
- [ ] Focus management noted (modals, drawers, after delete)

**Handoff**
- [ ] Figma file organized (pages clear, components linked to library)
- [ ] Dev notes/annotations added to key components
- [ ] Links to design tokens, component library, and this spec doc
- [ ] Engineering lead has reviewed scope and flagged concerns

---

# PART B — EXTENDED SECTIONS

## B1. Animation Library

*Document all animations for this feature.*

| Animation Name | Trigger | Properties | Duration | Easing | Reduced Motion |
|---|---|---|---|---|---|
| Modal enter | Dialog opens | `opacity: 0→1`, `transform: translateY(8px)→0` | 200ms | `ease-out` | Instant |
| Toast appear | Notification fires | `transform: translateX(100%)→0` | 250ms | `ease-out` | Instant |
| Skeleton pulse | Loading | `opacity: 0.5→1` infinite | 1.5s | `ease-in-out` | Static color |

---

## B2. QA Acceptance Criteria

*Engineering completes; designer reviews.*

**Visual accuracy:**
- [ ] Colors match within 1% (verified with color picker)
- [ ] Typography: font size, weight, line-height, letter-spacing exact
- [ ] Spacing/padding: ±1px tolerance
- [ ] Shadows, border-radius exact

**States:**
- [ ] All documented states implemented
- [ ] State transitions feel correct (timing, easing)
- [ ] Focus indicator visible on all interactive elements

**Responsive:**
- [ ] Mobile 375px: single column, correct font sizes
- [ ] Tablet 768px: 2-column where specified
- [ ] Desktop 1024px+: full layout

**Accessibility:**
- [ ] Focus visible on all interactive elements
- [ ] Color contrast passes (verify with axe DevTools)
- [ ] Screen reader: form labels announced, errors announced
- [ ] Keyboard navigation works throughout

**Performance:**
- [ ] Images optimized (below size targets)
- [ ] Animations use GPU-accelerated properties (transform, opacity)
- [ ] No layout thrash from animations

**Design QA sign-off:**
```
Reviewed by (Designer): ___________
Date: ___________
Result: APPROVED / REVISIONS NEEDED
Issues: ___________
```
