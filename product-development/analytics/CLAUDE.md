# Remarketing Analytics

Analytics resources for FINN Remarketing Tech.

## Contents

| Folder/File | Description |
|-------------|-------------|
| `queries/` | SQL query patterns (BigQuery), organized by pillar |
| `schemas/` | Table documentation for FINN Remarketing data sources, organized by pillar |
| `metrics/` | Metric definitions organized by pillar |
| `dashboards/` | Looker dashboard docs organized by pillar |
| `experiments/` | Experiment results organized by pillar |
| `investigations/` | Ad hoc investigations organized by pillar |
| `playbooks/` | Repeatable analysis playbooks (e.g. funnel-analysis.md) |
| `data-catalog.yaml` | BigQuery dataset/table registry — descriptions, owners, refresh cadence, upstream sources |

All pillar-organized folders use the same three subfolders: `supplier/`, `buyer/`, `operations/`.

---

## Data Sources

| Source | Description | Access |
|--------|-------------|--------|
| BigQuery | Primary data warehouse — vehicle lifecycle events, deal flow, compound operations, finance | SQL via Looker / direct query |
| Looker | Self-serve dashboards, exploration | https://finn.looker.com (TBD — confirm URL with Victor) |
| Amplitude | Product analytics — buyer/supplier portal funnels, retention, feature usage | Amplitude workspace |
| HubSpot | CRM — supplier/buyer account data, deal pipeline, contact history | HubSpot dashboard + BigQuery sync |

---

## Core Metrics

The full KPI tree lives in [strategy/okrs-t2-2026.md](../product/strategy/okrs-t2-2026.md). Headline metrics tracked here:

| Metric | Definition | Owner |
|--------|------------|-------|
| **De-fleeting cycle time** | Median days from subscription end to car sold | Operations + BI |
| **GPU per car (signed)** | Gross profit per unit on signed deals | BI / Finance |
| **Sell-through rate** | % of cars sold through primary channel within target window | Buyer + Operations |
| **GHG quota revenue per car** | Average GHG quota revenue captured per eligible EV | Finance + Operations |
| **Supplier onboarding cycle** | Time from supplier signed to first car processed | Supplier (RaaS) |
| **Auction conversion** | % of listed cars that close in-platform vs. fall back to manual | Buyer |

Additional metrics defined per-pillar in `metrics/`.

---

## Dashboards

Looker is the source of truth for dashboards. This repo holds links + descriptions, not the dashboards themselves. Per-pillar dashboard docs live under `dashboards/{supplier,buyer,operations}/`.

For dashboard-building methodology and Looker conventions, talk to Victor (BI Manager) or David (Staff Data Analyst).

---

## Common Queries

Queries are stored in `queries/{supplier,buyer,operations}/` and named by metric. See `queries/_template.md` for the standard SQL header (purpose, owner, last-validated date).
