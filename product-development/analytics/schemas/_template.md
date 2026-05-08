# [Table name]

**Full path:** `finn-data-prod.<dataset>.<table>`
**Pillar:** supplier | buyer | operations | shared
**Owner:** [Data eng / BI]
**Refresh:** [event-stream / hourly / daily HH:MM UTC]

---

## What this table is

One paragraph describing what each row represents (one vehicle, one event, one supplier-day, etc.) and what this table is the source of truth for.

## Columns

| Column | Type | Nullable | Description |
|--------|------|----------|-------------|
| `id` | STRING | No | Primary key |
| | | | |

## Partitioning / clustering

- Partition: `[column]` (e.g., `DATE(event_ts)`)
- Cluster: `[columns]`

## Source

- Upstream: [event source / app / Make.com scenario / HubSpot sync]
- Pipeline doc: `../../data-engineering/plans/{pillar}/{name}.md`

## Used by

- Queries: `../queries/{pillar}/`
- Looker explores:
- Dashboards:
