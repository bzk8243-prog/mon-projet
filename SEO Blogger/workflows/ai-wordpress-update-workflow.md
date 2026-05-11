# AI Workflow: Automatic Update of Existing Menopause WordPress Articles (Lonage)

## Objective
Create a semi-automated workflow where AI identifies opportunities, drafts safe improvements, and a human editor publishes final updates.

## Guardrails
- Keep menopause topical authority as the primary goal.
- Preserve original author voice and tone.
- Avoid generic AI phrasing and repetitive structure.
- Never auto-publish without human approval.

## Workflow Stages

### Stage 1 — Article Intake & Analysis
1. Pull list of existing menopause URLs from WordPress.
2. For each URL, capture:
   - publish/modified date,
   - word count,
   - parent pillar assignment,
   - Rank Math fields,
   - internal links out/in.
3. Score article risk/opportunity:
   - stale content,
   - weak structure,
   - low internal connectivity,
   - low CTR / poor position.

**Output:** prioritized update queue.

### Stage 2 — Missing Internal Link Detection
1. Compare article entities/headings vs pillar + cluster map.
2. Detect missing parent pillar link.
3. Detect missing sibling links by topical overlap.
4. Detect missing cross-cluster link to next-step user intent.

**Output:** link gap report per URL.

### Stage 3 — Orphan Detection
1. Crawl all menopause URLs and compute contextual inlinks.
2. Flag article as orphan when contextual inlinks = 0.
3. For each orphan, assign:
   - 1 source pillar,
   - 2–3 source sibling/related clusters for reintegration.

**Output:** orphan recovery plan.

### Stage 4 — Link Recommendation Engine
For each article, AI suggests:
- **Pillar link(s):** must include parent pillar in upper half when possible.
- **Cluster link(s):** 2–5 relevant siblings.
- **Anchor text options:** natural, non-spammy variants.

Recommendation format:
- source paragraph/heading,
- suggested anchor,
- destination URL,
- reason (intent match / journey next step).

### Stage 5 — Rank Math SEO Structure Improvement
AI prepares changes for human review:
- focus keyword alignment,
- title/meta rewrite for clarity + CTR,
- heading hierarchy cleanup,
- schema recommendation,
- image alt text opportunities,
- internal linking improvements.

### Stage 6 — Content Refresh Drafting (Style-Safe)
AI generates a **patch draft** only for outdated or weak sections:
- keep sentence rhythm similar to original,
- preserve brand vocabulary,
- avoid robotic transitions and over-template wording,
- keep practical menopause guidance concise and empathetic.

### Stage 7 — Human Editorial Review (Required)
Editor must approve:
- factual accuracy,
- tone consistency,
- natural readability,
- non-AI sounding flow,
- final link placement.

### Stage 8 — WordPress Update & Post-Update QA
1. Apply approved edits in WordPress.
2. Re-run Rank Math checks.
3. Publish update.
4. Monitor performance 14–30 days.

---

## Minimal Automation Contract (Per URL)
The workflow should return a structured output with:
- URL
- parent pillar
- missing pillar links
- missing sibling links
- orphan status
- Rank Math fixes
- content refresh patch
- human review checklist state
