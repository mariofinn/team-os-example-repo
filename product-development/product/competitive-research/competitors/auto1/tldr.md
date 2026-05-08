# Auto1 — TL;DR

**Slug:** `auto1`
**Website:** [auto1.com](https://www.auto1.com/) · [auto1-group.com](https://www.auto1-group.com/)
**HQ:** Berlin · **Founded:** 2012
**Last reviewed:** 2026-05-08

---

## What they do

Pan-European wholesale platform that buys used cars from dealers and fleet sellers, then resells them to other dealers across Europe. Auto1 acts as the **sole contractual buyer**: after an auction closes, Auto1 itself purchases the vehicle from the supplier, then resells onward to the winning dealer-buyer. The supplier never deals with the end-buyer.

Their parent company (Auto1 Group) also runs Autohero (D2C used cars) and Auto1 FT (dealer financing).

## Focus segments

| Supplier archetype | Fit |
|--------------------|-----|
| OEMs (RaaS) | Medium — they bid on OEM contracts but the buy-and-resell model can clash with OEM brand-protection asks |
| Banks / leasing | High — bulk volume, guaranteed offtake fits leasing de-fleet cycles |
| Dealers | Highest — original ICP, dealer-app first |

## Geographies

Pan-European footprint with reconditioning centres outside Germany. They emphasise cross-border arbitrage as a price-maximisation lever.

## Differentiators (stated)

- **Single-buyer model:** Auto1 itself buys the car → no payment-default risk for seller, no buyer-comms work for seller, payment is fast.
- **Self-evaluation app:** Dealer-side mobile flow that evaluates and uploads a car in ~15 minutes.
- **API for bulk partners:** Larger sellers can stream inventory directly from their DMS into the Auto1 platform.
- **Price Indicator:** Instant market-based price estimate for trade-ins.
- **Remarketing Dashboard:** Real-time auction monitoring (bids, buyer interest, status), report downloads.
- **Counter-offer negotiation:** Anonymous counter-offer to the highest bidder when the top bid is below the seller's minimum price.
- **Reconditioning capacity:** Production centres outside Germany.

## Pricing model

Marketplace-style fees on both sides. Seller-side fees are low (mobile evaluation €29, optional pickup €149). Buyer-side fees do the heavy lifting: car handling €289, document handling €119/€159, auction fees up to €1,950. Full breakdown in [`pricing.md`](pricing.md).

## How FINN compares

| Dimension | Auto1 | FINN Remarketing |
|-----------|-------|------------------|
| Model | Buy-and-resell (Auto1 owns the car) | RaaS — supplier retains ownership |
| OEM brand-protection | Limited (open marketplace once Auto1 owns) | Strong — supplier controls channel |
| Scale of buyer base | Pan-European, large | DACH-focused dealer network, growing |
| Reconditioning | In-house | Outsourced compound partners |

## Strengths to be aware of

- Scale of buyer demand and cross-border arbitrage
- Mature self-service tooling (app, API, dashboard, counter-offer)
- Single-buyer model is genuinely simple for the seller

## Weaknesses / opportunities for FINN

- Buy-and-resell model is structurally misaligned with OEMs that want brand protection and channel control (validated in supplier discovery — see `../../../customers/research/supplier-pain-points.md`)
- Christoph (Nissan) considered Auto1 in their 2024 tender and explicitly said *"Auto1 is not a serious competitor in this market"* for the OEM segment
- They don't run a closed-network / dealer-pre-sale flow as cleanly as BCA or a true RaaS player
