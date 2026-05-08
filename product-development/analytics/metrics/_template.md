# [Metric name]

**Pillar:** supplier | buyer | operations
**Owner:** [Analyst / BI]
**Type:** KPI | input metric | guardrail | diagnostic
**Status:** Active | Deprecated

---

## Definition

A precise, unambiguous definition. Someone reading this should be able to reproduce the metric without asking.

**Formula:**

```
[Plain-English or pseudocode formula]
```

## Source data

- Dataset(s): `finn-data-prod.<dataset>`
- Table(s): `<table>`
- Filters / segmentation: [what's included / excluded]

## Refresh cadence

How often the underlying data updates and where the metric is surfaced (Looker, Amplitude, dashboard).

## Why it matters

What decision this metric drives. Tie back to OKRs / business outcome.

## Known caveats

- [Edge case]
- [Known data-quality issue]
- [Comparison gotcha]

## Related

- Query: `../queries/{pillar}/{file}.sql`
- Schema: `../schemas/{pillar}/{file}.md`
- Dashboard: [Looker URL]
