# Funnel Analysis Playbook

A repeatable methodology for investigating conversion funnels across the FINN Remarketing pillars (supplier, buyer, operations).

## When to Use This Playbook

- A funnel metric (e.g., supplier onboarding completion, dealer bid-to-purchase conversion, compound throughput) drops below target
- Product or engineering requests a funnel investigation for a new or changed flow
- You need to identify the highest-leverage drop-off point to improve

## Step-by-Step Methodology

### 1. Define the Funnel Steps
- Identify the discrete steps in the user/vehicle flow
- Map each step to a measurable event in BigQuery (or Amplitude, for portal interactions)
- Example (de-fleeting): `subscription_ended` → `intake_scheduled` → `vehicle_arrived_at_compound` → `condition_report_signed` → `listed_for_sale` → `sold` → `paid_out`

### 2. Pull the Funnel Data
- Query the event tables for each step over the analysis window
- Use a CTE-based approach to count unique entities (users for portal funnels, vehicles for de-fleeting funnels) at each step:

```sql
WITH funnel AS (
    SELECT
        vehicle_id,
        MIN(CASE WHEN event = 'step_1' THEN event_ts END) AS step_1_at,
        MIN(CASE WHEN event = 'step_2' THEN event_ts END) AS step_2_at,
        MIN(CASE WHEN event = 'step_3' THEN event_ts END) AS step_3_at
    FROM `finn-data-prod.remarketing.vehicle_events`
    WHERE event_ts BETWEEN @start_date AND @end_date
    GROUP BY vehicle_id
)
SELECT
    COUNT(step_1_at) AS step_1_count,
    COUNT(step_2_at) AS step_2_count,
    COUNT(step_3_at) AS step_3_count,
    ROUND(COUNT(step_2_at) / NULLIF(COUNT(step_1_at), 0) * 100, 1) AS step_1_to_2_pct,
    ROUND(COUNT(step_3_at) / NULLIF(COUNT(step_2_at), 0) * 100, 1) AS step_2_to_3_pct
FROM funnel;
```

(Replace the dataset / table with the real BigQuery path — see `../data-catalog.yaml`.)

### 3. Identify the Largest Drop-off
- Calculate step-to-step conversion rates
- Flag the step with the largest absolute drop-off
- Segment by cohort (vehicle make/model, supplier, buyer segment, compound location) to see if the drop-off is universal or concentrated

### 4. Investigate Root Causes
- For portal flows: pull Amplitude session recordings around the drop-off step
- Check for error / timeout / SLA-miss events near the drop-off
- Look at time-between-steps to identify where things stall vs. where they abandon entirely
- For physical flows (compound, transport): check status/notes fields for operational blockers

### 5. Quantify the Opportunity
- Calculate the impact of closing the gap: "If we improved step X conversion from Y% to Z%, we'd gain N additional cars sold per week / €N additional GPU per month"
- Tie to KPI tree in `../../product/strategy/okrs-t2-2026.md`

### 6. Recommend and Track
- Propose specific interventions (UX changes, error-message rewrites, SLA changes, ops process tweaks)
- Set up a Looker dashboard or scheduled BigQuery query to track the metric post-intervention
- Document findings in an investigation file under `../investigations/{pillar}/`

## Where worked examples live

Add links here as we run real investigations. Each investigation under `../investigations/{pillar}/` should follow this playbook's steps.
