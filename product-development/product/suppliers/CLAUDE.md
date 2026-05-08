# Suppliers (RaaS)

Account context, calls, and research for FINN's RaaS supplier side — OEMs and leasing partners using FINN's remarketing capability as a service. Maps to the `supplier/` pillar.

## Folder layout

```
suppliers/
├── CLAUDE.md                       # this file
├── finn-commercial-ownership.md    # internal supplier-side owners (Tim, Annalisa) + BD/VP context
├── accounts/
│   ├── _template.md                # copy this when creating a new supplier folder
│   ├── nissan/
│   ├── renault/
│   └── mg/
└── research/
    ├── supplier-discovery-synthesis.md
    ├── supplier-pain-points.md
    └── oem-stakeholder-profiles.md
```

## Active accounts

| Supplier | Folder | Status |
|----------|--------|--------|
| Nissan | [`accounts/nissan/`](accounts/nissan/) | RaaS discovery / pilot prep |
| Renault | [`accounts/renault/`](accounts/renault/) | RaaS discovery |
| MG | [`accounts/mg/`](accounts/mg/) | RaaS discovery |

Source: [`research/supplier-discovery-synthesis.md`](research/supplier-discovery-synthesis.md) (4 interviews — Nissan x2, Renault x1, MG x1).

## Where to find supplier data

| Looking for... | Where |
|----------------|-------|
| Account context, goals, risks | `accounts/{name}/account-context.md` |
| Call summaries | `accounts/{name}/calls/summaries/` |
| Call transcripts | `accounts/{name}/calls/transcripts/` |
| Cross-supplier pain points / discovery synthesis | `research/` |
| OEM-side partner contacts (roles, operating models, what they value) | [`research/oem-stakeholder-profiles.md`](research/oem-stakeholder-profiles.md) |
| Pipeline / deals / contacts | HubSpot |
| Tickets and feature requests | Jira `FRT` project, filter by supplier label |
| Aggregate analytics | `../../analytics/` (organized by pillar) |
| Competitor intel for supplier conversations | [`../competitive-research/`](../competitive-research/CLAUDE.md) |

## FINN-side ownership

Supplier accounts have two internal owners (Relationships + Operations) plus cross-cutting BD and VP roles. See [`finn-commercial-ownership.md`](finn-commercial-ownership.md).

## Processing supplier calls

Use the `/customer-call` slash command. It will:
1. Ask which supplier
2. Save summary to `accounts/{name}/calls/summaries/{YYYY-MM-DD}.md`
3. Save transcript to `accounts/{name}/calls/transcripts/{YYYY-MM-DD}.md`
4. Update `accounts/{name}/account-context.md` with new insights / action items
5. File feature requests in Jira `FRT` with the supplier + pillar labels
