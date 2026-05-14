# Lonage Article Inventory & Ecosystem Mapping

## 1. Executive Summary
- Total actual published article files discovered: 2
- Total article briefs discovered: 5
- Pillar content available: 1 detailed menopause pillar guide
- Empty pillar placeholders: 6 (Healthy Aging, Nutrition, Mobility, Sleep, Fitness, Women’s Wellness, Recovery, Gut Health, Longevity)
- Cluster placeholders present but not populated
- Existing internal-linking reports and authority maps are present, but the live article relationship layer is mostly missing

## 2. Scan Results
### Files and content discovered
- `articles/menopause/brain-fog-menopause-article.md`
- `articles/menopause/brain-fog-menopause-article-v2.md`
- `SEO Blogger/article-briefs/menopause/brain-fog-menopause-brief.md`
- `SEO Blogger/article-briefs/menopause/menopause-sleep-fatigue-brief.md`
- `SEO Blogger/article-briefs/menopause/menopause-weight-gain-brief.md`
- `SEO Blogger/article-briefs/nutrition-recovery/best-protein-after-50-brief.md`
- `SEO Blogger/article-briefs/nutrition-recovery/vitamin-d-after-50-brief.md`
- `SEO Blogger/pillars/menopause-pillar.md` (detailed)
- `SEO Blogger/content-clusters/lonage-global-authority-map.md`
- `SEO Blogger/content-clusters/lonage-pillar-cluster-map.csv`

### Architecture state
- Primary ecosystems defined in the authority map: Menopause, Healthy Aging, Fitness, Women’s Wellness, Recovery, Nutrition, Sleep, Gut Health, Mobility, Longevity
- Only Menopause has a real pillar page drafted
- Content cluster files exist as placeholders, but have no article inventory inside them
- No published-article tracking entries were found in the `published-articles.md` file

## 3. Ecosystem Inventory
### Active ecosystem content
| Ecosystem | Primary content | Status |
|---|---|---|
| Menopause | 2 article files + 3 briefs | Active, needs consolidation and linking |
| Nutrition | 2 briefs | Planning stage |
| Sleep | 1 brief placeholder reference | Planning stage |
| Healthy Aging | none | Missing |
| Fitness | none | Missing |
| Recovery | none | Missing |
| Women’s Wellness | none | Missing |
| Gut Health | none | Missing |
| Mobility | none | Missing |
| Longevity | none | Missing |

### Primary ecosystem assignments
- `brain-fog-menopause-article` → Menopause
- `menopause-sleep-fatigue` (planned) → Menopause
- `menopause-weight-gain` (planned) → Menopause
- `best-protein-after-50` (planned) → Nutrition
- `vitamin-d-after-50` (planned) → Nutrition

### Supporting ecosystems
- Menopause articles should support: Sleep, Nutrition, Recovery, Women’s Wellness, Longevity
- Nutrition briefs should support: Healthy Aging, Recovery, Fitness, Menopause
- Sleep content should support: Recovery, Menopause, Longevity

## 4. Cluster Inventory
### Menopause cluster map
- Primary cluster: Menopause symptoms and cognitive support
- Supporting clusters: Menopause sleep disruption, Menopause weight/metabolism
- Pillar relationship: Menopause pillar page
- Status: weak but with a clear base topic; needs sibling articles, internal linking, and a pillar hub

### Nutrition cluster map
- Primary cluster: Protein for 50+ women, Vitamin D for 50+
- Pillar relationship: missing Nutrition pillar page
- Status: weak; article concepts exist only in briefs

### Sleep cluster map
- Primary cluster: Menopause sleep and fatigue
- Pillar relationship: missing Sleep pillar page
- Status: orphaned planning concept

### Missing / empty clusters
- Healthy Aging cluster content: none
- Fitness cluster content: none
- Recovery cluster content: none
- Women’s Wellness cluster content: none
- Gut Health cluster content: none
- Mobility cluster content: none
- Longevity cluster content: none

## 5. Article Relationship Map
### Published content and mapping
| Article | Ecosystem | Cluster | Supporting ecosystem | Pillar relationship | Notes |
|---|---|---|---|---|---|
| `brain-fog-menopause-article.md` | Menopause | Menopause brain fog / symptom support | Sleep, Nutrition, Recovery | Menopause pillar | Actual live content; core article |
| `brain-fog-menopause-article-v2.md` | Menopause | Duplicate of brain fog topic | Sleep, Nutrition, Recovery | Menopause pillar | Duplicate/cannibalization risk; likely replace / archive |

### Planned briefs mapped to clusters
| Brief | Ecosystem | Cluster | Supporting ecosystem | Pillar relationship | Status |
|---|---|---|---|---|---|
| `brain-fog-menopause-brief.md` | Menopause | Brain fog / cognitive clarity | Sleep, Nutrition | Menopause pillar | Brief exists; article content exists too |
| `menopause-sleep-fatigue-brief.md` | Menopause | Sleep disruption | Recovery, Nutrition | Menopause pillar | Planned, empty file; article missing |
| `menopause-weight-gain-brief.md` | Menopause | Weight gain / metabolism | Nutrition, Fitness | Menopause pillar | Planned, empty file; article missing |
| `best-protein-after-50-brief.md` | Nutrition | Protein / muscle support | Healthy Aging, Fitness | Nutrition pillar | Planned, empty file; article missing |
| `vitamin-d-after-50-brief.md` | Nutrition | Micronutrients | Healthy Aging, Recovery | Nutrition pillar | Planned, empty file; article missing |

## 6. Detection Summary
### Orphan articles
- `brain-fog-menopause-article.md` currently has no documented pillar or sibling link inventory in the workspace
- `brain-fog-menopause-article-v2.md` is functionally orphaned and also causes cannibalization risk
- Planned briefs are orphaned by definition because they are not published and lack internal linking

### Weak clusters
- Menopause cluster is weak because it currently has only one live topic and a duplicate file
- Nutrition cluster is weak because it has only planning-level briefs and no published pages
- Sleep cluster is weak / missing because the only relevant topic exists as a brief, not a page

### Overlapping / cannibalized articles
- `brain-fog-menopause-article.md` vs `brain-fog-menopause-article-v2.md` are overlapping duplicates
- The planned `brain-fog-menopause-brief.md` and published article cover the same intent; this is okay if the brief is used to improve the live article, but not okay if both become separate published pages with the same keyword intent

### Missing pillar pages
- `SEO Blogger/pillars/healthy-aging-pillar.md` is empty
- `SEO Blogger/pillars/nutrition-recovery-pillar.md` is empty
- `SEO Blogger/pillars/health-aging-pillar.md` is empty
- `SEO Blogger/pillars/mobility-joint-support-pillar.md` is empty
- `SEO Blogger/pillars/sleep-recovery-pillar.md` is empty
- `SEO Blogger/pillars/fitness-after-50-pillar.md` is empty
- `SEO Blogger/pillars/womens-wellness-pillar.md` is missing from the workspace (blueprint includes it)
- `SEO Blogger/pillars/gut-health-pillar.md` is missing from the workspace (blueprint includes it)
- `SEO Blogger/pillars/longevity-pillar.md` is missing from the workspace (blueprint includes it)

### Missing internal links
- No internal link inventory exists between the menopause pillar and published Menopause content
- No sibling or cross-ecosystem links are documented for current page(s)
- No internal linking map is present for Nutrition or Sleep planning pages
- `SEO Blogger/reports/orphan-articles-report.md` is empty, indicating the orphan-fix process is not yet executed

## 7. Priority Scores
### Score key
- 5 = Critical foundation gap
- 4 = High value fix with direct SEO leverage
- 3 = Moderate value, should be implemented after foundations
- 2 = Low effort but lower priority
- 1 = Maintenance / cleanup

### Priority list
1. 5 — Consolidate duplicate menopause pages
   - Remove or archive `brain-fog-menopause-article-v2.md`
   - Confirm canonical URL and ensure only one published brain fog article remains
2. 5 — Complete the Menopause pillar page and add internal links
   - Add explicit links from the pillar to the brain fog article, sleep/fatigue topic, and weight/metabolism topic
3. 4 — Publish the planned Menopause cluster pages
   - `menopause-sleep-fatigue` and `menopause-weight-gain`
4. 4 — Build Nutrition pillar and publish core nutrition cluster pages
   - `best-protein-after-50` and `vitamin-d-after-50`
5. 4 — Create a Sleep pillar and publish Menopause sleep content under it
6. 3 — Populate the empty cluster files and bridge them to the global authority map
7. 3 — Populate `published-articles.md` and `orphan-pages-tracker.md` with current page inventory and inlink status
8. 2 — Add cross-ecosystem links from Menopause to Nutrition, Sleep, Recovery, and Healthy Aging
9. 1 — Keep the authority map updated and move completed briefs into live publishing workflow

## 8. Recommended Fixes
### Immediate fixes
- Consolidate duplicate brain fog content into one canonical article
- Add a working internal linking plan for the Menopause pillar page
- Document the current published article(s) in `published-articles.md`

### Near-term fixes
- Publish or at least draft the missing article content for the 5 discovered briefs
- Build or flesh out the Nutrition and Sleep pillar pages
- Create the Women’s Wellness, Gut Health, and Longevity pillar page placeholders if they are part of the full ecosystem

### Structural fixes
- Populate `SEO Blogger/content-clusters/*` placeholder files with actual article lists and cluster relationships
- Link each published article to: 
  - Its pillar page
  - 2 sibling articles in the same cluster
  - 1 cross-ecosystem page where relevant
- Use the global authority map as the source of truth for pillar/cluster naming conventions

### Orphan repair process
1. Identify each page that has zero documented inlinks
2. Add one direct link from its primary pillar page
3. Add one contextual link from a sibling cluster article
4. Add one cross-ecosystem contextual link if relevant
5. Track completion in `orphan-pages-tracker.md`

## 9. Next step recommendations
1. Confirm the canonical Menopause content URL and remove the versioned duplicate
2. Create a pipeline for converting existing briefs into published content pages
3. Build the missing pillar pages for Nutrition and Sleep first, then fill other ecosystems
4. Execute an internal linking pass using the `lonage-global-authority-map.md` structure as the linking graph
5. Re-run the inventory after these changes and publish a refreshed ecosystem report

## 10. Limitations of this scan
- The report is based solely on markdown files found in the current workspace
- No site crawl or search-console data was available
- Internal link status was inferred from file presence only; actual URL inlinks are not confirmed
- The existing content architecture is still mostly planning-stage rather than a fully published article ecosystem
