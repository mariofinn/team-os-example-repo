# AUTOproff — TL;DR

**Slug:** `autoproff`
**Website:** [autoproff.com](https://www.autoproff.com/)
**HQ:** Denmark · **Founded:** 2013
**Owner:** AutoScout24 (majority stake, acquired August 2022)
**Last reviewed:** 2026-05-08

---

## What they do

Pan-European digital B2B used-car auction platform for professional dealers. Sellers list trade-ins, fleet vehicles, and retail-ready cars; buyers (10,000+ active dealers, 43,000+ reachable) bid through a mobile-first auction flow with integrated services on top: on-site appraisal, wholesale-price advice, guaranteed minimum prices, escrow payments, and transport.

Sits structurally close to CarOnSale (dealer-to-dealer marketplace) but with a Nordic origin and pan-European footprint, and with **AutoScout24's distribution + brand backing** since the 2022 acquisition.

## Focus segments

| Supplier archetype | Fit |
|--------------------|-----|
| OEMs (RaaS) | Medium — capable, but not the headline ICP |
| Banks / leasing | High — fleet de-fleet flows are an explicit use case |
| Dealers | **Highest** — the platform's original ICP, mobile-first dealer UX |

## Geographies

Active in: **Denmark, Sweden, Norway, Germany, Netherlands, Belgium, Italy, Slovenia, Poland, Austria** — ~10 countries. Strong Nordic base; meaningful but not dominant DE presence.

## Scale

- ~120,000–130,000 cars / year sold
- ~10,000 active selling + buying customers
- ~43,000 dealers reachable via the network
- 3,000+ used cars available daily

## Differentiators

- **AutoScout24 integration / lift:** Since the 2022 acquisition, AUTOproff plugs into AS24's pan-European dealer reach. AS24 brings distribution and brand trust; AUTOproff brings the auction stack. This is a real moat for buyer-side density.
- **Modern dealer mobile app:** Mobile-first listing creation flow; rated highly in dealer-press coverage.
- **On-site appraisal service:** Wholesale price advice + condition reports built into the seller flow (similar pattern to CarOnSale, BCA).
- **Guaranteed minimum prices:** Dealer-friendly risk mitigation on trade-ins.
- **Escrow trading:** Secure payment release pattern (similar to COSPay).
- **Integrated transport** as part of the platform service.
- **Subscription model with unlimited users:** Reported flat-rate pricing per dealership (~€1,000/dealership flat-rate referenced in 2020 coverage; current pricing region-specific and gated to sales).

## Pricing model

- Subscription / flat-rate per dealership rather than purely per-transaction (notable contrast to CarOnSale's flat €119/sale or BCA's % auction fee).
- Region-specific pricing — published only via sales contact / authenticated app.
- Specifics in [`pricing.md`](pricing.md).

## How FINN compares

| Dimension | AUTOproff | FINN Remarketing |
|-----------|-----------|------------------|
| Model | Dealer-to-dealer marketplace + integrated services | Supplier RaaS + B2B buyer side |
| Owner / parent | AutoScout24 (mass-reach distribution) | Standalone |
| Geographic footprint | ~10 EU countries | DACH-first |
| OEM RaaS depth | Limited | Core focus |
| Buyer network density | High (43,000 dealers via AS24) | Building |

## Strengths to be aware of

- **MG's Stefan already uses AUTOproff** as part of his current workflow ("Stefan manually exports CSV from Salesforce to AutoProf for every batch" — see [supplier-pain-points.md](../../../customers/research/supplier-pain-points.md)). Existing tool footprint at supplier compounds is a switching cost.
- AutoScout24 owns the largest pan-EU consumer car portal — combining that with a B2B auction stack is a serious distribution advantage on the buyer side.
- Subscription model is sticky once dealers are onboarded.
- Pre-sale window — MG is launching a pre-sale model with AUTOproff (3–4 months before physical return) — this is a distribution channel competitors haven't matched.

## Weaknesses / opportunities for FINN

- **Stefan's workflow is the wedge:** he's actively trying to remove himself from the manual Salesforce → AUTOproff CSV step. A FINN integration that eliminates this step is a concrete value prop, not a hypothetical one.
- AUTOproff's strength is breadth (dealer reach), not depth (operational integration). FINN's compound + transport + document handling stack is something AUTOproff doesn't run. For OEMs that need a managed operator (Nissan, Renault), AUTOproff alone is not enough — they pair with DEKRA or similar. FINN can be the managed operator that *also* connects to dealer-reach networks like AUTOproff (or replaces them where the OEM consolidates spend).
- Subscription pricing locks dealers in but creates a price-per-active-listing comparison challenge. Useful angle in pricing conversations.
- Auctioneer-only model means OEM brand controls (closed networks, dealer-quota routing) need to be configured per deal — not native to the product.

## Sources

- [AUTOproff homepage](https://www.autoproff.com/)
- [AUTOproff Pricing portal](https://www.autoproff.com/prices)
- [AutoScout24 acquires majority stake in AUTOproff (Autovista24)](https://autovista24.autovistagroup.com/news/autoscout24-expands-portfolio-majority-stake-automotive-business/)
- [AUTOproff acquisition coverage (Mainsights)](https://www.mainsights.io/ma-news/danish-car-dealer-platform-autoproff-acquired-by-german-autoscout24)
- [AUTOproff feature overview (Pixelconcept)](https://www.pixelconcept.de/en/autoproff-online-car-auctions/)
