# Onboarding: Analytics

Analytics-specific setup and orientation for analysts joining FINN Remarketing Tech.

## Setup

### Shared Tools (everyone gets these)

See [General Onboarding](onboarding-general.md#shared-tools-everyone-gets-these).

### Function-Specific Tools

| Tool | Purpose | Access |
|------|---------|--------|
| BigQuery | Data warehouse, SQL queries | Request access from Victor Franz |
| Looker | Dashboards, exploration, modeled metrics | Request access from Victor Franz |
| Amplitude | Product analytics for buyer/supplier portal funnels | Request access from Victor Franz |
| HubSpot | CRM data — pipeline, contacts, deals | Request access from Sales Ops |
| dbt | Data transformations (read access) | Confirm with Data Eng |

### Repos

| Repo | Why |
|------|-----|
| `finn-auto/team-os-example-repo` | Analytics docs, metric definitions, investigation write-ups |
| `finn-auto/<dbt-repo>` | dbt models, schema definitions (confirm repo name with Data Eng) |

### Environment Setup

1. Complete [General Onboarding](onboarding-general.md) setup first
2. Get BigQuery access and connect your SQL client
3. Get Looker access and bookmark the Remarketing dashboards
4. Get Amplitude access and explore existing portal funnels
5. Skim [analytics/CLAUDE.md](../../product-development/analytics/CLAUDE.md) and the data catalog for table structures

## Key Documents

- [Analytics CLAUDE.md](../../product-development/analytics/CLAUDE.md) — metrics, data sources, common queries
- [data-catalog.yaml](../../product-development/analytics/data-catalog.yaml) — BigQuery dataset/table registry
- [Funnel-analysis playbook](../../product-development/analytics/playbooks/funnel-analysis.md)
- [OKRs](../../product-development/product/strategy/okrs-t2-2026.md) — KPI tree and what we're moving
- [Customer Insights](../../product-development/product/customers/CLAUDE.md) — qualitative data to pair with quantitative

## Slack Channels

| Channel | Purpose |
|---------|---------|
| `#rem_tech_general` | Where data questions usually surface |
| `#rem_tech_internal` | Internal team discussions |

Plus FINN-wide BI / data channels — Victor will add you.

## People to Meet

| Person | Why |
|--------|-----|
| Victor Franz | Senior BI Manager — metrics, dashboards, data access |
| David Burgschwaiger | Staff Data Analyst — current investigations, dashboards |
| Mathilde Rychel | Associate Data Analyst — analytics peer |
| Mario Schiefer | PM — what metrics matter most this trimester |
| Lucy Mueller | Strategy & BI intern — partner on cross-team analyses |

## First Tasks

- [ ] Get BigQuery access and run a sample query against a Remarketing event table
- [ ] Review the metrics in [analytics/CLAUDE.md](../../product-development/analytics/CLAUDE.md) and the OKR KPI tree
- [ ] Explore 2–3 existing Looker dashboards to understand current reporting
- [ ] Meet with Victor + David for context transfer on current analytics projects
- [ ] Reproduce one existing analysis to validate your understanding of the data
- [ ] Pick up a small analytics task from Jira `FRT`
