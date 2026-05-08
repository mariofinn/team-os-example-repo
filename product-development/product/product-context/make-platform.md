# Make.com / Celonis — Platform Reference

**System:** Make.com (acquired by Celonis — URLs use the `celonis.com` domain)
**FINN tenant:** EU1 region, organization 6519
**Base URL:** `https://eu1.make.celonis.com/6519/`

---

## What it is

Make.com is a low-code automation platform. At FINN, it acts as the **glue between systems** — chaining together BigQuery, HubSpot, Google Workspace, internal FINN APIs, and external SaaS endpoints — where building a fully-coded service would be overkill.

Originally `make.com`. Acquired by Celonis; the URLs you'll see in PRs, RFCs, and Slack now point at `eu1.make.celonis.com`. Same product.

---

## How FINN Remarketing uses it

Operational automations live in Make when:

- The work spans 2+ external systems and a webhook / API chain is enough
- Ops needs to inspect or restart runs without calling engineering
- The logic is stable but plumbing-heavy (data transforms, lookups, retries)

Work that is **core domain logic** with high test or observability needs lives in code in the relevant `finn-auto/*` repo, not in Make.

Bidirectional shape of the integration:

- **Make → FINN backend** — scenarios call FINN APIs (e.g. for orchestration steps like the `/additional-transactions` endpoints under [Separate Deductible Invoicing](../../engineering/rfcs/buyer/separate-deductible-invoicing-rfc.md))
- **FINN backend → Make** — scenarios poll FINN APIs / consume webhooks for new work
- **Make → external** — scenarios push to HubSpot, Google Drive, invoicing services, etc.

---

## Where things live

| Resource | URL pattern |
|----------|-------------|
| Scenarios | `https://eu1.make.celonis.com/6519/scenarios/{id}/edit` |
| Functions (custom IML helpers) | `https://eu1.make.celonis.com/6519/functions/{id}` |
| Run history per scenario | inside the scenario page |

Both scenarios and functions are addressed by **numeric IDs**. Scenario names are often suffixed with the creator's email handle — useful for finding ownership at a glance.

---

## Ownership

A Make scenario is owned by whoever created it. When the original creator stops touching it (handover, role change, leaver), the new owner of the *feature* the scenario supports should take it over and update the scenario name / description.

For non-trivial scenarios that are part of a PRD or RFC, name the owner in the RFC's "Reviewers" line so it's findable from the repo as well as from Make.

---

## Access

Request access via your EM (Marco). Engineers and data engineers typically get access during onboarding; PM and Ops as the work demands.

---

## When to document a scenario in this repo

Document scenarios sparingly — Make is the source of truth for the scenario itself. Capture context in this repo only when:

- The scenario implements logic that is part of a PRD / RFC — document **inline** in the RFC, with the scenario URL embedded (the [Separate Deductible Invoicing RFC](../../engineering/rfcs/buyer/separate-deductible-invoicing-rfc.md) is the canonical example)
- The scenario owns a meaningful SLA or business-critical path — capture it in the relevant pillar's `CLAUDE.md`
- A new pipeline / integration is being designed — RFC-level doc, with the Make scenario(s) listed as part of the implementation steps

For routine automations (nothing surprising about what they do or why), no doc needed. The scenario name + description in Make should be self-explanatory.

---

## Related

- [`../../analytics/data-catalog.yaml`](../../analytics/data-catalog.yaml) — references Make scenarios as data sources for BigQuery datasets where applicable
- [`../../engineering/rfcs/buyer/separate-deductible-invoicing-rfc.md`](../../engineering/rfcs/buyer/separate-deductible-invoicing-rfc.md) — example RFC that pins down specific scenario and function IDs in context
- The Make MCP integration exposes a subset of FINN scenarios as Claude-callable tools (useful for ad-hoc operations; not a substitute for documentation)
