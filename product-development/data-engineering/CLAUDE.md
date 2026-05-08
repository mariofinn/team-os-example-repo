# Data Engineering

Data pipeline plans and RFCs for FINN Remarketing Tech. Organized by pillar.

## Folders

| Folder | What's Here |
|--------|-------------|
| `plans/` | Data pipeline implementation plans |
| `rfcs/` | Data pipeline design proposals |

## Pillars

Both folders share the same pillar structure:

| Pillar | Subfolder | Examples of work |
|-------------|-----------|-------------|
| Supplier (RaaS) | `supplier/` | Supplier event ingestion, OEM data integration, supplier-side reporting pipelines |
| Buyer / Dealer | `buyer/` | Auction/deal event modeling, buyer behaviour streams, dealer reporting feeds |
| Operations | `operations/` | Compound workflow events, transport status pipelines, GHG quota data, document tracking |

## Naming Conventions

- **Plans:** `{pipeline-name}.md` (e.g., `supplier-onboarding-events.md`)
- **RFCs:** `{pipeline-name}-rfc.md`

## Where the data lands

Most pipelines target BigQuery datasets — see `../analytics/data-catalog.yaml` for the canonical dataset/table registry.
