# Customer Insights

Customer feedback, account context, and call notes for FINN Remarketing's named buyer and supplier accounts.

## FINN-side ownership

For who at FINN owns which commercial relationships (suppliers, buyers, BD, VP), see [`finn-commercial-ownership.md`](finn-commercial-ownership.md). When creating a new `account-context.md`, fill the `FINN owner (commercial)` field from that doc (suppliers) or from the HubSpot company-record owner (buyers).

## Account Types

| Type | Folder | Who they are |
|------|--------|--------------|
| Buyers | `accounts/buyers/` | B2B trade buyers — independent dealers, dealer groups, trade buyers purchasing cars from FINN |
| Suppliers | `accounts/suppliers/` | OEMs and leasing partners using FINN's remarketing capability as a service (RaaS) |

Self-serve / long-tail accounts are tracked through aggregate analytics in HubSpot and BigQuery, not in this repo.

## Named Accounts

### Suppliers (in flight)

| Account | Folder | Status |
|---------|--------|--------|
| Nissan | [accounts/suppliers/nissan/](accounts/suppliers/nissan/) | RaaS discovery / pilot prep |
| Renault | [accounts/suppliers/renault/](accounts/suppliers/renault/) | RaaS discovery |
| MG | [accounts/suppliers/mg/](accounts/suppliers/mg/) | RaaS discovery |

Source: `research/supplier-discovery-synthesis.md` (4 interviews — Nissan x2, Renault x1, MG x1).

### Buyers

To be backfilled from December 2025 buyer call notes.

## Finding Customer Data

| Looking for... | Where to find it |
|----------------|-----------------|
| Account context, goals, risks | `accounts/{type}/{account}/account-context.md` |
| Call summaries | `accounts/{type}/{account}/calls/summaries/` |
| Call transcripts | `accounts/{type}/{account}/calls/transcripts/` |
| Cross-account research, pain points, discovery synthesis | `research/` |
| Pipeline / deal stage / contacts | HubSpot |
| Tickets and feature requests | Jira `FRT` project, filter by customer label |
| Aggregate analytics | `../../analytics/` (organized by pillar, not by customer) |

## Research

| File | Description |
|------|-------------|
| `research/supplier-pain-points.md` | Cross-supplier pain points synthesis (Nissan x2, Renault x1, MG x1) |
| `research/supplier-discovery-synthesis.md` | Synthesis of supplier discovery interviews |
| `research/buyer-portal-context.md` | Buyer portal product context — Dealer Portal Refactoring (Retool → Pro-Code) |
| `research/competitive-raas-platforms.md` | Competitive landscape for RaaS platforms |
| `research/supplier-oem-stakeholder-profiles.md` | OEM-side partner contacts (Nissan/Renault/MG): roles, operating models, what they value |

## Processing Customer Calls

When processing a new customer call (use the `/customer-call` slash command):

1. Identify whether this is a buyer or supplier
2. Save summary to `accounts/{type}/{account}/calls/summaries/{YYYY-MM-DD}.md`
3. Save transcript to `accounts/{type}/{account}/calls/transcripts/{YYYY-MM-DD}.md`
4. Update `accounts/{type}/{account}/account-context.md` with new insights, blockers, action items
5. Log feature requests in Jira `FRT` with the appropriate customer label
