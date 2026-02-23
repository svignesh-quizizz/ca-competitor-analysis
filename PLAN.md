# Competitor Research Plan: Pear Assess & Formative

## Objective
Research how **Pear Assess** (formerly Edulastic) and **Formative** (GoFormative) handle:
1. **Mastery Tracker Reports** — tracking student mastery of standards/skills
2. **Standards Growth Tracker Reports** — tracking growth over time on standards

## Research Dimensions (for both products)
- Feature set & capabilities
- UI/UX design patterns
- Data visualizations (charts, graphs, color coding)
- Report formats & layouts
- Filtering/grouping options
- Standards alignment methods
- Export/sharing capabilities

## Scope Strategy
Start narrow (pages directly about mastery tracking, standards growth, standards-based reporting), then expand to adjacent topics (progress monitoring, skill tracking, learning objectives, standard-based grading) if insufficient content is found.

## Output Format
Each subagent produces a structured markdown file with:
- Findings organized by research dimension
- Inline references to screenshot image URLs found on the pages
- Direct quotes from documentation where relevant
- Links to all source pages

## Directory Structure
```
ca-competitor-analysis/
├── pear-assess/
│   ├── resource-center/
│   │   ├── screenshots/       # Image URLs & descriptions
│   │   └── research.md        # Agent 1 output
│   └── help-center/
│       ├── screenshots/       # Image URLs & descriptions
│       └── research.md        # Agent 2 output
├── formative/
│   ├── resource-center/
│   │   ├── screenshots/       # Image URLs & descriptions
│   │   └── research.md        # Agent 3 output
│   └── help-center/
│       ├── screenshots/       # Image URLs & descriptions
│       └── research.md        # Agent 4 output
└── PLAN.md
```

---

## Subagent Plan (4 agents, all Sonnet, run in parallel)

### Agent 1: Pear Assess — Resource Center
**Goal:** Research Pear Assess's resource center (blog posts, webinars, case studies, product announcements) for content related to mastery tracking and standards growth reporting.

**Steps:**
1. WebSearch for "Pear Assess resource center", "Edulastic resource center", "Pear Assess blog"
2. Find the main resource center / blog URL
3. WebSearch for targeted content:
   - "Pear Assess mastery tracker"
   - "Edulastic mastery report"
   - "Pear Assess standards growth"
   - "Edulastic standards based reporting"
   - "Pear Assess progress monitoring report"
   - "Edulastic student growth tracking"
4. WebFetch each relevant page, extract:
   - Feature descriptions
   - UI screenshots / image URLs
   - Workflow descriptions
   - Any video/webinar references
5. If narrow search yields < 5 relevant pages, expand to:
   - "Pear Assess standards based grading"
   - "Edulastic learning objectives tracking"
   - "Pear Assess skill mastery"
6. Write findings to `pear-assess/resource-center/research.md`
7. Save image URL catalog to `pear-assess/resource-center/screenshots/image-catalog.md`

### Agent 2: Pear Assess — Help Center
**Goal:** Research Pear Assess's help/support documentation for how-to guides, feature docs, and technical details about mastery and standards growth reports.

**Steps:**
1. WebSearch for "Pear Assess help center", "Edulastic help center", "Pear Assess support"
2. Find the main help center URL
3. WebSearch for targeted content:
   - "site:peerassess.com mastery" or similar domain-scoped searches
   - "Pear Assess help mastery report"
   - "Edulastic help standards report"
   - "Pear Assess help growth tracker"
   - "Edulastic help student mastery"
4. WebFetch each help article, extract:
   - Step-by-step instructions
   - Feature configuration options
   - Report field descriptions
   - Filter/grouping options documented
   - Screenshots / image URLs in docs
5. If narrow search yields < 5 relevant pages, expand to:
   - "Pear Assess help reports"
   - "Edulastic help standards"
   - "Pear Assess help assessment data"
6. Write findings to `pear-assess/help-center/research.md`
7. Save image URL catalog to `pear-assess/help-center/screenshots/image-catalog.md`

### Agent 3: Formative — Resource Center
**Goal:** Research Formative's resource center (blog, webinars, case studies) for content related to mastery tracking and standards growth reporting.

**Steps:**
1. WebSearch for "Formative resource center", "GoFormative resource center", "Formative blog"
2. Find the main resource center / blog URL
3. WebSearch for targeted content:
   - "Formative mastery tracker"
   - "GoFormative mastery report"
   - "Formative standards growth"
   - "GoFormative standards based reporting"
   - "Formative progress monitoring"
   - "Formative student growth tracking"
4. WebFetch each relevant page, extract:
   - Feature descriptions
   - UI screenshots / image URLs
   - Workflow descriptions
   - Any video/webinar references
5. If narrow search yields < 5 relevant pages, expand to:
   - "Formative standards based grading"
   - "GoFormative learning objectives"
   - "Formative skill tracking"
   - "Formative data reports"
6. Write findings to `formative/resource-center/research.md`
7. Save image URL catalog to `formative/resource-center/screenshots/image-catalog.md`

### Agent 4: Formative — Help Center
**Goal:** Research Formative's help/support documentation for how-to guides, feature docs, and technical details about mastery and standards growth reports.

**Steps:**
1. WebSearch for "Formative help center", "GoFormative help center", "Formative support"
2. Find the main help center URL
3. WebSearch for targeted content:
   - "Formative help mastery"
   - "GoFormative help standards report"
   - "Formative help growth tracker"
   - "Formative help student mastery"
   - "GoFormative help progress monitoring"
4. WebFetch each help article, extract:
   - Step-by-step instructions
   - Feature configuration options
   - Report field descriptions
   - Filter/grouping options documented
   - Screenshots / image URLs in docs
5. If narrow search yields < 5 relevant pages, expand to:
   - "Formative help reports"
   - "GoFormative help data"
   - "Formative help tracking"
6. Write findings to `formative/help-center/research.md`
7. Save image URL catalog to `formative/help-center/screenshots/image-catalog.md`

---

## Execution Strategy
- All 4 agents run **in parallel** as Sonnet subagents
- Each agent is independent — no cross-dependencies
- Each agent writes its own output files
- After all agents complete, a synthesis step can combine findings

## Limitations & Notes
- **Screenshots:** WebFetch extracts text content and can identify image URLs on pages, but cannot render and capture visual screenshots of live pages. Image URLs found in documentation will be cataloged for manual review.
- **Gated content:** Some resource center content (webinars, gated PDFs) may not be fully accessible via WebFetch. These will be noted with links for manual follow-up.
- **Pear Assess branding:** Pear Assess was formerly known as Edulastic. Searches will use both names to maximize coverage.
- **Formative branding:** Formative is also known as GoFormative. Searches will use both names.
