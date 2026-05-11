# Lonage Menopause Internal Linking System

This document defines the internal linking system for Lonage’s menopause pillar/cluster architecture.

## 1) Scope

Applies only to menopause content and supporting health & fitness pages that directly strengthen menopause topical authority.

---

## 2) Content Roles

- **Pillar page:** broad, high-authority guide targeting a core menopause topic.
- **Cluster page:** focused article targeting a subtopic under one pillar.
- **Sibling cluster page:** another cluster page under the same pillar.

---

## 3) Pillar-to-Cluster Linking Rules

1. Every pillar must link to all core cluster pages in its section.
2. Each pillar should include a “Related menopause guides” block near the middle and end.
3. Prioritize links to:
   - highest-traffic clusters,
   - highest-conversion educational clusters,
   - recently updated clusters.
4. Use descriptive, intent-matching anchors (avoid generic “click here”).
5. Keep link destinations indexable (no orphan drafts, no noindex targets).

**Minimum target:** 6–12 contextual links from pillar to cluster pages, depending on pillar length.

---

## 4) Cluster-to-Pillar Linking Rules

1. Every cluster article must include at least one contextual link to its parent pillar in the first 40% of the article.
2. Include one additional pillar link near conclusion when natural.
3. Link should reinforce hierarchy language (e.g., “complete menopause guide”).
4. If the article has a quick-answer intro, add a pillar link in the “learn more” sentence.

**Minimum target:** 1 required + 1 optional contextual link to parent pillar.

---

## 5) Sibling Article Linking Rules (Cluster-to-Cluster)

1. Each cluster should link to 2–5 sibling clusters where intent overlap is useful.
2. Prioritize sibling links by:
   - journey sequence (symptom → solution → routine),
   - semantic proximity,
   - high-exit pages needing deeper navigation.
3. Place at least one sibling link above midpoint.
4. Avoid overlinking: if links do not improve user next-step clarity, do not add them.

---

## 6) Anchor Text Recommendations

### Anchor Format
- Prefer natural-language phrase anchors (3–8 words).
- Match anchor intent to target page intent.
- Vary anchors across pages to avoid repetitive exact matches.

### Recommended Mix (per target URL across site)
- **40%** partial-match descriptive anchors
- **30%** natural topical phrase anchors
- **20%** exact-match keyword anchors (max)
- **10%** branded/generic supportive anchors

### Avoid
- Repeating exact keyword anchor in every source article
- Non-descriptive anchors (“here”, “this page”) without context

---

## 7) Orphan Article Detection

An article is considered an orphan if:
- it has **0 internal inlinks** from indexable site pages, or
- it is only linked from taxonomy pages with no contextual body links.

### Detection SOP
1. Export all menopause URLs from WordPress.
2. Crawl with an SEO crawler (or internal script) to collect internal inlinks.
3. Flag URLs with 0 contextual inlinks.
4. Assign each orphan to a parent pillar.
5. Add:
   - 1 link from parent pillar,
   - 2 links from relevant sibling clusters,
   - 1 reciprocal link back to pillar.
6. Re-crawl and verify inlink count > 0.

---

## 8) Rank Math SEO Recommendations (Internal Linking + On-Page)

1. Set one primary focus keyword per article aligned to the assigned cluster intent.
2. Add 2–4 secondary keywords tied to menopause subtopic variants.
3. Ensure SEO title and H1 align with primary intent (without keyword stuffing).
4. Use Rank Math content analysis as guidance, not a hard target at the expense of readability.
5. Validate:
   - slug clarity,
   - meta description with intent + benefit,
   - heading hierarchy (H2/H3 topical flow),
   - image alt text relevance,
   - schema type suitability.
6. Confirm internal links include:
   - parent pillar link,
   - sibling cluster links,
   - at least one link from older menopause article into the new piece where relevant.

---

## 9) Link Quality Guardrails

- Link only when destination resolves the next user question.
- Keep medical framing careful and non-diagnostic unless clinically sourced.
- Update outdated anchors when article positioning changes.
- Do not inject links that break sentence flow.

---

## 10) Monthly Internal Linking Audit Cadence

- Review top menopause pillars and clusters every month.
- Fix orphan and weakly connected pages first.
- Refresh links on decaying pages before rewriting full content.
- Track before/after metrics: impressions, average position, CTR, pages/session.
