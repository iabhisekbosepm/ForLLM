# Design System Component Spec Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core Spec**: Required for every component in the design system. Always fill this.
> - **PART B — Extended Sections**: Add for platform-specific implementations, complex animation specs, or multi-theme support.
>
> **Rules of thumb**
> - Prefer semantic HTML over ARIA. `<button>` beats `<div role="button">` every time.
> - Document ALL states — not just the default. Missing states = inconsistent implementations across the product.
> - Use design tokens, never hardcoded values. Hardcoded values break theming and dark mode.
> - Link to live Storybook example. Written specs alone are ambiguous — visual components demand visual references.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **Spec quality checklist (before publishing)**
> - [ ] Anatomy diagram with labeled measurements and token references
> - [ ] All state combinations documented (default × all variants)
> - [ ] ARIA attributes table complete
> - [ ] Keyboard navigation matrix filled
> - [ ] Design tokens mapped (not hardcoded values)
> - [ ] Responsive breakpoint changes documented
> - [ ] "When not to use" section written

---

# PART A — CORE SPEC
*(Always fill this in.)*

## 1. Component Overview

| Field | Value |
|---|---|
| **Component name** | *(e.g., Primary Button)* |
| **Component ID** | *(e.g., button-primary — machine-readable, kebab-case)* |
| **Type** | Atom / Molecule / Organism |
| **Status** | Draft / Beta / Stable / Deprecated |
| **Version** | v2.1 |
| **Owner** | *(Design Systems team / specific designer)* |
| **Last updated** | YYYY-MM-DD |
| **Links** | *(Figma component, Storybook, GitHub, design tokens)* |

**One-sentence description:** *(What this component does and when it appears)*

---

## 2. Component Anatomy

*Create a labeled diagram in Figma with measurements. This section documents the structure.*

| Part | Name | Type | Optional? | Notes |
|---|---|---|---|---|
| 1 | *(e.g., Label text)* | Text | No | Max 50 chars; truncate with ellipsis |
| 2 | *(e.g., Leading icon)* | Icon slot | Yes | 24×24px; left-aligned; 8px gap to label |
| 3 | *(e.g., Loading spinner)* | Component | Yes | Appears only in loading state |
| 4 | *(e.g., Background)* | Shape | No | Border radius from `--radius-md` token |

**Layout:** *(Describe internal layout — flexbox, grid, inline)*

**Overflow behavior:** *(How does the component handle long text, narrow containers?)*

---

## 3. Variants & States Matrix

*Document ALL combinations. Every blank cell = implementation ambiguity.*

### Visual Variants (Style Options)

| Variant | Description | Token Reference | When to Use |
|---|---|---|---|
| Primary | High-emphasis action | `--color-btn-primary-bg` | One per page; most important action |
| Secondary | Medium-emphasis | `--color-btn-secondary-bg` | Supporting actions |
| Danger | Destructive actions | `--color-btn-danger-bg` | Delete, remove, irreversible actions |
| Ghost | Low-emphasis | Transparent background | Tertiary actions; toolbar buttons |

### Interactive States (per variant)

*For each state, document: background, text color, border, shadow, cursor, opacity.*

| State | Background | Text | Border | Shadow | Cursor | Notes |
|---|---|---|---|---|---|---|
| **Default** | `--color-btn-primary-bg` | `--color-btn-primary-text` | None | `--shadow-none` | pointer | |
| **Hover** | `--color-btn-primary-hover` | | | `--shadow-sm` | pointer | 150ms ease-out transition |
| **Active / Pressed** | `--color-btn-primary-active` | | | | pointer | 100ms, scale 0.98 |
| **Focus** | *(same as default)* | | 3px `--color-focus` outline | | pointer | Focus ring offset: 2px |
| **Disabled** | `--color-btn-primary-bg` at 50% | | | | not-allowed | `aria-disabled="true"`; no click handler |
| **Loading** | *(same as default)* | 50% opacity | | | not-allowed | Spinner replaces icon; `aria-busy="true"` |
| **Error** | *(same as danger variant)* | | | | | *(if applicable to this component)* |

### State × Variant Matrix

*Confirm all combinations are designed.*

| | Primary | Secondary | Danger | Ghost |
|---|---|---|---|---|
| Default | ✓ | ✓ | ✓ | ✓ |
| Hover | ✓ | ✓ | ✓ | ✓ |
| Active | ✓ | ✓ | ✓ | ✓ |
| Focus | ✓ | ✓ | ✓ | ✓ |
| Disabled | ✓ | ✓ | ✓ | ✓ |
| Loading | ✓ | ✓ | ✗ (N/A) | ✗ (N/A) |

---

## 4. Props & Parameters

| Prop | Type | Default | Required | Description | Valid Values |
|---|---|---|---|---|---|
| `variant` | string | `'primary'` | No | Visual style | `'primary' \| 'secondary' \| 'danger' \| 'ghost'` |
| `size` | string | `'md'` | No | Button size | `'sm' \| 'md' \| 'lg'` |
| `disabled` | boolean | `false` | No | Disable interaction | `true \| false` |
| `loading` | boolean | `false` | No | Show loading spinner | `true \| false` |
| `icon` | ReactNode | `undefined` | No | Leading icon element | Any icon component |
| `iconOnly` | boolean | `false` | No | Icon without label | `true \| false` |
| `fullWidth` | boolean | `false` | No | Stretch to container | `true \| false` |
| `onClick` | function | `undefined` | No | Click handler | `(e: MouseEvent) => void` |
| `ariaLabel` | string | `undefined` | Conditional | Accessible label | Required if `iconOnly=true` |
| `type` | string | `'button'` | No | HTML button type | `'button' \| 'submit' \| 'reset'` |

**Constraint rules:**
- `loading=true` automatically sets `disabled` behavior (no click, no hover)
- `iconOnly=true` requires `ariaLabel` — will warn in console if missing
- `fullWidth` is ignored on `iconOnly` variant
- `type='submit'` only for buttons inside `<form>` elements

**Content guidelines:**
- Label: 1–4 words preferred; max 50 characters; always start with verb
- Icons: Max 24×24px; must have accessible meaning independent of label
- CTA copy: "Save" not "Will Save"; "Delete" not "Remove this item"

---

## 5. Usage Guidelines

### When to Use

- The single most important action on a page or section
- Triggering a form submission
- Navigating to a destination that requires immediate action
- High-confidence, irreversible actions (with Danger variant)

### When NOT to Use

| Scenario | Use Instead |
|---|---|
| Navigation to another page | `<a>` link component |
| Secondary / tertiary action that doesn't need emphasis | Secondary or Ghost variant |
| More than 2 Primary buttons on the same screen | Reduce to 1; others become Secondary |
| Inline text action | Link component |
| Toggle that stays toggled | Toggle component with `aria-pressed` |

### Hierarchy on a Page

```
[Primary Button] — One maximum per section
  [Secondary Button] — Supporting action
    [Ghost / Text Button] — Tertiary actions
```

---

## 6. Accessibility

### ARIA Specifications

| Attribute | Value | When Applied |
|---|---|---|
| `role` | `"button"` (implicit on `<button>`) | Always |
| `aria-disabled` | `"true"` | When `disabled=true` |
| `aria-busy` | `"true"` | When `loading=true` |
| `aria-label` | Descriptive text | When `iconOnly=true` or label is ambiguous |
| `aria-pressed` | `"true" \| "false"` | For toggle buttons only |
| `type` | `"button"` | Must be explicit to prevent form submit |

### Keyboard Navigation

| Key | Behavior |
|---|---|
| `Tab` | Focus button |
| `Enter` | Activate button |
| `Space` | Activate button |
| `Escape` | Cancel if in an open dropdown/menu triggered by this button |

**Focus management:** When button triggers a modal, focus moves to modal. When modal closes, focus returns to triggering button.

### Color Contrast

| State | Foreground | Background | Ratio | Required |
|---|---|---|---|---|
| Default | `--color-btn-primary-text` | `--color-btn-primary-bg` | ≥ 4.5:1 | WCAG AA |
| Hover | | | ≥ 4.5:1 | |
| Disabled | | 50% opacity | N/A | Must look visually distinct |
| Focus ring | `--color-focus` | Any background it appears on | ≥ 3:1 | WCAG AA |

### Touch Targets

- Minimum size: 44×44px (WCAG 2.5.5)
- Small variant minimum: 44px height (padding compensates for smaller text)
- Spacing between adjacent buttons: ≥ 8px

---

## 7. Design Tokens

| Property | Token | Value | Notes |
|---|---|---|---|
| Background (primary) | `--color-btn-primary-bg` | `#0066CC` | |
| Background (hover) | `--color-btn-primary-hover` | `#005BB5` | |
| Text (primary) | `--color-btn-primary-text` | `#FFFFFF` | |
| Border radius | `--radius-md` | `6px` | |
| Padding (sm) | `--space-xs` `--space-sm` | `4px 8px` | |
| Padding (md) | `--space-sm` `--space-md` | `8px 16px` | |
| Padding (lg) | `--space-md` `--space-lg` | `12px 24px` | |
| Font size (md) | `--type-body-sm` | `14px/1.5` | |
| Transition | `--motion-standard` | `150ms ease-out` | |
| Focus ring | `--color-focus` | `#0066CC` | |
| Focus ring width | `--border-focus` | `3px` | |
| Shadow (hover) | `--shadow-sm` | `0 2px 4px rgba(0,0,0,0.1)` | |

---

## 8. Responsive Behavior

| Breakpoint | Change | Notes |
|---|---|---|
| Mobile (< 480px) | `sm` size default; `fullWidth` if primary CTA | Thumb-friendly |
| Tablet (480–768px) | Standard behavior | No change |
| Desktop (≥ 768px) | Standard behavior; hover effects active | |

**Hover effects:** Disable on touch devices (no hover state on mobile)

---

# PART B — EXTENDED SECTIONS

## B1. Motion & Animation Specs

| Transition | Duration | Easing | Properties |
|---|---|---|---|
| Hover enter | 150ms | `ease-out` | `background-color`, `box-shadow` |
| Hover exit | 100ms | `ease-in` | `background-color`, `box-shadow` |
| Active press | 100ms | `cubic-bezier(0.4, 0, 1, 1)` | `transform: scale(0.98)` |
| Focus ring appear | Instant | — | `outline` |
| Loading spinner | 1s infinite | `linear` | `transform: rotate(360deg)` |

```css
@media (prefers-reduced-motion: reduce) {
  .button { transition: none; animation: none; }
}
```

---

## B2. Code Implementation

**HTML:**
```html
<button
  class="button button--primary button--md"
  type="button"
  aria-label="Save changes"
>
  <span class="button__icon" aria-hidden="true"><!-- icon --></span>
  <span class="button__label">Save</span>
</button>
```

**CSS naming (BEM):**
```
.button                 → base component
.button--primary        → variant modifier
.button--md             → size modifier
.button--loading        → state modifier
.button__icon           → icon subcomponent
.button__label          → label subcomponent
```

---

## B3. Dark Mode & Theming

| Token | Light Value | Dark Value |
|---|---|---|
| `--color-btn-primary-bg` | `#0066CC` | `#4DA3FF` |
| `--color-btn-primary-text` | `#FFFFFF` | `#000000` |
| `--color-btn-primary-hover` | `#005BB5` | `#66B2FF` |

---

## B4. Changelog

| Version | Date | Change | Migration |
|---|---|---|---|
| v2.1 | YYYY-MM-DD | Added `loading` prop | Replace manual spinner implementation |
| v2.0 | YYYY-MM-DD | Renamed `type` to `variant` | `type="primary"` → `variant="primary"` |
| v1.0 | YYYY-MM-DD | Initial release | — |
