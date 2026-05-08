# Buyer Portal — Product Context
**Last updated:** Apr 27, 2026  
**Project:** Dealer Portal Refactoring (Retool → Pro-Code)  
**Designer:** Iryna Lysenko  
**Engineering:** Remarketing Tech team  
**Target subdomain:** remarketing.finn.com

---

## What We're Building

Replacing the existing Retool-based buyer portal with a pro-code, modern environment. V1 replicates current functionality. V2+ extends with new UX patterns, experimentation, and expanded features.

**Live portal:** https://partners.one.finn.auto/app/offers  
**V1 Prototype:** https://finn-partners.lovable.app

---

## Competitors

| Competitor | Notes | Access |
|---|---|---|
| AutoProff | Strong market presence, listing-only visible | No account |
| CarOnSale | Most innovative UX, fastest market share growth | 1Password |
| Auto1 | Older UX | 1Password |
| BCA | Oldest/most traditional, currently largest by market share | 1Password |
| OEM channels | Sell via telemarketing and email lists — no digital portal | N/A |

---

## Customer Profile

B2B dealers and dealer groups buying end-of-subscription FINN cars (used car remarketing). Most are professional car buyers who know vehicle specs by heart — they don't need hand-holding, they need speed and clarity.

**Group dealers** (~10+ subsidiaries) have additional complexity: they buy in bulk and must allocate cars to specific locations before delivery.

---

## FINN USPs vs Competitors

1. **Offer/counteroffer model** — most competitors use auctions (highest bid wins, no negotiation). FINN lets dealers negotiate without auction uncertainty.
2. **Bundle sales** — can purchase 4+ cars as a package, unavailable at auction platforms
3. **Dedicated account management** — every partner has a personal remarketing manager (goal: reduce FTE contact required over time)
4. **Pre-sales** — FINN sells cars before return (future delivery date), governed by condition deviation contracts. Most competitors only sell stock.
5. **Data transparency** — full configuration + appraisal files accessible. Most competitors don't have complete appraisals because their cars don't come from a controlled subscription.

---

## Core Functionality (V1 Scope)

### Offers (Discovery + Purchasing)
**Discovery:**
- Filter and sort the vehicle catalog
- Mark cars as favorites
- Add to cart (new — not in Retool today)
- Access key documents on PDP (configuration PDF, damage history, service history)
- Download Excel export

**Purchasing:**
- Place bids (single and bulk)
- Buy now
- See and respond to counter offers
- Bulk bid submission via cart

### Bidding Mechanics
- 95% of purchases start with a bid (not buy now)
- Bid flow: dealer bids → if below target, FINN forwards to supplier → supplier responds within 24h → FINN returns counteroffer to all interested buyers
- Counteroffer makes **buy now** the natural next action (accept or decline)
- Not an auction — dealers cannot see other bids
- End-to-end target: 24–48 hours
- Future v2+: separate Negotiations page for post-bid management (currently combined with Offers)

### My Cars
**Filters + sorting** (same as Offers, plus order ID filter — multiple cars often purchased under one order)

**Progress visibility:**
- Percentage = defleeting process completion (non-linear — most time is pre-return; urgency spikes once car is returned)
- Key customer anxiety: "Car is back from subscription — when do I actually get it?"
- Surface next actions contextually (e.g., "Invoice outstanding," "Export docs pending")

**Payments:**
- View open invoices + upcoming defleetings (organized by month)
- Download invoices
- Partners pay via bank transfer (no online payment)
- Primary use case: cash flow planning (e.g., ensuring BMW financing line covers upcoming defleets)
- No online payment planned for v1; future potential for in-portal batch payment

**Upload Actions:**
- **Export documents:** Required for partners exporting cars out of Germany to non-EU countries (VAT reclaim). Two PDFs required: CMR + Gelangensbestätigung. Usually batch uploaded (multiple cars on one truck). FINN defleeting team verifies → releases car papers. Car papers are withheld until confirmed.
- **Vehicle allocation:** For group dealers — assign purchased cars to specific subsidiaries (location). Blocks invoicing and delivery until complete. Filter: "pending allocations."

**Multi-car actions:**
- Download Excel
- Download car documents
- Copy VIN

### Delivery Selection
- 50% pick up themselves, 50% choose FINN delivery (~€250/car, adds a few days)
- Currently decided over phone — not in portal
- V1: out of scope
- Vision/future: add to checkout flow post-bid acceptance (ask at purchase confirmation)

### Production Slots (low priority — ~10 dealers)
Custom workflow for BMW/Mini dealers who buy production slots (right to submit configurations monthly). Cars are produced to spec, then invoiced after 6–12 month subscription. Highly custom flow; not a focus for v1.

### Global Settings
- Language selection
- Toggle between gross/net prices

---

## Key Pain Points (Current State)

1. **Defleeting cycle time** sits at ~7 weeks (industry standard: 2–3 weeks). Partners frustrated by slow delivery of car and papers after purchase.
2. **Limited process visibility** — partners don't know where a car is in the defleeting pipeline or when to expect delivery.
3. **Negotiation runs on Excel/phone** — bid management is manual, driven by dealer habit. Portal should reduce this friction over time.

---

## V2+ Roadmap Ideas (Not V1)
- Separate negotiations management page
- Checkout flow with delivery selection (pick up vs delivered)
- More My Cars functionality
- In-portal payment features
- Auction/visibility mode (exploratory — not decided)
- Export document status indicator on car card

---

## Design Principles for This Portal
- Business tool, not a marketing surface. Clarity > visual polish.
- Dealers are professionals — don't over-explain, give them speed and data.
- Most interactions involve multiple cars at once — bulk actions matter.
- Mobile less critical than desktop for this use case.
- Design full vision, then phase implementation. Engineers + Mario decide what ships in v1.

---

## Timeline
- Mid-June 2026: target for designs + EPR ready for engineering
- T2 second half (~July 2026): engineering implementation kickoff
- Designer check-ins: every 2–3 weeks
