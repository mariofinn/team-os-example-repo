# PRDs

## Purpose
Product Requirement Documents for FINN Remarketing Tech features.

PRDs in this repo are intended to **replace Confluence as the source of truth** for new specs. Existing PRDs in [Confluence — Remarketing Tech](https://finn.atlassian.net/wiki/spaces/FP/pages/2319581284/Remarketing+Tech) will be migrated in over time.

---

## Folder Structure

PRDs are organized by pillar:

```
PRDs/
├── _template.md           # Copy this for new PRDs
├── supplier/              # Supplier (RaaS) product PRDs
├── buyer/                 # Buyer / dealer product PRDs
└── operations/            # Compound + customer operations PRDs
```

---

## Naming Convention

```
{pillar}/{feature-name}-prd.md
```

Examples:
- `supplier/supplier-onboarding-prd.md`
- `buyer/dealer-bidding-flow-prd.md`
- `operations/transport-coordination-prd.md`

---

## PRD Template Sections

The full template lives in `_template.md`. At minimum every PRD should cover:

1. **Overview** — problem statement, target user (which pillar's user), success metrics
2. **User Stories / JTBD** — who benefits and what job are they hiring this to do
3. **Requirements** — functional and non-functional, must-have vs. nice-to-have
4. **Design** — UX flows, links to Figma frames
5. **Technical Considerations** — architecture, dependencies, integration points (HubSpot, BigQuery, OEM systems, etc.)
6. **Launch Plan** — rollout strategy, feature flags, success criteria, kill criteria

---

## Linking to Engineering / Analytics

When a PRD ships, link it from `product-development/feature-index.yaml` so the engineering plan, RFC, schema, and metrics are discoverable from one place.
