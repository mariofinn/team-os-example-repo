# Supplier Discovery Research Synthesis
**Date:** 2026-03-17
**Interviews:** 3 supplier interviews — Nissan x2, Renault x1
**Strategic Context:** T1 2026 OKR — Launch RaaS Supplier Product, 100 cars processed by EOT1
**Synthesized by:** Mario Schiefer
**Sources:** Full transcripts read for all 3 meetings (Granola)

---

## Executive Summary

**Top 3 Insights:**
1. **Pricing is the primary volume blocker — not process, not availability.** Christoph (Nissan) said it plainly: "I could give you 100 cars tomorrow. The bottleneck is purely pricing and sell-through speed." Fixing the process makes scaling possible; it won't unlock volume by itself.
2. **The shared-list idea came from the supplier, not from FINN.** Christoph proposed it himself — a shared SharePoint where DEKRA manages inventory, FINN marks interest and counter-offers, and he only approves exceptions. This is the minimum viable product for Nissan.
3. **OEMs choose and keep service partners based on proactivity and reliability, not price.** Christoph switched from BCA (25-year partner) to DEKRA because of professionalism, reporting quality, and speed — procurement cared about price, he didn't. FINN needs to internalize this.

**Product priorities based on research:**
1. Real-time vehicle status and blocking transparency (active pain, Nissan named a specific incident)
2. Structured price request / approval flow (primary volume unlock)
3. Regional buyer destination visibility (Nissan requirement — not a hard block, but a genuine ask)
4. Market price data sharing — aggregated Mobile.de benchmarks (Nissan explicitly requested; Renault interested in cross-border pricing intelligence)

---

## Sample

| Interview | Date | Participants | Notes |
|-----------|------|-------------|-------|
| Nissan x FINN v1 | Jan 30, 2026 | Christoph Grossfengels (Nissan), Henrik Sachs1 (DEKRA) | Full transcript read |
| Finn/Nissan Follow-up | Feb 4, 2026 | Christoph Grossfengels, Nadja Schmidt (Nissan, day 5 in role) | Full transcript read |
| FINN x Renault Produkt Interview | Feb 19, 2026 | Kirsten Güther (Renault Deutschland AG, 7 years in role) | Full transcript read |

**Sample notes:**
- Both OEMs are existing FINN relationships — findings likely skew positive vs. a cold prospect
- Both use DEKRA for compound/inspections — no OEM without DEKRA yet in sample
- Missing archetypes: banks/leasing companies, OEMs not yet using FINN, dealerships

---

## Theme 1: Process Is Built on Excel and Email — Painful at Scale, Manageable Today
**Frequency:** 3/3
**Severity:** Medium now, High at scale

Christoph is used to Excel and email. He said so directly: "Ich bin's halt gewohnt, dass wir halt Excel und E-Mail machen aufgrund von unserem Konzern." At current FINN volumes, it works. What he doesn't want is for it to stay this way as volume grows: "wenn ihr tatsächlich jetzt bei dreißig, vierzig, fünfzig Autos ankommen, ist das glaub ich einfacher für beide Seiten."

The shared-list idea was his own proposal — unprompted. He described it in detail: SharePoint, ~50-60 cars at a time, DEKRA fills and replenishes, FINN marks interest and counters, he approves exceptions only. DEKRA issues POAs from the list. "Sobald der Preis passt, wird direkt fakturiert, ohne mein Zutun."

Renault's situation is structurally similar. FCM has a price suggestion feature that "funktioniert noch nicht so rein" — so Kirsten still sends minimum prices to BCA via Excel manually. This workaround has been in place for 3 years and nobody has fixed it because other markets are now rolling out FCM and there's no spare capacity. The workaround creates time costs and error sources.

**Job-to-be-done:**
When I'm managing vehicles for multiple buyers, I want one place where the current status of every car is visible to everyone who needs it — so I don't lose deals to email threads nobody reads and cars don't sit reserved for buyers who've lost interest.

**Open questions:**
- [ ] Can FINN integrate with UWMS/Lineos (Nissan/DEKRA) or FCM (Renault/BCA) via API, or is upload/download the realistic path?
- [ ] Who at DEKRA would be the one maintaining the live list on their side?

---

## Theme 2: Vehicle Blocking Without Visibility Is an Active Problem
**Frequency:** 2/3 (Nissan Follow-up; implied in Renault FCM gaps)
**Severity:** High — Christoph named a specific, recurring incident

Christoph described the problem precisely: "Es kam jetzt in der Vergangenheit mal vor, dass viele Fahrzeuge für euch geblockt schon seit Ewigkeiten. Und die hat vielleicht auf eurer Seite keiner mehr aufm Schirm? Und wenn ich da irgendwann mal nachfrage, heißt es, ja, die brauchen wir gar nicht mehr. Die hätten wir vielleicht in der ganzen Zeit schon verkaufen können."

This is not theoretical. Cars are currently getting stuck in blocked status because neither side has live visibility into what the other is doing with them.

Renault has a related version of this problem: Kirsten cannot see FINN fleet vehicles in FCM until they have completed the full return process (appraisal, invoice, documents). There is no early visibility for pre-selling or reserving cars in advance. Any fix would require something to be "programmiert" in FCM.

**Recommended solution:** Per-vehicle status field (reserved, available, price requested, approved, sold, released) with timestamps. This is the most concrete, non-controversial feature across all interviews.

---

## Theme 3: Pricing Is the Primary Volume Bottleneck
**Frequency:** 3/3
**Severity:** High — explicitly stated as the single biggest constraint by Christoph

Christoph: "von mir aus geborene ich euch ab morgen jeden Tag hundert Autos. Ist nicht das Problem. Es ist halt eher das Problem, dass ihr die wahrscheinlich alle nicht verkauft bekommt... tatsächlich eher son Pricing Thema."

**Nissan pricing chain:**
- Target prices set from residual values (book values)
- DEKRA sends standard Excel template with RV to Christoph
- Christoph approves by email
- Large deviations → Finance Director involved

**Discount logic Christoph uses:**
1. Volume (package size)
2. Days on lot — cars at 3-4 months get much more flexibility than fresh arrivals
3. Model marketability — hard-to-sell models get easier discounts

**Renault pricing:**
- Works entirely in residual value percentages, never EUR
- Base: YTD historical benchmark
- Age adjustment: -1.5% RV per 3 months
- Adjustments for km and damage
- Does a "Kontrollisation" — a normalized/clean comparison price for each vehicle

**Market data interest:**
Christoph uses Autobiz (Neptune, part of Stellantis group) but lacks time to analyze raw data. He explicitly asked for FINN's Mobile.de aggregate pricing — ready-to-use market analysis would be a strong value-add: "Definitive." Kirsten is interested in cross-border pricing intelligence — knowing where specific models fetch better prices in different markets (e.g., used EVs in Denmark), so she can route vehicles to the right channel via Auto1.

---

## Theme 4: OEMs Value Proactivity and Reliability Above All — Not Price
**Frequency:** 2/3 (Nissan v1, Renault)
**Severity:** Foundational — determines whether relationships deepen or stall

Christoph chose DEKRA over BCA (25-year partner) on these grounds. Procurement cared about price; he cared about: professionalism, reporting quality, speed, and process stability. What specifically impressed him: "Proaktivität. Wenn jemand ein Problem sieht, das behiebt und das ist vielleicht nicht mal erwähnt." And: "aussagekräftige Reportings, dass ich intern schnell weiterteilen kann."

DEKRA's value proposition also goes well beyond selling cars — it covers the entire defleeting process. That's what won the tender.

Kirsten's take on the pilot: "Ich finde immer so grad, wenn man son Projekt startet, find ich immer wichtig, wenn man sich austauscht und sagt, wo sind die Stellschrauben? Was läuft gut? Was läuft falsch?" Close communication at launch is table stakes for her.

**What FINN needs to be:** The service layer that anticipates problems, communicates proactively, and makes the OEM feel like things are handled. The portal is a means to that end, not the end itself.

---

## Theme 5: OEMs Won't Change Their Physical Operations — FINN Connects Into Them
**Frequency:** 3/3
**Severity:** High — non-negotiable precondition

**Nissan:** DEKRA manages everything physical (Hapitec/CAT for logistics, compound operations). POA via Happy Tech/Hapitec. Process works. "Operativ mach ich gar nix."

**Renault:** All vehicles must flow through BLG Duisburg. DEKRA inspections required. Skipping duplicate inspections is possible in future but only after pilot experience and with Finance sign-off. Not a launch feature.

**Key insight:** DEKRA operates as the physical backbone for both OEMs. An integration with DEKRA would be disproportionately valuable. FINN should explore whether DEKRA has an API or data feed.

---

## Theme 6: Buyer Destination Transparency — Nissan Requires It, Renault Has Partial Visibility
**Frequency:** 2/3
**Severity:** Medium — a genuine Nissan requirement, softer for Renault

**Nissan (corrected from earlier version):**
No dealer quota obligations for GW — Christoph can sell to anyone. BUT he requires regional transparency on where cars go. The specific risk: a freelance dealer buying cheap Nissan cars via FINN and undercutting a neighboring official Nissan dealer in Germany. He wants to know when this might happen. "Wenn ihr das macht, dass wir da vielleicht bisschen Transparenz haben, dass ihr mir zumindest sagt, ja, ne, die Fahrzeuge sind schwierig im Ausland." He is not blocking such sales — he just wants visibility to manage internally: "wie gesagt, jeder darf jeder kaufen."

**Renault:**
Kirsten knows German franchise dealer buyers by name. She does NOT know foreign buyer identities — BCA GDPR restrictions. ~90% sales go to franchise dealers via JGW incentive system. ~10% independent trade. No visibility on international dealer status.

**Recommendation:** Light buyer visibility feature at launch — buyer country and buyer type (franchise dealer / independent trader). Sufficient for Nissan. Validate Renault's exact needs before building anything stricter.

---

## Theme 7: Reporting Is Important for Internal OEM Communication
**Frequency:** 2/3 (Nissan detailed, Renault secondary)
**Severity:** Medium

Christoph gets a daily PDF from DEKRA with: sales vs. target, inventory split (sellable/in-prep), top buyer ranking, returns analysis, days-on-lot, buyer count. He shares this internally and says: "wenn Du halt täglich Reporting hast, wo alle wichtigen draufstehen, dass Du's halt einfach relativ zeitnah teilen kannst."

Renault is building per-dealer dashboards for the new JGW incentive system. Kirsten tracks monthly dealer target fulfillment internally.

Neither is requesting this from FINN today, but it signals what belongs in a supplier dashboard eventually.

---

## Contradictions

**Urgency of the process problem:**
Christoph says current volumes are manageable with email/Excel. Kirsten's FCM workaround has persisted for 3 years without being fixed. The pain is real but both parties have adapted. The shared list / platform is a strategic investment for FINN, not an acute rescue.

**Automation vs. control:**
Both OEMs want faster processes but won't give up approval control. Christoph: "Im besten Fall kommen wir natürlich nie dahin [Finance Director escalation], aber wenn wir halt deutlich unter diese Preise sind, dann muss ich Finanzdirektor mit ins Boot holen." Kirsten's Finance team monitors every payment before release. Build for fast approval flows, never remove the OEM's sign-off.

**Pilot timing (Renault):**
Kirsten corrected the framing in the meeting — pre-marketing (showing vehicles to dealers, getting market feedback) starts March 1. Actual buying only happens after the contract is signed. These are different things. Don't conflate them.

---

## Missing Voices (Research Gaps)

Interviewed so far: 2 German OEMs (Nissan, Renault), both DEKRA-operated, both existing FINN relationships.

**Still missing:**
- Banks / leasing companies (different needs: process stability, bulk logistics, guaranteed capacity — per competitive research)
- OEM without DEKRA in their stack
- A supplier not yet in FINN's network (unbiased sample)
- Fleet operators (corporate fleets, different return cycles)

Recommendation: Next 2 interviews should target a bank/leasing company and ideally one non-FINN supplier.

---

## Strategic Fit (T1 2026 OKR)

Directly addresses: *"Conduct 5 supplier discovery interviews to surface top pain points and define the value proposition."*

**Top pain points confirmed:**
1. No shared real-time vehicle status → blocked cars, lost deals
2. Manual price negotiation → slows volume, doesn't scale
3. No proactive market data → Christoph pricing blind
4. No regional buyer visibility → Christoph managing risk manually

**Emerging value proposition:**
> For OEM suppliers already working with FINN as a buyer, FINN's Supplier Portal gives them a single place to manage vehicle availability, run price approvals with full market context, and track where their cars go — so they can move more volume without adding headcount or complexity.

---

## Next Steps

- [ ] `/prd-draft` — turn top 3 themes into the RaaS Supplier Product spec
- [ ] Schedule 2 more supplier interviews (bank/leasing archetype)
- [ ] Share Mobile.de aggregate pricing with Christoph — low effort, high goodwill
- [ ] Schedule product demo for Kirsten (she explicitly asked for 30-min walkthrough)
- [ ] Confirm Renault contract and March 1 pre-marketing timeline with Tim
- [ ] Explore DEKRA API/data feed — shared operational layer for both OEMs

---

## Appendix: Interview Sources

| Meeting | Granola ID | Date | Transcript |
|---------|------------|------|-----------|
| Nissan x FINN v1 | 1c83d4fb-d1a3-453f-84bd-c02ba42a606d | Jan 30, 2026 | Full transcript read |
| Finn/Nissan Follow-up | ded273d2-a26f-437f-a5f2-fe1e3ca743fe | Feb 4, 2026 | Full transcript read |
| FINN x Renault Produkt Interview | 0c72ff18-89c3-44ec-a275-aa6ed5211c00 | Feb 19, 2026 | Full transcript read |
