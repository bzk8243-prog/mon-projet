# Lonage SEO Blogger System

A clean, production-ready architecture for a **WordPress health & fitness blog** focused on **menopause SEO topical authority**.

This repository is now organized as a dedicated **SEO Blogger operating system** for planning, writing, optimizing, publishing, and maintaining menopause-focused content.

---

## 1) Architecture Overview

```text
/SEO Blogger
  /agents
  /prompts
  /workflows
  /internal-linking
  /content-clusters
  /rank-math
  /WordPress
```

### Folder Purposes

- **`SEO Blogger/agents`**  
  Role-based agents that execute specialized tasks (research, outlining, drafting, SEO optimization, linking, publishing, auditing).

- **`SEO Blogger/prompts`**  
  Reusable prompt templates used by agents for consistent outputs and quality control.

- **`SEO Blogger/workflows`**  
  End-to-end process definitions for article production, optimization, publishing, content updates, and audits.

- **`SEO Blogger/internal-linking`**  
  Rules, logic, and mapping files for internal linking automation across pillar and cluster pages.

- **`SEO Blogger/content-clusters`**  
  Menopause topical maps, pillar definitions, cluster topic inventories, and authority expansion plans.

- **`SEO Blogger/rank-math`**  
  Checklists and standards for Rank Math SEO scoring, schema usage, focus keyword alignment, and on-page optimization.

- **`SEO Blogger/WordPress`**  
  Publishing and update playbooks for WordPress: formatting standards, metadata completion, scheduling, and revision handling.

---

## 2) System Scope (Strict)

This architecture is intentionally limited to:

1. **Menopause SEO topical authority**
2. **Pillar and cluster architecture**
3. **Internal linking automation**
4. **Article writing workflows**
5. **Rank Math SEO optimization**
6. **WordPress publishing**
7. **Content updates and audits**

### Explicitly Excluded

- Any DP creators
- Any digital product systems
- Any non-SEO monetization workflow unrelated to the above scope

---

## 3) How Agents Work

Agents are modular specialists that run in sequence or in parallel depending on workflow stage.

### Suggested Agent Roles

- **Topical Authority Strategist**  
  Defines menopause pillars, subtopics, search intent, and content gap priorities.

- **Cluster Planner**  
  Builds pillar-cluster maps and assigns article briefs to cluster nodes.

- **Article Writer**  
  Produces drafts optimized for readability, intent satisfaction, and authority signals.

- **On-Page SEO Agent (Rank Math)**  
  Applies keyword placement, metadata, heading hierarchy, schema guidance, and score improvements.

- **Internal Linking Agent**  
  Adds contextual links to pillars, sibling clusters, and conversion-relevant educational pages.

- **WordPress Publisher Agent**  
  Prepares final post structure, slugs, categories, tags, featured elements, and publication scheduling.

- **Content Audit Agent**  
  Reviews existing posts for decay, cannibalization, outdated medical framing, and linking opportunities.

### Agent Operating Rules

- Agents must preserve menopause topical focus.
- Agents must reference pillar-cluster relationships before finalizing content.
- Linking decisions must prioritize user journey + topical reinforcement.
- Publishing must pass Rank Math and WordPress checklists.

---

## 4) How Workflows Connect Together

Workflows are chained so each output becomes the next input:

1. **Topical Planning Workflow**  
   Produces menopause pillar and cluster map.

2. **Brief Creation Workflow**  
   Converts cluster nodes into article briefs with intent + keyword targets.

3. **Article Writing Workflow**  
   Generates structured draft aligned to the assigned brief.

4. **SEO Optimization Workflow (Rank Math)**  
   Refines metadata, headings, schema, and on-page score.

5. **Internal Linking Workflow**  
   Inserts strategic links to pillar pages and adjacent clusters.

6. **WordPress Publishing Workflow**  
   Publishes or schedules content with final QA.

7. **Update & Audit Workflow**  
   Re-evaluates published content for freshness, performance, and linking upgrades.

This creates a closed-loop system: **Plan → Create → Optimize → Link → Publish → Audit → Improve**.

---

## 5) How Content Clusters Connect to Pillar Pages

Your authority model should follow a hub-and-spoke design:

- **Pillar Page (Hub):** comprehensive menopause topic page (broad intent)
- **Cluster Articles (Spokes):** focused subtopic pages (specific intents)

### Connection Model

- Every cluster article must link to its primary pillar page.
- Pillar pages should link back to all active high-value cluster pages.
- Related cluster pages should cross-link when intent overlap is useful.
- Anchor text should reflect user intent and topical relevance naturally.

### Example (Conceptual)

- **Pillar:** Menopause Symptoms Guide
  - Cluster: Sleep issues during menopause
  - Cluster: Weight changes in menopause
  - Cluster: Mood and anxiety during perimenopause
  - Cluster: Exercise strategies for menopause fatigue

Each cluster reinforces the pillar’s authority, while the pillar consolidates semantic depth and navigational clarity.

---

## 6) Recommended Next Build Steps

1. Add agent specs into `SEO Blogger/agents` (one markdown per agent).
2. Create prompt templates in `SEO Blogger/prompts` for each agent role.
3. Define workflow SOPs in `SEO Blogger/workflows` with clear input/output contracts.
4. Build internal link rulebook and mapping templates in `SEO Blogger/internal-linking`.
5. Add menopause pillar-cluster maps in `SEO Blogger/content-clusters`.
6. Add Rank Math quality checklist in `SEO Blogger/rank-math`.
7. Add WordPress publishing checklist and update SOP in `SEO Blogger/WordPress`.

---

## 7) Operating Principle

This repository functions as a **focused SEO execution framework** for Lonage.
Every action should strengthen menopause topical authority, improve internal discoverability, and support consistent publishing quality in WordPress.

---

## 8) Dedicated Internal Linking System (Implemented)

The Lonage menopause architecture now includes a dedicated internal linking system and a formal old-article update workflow:

- `SEO Blogger/internal-linking/lonage-menopause-internal-linking-system.md`
  - pillar-to-cluster linking rules,
  - cluster-to-pillar linking rules,
  - sibling article linking rules,
  - anchor text recommendations,
  - orphan article detection SOP,
  - Rank Math SEO recommendations,
  - monthly linking audit cadence.

- `SEO Blogger/workflows/old-article-update-workflow.md`
  - step-by-step workflow to refresh aging menopause articles,
  - integrates linking upgrades + Rank Math checks + WordPress update QA.

---

## 9) AI-Assisted Article Update Suite (Implemented)

To support automatic updates of existing menopause WordPress articles, the following workflow assets are now included:

- `SEO Blogger/workflows/ai-wordpress-update-workflow.md`
- `SEO Blogger/workflows/menopause-content-audit-checklist.md`
- `SEO Blogger/workflows/menopause-content-refresh-sop.md`
- `SEO Blogger/workflows/menopause-seo-optimisation-process.md`

These documents cover automated analysis, orphan detection, missing link recommendations, Rank Math structure improvements, human-style preservation guardrails, and final human editorial QA.

---

## 10) Complete Internal Linking Map (A–F) for Existing URLs

To operationalize the Lonage menopause architecture without changing indexed URLs/slugs/categories:

- `SEO Blogger/internal-linking/lonage-menopause-linking-map-A-F.md`
  - pillar-to-cluster map,
  - cluster-to-cluster sibling map,
  - missing-link task format,
  - orphan recovery system,
  - Rank Math linking rules,
  - WordPress editor implementation instructions.

- `SEO Blogger/internal-linking/lonage-menopause-linking-tracker.csv`
  - A–F cluster tracking sheet for URL-level execution, QA, and status control.

---

## 11) Full-Site Authority Expansion (Implemented)

The completed menopause architecture is now extended into a full-site authority model for all Lonage ecosystems:

- `SEO Blogger/content-clusters/lonage-global-authority-map.md`
  - global topical authority structure,
  - pillars/clusters/sibling groups for each ecosystem,
  - cross-category relationship graph,
  - orphan recovery at full-site level,
  - suggested missing authority pages.

- `SEO Blogger/internal-linking/lonage-global-linking-system.md`
  - site-wide linking quotas and rules,
  - Rank Math internal linking recommendations,
  - cross-ecosystem bridge logic.

- `SEO Blogger/WordPress/lonage-wordpress-linking-implementation.md`
  - actionable WordPress editor implementation instructions.

- `SEO Blogger/workflows/lonage-editorial-linking-sop.md`
  - editorial SOP for consistent linking execution across all ecosystems.

---

## 12) WordPress Implementation Roadmap (Live Site)

For live deployment of the full Lonage SEO authority system:

- `SEO Blogger/WordPress/lonage-wordpress-implementation-roadmap.md`
  - step-by-step implementation plan,
  - Rank Math configuration guidance,
  - category strategy,
  - pillar/cluster rollout,
  - internal linking implementation,
  - orphan recovery,
  - publishing and editorial SOP operations,
  - future article integration model,
  - monthly maintenance and quarterly scaling strategy.

Additional operational workflow files:
- `SEO Blogger/workflows/lonage-wordpress-workflow.md`
- `SEO Blogger/workflows/lonage-seo-maintenance-workflow.md`
- `SEO Blogger/workflows/lonage-future-scaling-strategy.md`
