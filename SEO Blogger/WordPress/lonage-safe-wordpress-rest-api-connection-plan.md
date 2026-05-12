# Lonage Safe WordPress REST API Connection Plan

## Purpose
Create a secure, reliable, and low-risk method for connecting automation tools (AI workflows, scripts, and integrations) to the Lonage WordPress site via the WordPress REST API.

---

## 1) Security Principles (Non-Negotiables)

1. **Least privilege access**
   - Use a dedicated integration user account.
   - Grant only the minimum role/capabilities needed.
   - Do not use the site owner/admin account for automation.

2. **Credential isolation**
   - Store API credentials only in environment variables or a secret manager.
   - Never hardcode credentials in scripts, prompts, or repository files.
   - Rotate credentials on a schedule and immediately after suspected exposure.

3. **Transport security**
   - Enforce HTTPS only.
   - Reject plain HTTP and mixed-content endpoints.

4. **Controlled write operations**
   - Restrict which endpoints are allowed for write/update/delete.
   - Add approval checkpoints for destructive actions (delete/unpublish).

5. **Auditability**
   - Log every API write action with timestamp, actor, endpoint, post ID, and result.
   - Keep logs outside publicly accessible directories.

---

## 2) Recommended Authentication Method

### Preferred: Application Passwords (WordPress native)
Use a dedicated WordPress user + Application Password for server-to-server automation.

**Why this is preferred:**
- Native to modern WordPress.
- Can be revoked per application without resetting the user password.
- Works cleanly over HTTPS with basic auth format.

### Implementation Steps
1. Create integration user (example: `lonage_api_bot`).
2. Assign role with minimum required permissions (Editor only if post publishing is necessary).
3. Generate an Application Password named by tool/pipeline.
4. Save credentials in secure secret storage:
   - `WP_API_BASE_URL`
   - `WP_API_USERNAME`
   - `WP_API_APP_PASSWORD`
5. Test read-only endpoint first (`/wp-json/wp/v2/posts`).
6. Then test constrained write endpoint with a draft post.

---

## 3) Access Scope and Endpoint Policy

## Allowed endpoints (baseline)
- `GET /wp-json/wp/v2/posts`
- `GET /wp-json/wp/v2/categories`
- `GET /wp-json/wp/v2/tags`
- `POST /wp-json/wp/v2/posts` (draft only by default)
- `POST /wp-json/wp/v2/posts/<id>` (update allowed fields only)

## Blocked or restricted by policy
- Permanent deletion (`force=true`) unless manual approval.
- User/role management endpoints.
- Plugin/theme update endpoints from automation.

## Field-level controls
Only permit automation to set/update:
- `title`
- `content`
- `excerpt`
- `status` (draft/pending by default)
- `categories`
- `tags`
- selected `meta` keys (explicit allowlist)

---

## 4) Environment & Secrets Management

1. Keep credentials in `.env` (local), CI secrets, or vault.
2. Add `.env` and secret files to `.gitignore`.
3. Use separate credentials for:
   - local development
   - staging
   - production
4. Rotate app passwords every 60–90 days.
5. Immediately revoke if logs show unknown IP/user agent.

---

## 5) Safe Workflow for AI/Automation Publishing

1. **Draft-only default**
   - Automation creates/updates posts as `draft`.
   - Human editor reviews before publish.

2. **Two-step publish gate**
   - Step A: AI writes content and metadata.
   - Step B: Human verifies facts, links, formatting, and brand voice.

3. **Rate limiting and retries**
   - Add capped retries with exponential backoff.
   - Respect host/WAF rate limits.

4. **Idempotency pattern**
   - Track external content ID to avoid duplicate post creation.

5. **Rollback readiness**
   - Keep previous post revision IDs.
   - Document quick rollback procedure in incident notes.

---

## 6) Validation and Monitoring Checklist

Before go-live:
- [ ] HTTPS certificate valid.
- [ ] Integration user is not admin unless strictly required.
- [ ] App password stored in secret manager (not plaintext docs).
- [ ] Read and write endpoint tests pass.
- [ ] Draft creation + update tested end-to-end.
- [ ] Logging enabled for all write operations.
- [ ] Alerting set for repeated 401/403/429/5xx responses.

Ongoing:
- [ ] Weekly review of API logs and failed auth attempts.
- [ ] Monthly credential/access review.
- [ ] Quarterly disaster-recovery drill for content rollback.

---

## 7) Incident Response Mini-Plan

If compromise is suspected:
1. Revoke Application Password immediately.
2. Disable integration user temporarily.
3. Review recent API write logs and post revisions.
4. Restore affected content from known good revisions/backups.
5. Generate new credentials and rotate dependent secrets.
6. Re-enable automation only after root-cause review.

---

## 8) Minimal Connection Test (Example)

```bash
curl -u "$WP_API_USERNAME:$WP_API_APP_PASSWORD" \
  "$WP_API_BASE_URL/wp-json/wp/v2/posts?per_page=1"
```

Expected result: JSON response with post objects and HTTP 200.

---

## 9) Lonage Operational Recommendation

For Lonage, keep automation in **draft-first mode** permanently, with manual editorial approval required for publication. This reduces brand, legal, and SEO risk while still enabling efficient AI-assisted workflows.
