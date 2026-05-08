# Onboarding: Engineering

Engineering-specific setup and orientation for engineers joining FINN Remarketing Tech.

## Setup

### Shared Tools (everyone gets these)

See [General Onboarding](onboarding-general.md#shared-tools-everyone-gets-these).

### Function-Specific Tools

| Tool | Purpose | Access |
|------|---------|--------|
| Datadog | Monitoring, alerting, APM | Request access from your EM (Marco) |
| PagerDuty | On-call rotation and incident management | Added by EM after first month |
| AWS Console | Infrastructure (read access initially) | Request from EM |
| Make.com | Low-code automation scenarios used by Operations | Request access if you'll touch ops scenarios (see scenario IDs in CLAUDE.md) |

### Repos

| Repo | Why |
|------|-----|
| `finn-auto/team-os-example-repo` | PRDs, plans, RFCs, bug investigations — design context |
| `finn-auto/<buyer-portal>` | Buyer / dealer portal codebase |
| `finn-auto/<supplier-portal>` | Supplier (RaaS) portal codebase |
| `finn-auto/<operations-tools>` | Internal ops tooling (compound, transport, document handling) |

(Exact repo names — confirm with Marco. Tracked here once stabilized.)

### Environment Setup

1. Complete [General Onboarding](onboarding-general.md) setup first
2. Clone the repos relevant to your starter project
3. Follow the `CONTRIBUTING.md` in each repo for local dev setup
4. Run the test suite locally and verify it passes
5. Bookmark the Datadog dashboards relevant to your service
6. Get added to the on-call rotation after your first month

## Key Documents

- [Engineering CLAUDE.md](../../product-development/engineering/CLAUDE.md) — plans / RFCs / bug-investigations layout
- [Product CLAUDE.md](../../product-development/product/CLAUDE.md) — pillars and terminology
- [Product Context](../../product-development/product/product-context/CLAUDE.md) — domain reference (pricing, GHG, compound flow)
- [Active PRDs](../../product-development/product/PRDs/CLAUDE.md)

## Slack Channels

| Channel | Purpose |
|---------|---------|
| `#rem_tech_general` | Team-wide announcements |
| `#rem_tech_internal` | Internal engineering / product / ops discussion |

Plus broader FINN engineering channels — your EM will add you.

## People to Meet

| Person | Why |
|--------|-----|
| Marco Milovanovic | EM — team structure, sprint process, growth plan |
| Ana Costa | Eng peer |
| Yahia Ragab | Eng peer |
| Fabian Röckel | Eng peer — automation & AI focus |
| Davi Lopes Mezencio | Eng peer — joined May 2026, fresh onboarding context |
| Iryna Lysenko | Design partner |
| Mario Schiefer | PM — product priorities, what to ship next |

## First Tasks

- [ ] Get local dev environment running and tests passing for at least one service
- [ ] Read 2–3 recent RFCs / engineering plans to understand current architecture decisions
- [ ] Review 2–3 recent PRs to learn code review norms
- [ ] Meet with Marco for an architecture walk-through
- [ ] Pick up a starter ticket from Jira `FRT` (Marco will assign one)
- [ ] Shadow an on-call shift after your first month
