# Menopause Cluster — SAFE Internal Linking Implementation Plan (No URL Changes)

## Scope & Safety Constraints
- This plan follows the Lonage internal-linking system and preserves all existing indexed URLs, slugs, categories, and permalink paths.
- This is a planning document only: **no publishing**, **no auto-implementation**, and **no URL edits**.
- Execution should occur via controlled editorial updates in WordPress drafts first, then QA, then manual publish approval.

---

## Source Alignment Used for This Plan
- Lonage menopause linking structure (A–F cluster model, pillar/cluster/sibling requirements).
- Lonage menopause internal linking rules (top-40% pillar link, sibling quotas, orphan recovery).
- Lonage WordPress implementation roadmap phases (link quotas, orphan recovery lifecycle).

---

## Objectives for the Menopause Cluster
1. Strengthen hierarchical authority flow from each menopause pillar to assigned cluster articles.
2. Ensure every menopause cluster article reinforces its parent pillar.
3. Improve depth and session continuity through sibling links.
4. Reduce or eliminate menopause orphans using deterministic inlink recovery.

---

## SAFE Implementation Framework

### Phase 0 — Pre-Implementation Controls (Required)
1. Export current menopause URL inventory and baseline link graph (inlinks/outlinks) from crawler + WordPress list.
2. Freeze URL structure rules for the sprint:
   - no slug edits,
   - no category changes,
   - no permalink updates.
3. Build/update a menopause linking tracker table with fields:
   - URL,
   - parent pillar,
   - has pillar link (Y/N),
   - current sibling links,
   - missing sibling links,
   - orphan status,
   - editor status,
   - QA status.
4. Work only in draft/revision mode until QA sign-off.

---

## Implementation Workstreams

### 1) Pillar-to-Article Linking Plan

#### Target state
- Each menopause pillar links to all core child cluster articles in its section.
- Per pillar, maintain a contextual link count target of ~6–12 menopause cluster links (scaled to content length).

#### Safe actions
1. Add/refresh a “Related menopause guides” block in each pillar (mid-content + near end where natural).
2. Ensure every assigned A–F child article appears at least once contextually from the parent pillar.
3. Prioritize missing links by:
   - highest traffic opportunity,
   - highest conversion/intent pages,
   - recently updated pages.
4. Use natural, intent-matched anchors (avoid repetitive exact-match anchors).

#### QA gates
- No links to non-indexable/noindex/draft URLs.
- No footer-only bulk linking as the only placement.
- Anchor text remains readable in sentence flow.

---

### 2) Article-to-Pillar Linking Plan

#### Target state
- Every menopause cluster article includes:
  - **1 required contextual link** to its parent pillar in the first ~40% of body content,
  - **+1 optional** pillar link near conclusion where relevant.

#### Safe actions
1. For each A1–F5 article, add parent pillar link in an explanatory sentence (“complete guide” framing).
2. If article includes a short answer intro, place a “learn more in our complete guide” style link there.
3. Standardize hierarchy language to strengthen pillar relevance without keyword stuffing.

#### QA gates
- Parent pillar URL must match assigned cluster mapping.
- No forced/awkward anchor insertion.
- Maintain medical framing guardrails and non-diagnostic tone.

---

### 3) Sibling Article Linking Plan

#### Target state
- Each menopause cluster article links to **2–4 (up to 5 where strongly relevant)** sibling articles in the same cluster.
- At least one sibling link appears above the article midpoint.

#### Safe actions
1. Use A–F sibling matrix model to pre-assign recommended sibling destinations.
2. Add links by journey sequence (symptom → explanation → routine → solution).
3. Place a “Related menopause articles” contextual block near end to support continuation.
4. Keep links selective: do not add links that do not answer a likely next-step question.

#### QA gates
- Avoid overlinking and repetitive anchors to the same target across many sources.
- Keep anchor mix varied (partial-match and natural topical phrasing favored).
- Ensure sibling links are cluster-relevant (avoid random cross-topic jumps).

---

### 4) Orphan Article Reduction Plan

#### Orphan definition
- Menopause article with zero contextual inlinks from published/indexable pages, or only taxonomy/archive links.

#### Recovery package (per orphan)
1. Add 1 contextual inlink from assigned parent pillar.
2. Add 2 contextual inlinks from relevant sibling cluster posts.
3. Add 1 reciprocal link from orphan back to parent pillar.
4. Add/update related-reading block within orphan article.
5. Re-crawl and confirm orphan cleared (>0 contextual inlinks).

#### Prioritization/SLA
- High-value menopause orphan: recovery within 3 business days.
- Standard menopause orphan: recovery within 7 business days.

---

## Suggested Rollout Sequence (Low-Risk)
1. **Wave 1 (Foundation):** Pillar pages only (add missing child links).
2. **Wave 2 (Hierarchy):** Add required article→pillar links across A–F.
3. **Wave 3 (Depth):** Implement sibling links in high-priority clusters first.
4. **Wave 4 (Recovery):** Resolve detected orphans using recovery package.
5. **Wave 5 (Stabilization):** Re-crawl, QA, and patch exceptions.

---

## Operational Tracker Schema (for the menopause plan)
Recommended columns:
- cluster_code
- article_code
- article_url
- parent_pillar_url
- has_pillar_link_top40 (Y/N)
- has_pillar_link_conclusion (Y/N)
- required_sibling_urls
- current_sibling_links
- missing_sibling_links
- pillar_inlinks_count
- contextual_inlinks_count
- orphan_status
- anchor_variants_used
- editor_status (To Do / In Progress / Done)
- qa_status (Pending / Pass / Rework)
- last_updated

---

## QA Checklist for Safe Approval (Pre-Publish)
For each updated article/pillar draft:
1. URL unchanged.
2. Parent pillar mapping correct.
3. Required pillar link present in top 40% (article pages).
4. Sibling links meet target and are contextually relevant.
5. Anchor text is natural, varied, and not over-optimized.
6. No broken links / no noindex targets.
7. Readability and clinical framing intact.
8. Tracker row updated.

---

## Success Metrics (30/60/90 Day Monitoring)
- % menopause articles with required article→pillar link.
- Avg sibling link count per menopause cluster article.
- # menopause orphans before vs after.
- Internal inlinks growth on priority cluster URLs.
- Engagement proxy: pages/session or next-page path improvements for menopause content.

---

## Explicit Non-Goals (This Task)
- No URL restructuring.
- No taxonomy redesign.
- No automated publishing.
- No bulk auto-insertion scripts.
- No live implementation in this step.
