# Query Template

SQL queries in this folder follow a standard header so anyone reading them can tell what they answer, who owns them, and when they were last validated.

```sql
-- Title: [Short query title — what question this answers]
-- Pillar: supplier | buyer | operations
-- Owner: [Name]
-- Last validated: YYYY-MM-DD
-- Used by: [dashboard / investigation / Jira ticket reference]
--
-- Description:
--   What this query computes and the assumptions it makes.
--
-- Tables referenced:
--   - finn-data-prod.<dataset>.<table>
--
-- Parameters:
--   @start_date, @end_date  -- analysis window
--   @<param>                -- description

WITH base AS (
  SELECT
    ...
  FROM `finn-data-prod.<dataset>.<table>`
  WHERE event_ts BETWEEN @start_date AND @end_date
)

SELECT
  ...
FROM base;
```

Save real queries as `.sql` files (not `.md`) in the appropriate pillar subfolder. Name files by the metric or question they answer.
