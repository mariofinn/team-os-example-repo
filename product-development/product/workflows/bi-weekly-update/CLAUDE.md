# Bi-Weekly Update Workflow

## Purpose

Automated workflow that generates the bi-weekly Remarketing Tech review document. Runs before each bi-weekly review meeting and compiles engineering progress, customer call themes, and stakeholder updates into a presentation-ready format.

## What This Workflow Does

1. **Pulls engineering status** from Jira (`FRT` board) + PM context dump
2. **Synthesizes recent customer calls** from `product-development/product/{suppliers,buyers}/accounts/*/calls/summaries/`
3. **Updates customer/pilot exec summaries** if new call data changes the narrative
4. **Pushes the compiled doc** to the bi-weekly Google Doc via the Google Workspace MCP
5. **PM reviews and finalizes** before the meeting

## Steps Overview

Each step has its own instruction file (`step-1-eng-status.md`, etc.) with detail.

1. Pull eng status by OKR / pillar — writes "What the Team Is Building Now"
2. Customer call synthesis — writes "Customer Calls" section
3. Customer / pilot updates — refreshes per-account exec summaries
4. Push to Google Doc
5. PM review and sign-off

## Output Location

`product-development/product/meetings/team-bi-weekly/docs/{YYYY-MM-DD}-bi-weekly-review.md`

## Source-of-truth files this workflow reads

- Jira `FRT` (board 245) — completed and in-progress tickets
- [Current OKRs](../../strategy/okrs-t2-2026.md) — workstream structure
- `product-development/product/suppliers/accounts/{name}/calls/summaries/` and `product-development/product/buyers/accounts/{name}/calls/summaries/` — recent customer calls
- The previous bi-weekly review doc (carry-forward content)

## File Naming

Output files: `{YYYY-MM-DD}-bi-weekly-review.md`
