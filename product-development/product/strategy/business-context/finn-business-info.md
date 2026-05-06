# Business Information - FINN GmbH

## Company Overview

**Company Name:** FINN GmbH
**Industry:** Automotive / Mobility / B2B SaaS
**Stage:** Series C
**Primary Goal:** Reach profitability by end of 2026
**Website:** finn.auto

---

## Planning Cycles

FINN plans in 4-month cycles called **Tashas** (T1, T2, T3):
- T1: January - April 2026 (completed)
- T2: May - August 2026 (current)
- T3: September - December 2026

---

## Products (Remarketing Domain)

Mario joined the remarketing department in July 2024. The domain covers the full defleet-to-sale cycle for cars coming off FINN's subscription fleet, plus cars from third-party suppliers (RaaS).

### 1. Remarketing as a Service (RAS) — primary growth driver
FINN sells cars on behalf of external OEM suppliers (Nissan, Renault, Stellantis, MG, etc.) through its B2B marketplace. OEMs have tiny internal remarketing teams (e.g. Nissan: 1.5 people for 15,000 cars/year; MG: 1 person for 10,000 cars) and rely on FINN's infrastructure. Launched T1 2025.

**Negotiation flow:** Supplier sets target price. If buyer bids at/above target, remarketing manager can sell without approval. If below, supplier sees the bid (anonymized), can accept/counter/decline.

### 2. Presales (internal FINN fleet — primarily BMW)
FINN sells BMW production slots to dealers before ordering from BMW. Dealer configures the car. After production, car goes into a 6 or 12-month subscription, then dealer receives it. ~80-90% of presales are BMWs. ~3,500 cars sold YTD. Big push each Oct-Dec for following year's production. Requires credit insurance per partner (sometimes a bottleneck).

### 3. Buyback agreements
Contractual commitments with OEMs (Stellantis, Renault, Nissan) where FINN agrees to buy back cars at a set residual value. FINN is pivoting from this toward RAS (sell on behalf of OEMs rather than buy from them).

**Invoicing complexity:** ~80% of invoices are for buyback cars. Two-invoice flow: first invoice issued immediately, second after appraisal (~3 weeks later). Ownership of buyback invoicing has been handed to the supply tech team.

### 4. Total damages
~1-2% of fleet are total damages; sold via partners (Copart, Schuster). Small revenue line, tracked in overall gross profit.

### 5. Buyer Portal (Dealer Product)
B2B used car marketplace for dealerships across Europe. Dealers register, bid on cars, purchase vehicles, handle after-sales (claims, invoice requests, documentation). Currently running on Retool (being replaced). ~230-300 MAU.

---

## Supplier Pipeline

| Supplier | Status | Notes |
|----------|--------|-------|
| Nissan | Active | ~5,500 cars; primary active supply |
| Stellantis | Hot pipeline — close within T2 | 6-8 brands; considered "rather safe" |
| Renault | Pipeline — "rather safe" | |
| MG | Early stage | |

Goal: 3+ committed suppliers with written commitments by end of T2.

---

## Org Structure (Remarketing)

| Person | Role | Notes |
|--------|------|-------|
| Bernhard Metzger | VP Remarketing | Overall oversight |
| Philip Schneider | Sales & Business Development | Focuses on sales and general BD |
| Thomas, Maximilian Retzmann, Jonathan + 1 joining | Remarketing Managers (5-6 total) | All remote; handle sales, touch points with dealers |
| Tim Hartdegen | Supply | Responsible for securing new supply relationships |
| Annalisa | Supply Operations | New; currently more operational, expanding scope |
| Niklas Bier | Operations Manager | Handles post-sale processing: POA, delivery, claims |
| Lucy Mueller | Agentic Sales Ops | Runs agentic outreach process and email campaigns |
| Fabio | De-fleeting cycle tracking | Building de-fleeting cycle time transparency tooling |
| Daria | Designer (UX scoping) | Scoping new buyer portal; shared across teams |
| Iryna Lysenko | Designer (UX/UI) | Shared designer; works on checkout and sign contract |
| David Burgschwaiger | Data Analyst | Remote from France; feeds into data warehouse |
| Victor Franz | BI | Sales tracking, BI tooling |
| Natalie | BI | Joined ~T1 2026 |
| Mario Schiefer | PM | Owns: Buyer Portal, Supplier Portal (RAS), Internal Sales Tooling |
| Davi Lopes Mezencio | Backend Engineer | Joined May 2026; Node.js |

---

## Key Metrics

**North Star:** Gross Profit = (gross profit per car + additional services gross profit) x cars sold
- **Gross profit per car:** ~€500 target (running ~€650-700; likely re-forecasting to ~€600)
- **Additional services (e.g. transport):** charge ~€250, cost ~€170, ~€80 upside
- **Cars sold** = MAU x bids per MAU per car x conversion rate x available supply

**Operational metric:** De-fleeting cycle time (days from ready-to-process to sale)
- Current: 63 days (last 30-day average)
- T2 target: 21 days
- Industry benchmark: BCA/AutoOne 1-2 weeks; OEM direct 2-3 weeks

**Health metrics:** Sales-to-opportunity ratio, customer satisfaction (dealer NPS), dealer touch points (personal + automated), internal tooling efficiency

---

## Tools

| Tool | Purpose |
|------|---------|
| Jira (FRT project) | Project management (Fleet Remarketing Tech) |
| Amplitude | Event tracking (API calls logged here) |
| Confluence (finn.atlassian.net/wiki/spaces/FP) | Documentation (Remarketing Tech space) |
| Slack | Communication |
| Granola | Meeting transcription |
| HubSpot | Activity and meeting tracking |
| Postgres | Operational DB + remarketing DB |
| Data warehouse + DBT | Consolidates Postgres, Amplitude, HubSpot |
| Looker | BI (being phased out company-wide — "the worst BI tool out there") |
| Retool | Current buyer portal UI (being replaced) |

---

**Owner:** Mario Schiefer
**Last Updated:** 2026-05-06
