# [Pipeline name] — Data Engineering Plan

**Status:** Draft | In Review | Approved | In Progress | Shipped
**Author:** [Data eng]
**Pillar:** supplier | buyer | operations
**Last updated:** YYYY-MM-DD
**Related:** [RFC] · [PRD] · [Jira FRT-XXX]

---

## 1. What this pipeline produces

The dataset(s) and table(s) this pipeline lands. Reference `../../analytics/data-catalog.yaml` after the table is registered.

## 2. Sources

| Source | Type | Notes |
|--------|------|-------|
| | event stream / DB / API / Make.com / HubSpot | |

## 3. Destination

- BigQuery dataset(s):
- Table(s):
- Owner / consumer:

## 4. Transformations

- Tool: dbt / native SQL / Airflow / Cloud Functions / etc.
- Key transformations:
- Refresh cadence:

## 5. Schema

Either inline the table schema or link to a schema doc under `../../analytics/schemas/{pillar}/`.

## 6. Backfill plan

How we populate history when this ships.

## 7. Monitoring

- Freshness checks
- Row-count / null-rate checks
- Alerting destination (Slack channel, PagerDuty)
