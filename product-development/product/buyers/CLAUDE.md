# Buyers (B2B dealers / trade buyers)

Account context, calls, and research for FINN's buyer side — independent dealers, dealer groups, trade buyers, and any other B2B counterparty purchasing cars from FINN. Maps to the `buyer/` pillar.

## Folder layout

```
buyers/
├── CLAUDE.md                       # this file
├── finn-commercial-ownership.md    # internal buyer-side owners (Sales Managers) + BD/VP context
├── accounts/
│   ├── _template.md                # copy this when creating a new buyer folder
│   └── {accounts as we add them}
└── research/
    └── buyer-portal-context.md
```

## Active accounts

To be backfilled from December 2025 buyer call notes. Each account gets its own folder with `account-context.md` plus `calls/summaries/` and `calls/transcripts/`.

## Where to find buyer data

| Looking for... | Where |
|----------------|-------|
| Account context, goals, risks | `accounts/{name}/account-context.md` |
| Call summaries | `accounts/{name}/calls/summaries/` |
| Call transcripts | `accounts/{name}/calls/transcripts/` |
| Cross-buyer research (portal context, segment patterns) | `research/` |
| Pipeline / deals / contacts | HubSpot |
| Tickets and feature requests | Jira `FRT` project, filter by buyer label |
| Aggregate analytics | `../../analytics/` (organized by pillar) |
| Competitor intel for buyer-side conversations | [`../competitive-research/`](../competitive-research/CLAUDE.md) — especially CarOnSale, Auto1, AUTOproff |

## FINN-side ownership

Buyer accounts are owned by the relevant Remarketing Sales Manager (per HubSpot company-record owner). See [`finn-commercial-ownership.md`](finn-commercial-ownership.md).

## Processing buyer calls

Use the `/customer-call` slash command. It will:
1. Ask which buyer
2. Save summary to `accounts/{name}/calls/summaries/{YYYY-MM-DD}.md`
3. Save transcript to `accounts/{name}/calls/transcripts/{YYYY-MM-DD}.md`
4. Update `accounts/{name}/account-context.md` with new insights / action items
5. File feature requests in Jira `FRT` with the buyer + pillar labels
