# Bi-Weekly Update Workflow Spec

## Overview

This workflow produces a dated bi-weekly Remarketing Tech review document. It runs interactively: each step has an automated part (data gathering, drafting) and an interactive part (the PM reviews, adds context, approves). Each section is written to the output file as it completes so progress is visible in real time. The final step auto-pushes the compiled document to a Google Doc via the Google Workspace MCP.

---

## Process Flow

```
1. Create dated output file
2. Step 1: Engineering Status     -> writes "What the Team Is Building Now" section
3. Step 2: Customer Call Synthesis -> writes "Customer Calls" section
4. Step 3: Customer Updates       -> writes pilot/launch status sections
5. Step 4: Push to Google Doc     -> auto-push via Google Workspace MCP
6. Step 5: Review & Finalization  -> PM reviews, edits, publishes
```

Each step reads its own instruction file (`step-1-eng-status.md`, etc.) for detailed process.

---

## What Changes Every Cycle vs. What's Stable

### Changes every cycle
- **Eng status:** Workstream statuses update based on Jira `FRT` + PM's context dump
- **Customer calls section:** Completely rewritten each cycle based on last 2 weeks of calls
- **What We're Hearing / Highlights:** Completely rewritten based on new call data
- **Pilot/customer exec summaries:** Updated only if new call data changes the narrative

### Stable across cycles (carried forward, not rewritten)
- **OKR structure and goals:** Updated only when OKRs change (per trimester — see `okrs-t1-2026.md`, `okrs-t2-2026.md`)
- **Customer deep-dive background sections:** Only updated when materially new info emerges
- **Cross-customer summary:** Updated when shared gaps change or new customers are added
- **Table of Contents structure:** Updated when sections are added or removed

---

## Conventions

### Formatting
- Business-goal-led headings (not feature-led)
- Customer quotes: *"Quote text."* — Speaker Name
- No em dashes in body text (use commas, semicolons, or sentence breaks)
- No horizontal rules between sections
- Tables and bullets for scannable content; paragraphs for narrative

### Customer Categorization
Each customer in the call synthesis table gets one of these categories:

| Category | Definition |
|----------|------------|
| Supplier — pilot | Active RaaS supplier pilot |
| Supplier — discovery | RaaS prospect in discovery / scoping |
| Buyer — active | Active B2B dealer / trade buyer using FINN's buyer product |
| Buyer — pilot | Buyer in pilot / onboarding |
| Buyer — pipeline | Buyer in sales pipeline, not yet onboarded |
| Internal | Internal Remarketing ops stakeholder (not a customer per se but worth tracking) |

### Output File Header

```markdown
# Remarketing Tech Bi-Weekly Review — {YYYY-MM-DD}

**Period:** {start_date} → {end_date}
**Compiled by:** Mario Schiefer
**Audience:** Remarketing leadership + cross-functional partners
```

---

## Configuration

The workflow keeps the following references stable across runs:

- Jira project key: `FRT`, board 245
- OKR file pointer: latest `okrs-tN-YYYY.md` under `../../strategy/`
- Supplier accounts root: `../../suppliers/accounts/`
- Buyer accounts root: `../../buyers/accounts/`
- Output dir: `../../meetings/team-bi-weekly/docs/`
- Google Doc target: stored in workflow config (a single rolling doc by default)
