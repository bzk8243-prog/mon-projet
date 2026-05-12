# Lonage SEO Blogging Structure Masterplan (Sitemap-Driven Framework)

> Scope: SEO blogging structure only (taxonomy, clusters, internal linking, future publishing ops).  
> Constraint noted: direct sitemap fetch from this environment is blocked by a 403 proxy tunnel response, so this plan is built to preserve all existing indexed URLs and be executable immediately once URLs are exported from WordPress/Rank Math.

## 1) Category & Cluster Detection Model

Use current ecosystem taxonomy as the canonical cluster backbone:

1. Menopause
2. Healthy Aging
3. Fitness
4. Women’s Wellness
5. Recovery
6. Nutrition
7. Sleep
8. Gut Health
9. Mobility
10. Longevity

### Cluster rules
- Each article must map to exactly **1 primary ecosystem**.
- Each article may map to up to **2 secondary ecosystems** for cross-linking.
- Each ecosystem should have:
  - 1–3 pillar/hub URLs (prefer existing URLs)
  - 4–8 cluster subtopics
  - 12+ supporting articles over time

## 2) Orphan Article Identification Protocol

Because preserving indexed URLs is mandatory, orphan handling is link-first (no slug edits, no URL replacements):

### Orphan definition
A published indexable URL with **0 contextual internal inlinks** from other published indexable posts.

### Detection workflow
1. Export all published post URLs + categories from WordPress.
2. Crawl internal links (Screaming Frog / Rank Math analytics export).
3. Join datasets in `SEO Blogger/orphan-audit/lonage-orphan-audit.csv`.
4. Mark URL as:
   - `orphan` (0 inlinks)
   - `weak` (1 inlink)
   - `supported` (2+ inlinks)

### Recovery SLA
- Orphan: add 4 links within 7 days.
- Weak: add 2 links within 14 days.
- Supported: monitor only.

## 3) Pillar/Cluster Architecture (Separated Menopause vs General Ecosystems)

## A. Menopause Ecosystem (Ring-fenced)
**Pillars (priority):**
- menopause-symptoms-guide
- perimenopause-guide
- menopause-lifestyle-guide

**Clusters:**
- symptoms by stage
- sleep disruption
- weight/metabolism changes
- training adaptation during menopause
- mood/stress support
- recovery and energy management

**Linking boundary rule:**
- Menopause pages must link mostly within menopause cluster first.
- Cross-links to non-menopause ecosystems capped at 2 contextual links/article.

## B. Non-Menopause Health/Fitness Ecosystem (Parallel graph)
Sub-ecosystems remain independent but cross-connected:
- Fitness ↔ Recovery ↔ Mobility
- Nutrition ↔ Gut Health
- Sleep ↔ Recovery
- Healthy Aging ↔ Longevity
- Women’s Wellness as a bridge layer (excluding core menopause intent pages)

## 4) Internal Linking Opportunities (Scalable Pattern)

Apply this link block per article:
- 1 link up to parent pillar
- 2 links sideways to siblings in same cluster
- 1 link forward to next-step article
- 1 selective cross-ecosystem link

### Anchor text standard
- 60% partial-match descriptive anchors
- 30% natural language anchors
- 10% exact-match anchors

### Priority order for retrofitting links
1. Orphan URLs
2. URLs ranking positions 4–20
3. High-impression / low-CTR URLs
4. Newly published URLs (<30 days)

## 5) Indexed URL Preservation Rules

Non-negotiables:
- Keep all indexed URL slugs unchanged.
- Keep existing category slugs unchanged.
- Do not merge/delete indexed posts unless redirected with 1:1 topical match.
- New authority should be built via net-new hubs, supporting articles, and internal links.

## 6) Rank Math SEO Recommendations (WordPress Execution)

### Global settings
- Enable primary category breadcrumbs.
- Enforce one primary focus keyword + 2 secondary phrases per post.
- Add schema type by intent:
  - Informational guides: `Article`
  - How-to workflows: `HowTo` (where valid)
  - Hub pages: `WebPage` + FAQ blocks when helpful

### On-page checklist
- SEO title includes topic + benefit + lifecycle qualifier when relevant.
- Meta description includes audience + expected outcome.
- H1 mirrors core intent; H2 tree mirrors cluster entities.
- Add at least 4 internal links (using block above).
- Image alt text aligned to section intent (not keyword stuffing).

### Menopause-specific Rank Math rules
- Add menopause lifecycle qualifiers (peri/meno/post) in metadata where medically relevant.
- Reinforce E-E-A-T: author bio, reviewed-by fields, source citations.

## 7) Future Publishing Workflow

1. **Intent selection:** choose ecosystem + cluster + stage-of-journey intent.
2. **SERP mapping:** define primary query + 3 entity-supporting subqueries.
3. **Outline build:** include pillar link target + 2 sibling targets before drafting.
4. **Draft writing:** solve single intent deeply, avoid mixed-intent cannibalization.
5. **Rank Math pass:** metadata, schema, keyword placement, readability.
6. **Linking pass:** apply 1-up / 2-sideways / 1-forward / 1-cross rule.
7. **Publish + index checks:** confirm canonical, sitemap presence, indexability.
8. **14-day refresh:** adjust intro CTR copy + add one new contextual internal link.

## 8) Scalable Topical Authority Map (Operating Model)

### Tier structure
- **Tier 1:** Pillar hubs (broad intent)
- **Tier 2:** Cluster guides (mid-intent)
- **Tier 3:** Supporting answers (long-tail intent)
- **Tier 4:** Conversion/support assets (newsletter lead magnets, checklists)

### Quarterly growth target per ecosystem
- +1 pillar improvement cycle
- +3 cluster articles
- +6 supporting articles
- +1 refresh sprint for old content

### KPI stack
- Crawl depth to key pillars ≤ 3 clicks
- Orphan rate < 3%
- Avg internal links per post ≥ 4
- 90-day growth in ranking keywords for each ecosystem

## 9) Execution Files Created

- `SEO Blogger/orphan-audit/lonage-orphan-audit.csv`
- `SEO Blogger/content-clusters/lonage-pillar-cluster-map.csv`
- `SEO Blogger/workflows/lonage-future-publishing-workflow.md`

Populate these from WordPress + Rank Math exports to operationalize this system without changing indexed URLs.
