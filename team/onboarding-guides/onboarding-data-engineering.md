# Onboarding: Data Engineering

Data engineering-specific setup and orientation for data engineers joining FINN Remarketing Tech.

## Setup

### Shared Tools (everyone gets these)

See [General Onboarding](onboarding-general.md#shared-tools-everyone-gets-these).

### Function-Specific Tools

| Tool | Purpose | Access |
|------|---------|--------|
| BigQuery | Data warehouse | Request access from Victor Franz |
| dbt | Data transformations and modeling | Access via the dbt repo (confirm name with Data Eng lead) |
| Fivetran / data-ingestion stack | Ingestion pipelines | Request from Data Eng lead |
| Airflow / Cloud Composer | Pipeline orchestration | Request from Data Eng lead |
| GCP Console | BigQuery, Cloud Storage, Cloud Functions | Request from EM |
| Make.com / Celonis | Operational scenarios that produce data into BigQuery | Request as needed — see [`product-context/make-platform.md`](../../product-development/product/product-context/make-platform.md) |

### Repos

| Repo | Why |
|------|-----|
| `finn-auto/team-os-example-repo` | Pipeline plans, RFCs, data-catalog |
| `finn-auto/<dbt-repo>` | dbt models, schema docs |
| Other data infra repos | Confirm with Data Eng lead |

### Environment Setup

1. Complete [General Onboarding](onboarding-general.md) setup first
2. Clone the dbt repo and follow its `CONTRIBUTING.md` for local setup
3. Get BigQuery access and connect your SQL client
4. Set up local dbt and run a test build against a dev schema
5. Review Airflow/Composer DAGs and current pipeline schedule

## Key Documents

- [Data Engineering CLAUDE.md](../../product-development/data-engineering/CLAUDE.md) — plans / RFCs by pillar
- [Analytics CLAUDE.md](../../product-development/analytics/CLAUDE.md) — downstream consumer context
- [data-catalog.yaml](../../product-development/analytics/data-catalog.yaml) — canonical dataset/table registry
- [Product CLAUDE.md](../../product-development/product/CLAUDE.md) — domain context for what data matters

## Slack Channels

| Channel | Purpose |
|---------|---------|
| `#rem_tech_general` | Team-wide announcements |
| `#rem_tech_internal` | Internal team discussions |

Plus FINN-wide data / infra channels — confirm with your manager.

## People to Meet

| Person | Why |
|--------|-----|
| Victor Franz | BI lead — pipeline architecture, downstream priorities |
| David Burgschwaiger | Staff Analyst — primary downstream consumer |
| Marco Milovanovic | EM — upstream service teams that produce events |
| Mario Schiefer | PM — what data unblocks which decisions |

## First Tasks

- [ ] Get BigQuery + dbt + orchestration access
- [ ] Run a local dbt build against the dev schema
- [ ] Review the current DAG schedule and pipeline dependencies
- [ ] Trace one pipeline end-to-end (source → ingestion → transformation → Looker / Amplitude)
- [ ] Meet with Victor + Data Eng lead for architecture walkthrough
- [ ] Pick up a small pipeline task from Jira `FRT`
