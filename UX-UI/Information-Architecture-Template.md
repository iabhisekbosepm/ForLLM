# Information Architecture Template — Reusable

> **How to use this template**
> Two tiers in one place:
> - **PART A — Core IA**: Required for every information architecture project. Always fill this.
> - **PART B — Extended Sections**: Add for content audits, card sorting studies, tree testing, or SEO IA optimization.
>
> **Rules of thumb**
> - Good IA is invisible. Users find what they need without thinking about the structure.
> - Organize by user perspective, not organizational structure. "Marketing Campaigns" (org) → "Run Campaigns" (user goal).
> - Test before building. Card sorting and tree testing cost $500–1K. Rebuilding navigation costs 10×.
> - Max 3 levels deep. Every additional level doubles the cognitive load and halves task completion.
> - IA and navigation are NOT the same. IA is the strategic structure; navigation is the UI implementation of that structure.
> - Delete this instruction block and italic *guiding prompts* once filled.
>
> **IA vs. Navigation**
> | IA | Navigation |
> |---|---|
> | Strategic, structural layer | Tactical, interface layer |
> | "How content is organized" | "How users move through it" |
> | Decided first | Designed to support IA |
> | Long-term; changes rarely | Ephemeral; can be redesigned |

---

# PART A — CORE IA
*(Always fill this in.)*

## 1. Project Metadata

| Field | Value |
|---|---|
| **Project name** | |
| **Product / Site** | |
| **IA scope** | Full site / Specific section / New feature only |
| **Owner** | |
| **Stakeholders** | *(Product, Marketing, Content, Engineering, SEO…)* |
| **Status** | Discovery / Draft IA / Validation / Approved / Live |
| **Version** | v0.1 |
| **Last updated** | YYYY-MM-DD |
| **Links** | *(Site map Figma, card sort results, tree test results, analytics)* |

---

## 2. IA Objectives

**Business goal:** *(What does the business need this IA to achieve?)*

**User goal:** *(What do users need to find or accomplish?)*

**Trigger for this IA work:**
- [ ] New product / section launch
- [ ] Content has grown significantly (> 40% new content)
- [ ] Task completion rates < 60% in tree testing or analytics
- [ ] Business strategy changed
- [ ] High bounce rates from main categories
- [ ] Navigation restructure / redesign

**Success metrics:**
| Metric | Current | Target |
|---|---|---|
| Task completion rate (tree test) | | > 75% |
| Findability (direct nav vs. search %) | | |
| Time to find content (avg. clicks) | | < 3 clicks to any content |
| Search abandonment rate | | |
| Bounce rate from category pages | | < 40% |

---

## 3. User Research Foundation

*IA decisions must be grounded in how users think, not how the organization thinks.*

**User mental models:**
- *(How do users think about this domain? What categories make sense to them?)*
- *(Where does user vocabulary differ from internal/org vocabulary?)*
- *(Research source: interviews / card sort / search analysis)*

**User vocabulary vs. internal vocabulary:**

| What users say | What org calls it | Use in IA | Notes |
|---|---|---|---|
| *(e.g., "Settings")* | "Manage Resources" | "Settings" | User language wins |
| | | | |

**Information-seeking behavior:**
- Do users primarily navigate or search? *(analytics data)*
- What are the top 10 search queries? *(reveals navigation gaps)*
- Where do users currently get lost? *(analytics: exit pages, search after navigation)*

---

## 4. Site Map / Navigation Structure

*The core IA artifact. Build visually in Figma or Lucidchart — this section documents the decisions.*

### Primary Navigation (Top Level)

*Max 5–9 items. More = cognitive overload. Scan time doubles with each additional item.*

| # | Label | User-Centered Rationale | Content under this node | Owner |
|---|---|---|---|---|
| 1 | | *(Why this label? What user goal does it serve?)* | | |
| 2 | | | | |
| 3 | | | | |

### Secondary Navigation (Level 2)

| Parent | Child Label | Rationale | Content |
|---|---|---|---|
| | | | |

### Tertiary Navigation (Level 3 — add only if necessary)

*Caution: Level 3 = 3 clicks minimum to reach content. Validate with tree test before building.*

| Level 2 Parent | Level 3 Label | Rationale |
|---|---|---|
| | | |

### Utility / Global Navigation

| Item | Type | Location | Notes |
|---|---|---|---|
| Search | Utility | Header — global | |
| Account / Login | Utility | Header — right | |
| Help / Support | Utility | Header or footer | |
| *(Legal / Compliance)* | Footer | Footer | |

### Breadcrumb Strategy

| Scenario | Breadcrumb Format | When to Use |
|---|---|---|
| Deep content page | Home > Category > Subcategory > Page | All pages > level 2 |
| Tool / app | *(Component breadcrumbs)* | Context-specific |
| Linear flow | Progress indicator instead | Checkout, onboarding |

---

## 5. Taxonomy & Labeling System

*Clear labels = users find things. Jargon labels = users get lost.*

### Labeling Principles

1. **Use user vocabulary** — test labels with card sorting
2. **Front-load keywords** — important word first ("Billing & Payments" not "Manage Your Billing")
3. **Be specific** — "Case Studies" not "Resources"
4. **Consistent across all sections** — same concept = same word everywhere

### Controlled Vocabulary

| Concept | Approved Label | Forbidden Labels | Notes |
|---|---|---|---|
| *(e.g., User account)* | "Account" | "Profile," "Portal," "Hub" | |
| *(e.g., Buying something)* | "Purchase" | "Procure," "Acquire" | |
| | | | |

### Taxonomy: Content Classification

| Primary Category | Secondary Categories | Content Types | Rules |
|---|---|---|---|
| | | | |

**Multi-dimensional classification:**
- Can a piece of content belong to multiple categories? *(Yes/No — document rules)*
- How are cross-links handled? *(canonical home + related links)*

---

## 6. Search Design

**Search scope:** *(What is searchable? All content / specific types / specific sections)*

**Search behavior:**
- Autocomplete: *(Yes/No — if yes, source: common queries / taxonomy labels / both)*
- Spell correction: *(Yes/No)*
- Results ranking: *(Keyword / Semantic / Hybrid — document logic)*
- Filters on results: *(By date / type / category / author)*

**"No results" handling:**
- Show: related terms, spelling suggestions, browseable categories
- Never: just "No results found" with no recovery path

**Search analytics:** *(Where are search queries logged? Who reviews them? What % of users search before/after navigation?)*

---

## 7. IA Decisions Log

*Document why you made each major structural decision. This prevents "why did we do it this way?" six months later.*

| Date | Decision | Options Considered | Chosen Option | Rationale | Evidence / Research | Owner |
|---|---|---|---|---|---|---|
| YYYY-MM-DD | *(e.g., 7 vs. 5 primary categories)* | | | | | |
| | | | | | | |

---

## 8. Wayfinding Strategy

*How do users know where they are and how to get where they want to go?*

| Wayfinding Element | Implementation | Notes |
|---|---|---|
| **Active state** | Current page highlighted in nav | Persistent across all pages |
| **Breadcrumbs** | Show on pages > level 1 | Current page is not linked |
| **Page titles** | H1 matches nav label exactly | No "Creative" H1 if nav says "Blog" |
| **Related links** | "See also" section within content | Cross-links by topic/task |
| **Section headers** | Visible section identity | Consistent placement |
| **Back to X** | Contextual return link | After detail view, return to list |

---

# PART B — EXTENDED SECTIONS

## B1. Content Inventory

*Complete audit of all existing content before redesigning IA.*

| Content ID | Title | Type | URL / Location | Owner | Status | Last Updated | Action |
|---|---|---|---|---|---|---|---|
| C001 | | Blog post | | | Active / Outdated / Archive | | Keep / Update / Archive / Delete |

**Summary:**
- Total content items: ___
- Active and current: ___
- Outdated (needs update): ___
- Duplicate (needs consolidation): ___
- Archive (low traffic, no longer relevant): ___
- Delete (wrong audience, wrong product): ___

---

## B2. Content Gap Analysis

| Needed Topic | Current Coverage | Priority | Proposed IA Location | Owner |
|---|---|---|---|---|
| | None / Partial / Full | High / Med / Low | | |

---

## B3. Card Sorting Study

### Open Card Sort (Use to DISCOVER taxonomy)

- **When:** Before designing IA — discover how users naturally group content
- **Sample size:** 15–30 participants
- **Process:** Users create their own groups + name them
- **Output:** Frequency tables, affinity diagram → identify natural categories
- **Success signal:** 70%+ agreement on main categories

### Closed Card Sort (Use to VALIDATE taxonomy)

- **When:** After designing IA draft — test fit of proposed structure
- **Sample size:** 20–40 participants
- **Process:** Users sort cards into your predefined categories
- **Success metric:** > 75% placement accuracy per category
- **Red flag:** < 60% accuracy for a category → label or concept is unclear

### Card Sort Results Summary

| Category | # Cards Sorted Here | Expected | Accuracy | Action |
|---|---|---|---|---|
| | | | % | Keep / Rename / Restructure |

---

## B4. Tree Testing

*Test navigation structure with text-only tree — before any visual design.*

- **When:** After IA draft; before design starts
- **Tool:** Optimal Workshop, UserTesting, or prototype
- **Sample size:** 20–40 participants
- **Metric:** Task completion rate > 75% per task = valid structure
- **Red flag:** < 60% = redesign that branch

**Test tasks:**

| Task # | Scenario | Expected Location | Completion Rate | Directness Rate | Issues |
|---|---|---|---|---|---|
| T1 | | | | | |

**Tree test findings:**

| Label / Node | Problem Identified | Recommendation |
|---|---|---|
| | Too few / too many users navigate here | Rename / Move / Split |

---

## B5. SEO-IA Alignment

*IA structure directly affects search engine discoverability.*

| IA Decision | SEO Implication | Action |
|---|---|---|
| Category page labels use user language | Matches search intent | Use target keywords in category names |
| Related content grouped under same category | Builds topical authority | Ensure breadth + depth per topic cluster |
| URL structure reflects IA hierarchy | `/products/shoes/running/` | URLs must match IA depth |
| Internal linking follows IA hierarchy | Page authority flows correctly | Pillar page → supporting content links |

**Topic clusters for this IA:**

| Pillar Page | Supporting Content | Internal Links |
|---|---|---|
| | | |

---

## B6. Common IA Failures & Remedies

| Failure | Symptom | Fix |
|---|---|---|
| **Deep hierarchy** | > 3 clicks to reach most content | Flatten; use faceted navigation for complex sets |
| **Org-centric labels** | Users don't recognize category names | User research → user vocabulary → rename |
| **Orphaned content** | Pages with no navigation path | Audit; add to category or archive |
| **No cross-links** | Related content isolated | Map related topics; add "See also" sections |
| **Mobile afterthought** | Desktop IA forced onto mobile | Progressive disclosure; mobile-optimized patterns |
| **Inconsistent taxonomy** | Same content type named differently in different sections | Single taxonomy with governance; document rules |
| **Search replacing navigation** | > 50% of users search for navigable content | Navigation gaps; add to primary/secondary nav |
| **Too many primary items** | > 9 top-level categories | Consolidate; use progressive disclosure |
