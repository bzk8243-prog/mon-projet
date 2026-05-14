# Lonage AI Agent Architecture

## Overview
This architecture defines the full Lonage SEO AI system for the complete ecosystem: Menopause, Healthy Aging, Fitness After 50, Nutrition, Recovery, Mobility, Sleep, Gut Health, Longevity, and Women’s Wellness.

It preserves all existing WordPress URLs, slugs, categories, and site structure.

Each agent is designed to operate within the Lonage content framework and to collaborate through a master orchestrator.

---

## Agent Definitions

### 1. Article Research Agent
**Role**
Research user intent, keywords, competitor coverage, and ecosystem fit for new Lonage articles.

**Inputs**
- Topic brief or idea
- Ecosystem assignment
- Pillar and cluster definitions
- Existing Lonage content inventory
- SERP and competitor signals

**Outputs**
- Article research brief
- Primary and secondary keyword map
- Suggested title and meta angles
- Target user questions
- Suggested internal link targets
- Ecosystem placement note

**Workflow steps**
1. Validate topic against Lonage ecosystem and pillar structure.
2. Confirm target search intent in Menopause, Healthy Aging, Fitness After 50, Nutrition, Recovery, Mobility, Sleep, Gut Health, Longevity, or Women’s Wellness.
3. Identify top competitor topics and gaps.
4. Create keyword and question map.
5. Recommend primary cluster and pillar.
6. Pass brief to the SEO Article Writing Agent.

**Validation rules**
- Topic must fit one primary ecosystem.
- Must preserve existing category taxonomy.
- No duplicate intent with existing URLs.
- Research output includes at least one pillar and cluster target.

**SEO rules**
- Prioritize user intent over keyword volume.
- Use ecosystem-specific phrasing.
- Avoid creating topic overlaps in the same cluster.

**Linking rules**
- Include a primary pillar target and 2 sibling article candidates.
- Flag potential cross-ecosystem bridge pages.

**Escalation rules**
- If the topic conflicts with existing published URL intent, escalate to Cannibalization Detection Agent.
- If research uncovers no valid ecosystem fit, escalate to Opportunity Discovery Agent.

**Collaboration**
- Works with Cluster Management Agent for correct cluster assignment.
- Feeds output into SEO Article Writing Agent and Publishing Calendar Management Agent.

---

### 2. SEO Article Writing Agent
**Role**
Write optimized, human-focused Lonage articles aligned to ecosystem, pillar, and cluster intent.

**Inputs**
- Research brief from Article Research Agent
- Lonage article templates
- Brand voice guidelines
- Pillar and cluster assignments
- Related existing content summary

**Outputs**
- Draft SEO article
- SEO title and meta description
- Heading structure (H1/H2/H3)
- FAQ section
- Suggested CTAs
- Suggested internal link anchors
- Image prompt ideas

**Workflow steps**
1. Validate research brief and ecosystem assignment.
2. Build article structure around pillar and cluster intent.
3. Write content in Lonage voice and target audience tone.
4. Publish draft for Rank Math optimization and QA.
5. Package article for WordPress Publisher Agent.

**Validation rules**
- Article must map to exactly one primary cluster.
- Primary keyword appears naturally in first 100 words.
- No content duplication with existing published URLs.
- Preserve recommended URL slug if a new page is created.

**SEO rules**
- Use user-focused headings and semantic subtopics.
- Write 1,200+ words for cluster pages and 1,500+ words for pillar-related content where needed.
- Include at least one FAQ if the topic benefits from it.
- Maintain readability for women 40+.

**Linking rules**
- Include one parent pillar link in the top third of content.
- Include 2 sibling links in the body.
- Include 1 cross-ecosystem contextual link if relevant.

**Escalation rules**
- If the draft overlaps with existing published content, escalate to Cannibalization Detection Agent.
- If internal linking targets are missing, escalate to Internal Linking Agent.

**Collaboration**
- Works closely with Rank Math Optimization Agent for on-page SEO.
- Passes draft to WordPress Publishing Agent and Image Generation Agent.
- Coordinates with Content Scoring QA Agent for quality validation.

---

### 3. Internal Linking Agent
**Role**
Audit and implement Lonage internal linking for pillar, cluster, sibling, and cross-ecosystem authority.

**Inputs**
- Existing content inventory
- Pillar and cluster map
- Article draft or published page
- Orphan list from Orphan Page Recovery Agent
- Authority gaps from Audit Agent

**Outputs**
- Link insertion recommendations
- Internal link map
- Orphan recovery actions
- Cross-ecosystem bridge suggestions
- Link validation report

**Workflow steps**
1. Review article ecosystem and cluster assignment.
2. Identify parent pillar and sibling cluster pages.
3. Suggest internal link anchor text.
4. Suggest cross-ecosystem links based on authority map.
5. Validate links against Rank Math and editorial rules.
6. Package link plan for publisher or update workflow.

**Validation rules**
- No URL renaming or slug changes.
- No irrelevant or forced links.
- Internal link density should be balanced.
- Cross-links only when topical relevance is strong.

**SEO rules**
- Prioritize pillar and sibling links first.
- Add at least one parent pillar link to each cluster page.
- Use natural anchor text, not exact-match spam.
- Avoid more than 30% outbound internal link proportion in one page.

**Linking rules**
- Pillar → articles: required for all cluster pages.
- Article → pillar: required for all cluster pages.
- Sibling → sibling: preferred inside each cluster.
- Cross-ecosystem: allowed when the content logically supports it.

**Escalation rules**
- If no suitable pillar exists, escalate to Pillar Authority Building Agent.
- If multiple link targets conflict, escalate to Master Orchestrator for manual review.
- If orphan list remains unchanged after two cycles, escalate to Traffic Decay Detection Agent.

**Collaboration**
- Works with Pillar Authority Building Agent, Cluster Management Agent, and WordPress Publishing Agent.
- Feeds recommendations into the Refresh Pipeline and Orphan Page Recovery Workflow.

---

### 4. Rank Math Optimization Agent
**Role**
Optimize Lonage articles for Rank Math and on-page SEO best practices.

**Inputs**
- Draft article from SEO Article Writing Agent
- Keyword and intent brief
- Current Rank Math settings
- Internal linking plan

**Outputs**
- Optimized title and meta description
- Heading/structure improvements
- Keyword placement suggestions
- Schema and FAQ recommendations
- Readability improvement suggestions
- Rank Math compatibility report

**Workflow steps**
1. Review draft against Rank Math requirements.
2. Apply title, description, keyword placement, heading, and schema improvements.
3. Validate internal links and anchor relevance.
4. Check image alt text and content readability.
5. Generate final Rank Math optimization report.

**Validation rules**
- Avoid keyword stuffing.
- Maintain human readability.
- Preserve article tone and narrative flow.
- Ensure each improvement is user-value positive.

**SEO rules**
- Use one primary keyword with supporting secondary terms.
- Place the primary keyword in the title, first paragraph, and at least one H2.
- Keep meta description under 160 characters.
- Use schema only when it improves user experience.

**Linking rules**
- Confirm 4+ internal links are present if the article is published.
- Ensure pillar link is in the top section.
- Validate sibling and cross-ecosystem links for relevance.

**Escalation rules**
- If the draft cannot be optimized without content rework, escalate to Article Research Agent.
- If Rank Math requirements conflict with the article’s user experience, escalate to Master Orchestrator.

**Collaboration**
- Works with SEO Article Writing Agent and WordPress Publishing Agent.
- Coordinates with Content Scoring QA Agent for final quality checks.

---

### 5. Content Refresh Agent
**Role**
Update published Lonage content for freshness, relevance, and authority.

**Inputs**
- Published article performance data
- Search Console analysis
- Internal linking audit results
- Content scoring and QA reports

**Outputs**
- Refresh plan
- Revised content drafts
- Updated internal links
- Rank Math re-optimization suggestions
- Refresh completion report

**Workflow steps**
1. Identify refresh candidates via Search Console and Traffic Decay Detection Agent.
2. Validate current intent and ranking status.
3. Update content with new insights, stats, and better examples.
4. Improve internal links and pillar references.
5. Re-optimize SEO elements.
6. Publish updated page and monitor impact.

**Validation rules**
- Refresh must improve user value.
- Do not thin content or remove essential context.
- Ensure canonical URLs remain unchanged.
- Track refresh reasons and outcomes.

**SEO rules**
- Refresh should focus on intent, accuracy, and topical depth.
- Add updated clusters or related content where relevant.
- Recheck Rank Math for updated elements.

**Linking rules**
- Add at least one new pillar or sibling link during refresh.
- Fix broken or outdated internal links.
- Verify anchor relevance before publishing.

**Escalation rules**
- If a page is decaying due to cannibalization, escalate to Cannibalization Detection Agent.
- If the refresh uncovers major strategy gaps, escalate to Authority Expansion Pipeline.

**Collaboration**
- Works with Search Console Analysis Agent, Traffic Decay Detection Agent, and Rank Math Optimization Agent.
- Provides refreshed content to WordPress Publishing Agent.

---

### 6. Affiliate Integration Agent
**Role**
Embed affiliate strategy into Lonage content while preserving user-first wellness tone.

**Inputs**
- Article brief and draft content
- Affiliate product lists and commission rules
- Lonage brand voice and compliance guidelines

**Outputs**
- Affiliate integration plan
- Product mention recommendations
- Soft-sell affiliate copy blocks
- Affiliate QA checklist

**Workflow steps**
1. Review article ecosystem and relevance of affiliate products.
2. Select only products that align with topic intent.
3. Write soft-sell affiliate mention copy.
4. Place affiliate links near the end of the article or inside relevant sections.
5. Validate against compliance and tone.

**Validation rules**
- Avoid overt sales language.
- Keep affiliate mentions relevant to the article.
- Do not create duplicate affiliate pages on similar topics.
- Respect medical and wellness sensitivity.

**SEO rules**
- Use affiliate links as supplemental value, not main content.
- Include nofollow where required by policy if not site-wide.
- Preserve the main article intent and keyword focus.

**Linking rules**
- Affiliate links are external only; never substitute internal pillar links.
- If affiliate content is highly relevant, ensure corresponding non-affiliate internal links remain in the same page.

**Escalation rules**
- If affiliate integration overpowers the article’s intent, escalate to Content Scoring QA Agent.
- If compliance issues arise, escalate to Master Orchestrator.

**Collaboration**
- Works with SEO Article Writing Agent and WordPress Publishing Agent.
- Coordinates with Content Scoring QA Agent for final signoff.

---

### 7. WordPress Publishing Agent
**Role**
Prepare and manage safe WordPress publishing workflows while preserving existing structure.

**Inputs**
- Final article draft and SEO assets
- Publish-ready content package
- Category and pillar assignment
- Rank Math optimization report
- Featured image prompt

**Outputs**
- WordPress-ready publication draft
- Publishing checklist
- Post-publish validation report
- Published page log

**Workflow steps**
1. Verify slug and category preservation.
2. Confirm URL and WordPress structure rules.
3. Insert final content into WordPress draft.
4. Apply Rank Math fields and schema settings.
5. Add images and featured image metadata.
6. Run pre-publish QA checklist.
7. Publish or schedule according to the calendar.

**Validation rules**
- Never change indexed URLs or slugs.
- Never overwrite existing pages without editorial approval.
- Confirm all internal links are intact.
- Validate category assignment against ecosystem.

**SEO rules**
- Preserve on-page SEO settings from Rank Math.
- Ensure canonical is correct and unchanged unless intentionally updated.
- Use excerpt and featured image metadata.

**Linking rules**
- Confirm pillar and sibling links are present in the published page.
- Verify any cross-ecosystem links are correctly formatted.
- Ensure internal anchor text is still natural after WordPress insertion.

**Escalation rules**
- If publishing requires slug changes, escalate to Master Orchestrator.
- If WordPress preview reveals formatting or link issues, pause publication and escalate to Content Scoring QA Agent.

**Collaboration**
- Receives work from SEO Article Writing Agent, Rank Math Optimization Agent, and Image Generation Agent.
- Works with Publishing Calendar Management Agent for schedule.
- Sends published page logs to Audit Pipeline.

---

### 8. Image Generation Agent
**Role**
Generate editorial image prompts for Lonage content with consistent wellness style.

**Inputs**
- Article topic and ecosystem
- Brand visual guidelines
- Featured image and social size requirements
- SEO article art brief

**Outputs**
- Featured image prompts
- Social media image prompts
- Pinterest-friendly prompts
- Asset metadata suggestions

**Workflow steps**
1. Review article ecosystem and audience.
2. Create prompt aligned with Lonage visual style.
3. Generate image suggestions for featured and social assets.
4. Validate prompt quality and brand alignment.
5. Forward prompts to WordPress Publishing Agent.

**Validation rules**
- Visuals must reflect women 40+ and wellness context.
- Avoid overtly AI or generic stock imagery prompts.
- Preserve editorial authenticity and diversity.

**SEO rules**
- Use alt text recommendations tied to article keywords.
- Ensure image themes support page intent.
- Optimize image descriptions for thumbnails and social sharing.

**Linking rules**
- No internal linking responsibilities.
- Ensure image assets complement page content and internal link anchors visually.

**Escalation rules**
- If prompts produce irrelevant imagery, escalate to Master Orchestrator.
- If brand guidelines are unclear, escalate to Content Scoring QA Agent.

**Collaboration**
- Works with WordPress Publishing Agent and SEO Article Writing Agent.
- Coordinates with Affiliate Integration Agent for product visuals when needed.

---

### 9. SEO Audit Agent
**Role**
Perform periodic SEO audits for Lonage content and site architecture.

**Inputs**
- Published content inventory
- Ranking and traffic data
- Internal linking reports
- Pillar/cluster map

**Outputs**
- SEO audit reports
- Gap analysis by ecosystem
- Authority and orphan reports
- Recommendations for content, linking, and pillar fixes

**Workflow steps**
1. Crawl published content and inventory all pages.
2. Detect orphan, weak cluster, and linking gaps.
3. Audit pillar coverage and ecosystem authority.
4. Produce actionable recommendations.
5. Feed findings into the Audit Pipeline and orchestrator.

**Validation rules**
- Audit outputs must be grounded in actual published content.
- Recommended actions must preserve URLs and categories.
- Include evidence for each issue.

**SEO rules**
- Focus on pillar authority, topical coverage, and internal linking.
- Prioritize issues with highest organic impact.
- Avoid recommendations that require wholesale URL changes.

**Linking rules**
- Highlight missing pillar and sibling links.
- Recommend cross-ecosystem bridges from strong to weak areas.
- Emphasize safe linking changes.

**Escalation rules**
- If major architecture gaps are found, escalate to Pillar Authority Building Agent.
- If audit finds content cannibalization, escalate to Cannibalization Detection Agent.

**Collaboration**
- Works with Master Orchestrator, Cluster Management Agent, and Authority Expansion Agent.
- Sends issues to Refresh and Publish Pipelines.

---

### 10. Cluster Management Agent
**Role**
Manage Lonage article clusters and ensure each piece fits the proper topical group.

**Inputs**
- Pillar definitions
- Article research briefs
- Content inventory
- SEO audit insights

**Outputs**
- Cluster assignment map
- Cluster health status
- Sibling article lists
- Gap analysis per ecosystem

**Workflow steps**
1. Review pillar definitions and cluster taxonomy.
2. Assign each article to one cluster.
3. Validate that cluster topics are discrete and non-overlapping.
4. Create sibling article sets.
5. Monitor cluster depth and coverage.

**Validation rules**
- Each article must belong to exactly one primary cluster.
- Cluster assignments must align with the ecosystem authority map.
- Prevent overlapping topics inside the same ecosystem.

**SEO rules**
- Keep cluster themes narrow and focused.
- Ensure cluster pages link back to their assigned pillar.
- Encourage cluster sibling link sets of 3+ articles.

**Linking rules**
- Provide sibling and pillar link targets for each article.
- Suggest cross-cluster connections only when semantically logical.

**Escalation rules**
- If cluster intent is unclear, escalate to Article Research Agent.
- If cluster depth is too low, escalate to Authority Expansion Agent.

**Collaboration**
- Partners with Pillar Authority Building Agent, Internal Linking Agent, and SEO Audit Agent.
- Feeds cluster assignments into the Publishing Calendar Management Agent.

---

### 11. Pillar Authority Building Agent
**Role**
Create and maintain pillar pages that anchor each Lonage ecosystem.

**Inputs**
- Ecosystem definitions
- Cluster inventory
- Existing content and briefs
- SEO audit results

**Outputs**
- Pillar page drafts
- Pillar link maps
- Authority-building plans
- Pillar update schedules

**Workflow steps**
1. Define pillar page scope and sections.
2. Map required cluster articles.
3. Create pillar content with cross-ecosystem bridge sections.
4. Add links to all cluster articles.
5. Monitor pillar authority and refresh quarterly.

**Validation rules**
- Pillar pages must be the top authority for the ecosystem.
- Each pillar must link to all cluster articles.
- Pillars must never duplicate cluster-level content.

**SEO rules**
- Use broader ecosystem keywords and theme coverage.
- Include 1-2 cross-ecosystem contextual links.
- Keep pillar pages evergreen and strategic.

**Linking rules**
- Pillar → cluster articles: mandatory.
- Cluster → pillar: mandatory.
- Pillar → related ecosystem pillars: encouraged.

**Escalation rules**
- If there are no cluster articles to link, escalate to Cluster Management Agent.
- If pillar coverage is insufficient, escalate to Master Orchestrator.

**Collaboration**
- Coordinates with Cluster Management Agent, Internal Linking Agent, and Content Scoring QA Agent.
- Sends pillar pages to WordPress Publishing Agent and Rank Math Optimization Agent.

---

### 12. Cannibalization Detection Agent
**Role**
Detect and resolve keyword and intent cannibalization across Lonage content.

**Inputs**
- Published article inventory
- Research briefs
- Search Console performance data
- Article topic map

**Outputs**
- Cannibalization report
- Merge or consolidation recommendations
- Redirect or rewrite plans
- Priority action list

**Workflow steps**
1. Compare topic maps and keywords across published content.
2. Identify duplicate intent or overlapping titles.
3. Flag competitor-like content collisions.
4. Recommend content mergers, consolidations, or canonicalization.
5. Validate against URL preservation rules.

**Validation rules**
- Ensure recommendations do not require URL renaming.
- Focus on intent clarity and user experience.
- Use data-based evidence from performance metrics.

**SEO rules**
- Prevent multiple pages from targeting the same primary keyword.
- Keep cluster topics distinct and non-redundant.
- Use pillar pages as canonical hubs.

**Linking rules**
- Recommend internal links to the strongest page when cannibalization exists.
- Use canonical or redirect strategies only when necessary.

**Escalation rules**
- If a major cluster is affected, escalate to Audit Pipeline and Master Orchestrator.
- If multiple pages require merging, escalate to Content Scoring QA Agent.

**Collaboration**
- Works with Article Research Agent, Content Refresh Agent, and WordPress Publishing Agent.
- Informs the Publishing Calendar Management Agent of cleanup needs.

---

### 13. Orphan Page Recovery Agent
**Role**
Rescue orphaned Lonage pages by assigning pillar links and sibling connections.

**Inputs**
- Orphan article list
- Pillar and cluster map
- Published content inventory
- Internal linking audit output

**Outputs**
- Orphan recovery plan
- Link insertion instructions
- Recovery progress tracker
- Updated orphan report

**Workflow steps**
1. Identify orphan pages using audit data.
2. Assign each orphan to a primary pillar.
3. Propose pillar links and sibling links.
4. Validate the recovery plan against ecosystem rules.
5. Implement recovery actions and monitor results.

**Validation rules**
- Each orphan must have a pillar link added.
- Each orphan should receive at least two sibling links.
- Recovery must preserve existing URLs.

**SEO rules**
- Use contextual authority-building links, not forced anchors.
- Prioritize high-value orphan pages first.
- Include cross-ecosystem links only when natural.

**Linking rules**
- Pillar link required.
- Sibling links recommended.
- Cross-ecosystem link optional.

**Escalation rules**
- If no suitable pillar exists, escalate to Pillar Authority Building Agent.
- If orphan count remains high after two cycles, escalate to Audit Pipeline.

**Collaboration**
- Works with Internal Linking Agent and Audit Agent.
- Feeds recovery tasks into Refresh Pipeline and WordPress Publishing Agent.

---

### 14. Cross-Ecosystem Linking Agent
**Role**
Create intentional cross-ecosystem bridges that strengthen Lonage authority.

**Inputs**
- Pillar and cluster authority map
- Published content inventory
- Ecosystem connection rules from the global authority map

**Outputs**
- Cross-ecosystem link map
- Bridge page recommendations
- Anchor text suggestions
- Link placement plan

**Workflow steps**
1. Identify strong ecosystem content with natural bridges.
2. Map cross-link opportunities using the authority blueprint.
3. Recommend anchor text and target pages.
4. Validate links for relevance and user experience.
5. Integrate cross-links into publishing and refresh workflows.

**Validation rules**
- Cross-links must be genuinely useful to readers.
- No more than 1-2 cross-ecosystem links per article.
- Preserve readability and content flow.

**SEO rules**
- Use cross-links to support adjacent ecosystems.
- Prioritize high-value bridges like Menopause → Sleep and Nutrition → Gut Health.
- Avoid meaningless site-wide cross-linking.

**Linking rules**
- Use pillar-to-pillar and cluster-to-cluster bridges.
- Keep cross-ecosystem anchors natural and contextual.
- Do not use cross-links to mask weak internal architecture.

**Escalation rules**
- If a cross-link target is missing, escalate to Authority Expansion Agent.
- If too many cross-links are suggested, escalate to Master Orchestrator.

**Collaboration**
- Works with Pillar Authority Building Agent, Cluster Management Agent, and Internal Linking Agent.
- Sends bridge plans to WordPress Publishing Agent.

---

### 15. Topical Authority Expansion Agent
**Role**
Grow Lonage topical authority across ecosystems by scaling pillar and cluster coverage.

**Inputs**
- Audit gap analysis
- Cluster health metrics
- Ecosystem authority scores
- Existing and planned content pipelines

**Outputs**
- Authority expansion roadmap
- Ecosystem priority list
- Cluster depth plan
- Content volume targets

**Workflow steps**
1. Evaluate ecosystem authority gaps.
2. Prioritize ecosystems by impact and feasibility.
3. Plan pillar and cluster builds.
4. Schedule content creation for low-authority areas.
5. Monitor progress and update goals.

**Validation rules**
- Expansion must align with the global authority map.
- Work should preserve current URLs and categories.
- Focus on ecosystem balance, not just volume.

**SEO rules**
- Build pillar depth before broad scale.
- Ensure each new article supports a clear cluster.
- Use authority flow from strong to weak areas.

**Linking rules**
- Support new pages with pillar and sibling links.
- Use cross-ecosystem bridges to distribute authority.
- Avoid creating isolated pages.

**Escalation rules**
- If authority gaps exceed available production capacity, escalate to Publishing Calendar Management Agent.
- If ecosystem authority is declining, escalate to Audit and Traffic Decay Detection Agents.

**Collaboration**
- Works with Audit Agent, Publishing Calendar Management Agent, and Content Refresh Agent.
- Communicates with WordPress Publishing Agent for execution.

---

### 16. Content Scoring QA Agent
**Role**
Score Lonage content for quality, compliance, and editorial readiness.

**Inputs**
- Draft or published content
- SEO brief and Rank Math report
- Brand voice and editorial guidelines
- UX and readability metrics

**Outputs**
- Quality score
- Pass/fail decision
- Improvement recommendations
- Editorial signoff checklist

**Workflow steps**
1. Review article for tone, structure, and factual accuracy.
2. Check SEO and Rank Math compliance.
3. Evaluate internal linking and pillar consistency.
4. Score content against Lonage quality standards.
5. Approve for publication or request revisions.

**Validation rules**
- Content must meet Lonage brand and readability standards.
- No sensitive or misleading medical claims.
- Editorial quality must be human-first.

**SEO rules**
- Ensure the content supports primary ecosystem and cluster intent.
- Validate heading structure and question-answer flow.
- Confirm internal linking and schema usage.

**Linking rules**
- Confirm that all required pillar and sibling links are present.
- Ensure cross-ecosystem links do not dilute the main intent.

**Escalation rules**
- If the content fails QA, send back to Article Writing Agent.
- If repeated failures occur, escalate to Master Orchestrator.

**Collaboration**
- Works with Rank Math Optimization Agent and WordPress Publishing Agent.
- Provides quality signoff for the Publish Pipeline.

---

### 17. Search Console Analysis Agent
**Role**
Analyze Search Console data to identify discovery, CTR, and query opportunities.

**Inputs**
- Search Console insights
- Published page inventory
- Keyword opportunity map
- Performance history

**Outputs**
- Search Console opportunity report
- CTR and impressions recommendations
- Query gap list
- Titles and meta refresh suggestions

**Workflow steps**
1. Review Search Console queries and pages.
2. Identify pages with high impressions but low CTR.
3. Detect keyword opportunities and query gaps.
4. Recommend click-focused metadata and content adjustments.
5. Feed recommendations to Content Refresh and Publishing Calendar Agents.

**Validation rules**
- Recommendations must be supported by query performance.
- Avoid broad changes that affect multiple ecosystems without reason.
- Preserve existing URLs and slugs.

**SEO rules**
- Use query intent to guide metadata and content refreshes.
- Prioritize pages with strong impressions and weak CTR.
- Avoid keyword changes that conflict with cluster assignments.

**Linking rules**
- Recommend internal link additions when queries show related intent.
- Support cross-ecosystem links when query data indicates relevance.

**Escalation rules**
- If search data shows a major topical gap, escalate to Opportunity Discovery Agent.
- If many pages are underperforming, escalate to Traffic Decay Detection Agent.

**Collaboration**
- Works with Traffic Decay Detection Agent, Content Refresh Agent, and Publishing Calendar Management Agent.
- Provides data to the Audit Pipeline.

---

### 18. Traffic Decay Detection Agent
**Role**
Detect and diagnose decay in organic traffic across Lonage content.

**Inputs**
- Traffic analytics
- Search Console trends
- Published page inventory
- Content refresh history

**Outputs**
- Traffic decay report
- Priority recovery list
- Root cause hypotheses
- Action recommendations

**Workflow steps**
1. Monitor traffic trends for all published pages.
2. Identify pages with sustained decline.
3. Compare against search console and competitor signals.
4. Classify decay by cause: cannibalization, freshness, linking, or content gap.
5. Send recovery and refresh recommendations.

**Validation rules**
- Use at least 4 weeks of data to confirm decay.
- Differentiate between seasonal and true decay.
- Preserve page URLs and categories.

**SEO rules**
- Prioritize pages with highest impact if recovered.
- Avoid unnecessary rewrites when decay is natural.
- Use data to target refresh or removing redundant content.

**Linking rules**
- Recommend internal linking fixes for decaying pages with low inlinks.
- Support pillar strengthening when necessary.

**Escalation rules**
- If decay is caused by cannibalization, escalate to Cannibalization Detection Agent.
- If multiple pages in one ecosystem decay, escalate to Audit Pipeline.

**Collaboration**
- Works with Search Console Analysis Agent, Content Refresh Agent, and Orphan Page Recovery Agent.
- Feeds recovery tasks into Refresh Pipeline.

---

### 19. Opportunity Discovery Agent
**Role**
Find new SEO and content opportunities across the Lonage ecosystem.

**Inputs**
- Keyword research data
- Search Console query gaps
- Competitive content gaps
- Ecosystem authority map

**Outputs**
- Opportunity list
- Priority topic ideas
- New cluster recommendations
- SEO growth plan

**Workflow steps**
1. Scan query gaps and low-coverage topics.
2. Identify new content opportunities per ecosystem.
3. Validate opportunities against existing Lonage architecture.
4. Create topic briefs and assign cluster/pillar.
5. Send opportunities to the Publishing Calendar Management Agent.

**Validation rules**
- Opportunities must fit an existing ecosystem.
- Must not require URL renaming.
- Should be aligned with current content priorities.

**SEO rules**
- Prioritize low-competition, high-relevance topics.
- Favor opportunities that build pillar authority.
- Avoid chasing keywords outside Lonage expertise.

**Linking rules**
- Recommend internal linking targets for each opportunity.
- Use cross-ecosystem bridge potential if relevant.

**Escalation rules**
- If an opportunity conflicts with a current ecosystem topic, escalate to Cannibalization Detection Agent.
- If opportunities exceed capacity, escalate to Publishing Calendar Management Agent.

**Collaboration**
- Works with Article Research Agent, Cluster Management Agent, and Authority Expansion Agent.
- Feeds the Publish Pipeline with new briefs.

---

### 20. Publishing Calendar Management Agent
**Role**
Schedule and manage the Lonage publishing cadence across ecosystems.

**Inputs**
- Content queue and briefs
- Pillar and cluster priorities
- Resource availability
- Audit and performance feedback

**Outputs**
- Publishing calendar
- Ecosystem release schedule
- Resource assignment matrix
- Deadline tracking

**Workflow steps**
1. Review pending briefs and published pipeline.
2. Prioritize by SEO impact and ecosystem balance.
3. Assign articles to publishing slots.
4. Coordinate with WordPress Publishing Agent.
5. Adjust the calendar based on audit and performance feedback.

**Validation rules**
- Preserve the existing WordPress category structure.
- Maintain a sustainable cadence.
- Keep ecosystem coverage balanced.

**SEO rules**
- Schedule high-impact pages first.
- Reserve slots for pillar pages and authority-building content.
- Include time for refresh, link, and QA workflows.

**Linking rules**
- Ensure publishing order supports pillar and cluster relationships.
- Prioritize sibling articles together when possible.

**Escalation rules**
- If deadlines slip or capacity is exceeded, escalate to Master Orchestrator.
- If calendar balance becomes uneven, escalate to Topical Authority Expansion Agent.

**Collaboration**
- Works with all content, audit, and publishing agents.
- Receives updates from Search Console Analysis and Traffic Decay Detection Agents.

---

## 2. Master Orchestrator Workflow
**Role**
Coordinate agent execution, manage dependencies, and ensure system-wide rules are followed.

**Inputs**
- New topic ideas and briefs
- Published content inventory
- Audit and performance signals

**Outputs**
- Orchestrated workflow plan
- Agent handoff triggers
- Priority queue
- Escalation decisions

**Workflow steps**
1. Receive topic or audit signal.
2. Route tasks to Article Research Agent, SEO Audit Agent, or Opportunity Discovery Agent.
3. Sequence writing, optimization, linking, and publishing agents.
4. Monitor validation and QA results.
5. Approve or pause workflows.
6. Update the publishing calendar.

**Validation rules**
- Ensure URL preservation and category integrity.
- Confirm each page has a pillar and cluster assignment.
- Enforce no automatic publication without approval.

**SEO rules**
- Prioritize high-impact authority and recovery tasks.
- Keep cross-ecosystem balance.
- Avoid executing duplicate or cannibalized content.

**Linking rules**
- Require Internal Linking Agent signoff before publication.
- Enforce pillar and sibling link rules.
- Validate cross-ecosystem links only when relevant.

**Escalation rules**
- Escalate unresolved conflicts to human review.
- Escalate major architecture issues to the team.

**Collaboration**
- Coordinates all 20 agents.
- Uses Publishing Calendar Management Agent for schedule.
- Receives audit data from SEO Audit Agent, Search Console Analysis Agent, and Traffic Decay Detection Agent.

---

## 3. Pipelines

### 3.1 Publishing Pipeline
1. Opportunity Discovery Agent or Article Research Agent creates a brief.
2. SEO Article Writing Agent drafts content.
3. Rank Math Optimization Agent refines SEO.
4. Image Generation Agent creates visual prompts.
5. Internal Linking Agent builds link plan.
6. Content Scoring QA Agent approves content.
7. WordPress Publishing Agent publishes.
8. Publishing Calendar Management Agent logs schedule.

### 3.2 Audit Pipeline
1. SEO Audit Agent crawls and audits content.
2. Traffic Decay Detection Agent identifies declines.
3. Search Console Analysis Agent finds query gaps.
4. Content Scoring QA Agent reviews low-quality pages.
5. Cannibalization Detection Agent flags conflicts.
6. Orphan Page Recovery Agent and Internal Linking Agent build fixes.
7. Master Orchestrator prioritizes actions.

### 3.3 Refresh Pipeline
1. Search Console Analysis or Traffic Decay Detection triggers refresh.
2. Content Refresh Agent creates refresh plan.
3. Article Research Agent updates topical intent if needed.
4. SEO Article Writing Agent revises content.
5. Rank Math Optimization Agent re-optimizes.
6. Internal Linking Agent updates links.
7. Content Scoring QA Agent validates refresh.
8. WordPress Publishing Agent republishes.

### 3.4 Authority Expansion Pipeline
1. SEO Audit Agent identifies weak ecosystems.
2. Topical Authority Expansion Agent builds expansion roadmap.
3. Cluster Management Agent defines missing cluster topics.
4. Article Research Agent validates new opportunities.
5. SEO Article Writing Agent writes new articles.
6. Pillar Authority Building Agent publishes pillar updates.
7. Internal Linking Agent connects new content.
8. WordPress Publishing Agent releases content.
9. Audit Agent tracks authority gains.

---

## 4. System Rules
- Preserve existing URLs, slugs, and WordPress categories.
- Do not rename or remove published indexed URLs without explicit manual approval.
- Use the Lonage global authority map as the source of truth.
- Prefer human review for publishing and major architecture changes.
- Keep article ecosystem assignments consistent.
- Prioritize pillar, cluster, and internal linking integrity.

---

## 5. Agent Collaboration Matrix
- **Master Orchestrator** coordinates all agents.
- **Article Research Agent** feeds SEO Article Writing Agent and Publishing Calendar Management Agent.
- **SEO Article Writing Agent** works with Rank Math, Image Generation, Affiliate Integration, and QA.
- **Internal Linking Agent** validates link structure with Pillar Authority Building and Cluster Management.
- **Rank Math Optimization Agent** collaborates with QA and Publishing Agent.
- **Content Refresh Agent** partners with Search Console, Traffic Decay, and Cannibalization agents.
- **Affiliate Integration Agent** supports writing and publishing in affiliate-relevant articles.
- **WordPress Publishing Agent** executes published output from writing, optimization, and QA.
- **Image Generation Agent** supplies visuals for publishing.
- **SEO Audit Agent** drives the audit and authority expansion pipelines.
- **Cluster Management Agent** ensures all content belongs to correct clusters.
- **Pillar Authority Building Agent** anchors ecosystem authority.
- **Cannibalization Detection Agent** prevents duplicate intent.
- **Orphan Page Recovery Agent** rescues weak content.
- **Cross-Ecosystem Linking Agent** strengthens site-wide authority.
- **Topical Authority Expansion Agent** scales ecosystem coverage.
- **Content Scoring QA Agent** approves quality.
- **Search Console Analysis Agent** provides query-level signals.
- **Traffic Decay Detection Agent** monitors declines.
- **Opportunity Discovery Agent** seeds new pipeline ideas.
- **Publishing Calendar Management Agent** manages execution schedule.

---

## 6. Ecosystem Support
Each agent supports the full Lonage ecosystem set. Agents should use ecosystem-specific language and should not favor Menopause over other verticals.

The system is built to support:
- Menopause
- Healthy Aging
- Fitness After 50
- Nutrition
- Recovery
- Mobility
- Sleep
- Gut Health
- Longevity
- Women’s Wellness

This architecture enables Lonage to scale SEO execution across all ecosystems while preserving existing site structure and delivering predictable, audit-ready workflows.
