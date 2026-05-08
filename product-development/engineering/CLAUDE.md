# Engineering

Engineering plans, RFCs, and bug investigations for FINN Remarketing Tech. All organized by pillar.

## Folders

| Folder | What's Here |
|--------|-------------|
| `plans/` | Implementation plans for upcoming features |
| `rfcs/` | Technical design proposals and architecture decisions |
| `bug-investigations/` | Dated investigation plans for production bugs |

## Pillars

All three folders share the same pillar structure:

| Pillar | Subfolder | What's Here |
|-------------|-----------|-------------|
| Supplier (RaaS) | `supplier/` | Supplier portal, pricing flows, OEM integration |
| Buyer / Dealer | `buyer/` | Dealer portal, auction mechanics, deal flow, buyer KYC |
| Operations | `operations/` | Compound ops (tyre, deregistration, refurb) + customer ops (PoA, transport, papers) |

## Naming Conventions

- **Plans:** `{feature-name}.md` (e.g., `dealer-bidding-flow.md`)
- **RFCs:** `{feature-name}-rfc.md` (e.g., `dealer-bidding-flow-rfc.md`)
- **Bug investigations:** `bug-{YYYY-MM-DD}-{short-description}/investigation-plan.md` (e.g., `bug-2026-05-08-supplier-export-stuck/investigation-plan.md`)

## Where the work is tracked

| System | Use |
|--------|-----|
| Jira `FRT` project | Tickets, sprints, roadmap surface (board 245) |
| GitHub `finn-auto` org | Code, PRs, code review |
| This repo | Plans, RFCs, investigations — the durable design artefacts |
