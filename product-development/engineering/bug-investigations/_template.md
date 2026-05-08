# Bug: [short description] — Investigation

**Date opened:** YYYY-MM-DD
**Investigator:** [Name]
**Severity:** P0 | P1 | P2 | P3
**Pillar:** supplier | buyer | operations
**Jira:** FRT-XXX

(File path convention: `bug-investigations/{pillar}/bug-{YYYY-MM-DD}-{short-description}/investigation-plan.md`.)

---

## Symptom

What's broken from the user's / system's perspective. Observed behaviour. Expected behaviour.

## Impact

- Who is affected (which suppliers, buyers, ops users)?
- How many cars / deals / users affected?
- Workarounds in place?

## Hypotheses

| # | Hypothesis | How to test | Status |
|---|------------|-------------|--------|
| 1 | | | Open |
| 2 | | | Open |

## Findings

Document evidence as you go: log snippets, BigQuery counts, repro steps.

## Root cause

Once known: the underlying cause and why it surfaced now.

## Fix

- Code/config change
- Tests added
- Backfill / cleanup needed

## Prevention

What stops this happening again — alert, test, schema constraint, runbook update.
